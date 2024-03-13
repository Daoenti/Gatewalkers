# Dashboard
## Party
```dataview
table without ID link(file.name) as "Character Name", player as Player, class as Class, ancestry as Ancestry, level as Level
from "People/PC"
where (role = "player")
where (status = "active")
```