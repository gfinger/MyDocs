# Handbuch_v19 zur Forschungstabelle Lorsch

**Datenbasis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-5.md`  
**Stand:** 2026-07-08  
**Status:** letzter inhaltlich normierter Stand im bisherigen 13-Spalten-Schema, vor geplanter Schema-Migration zu v7.

## Zweck

Dieses Handbuch beschreibt die derzeit verwendete Klassifikationslogik der Forschungstabelle. Es trennt bewusst:

| Feld | Funktion |
| --- | --- |
| `Buchgattung` | breite Großgattung oder formale Hauptgruppe |
| `Sub-Gattung` | nähere Form, Gebrauchsform oder fachliche Texttradition innerhalb der Großgattung |
| `Werktyp` | Überlieferungsstatus bzw. konkrete Funktion im Codex, z. B. `Originalwerk`, `Kompilation`, `Exzerpt`, `Fragment`, `Redaktion` |
| `Thema` | inhaltlicher Gegenstand bzw. Wissensbereich |
| `Überlieferungslinie` | literarisch-historischer oder schulischer Traditionszusammenhang |

## Aktuelle Leitentscheidungen

### 1. Biblische Primärtexte

Biblische Grundtexte werden als `Bibeltext` geführt. Konkrete Gebrauchsformen stehen in `Sub-Gattung`.

| Fall | Buchgattung | Sub-Gattung | Bemerkung |
| --- | --- | --- | --- |
| normaler biblischer Grundtext | `Bibeltext` | leer | Umfang steht in `Text` und `Werk`. |
| Evangelienbuch | `Bibeltext` | `Evangelienbuch` | fortlaufende Evangelienüberlieferung |
| Evangelistar | `Bibeltext` | `Evangelistar` | liturgisch geordnete Evangelienperikopen |
| Perikopenbuch | `Bibeltext` | `Perikopenbuch` | liturgisch geordnete biblische Lesungen, sofern nicht genauer bestimmbar |
| Bibel mit Glosse | `Bibeltext` | `Bibel mit Glosse` | biblischer Grundtext mit Glossen |

### 2. Bibelexegese

`Bibelexegese` ist der bevorzugte Oberbegriff für allgemeine biblische Auslegung. Reine Glossen- und Kommentarbestände können weiterhin als eigene Buchgattungen `Bibelglossen` bzw. `Bibelkommentar` erscheinen, sofern sie in der Tabelle bereits entsprechend klar benannt sind. Bibelbezogene Quaestiones werden als `Bibelexegese` mit `Sub-Gattung = Quaestiones` geführt.

| Fall | Buchgattung | Sub-Gattung |
| --- | --- | --- |
| allgemeine Auslegung | `Bibelexegese` | ggf. leer |
| bibelbezogene Quaestiones | `Bibelexegese` | `Quaestiones` |
| Bibelglossen | `Bibelglossen` | leer |
| Bibelkommentar | `Bibelkommentar` | leer |

### 3. Liturgische Gebrauchsbücher

`Liturgisches Buch` bleibt Großgattung für Bücher und Textformen, die unmittelbar dem liturgischen Vollzug dienen. Erklärende Texte über Liturgie stehen dagegen unter `Fachtext`.

| Fall | Buchgattung | Sub-Gattung |
| --- | --- | --- |
| Sakramentar / Sacramentarium | `Liturgisches Buch` | `Sakramentar` |
| Messbuch / Missale | `Liturgisches Buch` | `Messbuch` |
| Pontifikale / Pontificale | `Liturgisches Buch` | `Pontifikale` |
| Benedictionale | `Liturgisches Buch` | `Benedictionale` |
| Ordo / Ordo Romanus | `Liturgisches Buch` | `Ordo` |

### 4. Fachtexte, Artes liberales, Computus und Medizin

`Fachtext` ist die breite Großgattung für fachbezogene Sachtexte. Die Sub-Gattung benennt hier die fachliche Texttradition oder den engeren fachlichen Typ.

| Bereich | Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- | --- |
| Grammatik | `Fachtext` | `Grammatik` | `Grammatik` |
| Rhetorik | `Fachtext` | `Rhetorik` | `Rhetorik` |
| Grammatik / Rhetorik | `Fachtext` | `Grammatik / Rhetorik` | `Grammatik / Rhetorik` |
| Arithmetik | `Fachtext` | `Arithmetik` | `Arithmetik` |
| Computus | `Fachtext` | `Computus` | `Computus` |
| Medizin | `Fachtext` | `Medizin` | `Medizin` |
| Musiktheorie | `Fachtext` | `Musiktheorie` | meist `Musik` |
| Artes liberales allgemein | `Fachtext` | `Artes liberales` | `Artes liberales` |

### 5. Weitere vereinheitlichte Großgattungen

| Entscheidung | Normwert |
| --- | --- |
| `Brief` und `Briefsammlung` | `Briefe` |
| `Bücherverzeichnis` | `Katalog` |
| `Sequenz` / `Sequenzen` | `Dichtung`, Sub-Gattung `Sequenz` |
| `Predigt` / `Predigten` | `Homilien` |
| `Homiliensammlung` | `Homilien` |
| `Genealogie` | `Geschichtswerk`, Sub-Gattung `Genealogie` |
| hagiographische Dialoge | `Hagiographie`, Sub-Gattung `Dialog` |

## Materialisierung v6-5

Die in den ChangeLogs v9–v16 vorgemerkten Normierungen wurden in `v6-5` materialisiert.

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 405 |
| Spalten | 13 |
| geänderte Zeilen gegenüber v6-4 | 87 |
| geänderte Zellen gegenüber v6-4 | 122 |
| Buchgattungen vorher | 94 |
| Buchgattungen nach v6-5 | 79 |
| Sub-Gattungen nach v6-5 | 30 |

### Aggregierte Änderungen in v6-5

| Feld | vorher | nachher | Anzahl |
| --- | --- | --- | ---: |
| `Buchgattung` | `Briefsammlung` | `Briefe` | 13 |
| `Sub-Gattung` | `Handbuch` | `Medizin` | 11 |
| `Buchgattung` | `Grammatik` | `Fachtext` | 11 |
| `Sub-Gattung` | `` | `Grammatik` | 11 |
| `Buchgattung` | `Brief` | `Briefe` | 7 |
| `Buchgattung` | `Enzyklopädie` | `Fachtext` | 6 |
| `Sub-Gattung` | `` | `Artes liberales` | 5 |
| `Buchgattung` | `Bücherverzeichnis` | `Katalog` | 4 |
| `Sub-Gattung` | `` | `Dialog` | 4 |
| `Sub-Gattung` | `` | `Quaestiones` | 4 |
| `Sub-Gattung` | `Lehrschrift` | `Computus` | 3 |
| `Buchgattung` | `Predigten` | `Homilien` | 3 |
| `Sub-Gattung` | `` | `Computus` | 3 |
| `Sub-Gattung` | `` | `Medizin` | 2 |
| `Sub-Gattung` | `` | `Sequenz` | 2 |
| `Sub-Gattung` | `Lehrschrift` | `Arithmetik` | 2 |
| `Buchgattung` | `Dialog / Hagiographie` | `Hagiographie` | 2 |
| `Sub-Gattung` | `Lehrschrift` | `Dialektik` | 2 |
| `Buchgattung` | `Musiktheoretischer / liturgischer Text` | `Fachtext` | 2 |
| `Sub-Gattung` | `` | `Musiktheorie` | 2 |
| `Buchgattung` | `Dialog` | `Hagiographie` | 2 |
| `Buchgattung` | `Bibelkommentar` | `Bibelexegese` | 2 |
| `Buchgattung` | `Kalender` | `Fachtext` | 2 |
| `Sub-Gattung` | `Glossar` | `Medizin` | 1 |
| `Buchgattung` | `Sequenz` | `Dichtung` | 1 |
| `Buchgattung` | `Genealogie` | `Geschichtswerk` | 1 |
| `Sub-Gattung` | `` | `Genealogie` | 1 |
| `Buchgattung` | `Bibelbezogene Quaestionen` | `Bibelexegese` | 1 |
| `Buchgattung` | `Enzyklopädie / Lehrgedicht` | `Fachtext` | 1 |
| `Buchgattung` | `Predigt` | `Homilien` | 1 |
| `Buchgattung` | `Grammatik / Rhetorik` | `Fachtext` | 1 |
| `Sub-Gattung` | `` | `Grammatik / Rhetorik` | 1 |
| `Sub-Gattung` | `Lehrschrift` | `Dialektik / Rhetorik` | 1 |
| `Buchgattung` | `Rhetorik` | `Fachtext` | 1 |
| `Sub-Gattung` | `` | `Rhetorik` | 1 |
| `Buchgattung` | `Computistische Sammlung` | `Fachtext` | 1 |
| `Sub-Gattung` | `Ars` | `Rhetorik` | 1 |
| `Sub-Gattung` | `Glossar` | `Grammatik` | 1 |
| `Buchgattung` | `Sequenzen` | `Dichtung` | 1 |
| `Sub-Gattung` | `Glossar` | `Artes liberales` | 1 |

## Aktueller Wertebestand v6-5

### Buchgattungen

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

### Sub-Gattungen

| Wert | Anzahl |
| --- | ---: |
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

### Werktypen

| Wert | Anzahl |
| --- | ---: |
| `Originalwerk` | 227 |
| `Redaktion` | 40 |
| `Kompilation` | 33 |
| `Volltext` | 26 |
| `Übersetzung` | 18 |
| `Exzerpt` | 9 |
| `Anthologie` | 7 |
| `Nachtrag` | 5 |
| `Fragment` | 5 |
| `Glossierung / Kompilation` | 4 |
| `Glossierung` | 3 |
| `Kompilation / Glossierung` | 3 |
| `Bearbeitung` | 2 |
| `Nachtrag / Fragment` | 2 |
| `unsicher` | 2 |
| `Kompilation / Nachtrag` | 2 |
| `Beitext` | 2 |
| `Adaption` | 1 |
| `Fragment / Ergänzung` | 1 |
| `Redaktion / Kompilation` | 1 |
| `Einschub / Originalwerk` | 1 |
| `Fragment / Nachtrag` | 1 |
| `Sammlung` | 1 |
| `Traktat / Nachtrag` | 1 |
| `Glossierung / Nachtrag` | 1 |
| `Exzerpt / Bearbeitung` | 1 |
| `Teilüberlieferung` | 1 |
| `Übersetzung / editio composita` | 1 |
| `Originalwerk / Kommentar` | 1 |
| `Teilüberlieferung / Glossierung` | 1 |
| `Beitext / Marginalglosse` | 1 |
| `Kommentar / Glossierung` | 1 |

### Themata

| Wert | Anzahl |
| --- | ---: |
| `Exegese` | 74 |
| `Liturgie` | 37 |
| `Geschichte` | 32 |
| `Theologie` | 26 |
| `Bibel` | 22 |
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
| `Biblische Überlieferung` | 5 |
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

### Überlieferungslinien

| Wert | Anzahl |
| --- | ---: |
| `Lateinische Patristik` | 114 |
| `Karolingische Gelehrsamkeit` | 65 |
| `Spätantike Gelehrsamkeit` | 49 |
| `Klassische lateinische Literatur` | 32 |
| `Liturgische Tradition` | 28 |
| `Biblische Überlieferung` | 25 |
| `Angelsächsische Gelehrsamkeit` | 18 |
| `Griechische Patristik` | 14 |
| `Frühmittelalterliche Medizin` | 10 |
| `Frühmittelalterliche Gelehrsamkeit` | 9 |
| `Hochmittelalter` | 8 |
| `Kirchenrechtliche Tradition` | 7 |
| `Bibel` | 5 |
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

## Offene Redaktionsblöcke vor v7

- Spaltenschema: Reihenfolge, Umbenennungen und mögliche Löschungen werden erst nach diesem inhaltlich normierten Stand entschieden.
- `Bibelkommentar`, `Bibelglossen` und `Bibelexegese` sind noch nicht abschließend auf ein einziges Modell reduziert.
- `Kommentar` als allgemeine Buchgattung ist noch zu prüfen: ggf. je nach Gegenstand zu `Bibelexegese`, `Fachtext`, `Vergilkommentar` usw.
- `Enzyklopädie`, `Sammelhandschrift`, `Sammlung`, `Kirchenrecht`, `Kanonistische Sammlung`, `Rechtstext`, `Chronik`, `Annalen`, `Biographie`, `Vita` und hagiographische Spezialformen bleiben für spätere Redaktionsblöcke.
- Grenzfälle wie `Chronographie / Computus?`, `Kalender`, `Musiktheoretischer / liturgischer Text` wurden nur dort materialisiert, wo die bisherige Entscheidung eindeutig genug war.
