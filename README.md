Imagecover.js
==========
Imagecover is a jQuery plugin that allows an image to cover all its container.

####Author: Andrea Dell'Orco - [Adostudio](http://www.adostudio.it)
####License: Mit License
* * *
##Demo & Usage:
+ Regular Usage: (http://dev.adostudio.it/jquery/imagecover/demo.html)
+ Background Fullscreen: (http://dev.adostudio.it/jquery/imagecover/demo-background.html)
+ Background Fullscreen (with preloader): (http://dev.adostudio.it/jquery/imagecover/demo-background-loading.html)
* * *

## Install

+ Include [imagesloaded.pkgd.min.js](http://imagesloaded.desandro.com/imagesloaded.pkgd.min.js) - [Imagesloaded Plugin](https://github.com/desandro/imagesloaded)
+ Include [jquery.imagecover.js](http://dev.adostudio.it/jquery/imagecover/js/jquery.imagecover.js)

## Usage
Javascript: 
``` js
$('.containerClass').imagecover();
```
HTML Markup:
``` html
<div class="containerClass">
  <img src="img/monkey.jpg">
</div>
```
## Options
``` js
$('.containerClass').imagecover({
	runOnce	: false,
	throttle: 200 , 
	css2	: false,
	preloadAllImages:false,
	loadingClass: 'ic-loading',
	addPreload: false
});
```

+ `addPreload` _false_ / _true_ / _css-class_ : If is specified a _css-class_ (don't use . [dot] ), will be append an element _preloader_ with this class to the containers while images are loading. If is set _true_ the default class is _ic-preloader_.
+ `preloadAllImages` _false_ / _true_ : Wait the loading of all images in the containers to cover itself with the image  and to remove _ladingClass_ and _preloader_ (maybe  the container sizes depend from inner images).
+ `loadingClass` _css-class_ : Class applied to the containers while loading the image/s.
+ `css2` _false_ / _true_ : If _true_ avoid CSS3 features and force to use CSS2 procedure (used for old browsers). 
+ `runOnce` _false_ / _true_: If _true_ don't monitor costantly the changes of the conatainers and use plugin in "oneshot" mode. If browser supports CSS3 (and `css2` is not set) this options is ignored.
+ `throttle` 200 / _integer_ : Elapsed time in ms between checks the variation of the containers. (Used for `css2` and old Browser). If browser supports CSS3 (and `css2` is not set) this options is ignored.
