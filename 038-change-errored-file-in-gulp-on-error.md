## Как подменить сломанный .jade/.pug шаблон плейсхолдером

```javascript
gulp.src('content/*.pug')
  .pipe($.pug({ basedir: '.' }))
  .on('error', function(err) {
    this.push(new File({
      base: 'content/',
      path: err.path.replace(/\.jade/, '.html'),
      contents: Buffer.from('<h1>Fucked Up</h1>'),
    }));
    
    this.emit('end');
  })
  .pipe($.typograf({ lang: 'ru' })) // и типограф, и обработчики ниже получат плейсхолдер
  .pipe(gulp.dest('.build'));
```
