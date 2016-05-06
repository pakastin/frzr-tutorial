# Creating components

Components are just plain JS functions / classes. Only requirement is, that it must return an object, which has `el`-property.

ES5:
```js
function Hello () {
  this.el = el('h1', 'Hello world!');
}
```

ES6:
```js
class Hello {
  constructor () {
    this.el = el('h1', 'Hello world!');
  }
}
```

You can also define following special properties:
```js
class Hello {
  constructor () {
    this.el = el('h1',
      'Hello ',
      this.who = 'world',
      '!'
    );
  }
  update (who) {
    this.who.textContent = who;
  }
  mounted () {
    console.log('Mounted');
  }
}
```
..you can use: update, mounting, mounted, unmounting, unmounted, remounting, remounted
