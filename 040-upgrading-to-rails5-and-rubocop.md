## Как Rubocop может помочь с апгрейдом до пятых Рельс

Одна из проблем при апгрейде на пятые Рельсы — переход на keyword args params в тестах контроллеров:

```ruby
# было
get :show, id: post.id, format: :json

# стало
get :show, params: { id: post.id, format: :json }
```

Чтобы Рубокоп нашел все такие места и автоматически исправил их, укажите `TargetRailsVersion: 5.0` в `.rubocop.yml` и запустите `bin/rubocop -a`.
