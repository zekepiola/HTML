# HTML
Aca pongo todo lo relacionado con aprendizaje Html.

HMTL Semántico:

El header representa la parte inicial, introductorio o superior de tu sitio web. Este mismo puede contener elementos importantes como portadas, 
navegación e incluso títulos. Los h1 son meramente responsables de mostrar títulos en tu sitio.

Pero, una de las cosas mas importantes que contiene el <header> es el <nav>. Su palabra es la abreviación de navegador, y es usado al comienzo de
la pagina para vincular todos los enlaces necesarios. Enlaces o submenu's. En facebook por ejemplo, el nav esta hecho de varios botones como: Perfil,
notificaciones, messenger, menu, marketplace, amigos y demás.

  Ejemplo:
&lt;body&gt; <br>
  &lt;header&gt; <br>
    &lt;nav&gt; <br>
      &lt;ul&gt; Si, se usan listas y de las que no usan orden jerárquico. <br>
        &lt;li&gt; Esto atribuye a la cantidad de botones necesarios, cada (li) es un ítem. Y como dichos ítems son links <br>
          cada li estará compuesto de &lt;a href= [inserte link aquí]&gt; nombre de sección&lt;/a&gt; <br>
      &lt;/ul&gt; <br>
    &lt;/nav&gt; <br>
  &lt;/header&gt; <br>

  Lo mas probable es que las direcciones que ingresemos en los items sean .html si son accesos internos de nuestra pagina. Uno será <br>
 &lt;a href= index.html&gt; Inicio&lt;/a&gt; <br>
 &lt;a href= nosotros&gt; Sobre nosotros&lt;/a&gt; <br>
 &lt;a href= contacto&gt; contactános&lt;/a&gt; <br>
 &lt;a href= soporte&gt; soporte&lt;/a&gt; <br>
 Y así

 Es muy importante hacer un archivo html con solo el nav de nuestra pagina y reutilizarlo para cada sección distinta con cada body distinto.
  Ya que todas las paginas necesitan una forma de volver al inicio u otra sección.

 Ahora, para hacer de la pagina algo mas completo, el orden que recibirá sera este:
  
  &lt;body&gt; <br>
  &lt;header&gt; <br>
    &lt;nav&gt; <br>
      &lt;ul&gt; Si, se usan listas y de las que no usan orden jerárquico. <br>
        &lt;li&gt; Esto atribuye a la cantidad de botones necesarios, cada (li) es un ítem. Y como dichos ítems son links <br>
          cada li estará compuesto de &lt;a href= [inserte link aquí]&gt; nombre de sección&lt;/a&gt; <br>
      &lt;/ul&gt; <br>
    &lt;/nav&gt; <br>
  &lt;/header&gt; <br>
  &lt;article&gt; Este tag sirve para escribir artículos, o para encerrar los h1, h2, h3 y demás sin que queden sueltos ''en el aire''. Es una forma mas <br>
      de darle un lindo orden al código. <br>
    &lt;section&gt; Los artículos se dividen en secciones, y por mas que lleve una sola sección esta bueno agregar este tag para darle mas orden como <br> mencionamos antes. <br>
       &lt;h1&gt; <br>
             ''...'' <br>
       &lt;/h1&gt; <br>
       &lt;p&gt; <br>
             ''...'' <br>
       &lt;/p&gt; <br> 
    &lt;/section&gt; <br>
  &lt;/article&gt; <br>
  &lt;aside&gt; Es un tipo de tag que usamos para incluir información secundaria o extra, en un panel secundario. Suele estar a un lateral de la pagina por
  eso se le llama 'aside'.<br>
    &lt;h2&gt;<br>
      ''...'' <br>
    &lt;/h2&gt; <br>
  &lt;/aside&gt; <br>
  &lt;footer&gt; Este sería el pié de página y va siempre debajo del todo de esta. Sirve para poner la información de contacto, para insertar feedback, para
  poner el copyright, para otros enlaces fuera de la pagina, entre otros. <br>
  &lt;/footer&gt; <br>
  
