## requestIdleCallback

В 47-м Хроме у `requestAnimationFrame` появился напарник — функция `requestIdleCallback`. Браузер запустит переданный ей колбек в свободное от работы время. Как и когда использовать —  читайте [Google Developers](https://developers.google.com/web/updates/2015/08/using-requestidlecallback).

В остальных браузерах ее пока нет, но есть что-то похожее:

* [https://gist.github.com/paullewis/55efe5d6f05434a96c36](https://gist.github.com/paullewis/55efe5d6f05434a96c36);
* [https://github.com/aFarkas/requestIdleCallback](https://github.com/aFarkas/requestIdleCallback).
