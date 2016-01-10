# Режим песочницы у Рельсовой консоли

`bin/rails c -s` запустит консоль в режиме песочницы. В конце сеанса Рельсы откатят все изменения, сделанные в ней:

```
bin/rails c -s
Loading development environment in sandbox (Rails 4.2.4)
Any modifications you make will be rolled back on exit
```