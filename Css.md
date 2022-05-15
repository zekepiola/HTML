<!-- 
Estructura de css se conforma por un selector, {}, propiedad: y valor; 
Van de la siguiente manera:  selector {
                                    propiedad: valor;
}

El selector es aquello que elegimos para editar su estilo, puede ser un h1-h6, un <title>, un <header>,
<p>, <article>, <a img=...> y demás.

La propiedad sera aquél factor que modificaremos del selector, puede ser su altura (height), ancho (width),
sus bordes (border), su fuente (font), color (color), posición (position) y muchas cosas más.
En el caso del color, el valor del mismo deberá ser en hexadecimal para mayor compatibilidad con el navegador.

El valor es la cantidad en que el factor mencionado modificará al selector designado. Este puede medirse en 
numeros enteros ej: img width= 500px (le otorgamos 500 píxeles de ancho a la imagen) o 
img width= 50%  (le indicamos que la imagen tendrá un ancho del 50% de su totalidad).

Los enteros y los porcentajes se usan a conveniencia, para cuando un valor estático sirve en una plataforma 
pero no en otras, un valor porcentual que se pueda ajustar según la proporción de la interfaz sobre la que se
esté visualizando puede llegar a ser mas apta por su adaptabilidad. 

Existen varios tipos de 'prefijo' para el selector que otorga distintas funciones:

(*) Es un selector 'universal', al poner solo el asterisco estamos seleccionando todo lo que puede ser 
modificable por css en el archivo html.
------------------------------------------------------------------------------------------------------------------

('inserte aquí tag') Si nosotros solo ponemos h1, o <p> o <section> todos los tags denominados de esa forma
se verán modificados.
------------------------------------------------------------------------------------------------------------------

(.class='...') se hace uso del atributo 'class'. Al crear un class con un nombre, todas las etiquetas que posean
un class con dicho nombre se verán modificadas. La estructura sería la siguiente:
'.' 'nombre del class'{ propiedad: valor;}
Por ejemplo:

.ParrafosEncasillados2 {bordes: solid;}
Esto de parte de Css
y de parte de html:

<p class="ParrafosEncasillados2"> lorem ipsum bla bla bla bla bla bla bla bla bla bla </p>
<p> "...y así fué como conocí a tu padre (? ". </p>

Entonces con esta configuración, solo los parrafos (<p>) que poseen class= "ParrafosEncasillados2"
tendran bordes. 
------------------------------------------------------------------------------------------------------------------

Este próximo es parecido al '.class='. Comienza con # y le sigue un nombre. En html para usarlo se le agrega
el atributo 'id=' dentro del tag en el que lo van a usar. Id es 'identifier' del inglés identificador, da identidad
y por ende no es que se deba asignar a distintos elementos en simultáneo. Pero por sobretodo, este mal uso puede
interponers en el camino si usamos JavaScript por ejemplo.

Ej:
Visto desde Css:

'#...' {propiedad: valor;}
 #tortademanzana {alto: 100px;}

Visto desde Html:
(link para descarga de imagen https://recetatorta.com/wp-content/uploads/2020/10/Torta-de-manzana-invertida.jpg)

<a href="torta.jpg" id="tortademanzana">torta</a>
------------------------------------------------------------------------------------------------------------------

Por atributo, nosotros creamos un atributo y le damos un valor dentro de la misma línea de un tag para
que funcione. Dicho valor es parte del nombre del atributo y no da funcionalidad dentro del código. Cuando lo
usemos en Css encerraremos al atributo y su valor entre corchetes [] para que funcionen.

Ej: Visto desde CSS:
1
2  [header2=subrayado25px] {underline: ;}
3

Visto desde HTML:
10 <body>
11   <h2 header2=subrayado25px> texto aqui </h2>
12
------------------------------------------------------------------------------------------------------------------

Por descendencia, si ponemos un <p> dentro de un <h2> modificaremos todos los elementos que cumplan esto.
Visto desde CSS: 
1 h2 p {background color: green;} 
2
3

Visto desde HTML: 
11 <body>
12   <h2><p>'.....'<p></h2>
13

Tambien podemos ser mas específicos y al h2 darle un class o atributo; 
Visto desde CSS: 
1 .h2bgcol p {background color: green;} 
2
3

Visto desde HTML: 
11
12 <h2 class=h2bgcol><p> el lore ipsu <p></h2>
13

------------------------------------------------------------------------------------------------------------------

Por pseudo clase, comienzan con : en vez de . como el class y se agregan a tags del <body>.
Ejemplos de estas son :hover :target :root :focus :active :disabled :invalid.
Ejemplo; Visto desde CSS:
1 p:hover {color: green;}
2
3

Visto desde HTML:
11 <body>
12   <h2><p>'...'<p></h2>    Como se puede admirar, la pseudo clase solo toma accion desde CSS. A diferencia
13                            de los id, .class y atributos.

Claro, también se pueden aplicar pseudo clases en elementos con id, atributos o .class;
1 .hoverp p:hover {color: green;}                   | 1 [p=hover] p:hover {color: green;}
2  etc.


------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------
 * MEDIDAS DE UNIDAD PARA CADA ELEMENTO *:  
 Existen principalmente 2 tipos de unidades; fijas y relativas. Estas ultimas reciben este nombre por su
 característica de depender de otros valores, por lo que a diferencia de las unidades fijas las
 relativas pueden variar.

 Unidades fijas:

    in, pulgadas ("inches", en inglés). Una pulgada equivale a 2.54 centímetros.
    cm, centímetros.
    mm, milímetros.
    pt, puntos. Un punto equivale a unos 0.35 milímetros.
    pc, picas. Una pica equivale a 12 puntos, es decir, unos 4.23 milímetros.

A continuación se muestran ejemplos de utilización de unidades fijas/absolutas:

/* El cuerpo de la página debe mostrar un margen de media pulgada */
body { margin: 0.5in; }

/* Los elementos <h1> deben mostrar un interlineado de 2 centímetros */
h1 { line-height: 2cm; }

/* Las palabras de todos los párrafos deben estar separadas 4 milímetros entre si */
p { word-spacing: 4mm; }

/* Los enlaces se deben mostrar con un tamaño de letra de 12 puntos */
a { font-size: 12pt }

/* Los elementos <span> deben tener un tamaño de letra de 1 pica */
span { font-size: 1pc }

/*
Unidades relativas:

em, (no confundir con la etiqueta <em> de HTML) relativa respecto del tamaño de letra del elemento.

    En em se toma como referencia el font-size del element actual.

rem, tiene como referencia de medida el font-size del elemento root, la etiqueta <html>.

    Las rem toman como referencia el font-size del elemento <html>.

ex, relativa respecto de la altura de la letra x ("equis minúscula") del tipo y tamaño de letra del elemento.

px, (píxel) relativa respecto de la resolución de la pantalla del dispositivo en el que se visualiza 
la página HTML.

La gran ventaja de las unidades relativas es que siempre mantienen las proporciones del diseño de la página. 
Establecer el margen de un elemento con el valor 1em equivale a indicar que "el margen del elemento debe ser 
del mismo tamaño que su letra y debe cambiar proporcionalmente".

En efecto, si el tamaño de letra de un elemento aumenta hasta un valor enorme, su margen de 1em también 
será enorme. Si su tamaño de letra se reduce hasta un valor diminuto, el margen de 1em también será diminuto.
El uso de unidades relativas permite mantener las proporciones del diseño cuando se modifica el tamaño de letra 
de la página.

El funcionamiento de la unidad ex es idéntico a em, salvo que en este caso, la referencia es la altura de 
la letra 'x' minúscula, por lo que su valor es aproximadamente la mitad que el de la unidad em.

Por último, las medidas indicadas en píxel también se consideran relativas, ya que el aspecto de los elementos 
dependerá de la resolución del dispositivo en el que se visualiza la página HTML. Si un elemento tiene una 
anchura de 400px, ocupará la mitad de una pantalla con una resolución de 800x600, pero ocupará menos de la
tercera parte en una pantalla con resolución de 1440x900.

Como regla general ten en cuenta:

    Si estás haciendo un estilo que pretendes utilizar en muchos elementos distintos, por ejemplo una class
    de CSS que pretendes usar en varias partes, es mejor usar rem.
    Si lo que quieres es que el tamaño sea variable en función de dónde estés usando el estilo, usa em.
    Aunque este segundo caso lo veo menos habitual.


Tambien existen las medidas en viewports, que es como se vería el tamaño de las cosas repartidas por el tamaño
total disponible en pantalla. Existe vw (viewport width= ancho) y vh (viewport height= alto) entre otros.
Entonces si yo le doy al margen de un h1 un vw de 50. El ancho designado del h1 sera de la mitad de la pantalla.
Y si le doy un vh de 25 al margen del h1, el alto del mismo sera de un cuarto de la pantalla sobre la que se 
este viendo la pagina.

------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------
* PROPIEDADES DE TEXTO *:

font-size= tamaño del texto (medidas sugeridas em, rem)

font-family= formato de fuente de texto (como Arial, Calibri, Times New Roman, etc).

line-height= la altura que ocupan las letras dentro de los renglones en un texto. Para dejar mas claro esta 
propiedad,  la altura de la letra crece desde el centro de la misma. Es decir, de haber line-height de 1cm, 
la letra va a estar compuesta de 0,5cm hacia arriba y 0,5cm hacia abajo desde el centro de la letra. Y asi
sucesivamente con el resto de valores. Line-height 2 = 1 hacia cada lado. Es un tipo de agrandado de texto.

font-weight= se trata del grosor del formato de texto. La letra ensancha conforme mayor sea el valor de esta
propiedad. En algunos estilos de fuente se nota mas que en otros.

Para exportar una fuente, se usa un <link href= https:link de fuente.com/css rel=stylesheet> y se inserta en
el head, preferentemente cerca del link del archivo css.

En font family, si quisiera poner mas de 1 fuente para un mismo elemento lo podría hacer. Esto se hace con 
comas de la siguiente manera: font-family= Calibri, Georgia. 
Esto sirve para que si en el dispositivo no se encuentra alguna de las 2 fuentes, por descarte se elija la 
que si está disponible. De estar ambas fuentes disponibles se eligirá la que este primero despues del =.

------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------

*NORMALIZE* Es un repositorio que resetea 'en blanco' lo mas posible a los valores predeterminados que da el 
buscador a un archivo sin diseño alguno. Al sacarle estos valores y atributos, el archivo se vuelve mucho mas
personalizable desde 0 que antes. Es decir, quedaría completamente mejorado por nosotros.
Esto se puede hacer descargando y linkeando el repositorio localmente, o a traves de un url https.

------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------

*CSS, HTML y las 'cajas'*: 
 Cuando entramos a inspeccionar una página html y ponemos el cursor sobre un elemento como un h2 o un p, entre 
 otros, se hace visible un 'tamaño de caja' el cual predeterminadamente suele ocupar el ancho de todo el renglón
 del código.
 También existen elementos de caja reducida a un margen rectangular que ocupa unicamente a la letra o
 palabra del elemento. Tales como   <b></b> | <i></i> | <span> </span> entre otros.
 
 Sin embargo también podemos hacer que el tamaño de caja de los elementos que ocupan un margen del ancho total
 del renglón abarquen menos espacio. Con la propiedad display manipulamos los tamaños de las cajas. En este caso
 sería inline.
 Ej visto desde CSS:
 1  h2 {display:inline;} 
 2
 3
 Y para que un elemento cual tamaño de caja solo ocupa el ancho de su contenido cambie al ancho del renglón, basta
 con reemplazar inline por block.
 * Las propiedades height y width no funcionan con cajas inline.*

 *Propiedades de cajas*: 
Comenzamos desde las propiedades mas cercanas al contenido del elemento y avanzamos hacia las que se encuentran mas periféricas
al mismo.

 (0) Content: mas alla de modificar el ancho del contenido con block o inline, tambien podemos modificar la altura
 disponible dentro del contenido. Se utiliza line-height para esto y se maneja en px.

 (1) Padding: El área de padding es el espacio entre el contenido del elemento y su borde ( border )

 Dentro del padding tenemos: paddingtop ^ | paddingbottom v | paddingleft < | paddingright > 
 Podemos usar cada uno de los mencionados arriba para dar especificidad. O podemos simplemente usar solo padding para
 asignar la misma cantidad a cada lado sin usar todos los elementos particulares de padding.

 Tambien hay formas rapidas de usar las orientaciones del padding:
 padding: x ; y.
 padding: 50px 60px; .  El primer valor (50) modifica al eje x. El segundo modifica al eje y. 
 Esto quiere decir que, 50px de relleno se añadirán al padding der y izq mientras que 60px se añadirán 
 al padding top y bottom.

 padding: ^ ; > ; v ; < ; (1 top; 2 right; 3 bottom; 4 left;).
 padding: 10px 30px 20px 40px;. Cada valor será asignado a cada lado según el orden de la formula
 descrita arriba.

 (2) Los border son los bordes en el diseño de la caja, ya sea el contorno, forma o color del borde.
    Border-radius: 1(em) redondea las esquinas del borde.
    La fórmula que usa es: 
    border: 10px (grosor de los bordes) ; solid/double/inset/outset/groove/etc (tipo de borde) ; #xxx (color).
    Ejemplo: border: 20px solid gray. Esta sería la forma de escribirlo, separado por espacios y no puntos o comas.

 (2,5) Outline: esta propiedad está en esta descripción a pesar de que no forma parte de la jerarquía. Outline tiene una
 función muy parecida a border pero con la pequeña gran diferencia que no ocupa espacio 'físico' dentro el contenido de la caja.
 Es decir, enmarca, pero su margen de enmarcado no corre ni superpone al contenido, ni padding ni margin de la caja.

 (3) Marging: es el area de espacio que delimita el espacio de la caja de un elemento. Es lo que recubre el borde, el cual
 recubre el padding. Su forma de ser usado es igual al padding, tienen las mismas fórmulas.
 
 Todas las propiedades de las que hablamos hasta ahora de las cajas forman parte de lo que se llama box model.
 (content, padding, border, margin)< Box Model.

 *Box Shadow y Text Shadow*: es lo que es, la sombra del borde del contenido y del texto. Se utiliza con la siguiente fórmula:

 box-shadow: (eje x) px; (eje y) px; desenfoque/difuminado de la sombra (px); relleno de la sombra (px); #(color).
 Ej; Box-shadow: 30px 20px 10px 10px #000(negro). 
 
 text-shadow funciona igual que la fórmula anterior, pero carece de la 4ta variable que es el relleno de la sombra. Para 
 otorgar este efecto y darle mas magnitud en el texto se agrega una coma y se repiten los valores asignados, dicho
 proceso se puede repetir cuantas veces se prefiera. Es decir:

 text-shadow: 2px 2px 7px #ff0; (, 2px 2px 7px #ff0; para mayor fuerza en la sombra).
---------------------------------------------------------------------------------------------------------------------------------
 
*Tambien existe la propiedad transform:                                                                             *

transform: rotate(xdeg). Esto aplica rotación al diseño de las cajas. Y se señala en grados, en el código no usamos
el signo de 'º' sino que ponemos 'deg' que es una abreviación de 'degree'. Ej:

transform: rotate(90deg).
-------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------
 Así como en el text shadow usamos una , para repetir el valor del atributo. Si añadimos elementos que compartan las
 mismas propiedades también usamos la  , 
 Es decir: si tengo dos clases que van a ocupar las mismas propiedades ejemplo:
 
 1  .caja1, .caja2, .caja5 {display: block}
 2
 3


-------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------





-------------------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------------------

* Text align: center left right justify sirve para modificar los márgenes del texto.*
------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------


