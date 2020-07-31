## Events
Let's Add a `Add to Cart` button for increasing the amount of elements at the shopping cart.

### v-on:{event}
1. Add a `v-on:click` on the new button tag for Cart
2. The value could be a js expression like `cart += 1` or a function (`addToCart`) this case defined at the Vue instance.
```js
  const app = new Vue({
    //...
    methods: {
      addToCart: function () {
        this.cart +=1;
      }
    }
  });
```

Let's add another event when mouse is over the colors in order to change displayed picture.

1. Add another method for updating the product
```js
  const app = new Vue({
    //...
    methods: {
      //...
      updateProduct: function(variantImage) {
        this.image = variantImage;
      },
    }
  });
```
2. Add a `variantImage` at each element from the `variants` array
```js
{
  variantImage: './assets/vmSocks-green-onWhite.jpg',
}
```
3. Finally change the `<p>` tag used to display colors to add the event
```html
<p @mouseover="updateProduct(variant.variantImage)">{{variant.variantColor}}</p>
```
_This is sending the variantImage at the current iteration of the array to the recently defined fn when mouse is over_

Try other events like:
- `@click`
- `@submit` on a form
- `@keyup.enter` on a text input.  `enter` becomes a modifier which helps to know the pressed key

Check:

- [vue-cheat-sheet](https://www.vuemastery.com/vue-cheat-sheet)
- [Event Handling](https://www.vuemastery.com/courses/intro-to-vue-js/event-handling)
