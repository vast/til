## How to use comprehensions in CoffeeScript

Take advantage of comprehensions whenever possible. Instead of:

```coffee
results = []

for item in array
  results.push(item.name)
```

Use:

```coffee
results = (item for item in array)
```

With filtering:

```coffee
inputs = (input for input in inputs when input.type isnt "hidden")
```