# Creating components

Components are just plain JS functions / classes. Only requirement is, that it must return an object, which has `el`-property. You can mix and match components and HTMLElements like you want.

ES5:
```js
function Hello () {
  this.el = el('h1', 'Hello world!');
}
mount(document.body, new Hello());
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
