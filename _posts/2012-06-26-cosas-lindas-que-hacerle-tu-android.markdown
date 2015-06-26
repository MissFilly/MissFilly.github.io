---
layout: post
title: Cosas "lindas" que hacerle a tu Android
date: '2012-06-26T12:05:00.001-03:00'
author: Filly
tags:
- privacidad
- software libre
- programas
modified_time: '2012-08-07T20:41:50.173-03:00'
thumbnail: http://4.bp.blogspot.com/-PZy0c6zRUDc/T-jAZ8QAZ4I/AAAAAAAAAyc/7lMPdn9hu0Y/s72-c/android.jpg
blogger_id: tag:blogger.com,1999:blog-6145090415061302130.post-4968842485943625475
blogger_orig_url: http://missfillys.blogspot.com/2012/06/cosas-lindas-que-hacerle-tu-android.html
---

[![](http://4.bp.blogspot.com/-PZy0c6zRUDc/T-jAZ8QAZ4I/AAAAAAAAAyc/7lMPdn9hu0Y/s400/android.jpg)][0]  

Empecé a usar Android hace algunos meses, con la adquisición de mi primer _smartphone_, un Milestone 2 (A953). La
primera cosa que noté usando el OS fueron los permisos ridículos que requieren la mayoría de las aplicaciones de
[Google Play][1], y más tarde empezaron a ponerme nerviosa varias otras cosas, como el _lag_ que solía experimentar y
lo molesto que era tener un montón de aplicaciones instaladas (y ocupando espacio en el menú) que nunca en mi vida
pensaba utilizar.

¿Solución? Bueno, esto es software libre (¿es software libre?)... A meter mano se ha dicho. (Nota: este post no
pretende de ninguna manera ser un tutorial, es simplemente una mención de las cosas que hice con (¿le hice a?) mi
Android. En algunos _links_ que dejo sí pueden encontrar buenos tutoriales para lo que quieran hacer ustedes.)

[![](http://4.bp.blogspot.com/-UwTMUUZTz1Y/T-jEP1ad7kI/AAAAAAAAAyo/X1HZpkilScA/s200/cyanogen.png)][2]

### 

### 1\. Rooting y custom ROM

Ante la duda, recomendado leer: [Qué es una custom ROM y cuáles son sus beneficios][3]. Lo mismo, pero
[sobre rooting][4].

Mis razones principales para instalar una custom ROM fueron, como mencioné, el _lag_ que sufría mi Android y el
irretenible odio (?) que sentía hacia las aplicaciones de Motorola y del operador de telefonía móvil. Por otro lado,
aunque además de DroidWall (de la que hablo más adelante), no había aplicaciones que requirieran root que me llamaran
la atención, siempre es bueno saber que tengo control total sobre MI dispositivo (más info sobre esa forma de pensar
[acá][5]).

"Rootear" el teléfono no debería traer mayores problemas, pero si van a elegir una custom ROM recomiendo que estén
dispuestos a sentarse y leer, leer, leer sobre las opciones que tienen y los pros y contras de cada una. Un excelente
lugar para hacer eso es el [foro de xda-developers][6]. Yo me decidí por un _port_ no oficial de CyanogenMod 7
(Android 2.3.7) para Milestone 2, más que nada porque [CyanogenMod][7] es la custom ROM más popular (y eso suele
implicar un mayor soporte de la comunidad) y su estabilidad. Otra buena opción es [MIUI][8]. [Algunas custom ROMs][9]
van a soportar más dispositivos, otras menos... Como dije, es todo cuestión de sentarse a leer y comparar.

### 2\. Ajustes de privacidad y otros

Como me interesa la privacidad, una vez tuve CyanogenMod funcionando lo primero que hice fue configurar algunas cosas
relacionadas a mi ubicación y la sincronización de cuentas. Obviamente, si ustedes no están tan [preocupados por su
privacidad][10] o no les interesa si sus dispositivos los "trackean" o no, no van a querer hacer esto.

_Settings_ \> _Location & security settings_ \> _Use wireless networks_, _Use GPS satellites_ y _GPS Source_, todos
destildados.

_Settings _\> _Location & security settings _\> _Set up screen lock_ (yo prefiero el _pattern_)

_Settings_ \> _Privacy settings_ \> _Back up my data_ destildado.

_Settings _\> _Account & sync settings_ \> ___Auto-sync_ destildado. (Aplicaciones como Play Store y K-9 Mail necesitan
que _Background data_ esté habilitado; pueden desactivarlo y activarlo manualmente si no quieren dejar la opción
habilitada de forma permanente.)  

[![](http://3.bp.blogspot.com/-dp5E5JjUrnY/T-kjQ7JVygI/AAAAAAAAAy0/2NUYB7n-20A/s1600/orbot.png)][11]  

### 3\. Reemplazar las _stock apps_, instalar software libre  

Junto con la custom ROM necesité instalar las Google Apps (GApps) para poder sincronizar Gmail (y poder usar Play Store)
con mi teléfono. Como siempre, no tenía pensado usar el 90% de éstas y de las "aplicaciones _stock_", así que eliminé 
la mayoría. Existen [varias formas de eliminar][12] _stock apps_ (root requerido).  

Algunas _apps_ que uso, muchas provistas por [The Guardian Project][13], son:  

* [Orbot][14]: Tor on Android (libre, _port_ de Tor) \> [Google Play][15]
* [Orweb][16] (libre, _browser_) \> [Google Play][17]
* [Gibberbot][18] (libre, cliente de chat) \> [Google Play][19]
* [K-9 Mail][20] (libre, cliente de correo) \> [Google Play][21]
* [TextSecure][22] (libre, _app_ de mensajería de texto) \> [Google Play][23]
* [Songbird][24] (versiones para Windows, Mac, Solaris y Linux libres, pero el cliente de Android es código cerrado ¬¬,
reproductor multimedia) \> [Google Play][25]
* [DroidWall][26] (libre, _firewall_) \> [Google Play][27]  
DroidWall es por lejos mi aplicación preferida. Yo tengo en la _white list_ solamente Firefox for Mobile, Gibberbot, 
K-9 Mail, Orbot, Orweb y la aplicación oficial de Twitter. Así no tengo que preocuparme por que mi red esté siendo
utilizada innecesariamente o por aplicaciones accediendo a la misma aunque no les competa (por ejemplo, Songbird).  

Lista de _apps_ _privacy-friendly_ en [The Guardian Project][28], y listas de aplicaciones _open source_ para Android en
[Wikipedia][29], [F-Droid][30] (Android FOSS Repository) y [Android Open Source][31].  

### 4\.  Theme   
Por último, pero no menos importante... Nah, mentira, sí es menos importante, pero la quería mencionar: el _theme _para
ADWLauncher. ADWLauncher vino con CyanogenMod, y no tuve necesidad de cambiarlo. Probé varios _themes_
(desde _Settings_ \> _ADWLauncher_ \> _Themes Preferences_ \> _Get themes!_), y finalmente elegí "Minimalist."   

¿El resultado final? Un Android lindo, prolijo, (casi) libre de _apps_ innecesarias y conexiones no deseadas, y
funcionando más "_smoothly_" que nunca:  

[![](http://1.bp.blogspot.com/-dpFwq6aCUH8/T-nCxr7BD0I/AAAAAAAAAzA/fm4J264QI1w/s400/my_android.png)][32]

El _wallpaper_ lo saqué de [acá][33], el _theme_ no tenía un icono para Orbot, pero por alguna razón sí tenía uno de
[Fullmetal Alchemist][34].

Si les gusta personalizar el software que utilizan y/o quieren aprovechar más el potencial de sus dispositivos con
Android, definitivamente les diría que ustedes también se animen a meter mano. :)

[0]: http://4.bp.blogspot.com/-PZy0c6zRUDc/T-jAZ8QAZ4I/AAAAAAAAAyc/7lMPdn9hu0Y/s1600/android.jpg
[1]: https://en.wikipedia.org/wiki/Google_play
[2]: http://4.bp.blogspot.com/-UwTMUUZTz1Y/T-jEP1ad7kI/AAAAAAAAAyo/X1HZpkilScA/s1600/cyanogen.png
[3]: http://www.androidpolice.com/2010/05/01/custom-roms-for-android-explained-and-why-you-want-them/
[4]: http://www.androidpolice.com/2010/04/15/rooting-explained-top-5-benefits-of-rooting-your-android-phone/
[5]: http://www.missfilly.com.ar/2011/09/por-que-software-libre.html
[6]: http://forum.xda-developers.com/index.php
[7]: http://www.cyanogenmod.com/
[8]: http://en.miui.com/
[9]: http://www.redmondpie.com/best-most-popular-custom-roms-for-android-and-why-you-should-try-them-out/
[10]: http://www.missfilly.com.ar/2011/12/historias-de-computadoras-privacidad-y.html
[11]: http://3.bp.blogspot.com/-dp5E5JjUrnY/T-kjQ7JVygI/AAAAAAAAAy0/2NUYB7n-20A/s1600/orbot.png
[12]: http://www.market4android.com/how-to-remove-stock-android-apps.php
[13]: https://guardianproject.info/
[14]: https://guardianproject.info/apps/orbot/
[15]: https://play.google.com/store/apps/details?id=org.torproject.android
[16]: https://guardianproject.info/apps/orweb/
[17]: https://play.google.com/store/apps/details?id=info.guardianproject.browser
[18]: https://guardianproject.info/apps/gibber/
[19]: https://play.google.com/store/apps/details?id=info.guardianproject.otr.app.im
[20]: https://code.google.com/p/k9mail/
[21]: https://play.google.com/store/apps/details?id=com.fsck.k9
[22]: https://github.com/WhisperSystems/TextSecure
[23]: https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms
[24]: http://getsongbird.com/
[25]: https://play.google.com/store/apps/details?id=com.songbirdnest.mediaplayer
[26]: http://code.google.com/p/droidwall/
[27]: https://play.google.com/store/apps/details?id=com.googlecode.droidwall.free
[28]: https://guardianproject.info/apps/
[29]: https://en.wikipedia.org/wiki/List_of_Open_Source_Android_Applications
[30]: http://f-droid.org/
[31]: http://www.aopensource.com/
[32]: http://1.bp.blogspot.com/-dpFwq6aCUH8/T-nCxr7BD0I/AAAAAAAAAzA/fm4J264QI1w/s1600/my_android.png
[33]: http://www.flickr.com/photos/salendron/6976977047/in/photostream/
[34]: http://myanimelist.net/anime/5114/Fullmetal_Alchemist:_Brotherhood