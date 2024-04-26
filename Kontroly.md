## Lístečky bez tagů
```dataview
TABLE file.tags, file.path
WHERE length(file.tags) = 0 and startswith(file.path, "Lístečky")
```

```dataview
TABLE file.ctime as "Created"
FROM "Lístečky ✍🏻"
SORT file.ctime
DESC
```