## Как использовать ES6/ES2015 в Middleman 4

Middleman 4 работает с Sprockets 3.x, который давно умеет ES6. Устанавливаем `sprockets-es6` и
просим `middleman-sprockets` обрабатывать и `.es6` файлы:

```ruby
# Gemfile

gem "middleman-sprockets", "~> 4.0.0.rc"
gem "sprockets-es6"
```

```ruby
# config.rb

require "sprockets/es6"
activate :sprockets do |s|
  s.supported_output_extensions << ".es6"
end
```

Если нужны полифилы:

```javascript
// application.js.es6

//= require babel/polyfill
```
