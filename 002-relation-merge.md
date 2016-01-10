## About `Relation#merge`

`#merge` allows you to merge AR relations. So instead of:

```ruby
class Message < ActiveRecord::Base
  scope :unread, -> { where(read_at: nil) }
end

class Dialog < ActiveRecord::Base
  scope :with_unread_messages,
    -> { joins(:messages).where(messages: { read_at: nil }) }
end
```

You could do:

```ruby
class Dialog < ActiveRecord::Base
  scope :with_unread_messages, -> { joins(:messages).merge(Message.unread) }
end
```