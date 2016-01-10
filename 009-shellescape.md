### About `shellescape`

When you need to execute some external program you'd usually use backticks or `%x()`:

```ruby
%x(mplayer #{song.file})
```

This leads you to "Command Injection" vulnerability. If `song.file` is `foo& sudo cat /etc/passwd` then Ruby will actually run:

```bash
mplayer foo& sudo cat /etc/passwd
```

To properly escape shell input use `Shellwords.shellescape`:

```ruby
%x(mplayer #{song.file.shellecape})
# runs mplayer foo\&\ sudo\ cat\ /etc/passwd
```