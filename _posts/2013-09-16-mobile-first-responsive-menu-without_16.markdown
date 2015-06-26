---
layout: post
title: Mobile-first responsive menu without Bootstrap
date: '2013-09-16T13:32:00.000-03:00'
author: Filly
tags:
- tutorial
- software libre
- programación
- browser
modified_time: '2014-01-06T15:01:31.226-02:00'
blogger_id: tag:blogger.com,1999:blog-6145090415061302130.post-5371095719602876069
blogger_orig_url: http://missfillys.blogspot.com/2013/09/mobile-first-responsive-menu-without_16.html
---
I found [this useful Codrops' tutorial][0] for creating a responsive menu that looks good in mobile, tablets and
desktop. It is a very complete and includes a beautiful design, but there were a lot of things I had to change from
it in order to adapt it to my needs. For example, I didn't want to use that design (I was looking for a
[Bootstrap Navbar][1]-like menu, but I wanted it to be more flexible, to respond to vertical-align, etc.), I was
interested in using a mobile first approach, etc. So here is a base version of a responsive mobile-first menu, so you
can add your own pretty CSS to it without overwriting another person's (but remember this **[doesn't support < Internet
Explorer 8][2]**).  

[Here is a jsFiddle][3] with a demo of the complete code. I repeat, this code, including the CSS, just makes the menu
functional, **it's just a base code, meaning I don't add any extra styles, so you can use your own**.  

### 1\. Setting up

We will be using JQuery, so make sure to [get it][4] and add it your project.  

Get a CSS reset script, I always use Eric's Meyer "Reset CSS", which you can find [here][5].  

Also, remember to use the [viewport meta tag][6] inside your __ when working mobile-first.  

    <meta name="viewport" content="width=device-width, initial-scale=1" />

### 

### 2\. The menu HTML

I'll use my website's name on the left, and the navigation on the right. In my project I used an image inside the
`<h1\>` tag, but we'll keep it simple using just the name now.  

{% highlight html %}
<header>  
    <div id="header-wrapper">  
        <div id="logo-wrapper">  
             <h1>My website</h1>  
        </div>  
        <nav id="main-nav">  
            <ul>  
                <li class="nav-li"><a href="#">Link 1</a></li>  
                <li class="nav-li"><a href="#">Link 2</a></li>  
                <li class="nav-li"><a href="#">Link 3</a></li>  
                <li class="nav-li"><a href="#">Link 4</a></li>  
            </ul>  
        </nav>  
    </div>  
</header>
{% endhighlight %}

### 3\. Adding the menu button for small screens

Just like in the Codrops' tutorial, I'll add the button through JavaScript to keep the HTML cleaner,
but this time using JQuery:  

{% highlight javascript %}
// Adding the menu button inside a div. This div will help us align the menu to the left.  
$('<div id="menu-btn-wrapper"><button id="menu-btn">Menu</button></div>').insertAfter('h1');  

$('#menu-btn').click(function () {
    $('#main-nav').toggleClass('active');  
});
{% endhighlight %}

### 4\. The CSS

Following the mobile-first approach, we'll set the style for the small screen first, then overwrite them when necessary,
as the screen width increases. The comments will speak for themselves.  

{% highlight css %}
/* Eric Meyer's Reset CSS v2.0 - http://cssreset.com */  
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{border:0;font-size:100%;font:inherit;vertical-align:baseline;margin:0;padding:0}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:none}table{border-collapse:collapse;border-spacing:0}  

/* Display the logo/website name and menu button alongside each other */  
#logo-wrapper, #menu-btn-wrapper {  
    display: inline-block;  
    width: 50%;  
}  
/* Send menu button to the right */  
#menu-btn-wrapper {  
    text-align: right;  
}  
#menu-btn, #logo-wrapper h1 {  
    vertical-align: middle;  
}  
/* Don't show the navigation links by default */  
#main-nav > ul {  
    max-height: 0em;  
    overflow: hidden;  
}  
/* Unhide the navigation links when menu button is pressed */  
 #main-nav.active > ul {  
    max-height: 30em;  
}  
.nav-li {  
    text-align: center;  
}  
/* Force links to occupy as much space as they can (the entire screen width) */  
.nav-li a {  
    display: block;  
}  

/* Overwriting CSS rules for screens wider than 34.688em (555px) */  
@media (min-width: 34.688em) {  
    /* Hide menu button */  
    #menu-btn-wrapper {  
        display: none;  
    }  
    /* Show navigation links by default */  
    #main-nav > ul {  
        max-height: 30em;  
    }  
    /* Display links in two columns */  
    .nav-li {  
        width: 50%;  
        float: left;  
        display: inline-block;  
    }  
}  

/* Overwriting CSS rules for screens wider than 48.125em (770px) */  
@media (min-width: 48.125em) {  
    /* Display the entire navigation bar and the logo alongside eacth other, like we did with the menu button */  
    #main-nav {  
        display: inline-block;  
        width: 50%;  
        margin-left: -5px;  
        text-align: right;  
    }  
    .nav-li {  
        float: none;  
        width: auto;  
    }  
}  
{% endhighlight %}

[0]: http://tympanus.net/codrops/2013/05/08/responsive-retina-ready-menu/
[1]: http://webdesign.tutsplus.com/tutorials/htmlcss-tutorials/twitter-bootstrap-101-the-navbar/
[2]: http://caniuse.com/inline-block
[3]: http://jsfiddle.net/Filly/qU7zL/1/
[4]: http://jquery.com/
[5]: http://www.cssreset.com/
[6]: https://developer.apple.com/library/ios/DOCUMENTATION/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html