## Polymer

![polymer](/img/polymer.svg) <!-- .element class="emblem logo-emblem" -->

* By Google (Chrome)
* Called a "Library" by the team
* Embrace the web
* Goal is to *become obsolete*

---

### Example

```js
class CalculatorElement extends PolymerElement {
  
  static get template() { return html`
    <form name="calculator">
    <input type="number" name="a" on-change="update"> +
    <input type="number" name="b" on-change="update"> =
    <input type="number" name="c" value="{{c}}">
  </form>
  <button on-click="calculate">Calculate</button>    
  `; }
  
  static get is() { return 'calculator-element'; }
  
  update(event) { this[event.target.name] = parseInt(event.target.value); }
  calculate() { this.c = this.a + this.b; }
}

window.customElements.define(CalculatorElement.is, CalculatorElement);
```

<!-- .element class="compact" -->

```html
<calculator-element></calculator-element>
```

<!-- .element class="compact" -->

https://www.w3schools.com/code/tryit.asp?filename=FSAA3P3H7YOR <!-- .element target="_blank" class="reference" -->

---

### Focus

Polymer is counter-reaction to frameworks like React and Angular

* Focus on enabling the HTML's full potential
* Focus on progressive web apps
* *Polyfill* missing functionality 

---

### Releases

* Polymer 1: ES5 syntax with HTML Imports
* Polymer 2: ES6 syntax with HTML Imports
* Polymer 3: ES6 syntax with ES Modules

Big changes in each major release so far

---

### Criticism

* No real change detection
* No helpful error messages (white screen)
* Big changes in major releases 