## JQuery

<div class="timeline compact">
  <div class="container left">
    <div class="content">
      <h3>2005</h3>
      <p>JQuery</p>
    </div>
  </div>
</div>

* Browser compatibility was bad!
    * Selecting elements
    * Event handler
    * Iterating an array

---

### JQuery to the rescue!

* Add event
* Use css selectors to select elements
* Iterate arrays
* 90% adoption world wide!
* Separation of behavior, structure and design

---

### JQuery example

```html
<form name="calculator">
  <input type="text" name="a">
  +
  <input type="text" name="b">
  =
  <input type="text" name="c">
</form>
<input type="submit">
```

```js
$(document).ready(function(){
    $('input[type=submit]').click(function(){
        $('input[name=c]').val(
        	parseInt($('input[name=b]').val()) + parseInt($('input[name=a]').val()));
    });
});
```

<!-- .element class="compact" -->


https://www.w3schools.com/code/tryit.asp?filename=FZ8GU61OPDPG <!-- .element target="_blank" class="reference" -->


---

### JQuery problem 🍝

![jquery-bad-example](/img/jquery-bad-example.png)


