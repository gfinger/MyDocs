# Handbuch_v23 zur Forschungstabelle Lorsch

**Datenbasis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Stand:** 2026-07-08  
**Status:** Normierung v7-3 nach v7-2; `Bibel` und `Kirchenrechtliche Tradition` in der Spalte `Überlieferungslinie` zu `Christlicher Kanon` vereinheitlicht; `Thema = Biblische Überlieferung` zu `Bibel` bereinigt.

## Aktuelles Spaltenschema v7-3

| Spalte | Funktion |
| --- | --- |
| `TXT-ID` | Primärschlüssel der Textebene. |
| `LHS-ID` | Fremdschlüssel zur Bischoff-/Handschriftenebene. |
| `Siegel` | BL-/Dateisigel bzw. Arbeitskennung des ausgewerteten Codex. |
| `Seiten` | Blatt-/Seitenangaben aus dem BL-Eintrag, soweit bereits aus den Bemerkungen extrahiert. Dazu gehören auch Lagen-/Spiegelangaben wie `Vorderspiegel` oder `Hinterspiegel`, wenn der Text dort lokalisiert ist. |
| `Autor` | Autor, zugeschriebener Autor oder `Anonymus`; leer, wenn nicht sinnvoll bestimmbar. |
| `Titel` | Werktitel. In der Schema-Migration aus der früheren Spalte `Werk` übernommen; künftig möglichst nach BL-Titelansatz zu befüllen. |
| `Buchgattung` | breite Großgattung oder formale Hauptgruppe. |
| `Untergattung` | nähere Form, Gebrauchsform oder fachliche Texttradition innerhalb der Großgattung. Entspricht der früheren Spalte `Sub-Gattung`. |
| `Thema` | inhaltlicher Gegenstand bzw. Wissensbereich. |
| `Überlieferungslinie` | literarisch-historischer oder schulischer Traditionszusammenhang. |
| `Bemerkungen` | Freitext für Besonderheiten, Unsicherheiten, relevante frühere Werktyp-Informationen, BL-Hinweise und redaktionelle Notizen. Blatt-/Seitenangaben sollen nicht mehr hier, sondern in `Seiten` stehen. |
| `Lorsch-Bezug` | einfacher Marker `ja`; ans Tabellenende verschoben und perspektivisch entbehrlich, wenn nur noch Lorscher Einträge geführt werden. |

## Schemaänderungen gegenüber v7

| Änderung | Umsetzung |
| --- | --- |
| Neue Spalte `Seiten` | direkt nach `Siegel` eingefügt |
| Blatt-/Seitenangaben in `Bemerkungen` | soweit maschinell eindeutig erkennbar nach `Seiten` verschoben |
| Standardformel `Text [Nr.] nach Bibliotheca Laureshamensis` | aus `Bemerkungen` entfernt |
| Standardformel `Nachtrag [Nr.] nach Bibliotheca Laureshamensis` | bereinigt; `Nachtrag` / `Nachtrag [Nr.]` bleibt erhalten, wenn sachlich sinnvoll |
| `Bemerkungen` | von Seitenangaben und Standardformeln entlastet |


## Normierungsänderung gegenüber v7-2

| Änderung | Umsetzung |
| --- | --- |
| `Überlieferungslinie = Bibel` | zu `Christlicher Kanon` vereinheitlicht |
| `Überlieferungslinie = Kirchenrechtliche Tradition` | zu `Christlicher Kanon` vereinheitlicht |
| `Thema = Biblische Überlieferung` | zu `Bibel` vereinheitlicht |

**Regel:** `Christlicher Kanon` bezeichnet in der Spalte `Überlieferungslinie` die normative christliche Kanontradition. Dazu gehören biblische Grundtexte ebenso wie kanonisch-normative Texte, insbesondere Konzilsbeschlüsse, Kanones und kirchenrechtliche Sammlungen. Das Feld `Thema` benennt dagegen den konkreten Gegenstand, z. B. `Bibel` oder `Kirchenrecht`.

## Leitentscheidungen zur Klassifikation

### Biblische Primärtexte

Biblische Grundtexte werden als `Bibeltext` geführt. Konkrete Gebrauchsformen stehen in `Untergattung`, etwa `Evangelienbuch`, `Evangelistar`, `Perikopenbuch` oder `Bibel mit Glosse`. In der Spalte `Überlieferungslinie` gilt hierfür der Normwert `Christlicher Kanon`; im Feld `Thema` kann `Bibel` stehen.

### Bibelexegese

`Bibelexegese` ist der bevorzugte Oberbegriff für allgemeine biblische Auslegung. Bibelbezogene Quaestiones werden als `Bibelexegese` mit `Untergattung = Quaestiones` geführt. `Bibeltext` bleibt biblischem Grundtext vorbehalten.

### Liturgische Gebrauchsbücher

`Liturgisches Buch` bleibt Großgattung für Bücher und Textformen, die unmittelbar dem liturgischen Vollzug dienen. Untergattungen sind z. B. `Sakramentar`, `Messbuch`, `Pontifikale`, `Benedictionale` und `Ordo`. Erklärende Texte über Liturgie stehen dagegen unter `Fachtext`, z. B. mit `Untergattung = Liturgik` oder `Messerklärung`.

### Fachtexte, Artes liberales, Computus und Medizin

`Fachtext` ist die breite Großgattung für fachbezogene Sachtexte. Die `Untergattung` benennt die fachliche Texttradition oder den engeren Typ, z. B. `Grammatik`, `Rhetorik`, `Arithmetik`, `Computus`, `Medizin`, `Musiktheorie`, `Glossar`, `Lehrschrift`, `Traktat`, `Handbuch` oder `Rezeptsammlung`.

### Weitere beschlossene Vereinheitlichungen

| Entscheidung | Normierung |
| --- | --- |
| Bücherverzeichnis | `Katalog` |
| Brief / Briefsammlung | `Briefe` |
| Sequenz / Sequenzen | `Buchgattung = Dichtung`, `Untergattung = Sequenz` |
| Dialog / Hagiographie | `Buchgattung = Hagiographie`, `Untergattung = Dialog` |
| Genealogie | `Buchgattung = Geschichtswerk`, `Untergattung = Genealogie` |
| Predigt / Predigten / Homiliensammlung | `Homilien` |

## Aktuelle Kennzahlen v7-3

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 405 |
| Spalten | 12 |
| befüllte `Seiten`-Zellen | 66 |
| Buchgattungen | 79 |
| Untergattungen inkl. leer | 31 |
| verbleibende Standardformeln `Text ... nach Bibliotheca Laureshamensis` | 0 |
| verbleibende `Thema = Biblische Überlieferung` | 0 |
| verbleibende `Überlieferungslinie = Bibel` | 0 |
| verbleibende `Überlieferungslinie = Kirchenrechtliche Tradition` | 0 |
| `Überlieferungslinie = Christlicher Kanon` | 37 |

## Aktuelle Wertelisten v7-3


### Buchgattung

| Wert | Anzahl |
| --- | ---: |
| `Fachtext` | 98 |
| `Bibeltext` | 34 |
| `Bibelkommentar` | 31 |
| `Homilien` | 21 |
| `Briefe` | 20 |
| `Geschichtswerk` | 20 |
| `Liturgisches Buch` | 19 |
| `Kommentar` | 18 |
| `Dichtung` | 15 |
| `Hagiographie` | 9 |
| `Bibelexegese` | 8 |
| `Sammelhandschrift` | 7 |
| `Kirchenrecht` | 6 |
| `Chronik` | 6 |
| `Mönchsliteratur` | 5 |
| `Katalog` | 4 |
| `Bibelglossen` | 4 |
| `Kanonistische Sammlung` | 3 |
| `Glossen` | 3 |
| `Martyrologium` | 3 |
| `Kirchengeschichte` | 3 |
| `Epos` | 2 |
| `Sammlung` | 2 |
| `Rechtstext` | 2 |
| `Psalmenkommentar` | 2 |
| `Vita` | 2 |
| `Biographie` | 2 |
| `Hagiographische Sammlung` | 2 |
| `Annalen` | 2 |
| `Philosophischer Dialog` | 2 |
| `Kanonessammlung` | 2 |
| `Liturgischer Text` | 1 |
| `Hagiographie / Vita` | 1 |
| `Geographie / Naturkunde` | 1 |
| `Kommentar / Exzerpt?` | 1 |
| `Florilegium` | 1 |
| `Urkundenbuch` | 1 |
| `Autobiographie` | 1 |
| `Klagevers` | 1 |
| `Enzyklopädie` | 1 |
| `Konzilsakten` | 1 |
| `Kanonistische Sentenzen` | 1 |
| `Chronographie / Computus?` | 1 |
| `Bibliothekskatalog` | 1 |
| `Urkunde / Testament` | 1 |
| `Liste` | 1 |
| `Traktat / Dialog` | 1 |
| `Literaturgeschichtlicher Katalog` | 1 |
| `Florilegium / Exzerptwerk` | 1 |
| `Einleitung` | 1 |
| `Anthologie` | 1 |
| `Bußbuch` | 1 |
| `Regel` | 1 |
| `Inschriftensammlung` | 1 |
| `Naturkundliche Schrift` | 1 |
| `Dialog / Enzyklopädisches Werk` | 1 |
| `Chronographisch-enzyklopädische Schrift` | 1 |
| `Biographiensammlung` | 1 |
| `Kosmographie` | 1 |
| `Liturgische Notiz` | 1 |
| `Philosophischer Text` | 1 |
| `Lehrgedicht` | 1 |
| `Enzyklopädie / Lehrgedicht` | 1 |
| `Enzyklopädie / Naturkunde` | 1 |
| `Mythographische Schrift` | 1 |
| `Vergilkommentar / Allegorese` | 1 |
| `Vita / Autorenbiographie` | 1 |
| `Philosophischer Dialog / Prosimetrum` | 1 |
| `Kommentar / Glossenapparat` | 1 |
| `Dichtung / Schreiberverse` | 1 |
| `Dichtung / Spottgedicht` | 1 |
| `Drama` | 1 |
| `Satire` | 1 |
| `Biblisches Epos` | 1 |
| `Rätseldichtung` | 1 |
| `Lexikon / Auslegungshilfe` | 1 |
| `Mirakelbuch` | 1 |
| `Papstchronik` | 1 |
| `Nekrolog` | 1 |

### Untergattung

| Wert | Anzahl |
| --- | ---: |
| `(leer)` | 255 |
| `Traktat` | 41 |
| `Evangelienbuch` | 14 |
| `Medizin` | 14 |
| `Grammatik` | 12 |
| `Sakramentar` | 11 |
| `Computus` | 6 |
| `Artes liberales` | 6 |
| `Evangelistar` | 5 |
| `Dialog` | 4 |
| `Quaestiones` | 4 |
| `Lehrschrift` | 3 |
| `Pontifikale` | 3 |
| `Liturgik` | 2 |
| `Sequenz` | 2 |
| `Arithmetik` | 2 |
| `Bibel mit Glosse` | 2 |
| `Epitome` | 2 |
| `Dialektik` | 2 |
| `Musiktheorie` | 2 |
| `Rhetorik` | 2 |
| `Messbuch` | 2 |
| `Genealogie` | 1 |
| `Messerklärung` | 1 |
| `Grammatik / Rhetorik` | 1 |
| `Lehrnotiz` | 1 |
| `Glossar` | 1 |
| `Dialektik / Rhetorik` | 1 |
| `Benedictionale` | 1 |
| `Ordo` | 1 |
| `Lehrschema` | 1 |

### Thema

| Wert | Anzahl |
| --- | ---: |
| `Exegese` | 74 |
| `Liturgie` | 37 |
| `Geschichte` | 32 |
| `Bibel` | 27 |
| `Theologie` | 26 |
| `Literatur` | 18 |
| `Medizin` | 17 |
| `Hagiographie` | 15 |
| `Kirchenrecht` | 14 |
| `Briefliteratur` | 13 |
| `Homiletik` | 13 |
| `Grammatik` | 12 |
| `Mönchtum` | 8 |
| `Philosophie` | 8 |
| `Dogmatik` | 7 |
| `Chronographie` | 7 |
| `Bibliothekswesen` | 6 |
| `Computus` | 6 |
| `Artes liberales` | 5 |
| `Naturkunde` | 5 |
| `Dichtung` | 4 |
| `verschieden` | 4 |
| `Asketik` | 4 |
| `Arithmetik` | 2 |
| `Exzerptliteratur` | 2 |
| `Dialektik` | 2 |
| `Klostergeschichte` | 2 |
| `Metrik` | 2 |
| `Lexikographie` | 2 |
| `Musik` | 2 |
| `Recht` | 2 |
| `Rhetorik` | 2 |
| `Philosophie / Logik` | 2 |
| `Astronomie` | 2 |
| `Liturgie / Dichtung` | 1 |
| `Autobiographie` | 1 |
| `Liturgie / Kirchenjahr` | 1 |
| `Eschatologie` | 1 |
| `Dichtung / Moral` | 1 |
| `Askese / Jungfräulichkeit` | 1 |
| `Grammatik / Rhetorik` | 1 |
| `Anthropologie / Morallehre` | 1 |
| `Dialektik / Rhetorik` | 1 |
| `Kanonistik` | 1 |
| `Urkundenwesen` | 1 |
| `Kosmologie` | 1 |
| `Wissenschaftstheorie` | 1 |
| `Artes liberales / Astronomie` | 1 |
| `Philosophie / Astronomie` | 1 |
| `Liturgie / Eucharistie` | 1 |
| `Biographie` | 1 |
| `Philosophie / Exegese eines Schultextes` | 1 |
| `Dichtung / Buchkultur` | 1 |
| `Enzyklopädie / Artes liberales` | 1 |
| `Exegese / Liturgie` | 1 |

### Überlieferungslinie

| Wert | Anzahl |
| --- | ---: |
| `Lateinische Patristik` | 114 |
| `Karolingische Gelehrsamkeit` | 65 |
| `Spätantike Gelehrsamkeit` | 49 |
| `Christlicher Kanon` | 37 |
| `Klassische lateinische Literatur` | 32 |
| `Liturgische Tradition` | 28 |
| `Angelsächsische Gelehrsamkeit` | 18 |
| `Griechische Patristik` | 14 |
| `Frühmittelalterliche Medizin` | 10 |
| `Frühmittelalterliche Gelehrsamkeit` | 9 |
| `Hochmittelalter` | 8 |
| `Spätantike Medizin` | 2 |
| `Oribasianische Tradition` | 2 |
| `Hellenistisch-jüdische Tradition` | 2 |
| `Biblische Glossentradition` | 2 |
| `Antike Naturphilosophie` | 1 |
| `Ottonische Gelehrsamkeit` | 1 |
| `St. Galler Sequenztradition` | 1 |
| `Sprachlogische Tradition` | 1 |
| `Lorscher Überlieferung` | 1 |
| `Antike Philosophie` | 1 |
| `Humanismus` | 1 |
| `Frühmittelalterliche Theologie` | 1 |
| `Boethius-Überlieferung` | 1 |
| `Mittelalterliche Schreibkultur` | 1 |
| `Mittelalterliche Gelegenheitsdichtung` | 1 |
| `Angelsächsisch-karolingische Glossentradition` | 1 |
| `Biblische Glossentradition; Karolingische Gelehrsamkeit` | 1 |
