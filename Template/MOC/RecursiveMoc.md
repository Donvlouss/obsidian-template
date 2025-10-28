---
modified: 2025-10-15T10:12:19+08:00
---
```dataview
TABLE
file.folder AS "Path",
title AS "Title",
file.ctime AS "Created",
file.mtime AS "Modified",
file.etags AS "Tags",
file.link AS "Link"
FROM "Folder"
```