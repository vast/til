## Как пользоваться упрощениями в CoffeeScript

Пользуйтесь упрощениями, если это возможно. Вместо:

```coffee
results = []

for item in array
  results.push(item.name)
```

Используйте:

```coffee
results = (item for item in array)
```

А если фильтруете:

```coffee
inputs = (input for input in inputs when input.type isnt "hidden")
```
