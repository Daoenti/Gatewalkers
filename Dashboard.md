# Dashboard

## Party
```dataview
table without ID link(file.name) as "Character Name", player as Player, class as Class, ancestry as Ancestry, level as Level
from "People/PC"
where (role = "player")
where (status = "active")
```

## Latest Story Entries
```dataview
TABLE WITHOUT ID link(file.path, file.folder + "/" + file.name) as "Note",
file.mtime AS "Last Modified"
FROM "Story"
WHERE file.mtime >= date(today) - dur(30 days)
AND file.name != this.file.name
SORT file.mtime DESC
LIMIT 5
```