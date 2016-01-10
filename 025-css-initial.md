# initial в CSS

Часто путаюсь со значениями по умолчанию для `max-height` (`none`, а не `auto`), `min-height` (`0`, а не `auto`) и `z-index` (`auto`, а не `0` или `none`). К счастью таких же беспамятных разработчиков как я, современные браузеры (кроме ИЕ) умеют ключевое слово `initial`:

```css
max-height: initial; /* == none */
min-height: initial; /* == 0 */
z-index: initial; /* == auto */
```

Подробнее [в спецификации](http://www.w3.org/TR/css-values/#common-keywords) и [caniuse.com](http://caniuse.com/#feat=css-initial-value).
