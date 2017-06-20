## Про `Relation#merge`

`#merge` позволяет объединять связи ActiveRecord. Вместо такого:

```ruby
class Message < ActiveRecord::Base
  scope :unread, -> { where(read_at: nil) }
end

class Dialog < ActiveRecord::Base
  scope :with_unread_messages,
    -> { joins(:messages).where(messages: { read_at: nil }) }
end
```

Можно делать так:

```ruby
class Dialog < ActiveRecord::Base
  scope :with_unread_messages, -> { joins(:messages).merge(Message.unread) }
end
```
