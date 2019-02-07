## AlloyTouch

библиотека для обработки касаний сенсорных экранов

Smooth scrolling, rotation, pull to refresh and any motion for the web.

## Install

```js
npm install alloytouch
```

* [https://unpkg.com/alloytouch@0.2.5/alloy_touch.js](https://unpkg.com/alloytouch@0.2.5/alloy_touch.js)
* [https://unpkg.com/alloytouch@0.2.5/alloy_touch.css.js](https://unpkg.com/alloytouch@0.2.5/alloy_touch.css.js)

## Usage

```js
var alloyTouch = new AlloyTouch({
            touch:"#wrapper",//обратная связь touch dom
            vertical: true,//не обязательный, по умолчанию true, означает - что касание монитора в вертикальном направлении
            target: target, //движущийся объект
            property: "translateY",  //перемещаемое свойство
            min: 100, //не обязательный, минимальное значение атрибута движения
            max: 2000, //не обязательный, максимальное значение свойства прокрутки
            sensitivity: 1,//не обязательный, чувствительность области касания, значение по умолчанию 1, может быть отрицательной
            factor: 1,//не обязательный, что указывает на связь между смещением движения смещения и атрибутом движения. Значение по умолчанию 1
            moveFactor: 1,//не обязательный, указывает на смещение прикосновения и атрибут отображения атрибута движения, значение по умолчанию равно 1
            step: 45,//используется для исправления целого кратного шага
            bindSelf: false,
            maxSpeed: 2, //не обязательный, ограничение максимальной скорости для сенсорной обратной связи
            initialValue: 0,
            change:function(value){  }, 
            touchStart:function(evt, value){  },
            touchMove:function(evt, value){  },
            touchEnd:function(evt,value){  },
            tap:function(evt, value){  },
            pressMove:function(evt, value){  },
            animationEnd:function(value){  } //Конец движения
 })
```

DOM может быть перемещен сам по себе через экземпляр объекта:

``` js
alloyTouch.to(value, time, ease)
```

* `value` обязательно
* `time` не обязательно, значение по умолчанию 600
* `easy` не обязательно. Значением по умолчанию является функция движения, которая ускоряется, а затем замедляется. Значением по умолчанию для версии CSS является` cubic-bezier (0.1, 0.57, 0.1, 1).


Движение DOM может быть остановлено само по себе через экземпляр объекта:

``` js
alloyTouch.stop()
```

## Demo(Mobile)

- Pull To Refresh: [http://alloyteam.github.io/AlloyTouch/refresh/pull_refresh/](http://alloyteam.github.io/AlloyTouch/refresh/pull_refresh/)
- QQ KanDian: [http://alloyteam.github.io/AlloyTouch//refresh/infinite/kandian.html](http://alloyteam.github.io/AlloyTouch//refresh/infinite/kandian.html)
- Full Page Scroll : [http://alloyteam.github.io/AlloyTouch/full_page/](http://alloyteam.github.io/AlloyTouch/full_page/)
- Simple : [http://alloyteam.github.io/AlloyTouch/example/simple.html](http://alloyteam.github.io/AlloyTouch/example/simple.html)
- 3D : [http://alloyteam.github.io/AlloyTouch/example/3d.html](http://alloyteam.github.io/AlloyTouch/example/3d.html)
- Rotate : [http://alloyteam.github.io/AlloyTouch/example/rotate.html](http://alloyteam.github.io/AlloyTouch/example/rotate.html)
- Carousel : [http://alloyteam.github.io/AlloyTouch/example/carousel.html](http://alloyteam.github.io/AlloyTouch/example/carousel.html)
- Carousel2 : [http://alloyteam.github.io/AlloyTouch/example/carousel2.html](http://alloyteam.github.io/AlloyTouch/example/carousel2.html)
- Three.js : [http://alloyteam.github.io/AlloyTouch/example/threejs/](http://alloyteam.github.io/AlloyTouch/example/threejs/)

## Related links

* [omi-touch: Omi /AlloyTouch integration](https://github.com/Tencent/omi/tree/master/packages/omi-touch)
* [AlloyTouch Wiki](https://github.com/AlloyTeam/AlloyTouch/wiki)
* [css3transform](https://github.com/Tencent/omi/tree/master/packages/omi-transform)

## License
This content is released under the [MIT](http://opensource.org/licenses/MIT) License.
