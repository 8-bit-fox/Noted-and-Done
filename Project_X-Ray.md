>[!info] Inbox
>```dataview
>Task 
>where !contains(file.tags, "#project/active") and !(due or scheduled or tags) and !completed
>```


>[!warning] Missing Next Actions
>```dataview
>Table without id file.link as Project, length(map(file.tasks, (x) => contains(x.tags, "#next-action"))) as Tasks
>From #project/active and "Projekte"
>where none(map(file.tasks, (x) => contains(x.tags, "#next-action")))
>```

>[!error] Missing Tasks
>```dataview
>Table without id file.link as Project, length(map(file.tasks, (x) => contains(x.tags, "#next-action"))) as Tasks
>From #project/active and "Projekte"
>where none(map(file.tasks, (x) => contains(x.tags, "#next-action")))
>```