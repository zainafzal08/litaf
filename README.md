# LitAF
A simple library which builds on the polymer Lit project to make it easier to use. Takes something lit and makes it litAF. This includes a set of core components you can extend to make building lit elements easier.

It's built on a strong foundation of leveraging web components and events as much as possible.

## LitAFElement

Core features are

1. Support for loading states.
2. Support for offline persistance via localstorage.
3. Support for simple lifecycle hooks that are called when all sub-webcomponents are ready to be interacted with.
4. Adds a .dispatch function which automatically generates a shadow boundary peircing event.

## LitAFInput

Built ontop of litAFElement to let you define your own input components.
Core feature are

1. Automatically sets up value getters and setters.
2. Automatically sets up input value to persist accross reloads.
2. Supports input validity checking.
3. Automatically generates events when the value changes.
4. Automatically watches children input fields and generates value change events when they change.

Basically makes it easy to create a custom input element composed of a set of smaller input components.

## LitAfRouter

Lets you define a router element which swaps out it's child content depending on the current path.

## LitAfPage

Lets you delcare the url of a page as a regex w/ group matching.

## LitAfModal

Lets you easily declare a modal which when opened will take up the viewport.

# Usage

When declaring a new lit element you would generally do something such as 

```ts
@customElement('my-web-component')
class MyWebComponent extends LitElement {
  static get styles() {
    return css``;
  }
  
  render() {
    return html``
  }
}
```
