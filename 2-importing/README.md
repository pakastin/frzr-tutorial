# Importing FRZR methods
ES6 modules:
```js
import { el, text, svg, List, mount, mountBefore, replace, unmount, setChildren } from 'frzr';
```
^ btw. those are all of FRZR's methods ;)

CommonJS:
```js
var frzr = require('frzr');
var el = frzr.el;
...
```

CommonJS with ES6:
```js
const { el, mount, ... } = require('frzr');
```

Oldskool:
```html
<script src="https://frzr.js.org/frzr.min.js"></script>
```
```js
var el = frzr.el;
...
```

Serverside:
```
npm install frzr frzr-dom
```
```js
var render = require('frzr-dom').render;
var frzr = require('frzr');
var el = frzr.el;
var mount = frzr.mount;

var h1 = el('h1', 'Hello world!');

mount(document.body, h1);

console.log(render(document.body, true)); // with second parameter true renders just innerHTML 
```
