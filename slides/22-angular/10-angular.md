## Angular

![angular](/img/angular.svg) <!-- .element class="emblem logo-emblem" -->

* Successor to AngularJS
* By Google
* One framework for mobile & desktop
* All-in-one solution
* TypeScript out-of the box

---

### Example

```ts
@Component({
  selector: 'calculator',
  template: `<form name="calculator">
  <input type="number" [(ngModel)]="a" name="a">
  +
  <input type="number" [(ngModel)]="b" name="b">
  =
  <input type="number" [(ngModel)]="c" name="c">
</form>
<button (click)="calculate()">Calculate</button>`,
  styles: [/**/]
})
export class CalculatorComponent  {
  a = 0;
  b = 0;
  c: number;
  calculate(){
    this.c = this.a + this.b;
  }
}
```

<!-- .element class="compact" -->

https://angular-eqdand.stackblitz.io
<!-- .element target="_blank" class="reference" -->

---

### Developer workflow

A browser doesn't understand TypeScript

* TypeScript compilation -> Bundling -> Serve
* Usually done with Webpack
* Tests can be done with Protractor and Karma

There is an Angular CLI that helps you with this.

---

### Use cases

* Desktop applications
* Server side rendering
* Web apps
* Hybrid mobile app (Ionic)
* Native mobile app (NativeScript)

---

### Native mobile app example

Native mobile app using NativeScript

```ts
@Component({
  selector: "my-app",
  template: `
    <ActionBar title="My Apple" class="action-bar"></ActionBar>
    <Image src="~/images/apple.jpg"></Image>
  `,
  styles: [ /**/ ]
})
export class AppComponent {}
```

<!-- .element class="compact" -->

Same Angular syntax, but different bootstrap

<!-- .element class="fragment" data-fragment-index="0" -->

```ts
import { platformNativeScriptDynamic } from "nativescript-angular/platform";

import { AppModule } from "./app.module";

platformNativeScriptDynamic({ createFrameOnBootstrap: true }).bootstrapModule(AppModule);
```

<!-- .element class="compact fragment" data-fragment-index="0" -->

---

### Release cadence

Angular adheres to Semver 2.0.0

`major`.`minor`.`patch`

* A major release every 6 months
* 1-3 minor releases for each major release
* A patch release almost every week

Every major release is supported for 18 months

---

## Angular Criticism

* Too little too late
    * Announced in 2014, released in sept 2016
    * Many enterprises couldn't wait that long
    * https://medium.com/@chriscordle/why-angular-2-4-is-too-little-too-late-ea86d7fa0bae <!-- .element target="_blank" class="reference" -->
* Steep learning curve
    * Bad API design in some places
        * https://codeburst.io/how-i-stopped-loving-angular-c2935f7378c4 <!-- .element target="_blank" class="reference" -->
    * [Info Support training](https://training.infosupport.com/trainingen/building-professional-single-page-applications-with-angular) <!-- .element target="_blank"--> is 4 days
    * Positive point: there is a CLI
