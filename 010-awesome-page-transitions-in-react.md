## How to Animate Components Transition with React and React Router

To animate routing transitions with React Router use `[CSSTransitionGroup](https://facebook.github.io/react/docs/animation.html)` component and a bit of CSS:

```jsx
render() {
  const name = this.context.router.getCurrentPath()

  return (
    <CSSTransitionGroup
      component="div"
      transitionName="application_container"
      transitionLeave={false}>

      <RouteHandler key={name} />

    </CSSTransitionGroup>
  )
}
```

```css
.application_container-enter::before {
  position: fixed;
  top: 0;
  left: 0;

  width: 1%;

  content: "";
  transition: width .3s;

  border-bottom: 5px solid $text-color;
}

.application_container-enter.application_container-enter-active::before {
  width: 100%;
}
```

<DEMO>

