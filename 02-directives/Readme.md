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