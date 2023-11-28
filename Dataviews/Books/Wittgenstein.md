```dataviewjs
let pages = dv.pages("#Wittgenstein")
let pages2 = pages.sort(p => p.order)
// Loop through pages2
for (let p of pages2){
  dev.el("h3", p.file.tags)
  dv.el("h2",p.file.name); // note title
  dv.paragraph(dv.fileLink(p.file.name,false)) // link to note
  dv.el("article", await dv.io.load(p.file.path)); // note body
}
```
