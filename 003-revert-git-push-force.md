## How to revert `git push --force`

```
$ git push --force origin master

...
a1a1a1..b2b2b2 master -> master
```

Don't panic. Here `a1a1a1` is the latest commit in remote `master` before the push. So we can return to it by doing:

```
$ git reset --hard a1a1a1
$ git push --force origin master
```