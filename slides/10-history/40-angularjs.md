## AngularJS

<div class="timeline compact">
  <div class="container right">
    <div class="content">
      <h3>2012</h3>
      <p>AngularJS</p>
    </div>
  </div>
</div>

* Miško Hevery
* Challenge: rewrite "Google Feedback Tool"
    * 17000 LoC / 6 months
    * Google Web Toolkit
    * Took 3 weeks


http://www.angularjswiki.com/angularjs/history-of-angularjs/ <!-- .element target="_blank" class="compact" -->

---

### AngularJS to the rescue!

![AngularJS](/img/AngularJS_logo.svg) <!-- .element: style="background: #fff"-->

* Extend HTML
* JQuery out-of-the box
* 2-way databinding
* Dependency injection
* Testable
* Full solution

---

### AngularJS example

```html
<body ng-app="myApp" ng-controller="calculator">

<form name="calculator">
  <input type="number" ng-model="a" name="a">
  +
  <input type="number" ng-model="b" name="b">
  =
  <input type="number" ng-model="c" name="c">
</form>
<input ng-click="calculate()" type="submit">
```

<!--.element class="compact"-->

```js
angular.module('myApp', []).controller('calculator', function($scope){
	$scope.a = 0;
    $scope.b = 0;
    $scope.calculate = function() {
      $scope.c = $scope.a + $scope.b;
    }
    $scope.calculate();
});
```

<!--.element class="compact"-->

https://www.w3schools.com/code/tryit.asp?filename=FZ8HR4LY7B8N <!-- .element target="_blank" class="reference" -->

---

### AngularJS problem

* Does not scale to enterprise big applications
    * Dramatic performance degradation 
    * No lazy loading
* Minefield of bad practices
* Does not play nice with other frameworks