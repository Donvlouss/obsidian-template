---
created: 2025-10-14 17:15
modified: 2025-10-14T17:16:09+08:00
tags:
  - "#🗺️MOC"
---
```dataview
TABLE WITHOUT ID 
	file.link AS MOC,
	file.ctime AS "Created",
	file.mtime AS "Modified"
WHERE startswith(file.folder, this.file.folder + "/")
AND file.name = split(regexreplace(file.folder, "^" + this.file.folder + "/", ""), "/")[0]
SORT file.name ASC
```