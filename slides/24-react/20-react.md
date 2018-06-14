## React

![react](/img/react.svg) <!-- .element class="emblem logo-emblem" -->

* Facebook
* Introduced in 2013
* JSX - A JavaScript extension
    * Although you can use TSX (TypeScript)
* Focus on view

---

### Example

```jsx
class App extends Component {
  constructor() { this.state = { a: 0, b: 0, c: 0 }; }

  calculate(){
    this.setState({ c: this.state.a + this.state.b });
  }

  handleChange(event){
    this.setState({ [event.target.name]: parseInt(event.target.value) });
  }

  render() {
    return (
      <div>
        <form name="calculator">
          <input type="number" name="a" value={this.state.a} onChange={this.handleChange} /> +
          <input type="number" name="b" value={this.state.b} onChange={this.handleChange} />
          =
          <input type="number" name="c" value={this.state.c} />
        </form>
        <button onClick={this.calculate}>Calculate</button>
      </div>
    );
  }
}
```

<!--.element class="compact stretch"-->

https://stackblitz.com/edit/react-drm3v1 <!--.element target="_blank" class="reference"-->

---

### Developer workflow

A browser doesn't understand JSX

* JSX compilation -> to ES5 -> Bundling -> Serve
* Usually done with Webpack
* Tests are done with [Jest](https://www.npmjs.com/package/jest) <!-- .element target="_blank" -->

There are helpers scripts that help you: [create-react-app](https://www.npmjs.com/package/create-react-app) <!-- .element target="_blank" -->

---

### Use cases

* Desktop applications
* Server side rendering
* Web apps
* Hybrid mobile app
* Native mobile app (React Native)

---

### Popularity

React is immensely popular!

* Many switched from AngularJS 

---

### Criticism

* It's Facebook... 
* Steep learning curve
