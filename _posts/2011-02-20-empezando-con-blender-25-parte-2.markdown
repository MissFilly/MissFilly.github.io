---
layout: post
title: 'Empezando con Blender 2.5 [Parte 2: Extrude y parte inferior del modelo]'
date: '2011-02-20T13:50:00.002-03:00'
author: Filly
tags:
- 3D
- tutorial
- software libre
- programas
modified_time: '2011-09-14T15:32:48.603-03:00'
thumbnail: http://3.bp.blogspot.com/-sYv4Yrbi9p4/TWFFpKHAIkI/AAAAAAAAALM/C0u0TiRD0lg/s72-c/blender.png
blogger_id: tag:blogger.com,1999:blog-6145090415061302130.post-5008099346645009738
blogger_orig_url: http://missfillys.blogspot.com/2011/02/empezando-con-blender-25-parte-2.html
---

[![](http://3.bp.blogspot.com/-sYv4Yrbi9p4/TWFFpKHAIkI/AAAAAAAAALM/C0u0TiRD0lg/s320/blender.png)][0]

Para poner nuestras herramientas directamente en práctica y no aburrirnos con otra larga teoría, vamos a modelar
una figura básica. En este caso me basé en [este tutorial][1] (acuérdense de que yo también soy _newbie_), que aunque
está escasamente explicado (por eso no va a ser suficiente con sólo ver el vídeo) puede ayudarnos para observar el
progreso del modelo. No vamos a realizar cabeza, manos ni pies, porque son bastante más complejo de lo que queremos.  

Nota: Usando la **barra espaciadora**, Blender 2.5 nos ofrece una maravillosa herramienta de búsqueda que nos será muy
útil si olvidamos un _shortcut _o intentamos trasladar un tutorial de Blender 2.4 a la nueva versión (muchos _shortcuts_
y menús han cambiado).  

1\. Preparar nuestro espacio de trabajo

Abrimos Blender y eliminamos el cubo del escenario con **X** o **Delete** (**Supr**).

Yo elegí trabajar con dos áreas o ventanas al mismo tiempo, aunque se puede trabajar con una sola e ir cambiando de
perspectiva. A la izquierda le asigné perspectiva ortogonal (**5** para cambiar a perspectiva ortogonal) frontal
(_front ortho_) con **1** del _numpad_, y a la derecha perspectiva ortogonal izquierda (_left ortho_) con **Ctrl + 3**.

Para este modelo básico, preparé dos imágenes de referencia. Click en cada una para ampliarlas, botón derecho del
_mouse_ \> Guardar imagen como..., y nos fijamos en la dirección donde colocamos las imágenes guardadas.

[![](http://1.bp.blogspot.com/-m-ULbPqenxE/TVsGHnBDW9I/AAAAAAAAAJw/f6XO7NOXDgk/s200/blenderreference1.png)][2]

[![](http://4.bp.blogspot.com/-hOfVE9CyPzg/TVt7sGQw24I/AAAAAAAAAJ8/ai4Rm78ar94/s200/blenderreference2.png)][4]  

Con el puntero del _mouse_ sobre el área izquierda (esto es importante, las imágenes se agregaran sólo a la ventana
sobre la que estemos posicionados), apretando **N** abrimos el menú Properties (también puede hacerse desde View \>
Properties). Casi al final de la lista de opciones, tildamos la casilla de _**Background Images**_, desplegamos el menú,
vamos a Add Image \> Non set \> Open. Buscamos el directorio de la imagen de referencia del cuerpo visto de frente, y
la abrimos.  

Debajo del botón Add Image y el nombre de la imagen, abrimos el menú de **Axis:** y cambiamos All Views (por defecto)
por **Front**. Esto indica en qué perspectiva deberemos estar colocados para ver la imagen de referencia. Ahora podemos
ocultar el menú otra vez con **N**.

Hacemos lo mismo en el área de derecha, pero eligiendo el directorio de la imagen de referencia de perfil, y
seleccionando **Left **en **Axis:**.  

[![](http://2.bp.blogspot.com/-j-cQXk7MkLM/TVuHNGUuDQI/AAAAAAAAAKM/jGGEzLyf7dY/s320/blendertutorial1.png)][5]

Ahora estamos listos para empezar a modelar.

2\. Modelado  

Con **Shift + A** abriremos el menú Add, desde donde podemos agregar nuevos objetos a nuestro escenario. (Nota: los
elementos que se añaden en Edit Mode van a ser considerados como un solo objeto, y se moverán, escalarán y comportarán
como tal; mucho cuidado con eso.) Seleccionamos **Mesh \> Cylinder**.  

En el menú de la izquierda (Object Tools), bajo el título "Add Cylinder", cambiamos el número de vértices (Vertices)
por, digamos, 10 (haciendo click sobre el número 32 predeterminado, escribiendo 10 y apretando Enter). Nota: Una vez
que toquemos otra cosa, las opciones de Add Cylinder desaparecerán y ya no podremos modificar esos parámetros de
nuestro objeto.

En el área izquierda, con **S** vamos a escalar nuestro cilindro hasta que tenga el tamaño adecuado, y con **G** lo
movemos hasta posicionarlo sobre el tobillo derecho del dibujo en perspectiva frontal. Después, en el área derecha,
con **G **y **Y** lo movemos sobre el eje Y para que quede bien posicionado en la vista de perfil. También lo escalamos
en el eje Y (**S** y **Y**) hasta que el borde superior del cilindro coincida con el ancho de la pierna. Como el dibujo
es imperfecto, nos va a quedar el pie del segundo dibujo un poco más abajo, pero no vamos a modelar manos ni pies en
este tutorial, así que podemos ignorar eso y debería quedarnos algo así:  

[![](http://4.bp.blogspot.com/-vQO00kaLOwE/TWBnOwY2vZI/AAAAAAAAAKs/_AxgBpz8uE0/s320/blendertutorial2.png)][6] 
 
¡Ahora se pone interesante! Con **Tab** (tabulación) pasamos a Edit Mode, y ahora es cuando podemos empezar a modificar
de verdad nuestra malla.  

Primero, buscamos en nuestra barra de herramientas inferior el icono de la forma
![](http://2.bp.blogspot.com/-jgUZ-NUMaVY/TWAf-agm64I/AAAAAAAAAKg/ZLEoDD6iTq8/s1600/blendericon.png)
(herramienta que limita la selección a lo que está visible), que por defecto estará activado, y lo desactivamos
en las dos áreas por el momento.

**A** para no tener ningún objeto seleccionado. Ahora, con una herramienta de selección (yo prefiero _Cyrcle Select_ con
**C**), elegimos todos los vértices superiores de nuestro cilindro. Sin importar en qué ventana los "pintemos", la
selección se aplicará al objeto en todas las áreas.  

[![](http://1.bp.blogspot.com/-ibNdmBhUYqw/TWBngynY6NI/AAAAAAAAAKw/r6ycRkDRZn0/s320/blendertutorial4.png)][7]  

Con **E** realizamos **Extrude**, la forma clásica y fácil de modelar. _Extrude_ básicamente clona los objetos que
seleccionamos (pueden ser vértices, bordes o caras, configurable desde
![](http://4.bp.blogspot.com/-fUN2ksxoJKQ/TWAtNZ6b6LI/AAAAAAAAAKo/AbFq09TQ7Hg/s1600/blendericon2.png)) y crea caras
entre éstos y los nuevos para formar prismas. Si apretamos el **botón derecho del _mouse_**, nuestros objetos clonados
(en este caso deben ser vértices) van a permanecer en el mismo lugar que sus objetos de origen. Tenemos que tener mucho
cuidado con esto, ya que a veces podemos extrudir más de una vez sin querer y quedarán varios vértices superpuestos;
esto puede solucionarse apretando **W** y seleccionando **Remove Doubles**. Para que no haya confusiones sobre cuándo
hay un vértice sobre otro, la forma en que se ven los puntos solos o con _extrude_ es diferente:  

Vértices sin extrudir (izquierda) y vértices producidos con _extrude_ (derecha):

[![](http://4.bp.blogspot.com/-2b2ela3YLtA/TWBtN3SF2JI/AAAAAAAAAK0/jO8iZ-9yek0/s320/blendertutorial5.png)][8]

Si habíamos apretado el botón derecho del _mouse_ para cancelar el movimiento de los nuevos vértices, elegimos **G**
para _grab_, y los llevamos hacia arriba hasta cubrir otra porción de la pierna. Una vez que elegimos dónde los
queremos, los colocamos con el **botón izquierdo del _mouse_**. Los escalamos y movemos con con **S** o **G** y **X**
en el área de la izquierda, y con **S** o **G **y **Y** en la derecha para que su forma vaya coincidiendo con el modelo.
Cuando nos gusta cómo está posicionado, volvemos a extrudir y repetimos el proceso. Para observar mejor el avance,
como dije antes, se pueden ayudar con [este video tutorial][1].  

Al llegar a la altura de la entrepierna, extrudimos nuevamente, y rotamos sobre el eje Y de modo que la curva se
corresponda con la línea de la cadera:  

[![](http://3.bp.blogspot.com/-SA8h9VeUw-U/TWChrO7Ui_I/AAAAAAAAAK4/9qjbbBPl0mk/s320/blendertutorial6.png)][9]  

**A** para seleccionar todo. Buscamos en el _Outliner_ (menú de la derecha) el icono de los modificadores (_modifiers_)
![](http://3.bp.blogspot.com/-ArCLadm8_N4/TWCjxfnxHYI/AAAAAAAAAK8/A3Ww3UObwwE/s1600/blendertutorial7.png), seleccionamos
Add Modifier \> Mirror. Esto añadirá un reflejo exacto de todo lo que hemos modelado hasta ahora, tenemos que
asegurarnos que en la configuración del modificador estén tildadas las casillas _X _y _Merge_, y también activaremos la
opción _Clipping_. Con **G **y **X** movemos nuestros objetos hasta que el espacio entre las piernas sea aproximadamente
el mismo que en el dibujo, volvemos a _Object Mode_ con **Tab** y acomodamos todo como debe ir. (Nota: el modificador
Mirror no crea otro objeto, de modo que las acciones que realicemos en _Object Mode_ van a modificar al original y al
espejo como a un mismo elemento.)  

Volvemos a _Edit Mode_, elegimos _Face select mode_ (desde
![](http://4.bp.blogspot.com/-fUN2ksxoJKQ/TWAtNZ6b6LI/AAAAAAAAAKo/AbFq09TQ7Hg/s1600/blendericon2.png)) y seleccionamos
la mitad interna de la parte superior de nuestro modelo:  

7 del _numpad_ para _Top view_:

[![](http://3.bp.blogspot.com/-y0hn-U58Jv4/TWCojVgteYI/AAAAAAAAALA/wnElooqMDyU/s320/blendertutorial9.png)][10]

**E** para _extrude_ y **X** para mover las nuevas cara sobre el eje X. Como tenemos _Clipping_ activado en el
modificador, cuando acerquemos las nuevas caras al reflejo, éstas se van a "unir". Cuando estén completamente juntas,
confirmamos con el botón izquierdo del _mouse_.

Ahora tenemos listas las piernas de nuestro modelo.  

Cómo debe lucir aproximadamente nuestro resultado:

[![](http://3.bp.blogspot.com/-vYBGOm1nswM/TWFEJYu-_hI/AAAAAAAAALI/_hxqM3rdHtM/s320/blendertutorial8.png)][11]

[0]: http://3.bp.blogspot.com/-sYv4Yrbi9p4/TWFFpKHAIkI/AAAAAAAAALM/C0u0TiRD0lg/s1600/blender.png
[1]: http://www.youtube.com/watch?v=9BdzTufv3_0
[2]: http://1.bp.blogspot.com/-m-ULbPqenxE/TVsGHnBDW9I/AAAAAAAAAJw/f6XO7NOXDgk/s1600/blenderreference1.png
[4]: http://4.bp.blogspot.com/-hOfVE9CyPzg/TVt7sGQw24I/AAAAAAAAAJ8/ai4Rm78ar94/s1600/blenderreference2.png
[5]: http://2.bp.blogspot.com/-j-cQXk7MkLM/TVuHNGUuDQI/AAAAAAAAAKM/jGGEzLyf7dY/s1600/blendertutorial1.png
[6]: http://4.bp.blogspot.com/-vQO00kaLOwE/TWBnOwY2vZI/AAAAAAAAAKs/_AxgBpz8uE0/s1600/blendertutorial2.png
[7]: http://1.bp.blogspot.com/-ibNdmBhUYqw/TWBngynY6NI/AAAAAAAAAKw/r6ycRkDRZn0/s1600/blendertutorial4.png
[8]: http://4.bp.blogspot.com/-2b2ela3YLtA/TWBtN3SF2JI/AAAAAAAAAK0/jO8iZ-9yek0/s1600/blendertutorial5.png
[9]: http://3.bp.blogspot.com/-SA8h9VeUw-U/TWChrO7Ui_I/AAAAAAAAAK4/9qjbbBPl0mk/s1600/blendertutorial6.png
[10]: http://3.bp.blogspot.com/-y0hn-U58Jv4/TWCojVgteYI/AAAAAAAAALA/wnElooqMDyU/s1600/blendertutorial9.png
[11]: http://3.bp.blogspot.com/-vYBGOm1nswM/TWFEJYu-_hI/AAAAAAAAALI/_hxqM3rdHtM/s1600/blendertutorial8.png