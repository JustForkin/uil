<img src="http://lo-th.github.io/uil/examples/img/uil.png"/> uil v1.0

uil.js is a lightweight ui for javascript with some svg.
[**example**](http://lo-th.github.io/uil/index.html)

**1 - init engine**
```sh
var ui = new UIL.Gui( { css:'top:145px; left:50%;', size:300, center:true } );
```
**2 - add value**
```sh
ui.add('title', { name:'Title'});
ui.add('bool', { name:'Bool', callback:callback});
ui.add('color', { name:'Color', callback:callback, type:'html', value:0xff0000});
ui.add('color', { name:'Color', callback:callback, type:'rgba', value:[0,1,1,1]});
ui.add('slide', { name:'Slide', callback:callback, value:50});
ui.add('string', { name:'String', callback:callback, value:'welcome to uil'});
ui.add('list', { name:'List', callback:callback, list:['item1', 'item2', ...]});
ui.add('number', { name:'Number', callback:callback, value:20, min:0, max:10, precision:2, step:0.01 });
ui.add('number', { name:'Vector2', callback:callback, value:[0,0] });
ui.add('number', { name:'Vector3', callback:callback, value:[0,0,0] });
ui.add('number', { name:'Vector4', callback:callback, value:[0,0,0,0] });
```
**3 - callback is simple function easy to define**
```sh
var callback = function(value){ debug.innerHTML = value; }
// you can also set like that 
ui.add('number', { name:'Vector4', value:[0,0,0,0] }).onChange( function(v){ debug.innerHTML = v; } );
```
**4 - you can reset all value**
```sh
ui.clear();
```

[**uil_listen**](http://lo-th.github.io/uil/examples/uil_listen.html)

[**uil_stresstest**](http://lo-th.github.io/uil/examples/uil_stresstest.html)

[**uil_test**](http://lo-th.github.io/uil/examples/uil_test.html)
