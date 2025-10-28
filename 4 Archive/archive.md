---
title: Archive MOC
created: 2025-10-17 11:29
modified: 2025-10-17T16:28:58+08:00
tags:
  - "#🗺️MOC"
---

# Metadata

```dataview
TABLE WITHOUT ID
	Status,
	file.link AS MOC,
	description AS "Description",
	Language AS "Language",
	repo AS "Repository",
	file.ctime AS "Created",
	file.mtime AS "Modified"
WHERE startswith(file.folder, this.file.folder + "/")
AND file.name = split(regexreplace(file.folder, "^" + this.file.folder + "/", ""), "/")[0]
SORT file.name ASC, language ASC
```