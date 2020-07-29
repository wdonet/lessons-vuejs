## Directives

### if-else-if
It change DOM to show/hide elements

1. Right after `<h1>` tag add 3 `<p>` tags with different legend:
  - In Stock
  - Almost sold out
  - Out of Stock
2. Use directives respectively:
  - `v-if="inventory > 10"`
  - `v-else-if="inventory > 0 && inventory <= 10"`
  - `v-else`
3. Add a new `inventory` prop at `data` Vue instance
```js
data: {
  inventory: 100,
}
```
  - Play around with the number and see changes in the DOM

### v-show
It adds inline style `display:none` for hidding element

1. Use `v-show` instead of the three p tags to show/hide the message: "In Stock"
2. Add a new `inStock` prop at `data` Vue instance with a boolean value and play around
```js
data: {
  inStock: true,
}
```

### v-for
Used for looping over collections

1. Use `v-for` at a `<li>` tag
```html
<ul>
  <li v-for="detail in details">{{detail}}</li>
</ul>
```
2. Add a new `details` array at `data` Vue instance. Each detail in the array could be a string.
```js
data: {
  details: ['80% cotton', '20% polyester'],
}
```
3. Repeat the same for `variants` where the array has objects with and id and a color.
```js
data: {
  variants: [
    {
      variantId: 2234,
      variantColor: 'green'
    },
    {
      variantId: 2235,
      variantColor: 'blue'
    },
  ],
}
```
4. Use the color as in detail case but the id to bind a key attribute for the div (very recommendable)
```html
<div v-for="variant in variants" :key="variant.variantId">
  <p>{{variant.variantColor}}</p>
</div>
```

