# Reagent

[Reagent](https://reagent-project.github.io/) provides a ClojureScript interface to React.js, greatly simplifying the development of single page apps and web user interfaces.

Reagent apps are extremely fast due to the use of immutable data structures, which makes calculating Virtual DOM changes extremely efficient.

- React components are ClojureScript functions.
- State is held in ClojureScript data structures.
- A User interface is generated using a simple [Hiccup syntax](../introduction/hiccup-style-syntax.md).

!!! INFO "Reagent uses the JSX approach"
    Those familiar with React may wondering where the boilerplate calls to `createClass`, `componentDidMount`, `render`, etc. are, these are simply not needed in Reagent.

[Reagent Rocks tutorial](http://www.mattgreer.org/articles/reagent-rocks/#on-to-reagent){target=_blank .md-button}


## Designing a Reagent app

A simple reagent app consists of 3 main sections

* state - shared between one or more components
* components - behavior of the application, such as rendering content
* rendering - render components and update them when state changes


### State

The application state is modeled using Clojure data structures, e.g. hash-maps, vectors, contained within a reagent atom.

A reagent atom is a mutable container into which new values can be swapped or reset in a controlled way (Software Transactional Memory)

### Components as functions

A Reagent component is a function that returns a vector containing a keyword and a string.

```clojure
(defn hello []
  [:div "I am a reagent component, defining HTML content using the hiccup style syntax"])
```

This is the Reagent equivalent to `React.createElement('div', null, 'hello world')` in React.

> With Reagent there is no distinction between React elements and components, they’re all defined as ClojureScript functions.


### Rendering

<!-- TODO: add description of reagent rendering -->
