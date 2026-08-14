# Handbuch_v24 zur Forschungstabelle Lorsch

**Datenbasis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Stand:** 2026-07-08  
**Status:** Normierung v7-3; zusätzliche, noch nicht materialisierte Entscheidungen: `Oribasianische Tradition` soll künftig zu `Spätantike Medizin` vereinheitlicht werden; `TXT0015-01` wird bei Thema/Überlieferungslinie nachnormiert.


## Vorgemerkte Normierungsentscheidung nach v7-3

| Feld | bisheriger Wert | künftiger Normwert | Status |
| --- | --- | --- | --- |
| `Überlieferungslinie` | `Oribasianische Tradition` | `Spätantike Medizin` | vorgemerkt, noch nicht in der Forschungstabelle materialisiert |
| `Thema` | `Liturgie / Dichtung` | `Dichtung` | vorgemerkt, noch nicht in der Forschungstabelle materialisiert; betrifft `TXT0015-01` |
| `Überlieferungslinie` | `St. Galler Sequenztradition` | `Karolingische Gelehrsamkeit` | vorgemerkt, noch nicht in der Forschungstabelle materialisiert; betrifft `TXT0015-01` |

### Begründung

`Oribasianische Tradition` ist als Datenbankwert zu speziell und für die Auswertung wenig transparent. Der Normwert `Spätantike Medizin` benennt den medizinischen Traditionszusammenhang breiter und verständlicher. Falls ein konkreter Textbezug zu Oribasius sachlich relevant ist, kann dieser in `Titel` oder `Bemerkungen` vermerkt werden.

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


### Sequenzen und überfeine Überlieferungslinien

Sequenzen werden als `Buchgattung = Dichtung`, `Untergattung = Sequenz` geführt. Für das Feld `Thema` genügt bei Sequenzen in der Regel `Dichtung`; der liturgische Gebrauch ist durch die Untergattung und ggf. Bemerkungen erkennbar. Zu enge, nur an einem einzelnen Werk sichtbare Überlieferungslinien werden vermieden. `St. Galler Sequenztradition` wird daher für `TXT0015-01` zu `Karolingische Gelehrsamkeit` vereinheitlicht. Spezifische Schul-, Kloster- oder Lokaltraditionen sollen nur als `Überlieferungslinie` verwendet werden, wenn sie für mehrere Einträge analytisch tragfähig sind.

### Fachtexte, Artes liberales, Computus und Medizin

`Fachtext` ist die breite Großgattung für fachbezogene Sachtexte. Für Texte aus dem Bereich der `Artes liberales` gilt ab v7-32 eine eigene Normierung: `Buchgattung = Fachtext`, `Untergattung = Artes liberales`, `Thema =` jeweilige Ars bzw. bei Mehrfachbezug `Trivium`, `Quadrivium` oder `Sieben freie Künste`, `Überlieferungslinie = Spätantike Gelehrsamkeit`.

Die Einzelwerte `Grammatik`, `Rhetorik`, `Dialektik`, `Arithmetik`, `Metrik`, `Orthographie` und `Musiktheorie` werden daher nicht mehr als `Untergattung` für Artes-Texte verwendet. `Metrik`, `Orthographie`, Donat-Exzerpte und grammatische Glossen stehen thematisch unter `Grammatik`; Kommentar-, Glossen- und Exzerptformen werden bei Artes-Texten nicht über `Buchgattung = Kommentar`, sondern über Titel und Bemerkungen sichtbar gemacht. Echte Reden und Orationen sind davon ausgenommen: Sie werden als `Buchgattung = Rede`, `Thema = Rhetorik` geführt.

Für andere Fachbereiche bleiben engere Untergattungen wie `Computus`, `Medizin`, `Glossar`, `Traktat`, `Handbuch` oder `Rezeptsammlung` möglich.

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


## v26 – Vorgemerkte Normierung: Isidor und `Lateinische Patristik` (2026-07-08)

### Entscheidung

Isidor von Sevilla bzw. isidorische Texte werden in der Spalte `Überlieferungslinie` nicht unter `Lateinische Patristik` geführt. Der bevorzugte Normwert ist `Spätantike Gelehrsamkeit`.

### Begründung

`Lateinische Patristik` soll vor allem für die lateinische Vätertradition im engeren Sinn verwendet werden. Isidor steht zwar in der christlich-lateinischen Tradition, ist für diese Tabelle aber analytisch besser als spätantiker bzw. frühmittelalterlich rezipierter Wissenskompilator zu erfassen. Seine Werke — insbesondere `Etymologiae`, `Sententiae`, `De natura rerum`, `Chronicon`, `De ecclesiasticis officiis` usw. — werden daher der Linie `Spätantike Gelehrsamkeit` zugeordnet.

### Vorgemerkte Tabellenänderung

| Feld | bisheriger Wert | künftiger Wert | Anwendungsfall |
| --- | --- | --- | --- |
| `Überlieferungslinie` | `Lateinische Patristik` | `Spätantike Gelehrsamkeit` | Isidorische Texte, soweit noch nicht entsprechend normiert |

Im aktuellen Stand `v7-3` betrifft dies nach Prüfung insbesondere `TXT0008-02` (`Isidorus`, `Versus seu Carmina`). Die übrigen expliziten Isidor-Zeilen sind bereits als `Spätantike Gelehrsamkeit` geführt.

## v27 – Methodische Präzisierung: Überlieferungslinie nach Textfunktion, nicht mechanisch nach Autor (2026-07-08)

### Entscheidung

Die Spalte `Überlieferungslinie` wird grundsätzlich vom konkreten Text, seiner Funktion und seinem Überlieferungszusammenhang her bestimmt, nicht mechanisch vom Autorennamen.

### Regel

Ein Autor kann in verschiedenen Überlieferungslinien erscheinen, wenn unterschiedliche Texte desselben Autors bzw. derselben Zuschreibung in unterschiedlichen funktionalen Kontexten überliefert werden.

| Beispiel | maßgebliche Einordnung |
| --- | --- |
| Johannes Cassianus, `Collationes` | `Monastische Tradition` |
| Gregorius Magnus (trad.), `Sacramentarium Gregorianum` | `Liturgische Tradition` |
| Gregor der Große, `Moralia in Iob` | `Lateinische Patristik` bzw. exegetisch-patristische Tradition |
| Isidorische Wissenskompilationen | `Spätantike Gelehrsamkeit` |

### Begründung

Die Überlieferungslinie soll analytisch abbilden, in welchem Traditionszusammenhang der jeweilige Text in der Lorscher Bibliothek steht. Der Autor ist dafür ein wichtiger Hinweis, aber nicht allein ausschlaggebend. Entscheidend ist die Textfunktion: liturgisches Gebrauchsbuch, monastischer Lehr- und Übungstext, patristische Exegese, spätantike Wissenskompilation usw.

### Vorgemerkte Tabellenänderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0009` | `Überlieferungslinie` | `Lateinische Patristik` | `Monastische Tradition` | Cassians `Collationes I–X` sind für die Tabelle primär monastische Lehr- und Übungsliteratur. |
| `TXT0010` | `Überlieferungslinie` | `Lateinische Patristik` | `Monastische Tradition` | Cassians `Collationes XI–XVII` sind für die Tabelle primär monastische Lehr- und Übungsliteratur. |

Die liturgischen Einträge zum `Sacramentarium Gregorianum` bleiben dagegen trotz gregorianischer Zuschreibung bei `Liturgische Tradition`.



## v28 – Vorgemerkte Normierung: `Homiletik` als Thema vermeiden (2026-07-08)

### Entscheidung

`Homiletik` wird in der Spalte `Thema` nicht als Normwert für konkrete Homilienüberlieferung verwendet. Der Begriff bezeichnet eher die Lehre, Theorie oder Wissenschaft von der Predigt bzw. Homilie. Für konkrete Homilien oder Homilienbestände ist als Thema `Homilien` bzw. — wenn der Auslegungscharakter im Vordergrund steht — `Bibelexegese` zu verwenden.

### Anwendung

| Fall | Thema | Begründung |
| --- | --- | --- |
| konkrete Homilien / Homilienbestand | `Homilien` | Gegenstand ist die Textgattung selbst, nicht die Theorie der Predigt |
| Homilien als biblische Auslegung | `Bibelexegese` | wenn der exegetische Charakter stärker analytisch relevant ist |
| theoretischer Text über Predigt/Homilie | `Homiletik` | nur für ausdrücklich theoretische oder regelhafte Texte zur Predigtlehre |

### Vorgemerkte Tabellenänderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0018` | `Thema` | `Homiletik` | `Homilien` | LHS0017 trägt den Titel `Homiliae`; gemeint ist ein Homilienbestand, nicht Predigtlehre. |


## v29 – Vorgemerkte Normierung: Pseudo-Hegesippus nicht `Lateinische Patristik` (2026-07-08)

### Entscheidung

Pseudo-Hegesippus, `De excidio Hierosolymitano`, wird in der Spalte `Überlieferungslinie` nicht unter `Lateinische Patristik` geführt. Der bevorzugte Normwert ist `Spätantike Gelehrsamkeit`.

### Begründung

`Lateinische Patristik` bleibt für patristische Autoritäts- und Exegesetraditionen im engeren Sinn reserviert. `De excidio Hierosolymitano` ist in der Tabelle bereits als `Geschichtswerk` erfasst; analytisch ist der Text besser als spätantike lateinisch-christliche Geschichtsdarstellung bzw. Wissensüberlieferung zu behandeln. Die Josephus-/Hegesippus-Bezüge können bei Bedarf in `Bemerkungen` erscheinen, sollen aber keine eigene Überlieferungslinie erzwingen.

### Vorgemerkte Tabellenänderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0021` | `Überlieferungslinie` | `Lateinische Patristik` | `Spätantike Gelehrsamkeit` | Pseudo-Hegesippus ist hier als spätantikes Geschichtswerk relevant, nicht als Patristik im engeren Sinn. |


## v30 – Vorgemerkte Normierung: `Hellenistisch-jüdische Tradition` zu `Antik-jüdische Literatur` (2026-07-08)

### Entscheidung

Der bisherige Wert `Hellenistisch-jüdische Tradition` wird in der Spalte `Überlieferungslinie` künftig durch `Antik-jüdische Literatur` ersetzt.

### Definition

`Antik-jüdische Literatur` bezeichnet jüdische Autoren und Werke der hellenistischen und römischen Zeit, die in lateinischer bzw. christlicher Rezeption überliefert sind. Der Begriff umfasst insbesondere Philo von Alexandria und Flavius Josephus.

### Begründung

`Hellenistisch-jüdische Tradition` ist zwar für Philo grundsätzlich passend, aber für Josephus zu eng und insgesamt etwas sperrig. `Antik-jüdische Literatur` ist breiter, verständlicher und trägt beide bisher betroffenen Einträge. Die Linie bleibt zugleich spezifisch genug, um Philo und Josephus nicht unpassend unter `Spätantike Gelehrsamkeit` oder `Klassische lateinische Literatur` einzuordnen.

### Vorgemerkte Tabellenänderung

| Feld | bisheriger Wert | künftiger Wert | Anwendungsfall |
| --- | --- | --- | --- |
| `Überlieferungslinie` | `Hellenistisch-jüdische Tradition` | `Antik-jüdische Literatur` | Philo von Alexandria, Flavius Josephus und vergleichbare jüdische Autoren/Werke der hellenistischen und römischen Zeit |

Im aktuellen Stand `v7-3` betrifft dies nach Prüfung `TXT0028` und `TXT0250`.


## v31 – Vorgemerkte Normierung: Gregor von Tours nicht `Lateinische Patristik` (2026-07-08)

### Entscheidung

Gregor von Tours wird in der Spalte `Überlieferungslinie` nicht unter `Lateinische Patristik` geführt. Für die derzeit betroffenen Einträge ist der bevorzugte Normwert `Frühmittelalterliche Gelehrsamkeit`.

### Begründung

`Lateinische Patristik` bleibt für patristische Autoritäts-, Exegese- und Lehrtraditionen im engeren Sinn reserviert. Gregor von Tours gehört für diese Datenbank eher in den Bereich frühmittelalterlicher, insbesondere merowingisch-fränkischer Geschichts- und Hagiographieüberlieferung. Da wir Ein-Werk- oder Ein-Zeilen-Sondertraditionen vermeiden wollen, wird vorläufig kein eigener Normwert wie `Merowingische Historiographie` eingeführt. Die konkrete Textform bleibt über `Buchgattung` und `Thema` sichtbar.

### Anwendung

| TXT-ID | Titel | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- | --- |
| `TXT0034` | `Historia Francorum` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Frühmittelalterlich-fränkisches Geschichtswerk, nicht Patristik im engeren Sinn. |
| `TXT0310` | `Libri miraculorum` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Frühmittelalterliche hagiographische bzw. Mirakelüberlieferung; das Thema bleibt `Hagiographie`. |
| `TXT0342` | `Werk unbestimmt` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Zuschreibung an Gregor von Tours reicht nicht für Patristik; bei unbestimmtem Werk ist die breitere frühmittelalterliche Linie vorzuziehen. |

### Allgemeine Regel

Gregor von Tours wird nicht pauschal als `Lateinische Patristik` behandelt. Die konkrete Einordnung richtet sich nach dem Text: Geschichtswerke bleiben als `Geschichtswerk`/`Geschichte` erfasst, hagiographische Texte als `Hagiographie`; die Überlieferungslinie ist vorläufig `Frühmittelalterliche Gelehrsamkeit`, solange keine tragfähigere, mehrfach belegte Speziallinie eingeführt wird.

---

## v32 – Materialisierung der gesammelten Normierungsentscheidungen als Forschungstabelle v7-4 (2026-07-08)

Die seit `v7-3` gesammelten Normierungsentscheidungen wurden als Forschungstabelle `v7-4` materialisiert. Das Spaltenschema blieb unverändert.

Umgesetzt wurden insbesondere:

| Bereich | Umsetzung |
|---|---|
| Cassian, `Collationes` | Titelpräzisierung zu `Collationes I–X` bzw. `Collationes XI–XVII`; Überlieferungslinie zu `Monastische Tradition` |
| Medizinische Traditionslinie | `Oribasianische Tradition` zu `Spätantike Medizin` |
| Sequenz `TXT0015-01` | Thema zu `Dichtung`; Überlieferungslinie zu `Karolingische Gelehrsamkeit` |
| Isidor | `TXT0008-02` zu `Spätantike Gelehrsamkeit` |
| Homilien | `TXT0018`, Thema `Homiletik` zu `Homilien` |
| Pseudo-Hegesippus | `TXT0021` zu `Spätantike Gelehrsamkeit` |
| Philo/Josephus | `Hellenistisch-jüdische Tradition` zu `Antik-jüdische Literatur` |
| Gregor von Tours | betroffene Einträge zu `Frühmittelalterliche Gelehrsamkeit` |

Prüfung der Forschungstabelle `v7-4`:

| Kennzahl | Ergebnis |
|---|---:|
| Datenzeilen | 405 |
| Spalten | 12 |
| geänderte Zeilen gegenüber `v7-3` | 13 |
| geänderte Zellen gegenüber `v7-3` | 16 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |



## Aktualisierung v33: Homilien / Homiletik

`Homiletik` wird nicht als Thema für konkrete Homilienbestände verwendet. Bei Titeln wie `Homiliae` gilt als Thema `Homilien`; `Homiletik` bleibt höchstens für theoretische Texte über Predigt/Homilie reserviert.

Materialisiert in Forschungstabelle v7-6 für `TXT0039`.


## Nachtrag v34: Bibelglossen als bibelexegetische Glossenüberlieferung

Für Einträge des Typs `Glossae in Bibliam` gilt: Wenn der Textbestand eindeutig biblische Glossen umfasst, wird die Buchgattung als `Bibelglossen` geführt; die Überlieferungslinie kann `Biblische Glossentradition` lauten, sofern kein präziserer, wiederholt verwendbarer Traditionszusammenhang vorliegt. `Karolingische Gelehrsamkeit` soll hier nicht als Ersatz für die eigentliche Glossen- bzw. Auslegungstradition dienen.

## Nachtrag v35 – LHS0038 / St. Peter perg. 87

### Korrektur zur Überlieferungslinie bei `TXT0042`

Der Sonderwert `Biblische Glossentradition` wird für `LHS0038` nicht als Normwert fortgeführt. Er ist zu speziell und widerspricht der Reduktionsmaxime für die Spalte `Überlieferungslinie`.

Für die Lorscher Faszikel von St. Peter perg. 87 gilt vorläufig:

| Sachverhalt | Normierung |
|---|---|
| Datierung Mitte oder 3. Viertel 11. Jh. | nicht streng ottonisch, sondern eher frühsalisch; in der Tabelle breit als `Frühmittelalterliche Gelehrsamkeit` geführt |
| Bibelglossar | `Buchgattung = Bibelglossen`, `Thema = Exegese` |
| allgemeine Glossare | `Buchgattung = Fachtext`, `Untergattung = Glossar`, `Thema = Lexikographie` |
| Faszikel II, 14. Jh., Entstehungsort unbekannt | kein `Lorsch-Bezug`; Überlieferungslinie bleibt vorläufig leer |

Die oberste Gliederung des BL-Inhaltsverzeichnisses wird für `LHS0038` in fünf Einträge umgesetzt: `Glossarium biblicum`, `Glossarium de diversis`, `Glossarium de diversis auctoribus`, `Interpretationes nominum Hebraicorum secundum Hieronymum`, `Glossarium Latinum`.



---

## Nachtrag v36 – LHS0038: Ausschluss des nicht-Lorscher Faszikel II

Für `LHS0038` / Karlsruhe, BLB, St. Peter perg. 87 wird der zweite Faszikel (`Glossarium Latinum`, 3ra-57vb) nicht in der Forschungstabelle geführt. Er ist nach der BL-Beschreibung ein eigenständiger Faszikel des 14. Jh. mit unbekanntem Entstehungsort und ohne Lorsch-Bezug.

Damit gilt für diesen Codex:

| Bereich | Tabellenbehandlung |
|---|---|
| Faszikel I, Bll. [1]-2 und 62-106 | wird in vier Einträgen geführt, da Lorsch-Bezug besteht |
| Faszikel II, Bll. 3-61 | wird gelöscht / nicht geführt, da kein Lorsch-Bezug besteht |

Die frühere Zeile `TXT0042-05` (`Glossarium Latinum`) ist damit aufgehoben.

Der Sonderwert `Biblische Glossentradition` wird weiterhin nicht verwendet. Für die Lorscher Faszikel bleibt die breite Überlieferungslinie `Frühmittelalterliche Gelehrsamkeit`.

## Normierungsentscheidung v37: Keine Slash-Werte in Buchgattung und Untergattung

Für die Spalten `Buchgattung` und `Untergattung` werden keine Mischwerte mit Schrägstrich mehr verwendet. Wenn ein bisheriger Gattungswert zwei Aspekte verband, wird er auf die beiden Klassifikationsachsen verteilt:

- `Buchgattung` enthält die breitere formale Gattung.
- `Untergattung` enthält die nähere Textform, Gebrauchsfunktion oder fachliche Ausprägung.
- Unsichere oder sekundäre Aspekte, die nicht mehr sinnvoll in die zwei Felder passen, werden nur in begründeten Einzelfällen in `Bemerkungen` gesichert.

Beispiele:

| bisher | künftig |
|---|---|
| `Hagiographie / Vita` | `Buchgattung = Hagiographie`, `Untergattung = Vita` |
| `Dichtung / Schreiberverse` | `Buchgattung = Dichtung`, `Untergattung = Schreiberverse` |
| `Kommentar / Glossenapparat` | `Buchgattung = Kommentar`, `Untergattung = Glossenapparat` |
| `Vergilkommentar / Allegorese` | `Buchgattung = Kommentar`, `Untergattung = Allegorese` |
| `Enzyklopädie / Naturkunde` | `Buchgattung = Fachtext`, `Untergattung = Enzyklopädie` |
| `Geographie / Naturkunde` | `Buchgattung = Fachtext`, `Untergattung = Geographie` |

Die Regel betrifft zunächst nur `Buchgattung` und `Untergattung`. Schrägstriche in `Thema` können später gesondert bereinigt werden, weil dort gelegentlich bewusst zwei Gegenstandsbereiche angezeigt werden.



## Nachtrag v38 – Untergattungen `Vita` und `Schreiberverse`; Begriff `Allegorese`

### `Vita`

`Vita` wird vorläufig nicht als eigene Untergattung geführt. Bei hagiographischen Lebensbeschreibungen genügt in der Regel die Buchgattung `Hagiographie`; die konkrete Vita ist bereits im Titel erkennbar.

Normierung:

| bisher | künftig |
|---|---|
| `Buchgattung = Hagiographie`, `Untergattung = Vita` | `Buchgattung = Hagiographie`, `Untergattung` leer |

### `Schreiberverse`

`Schreiberverse` wird vorläufig nicht als eigene Untergattung geführt. Gemeint sind kurze metrische Schreibervermerke oder Verse im Umfeld des Schreibvorgangs bzw. Kolophons. Für die Forschungstabelle genügt `Buchgattung = Dichtung`; die genauere Information bleibt im Titel oder in den Bemerkungen.

Normierung:

| bisher | künftig |
|---|---|
| `Buchgattung = Dichtung`, `Untergattung = Schreiberverse` | `Buchgattung = Dichtung`, `Untergattung` leer |

### `Allegorese`

`Allegorese` bezeichnet eine allegorische Auslegung: Ein Text wird nicht nur wörtlich verstanden, sondern als Träger eines verborgenen moralischen, philosophischen, theologischen oder kosmologischen Sinns gelesen.

Für die Tabelle ist wichtig: `Allegorese` ist eher eine Interpretationsweise als eine stabile Buch- oder Untergattung. Ob der Wert als Untergattung erhalten bleibt, wird gesondert entschieden. Eine mögliche spätere Normierung wäre: `Buchgattung = Kommentar`, `Untergattung` leer oder `Untergattung = Kommentar`, mit Hinweis auf allegorische Deutung in den Bemerkungen.

## Nachtrag v39 – `Allegorese` und `Schreiberverse` nur in Bemerkungen

`Allegorese` und `Schreiberverse` werden nicht als Untergattungen geführt. Beide Werte sind für die Untergattung zu fein bzw. bezeichnen eher eine Interpretationsweise oder einen besonderen Beitexttyp.

Normierung:

| bisher | künftig |
|---|---|
| `Buchgattung = Kommentar`, `Untergattung = Allegorese` | `Buchgattung = Kommentar`, `Untergattung` leer; Hinweis `Allegorese` in `Bemerkungen` |
| `Buchgattung = Dichtung`, `Untergattung = Schreiberverse` | `Buchgattung = Dichtung`, `Untergattung` leer; Hinweis `Schreiberverse` in `Bemerkungen` |

Damit bleibt die Untergattungsspalte schlank. Spezifische Hinweise, die nur einzelne Einträge betreffen, werden in der Bemerkungsspalte gesichert.



## Nachtrag v40 – BL-Neuauswertung Pal. lat. 1588 / LHS0264

Der bisherige Platzhalter zu `LHS0264` wurde auf Grundlage des BL-Begleittexts zu Vatikan, BAV, Pal. lat. 1588 ersetzt. Die rhetorische Sammelhandschrift wird nicht mehr als Einzelwerk `Ars rhetorica` mit `etc.` geführt, sondern nach den obersten BL-Inhaltseinheiten aufgespalten.

Normierungsentscheidung für diese Handschrift:

| Bereich | Erfassung |
|---|---|
| Rhetorische Lehr- und Schultexte | `Buchgattung = Fachtext`, `Untergattung = Rhetorik` |
| Dialektischer Lehrtext | `Buchgattung = Fachtext`, `Untergattung = Dialektik` |
| Kommentar zu Ciceros Rhetorik | `Buchgattung = Kommentar`, Thema `Rhetorik` |
| Censorinus / Ps.-Censorinus | `Buchgattung = Fachtext`, `Untergattung = Enzyklopädie` |
| Cassiodor-Nachtrag | eigene Zeile, da BL ihn als Nachtrag 39v–41v ausweist |

Der Nachtrag wird trotz späterer Einfügung in der Handschrift geführt, da er im BL-Begleittext als eigener Bestandteil von Pal. lat. 1588 beschrieben ist und zur rhetorischen Sammelfunktion des Codex gehört.

## Nachtrag v41 – Pal. lat. 824 / LHS0231

Für `LHS0231` / `bav_pal_lat_824` wurde der bisherige Eintrag `TXT0252` auf Grundlage des BL-Begleittexts in zwei Zeilen aufgeteilt:

- `TXT0252-01`: Epiphanius scholasticus / Cassiodor, `Historia ecclesiastica tripartita e Socrate scholastico, Sozomeno et Theodoreto collecta et e Graeco in Latinum versa`, `1v-168v`, `Überlieferungslinie = Spätantike Gelehrsamkeit`.
- `TXT0252-02`: Bernardus Claraevallensis, `Epistula 238`, `168v`, Nachtrag, unvollständig, `Überlieferungslinie = Mittelalterliche Gelehrsamkeit`.

`Mittelalterliche Gelehrsamkeit` wird hier als breiter Normwert für einen mittelalterlichen theologischen bzw. kirchlichen Nachtrag verwendet; es wird keine Sonderlinie für Bernhard oder die Zisterzienser eingeführt.



## Nachtrag v42: Pal. lat. 273 / LHS0191

Der bisherige Einzeleintrag zu `Cassiodor, Variae` wird nach BL auf fünf oberste Inhaltseinheiten aufgesplittet. Für `Marbodus Redonensis, De ornamentis verborum` gilt `Buchgattung = Fachtext`, `Untergattung = Rhetorik`. Für `De Homeri centone et Eudoxia augusta` wird `Untergattung = Literaturkunde` verwendet. Für `Versus de terra et firmamento una cum tractatulo de ventis XII` wird `Untergattung = Kosmographie` verwendet. Für die mittelalterlichen Nachträge bzw. Zusatztexte wird `Überlieferungslinie = Mittelalterliche Gelehrsamkeit` verwendet.


## Nachtrag v43: Pal. lat. 814 / LHS0229

Der Eintrag zu `LHS0229 / TXT0250` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_814` präzisiert. Der Titel wird nach BL als `Antiquitates Iudaicae (libb. I-XII) curis Cassiodori e Graeco versae` geführt. Die Einordnung bleibt `Buchgattung = Geschichtswerk`, `Thema = Geschichte`, `Überlieferungslinie = Antik-jüdische Literatur`. Die spezifische lateinische Überlieferung durch Cassiodor wird im Titel und in den Bemerkungen sichtbar, ohne eine neue Sondertradition einzuführen.


## Nachtrag v44: Pal. lat. 24 / LHS0132 und Spalte `palimpsestiert`

Die Forschungstabelle erhält eine neue Spalte `palimpsestiert`. Sie steht unmittelbar vor `Lorsch-Bezug`, damit `Lorsch-Bezug` weiterhin die letzte Spalte der Tabelle bleibt.

Normierung:

| Wert | Bedeutung |
|---|---|
| `ja` | Der konkrete Texteintrag ist als ältere, radierte bzw. palimpsestierte Schrift überliefert. |
| leer | Der konkrete Texteintrag ist nicht selbst palimpsestiert oder der Befund ist nicht einschlägig. |

Für Pal. lat. 24 gilt daher: Die jüngere biblische Schrift wird nicht mit `ja` markiert, obwohl sie auf wiederverwendeten Palimpsestblättern steht. Mit `ja` markiert werden nur die älteren, radierten Untertexte.

Der bisherige Block `LHS0132` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_24` ersetzt. Erfasst werden fünf Einträge der jüngeren Schrift und zwölf Einträge der älteren, radierten Schrift. Die älteren Untertexte erhalten `palimpsestiert = ja`.

## Nachtrag v45: Pal. lat. 1519 / LHS0257

Der bisherige Block zu `LHS0257` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_1519` ersetzt. Die Handschrift wird nicht mehr nur mit `Cicero, De natura deorum` und `Walahfrid Strabo, Hortulus` geführt, sondern nach den drei obersten BL-Inhaltseinheiten erfasst:

- `TXT0281-01`: Cicero, `De natura deorum`, `1r-40v`, unvollständig.
- `TXT0281-02`: Cicero, `De divinatione`, `40ar-85v`, unvollständig.
- `TXT0281-03`: Walahfridus Strabo, `De cultura hortorum sive Hortulus`, `85va-88vb`, Ende fehlt.

Normierung: Für den `Hortulus` wird `Buchgattung = Dichtung`, `Untergattung = Lehrgedicht` verwendet. Die althochdeutschen Glossen auf 85va werden in den `Bemerkungen` gesichert, nicht als eigener Texteintrag. Die neue Spalte `palimpsestiert` bleibt bei allen drei Einträgen leer.

## Nachtrag v46: Pal. lat. 1513 / LHS0256

Der Eintrag zu `LHS0256 / TXT0280` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_1513` präzisiert. BL weist eine einzige oberste Inhaltseinheit aus: Cicero, `De finibus bonorum et malorum`, `1va-44rb`, unvollständig. Daher erfolgt keine Aufspaltung.

Normierung: Die Einordnung bleibt `Buchgattung = Philosophischer Dialog`, `Thema = Philosophie`, `Überlieferungslinie = Klassische lateinische Literatur`. Die besondere Überlieferungsstellung der Handschrift — ältester überlieferter Textzeuge, Zugehörigkeit zur sog. deutschen Familie bzw. zu den codices meliores — wird in den `Bemerkungen` gesichert. `palimpsestiert` bleibt leer.



## Nachtrag v48 / Materialisierung v7-21 – Rollback Zürich, Ms. C 132

Die Materialisierung v7-20 wurde zurückgenommen. Die Zuordnung von `Zürich, Zentralbibliothek, Ms. C 132` zu `LHS0127` war fehlerhaft.

Grund:
- Die Bischoff-Ausgangstabelle führt `LHS0127` als `Vat. lat. 11506` mit `Cicero, De inv.; Priscianus`, Entstehung `IX¾`, Herkunft/Provenienz `Weißenburg`.
- Der BL-Begleittext `zbz_msc132` beschreibt dagegen `Zürich, Zentralbibliothek, Ms. C 132`: Cicero, `De inventione`, `Rhetorica ad Herennium`, späterer Index und Sakramentarfragment; das ist nicht dieselbe Handschrift.

Regel: Eine BL-Beschreibung darf eine Tabellenzeile nur ersetzen, wenn Signatur/Siegel bzw. Handschriftenidentität sicher übereinstimmen. Inhaltliche Ähnlichkeit, z. B. `Cicero, De inventione`, genügt nicht.

Folge:
- `v7-21` stellt für `LHS0127` wieder die zwei Zeilen aus `v7-19` her.
- `zbz_msc132` wird vorerst nicht in die Forschungstabelle aufgenommen, solange keine passende LHS-ID aus der Bischoff-Ausgangstabelle feststeht.

## Nachtrag v49: Pal. lat. 1756 / LHS0276

Der Eintrag `LHS0276 / TXT0303` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_1756` ersetzt. Die Handschrift besteht aus zwei Faszikeln; der BL-Begleittext weist drei oberste Inhaltseinheiten aus:

- `TXT0303-01`: Pompeius grammaticus, `Commentum artis Donati`, `1r-157v`, Faszikel I, Heidelberg 1464.
- `TXT0303-02`: Anonymus (Pseudo-Cicero), `Rhetorica ad C. Herennium`, `168ra-190rb`, Faszikel II, Entstehungsort unbekannt, 13./14. Jh.
- `TXT0303-03`: Anonymus, `Exercitationes rhetoricae`, `190va-191vb`, Faszikel II.

Normierung: `Commentum artis Donati` bleibt `Buchgattung = Fachtext`, `Untergattung = Grammatik`. Die rhetorischen Texte werden als `Fachtext`, `Untergattung = Rhetorik` geführt. Für die `Exercitationes rhetoricae` wird `Überlieferungslinie = Mittelalterliche Gelehrsamkeit` verwendet.

Lorsch-Bezug: Bei allen drei Einträgen bleibt `Lorsch-Bezug` leer. Der BL-Begleittext vermerkt ausdrücklich, dass fraglich ist, ob die Handschrift oder einer ihrer Teile jemals in Lorsch war. Die Nennung von Handschriften gleichen Inhalts in den karolingischen Lorscher Bibliothekskatalogen wird nur in den Bemerkungen gesichert.

Palimpsest-Regel: Faszikel II ist auf palimpsestiertem Pergament geschrieben; die ältere radierte Schrift ist nach BL jedoch nur wenig älter und nicht als eigener Text identifiziert. Daher bleibt `palimpsestiert` bei den erfassten Obertexten leer.



## Nachtrag v50: Nebenliste für nicht bei Bischoff bestätigte Lorscher Identität

Neben der Haupttabelle wird eine separate Kontrolltabelle geführt:

- `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v1.md`
- `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v1.tsv`

Zweck: Erfassung von Texten bzw. Codexteilen, deren Lorscher Identität nicht durch die Bischoff-/LHS-Ausgangstabelle gesichert ist.

Regel:
- Bloßer Schreibort Lorsch, ähnliche Inhaltsangabe oder eine Handschrift gleichen Inhalts genügt nicht für eine LHS-Zuordnung.
- In der Haupttabelle verbleibende, aber nicht als Lorsch bestätigte Fälle behalten ein leeres Feld `Lorsch-Bezug`.
- Nicht identifizierte außerbischoffliche Codices erhalten keine LHS-ID und bleiben außerhalb der Haupttabelle.

Der erste Stand der Nebenliste umfasst:

1. `LHS0231 / bav_pal_lat_824`: Pal. lat. 824, in der Haupttabelle geführt, aber ohne Lorsch-Bezug; BL nennt Provenienz Heidelberg und nur eine Handschrift gleichen Inhalts in den karolingischen Lorscher Bibliothekskatalogen.
2. `LHS0276 / bav_pal_lat_1756`: Pal. lat. 1756, in der Haupttabelle geführt, aber ohne Lorsch-Bezug; BL hält offen, ob die Handschrift oder einer ihrer Teile jemals in Lorsch war.
3. `zbz_msc132`: Zürich, Zentralbibliothek, Ms. C 132; nach Rollback nicht in der Haupttabelle geführt, da keine sichere Bischoff-/LHS-Identität vorliegt.

## Nachtrag v51: Auslagerung der Nebenlisten-Einträge aus der Haupttabelle

Die Nebenliste wird ab `v2` als echte Auslagerungsliste geführt. Einträge, deren Lorscher Identität nicht durch die Bischoff-/LHS-Ausgangstabelle gesichert ist, werden nicht mehr parallel in der Haupttabelle geführt.

Materialisierung:
- Aus der Haupttabelle `v7-22` entfernt und in der Nebenliste belassen:
  - `TXT0252-01` und `TXT0252-02` zu `bav_pal_lat_824 / Pal. lat. 824`.
  - `TXT0303-01`, `TXT0303-02` und `TXT0303-03` zu `bav_pal_lat_1756 / Pal. lat. 1756`.
- `zbz_msc132` bleibt weiterhin ausschließlich in der Nebenliste und erhält keine LHS-ID.
- Die Nebenliste wurde von `v1` auf `v2` aktualisiert; die Spalte `Haupttabelle` entfällt.

Regel: Die Haupttabelle enthält nur Texte mit gesicherter Bischoff-/LHS-Identität. Unsichere, außerbischoffliche oder nur durch Schreibort/ähnlichen Inhalt verbundene Fälle werden ausschließlich in der Nebenliste geführt.

## Nachtrag v52: Pal. lat. 889 / LHS0243

Der bisherige Platzhalter `LHS0243 / TXT0265 / Sallust / Opera` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_889` ersetzt. Die Handschriftenidentität ist gesichert: Die Bischoff-Ausgangstabelle führt `Pal. lat. 889` als Lorscher Sallust-Handschrift, und BL bestätigt Entstehungsort und Provenienz Lorsch.

Erfasst werden nach den obersten BL-Inhaltseinheiten:

- `TXT0265-01`: `Hymnus de oratione dominica`, Nachtrag auf dem ungezählten Blatt vor Bl. 1r.
- `TXT0265-02`: Iuvenalis, `De Catilina, Cicerone et Mario excerpta IV ex Saturis`, Nachtrag auf dem ungezählten Blatt vor Bl. 1r.
- `TXT0265-03`: Anonymus, `Accessus in Sallustium`, Nachtrag auf dem ungezählten Blatt vor Bl. 1v.
- `TXT0265-04`: Sallustius, `De coniuratione Catilinae cum glossis`, ungezähltes Bl. vor Bl. 1v und 1r-35v.
- `TXT0265-05`: Sallustius, `De bello Iugurthino`, ungezähltes Bl. vor Bl. 1v und 35v-102v.
- `TXT0265-06`: Anonymus, `Translatio sanctorum Benedicti et Scholasticae in Galliam`, 102v-103v.

Normierung: Die beiden Sallust-Texte bleiben `Buchgattung = Geschichtswerk`, `Thema = Geschichte`, `Überlieferungslinie = Klassische lateinische Literatur`. Der Accessus wird als `Fachtext`, `Untergattung = Accessus`, `Thema = Literaturkunde` geführt. Die Translatio wird als `Hagiographie`, `Thema = Heiligenverehrung`, `Überlieferungslinie = Hagiographische Tradition` geführt. Die neue Spalte `palimpsestiert` bleibt bei allen Einträgen leer.

## Nachtrag v53: Pal. lat. 492 / LHS0211

Der bisherige Platzhalter `LHS0211 / TXT0232 / Albertus de Ferrariis / Werk unbestimmt` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_492` ersetzt. Die Handschriftenidentität ist gesichert: Die Bischoff-Ausgangstabelle führt `Pal. lat. 492` mit `Albertus de Ferrariis; Eberhardus praep. Laur.`; BL bestätigt die Provenienz Lorsch, erschlossen aus Briefen u. Ä. des Lorscher Propstes Eberhard.

Erfasst werden nach den obersten BL-Inhaltseinheiten:

- `TXT0232-01`: Albertus Trottus (de Ferrariis), `De horis canonicis`, 2r-19v.
- `TXT0232-02`: Iohannes Serra, `Ars nova epistolarum`, 25v-54r.
- `TXT0232-03`: Eberhardus praepositus Laureshamensis, `Epistulae et testimonium de visitatione a. 1467-1469`, 54v-60r.
- `TXT0232-04`: Balthasar Rasinus, `Epistulae`, 61r-78r.
- `TXT0232-05`: Cicero, `Epistulae ad familiares selectae`, 79r-111r.
- `TXT0232-06`: Eberhardus praepositus Laureshamensis, `Testimonium de visitatione a. 1469`, 111v-112v.
- `TXT0232-07`: Guarinus Veronensis und andere, `Epistulae et orationes`, 115r-213v.
- `TXT0232-08`: Homerus Latinus (Baebius Italicus ?), `Ilias Latina`, 215r-233v.

Normierung: `De horis canonicis` wird als `Fachtext`, `Untergattung = Liturgik`, `Thema = Liturgie` geführt. Die Brieflehre des Iohannes Serra wird als `Fachtext`, `Untergattung = Brieflehre` geführt. Die Eberhard-Texte erhalten `Überlieferungslinie = Lorscher Überlieferung`; humanistische Brief- und Redesammlungen erhalten `Überlieferungslinie = Humanismus`. Die `Ilias Latina` wird als `Dichtung`, `Untergattung = Epos` geführt. Die Spalte `palimpsestiert` bleibt bei allen Einträgen leer.



## Nachtrag v54: Pal. lat. 1741 / LHS0272 in Nebenliste ausgelagert

Der bisherige Platzhalter `LHS0272 / TXT0299 / Terentius Scaurus / Werk unbestimmt` wurde nicht in der Haupttabelle ausgebaut, sondern aus der Haupttabelle entfernt und in der Nebenliste erfasst.

Grund: Der BL-Begleittext zu `bav_pal_lat_1741` beschreibt die Provenienz nur als `Lorsch (?) (LEHMANN 1911); Heidelberg`. Der Laurissano-Hinweis betrifft die von Johannes Sichardus besorgte Abschrift bzw. den Druck des Terentius-Scaurus-Texts aus einem `codex Laurissanus`; er sichert nicht die Lorscher Identität der gesamten humanistischen Sammelhandschrift. Da der bisherige Haupttabelleneintrag zudem keinen `Lorsch-Bezug = ja` hatte, wird Pal. lat. 1741 nach der v51-Regel ausschließlich in der Nebenliste geführt.

Die Nebenliste `v3` ergänzt 17 oberste BL-Inhaltseinheiten:

- `TXT0299-01`: Anonymus, `Schemata diversa (de genealogia deorum, poetis, montibus, fluviis etc.) cum notis`, 1v-5v.
- `TXT0299-02`: Anonymus, `Fabularius compendiosus in Ovidii Metamorphoses`, 6r-26r.
- `TXT0299-03`: Conradus de Mure, `Fabularius`, 28r-157r.
- `TXT0299-04`: Albericus Londoniensis (?), `Mythographus Vaticanus III qui dicitur`, 159r-192v.
- `TXT0299-05`: Cicero, `Epistulae ad familiares aliquae subsequentis glossis`, 209r-239v.
- `TXT0299-06`: Anonymus, `Moralia quaedam, proverbium et Iuvenalis versus`, 240r/v.
- `TXT0299-07`: Anonymus, `Reformatio des heiligen gerichtes lingua Germanica`, 241r-242r.
- `TXT0299-08`: Petrus Antonius Finariensis, `Epistulae Heidelbergae scriptae II`, 242r-243r.
- `TXT0299-09`: Q. Terentius Scaurus, `De orthographia liber subsequente De ordinatione partium orationis appendice`, 245r-249v.
- `TXT0299-10`: Cicero, `Oratio pro M. Marcello`, 255r-259r.
- `TXT0299-11`: Pseudo-Cicero, `De optimo genere oratorum`, 260r-262v.
- `TXT0299-12`: Rufinus grammaticus Antiochenus, `De numeris oratorum`, 262v-266r.
- `TXT0299-13`: Martianus Capella, `Ex libro V De nuptiis Philologiae et Mercurii excerpta`, 266v-270v.
- `TXT0299-14`: Anonymus, `De figuris rhetoricis notae diversae`, 270v/271r.
- `TXT0299-15`: Rufius (?) Festus, `Breviarium rerum gestarum populi Romani`, 271r-278r.
- `TXT0299-16`: Anonymus, `Registrum super libros Laurentii Vallae`, 283ra-285va.
- `TXT0299-17`: Anonymus, `Liber monstrorum de diversis generibus`, 286r-291v.

Die Spalte `palimpsestiert` ist nicht betroffen.


## Nachtrag v55: Nebenliste v4 – Häse 328 zu Pal. lat. 1756 / Commentum artis Donati

Die Nebenliste wird von `v3` auf `v4` aktualisiert. Bei `TXT0303-01 / LHS0276 / bav_pal_lat_1756 / Pompeius grammaticus / Commentum artis Donati` wird ergänzt, dass nach dem BL-Begleittext in den karolingischen Lorscher Bibliothekskatalogen laut HÄSE 2002, Nr. 328, eine Handschrift gleichen Inhalts belegt ist.

Diese Ergänzung ist als Hinweis auf einen Lorscher Textbestand gleichen Inhalts zu verstehen. Sie hebt die Nebenlisten-Einstufung nicht auf, weil BL zu Pal. lat. 1756 weiterhin ausdrücklich offen lässt, ob diese Handschrift oder einer ihrer Teile jemals in Lorsch war.

## Nachtrag v56: Pal. lat. 1753 / LHS0274

Der bisherige Platzhalter `LHS0274 / TXT0301 / Marius Victorinus / Ars grammatica` wurde auf Grundlage des BL-Begleittexts zu `bav_pal_lat_1753` ersetzt. Die Handschriftenidentität ist gesichert: Die Bischoff-Ausgangstabelle führt `Pal. lat. 1753`; BL bestätigt Entstehungsort Lorsch, um 800, Älterer Lorscher Stil, Provenienz Lorsch und HÄSE 2002, Nr. 334.

Erfasst werden nach den obersten BL-Inhaltseinheiten:

- `TXT0301-01`: Marius Victorinus; Aelius Festus Asmonius (Aphtonius?), `Ars grammatica; De metris`, 2r-58v.
- `TXT0301-02`: Aelius Festus Asmonius (Aphtonius?) (Marius Victorinus?), `De metris Horatianis`, 59r-62r.
- `TXT0301-03`: Proba, `Cento Vergilianus`, 62r-69r.
- `TXT0301-04`: Pomponius, `Cento Tityri (Versus ad gratiam Domini)`, 69r-70v.
- `TXT0301-05`: Metrorius (Pseudo-Victorinus), `De finalibus metrorum`, 71r-74v.
- `TXT0301-06`: Papirius (Papirianus?), `De orthographia`, 75r.
- `TXT0301-07`: Aldhelmus Scireburnensis, `Epistula ad Acircium sive Liber de septenario, de metris, aenigmatibus ac pedum regulis`, 76v-109v.
- `TXT0301-08`: Symphosius, `Aenigmata`, 110r-111v; 112v-113r.
- `TXT0301-09`: Anonymus, `Precatio`, 112r.
- `TXT0301-10`: Pompeius grammaticus, `Ex commento artis Donati excerptum`, 113v.
- `TXT0301-11`: Bonifatius (?), `Ars metrica`, 114r/v; 116r.
- `TXT0301-12`: Anonymus, `Aenigmata Laureshamensia (vel Anglica)`, 115r/v; 117r/v.
- `TXT0301-13`: Bonifatius (?), `Epitaphium Domberchti`, 116v.

Normierung: Grammatische, orthographische und metrische Traktate werden als `Fachtext` mit `Untergattung = Grammatik`, `Orthographie`, `Metrik` bzw. `Grammatik und Metrik` geführt. Centones, Rätsel und Epitaph erhalten `Buchgattung = Dichtung` mit entsprechender Untergattung. Aldhelm und Bonifatius werden der `Angelsächsischen Gelehrsamkeit` zugeordnet. Die Spalte `palimpsestiert` bleibt bei allen Einträgen leer.



## Nachtrag v57: Brüssel, KBR, Ms. 9845-9848 / LHS0013

Der bisherige Eintrag `LHS0013 / TXT0014 / Magnus Felix Ennodius / Epistulae` wurde auf Grundlage des BL-Begleittexts zu `kbr_ms9845-48` ersetzt. Die Handschriftenidentität ist gesichert: Die Bischoff-Ausgangstabelle führt `Brüssel 9845–48`; BL beschreibt die Provenienz als Lorsch, nennt die Beteiligung einer Hand des Jüngeren Lorscher Stils und führt den karolingischen Katalogeintrag HÄSE 2002, Nr. 301.

Erfasst werden nach den obersten BL-Inhaltseinheiten:

- `TXT0014-01`: Magnus Felix Ennodius, `Opera omnia (Epistularum libri IX, Opuscula miscella 10, Dictiones 28, Carminum et hymnorum libri II)`, 1r-206r.
- `TXT0014-02`: `Officium in natale XI milium virginum`, 206v.

Normierung: Der Ennodius-Hauptbestand wird nicht weiter in die zahlreichen ineinander verschränkten Briefe, Dictiones, Carmina, Opuscula und Hagiographica zerlegt, sondern als oberste BL-Einheit `Opera omnia` geführt. `Buchgattung = Sammlung`, `Thema = Spätantike Literatur`, `Überlieferungslinie = Spätantike Gelehrsamkeit`. Der liturgische Nachtrag des 13. Jh. wird als `Liturgischer Text`, `Untergattung = Officium` geführt. Die Spalte `palimpsestiert` bleibt bei beiden Einträgen leer.


## Normierungsentscheidung v58 / Materialisierung v7-29: `Sammlung` ist keine Buchgattung

`Sammlung`, `Sammelhandschrift` und zusammengesetzte Werte wie `Kanonistische Sammlung` oder `Hagiographische Sammlung` werden nicht mehr als Werte der Spalte `Buchgattung` verwendet. Sie beschreiben einen Überlieferungs- oder Codexzustand, aber keine tragfähige Textgattung.

Regel: Die Spalte `Buchgattung` enthält künftig möglichst eine echte Textform oder einen fachlichen Texttyp. Sammelcharakter, Corpuscharakter oder noch nicht aufgelöste Mischüberlieferung werden in `Titel`, `Untergattung` oder `Bemerkungen` dokumentiert.

Für `LHS0013 / kbr_ms9845-48` wurde deshalb die in v7-28 zu grobe Zeile `Opera omnia` mit `Buchgattung = Sammlung` ersetzt. Der Ennodius-Bestand wird nicht als pauschale Sammlung geführt, sondern in gattungsfähige Hauptgruppen und Einzel-Opuscula gegliedert: `Briefe`, `Rede`, `Dichtung`, `Rechtstext`, `Liturgischer Text`, `Fachtext`, `Hagiographie` und `Autobiographie`.

Zusätzlich wurden ältere Buchgattungswerte mit `Sammlung` oder `Sammelhandschrift` bereinigt:

| bisheriger Buchgattungswert | neuer Umgang |
| --- | --- |
| `Sammlung` | je nach Text: `Florilegium` oder gattungsfähige Auflösung |
| `Kanonistische Sammlung`, `Kanonessammlung` | `Kirchenrecht`, mit `Untergattung = Decretum` oder `Canones` |
| `Hagiographische Sammlung` | `Hagiographie`; Sammelcharakter nur in `Bemerkungen` |
| `Inschriftensammlung` | `Inschriften`, `Untergattung = Sylloge` |
| `Biographiensammlung` | `Biographie`, `Untergattung = De viris illustribus` |
| `Sammelhandschrift` | bei unaufgelösten Platzhaltern leerer Buchgattungswert oder, wenn erkennbar, fachliche Einordnung wie `Fachtext` oder `Liturgischer Text` |

Prüfung v7-29: 466 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal. In `Buchgattung` kommt `Sammlung`/`Sammelhandschrift` nicht mehr vor.


---

## Nachtrag v59 / Tabellenstand v7-30: Pal. lat. 1449

**Neue Tabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-30.md`  
**Ausgangstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-29.md`

### Materialisierte BL-Auswertung

`Pal. lat. 1449 / LHS0255` wurde anhand der BL-Beschreibung vollständig als sicherer Lorscher Codex erfasst. Die beiden alten Platzhalter `TXT0278` (`Computus`) und `TXT0279` (`Beda, De temporum ratione`) wurden entfernt und durch zwanzig Einträge `TXT0278-01` bis `TXT0278-20` ersetzt.

### Klassifikationsentscheidungen

- Der im BL-Titel genannte Sammelcharakter der Handschrift wird nicht als `Buchgattung` verwendet.
- Komputistische Texte, Kalenderrechenstücke, Ostertafeln und Mondsprungnotizen stehen unter `Buchgattung = Fachtext`, meist mit `Untergattung = Computus`.
- `Kalendarium Laureshamense cum additamentis` wird analog zu anderen Lorscher Kalendern als `Fachtext / Computus` geführt; die liturgische bzw. lokale Funktion steht in `Überlieferungslinie` und `Bemerkungen`.
- Beda, `De temporum ratione` wurde nach der BL-Struktur in den Hauptteil `cap. I-LXV` und die `Chronica maiora` (`cap. LXVI-LXXI`) getrennt; die Chronica maiora stehen als `Chronik`.
- Die drei kleinen `Tractatuli` auf 120r/v wurden wegen unterschiedlicher Gegenstände in drei Einträge getrennt: Namenskunde, medizinische Zeichenlehre und Diätetik.
- Nachträge bleiben mit `Lorsch-Bezug = ja`, weil die Handschrift sicher Lorsch ist; sie werden im Feld `Bemerkungen` als Nachträge gekennzeichnet.


## Nachtrag v60 / Tabellenstand v7-31: Normierung `Iatromathematik`

Für `LHS0255 / Pal. lat. 1449 / TXT0278-20` wurde die Klassifikation des Textes `Sphaera Pythagorae philosophi quam Apologius descripsit` präzisiert. `Iatromathematik` wird nicht als Untergattung geführt, sondern nur erklärend in der Bemerkung belassen.

Neue Normierung:

| Feld | Wert |
| --- | --- |
| `Buchgattung` | `Fachtext` |
| `Untergattung` | `Prognostik` |
| `Thema` | `Medizinische Astrologie` |
| `Überlieferungslinie` | `Frühmittelalterliche Gelehrsamkeit` |

Begründung: Der Text ist ein onomatomantisch-iatromathematisches Prognoseinstrument mit Schaubild; die spezielle Terminologie bleibt in `Bemerkungen`, während die tabellarische Normalform verständlicher und anschlussfähiger bleibt.


## v61 / Materialisierung v7-32 – Normierung Artes liberales

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-31.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-32.md`.
- Anlass: Bei Texten der Artes liberales wurden bisher häufig `Untergattung` und `Thema` identisch geführt, z. B. `Dialektik | Dialektik`, `Arithmetik | Arithmetik`, `Grammatik | Grammatik`.
- Neue Regel: `Buchgattung = Fachtext`, `Untergattung = Artes liberales`, `Thema = jeweilige Ars`.
- Als Themenwerte verwendet: `Grammatik`, `Rhetorik`, `Dialektik`, `Arithmetik`, `Musik`, `Astronomie`; bei Mehrfachbezug zusätzlich `Trivium`, `Quadrivium`, `Sieben freie Künste` und bei einer gemischten Glossenreihe `Enzyklopädie`.
- `Überlieferungslinie` wurde für diese Artes-Einträge einheitlich auf `Spätantike Gelehrsamkeit` gesetzt.
- Metrik und Orthographie werden innerhalb der Artes unter `Thema = Grammatik` geführt.
- Artes-Kommentare, Glossen und Exzerpte werden nicht mehr als `Buchgattung = Kommentar` separiert, sondern als `Fachtext / Artes liberales`; Kommentar- bzw. Exzerptcharakter bleibt in Titel und Bemerkungen erkennbar.
- Fünf palimpsestierte klassische Reden bzw. Rede-Fragmente wurden nicht als Artes-Texte umgestellt, sondern als `Buchgattung = Rede`, `Thema = Rhetorik` normalisiert.
- Audit-Datei: `materialisierung_v7-32_artes_liberales_normierung.tsv`.

Prüfung: 484 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal. In der Spalte `Untergattung` kommen die alten Artes-Disziplinwerte `Grammatik`, `Rhetorik`, `Dialektik`, `Arithmetik`, `Metrik`, `Orthographie` und `Musiktheorie` nicht mehr vor.


---

## v62 / Materialisierung v7-33 – Pal. lat. 169

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-32.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-33.md`.
- BL-Grundlage: `bav_pal_lat_169.pdf`.

### Materialisierte BL-Auswertung

`Pal. lat. 169` wurde den bestehenden Einträgen `LHS0142` und `LHS0143` zugeordnet. Die beiden bereits vorhandenen Platzhalter wurden nicht aufgespalten, sondern bibliographisch und klassifikatorisch präzisiert:

- `TXT0158 / LHS0142`: Ambrosiaster qui dicitur (Pseudo-Ambrosius), `Commentarius in epistulas Paulinas ad Corinthios (ex Pelagio interpolatus)`, 1v/2r-150v.
- `TXT0159 / LHS0143`: Anonymus, `Nomina Laureshamensis monasterii fratrum`, 151r.

### Klassifikationsentscheidungen

- Der Ambrosiaster-Text bleibt als `Bibelkommentar`; das Thema wurde von dem zu allgemeinen `Exegese` zu `Korintherbriefe` präzisiert.
- Der Pelagius-Anteil wird nicht als eigene Zeile geführt, weil BL den Codex als Ambrosiaster-Kommentar in interpolierter Überlieferungsgruppe beschreibt; der Interpolationsbefund steht in Titel und Bemerkungen.
- Die Mönchsliste wird als `Liste / Namenliste` mit `Thema = Klostergeschichte` und `Überlieferungslinie = Lorscher Überlieferung` geführt.
- `palimpsestiert` bleibt in beiden Zeilen leer.


---

## v63 / Materialisierung v7-34 – Graz, UB, Ms. 1703/124

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-33.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-34.md`.
- Audit-Datei: `materialisierung_v7-34_ubg_ms1703_124_aenderungen.tsv`.
- Betroffener Eintrag: `TXT0029 / LHS0028`.
- `Graz, Universitätsbibliothek, Ms. 1703/124` wird als sicherer Lorscher Priscianus-Fragmentzeuge geführt: BL nennt Lorsch als Entstehungsort, 1. Hälfte 9. Jh., Übergangsstil und den karolingischen Katalogbezug `HÄSE 2002, Nr. 332c`.
- Klassifikation nach Artes-Regel v7-32: `Buchgattung = Fachtext`, `Untergattung = Artes liberales`, `Thema = Grammatik`, `Überlieferungslinie = Spätantike Gelehrsamkeit`.
- Fragmentcharakter wird in Titel und Bemerkungen vermerkt.

### Validierung v7-34

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 484 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## v64 / Materialisierung v7-35 – Zürich, Zentralbibliothek, Ms. Car. C 131

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-34.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-35.md`.
- BL-Grundlage: `zbz_mscarc131.pdf`.
- Audit-Datei: `materialisierung_v7-35_zbz_mscarc131_aenderungen.tsv`.
- Betroffener Eintrag: `TXT0347 / LHS0317`.

### Materialisierte BL-Auswertung

`Zürich, Zentralbibliothek, Ms. Car. C 131` wird als sicherer Lorscher Codex geführt. Der bisherige Kurzeintrag `Didymus der Blinde, De Spiritu Sancto` wurde präzisiert zu:

- `Didymus Alexandrinus`, `Liber de spiritu sancto secundum Hieronymi translationem (unvollständig)`, `Iv/1r-23v`.

### Klassifikationsentscheidung

- `Buchgattung = Fachtext`.
- `Untergattung = Traktat`.
- `Thema = Dogmatik`.
- `Überlieferungslinie = Griechische Patristik`.
- Der Übersetzungs- und Prologbefund wird in `Bemerkungen` dokumentiert: lateinische Übersetzung des Hieronymus mit dessen Prolog; erhalten ist etwa die Hälfte des Textes.
- `palimpsestiert` bleibt leer; `Lorsch-Bezug = ja` bleibt gesetzt.

### Validierung v7-35

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 485 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## v65 / Materialisierung v7-36 – Pal. lat. 189

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-35.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-36.md`.
- Audit-Datei: `materialisierung_v7-36_pal_lat_189_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-36-001 | `LHS0154 / Pal. lat. 189` | `Augustinus, De doctrina christiana` mit BL-Siegel, Seitenangabe, Thema `Hermeneutik` und Bemerkung zum vorangestellten Retractationes-Prolog aktualisiert. | 1 Zeile |
| UM-v7-36-002 | Klassifikation | Bestehende Hauptgattung `Fachtext / Traktat` bestätigt; `Thema` nach BL auf `Hermeneutik` präzisiert. Die `Retractationes II,4,30` werden nicht als eigene Textzeile abgespalten, sondern in den Bemerkungen festgehalten. | 1 Zeile |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 484 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## v66 / Materialisierung v7-37 – Pal. lat. 886, Pal. lat. 1578, Pal. lat. 1579

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-36.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-37.md`.
- BL-Grundlagen: `bav_pal_lat_886.pdf`, `bav_pal_lat_1578.pdf`, `bav_pal_lat_1579.pdf`.
- Audit-Datei: `materialisierung_v7-37_pal_lat_886_1578_1579_aenderungen.tsv`.

### Materialisierte BL-Auswertung

#### Pal. lat. 886, Faszikel VII–VIII

- `TXT0261 / LHS0240`: Macrobius, `Ex Macrobii Saturnalibus excerpta`, 125r-142r.
- `TXT0262 / LHS0240`: `Ex Scriptoribus Historiae Augustae excerpta`, 142r-164r.
- `TXT0263 / LHS0241`: Fulgentius mythographus, `De aetatibus mundi et hominis`, 165r-189v.

Die beiden Faszikel werden als sichere Lorscher Einheiten geführt. Faszikel VII: Lorsch, 1. Hälfte 9. Jh., Jüngerer Lorscher Stil, HÄSE 2002, Nr. 320. Faszikel VIII: Lorsch, 1. Hälfte 9. Jh., Übergangsstil, HÄSE 2002, Nr. 72.

#### Pal. lat. 1578

Der bisherige Einzelplatzhalter `TXT0286 / LHS0260 / Fulgentius, Mythologiae` wurde in drei BL-Einheiten aufgespalten:

- `TXT0286-01`: Fulgentius mythographus, `Mythologiae (Mitologiae) (unvollständig)`, 1v-23v.
- `TXT0286-02`: Fulgentius mythographus, `Expositio sermonum antiquorum`, 23v/24r-28r.
- `TXT0286-03`: Fulgentius mythographus, `Expositio Virgilianae continentiae secundum philosophos moralis`, 28r-36r.

Alle drei bleiben unter `LHS0260`, da sie zu demselben sicher Lorscher Codex `Pal. lat. 1578` gehören. BL: Lorsch, um 800, Älterer Lorscher Stil, HÄSE 2002, Nr. 347.

#### Pal. lat. 1579, Faszikel I

- `TXT0287 / LHS0261`: Fulgentius mythographus, `Expositio Virgilianae continentiae secundum philosophos moralis`, 1r-15v.
- `TXT0288 / LHS0262`: Gregorius Magnus, `Dialogorum ex libro II excerptum`, 16r.

`TXT0288` wird als Nachtrag einer Lorscher Hand aus der 1. Hälfte des 10. Jh. geführt; es handelt sich um Greg. M. dial. II,2,4-3,3.

### Klassifikationsentscheidungen

- Fulgentius, `Mythologiae`: `Fachtext / Mythographie / Mythologie / Spätantike Gelehrsamkeit`.
- Fulgentius, `Expositio sermonum antiquorum`: `Fachtext / Glossar / Lexikographie / Spätantike Gelehrsamkeit`.
- Fulgentius, `Expositio Virgilianae continentiae`: `Kommentar / [leer] / Literatur / Spätantike Gelehrsamkeit`; der allegorisch-moralische Charakter steht in `Bemerkungen`, nicht in `Untergattung`.
- Macrobius, `Saturnalia`-Exzerpte: `Fachtext / Dialog / Altertumskunde / Spätantike Gelehrsamkeit`.
- `Historia Augusta`-Exzerpte: `Geschichtswerk / Biographie / Geschichte / Spätantike Gelehrsamkeit`.
- Fulgentius, `De aetatibus mundi et hominis`: `Geschichtswerk / Chronographie / Geschichte / Spätantike Gelehrsamkeit`.
- Gregorius-Magnus-Exzerpt: `Hagiographie / Dialog / Hagiographie / Lateinische Patristik`.

### Validierung v7-37

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 486 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## v67 / Materialisierung v7-38 – Pal. lat. 200

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-37.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-38.md`.
- BL-Grundlage: `bav_pal_lat_200.pdf`.
- Audit-Datei: `materialisierung_v7-38_pal_lat_200_aenderungen.tsv`.

### Materialisierte BL-Auswertung

Der bisherige Einzelplatzhalter `TXT0175 / LHS0157 / Augustinus, De civitate Dei` wurde in zwei BL-Einheiten aufgespalten:

- `TXT0175-01`: Augustinus, `De civitate Dei (libb. XVIII-XXII)`, 1va-138vb.
- `TXT0175-02`: `Lectio officii in sabbato sancto ad matutinum`, 139ra/rb.

`Pal. lat. 200` wird als sichere Lorscher Handschrift geführt: Lorsch, 1. Hälfte 9. Jh., Übergangsstil; Besitzvermerk `Codex de monasterio sancti Nazarii in Lauresham`; karolingischer Katalogbezug HÄSE 2002, Nr. 80. Für den Haupttext ist außerdem der Schreiber Donadeus mit Kolophon auf 138vb berücksichtigt.

### Klassifikationsentscheidungen

- Augustinus, `De civitate Dei`: `Fachtext / Traktat / Theologie / Lateinische Patristik`.
- Die vorangestellten Capitula aus dem sogenannten `Breviculus` werden nicht als eigene Textzeilen abgespalten, sondern in `Bemerkungen` dokumentiert.
- Die neumierte Karsamstagslektion wird als einzelner liturgischer Nachtrag geführt: `Liturgischer Text / Offiziumslektion / Liturgie / Liturgische Tradition`. Sie ist kein `Liturgisches Buch`.

### Validierung v7-38

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 487 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## v68 / Materialisierung v7-39 – Karlsruhe, BLB, Aug. perg. 105

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-38.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-39.md`.
- BL-Grundlage: `blb_augperg105.pdf`.
- Audit-Datei: `materialisierung_v7-39_blb_augperg105_aenderungen.tsv`.

### Materialisierte BL-Auswertung

Der bisherige Einzelplatzhalter `TXT0040 / LHS0036 / Hieronymus, Epistulae` wurde nach BL in einen Hieronymus-Haupteintrag und separate Einträge für die ausdrücklich ausgewiesenen anderen Autoren Isidor und Damasus aufgespalten:

- `TXT0040-01`: Hieronymus, `Hieronymi epistulae et opuscula`, 1r-2v; 4ra-234va.
- `TXT0040-02`: Isidor von Sevilla, `De differentiis rerum sive Differentiae theologicae vel spiritales (Auszug)`, 3r/v.
- `TXT0040-03`: Damasus papa, `Epistula ad Hieronymum (ep. 8 = Hier. ep. 19)`, 41v; 47rb/va.
- `TXT0040-04`: Damasus papa, `Epistula ad Hieronymum (ep. 9 = Hier. ep. 35)`, 46va-47rb.

`Aug. perg. 105` wird als sichere Lorscher Handschrift geführt: Lorsch, um 800, Älterer Lorscher Stil, karolingischer Katalogbezug HÄSE 2002, Nr. 172; später Reichenau.

### Klassifikationsentscheidungen

- Der Hieronymus-Hauptbestand bleibt wegen des dominierenden Briefcorpus als `Briefe / [leer] / Briefliteratur / Lateinische Patristik` geführt; Opuscula und zugeschriebene bzw. eingefügte Stücke werden in den Bemerkungen dokumentiert.
- Isidors theologischer Differenzen-Auszug wird als `Fachtext / Traktat / Dogmatik / Spätantike Gelehrsamkeit` geführt.
- Damasus wird als Briefautor separat ausgewiesen: `Briefe / [leer] / Theologie / Lateinische Patristik`.
- Die doppelte Überlieferung von Damasus ep. 8 = Hier. ep. 19 wird in einer Textzeile zusammengeführt, nicht zweimal als eigenes Werk gezählt.

### Validierung v7-39

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 490 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## v69 / Materialisierung v7-40 – Pal. lat. 829

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-39.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-40.md`.
- BL-Grundlage: `bav_pal_lat_829.pdf`.
- Audit-Datei: `materialisierung_v7-40_pal_lat_829_aenderungen.tsv`.

### Materialisierte BL-Auswertung

Der bisherige Einzelplatzhalter `TXT0254 / LHS0233 / Orosius, Historiae adversus paganos` wurde nach BL in drei Einheiten aufgespalten:

- `TXT0254-01`: Orosius, `Historiae adversum paganos (unvollständig)`, Av/1r-113r.
- `TXT0254-02`: Ps.-Sulpicius Severus, `Epistulae`, 113r-115r.
- `TXT0254-03`: Anonymus, `Tabula circularis orbis terrae`, 115v.

`Pal. lat. 829` wird als sichere Lorscher Handschrift geführt: Lorsch, um 800; 1r-44v im Älteren Lorscher Stil, 45r-115r in insularer Minuskel; karolingischer Katalogbezug HÄSE 2002, Nr. 64. Die althochdeutsche Interlinearglosse zu Orosius auf 86v wird in den Bemerkungen zu `TXT0254-01` dokumentiert.

### Klassifikationsentscheidungen

- Orosius bleibt `Geschichtswerk / [leer] / Geschichte / Lateinische Patristik`.
- Die Ps.-Sulpicius-Severus-Briefe werden als `Briefe / [leer] / Briefliteratur / Lateinische Patristik` geführt; ep. 7 als Ps.-Pelagius wird nur in den Bemerkungen dokumentiert.
- Die T-O-Weltkarte wird als `Fachtext / Kosmographie / Geographie / Mittelalterliche Gelehrsamkeit` geführt. Sie ist ein Nachtrag und kein eigenständiges liturgisches oder historiographisches Werk.

### Validierung v7-40

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 492 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## v70 / Materialisierung v7-41 – Pal. lat. 1635 und Pal. lat. 1646

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-40.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-41.md`.
- BL-Grundlagen: `bav_pal_lat_1635.pdf`, `bav_pal_lat_1646.pdf`.
- Audit-Datei: `materialisierung_v7-41_pal_lat_1635_1646_aenderungen.tsv`.

### Materialisierte BL-Auswertung

`LHS0266 / Pal. lat. 1635` wurde nach BL präzisiert. Der Vergil-Platzhalter `TXT0292 / Vergil, Opera` wurde in drei Werkteile aufgespalten:

- `TXT0292-01`: Vergilius, `Eclogae sive Bucolica cum glossis ex Servio`, 1r-18v.
- `TXT0292-02`: Vergilius, `Georgica cum argumentis metricis et glossis ex Servio`, 19v/20r-67v.
- `TXT0292-03`: Vergilius, `Aeneis cum argumentis metricis et glossis ex Servio`, 68r-283v.

`TXT0293 / Seneca` wurde als `(Ps.-)Seneca philosophus, Tragoediae cum argumentis et glossis`, 284r-486r, präzisiert; die pseudo-senecanischen Stücke `Octavia` und `Hercules Oetaeus` werden in den Bemerkungen dokumentiert.

`LHS0267 / Pal. lat. 1646` wurde nach BL präzisiert. Der Servius-Platzhalter `TXT0294 / Servius, Commentarius in Vergilium` wurde in Haupttext und zwei Nachträge aufgespalten:

- `TXT0294-01`: Servius grammaticus, `Commentarii in Vergilii opera`, 1ra-221rb.
- `TXT0294-02`: Anonymus, `Versus de ortu mundi`, 221va.
- `TXT0294-03`: Anonymus, `Passio cuiusdam monachi secundum luxuriam`, 221vb.

### Klassifikationsentscheidungen

- Die Vergil-Texte bleiben unter `Dichtung / Literatur / Klassische lateinische Literatur`; die Werkformen stehen in `Untergattung` (`Bukolik`, `Lehrgedicht`, `Epos`).
- Die Seneca-Tragödien werden als `Drama / Tragödie / Literatur / Klassische lateinische Literatur` geführt.
- Servius wird gemäß der Artes-liberales-Regel als `Fachtext / Artes liberales / Grammatik / Spätantike Gelehrsamkeit` geführt; die Kommentarform bleibt im Titel und in den Bemerkungen sichtbar.
- `Versus de ortu mundi` wird als `Dichtung / Lehrgedicht / Kosmologie / Mittelalterliche Gelehrsamkeit` geführt.
- `Passio cuiusdam monachi secundum luxuriam` wird wegen ihres parodistischen Charakters als `Dichtung / Parodie / Literatur / Mittelalterliche Gelegenheitsdichtung` geführt.
- `palimpsestiert` bleibt bei allen neuen Einträgen leer.

### Validierung v7-41

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 496 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## v71 / Materialisierung v7-42 – Pal. lat. 46

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-41.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-42.md`.
- BL-Grundlage: `bav_pal_lat_46.pdf`.
- Audit-Datei: `materialisierung_v7-42_pal_lat_46_aenderungen.tsv`.

### Materialisierte BL-Auswertung

`LHS0133 / Pal. lat. 46` wurde nach BL präzisiert. Der bisherige Platzhalter `TXT0148 / Evangelia` wurde in sechs Text- bzw. Paratexteinheiten aufgespalten:

- `TXT0148-01`: Hieronymus, `Praefatio in evangelio (Novum opus)`, 1r-3r.
- `TXT0148-02`: Hieronymus, `Commentarius in Mattheum, Praefatio (Auszug; Plures fuisse)`, 3r-4v.
- `TXT0148-03`: Anonymus, `Canones evangeliorum`, 4v/5r-9r.
- `TXT0148-04`: Ps.-Hieronymus, `Argumentum in canones evangeliorum (Sciendum tamen)`, 9v.
- `TXT0148-05`: `Evangelia IV cum argumentis ac capitulis`, 10r-137v.
- `TXT0148-06`: `Capitulare evangeliorum`, 137v-149r.

Die Handschrift wird nicht als sicher in Lorsch entstanden formuliert. BL nennt als Entstehungsraum das linksrheinische Gebiet (?) bzw. das Gebiet zwischen Rhein und Maas (?) und als Provenienz `Lorsch (?)`; zugleich verweist BL auf karolingische Katalogeinträge HÄSE 2002, Nr. 15-18 und auf wahrscheinliche Lorscher Korrekturen im 9. Jh. Der Lorsch-Bezug bleibt daher `ja`, aber mit ausdrücklicher Unsicherheitsnotiz in den Bemerkungen.

### Klassifikationsentscheidungen

- Hieronymus-Prologe und der pseudo-hieronymische Kanones-Text werden als biblische Paratexte geführt: `Bibelexegese`, bei den Prologen mit `Untergattung = Prolog`.
- Die Eusebianischen `Canones evangeliorum` werden nicht als kirchenrechtliche `Canones`, sondern als `Bibelexegese / Kanontafeln / Evangelienharmonie / Spätantike Gelehrsamkeit` geführt.
- Der eigentliche Evangelientext wird als `Bibeltext / Evangelienbuch / Bibel / Christlicher Kanon` geführt; Argumenta und Capitula bleiben im Titel und in den Bemerkungen sichtbar.
- Das `Capitulare evangeliorum` wird als liturgischer Gebrauchstext klassifiziert: `Liturgischer Text / Evangeliencapitulare / Liturgie / Liturgische Tradition`.
- Der Schreibervermerk des Klerikers Jonathan wird in den Bemerkungen zu `TXT0148-05` dokumentiert.
- Die Frankenthaler Korrektur- und Benutzungsgeschichte wird in den Bemerkungen zu `TXT0148-06` dokumentiert.
- `palimpsestiert` bleibt bei allen neuen Einträgen leer.

### Validierung v7-42

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 501 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |



## Materialisierung v7-43: Leiden, UB, BPL 36 / LHS0041

### Quelle und Zuordnung

BL beschreibt BPL 36 als Martianus-Capella-Codex mit Nachtrag auf 130r und einem später eingebundenen Fragmentblatt 131. Für Bll. 1-130 nennt BL als Entstehungsort nach Bischoff `Lorsch`, 2. Hälfte bzw. Ende 9. Jh., `Jüngerer Lorscher Stil (Spätphase)` und den karolingischen Katalogbezug HÄSE 2002, Nr. 13. Zugleich werden abweichende Lokalisierungen bzw. Unsicherheiten in der Forschung genannt: Auxerre (?) nach Préaux und eventuell Lorsch (?) nach Leonardi.

### Tabellenänderung

Der bisherige Platzhalter `TXT0047 / Martianus Capella / De nuptiis Philologiae et Mercurii` wurde nach BL in zwei Haupttabellenzeilen überführt:

- `TXT0047-01`: Martianus Capella, `De nuptiis Philologiae et Mercurii cum glossis`, 1r-129v.
- `TXT0047-02`: Lupus Ferrariensis, `Epistula respondens ad quaestionem: Quid sit ceroma (ep. add. 6)`, 130r.

Das Nachstoßblatt 131 mit Gregor dem Großen, `Moralia sive Expositio in Iob` II,55-62, wurde nicht in die Haupttabelle übernommen: BL beschreibt es als Fragment aus Frankreich (?) des 12. Jh.; ein gesicherter Lorscher Textbestand ist dafür nicht erkennbar.

### Klassifikationsentscheidungen

- Martianus Capella wird nach der Artes-Regel als `Fachtext / Artes liberales / Sieben freie Künste / Spätantike Gelehrsamkeit` geführt.
- Die Glossen und Schemata werden nicht als eigene Textzeilen abgespalten, sondern in den Bemerkungen zu `TXT0047-01` dokumentiert. Die Schemata 128r-129v beziehen sich nach BL auf Dialektik, Arithmetik, Astronomie und Musik.
- Lupus Ferrariensis wird als `Briefe / Worterklärung / Karolingische Gelehrsamkeit` geführt, weil der Nachtrag formal eine Epistula ist, inhaltlich aber eine gelehrte Worterklärung zu `ceroma` bietet.
- `palimpsestiert` bleibt bei beiden aufgenommenen Einträgen leer.

### Validierung v7-43

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 502 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## Materialisierung v7-44: Vatikan, BAV, Pal. lat. 1877 / LHS0279-LHS0281

### Quelle und Zuordnung

BL beschreibt Pal. lat. 1877 als aus vier Faszikeln zusammengesetzten Codex. Für die Haupttabelle wurden die drei Lorscher Katalogfaszikel übernommen: Faszikel I mit HÄSE C / Bischoff III, Faszikel III mit HÄSE B / Bischoff II und Faszikel IV mit HÄSE A / Bischoff I.

Faszikel II, der Fuldaer Bibliothekskatalog mit vier Fuldaer Bücherlisten, wurde nicht in die Haupttabelle aufgenommen. BL nennt für diesen Faszikel Entstehungsort und Provenienz Fulda; ein Lorsch-Bezug ist nur unsicher formuliert.

### Tabellenänderung

Die bisherigen Platzhalter wurden präzisiert:

- `TXT0306 / LHS0279`: `Catalogus codicum monasterii Laureshamensis (HÄSE C)`, 1r-34r.
- `TXT0307 / LHS0280`: `Catalogus codicum monasterii Laureshamensis (HÄSE B) (unvollständig)`, 44ra-66vb.
- `TXT0308 / LHS0281`: `Catalogus codicum monasterii Laureshamensis (HÄSE A) (unvollständig)`, 67ra-79vb.

### Klassifikationsentscheidungen

- Alle drei Lorscher Kataloge werden als `Katalog / Bibliothekskatalog / Bibliothekswesen / Lorscher Überlieferung` geführt.
- Die Zählung HÄSE A/B/C und Bischoff I/II/III wird in Titel und Bemerkungen dokumentiert.
- Für HÄSE C wird die Gerward-Bücherliste innerhalb der Bemerkungen festgehalten, aber nicht als eigene Textzeile abgespalten.
- Für HÄSE B wird die abweichende bzw. vorsichtige Lokalisierung dokumentiert: BL nennt Nord(ost)frankreich (?) und zugleich die Vermutung, die Handschrift sei wohl in Lorsch von westfränkischen Schreibern geschrieben worden und dort verblieben.
- `palimpsestiert` bleibt leer.

### Validierung v7-44

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 502 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## Materialisierung v7-45: Vatikan, BAV, Pal. lat. 822 / LHS0230

### Quelle und Zuordnung

BL beschreibt Pal. lat. 822 als Rufinus-Aquileiensis/Eusebius-Caesariensis-Codex: `Eusebii Caesariensis Historia ecclesiastica ex Graeco in Latinum translata et continuata`, 1r-175v. Die Bischoff-Zuordnung in der Primärtabelle ist sicher: `LHS0230 / Pal. lat. 822 / Eusebius, Hist. eccl.`, VIII/IX, Schriftheimat und Bibliotheksheimat Lorsch.

### Tabellenänderung

`TXT0251` wurde nicht gesplittet, sondern präzisiert:

- `TXT0251 / LHS0230`: Rufinus Aquileiensis; Eusebius Caesariensis, `Eusebii Caesariensis Historia ecclesiastica ex Graeco in Latinum translata et continuata`, 1r-175v.

Die BL-Untergliederung — Prolog 1r/v, Translatio libri I-IX 1v-148r, Continuatio libri X-XI 148r-175v — wurde in den Bemerkungen dokumentiert, aber nicht als separate Textzeilen abgespalten, weil sie zusammen den einen in BL ausgewiesenen Werkkomplex bilden.

### Klassifikationsentscheidungen

- Die frühere `Buchgattung = Kirchengeschichte` wurde auf `Geschichtswerk` normalisiert; `Kirchengeschichte` steht jetzt in `Untergattung` und `Thema`.
- `Überlieferungslinie = Griechische Patristik` wurde beibehalten, weil der Textkomplex auf Eusebius beruht; die lateinische Übersetzung und Fortsetzung durch Rufinus wird in Autor, Titel und Bemerkungen sichtbar.
- Der Befund der angelsächsischen Vorlage, der übernommenen bzw. vorlagengebundenen Randerläuterungen und des Canterbury-/Leidener-Glossar-Kontexts wurde in die Bemerkungen aufgenommen.
- `palimpsestiert` bleibt leer.

### Validierung v7-45

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 502 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |



---

## Materialisierung v7-46: Oxford, Bodleian Library, MS. Laud. misc. 276 / LHS0099

### Quelle und Zuordnung

BL beschreibt MS. Laud. misc. 276 als Lorscher Codex der 1. Hälfte bzw. des 2. Viertels bis Mitte des 9. Jh. mit Gregorius Nazianzenus in der lateinischen Übersetzung des Rufinus sowie Gregorius Iliberritanus. Die Bischoff-Zuordnung in der Primärtabelle ist `LHS0099 / Laud. misc. 276 / Gregorius Naz., Tract.`, Schriftheimat Lorsch, Bibliotheksheimat Eberbach (?) bzw. spätere Eberbacher Provenienz; BL nennt den karolingischen Katalogbezug HÄSE 2002, Nr. 293.

### Tabellenänderung

Der bisherige Platzhalter `TXT0107 / Gregor von Nazianz / Tractatus` wurde in vier gattungsfähige Einträge aufgespalten:

- `TXT0107-01 / LHS0099`: Gregorius Nazianzenus; Rufinus Aquileiensis, `Orationes IX a Rufino Aquileiensi Latine versae`, 1r/v-70v; 81r-85r.
- `TXT0107-02 / LHS0099`: Gregorius Iliberritanus, `De fide (recensio II)`, 71r-80r.
- `TXT0107-03 / LHS0099`: Ps.-Gregorius Iliberritanus (Ps.-Damasus), `Fides Romanorum`, 80r/v.
- `TXT0107-04 / LHS0099`: Alcuinus (?), `Sequentia „Summi regis archangele Michael“`, 85r.

### Klassifikationsentscheidungen

- Die Gregor-von-Nazianz-Orationes werden als `Homilien / Dogmatik / Griechische Patristik` geführt; Rufinus erscheint als lateinischer Übersetzer im Autor- und Titelbereich.
- Gregorius Iliberritanus, `De fide`, wird als `Fachtext / Traktat / Dogmatik / Lateinische Patristik` geführt.
- `Fides Romanorum` wird wegen seiner Form als `Fachtext / Glaubensbekenntnis / Dogmatik / Lateinische Patristik` geführt.
- Die Michaels-Sequenz wird nach der bestehenden Regel als `Dichtung / Sequenz` geführt; der neumierte Nachtrag des späten 10. Jh. und die unsichere Alkuin-Zuschreibung bleiben in den Bemerkungen.
- Die nicht in Lorsch geschulten Hände für 40r-41r und 50v-70v werden in den Bemerkungen dokumentiert, ändern aber wegen der BL- und Bischoff-Zuordnung die LHS-Zuordnung nicht.
- `palimpsestiert` bleibt leer.

### Validierung v7-46

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 505 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## Materialisierung v7-47: Wolfenbüttel, Herzog August Bibliothek, Cod. Guelf. 18.22 Aug. 4° / LHS0309

### Quelle und Zuordnung

BL beschreibt Cod. Guelf. 18.22 Aug. 4° als aus zwei Faszikeln zusammengesetzten Codex. Für die Haupttabelle wurde nur Faszikel I übernommen: ein Evangeliar aus Lorsch, 2. Viertel 11. Jh., von einer Hand geschrieben. Die Bischoff-Zuordnung in der Primärtabelle ist `LHS0309 / Wolfenbüttel, 18.22. Aug. 4° / Evangelia IV`, Schriftheimat Lorsch, spätere Bibliotheksheimat Paderborn, Dominikaner.

Faszikel II (`Apocalypsis cum glossa`, 12./13. Jh., Entstehungsort unbekannt, Provenienz Paderborn) wurde nicht in die Haupttabelle aufgenommen, da kein gesicherter Lorsch-Bezug vorliegt.

### Tabellenänderung

Der bisherige Platzhalter `TXT0339 / LHS0309 / anonym / Evangelia` wurde in zehn gattungsfähige Einträge aufgespalten:

- `TXT0339-01`: Hieronymus, `Commentarius in Mattheum, Praefatio (Auszug; Plures fuisse)`, 1r-2r.
- `TXT0339-02`: Hieronymus, `Praefatio in evangelio (Novum opus)`, 2r-3r.
- `TXT0339-03`: Hieronymus, `Ex epistula ad Paulinum presbyterum excerptum (ep. 53,9)`, 3r.
- `TXT0339-04`: Anonymus, `Canones evangeliorum`, 4r-7r.
- `TXT0339-05`: Anonymus, `Argumentum in Mattheum`, 7v.
- `TXT0339-06`: Anonymus, `Capitulare evangeliorum`, 8r-11r.
- `TXT0339-07`: Anonymus, `Capitulare evangeliorum`, Nachtrag des 13. Jh., 11r-12r.
- `TXT0339-08`: Anonymus, `Carmen rhythmicum in Eusebii canones`, 12v.
- `TXT0339-09`: Aileranus sapiens, `Carmen rhythmicum in Eusebii canones`, 12v.
- `TXT0339-10`: Anonymus, `Evangelia IV cum argumentis`, 13r-115r.

### Klassifikationsentscheidungen

- Die Hieronymus-Prologe und das Matthäus-Argumentum werden als `Bibelexegese / Prolog / Exegese / Lateinische Patristik` geführt.
- Die eusebianischen Kanontafeln werden als `Bibelexegese / Kanontafeln / Evangelienharmonie / Spätantike Gelehrsamkeit` geführt.
- Die beiden Evangeliencapitularia werden als `Liturgischer Text / Evangeliencapitulare / Liturgie / Liturgische Tradition` geführt; der Nachtragscharakter des zweiten Capitulares bleibt in den Bemerkungen sichtbar.
- Die beiden rhythmischen Gedichte zu den eusebianischen Kanones werden als `Dichtung / Merkgedicht / Evangelienharmonie / Frühmittelalterliche Gelehrsamkeit` geführt.
- Der Evangelientext wird als `Bibeltext / Evangelienbuch / Bibel / Christlicher Kanon` geführt.
- Der BL-Hinweis auf karolingische Bibliothekskataloge wird vorsichtig formuliert: Es sind Handschriften gleichen Inhalts nach HÄSE 2002, Nr. 15-18 belegt, nicht zwingend dieser Codex des 11. Jh.
- `palimpsestiert` bleibt leer.

### Validierung v7-47

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 514 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


---

## Materialisierung v7-48: Vatikan, Biblioteca Apostolica Vaticana, Pal. lat. 202 / LHS0159

### Quelle und Zuordnung

BL beschreibt Pal. lat. 202 als Augustinus-Codex um 800 aus dem deutsch-angelsächsischen Gebiet; Lorsch wird bei Lindsay/CLA als Möglichkeit genannt. Die Provenienz ist nach Bischoff/Krämer Lorsch; BL hält außerdem fest, dass der Codex eventuell schon kurz nach der Entstehung nach Lorsch gelangte und zeitgenössische Korrekturen mit Lorscher `hd`/`hl`-Verweiszeichen enthält. Der karolingische Katalogbezug ist HÄSE 2002, Nr. 83. Die Bischoff-Zuordnung in der Primärtabelle ist `LHS0159 / Pal. lat. 202 / Augustinus, De trin.`.

### Tabellenänderung

Der bisherige Platzhalter `TXT0177 / LHS0159 / Augustinus / De trinitate` wurde nicht aufgespalten, sondern nach BL präzisiert:

- `TXT0177`: Augustinus, `De trinitate`, 1r-181va.

### Klassifikationsentscheidungen

- Die Klassifikation bleibt `Fachtext / Traktat / Theologie / Lateinische Patristik`.
- Der sog. Breviculus mit Capitula (1r-6r) und der Prolog `Aug. ep. 174` (6r/v) werden als Bestandteil der De-trinitate-Überlieferung in den Bemerkungen dokumentiert, nicht als eigene TXT-Zeilen geführt.
- Der Textverlust zwischen Bll. 109 und 110, die Zugehörigkeit zur zweiten Textklasse nach Mountain/Glorie, die insularen Schriftmerkmale, die zahlreichen Hände sowie der wahrscheinliche frühe Lorscher Gebrauch werden in den Bemerkungen festgehalten.
- `palimpsestiert` bleibt leer.

### Validierung v7-48

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 514 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |
