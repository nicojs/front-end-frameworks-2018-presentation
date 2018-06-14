## JavaScript

<div class="timeline compact">
 <div class="container right">
    <div class="content">
      <h3>1995</h3>
      <p>JavaScript</p>
    </div>
  </div>
</div>

* Introduced as *Mocha* by **Brendan Eich**
* Netscape Navigator
* Written in 10 days
* Make the web more dynamic

---

### JavaScript example

```html
<form name="calculator">
  <input type="text" name="a">
  +
  <input type="text" name="b">
  =
  <input type="text" name="c">
</form>
<input type="submit" onclick="calculate()">

<script>
function calculate() {
  var calculatorForm = document.forms.calculator;
  calculatorForm.c.value = parseInt(calculatorForm.a.value) 
  + parseInt(calculatorForm.b.value);
}
</script>
```

<!-- .element class="compact" -->

https://www.w3schools.com/code/tryit.asp?filename=FSA1BH9NLKHR <!-- .element target="_blank" class="reference" -->

---

### JavaScript evolution

* ~ Since 2005
    * AJAX, JQuery, ES5
* Douglas Crockford's book

![js-good-parts](/img/js-good-parts.jpg) <!--.element class="img-width-300"-->


---

### JavaScript nowadays

* Specification updated yearly
    * ES2015, ES2016, ES2017, ES2018
* Proposals right in the open
    * [github.com/tc39/proposals](https://github.com/tc39/proposals#readme) <!-- .element target="_blank" -->