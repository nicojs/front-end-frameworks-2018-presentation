## Aurelia

![aurelia](/img/aurelia.svg) <!-- .element class="emblem logo-emblem" -->

* Open source framework by BlueSpire
* Focus on simplicity
* Focus on enterprise
  * Enterprise license
* TypeScript out-of-the box

---

### Example

```ts
export class Home {
  a = 0;
  b = 0;
  calculate() {
    this.c = this.a + this.b;
  }
}
```

```html
<template>
	<form name="calculator">
		<input type="number" value.two-way="a" name="a"> +
		<input type="number" value.two-way="b" name="b"> =
		<input type="number" value.two-way="c" name="c">
	</form>
	<button click.trigger="calculate()">Calculate</button>
</template>
```

<!-- .element class="compact" -->

https://codesandbox.io/s/0yj7yz61yp  <!-- .element target="_blank" class="reference" -->

---

### Focus

Started as counter reaction to Angular

* Focus on stability
* Dependency injection
