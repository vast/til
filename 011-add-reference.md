## About `add_reference` in Rails migrations

In Rails 4 there is `add_reference` helper for adding a reference column and its index and foreign key:

```ruby
add_reference :products, :user, index: true, foreign_key: true
```

It's the same as:

```ruby
add_column :products, :user_id
add_index :products, :user_id
add_foreign_key :products, :users, :user_id
```