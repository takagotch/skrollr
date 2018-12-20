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

