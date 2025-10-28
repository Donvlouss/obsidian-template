---
title: Resource MOC
created: 2025-10-15 10:13
modified: 2025-10-17T10:35:14+08:00
tags:
  - "#🗺️MOC"
---

# Metadata


```dataview
TABLE WITHOUT ID 
	file.link AS MOC,
	file.ctime AS "Created",
	file.mtime AS "Modified"
WHERE startswith(file.folder, this.file.folder + "/")
AND file.name = split(regexreplace(file.folder, "^" + this.file.folder + "/", ""), "/")[0]
SORT file.name ASC
```