
## JavaScript

### Maneras de enlazar JS al código:

La mas recomendada es linkear un archivo JS externo como lo haríamos con CSS. La pequeña gran diferencia, es que el link
del archivo JS suele ir por conveniencia en el <body> y no en el <head> como el CSS.
Se tipea dentro del body: 
<script src= "dirección del archivo.js"></script>.

Las menos recomendadas son; ** --en línea, ej: 
 <!DOCTYPE html>
 <html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Johnny</title>
  </head>
  <body>
    <h1 onclick="alert('hola')">Lorem ipsum dolor sit amet.</h1>
    Parecido a como insertaríamos Css en una linea de codigo.

--Encerrando codigo html con el comando <script type="text/javascript">...</script>.
---------------------------------------------------------------------------------------------------------------------------------

Javascript se maneja con **variables**. Las variables son items con un nombre y un dato que contienen.
Tanto el nombre de la variante como el nombre del dato que contenga son escritos por el autor. No un comando predeterminado 
que requiera de una palabra clave.

Entonces al hacer scripts, siempre haremos uso de la variable citandola por su nombre, y lo que esta entregará será el/los 
dato/s que contenga.
--------------------------------------------------------------------------------------------------------------------------------
Ahora bien, existen varios tipos de datos:

* String (usado para texto, cualquier dato que sea string será tomado como texto). Otra característica de los strings es que se identifican por estar encerrados entre comillas.

* Number (usado para números, cualquier dato que sea number deberá contener únicamente números). __Este tipo de dato es válido para hacer operaciones matemáticas y no lleva comillas__.

En los number no se deben poner letras y en los string se pueden poner números. Pero hay que recordar que el string siempre debe tener las "..." porque de no ser así este dato será tomado como number.

Decimos que se usa number para las matematicas ya que, si por ejemplo tenemos:
number1= 15
number2= 20
Sumamos ambas variables: number1 + number2 y el resultado será = 35.

Ahora si hacemos que ambas variables sean string:
number1= "15"
number2= "20"
number1 + number2= "1520".

Es decir, lo que resulta de sumar el valor de un string a otro dato será añadir el contenido de dicha variable a otra.
Y de ser esta variable un string no interactuará matematicámente puesto a que es **texto**.

* Boolean: este tipo de variable solo reconoce los valores 0 / 1 o true / false. Solo se puede usar un tipo de valores, y poner
solo un resultado. Esto es true o es false, no ambas. ME ESCUCHASTE
Siendo entonces true o 1 un valor 'positivo', y false o 0 uno 'negativo'. Con booleanos se pueden armar muchas cosas.
--------------------------------------------------------------------------------------------------------------------------------

## Sabemos que es una variable y que tipos de datos usa. ¿Como 'declaramos' una variable y que es esto?

Declarar una variable es darle un valor. Una variable no declarada es una variable indefinida, por ende cualquier variable sin valor se la considerara como 'undefined'. Esto no es un error sino otro tipo de dato mas, conocido como 'vacío' 'sin valor'.
Pero declarar conlleva una sintaxis. Nosotros podemos declararla con: var, let y  const. Ejemplo:

1  var number = 50; let number 50; const number = 50
2
Tambien se pueden declarar en líneas separadas, aunque es mas rápido hacer lo anterior, esto puede dar mas especificidad:
1  var number;
2  number = 50;

Normalmente se utiliza let debido a que tiene un rango mas específico mientras que var tiene un rango mas global de alcance.

* Const es una constante. Es decir una variable que una vez decidido su valor no puede modificarse en un futuro, es cons-tante JA! Cualquier intento de modificación de la misma resultará en un error. Y **la unica forma de escribir una variable const es declarándola al momento de crearla**. Es decir, **no se puede declarar en lineas separadas como var o let.**

--------------------------------------------------------------------------------------------------------------------------------

## Valores null y undefined:

Sabemos que cuando una variable esta vacía esta está indefinida. Al estarlo resulta en errores o en la aparición de un 'undefined' como valor.
Pero este tipo de dato debe definirse en algun momento, no está 'hecho' para permanecer así. El tipo de valor que si está hecho
para definir una **variable** y al mismo tiempo decirle que **no tiene valor** es **null__**. Es decir, es un valor.. Y cual es?
No tenerlo intencionalmente.
--------------------------------------------------------------------------------------------------------------------------------

## Tipos de errores: undefined, NaN, etc:

Como mencionamos, una variable con valor 0 o vacío/nulo se llama null. Y una variable que no tiene valor y debe definirse resulta en error o undefined.
Pero también existen otras notificaciones de errores como **NaN**, acrónimo de **'Not a Number'** (no es un número). NaN ocurre por ejemplo, cuando hacemos operaciones matemáticas entre variables cuando sus contenidos o uno de ellos no es en su totalidad una cifra numérica. Pudiendo haber letras en los valores, al no ser válida la operación resultará en NaN.
--------------------------------------------------------------------------------------------------------------------------------

## Prompt:

Se usa para mostrar un cuadro de diálogo con un mensaje que solicita al usuario que ingrese algún texto o información. Se usa para muchas cosas, y dicha información queda almacenada en una variable la cual puede ser reutilizada en otras acciones.
Ej:

1  prompt(Que día es hoy?) 
2     ^acción        ^Mensaje de la acción, en este caso un cuadro de dialogo con la interrogante a ser respondida.

Al yo declarar en medio de la ejecución de código a esta variable se almacenará con la respuesta para ser utilizada.
Ahora prompt(Que día es hoy?) = miércoles.
--------------------------------------------------------------------------------------------------------------------------------

# #-# 

<!-- para hacer comentarios.

