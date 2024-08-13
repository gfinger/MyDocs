```dataviewjs
// sort documents
let pages1 = dv.pages()
let pages2 = pages1.where(p => (p.year != null || p.years != null))
let pages3 = pages2.sort(p => {
    if(p.year != null) return p.year
    else if(p.years != null) {
      let years = p.years
      let from = years["from"]
      return from
    }
  })

// render timeline
for (let p of pages3){
  if(p.year != null) {
    dv.header(3, p.year)
  } else if(p.years != null) {
    dv.header(3, (p.years)["from"] + "-" + p.years["to"])
  }
  let text1 = (await dv.io.load(p.file.path))
  dv.paragraph("<small>" + dv.fileLink(p.file.name,false) + "<small>");
  let text2 = text1.split("---")[2].split("\n")[1]
  dv.span(text2); // note body
  dv.paragraph("<small>" + p.file.tags + "</small>")
}
```