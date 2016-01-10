# Быстрый тап в Сафари

В Сафари ИОС [убирают задержку в 350мс у тапа](https://webkit.org/blog/5610/more-responsive-tapping-on-ios/). Быстрый тап включается в следующих ситуациях:

* страница не зумится (user-scalable=no или minimum-scale равный maximum-scale);
* `width=device-width` в начальном зуме;
* в стилях у элемента `touch-action: manipulation`.