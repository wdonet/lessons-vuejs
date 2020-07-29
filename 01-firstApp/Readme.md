## First App

1. Create a basic HTML in `index.html`
2. Include the script at [documentation](https://vuejs.org/v2/guide/installation.html)
```html
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```
3. Have a `<div>` with `id="app"` for linking the js code below to the DOM
```js
var app = new Vue({
  el: '#app',
  data: {
    product: 'Socks'
  }
});
```
4. Inside div, add any other container like a `h1` tag for displaying product value using `{{}}`.
5. Now add two different tag elements pointing to `{{product}}` and open Dev Tools to change `app.product` value to anyting else.
```html
  <h1>{{product}}</h1>
  <p>My product is {{product}}</p>
```

_Check how value in DOM also changes_

### Bind data to attribute
1. Create a link tag and a link property of data inside Vue instance
```html
<a :href="link">Search</a>
```
_The long way to do this is `v-bind:href`, the shorthand is only using a colon `:`_

```js
var app = new Vue({
  el: '#app',
  data: {
    product: 'Socks'
    link: 'https://www.google.com/search?q=product'
  }
});
```
