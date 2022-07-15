# Strings (cadenas de texto)

### (MDN) Methods and properties:
<!-- Existe una pagina denominada Mozilla Development Network (MDN) la cual da información de la sintaxis y comandos de JS, de allí saqué la infomación que escribiré a continuación. -->


- String Properties; describe al objeto string según parámetros:

1. String.prototype (no la describo pero la dejo como 'vista').

2. String.length: representa el largo de una cadena en unidades de código UTF-16. 

- String Methods; permite la capacidad de acción al objeto string mediante comandos:
(pongo para dar ejemplos, no para desarrollar)

1. String.fromCharCode()
2. String.fromCodePoint()
3. String.prototype.concat()

Los methods tienen la diferencia de las propiedades que terminan con paréntesis, dentro de los cuales se escribirá el valor de la acción descrita a ejecutar.
-------------------------------------------------------------------------------------------------------------------------
### Strings o cadenas de texto:

Se pueden representar con comillas simples (') o dobles ("). Ejemplo:

let edad = '46'  /  let valor = "5pe"

<!-- Se puede usar el comando console.log para manifestar en la consola del navegador de la página. Ejemplo:
console.log(edad + valor) y lo que ocurrirá es que en la consola se nos mostrará la concatenación de los strings declarados anteriormene. 
También puedo hacer: console.log(edad,valor)
Esto no concatenará los strings pero los pondrá en el mismo renglón separados por comas.
Esto esta ejemplificado con strings pero se pueden hacer mas cosas con console.log() -->

Se puede usar la *manera simple* de declarar los strings como hicimos anteriormente (*let edad = "46"*) y tambien existe la forma para que el string cree otro (string) dentro de sí mismo. No se suele usar, pero se manifiesta de manera diferente en la consola a comparación de la simple mencionada y considero importante incluírla:

- La palabra reservada 'new' es usada para añadir un comando dentro del valor de la string.

let saludo = new String("Hola Mundo")

En este caso si insertamos lo siguiente estaremos haciendo que el string de nombre 'saludo' cree mediante el uso de 'new' otra string la cual contiene el valor (es decir el mensaje, la cadena de caracteres): "Hola Mundo".

- ¿Pero que tiene de distinto **let saludo = new String("Hola Mundo")**
de
*let saludo = "Hola Mundo"*?

La ultima se manifestará en el console.log() de la siguiente forma:

*Hola Mundo*

Mientras que la primera se verá::

**>String: {"Hola Mundo"}** (Es clickeable para desplegar mas información)

Y si la desplegamos dirá:

**\/String: {"Hola Mundo"}**
**- 0: "H"**
**- 1: "o"**
**- 2: "l"**
**- 3: "a"**
**- 4: " "**
**- 5: "M"**
**- 6: "u"**
**- 7: "n"**
**- 8: "d"**
**- 9: "o"**
**- length: 10**
**>__proto__: String**
**[[Primitive Value]]**

Esta acción hará que se vea así en la consola proporcionándonos detalles del string como la ubicación de cada caracter y el largo (length) de la string como mencionabamos en principio cuando hablabamos de las **propiedades de los strings**.

Y por que dice length: 10? Aclaro por las dudas el 0 siempre se cuenta en programación, al ser un caracter aparte se suma y se hacen 10. Y por supuesto los espacios también son caracteres.

Tambien le puedo ordenar a la consola que solo me de la cantidad de caracteres de un string (es decir el length) de la siguiene forma:

console.log(edad.length, valor.length, saludo.length)

|| || ||
\/ \/ \/

2, 3, 10

----------------------------------------------------------

También hablamos de los **methods de las strings**, por ejemplo una acción realizable en JS es que me devuelva el valor del string completamente en mayúsculas  o minúsculas. Para eso lo manifestaremos en la consola y para ello escribiremos:

- console.log(valor.toUpperCase (mayus), saludo.toLowerCase(lower) )

|| || ||
\/ \/ \/

5PE, hola mundo. 

Otro method es: 

**valordelstring.includes()**; Esto es útil para buscar si un string posee ciertos caracteres o cadena de caracteres en su valor, Ejemplo:

console.log(saludo.includes(Hola))

|| || ||  Consola dirá
\/ \/ \/

*true*
Porque dentro del string "saludo" se encuentra la palabra Hola.
De insertar una palabra que no se encuentra en el string el resultado será *false*