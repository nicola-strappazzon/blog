+++
draft = false
title = 'Diodo emisor de luz (LED)'
+++

Los diodos LED es la forma más habitual de indicar estados en los circuitos electrónicos. Para que funcione un LED necesitamos que una corriente lo atraviese, la intensidad de esta corriente debe ser cuidadosamente calculada, dado que si excedemos los límites especificados en el datasheet, este se destruirá. La siguiente lista nos da una idea de la tensión aproximada que se necesita:

| Color    | Forward Voltage F{{<sub f>}} |
|----------|------------------------------|
| Rojo     | 1.8 - 2.1                    |
| Ámbar    | 2   - 2.2                    |
| Naranja  | 1.9 - 2.2                    |
| Amarillo | 1.9 - 2.2                    |
| Verde    | 2   - 3.1                    |
| Azul     | 3   - 3.7                    |

Generalmente, los valores están entre 10mA y 30mA, por lo general se usa un valor medio `20mA` (0,02A) con el cual se logra un buen brillo con una larga vida útil, mientras usemos los valores mínimos alargamos la vida del componente. La forma para limitar la corriente que circula por el LED es colocando una resistencia en serie antes o después del componente.

A continuación explicaremos cómo calcular los ohms y los watts necesarios para la resistencia que acompaña el LED.

> Recuerde consultar el datasheet para tener el valor exacto.

## Calcular el valor de la resistencia

El cálculo del valor de esta resistencia es muy simple, y solo implica el uso de la ley de ohm. Debemos restar la tensión de la fuente y tensión del LED, y dividir el resultado por la corriente que deseamos atraviese el componente. Si usamos las unidades correctas (tensiones en Volts y corrientes en Amperes), el resultado estará expresado en Ohms.

{{< svg name="formula01" style="width: 200px; padding: 4px; background-color: white;">}}

Supongamos que tenemos un LED de color rojo, que según su hoja de datos, necesita para funcionar correctamente una corriente de `18mA` y una tensión entre ánodo y cátodo de `1,9V`, y queremos alimentarlo con una batería de `9V` ¿Cuál será el valor de la resistencia limitadora?

Aplicando la fórmula anterior, obtenemos que:

{{< svg name="example01" style="width: 700px; padding: 4px; background-color: white;">}}

Como puede observar, el valor para la resistencia es `394,44Ohms`, y no existe una resistencia comercial de ese valor, utilizaremos el más cercano: `390Ohms`.

## Calcular la potencia limitadora de la resistencia

Además de hayar el valor en ohms, debemos saber el tamaño de la resistencia en valores comerciales, por lo que debemos calcular la potencia que debe disipar en forma de calor por si misma.

La potencia se calcula con la siguiente fórmula:

{{< svg name="formula02" style="width: 200px; padding: 4px; background-color: white;">}}

Aplicando la fórmula anterior, obtenemos que:

{{< svg name="example02" style="width: 850px; padding: 4px; background-color: white;">}}

> Debemos seleccionar siempre una resistencia con una potencia superior al cálculo para evitar que se queme.

Potencias comerciales:

- 1/8W=0,125W
- 1/4W=0,250W La más común.
- 1/2W=0,5W
- 1W
- 2W
- 3W
- 5W
- 7W
- 10W
- 15W

Puedes usar esta [calculadora](https://www.digikey.es/en/resources/conversion-calculators/conversion-calculator-led-series-resistor).

Fórmulas en LaTex:

- `R={\frac{{{V}_{s}}-{{V}_{f}}}{{I}_{f}}}=\frac{9v-1,9v}{0.018A}=\frac{7,1v}{18mA}=394,44\Omega`.
- `P=V\times I=\left(9v-1,9v\right)\times0.018A=0,1278W\sim127,8mW`.
