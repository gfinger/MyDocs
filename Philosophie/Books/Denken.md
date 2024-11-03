```dataviewjs
let pages1 = dv.pages()
let pages2 = pages1.where(p => p.document == "Denken")
let pages3 = pages2.sort(p => p.order)
// Loop through pages3
for (let p of pages3){
  dv.el("h2",dv.fileLink(p.file.name,false)); // note title
  dv.el("div", "<small>" + p.file.tags + "</small>")
  dv.el("div", "<small>" + p.abstract + "</small>")
  // dv.paragraph(dv.fileLink(p.file.name,false)) // link to note
  dv.el("article", await dv.io.load(p.file.path)); // note body
}
```
