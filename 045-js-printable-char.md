## Как в JS определить, ввел ли пользователь печатный символ

`keydown` и `keyup` возникают при нажатии любых клавиш, включая функциональные: Ctrl, Cmd, F1, ...
`keypress` возникает при нажатии _символьной_ клавиши и помогает получить код-символа.

К сожалению, `keypress` срабатывает при нажатии символьных клавиш, дающих непечатный символ: например, ctlr+g дает непечатный символ с кодом 7.

Железобетонный способ проверить, печатный ли символ ввел пользователь, — пробник. Вставляем то, что пользователь ввел, в ДОМ и смотрим ширину элемента:

```js
const .$probe = $('<span></span')
  .css({ position: 'fixed', left: '-1000px', bottom: 0 })
  .appendTo('body')

$el.on('keypress', () => {
  const char = String.fromCharCode(e.charCode)
  if (!char || !char.length) return

  if ($probe.html(char).width() > 0) {
    // handle printable char `char`
  }
})
```
