---
layout: post
title: 'Empezando con Blender 2.5 [Parte 1: Interfaz y Object Mode]'
date: '2011-02-15T18:58:00.004-02:00'
author: Filly
tags:
- 3D
- tutorial
- software libre
- programas
modified_time: '2011-09-14T15:32:48.608-03:00'
thumbnail: http://3.bp.blogspot.com/-tOSk1dUIOro/TVTUli6vq2I/AAAAAAAAAIQ/wxJaMGuTob4/s72-c/blendermonster.png
blogger_id: tag:blogger.com,1999:blog-6145090415061302130.post-8912285814269081743
blogger_orig_url: http://missfillys.blogspot.com/2011/02/empezando-con-blender-25-tutorial.html
---
[![](http://3.bp.blogspot.com/-tOSk1dUIOro/TVTUli6vq2I/AAAAAAAAAIQ/wxJaMGuTob4/s320/blendermonster.png)][0]  
Dado que todavía no está lista la versión definitiva de Blender 2.5 y hay muy poca documentación sobre cómo
empezar a usarlo, decidí escribir un par de tutoriales MUY básicos para los recién iniciados en este programa.

* [¿Qué es Blender?][1]
* [Instalar la versión 2.5 Beta desde repositorio (Ubuntu)][2] 

1\. Movernos por la interfaz

Blender 2.5 luce muy diferente a sus versiones anteriores. Su interfaz está mucho más "organizada" y tiene un
diseño mucho más agradable a la vista.

Cuando abrimos el programa, nos encontramos con el clásico cubo predeterminado en el escenario. En distintos lugares
del espacio de trabajo tenemos también la **Lamp** (fuente de iluminación) y la **Camera** (cámara).  

Por ahora vamos a dejar a nuestro cubo en su lugar y probar cómo movernos a su alrededor. 

_Selección de objetos_

* Botón derecho del _mouse_ para seleccionar cada uno de los diferentes elementos del escenario. El objeto
seleccionado aparece con borde naranja.
* Tecla **A** para seleccionar todos los objetos del escenario. Tecla **A **nuevamente para no tener ningún
elemento seleccionado.
* Para seleccionar más de un objeto, primero elegimos uno con el botón derecho del _mouse_ y, manteniendo la
tecla **Shift** presionada, elegimos el segundo.
* Teclas **Ctrl + I **para realizar la selección inversa. 

_Selección por _Border_ o _Circle__  

Por el momento no nos será de gran utilidad, porque todavía estamos posicionados en _Object Mode_, donde no se
nos permite deformar la malla básica de nuestro modelo. Sin embargo, cuando pasemos a _Edit Mode_ (desde donde
realizaremos el modelado propiamente dicho), generalmente vamos a necesitar seleccionar varios vértices o varias
aristas rápidamente.  

Para esto tenemos dos herramientas de selección: _Border Select_, que funciona como una "caja" que desplazaremos
hasta que cubra los objetos que necesitamos seleccionar, y _Circle Select_, que se utiliza como un "pincel",
con el que vamos a pintar lo que necesitemos. La selección _Border_ se activa con **B**, y la _Circle_ con **C**.
Las utilizamos manteniendo apretado el **botón izquierdo del _mouse_**. Para deshacer una selección, realizamos el
mismo proceso pero con la **rueda del _mouse_**.  

[![](http://1.bp.blogspot.com/-24RRneLW7D4/TVknSEVD8DI/AAAAAAAAAJQ/8M0CaN_aW7Y/s320/blenderejemplo1.png)][3]

El modo en perspectiva hace mucho más difícil medir de las proporciones de nuestro modelo, pero a veces puede
resultar útil dado que la Cámara utiliza esta visión para el renderizado final. Modelo basado en
[tutorial para 3ds Max][4]

_Diferentes vistas del escenario_

Esto es algo fundamental a la hora de trabajar con Blender. No se puede hacer un modelo 3D sin saber cómo luce
desde todos los ángulos. Para cambiar la perspectiva, usamos las teclas del **_numbpad ___o teclado numérico**.
Los números del teclado alfabético realizan una función diferente, así que por el momento no los vamos a tocar. 

* **1** para la vista frontal (_front_). **Ctrl + 1** para vista de atrás (_back_).
* **3 **para la vista derecha (_right_). **Ctrl + 3** para vista izquierda (_left_).
* **7** para la vista superior (_top_). **Ctrl + 7 **para la vista desde abajo (_bottom_).
* **2** y **8 **para rotar nuestra perspectiva sobre el eje X.
* **4** y **6** para rotar nuestra perspectiva sobre el eje Z.

La vista seleccionada aparece en la esquina superior izquierda del escenario. Por defecto es "**Persp**"
(_front perspective_, _left perspective_, etc.), pero en general nosotros no vamos a usar perspectivas occidentales,
que pueden hacer nuestro trabajo confuso, sino que vamos a preferir la perspectiva ortogonal, o isométrica.
Para cambiar de una a otra, usamos la tecla **5** del _numpad_.

_Abrir ventanas (más de una vista a la vez)_  

Trabajar desde diferentes ángulos al mismo tiempo es algo muy útil en Blender, y una buena forma de ahorrar tiempo.
En las versiones anteriores del programa, por defecto al ejecutarlo nos encontrábamos con cuatro ventanas que nos
ofrecían diferentes perspectivas de nuestro objeto.  

Ahora, inicialmente contamos con una sola ventana (tengo entendido que todo esto es configurable desde las preferencias
de usuario). Para abrir una o varias más, simplemente vamos a la esquina superior derecha de nuestro escenario, donde
hay un icono con tres líneas paralelas, lo apretamos, y sin soltar el botón del _mouse_ lo arrastramos hacia la
izquierda o abajo. A partir de estas ventanas nuevas puede abrirse otras usando el icono de la misma forma.
Para cerrarlas, se arrastra el icono de una de ellas hacia la derecha o arriba, produciendo que una ventana "cubra"
a la otra.  

Cada una de estas ventanas va a tener sus propios menúes dependiendo de los que hayamos estado usando en la ventana
original. Para cerrar las _Object Tools _de una ventana, ponemos el cursor sobre la misma y apretamos **T** (_tools_).
Lo mismo pasa si queremos cambiar la perspectiva de cada una: se coloca el _mouse_ sobre la ventana a modificar y
elegimos la vista desde el _numpad_.  

Diferentes vista del mismo objeto al mismo tiempo. Los menúes laterales se ocultaron para mayor comodidad:

[![](http://2.bp.blogspot.com/-o6GRHT1Z-YY/TVnB6td9koI/AAAAAAAAAJs/L-qPglPmdrQ/s320/blenderejemplo6.png)][5]

_Rotar libremente nuestra visión_

Cuando queremos examinar nuestro objeto desde otros puntos de vista no tan específicos, nos movemos alrededor de él
manteniendo presionada la rueda del _mouse_ y apuntando para el lado para el que queremos girar.  

Si, en cambio, queremos mover nuestra ventana para, por ejemplo, centrarnos en una parte específica del modelo, sin
cambiar la perspectiva, usamos **Shift + rueda del _mouse_** para posicionarnos donde queremos.  

2\. Manipular nuestro objeto  

Una vez que sabemos movernos alrededor de nuestro objeto, conozcamos cómo empezar a tocarlo para prepararlo para el
modelado. Vamos a utilizar el cubo predeterminado. Si estuvimos moviendo muchas cosas del escenario en la parte 1\. y
queremos volver a tener todo en orden, con **Ctrl + N **creamos un nuevo archivo. ¡Cuidado! Blender no nos va a
preguntar si queremos guardar nuestro proceso cuando creamos un archivo nuevo o cuando cerramos el programa,
así que es conveniente acostumbrarse a guardar nuestros avances con frecuencia.  

Existen 3 _shortcuts _principales que nunca, nunca nos debemos olvidar. Éstos sirven para rotar, desplazar y modificar
el tamaño, y le corresponden las teclas **R** (_rotate_), **G** (_grab) y_ **S** (_scale_), respectivamente. Veamos
cómo funcionan.  

Tomemos nuestro cubo, que estará seleccionado por defecto (si tocamos algo para quitarle la selección, usamos el botón
derecho del mouse como indiqué antes).  

Presionamos **G** y movemos el puntero del _mouse_. En efecto, _grab_ sirve para desplazar nuestro objeto de lugar.
Recordemos que si presionamos la G accidentalmente, o ya no queremos mover nuestro cubo, podemos cancelar nuestra acción
usando el **Botón derecho del _mouse_**. Nuestro cubo regresará a su posición anterior como si nada hubiera pasado.
Esta cancelación aplica para todas las otras acciones que podamos realizar sobre el objeto (_rotate_, _scale_, etc.).
Haga la prueba.  

Volvemos a presionar **G** y movemos nuestro cubo a otro lugar del escenario. Lo "colocamos" haciendo click una vez con
el **Botón izquierdo del _mouse_**. De nuevo, si nos arrepentimos, el clásico deshacer con **Ctrl + Z** será nuestra
solución.  

Una herramientas indispensable también, es la capacidad de mover, rotar o escalar de acuerdo a uno solo de los ejes
del espacio. ¿Qué significa esto? Probemos con **G **nuevamente. Sin tocar nada, presionemos **X** y movamos el puntero
del _mouse_. Vemos que ahora nuestro cubo se mueve solamente sobre el eje **X**. Lo mismo pasa si apretamos **Y** o
**Z**, el eje sobre el que se mueve nuestro cuba irá cambiando.  

Cancelamos _grab_ con el botón derecho del _mouse_. Con nuestro cubo todavía seleccionado, apretamos **S**.
Cuando movamos el puntero, el objeto irá aumentando o disminuyendo de tamaño. Si limitamos el _scale_ a uno de los ejes,
deformamos nuestro cubo para convertirlo en un prisma. Esto también se hace usando **X**, **Y** y**Z **mientras tenemos
_scale _activo.  

_Scale_ sin limitación a ningún eje:

[![](http://2.bp.blogspot.com/-F_YXxHXl_IY/TVlLyHG_IjI/AAAAAAAAAJU/QqgZpMdlsUY/s320/blenderejemplo2.png)][6]

_Scale _limitado al eje X:

[![](http://4.bp.blogspot.com/-2NL0OMfpJtE/TVlL58CEt5I/AAAAAAAAAJY/57OHLXvK-XU/s320/blenderejemplo3.png)][7]

Por último veremos la acción _rotate_. De vuelta, con nuestro cubo original seleccionado, usamos **R**, y al mover el
_mouse_ el objeto rotará en la dirección que apuntemos, aunque estará un poco limitado a nuestro campo de visión.
Presionando **R** nuevamente, cambiamos a _trackball_, que básicamente es otro sistema de rotación un poco más libre.  

_Ejes globales y locales_  

Nuestro espacio de trabajo, si lo pensamos como "el mundo" donde vamos a desplegar nuestros modelos, tiene tres ejes:
X, Y y Z (geometría del espacio básica). Estos son los ejes globales, los de nuestro escenario. Ahora bien, cada uno
de nuestros objetos tendrá sus propios ejes, llamados ejes locales.  

Tomando como ejemplo el modelo del monstruo en 3D anterior, decimos que su altura se mide en el eje Z (vertical).
Entonces, ¿qué pasa si lo giramos de modo que quede "acostado" con respecto este eje? Ahora su altura estará dispuesta
sobre, por ejemplo, el eje Y (dependiendo de hacia dónde lo giremos), pero seguirá siendo parte del eje Z local del
monstruo, porque sigue siendo SU altura aunque esté acostado sobre el escenario.  

Por eso, en Blender podemos restringir el movimiento, escalado y rotación de cada uno de nuestros objetos a sus ejes
locales. Para esto, activamos una de estas acciones, y apretamos dos veces la tecla del eje local que queremos usar.
(Por ejemplo, **G** para _grab_, X para seleccionar el eje global, y X nuevamente para seleccionar el eje local).  

_Grab_ restringido al eje X global:

[![](http://2.bp.blogspot.com/-0cNM4DFCPWk/TVm40tljlyI/AAAAAAAAAJc/XWMAEpwL92E/s320/blenderejemplo4.png)][8]

_Grab_ restringido al eje X local:

[![](http://4.bp.blogspot.com/-0qXzjKYzodk/TVm42wVXVdI/AAAAAAAAAJg/_vs3nrg-u6w/s320/blenderejemplo5.png)][9]

* [Parte 2 del tutorial][10]

[0]: http://3.bp.blogspot.com/-tOSk1dUIOro/TVTUli6vq2I/AAAAAAAAAIQ/wxJaMGuTob4/s1600/blendermonster.png
[1]: http://es.wikipedia.org/wiki/Blender
[2]: http://www.atareao.es/ubuntu/conociendo-ubuntu/blender-2-5-beta-en-ubuntu-desde-repositorio/
[3]: http://1.bp.blogspot.com/-24RRneLW7D4/TVknSEVD8DI/AAAAAAAAAJQ/8M0CaN_aW7Y/s1600/blenderejemplo1.png
[4]: http://www.polygonblog.com/3d-monster
[5]: http://2.bp.blogspot.com/-o6GRHT1Z-YY/TVnB6td9koI/AAAAAAAAAJs/L-qPglPmdrQ/s1600/blenderejemplo6.png
[6]: http://2.bp.blogspot.com/-F_YXxHXl_IY/TVlLyHG_IjI/AAAAAAAAAJU/QqgZpMdlsUY/s1600/blenderejemplo2.png
[7]: http://4.bp.blogspot.com/-2NL0OMfpJtE/TVlL58CEt5I/AAAAAAAAAJY/57OHLXvK-XU/s1600/blenderejemplo3.png
[8]: http://2.bp.blogspot.com/-0cNM4DFCPWk/TVm40tljlyI/AAAAAAAAAJc/XWMAEpwL92E/s1600/blenderejemplo4.png
[9]: http://4.bp.blogspot.com/-0qXzjKYzodk/TVm42wVXVdI/AAAAAAAAAJg/_vs3nrg-u6w/s1600/blenderejemplo5.png
[10]: http://www.missfilly.com.ar/2011/02/empezando-con-blender-25-parte-2.html