#project/active
## Gesammelte Aufgaben

```tasks
filter by function \
	const title = 'Klimbim'; \
	const tag = '#klimbim'; \
	return task.heading?.includes(title) || task.tags.find((t) => t === tag) && true || false;
```
## Explizite Aufgaben

## Journal

```dataview
List
FROM "journal"
WHERE icontains(file.lists.tags, "#klimbim") or contains(file.outlinks, this.file.link)
```
## Notizen