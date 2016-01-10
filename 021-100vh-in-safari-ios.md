## 100vh в Сафари ИОС

В Сафари ИОС элемент с высотой в `100vh` имеет разную высоту, в зависимости от того, как Сафари посчитал высоту вьюпорта: с минимальным или полным тулбаром.

Самое интересное — это [не баг, а фича](http://nicolas-hoizey.com/2015/02/viewport-height-is-taller-than-the-visible-part-of-the-document-in-some-mobile-browsers.html).

> This is completely intentional. It took quite a bit of work on our part to achieve this effect.
