```dataviewjs
const pages = dv.pages().sort(p => p.file.name);
dv.table(["#", "Notes"], pages.map((p, i) => [i + 1, p.file.link]));
```
