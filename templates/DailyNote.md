#journal
## Aufgaben

> [!error] Overdue
> ```tasks
> filter by function task.due.moment?.isBefore(moment('<% tp.file.creation_date() %>'), 'day') || false
> not done
> ```

> [!warning] Due today
> ```tasks
> filter by function (task.due.moment?.isSame(moment('<% tp.file.creation_date() %>'), 'day') ||  task.due.moment?.isSame(moment('<% tp.file.creation_date() %>').add(1, 'days'), 'day')) || false
> not done
> ```

>[!info] Scheduled for today
>```tasks
>filter by function task.scheduled.moment?.isSame(moment('<% tp.file.creation_date() %>'), 'day') || false
>not done
>```

> [!check] Done today
> ```tasks
> filter by function task.done.moment?.isSame(moment('<% tp.file.creation_date() %>'), 'day') || false
> ```

### Notizen
