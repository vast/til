## About Using Relations as Subqueries

Instead of using `pluck` + `where` combo which runs two queries:

```ruby
project_ids = user.projects.pluck(:id)
# SELECT id FROM projects WHERE ...
Task.where(project_id: project_ids)
# SELECT * FROM tasks WHERE project_id IN (....)
```

You can use relation directly and have only one query:

```ruby
Task.where(project_id: user.projects)
# SELECT * FROM tasks WHERE project_id IN (SELECT id FROM projects WHERE ...)
```