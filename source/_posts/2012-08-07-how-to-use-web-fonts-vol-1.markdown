---
layout: post
title: "How-to use web fonts: vol. 1"
date: 2012-08-07 20:56
comments: true
categories:
---

HTML5 web fonts are awesome! On the web, it was previously only possible to use fonts already installed on the user-agent's operating system. No more! Since I had not yet actually embedded any web fonts myself, I stumbled upon some problems. This post shares my advice that I got from the internets.

<!-- more -->

The Big Picture
===============

1. You need the actual [font data](http://www.google.com/webfonts/).
2. [You need a license](http://www.adobe.com/aboutadobe/antipiracy/ff_faq.html) to use the font.
3. The font data may be embedded inside a CSS file or linked from a font file.
4. If you are viewing a local file, you may not link the font outside your local filesystem.


Details
=======

You may either link the font file or embed it inside your CSS file. Requesting many external downloads will slow down the load time of your page. Therefore it is preferred trying not to add too many references to external resources and consider embedding the fonts inside a common CSS file. For example:
    <link href='/style/fonts.css' rel='stylesheet' type='text/css'>

The embedded fonts are encoded in Base64 format. I found [a handy service](http://base64fonts.com/) which does the formatting: you only need to upload the font file. (They also get a copy of all the submitted fonts. Clever way to collect them..)

The embedded font inside the CSS file looks like the following:

    @font-face {
      font-family: 'MinionPro';
      src: url(data:font/OpenType;charset=utf-8;base64,[...font data...]) format('OpenType');
      font-weight: normal;
      font-style: normal;
    }

The font may also be linked as follows.

    @font-face {
      font-family: 'MinionPro';
      src: url('/style/fonts/minion-pro.ttf');
    }

A good place to find free fonts is [Google Web Fonts](http://www.google.com/webfonts/). Most of fonts require a commercial license. However, you may have a right to use some fonts if you own an applicable software licence. [Unauthorized copying of fonts](http://www.adobe.com/aboutadobe/antipiracy/ff_faq.html) is against most copyrights, so you should check the licenses carefully for commercial use.

Note that if you are viewing your page directly from a local file, the browser's same-origin policy does not allow linking files outside your local file system. That is, for example Google Web Fonts may not work without using a local webserver.

Summary: Web will get a facelift since layouts are no longer restricted to Helvetica, Verdana, Lucida &amp; co!