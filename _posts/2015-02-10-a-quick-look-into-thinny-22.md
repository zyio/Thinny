---
layout: post
title: "A quick look into Thinny 2.2"
quote: "Light of my life, fire of my loins... Dolores, the new version of Thinny, is prettier than ever!"
image:
   url: /media/2015-02-10-a-quick-look-into-thinny-22/cover.jpg
   source: http://youtube.com/watch?v=IHyTv0TM1CQ
video:
   mp4: /media/2015-02-10-a-quick-look-into-thinny-22/lolita.mp4
color: "df281a"
comments: false
---

After almost a year, I'm releasing Thinny 2.2, with great improvements from the last stable version.

This version includes:

- A redesigned menu, with sharing buttons for desktop;

- A rewritten stylesheet, using [Sass](http://sass-lang.com);

- Integration with some APIs ([Cards](https://cards.twitter.com), [Theme-Color](http://updates.html5rocks.com/2014/11/Support-for-theme-color-in-Chrome-39-for-Android) and [Transparency](https:/api.yandex.com/transparency/));

- Lots of bug fixes (thanks to all of you making pull requests!).

As a downside, the Parallax effect was causing some troubles, so it's now disabled by default. But you can still use it by setting the `parallax` variable to `true`. I'll try to redo it for 2.3, and I'd appreciate [your help](https://github.com/camporez/Thinny/tree/dev).

Now, let's take a look at some things you need to know for writing beautiful posts on Thinny... I hope you enjoy it!

# Using Thinny

## Global variables

Global variables are set on the `_config.yml` file.

They are responsible for the site configuration, for the common settings in all pages (like the menu items and the social links), and for the default values for some variables.

### Menu

Inside the `menu` variable you can put all the links you want to display on the menu.

For each entry you'll have to declare the `title` and the `url`. Example:

~~~
menu:
  title:        Portfolio
  url:          /portfolio
~~~

### Social links

The social icons are provided by [Genericons](http://genericons.com/). Each entry has an `icon` (you can see all the icons on [the Genericons website](http://genericons.com/)), a `url` and a description (`desc`).

~~~
social:
  - icon:         reddit
    url:          https://reddit.com/r/jekyll
    desc:         Subscribe on reddit
~~~

### Comments

To enable comments, you have to set the `commentsystem` variable to either `disqus` or `google`.

If you choose Disqus, you'll need to set your username inside the variable `disqus`.

## Page variables

The page variables are set on the beginning of every post or page. Some of then are required, but others are optional.

### Title and quote

The `title` variable sets a title for your post, and it's required.

The `quote` variable is optional. It must be a small (about the size of a tweet) subtitle for your post.

### Page cover

On the top of your post, a full width and height image or video will be displayed. This image should be related to your post, and if no image/video is set the default cover in `_config.yml` will be used.

You can use just an image, or also include a video (if on mobile, or if the browse don't have video support, the image will be displayed instead).

You can also include a URL pointing to the source of the cover image/video, this will add a small icon on the bottom right of the cover image. Clicking this icon will open the source link in a new tab.

The video should be at least in one of the three available formats (mp4, webm and ogv), but using two of them is recommended.

This is how the `image` and `video` variables should look like:

~~~
image:
   url: [URL]
   source: [source URL]
video:
   mp4: [mp4 URL] 
   webm: [webm URL]
   ogv: [ogv URL]
~~~

All of this is optional.

### Colors

Each post can use a different color for its links, and if no `color` variable is set the default one in `_config.yml` will be used.

This color will also be used [on Android Lollipop](http://updates.html5rocks.com/2014/11/Support-for-theme-color-in-Chrome-39-for-Android).

~~~
color: "00b5f5"
~~~

{% include image.html url="/media/2015-02-10-a-quick-look-into-thinny-22/lollipop.jpg" description="Colorful toolbar on Android Lollipop's Chrome." %}

### Comments

Comments can be enabled/disabled per post, all you have to do is set the `comments` variable to `true` or `false`:

~~~
comments: true
~~~

# Getting Thinny

## Versions

|----
| Version | Codename | Platform | Release date
|:-:|:-:|:-:|:-:
| [0.3](https://github.com/camporez/Thinny/releases/tag/v0.3-alexandra) | [Alexandra](http://nikita2010.wikia.com/wiki/Alexandra_Udinov) | Ghost 0.3.x |November 2013 
| [2.0](https://github.com/camporez/Thinny/releases/tag/v2.0-bianca) | [Bianca](http://memoriaglobo.globo.com/programas/entretenimento/novelas/caras-bocas/caras-bocas-bianca-isabelle-drummond.htm) | Jekyll | January 2014 |
| [2.1](https://github.com/camporez/Thinny/releases/tag/v2.1-cosette) | [Cosette](http://lesmiserables.wikia.com/wiki/Cosette) | Jekyll | February 2014 
| [2.2](https://github.com/camporez/Thinny/releases/tag/v2.2-dolores) | [Dolores](http://en.wikipedia.org/wiki/Dolores_Haze) | Jekyll | February 2015
| [2.3](https://github.com/camporez/Thinny/releases/tag/v2.3-evey) | [Evey](http://en.wikipedia.org/wiki/Evey_Hammond) | Jekyll | *Stay tuned* 
|----

## Download

> You can download Thinny 2.2 [on GitHub](https://github.com/camporez/Thinny/releases).

-----
Want to see something else added or report a bug? [Open an issue](https://github.com/camporez/Thinny/issues/new).

