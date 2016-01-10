## About filenames

There are a lot of [characters invalid in filenames](https://en.wikipedia.org/wiki/Filename). In short the following characters should not be used in filenames:

```
/ \ ? * : | " < >
```

To accurately strip all of them use [Zaru](https://github.com/madrobby/zaru) or `parameterize`:

```ruby
Zaru.sanitize! "  what\ver//wird:user:nput:"
# => "what erwirdusernput"
"  what\ver//wird:user:nput:".parameterize
# => "what-er-wird-user-nput"
```