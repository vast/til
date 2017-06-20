## Как исправить `git push --force`

```
$ git push --force origin master

...
a1a1a1..b2b2b2 master -> master
```

Без паники. `a1a1a1` – последний коммит в удалённой ветке `master` до пуша, поэтому мы можем вернуться к нему так:

```
$ git reset --hard a1a1a1
$ git push --force origin master
```
