## About `#safe_constantize`

The `String#constantize` method converts a string to the constant (class, module) that the string contains or throws a `NameError` if there is no such constant.

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

Fortunately, there is `#safe_constantize` which returns `nil` if there is no such constant:

```ruby
def category_class
  "Category::#{target_type}".safe_constantize || Category::Default
end
```
