---
modified: 2025-10-15T10:30:21+08:00
---
```dataview
TABLE WITHOUT ID
	file.link AS File,
	title AS Title,
	file.ctime AS Created,
	file.mtime AS Modified
WHERE file.folder = this.file.folder
AND lower(replace(file.name, " ", "")) != lower(
  replace(split(this.file.folder, "/")[length(split(this.file.folder, "/")) - 1], " ", "")
)
SORT file.name ASC
```