## Про использование Рилейшенов для подзапросов

Вместо использования комбинации `pluck` + `where`, которая выполняется двумя запросами:

```ruby
project_ids = user.projects.pluck(:id)
# SELECT id FROM projects WHERE ...
Task.where(project_id: project_ids)
# SELECT * FROM tasks WHERE project_id IN (....)
```

Можно использовать рилейшен напрямую и обойтись одним запросом:

```ruby
Task.where(project_id: user.projects)
# SELECT * FROM tasks WHERE project_id IN (SELECT id FROM projects WHERE ...)
```
