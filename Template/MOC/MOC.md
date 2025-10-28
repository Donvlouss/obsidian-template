---
title: XXX MOC
created: {{date}} {{time}}
modified: 2025-10-14T15:55:28+08:00
tags:
  - "#🗺️MOC"
---

# Metadata
Parent :: [[]]


```dataview
TABLE WITHOUT ID 
	file.link AS MOC,
	file.ctime AS "Created",
	file.mtime AS "Modified"
WHERE startswith(file.folder, this.file.folder + "/")
AND file.name = split(regexreplace(file.folder, "^" + this.file.folder + "/", ""), "/")[0]
SORT file.name ASC
```