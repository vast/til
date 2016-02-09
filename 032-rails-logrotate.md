## Как ротировать логи Рельсами

Кабум!

```ruby
# config/environments/staging.rb

config.logger = ActiveSupport::TaggedLogging.new(
  Logger.new(config.paths["log"].first, 10, 50.megabytes) # 10 файлов по 50 Мб
)
```
