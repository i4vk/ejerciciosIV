# Introducción a la infraestructura virtual: concepto y soporte físico

## Ejercicio 1
**Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años. Consultar este artículo en [Infoautónomos sobre el tema](https://infoautonomos.eleconomista.es/consultas-a-la-comunidad/988/).**

El servidor que he elegido es el siguiente: https://www.pccomponentes.com/hp-proliant-ml30-gen10-intel-xeon-e-2134-16gb

El precio sin IVA de este servidor es de **833,88€**.  
Para amortizarlo, lo que debemos hacer es dividir el total del precio del servidor entre el número de años que se pretende ser usado.  
En este caso, para la amortización en 4 años, debemos dividir **833,88/4 = 208,47€**. Este será el valor de la amortización para 4 años.

Por otro lado, si realizamos esto mismo para una amortización en 7 años, el resultado será **833,88/7 = 119,1257€**


## Ejercicio 3
**En general, cualquier ordenador con menos de 5 o 6 años tendrá estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden? Si usas una máquina virtual, ¿qué resultado da? ¿Y en una Raspberry Pi o, si tienes acceso, el procesador del móvil?**

El modelo de mi procesador es un *Intel Core i5-8250U*. Si ejecutamos la orden "egrep '^flags.\*(vmx|svm)' /proc/cpuinfo", vemos cómo ciertamente, este procesador sí que tiene soporte para virtualización a nivel de hardware, como podemos observar en la siguiente captura de pantalla.

![](./capturas/cpuinfo)

Si el procesador no tuviera esta funcionalidad, entonces el resultado de ejecutar esta orden no nos mostraría ningún texto.
