## VueJS

![vue](/img/vue.svg) <!-- .element class="emblem logo-wide" -->

* Open source initiative
* Focus on performance and the view
* Comparable to React
* Scalable
* Easier to use (works with a `<script>` include)

---

### Example

```html
  <script type="text/x-template" id="calculator">
    <div>
      <form name="calculator">
        <input type="number" v-model="a" name="a">
        +
        <input type="number" v-model="b" name="b">
        =
        <input type="number" v-model="c" name="c">
      </form>
      <button @click="calculate">Calculate</button>
    </div>
  </script>
  
  <calculator></calculator>
```

<!-- .element class="compact" -->

```js
Vue.component('calculator', {
  template: '#calculator',
  data() {
    return {
      a: 0,
      b: 0,
      c: 0
    };
  },
  methods: {
    calculate(){
      this.c = this.a + this.b;
    }
  }
});
```

<!-- .element class="compact" -->

https://codepen.io/nicojs/project/editor/AnVLrb  <!--.element class="reference" target="_blank"-->

---

### Popularity

* Easy to get started
* As an alternative to React
  * Same scope
  * License debacle 
* Still a smaller developer base

https://react-etc.net/entry/your-license-to-use-react-js-can-be-revoked-if-you-compete-with-facebook <!--.element class="reference" target="_blank"-->

---

### Criticism

* More work for enterprise-style application
    * Decide and implement testing strategy
    * Bundling for production
