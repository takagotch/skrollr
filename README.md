### skrollr
---
https://github.com/Prinzhorn/skrollr

https://github.com/Prinzhorn/skrollr/tree/master/examples#examples

```
<script type="text/javascript" src="skrollr.min.js"></script>
<script type="text/javascript">
  var s = skrollr.init();
</script>

<div data-0="background-color:rgb(0,0,255);" data-500="background-color:rgb(255,0,0);">WOOOT</div>

<div data-0="backgrond-color:rgb(0,0,255);transform:rotate(0deg);" data-500="background-color:rgb(255,0,0);transform:rotate">

<div data-0="background-color:rgb(0,0,255);transform[bounce]:rotate(0deg);" data-top="background-color:rgb(255,0,0);transform[bounce]:rotate(360deg);">WOOOT</div>

<div data-_foobar="left:0%;" data-_foobar--100="left:50%;" data-_foobar-100="left:100%;"></div>
<div data-1337="left:0%;" data-1237="left:50%;" data-1437="left:100%;"></div>

<polygon
  points='426,700 -200,720 -200,0 955,0'
  data-0="@points: 426,720 -200,720 -200,0 955,0"
  data-500="@points:380,720 -200,720 -200,0 1302,0">
</polygon>
```

```js
require(['skrollr'], function(skrollr){
  var s = skrollr.init();
});

require(['skrollr'], function(skrollr){
  skrollr.init();
});

skrollr.init({
  constants: {
    foobar: 1337
  }
});

skrollr.init({
  constants: {
    foo: function(){
      return Math.random() * 100;
    },
    vh: '100p'
  }
});

function(){
  return (/Android|iPhone|iPad|iPad|BlackBerry/i).test(navigator.userAgent || navigator.vendor || window.opera);
}

function(p){
  return 0.5;
}

skrollr.init({
  render: function(data){
    console.log(data.curTop);
  }
});

skrollr.init({
  keyframe: function(element, name, direction){
  }
});

document.querySelector('#foo').addEventListener('skrollr.dataTopBottom.up', function(){
}, false)

skrollr.init({
  easing: {
    wtf: Math.random,
    inverted: function(p){
      return 1 - p;
    }
  }
});

t5(p*p*p*p*p) + t4(p*p*p*p) + t3(p*p*p) + t2(p*p) + t*p

easeOutElastic: function(p){
  return 56*(p*p*p*p*p) - 175*(p*p*p*p) + 200(p*p*p) - 100*(p*p) + 20*p;
}

var offset = s.relativeToAbsolute(document.getElementById('foo'), 'top', 'bottom');
```

```json
{
  curTop: 10,
  lastTop: 0,
  maxTop: 100,
  direction: 'down'
}
```

```js
// skrollr/exs/scripts/main.js
require.config({
  baseUrl: "../dist",
  paths: {
    'skrollr' : "skrollr.min"
  },
  waitSeconds: 15
});

require(['skrollr'], function(skrollr){
  var s = skrollr.init({
    edgeStrategy: 'set',
    easing: {
      WTF: Math.random,
      inverted: function(p) {
        return 1-p;
      }
    }
  });
});

// src/skrollr.js
(function(window, document, undefined) {
  'use strict';
  
  var skrollr = {
    get: function() {
      return _instance;
    },
    init: function(options) {
      return _instance || new Skrollr(options);
    },
    VERSION: '0.6.30'
  };
  
  var hasProp = Object.prototype.hasProperty;
  var Math = window.Math;
  var getStyle = window.getComputedStyle;
  
  var documentElement;
  var body;
  
  var EVENT_TOUCHSTART = 'touchstart';
  var EVENT_TOUCHMOVE = 'touchmove';
  var EVENT_TOUCHCHANCEL = 'touchcancel';
  var EVENT_TOUCHEND = 'touchend';
  
  
  
  var _instance;
  
  var _skrollables;
  
  var _skrollrBody;
  
  var _listeners;
  var _forceHeight;
  var _maxKeyFrame = 0;
  
  var _scale = 1;
  var _constants;
  
  var _mobileDeceleration;
  
  var _direction = 'down';
  
  var _lastTop = -1;
  
  var _lastRenderCall = _now();
  
  var _lastViewportWidth = 0;
  var _lastViewportHeight = 0;
  
  var _requestReflow = false;
  
  var _scrollAnimation;
  
  var _smoothScrollingEnabled;
  
  var _smoothScrollingDuration;
  
  var _smoothScrolling;
  
  var _forceRender;
  
  var _skrollableIdCounter = 0;
  
  var _edgeStrategy;
  
  var _isMobile = false;
  
  var _movileOffset = 0;
  
  var _translateZ;
  
  var _reigsterdEvents = [];
  
  var _animFrame;
  
  if(typeof define === 'function' && define.amd) {
    define([], function() {
      return skrollr;
    });
  } else if (typeof module !== 'undefined' && module.exports) {
    module.exports = skrollr;
  } else {
    window.skrollr = skrollr;
  }
  
})(window, document);

```
