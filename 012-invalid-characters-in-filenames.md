## About filenames

There are some [characters that can't be used in filenames](https://en.wikipedia.org/wiki/Filename#Reserved_characters_and_words):

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
