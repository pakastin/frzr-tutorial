# Creating HTML elements
Regular elements:
```js
var h1 = el('h1', 'Hello world!');

mount(document.body, h1);
```
Text nodes:
```js
var who = text('world');

var hello = el('h1',
  'Hello ',
  who
);
```
SVG elements:
```js
var graphic = svg('svg', 
  svg('circle', { cx: 50, cy: 50, r: 50 })
);
```

next: [Creating components](https://github.com/pakastin/frzr-tutorial/tree/master/4-creating-components)
