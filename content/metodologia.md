---
title: "Metodología"
date: 2019-11-27T09:37:24-05:00
draft: false
---

La información de este especial web está basada en la investigación “Ensayo y error: análisis de la efectividad del registro de celulares” de Fundación Karisma. En ese informe se analizan en detalle las cifras de hurto de celulares y se evidencia la falta de herramientas de monitoreo y evaluación en la política de registro de celulares en Colombia.

Para la realización de este especial se utilizaron distintas fuentes de información pública disponibles a través de la Comisión de Regulación de Comunicaciones, la Asociación de la Industria Móvil de Colombia y la Policía Nacional. 

Debido a la importancia que se le ha dado a esta medida por parte del Ministerio de las TIC y la Comisión de Regulación de Comunicaciones, no se cruza esta información con otras fuentes para probar la hipótesis oficial de disminución del hurto de celulares en Colombia. 

Vale aclarar que en esta investigación no se buscó explicar por qué se ha afectado el hurto de celulares, ni señalar responsables en el sector público o privado de ningún tipo de violación a la legislación o regulación sobre el tema. Se trata de constatar cuál ha sido la efectividad de la medida de registro de celulares en la reducción del hurto de acuerdo con la información disponible.

Para obtener la información se enviaron solicitudes de acceso a la información relacionada con la medida de registro. 

Como resultado de esas peticiones recibimos de parte de la Comisión de Regulación de Comunicaciones una base de datos con cifras desde 2012 hasta octubre de 2018 de IMEI reportados por las distintas causas establecidas en la regulación. A través de Asomóvil recibimos las cifras que se reportan en la Base de Datos Administrativa (positiva y negativa) por parte de Informática El Corte Inglés, por mes, año y causal del registro.

Y de parte de la Policía Nacional recibimos varias tablas con reportes de hurtos de celulares con información especifica del municipio y departamento del robo, datos de la víctima, del victimario y del celular robado. Aunque la Policía Nacional tiene un sitio web dispuesto para la [consulta de estadísticas delictivas](https://www.policia.gov.co/grupo-informacion-criminalidad/estadistica-delictiva) fue necesario solicitar la información sobre hurto de celulares porque a la fecha de la consulta no estaba disponible a través del sitio web.

Todas las visualizaciones de datos se realizaron con [Datasketch Apps](https://www.datasketch.co/aplicaciones/galeria).

## Evaluación estadística de la BDA negativa

Para la realización de la sección ["Las cifras de hurto"]({{< ref "/post/las-cifras-de-hurto-de-celulares.md" >}}) se tuvo que realizar una evaluación sobre la tendencia en la serie de tiempo de la Base de Datos Administrativa Negativa respecto al robo de celulares.

En términos estadísticos esto es probar si la serie de tiempo proviene de una caminata aleatoria. Es necesario entonces que la serie de tiempo sea estable, es decir, que la media y la varianza sean constantes en el tiempo. Para ello se realizan tres procedimientos:

- Se traslada la serie de tiempo para que tenga una media cero.
- Se evalúa si la serie es o no de varianza constante.
- Se evalúa si es necesario hacer alguna corrección para garantizar que la serie de tiempo sea de media constante.

A través del test de Barlett y la prueba de raíz unitario se encontró que era necesario aplicar la transformación de logaritmo natural para estabilizar la varianza y diferenciar la serie de tiempo para garantizar la media constante. 

Aplicadas dichas transformaciones y correcciones, se puede probar si la serie es o no una caminata aleatoria a través de un autocorrelograma que rechaza la hipótesis de que la serie sea una caminata aleatoria, y se concluye que existe una correlación del número de celulares robados de un mes con el número de celulares robados en el mes inmediatamente anterior. Sin embargo esta correlación existente es débil y se encuentra alrededor del -0.25. Lo que indica que no hay una diferencia significativa en las cifras de un mes a otro.

Este mismo procedimiento se realizó para la base de datos de hurtos de celulares entregada por la Policía Nacional.
