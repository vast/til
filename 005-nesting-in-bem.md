## About nesting in BEM

In BEM blocks should have plain structure. There is no need to repeat DOM nesting in BEM classes:

```css
.nav__item__link { }
```

You won't be able to reuse this element in another context or refactor later.

To reflect nesting it's enough to use only DOM:

```html
<ul class="nav">
  <li class="nav__item">
    <a class="nav__link"></a>
  </li>
</ul>
```