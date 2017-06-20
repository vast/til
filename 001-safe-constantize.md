## Про `#safe_constantize`

Метод `String#constantize` конвертирует строку в константу (класс, модуль) или бросает `NameError`, если такой константы нет.

```ruby
def category
  category_class.new(self)
end

def category_class
  "Category::#{target_type}".constantize
rescue
  Category::Default
end
```

К счастью, обработать отсутствие константы можно более эффективно. Для этого предусмотрен `#safe_constantize`, который возвращает `nil` если такой константы нет:

```ruby
def category_class
  "Category::#{target_type}".safe_constantize || Category::Default
end
```
