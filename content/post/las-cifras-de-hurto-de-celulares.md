---
title: "Las cifras de hurto de celulares"
date: 2019-11-27T09:29:48-05:00
draft: false
image: pistola.png
---

No existe un repositorio definitivo y público con cifras sobre el comportamiento del hurto de celulares en Colombia. Por eso, para saber si el robo de celulares disminuyó desde que se creó la medida de registro de IMEI, esta investigación recurrió a solicitudes de información a la Comisión de Regulación de Comunicaciones (CRC) y la Policía Nacional. A través de Asomóvil se obtuvieron los datos de la empresa Informática El Corte Inglés, que fue contratada como administradora de las bases de datos centralizadas o administrativas (BDA).

De acuerdo con el diseño legal y regulatorio colombiano, los operadores de telefonía móvil deben contratar con un tercero la administración de las bases de datos que recogerían todos los IMEI a ser bloqueados (base de datos negativa) y todos los autorizados a funcionar (base de datos positiva). La empresa [Informática El Corte Inglés](https://www.iecisa.com/en/digital-transformation/) fue elegida como Administradora de las bases de datos comunes a todos los operadores pero responde sólo a la CRC y a los operadores. Por lo tanto la empresa no provee directamente datos de las bases de datos administrativas.

El primer hallazgo encontrado entre las tres distintas fuentes de información es que no hay coincidencia sobre los datos que reportan. Esta diferencia es más importante entre la información de la CRC y la de Informática El Corte Inglés (BDA) puesto que la segunda debe reportar los mismos datos a la primera.

Ya que la información de la BDA es el reporte del número de IMEI efectivamente bloqueados, usaremos esta fuente y no la de la CRC en lo que sigue.

## Base de datos centralizada o administrativa

La BDA recibe los IMEI de todos los operadores del país que están autorizados a funcionar (BDA positiva) y los que deben ser bloqueados por distintos motivos (BDA negativa)

### BDA Positiva

La información consignada en la BDA positiva no indica cuántos IMEI están autorizados a funcionar por mes y año en Colombia. Las cifras corresponden a los IMEI que se agregaron a la BDA positiva, por lo cual no es posible usar esta información para saber cuántos IMEI en 
total han sido activados y calcular así la proporción de IMEI robados.

{{< chart "uno.html" >}}

### BDA Negativa

Hay varias causales por las cuales el sistema de registro bloquea un IMEI. Vale la pena destacar acá 4 de ellas.

- __Hurto__: se bloquean los IMEI de celulares reportados al operador como robados. 
- __No registrados__: para obligar a las personas a registrar su celular en las bases positivas, se bloquean todos los IMEI que no hayan pasado por ese proceso.
- __No homologados__: la homologación es un procedimiento para asegurar que los celulares que se usan en el país cumplen con ciertos estándares y no pueden dañar la red o ser un peligro para las personas. El sistema de registro incluyó el bloqueo de los IMEI de celulares no homologados aún si esto no tiene que ver con el robo de celulares.
- __Sin tipo de reporte__: desde que inició la medida y hasta el 2016, se registraron celulares bajo la causal "sin tipo de reporte", por lo que no es posible diferenciar en esos casos si corresponden a robo o pérdida.

Se evidencia que los hurtos de celulares tienen una cantidad constante de casos por año (1 millón aproximadamente), lo que representaría a simple vista una nula disminución del hurto a celulares en este periodo de tiempo.

<!-- {{< chart "tabla_1.html" >}} -->

No obstante, se observa una tendencia creciente entre enero de 2015 y julio de 2017 que alcanza el valor máximo de la serie. Después de julio de 2017 el comportamiento parece estabilizarse alrededor de los 104,470 celulares robados por mes.

{{< chart "cinco.html" >}}

El comportamiento se puede describir como un sube y baja: si en un año subió respecto al anterior, en el siguiente baja y viceversa, sin embargo, no hay una diferencia significativa en las cifras. Este comportamiento sin relación en el tiempo se comprobó a través de una [evaluación estadística]({{< ref "metodologia.md" >}}).

Mientras que el hurto se mantiene estable, las causales de no registro y no homologados son siempre mayores a las de robo. Es decir, se han bloqueado más celulares porque las personas no registraron el IMEI o porque no pudieron realizar el proceso de homologación, que por los reportes por robo.

{{< chart "dos.html" >}}

Sin embargo, el reporte de la BDA Negativa puede representar un obstáculo para saber exactamente cuántos celulares son bloqueados por haber sido robados. Un celular con un IMEI que se reporta como robado y luego es reprogramado con un IMEI distinto podría aparecer nuevamente reportado, por ejemplo, como duplicado. En caso de que ambos reportes se conserven en las bases de datos el número total de celulares reportados en la BDA Negativa podría duplicarse.

## Datos de la Policía Nacional

La Policía Nacional registra las denuncias por robo de celulares desde 2003. La diferencia con la información de la BDA es que la Policía registra los casos en los que una persona se acerca a una autoridad para denunciar el delito. Por esta razón hay un subreporte y no todas las personas que llaman a su operador para bloquear su celular por robo se dirigen a la Policía para denunciar el hecho.

Las cifras de la Policía muestran una tendencia al aumento, no obstante, como son cifras de denuncias por hurto, pueden existir otros factores no propios del delito que sean la razón de este aumento, por ejemplo, mayor facilidad y disposición para hacer la denuncia.

{{< chart "tres.html" >}}

A pesar del subreporte las denuncias no tienden a disminuir o aumentar como en el caso del bloqueo por robo.

### Comparación entre bases de datos

Aprovechando que la Policía registró casos 8 años antes de que iniciara la medida de registro de IMEI, quisimos saber si el número de denuncias por robo de celulares se comporta de forma similar a los bloqueos en la BDA.

Encontramos que no hay una coincidencia clara entre las dos, lo que significa que cuando hay un aumento en las denuncias no hay necesariamente un aumento en los bloqueos y la información de la Policía no puede decir mucho sobre el número real de celulares robados en el país.

Sin embargo, la información de la Policía Nacional no cubre el 94.7% de los celulares reportados en la Base de Datos Negativa y por lo tanto se debe decir que no es posible una comparación entre bases de datos ya que el porcentaje de diferencia entre una y otra es de más del 90%.

Comparación casos de hurto de celulares de Policía Nacional y Base de Datos Administrativa negativa de 2013 a 2017.

{{< chart "seis.html" >}}

<!-- {{< chart "tabla_2.html" >}} -->

La información recopilada en este informe pone en evidencia que el hurto de teléfonos continúa sin que haya cambios significativos en las cifras o sin que se pueda contener la adaptabilidad de las conductas delictivas a los controles implementados, a pesar de que exista una Estrategia para contenerlas.
