## Как правильно использовать gulp-changed с Jade/Pug

Чтобы gulp-changed правильно отслеживал изменения в шаблонах, ему надо подсказать расширение:

```javascript
return gulp.src(templates)
    .pipe($.changed('.build', { extension: '.html' }))
    .pipe($.jade())
    .pipe(gulp.dest('.build'));
```
