# Handbuch_v10 zur Forschungstabelle Lorsch

**Datenbasis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-3.md`

**Version:** v10 – Materialisierung der liturgischen Gebrauchsbücher: `Liturgisches Buch` als Buchgattung, Spezialformen als `Sub-Gattung`.

**Umfang der ausgewerteten Tabelle:** 404 Textzeilen. Erfasst sind die aktuell verwendeten Werte in den Spalten `Buchgattung`, `Werktyp`, `Thema` und `Überlieferungslinie`. Leere Werte wurden nicht als Begriffe aufgenommen.

## Zweck

Dieses Handbuch definiert die bisher verwendeten Normbegriffe der Forschungstabelle. Es ändert die Forschungstabelle nicht. Die Spalte „Homogenisierungsvorschlag“ enthält nur Vorschläge für eine spätere Endredaktion.

## Materialisierung v6-3: liturgische Gebrauchsbücher

Die zuvor besprochene Regel zu liturgischen Gebrauchsbüchern ist in `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-3.md` materialisiert.

| Fall | Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- | --- |
| Sakramentar / Sacramentarium | `Liturgisches Buch` | `Sakramentar` | `Liturgie` |
| Messbuch / Missale | `Liturgisches Buch` | `Messbuch` | `Liturgie` |
| Pontifikale / Pontificale | `Liturgisches Buch` | `Pontifikale` | `Liturgie` |
| Benedictionale | `Liturgisches Buch` | `Benedictionale` | `Liturgie` |
| Ordo Romanus / liturgische Ordnung | `Liturgisches Buch` | `Ordo` | `Liturgie` |

`Liturgisches Buch` bezeichnet damit die Großgattung liturgischer Gebrauchsbücher. Die konkrete Gebrauchsform steht in `Sub-Gattung`. Erklärende Texte über Liturgie bleiben davon getrennt: sie werden als `Fachtext` mit Sub-Gattungen wie `Liturgik`, `Messerklärung` oder `Traktat` geführt.


## Schemaänderung v6-1

Die Forschungstabelle besitzt ab `v6-1` die zusätzliche Spalte `Sub-Gattung` direkt nach `Buchgattung`.

Für biblische Primärtexte gilt:

| Buchgattung | Sub-Gattung | Verwendung |
| --- | --- | --- |
| `Bibeltext` | *(leer)* | Normalfall für biblischen Grundtext; genauer Umfang steht in `Text` und `Werk`. |
| `Bibeltext` | `Evangelienbuch` | Fortlaufende Evangelienüberlieferung. |
| `Bibeltext` | `Evangelistar` | Liturgisch geordnete Evangelienperikopen. |
| `Bibeltext` | `Perikopenbuch` | Liturgisch geordnete biblische Lesungen, sofern nicht genauer als Evangelistar bestimmbar. |
| `Bibeltext` | `Bibel mit Glosse` | Biblischer Grundtext mit beigegebener Glosse. |

`Evangelistar` und `Perikopenbuch` sind liturgisch gebrauchte Bibeltexte. Sie stehen deshalb unter `Bibeltext`; die liturgische Funktion bleibt zusätzlich über `Thema = Liturgie` sichtbar. `Liturgisches Buch` bleibt enger reserviert für liturgische Formulare, Gebete, Ordnungen und Riten, nicht für primär biblische Lesetexte.

## Zwischenstand v8: Reduktion der Buchgattungen durch `Fachtext`

Diese Entscheidung ist als Zwischenstand festgehalten und noch nicht in der Forschungstabelle umgesetzt. Sie ersetzt bzw. korrigiert die ältere vorläufige Regel, `Lehrschrift` als breite Hauptgattung für fachbezogene Texte zu verwenden.

### Grundregel

`Fachtext` wird als vorläufige breite Buchgattung für nicht-biblische, nicht primär liturgische und nicht primär erzählende Texte eingeführt, die Wissen, Begriffe, Regeln, Verfahren oder praktische Anweisungen eines bestimmten Wissensbereichs vermitteln, sammeln oder erklären.

Die Differenzierung erfolgt nicht mehr durch immer neue fachlich spezifizierte Buchgattungen, sondern durch die Kombination der Felder:

| Feld | Funktion | Beispiel |
| --- | --- | --- |
| `Buchgattung` | breite formale Großgattung | `Fachtext` |
| `Sub-Gattung` | nähere Textform oder Gebrauchstyp | `Lehrschrift`, `Handbuch`, `Rezeptsammlung`, `Traktat`, `Ars`, `Messerklärung`, `Glossar` |
| `Thema` | Fachgebiet bzw. Inhalt | `Medizin`, `Arithmetik`, `Grammatik`, `Computus`, `Liturgie`, `Theologie` |
| `Werktyp` | Überlieferungsstatus/Funktion im Codex | `Originalwerk`, `Exzerpt`, `Kompilation`, `Fragment`, `Nachtrag` |
| `Überlieferungslinie` | literarisch-historischer Traditionszusammenhang | `Spätantike Gelehrsamkeit`, `Karolingische Gelehrsamkeit`, `Liturgische Tradition` |

### Konsequenz für medizinische und gelehrte Texte

| bisheriger Wert | künftige Buchgattung | künftige Sub-Gattung | Thema |
| --- | --- | --- | --- |
| `Medizinisches Handbuch` | `Fachtext` | `Handbuch` | `Medizin` |
| `Medizinische Rezepte` | `Fachtext` | `Rezeptsammlung` | `Medizin` |
| `Medizinische Lehrschrift` | `Fachtext` | `Lehrschrift` | `Medizin` |
| Boethius, *De institutione arithmetica* | `Fachtext` | `Lehrschrift` | `Arithmetik` |
| computistische Lehrtexte | `Fachtext` | `Lehrschrift` oder `Traktat` | `Computus` |
| grammatische Lehrtexte | `Fachtext` | `Ars` oder `Lehrschrift` | `Grammatik` |
| erklärende Texte über Liturgie | `Fachtext` | `Liturgik`, `Messerklärung` oder `Traktat` | `Liturgie` |

### Abgrenzung

`Fachtext` soll nicht alles aufnehmen. Eigene Großgattungen bleiben vorläufig insbesondere:

| Buchgattung | Grund |
| --- | --- |
| `Bibeltext` | biblischer Primärtext |
| `Bibelexegese` | Auslegung biblischer Texte |
| `Liturgisches Buch` | Gebrauchsbuch für den liturgischen Vollzug |
| `Homilien` | homiletische Textform |
| `Brief` | kommunikative Textform |
| `Dichtung` | poetische Form |
| `Hagiographie` | Heiligenleben, Passiones und verwandte Formen |
| `Kirchenrecht` | normative kirchliche Rechtstexte, soweit als eigene Gruppe beibehalten |

### Maxime

Die Zahl der Buchgattungen soll deutlich reduziert werden. Fachadjektive wie `medizinisch`, `arithmetisch`, `grammatisch`, `liturgisch` oder `theologisch` gehören grundsätzlich nicht in die Buchgattung. Die Buchgattung beschreibt die breite Textform; die nähere Textform steht in `Sub-Gattung`; das Fachgebiet steht in `Thema`.

## Normierungsentscheidung v10: `Liturgisches Buch` und `Liturgik`

Diese Entscheidung ist für die klaren liturgischen Gebrauchsbücher in `v6-3` materialisiert. Die frühere Lehrschrift-Regel aus v6 wird durch den Zwischenstand v8 zu `Fachtext` ersetzt; die Unterscheidung zwischen `Liturgisches Buch` und `Liturgik` bleibt bestehen.

1. `Liturgisches Buch` bleibt eine Buchgattung, aber nur für Bücher bzw. Textbestände, die primär dem Vollzug der Liturgie dienen, also liturgische Gebrauchsbücher, Formulare, Gebete, Ordnungen oder Riten enthalten. Spezialformen wie Sakramentar, Messbuch/Missale, Pontifikale, Benedictionale und Ordo werden nicht als eigene Buchgattungen geführt, sondern als `Sub-Gattung` unter `Liturgisches Buch`.
2. `Liturgik` wird nicht mit `Liturgisches Buch` gleichgesetzt. `Liturgik` bezeichnet erklärende, systematische oder lehrhafte Texte über Liturgie. Als Buchgattung soll `Liturgik` daher möglichst nicht fortgeführt werden.
3. Für erklärende Texte über Liturgie gilt nach dem Zwischenstand v8 eher: `Buchgattung = Fachtext`, `Sub-Gattung = Liturgik`, `Messerklärung` oder `Traktat`, `Thema = Liturgie`.
4. `Lehrschrift` wird nicht mehr als breite Hauptgattung empfohlen, sondern als mögliche `Sub-Gattung` unter `Fachtext` geführt.
5. `Theologie` wird nicht als eigene Buchgattung eingeführt. Theologische Inhalte werden über `Sub-Gattung`, `Thema` und gegebenenfalls `Überlieferungslinie` erfasst.

Beispiele:

| Texttyp | Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- | --- |
| Boethius, *De institutione arithmetica* | `Fachtext` | `Lehrschrift` | `Arithmetik` |
| erklärender Text über liturgische Vollzüge | `Fachtext` | `Liturgik` | `Liturgie` |
| Messerklärung | `Fachtext` | `Messerklärung` | `Liturgie / Messe` |
| eucharistietheologischer Text | `Fachtext` | `Traktat` oder `Lehrschrift` | `Eucharistie` |
| liturgisches Gebrauchsbuch | `Liturgisches Buch` | `Sakramentar`, `Messbuch`, `Pontifikale`, `Benedictionale`, `Ordo` | `Liturgie` |

## Grundregeln für die vier Normfelder

1. **Buchgattung** bezeichnet die formale Text- oder Buchart: z. B. Evangelienbuch, Bibelkommentar, Glossar, Traktat, Chronik.
2. **Werktyp** bezeichnet den Überlieferungsstatus oder die Funktion im Codex: z. B. Originalwerk, Übersetzung, Exzerpt, Fragment, Nachtrag, Redaktion, Kompilation.
3. **Thema** bezeichnet den inhaltlichen Schwerpunkt: z. B. Exegese, Liturgie, Medizin, Grammatik, Philosophie / Logik.
4. **Überlieferungslinie** bezeichnet den literarisch-historischen Traditionszusammenhang: z. B. Lateinische Patristik, Spätantike Gelehrsamkeit, Karolingische Gelehrsamkeit, Biblische Glossentradition.
5. Doppelbegriffe mit ` / ` sollen nur stehen bleiben, wenn beide Komponenten für die Auswertung wirklich gleichrangig sind. Andernfalls sollte eine Komponente in `Werktyp`, `Thema` oder `Bemerkungen` verschoben werden.
6. Provenienz oder Schriftheimat gehören nicht in die Überlieferungslinie. Ein spezifischer Lorscher Traditionszusammenhang kann aber als `Lorscher Überlieferung` erfasst werden.

## Priorisierte Homogenisierungsvorschläge

- `Bibel` und `Biblische Überlieferung` trennscharf verwenden: `Bibel` als Thema für den Textbestand, `Biblische Überlieferung` als Traditionslinie bzw. Buchkontext.
- Für biblische Auslegung gilt künftig: `Bibelexegese` statt `Bibelauslegung`; `Bibelglossen` und `Bibelkommentar` ohne Untergattungen oder Slash-Mischformen verwenden.
- Biblische Primärtexte künftig zweistufig erfassen: `Bibeltext` als Hauptgattung; `Evangelienbuch`, `Perikopenbuch`, `Evangelistar`, `Bibel mit Glosse` usw. als `Sub-Gattung` bzw. Gebrauchsform. `Einzelbuch` und `Teilbibel` werden nicht als Sub-Gattungen eingeführt; bei normalen biblischen Texten bleibt `Sub-Gattung` leer. Diese Schemaänderung ist in `v6-1` materialisiert.
- `Liturgisches Buch` und `Liturgik` trennen: `Liturgisches Buch` bezeichnet liturgische Gebrauchsbücher; konkrete Formen wie `Sakramentar`, `Messbuch`, `Pontifikale`, `Benedictionale` und `Ordo` stehen in `Sub-Gattung`. `Liturgik` bezeichnet erklärende/lehrhafte Texte über Liturgie und erscheint als `Sub-Gattung` unter `Fachtext`.
- `Fachtext` als vorläufige breite Hauptgattung für fachbezogene Sachtexte verwenden; `Lehrschrift`, `Handbuch`, `Rezeptsammlung`, `Traktat`, `Ars`, `Messerklärung` usw. werden Sub-Gattungen, das Fachgebiet steht im `Thema`.
- Reihenfolge in kombinierten Werktypen vereinheitlichen: bevorzugt `Kompilation / Glossierung` statt wechselnd `Glossierung / Kompilation`; bevorzugt `Nachtrag / Fragment` statt wechselnd `Fragment / Nachtrag`.
- `Fragment` möglichst nicht als Buchgattung verwenden, wenn die Sachgattung bestimmbar ist; Fragmentarität gehört primär in `Werktyp`.
- `Traktat`-Spezifizierungen wie `Dogmatischer Traktat`, `Theologischer Traktat`, `Polemischer Traktat` können bei Bedarf auf `Traktat` vereinheitlicht werden; die Spezialisierung steht dann im Thema.
- Semikolon-Doppellinien vermeiden, besonders `Biblische Glossentradition; Karolingische Gelehrsamkeit`; besser eine Hauptlinie wählen und den zweiten Kontext in die Bemerkungen setzen.
- `verschieden`, `unsicher`, `Werk unbestimmt` und Fragezeichen-Kategorien bleiben nur Arbeitsmarker und sollten in späteren Erschließungsrunden gezielt reduziert werden.


## Normierungsentscheidung v2: biblische Buchgattungen

1. `Bibelexegese` ist der bevorzugte Oberbegriff für allgemeine Auslegung biblischer Texte. Der bisherige Begriff `Bibelauslegung` soll nicht weitergeführt werden.
2. `Bibelglossen` und `Bibelkommentar` bleiben als zwei getrennte, einfache Buchgattungen erhalten. Es werden keine Untergattungen oder Mischformen wie `Bibelglossen / Kommentar`, `Bibelglossen / liturgisch-theologischer Exzerpt`, `Bibelkommentar / Homilien` oder `Bibelkommentar / Predigten` als Normbegriffe geführt.
3. Die Entscheidung zwischen `Bibelglossen` und `Bibelkommentar` richtet sich nach der dominierenden Form: stellenweise Wort- und Sacherläuterungen = `Bibelglossen`; fortlaufende oder abschnittsweise Auslegung = `Bibelkommentar`.
4. Homilien oder Predigten mit biblischem Bezug werden als `Homilien` oder `Predigten` geführt; `Homiliensammlung` wird nicht als eigener Normbegriff fortgeführt. Wenn die exegetische Form im Vordergrund steht, kann stattdessen `Bibelexegese` gewählt werden.
5. Sonderbestandteile wie liturgische Exzerpte, homiletischer Charakter oder eingestreute Einzeltraktate gehören in `Werktyp`, `Thema` oder `Bemerkungen`, nicht in die Buchgattung.


## Normierungsentscheidung v3: `Bibel mit Glosse`

`Bibel mit Glosse` bleibt als eigener Normbegriff erhalten. Er bezeichnet einen biblischen Grundtext mit beigegebener Glosse und ist deshalb nicht ohne Weiteres durch `Bibeltext` zu ersetzen. Der Begriff wird nur verwendet, wenn der biblische Textbestand selbst mit Glosse überliefert ist. Reine Glossenbestände ohne fortlaufenden biblischen Grundtext werden dagegen als `Bibelglossen` geführt.

Diese Entscheidung betrifft zunächst nur das Handbuch und das Änderungsprotokoll. Die Forschungstabelle wird erst in einem späteren, gebündelten Redaktionsschritt angepasst.

## Normierungsentscheidung v4/v5: Sub-Gattung für biblische Textbestände

Die bisherigen Werte `Bibeltext`, `Bibel mit Glosse`, `Evangelienbuch`, `Perikopenbuch` und `Evangelistar` bezeichnen nicht gleichartige Buchgattungen, sondern biblische Textbestände in unterschiedlichen Gebrauchsformen. Deshalb wird für biblische Primärtexte ein zweistufiges Modell verwendet:

| Ebene | Normwert / Funktion | Erläuterung |
| --- | --- | --- |
| Buchgattung | `Bibeltext` | Oberbegriff für biblische Primärtexte, unabhängig davon, ob sie fortlaufend, liturgisch geordnet oder glossiert überliefert sind. |
| Sub-Gattung | *(leer)* | Normalfall für biblischen Grundtext; der genaue Umfang steht in `Text` und `Werk`. |
| Sub-Gattung | `Evangelienbuch` | Fortlaufender Text der vier Evangelien oder eines klar als Evangelienbuch geführten Evangelienbestands. |
| Sub-Gattung | `Perikopenbuch` | Liturgisch geordnete Auswahl biblischer Lesungen für Gottesdienst und Kirchenjahr, sofern nicht genauer als Evangelistar bestimmbar. |
| Sub-Gattung | `Evangelistar` | Spezialisierter Fall mit Evangelienperikopen. Der Begriff bleibt erhalten, weil er eine präzisere Gebrauchsform bezeichnet. |
| Sub-Gattung | `Bibel mit Glosse` | Biblischer Grundtext mit beigegebener Glosse; nicht mit reinen `Bibelglossen` verwechseln. |

`Einzelbuch` und `Teilbibel` werden nicht als Sub-Gattungen eingeführt. Bei normalen biblischen Texten bleibt `Sub-Gattung` leer; der konkrete Umfang wird über `Text` und `Werk` erfasst.

`Evangelistar` und `Perikopenbuch` sind liturgisch gebrauchte Bibeltexte. Sie stehen deshalb unter `Bibeltext`; die liturgische Funktion wird zusätzlich über `Thema = Liturgie` sichtbar. `Liturgisches Buch` bleibt enger reserviert für liturgische Formulare, Gebete, Ordnungen und Riten, nicht für primär biblische Lesetexte.

Diese Entscheidung ist für die klaren biblischen Primärtexte in `v6-1` materialisiert. Reine Auslegungstexte ohne fortlaufenden biblischen Grundtext gehören nicht unter `Bibeltext`, sondern unter `Bibelexegese` mit Sub-Gattungen wie `Bibelkommentar`, `Bibelglossen` oder ggf. `Quaestionen`.


## Normierungsentscheidung v7: `Homilien` und `Homiliensammlung`

`Homiliensammlung` wird nicht als eigener Normbegriff fortgeführt. Für einzelne Homilien ebenso wie für Sammlungen von Homilien genügt vorläufig die Buchgattung `Homilien`. Die Unterscheidung zwischen Einzeltext, Sammlung, autorbezogener Sammlung oder gemischter Sammlung ist für die gegenwärtige Auswertung zu fein und kann, falls nötig, in `Werk`, `Werktyp` oder `Bemerkungen` erscheinen.

Ein gesonderter Begriff `Homiliar` wird vorerst nicht als Standard-Sub-Gattung eingeführt. Er bleibt höchstens ein später zu prüfender Sonderfall für ausdrücklich liturgisch geordnete und liturgisch gebrauchte Homilienbücher. Solange ein solcher Gebrauch nicht sicher aus dem Eintrag hervorgeht, wird nicht von `Homiliar` gesprochen.

Arbeitsregel:

| bisheriger Wert | künftiger Normwert | Bemerkung |
| --- | --- | --- |
| `Homiliensammlung` | `Homilien` | Sammlung nicht als eigene Buchgattung ausdifferenzieren. |
| `Homilie` | `Homilien` | Singularform zugunsten des stabilen Normwerts vermeiden. |
| `Homilien` | `Homilien` | Normwert für einzelne und gesammelte Homilien. |
| `Homiliar` | noch kein Standardwert | Nur bei sicher liturgisch geordnetem Gebrauchsbuch später erneut prüfen. |

## Buchgattungen

| Begriff | Häufigkeit | Arbeitsdefinition | Homogenisierungsvorschlag |
| --- | ---: | --- | --- |
| Annalen | 2 | Chronologische, jahrweise angelegte Aufzeichnung historischer Ereignisse. | Beibehalten. |
| Anthologie | 1 | Auswahl mehrerer Texte, Gedichte oder Exzerpte, die als Sammlung überliefert sind. | Beibehalten. |
| Autobiographie | 1 | Selbstdeutung oder Lebensbericht in der Ich-Perspektive; in der Tabelle v. a. für Augustinus’ Confessiones. | Beibehalten. |
| Bibel mit Glosse | 2 | Biblischer Grundtext mit beigegebenen Wort- oder Sachglossen. | Beibehalten. |
| Bibelauslegung | 2 | Nicht mehr bevorzugter Arbeitsbegriff für exegetische Texte zu biblischen Stoffen. | Durch `Bibelexegese` ersetzen. |
| Bibelbezogene Quaestionen | 1 | Frage-Antwort- oder Problemexegese zu biblischen Stoffen. | Möglichst zu `Bibelexegese` ziehen; die Frage-Antwort-Form ggf. im Werktyp oder in den Bemerkungen erfassen. |
| Bibelexegese | 1 | Bevorzugter Oberbegriff für Auslegung biblischer Texte, sofern die Form nicht eindeutig als `Bibelglossen`, `Bibelkommentar`, `Homilie` oder `Homilien` bestimmt werden soll. | Als Normbegriff für allgemeine biblische Auslegung verwenden; ersetzt `Bibelauslegung`. |
| Bibelglossen | 2 | Stellenbezogene, meist kurze Wort- und Sacherläuterungen zu Bibeltexten, Prologen oder biblischen Namen. | Als einfacher Normbegriff beibehalten; keine Untergattungen bilden. |
| Bibelglossen / Kommentar | 1 | Nicht normgerechte Mischform zwischen kurzen Bibelglossen und fortlaufender Kommentierung. | Nach dominierender Form durch `Bibelglossen` oder `Bibelkommentar` ersetzen. |
| Bibelglossen / liturgisch-theologischer Exzerpt | 1 | Nicht normgerechte Mischform: Bibelglossenbestand mit eingelagertem liturgisch-theologischem Exzerpt. | Durch `Bibelglossen` ersetzen; den Exzerptcharakter in Werktyp oder Bemerkungen erfassen. |
| Bibelkommentar | 31 | Fortlaufende oder abschnittsweise Auslegung eines biblischen Buches. | Als einfacher Normbegriff beibehalten; keine Untergattungen bilden. |
| Bibelkommentar / Homilien | 1 | Nicht normgerechte Mischform: biblische Auslegung in homiletischer Form oder mit Predigtcharakter. | Nach dominierender Form durch `Bibelkommentar` oder `Homilien` ersetzen. |
| Bibelkommentar / Predigten | 2 | Nicht normgerechte Mischform: biblische Auslegung mit Predigtcharakter. | Nach dominierender Form durch `Bibelkommentar`, `Predigten` oder `Homilien` ersetzen; keine Untergattung des Bibelkommentars bilden. |
| Bibeltext | 13 | Text eines biblischen Buches oder einer größeren biblischen Texteinheit. | Beibehalten. |
| Bibliothekskatalog | 1 | Verzeichnis von Büchern oder Handschriften einer Bibliothek. | Beibehalten. |
| Biblisches Epos | 1 | Dichtung, die biblischen Stoff episch gestaltet. | Beibehalten. |
| Biographie | 2 | Lebensbeschreibung einer historischen Person. | Beibehalten. |
| Biographiensammlung | 1 | Sammlung mehrerer Lebensbeschreibungen. | Beibehalten. |
| Brief | 7 | Einzelbrief oder epistolarischer Einzeltext. | Beibehalten. |
| Briefsammlung | 13 | Sammlung mehrerer Briefe eines Autors oder einer Briefgruppe. | Beibehalten. |
| Bußbuch | 1 | Kirchenrechtlich-pastorale Sammlung von Bußbestimmungen. | Beibehalten. |
| Bücherverzeichnis | 4 | Liste von Büchern, Beständen oder Schenkungen; enger und neutraler als Bibliothekskatalog. | Beibehalten. |
| Chronik | 6 | Zeitlich geordnete Darstellung historischer Ereignisse, meist knapper als ein Geschichtswerk. | Beibehalten. |
| Chronographie / Computus? | 1 | Unsichere Mischbestimmung zwischen Zeitrechnung und chronographischer Darstellung. | Fragezeichen auflösen: nach Prüfung entweder „Chronik/Chronographie“ oder „Computistische Sammlung“. |
| Chronographisch-enzyklopädische Schrift | 1 | Text, der Weltalter-, Zeitrechnungs- oder Geschichtswissen enzyklopädisch ordnet. | Beibehalten. |
| Computistische Sammlung | 1 | Sammlung von Texten oder Tabellen zur Zeitrechnung, insbesondere Osterrechnung. | Beibehalten. |
| Dialog | 2 | Text in Gesprächsform. | Beibehalten. |
| Dialog / Enzyklopädisches Werk | 1 | Dialogische oder dialogähnliche Wissensdarstellung mit enzyklopädischem Anspruch. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Dialog / Hagiographie | 2 | Dialogische hagiographische Erzählung, besonders für Gregors Dialogi. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Dichtung | 13 | Versdichtung ohne engere Spezialisierung. | Beibehalten. |
| Dichtung / Schreiberverse | 1 | Versförmiger Beitext, der auf Schreiber, Schreibakt oder Buchproduktion Bezug nimmt. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Dichtung / Spottgedicht | 1 | Gelegenheitsgedicht mit satirischem oder spöttischem Charakter. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Dogmatischer Traktat | 2 | Lehrhafte theologische Abhandlung zu Glaubenslehre oder Dogma. | Optional auf „Traktat“ vereinheitlichen und die inhaltliche Spezialisierung im Thema abbilden. |
| Drama | 1 | Bühnendichtung oder dramatische Literatur. | Beibehalten. |
| Einleitung | 1 | Prooemium, Prolog oder systematische Einführung zu einem Werk oder Textcorpus. | Beibehalten. |
| Enzyklopädie | 7 | Systematische Sammlung von Wissen über mehrere Wissensgebiete. | Beibehalten. |
| Enzyklopädie / Lehrgedicht | 2 | Enzyklopädischer Text mit dichterischer oder prosimetrischer Form. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Enzyklopädie / Naturkunde | 1 | Enzyklopädischer Wissensbestand mit naturkundlichem Schwerpunkt. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Epos | 2 | Längere erzählende Dichtung in gehobener Form. | Beibehalten. |
| Eucharistischer Traktat | 1 | Theologische Abhandlung über Eucharistie, Messopfer oder Altarsakrament. | Optional auf „Traktat“ vereinheitlichen und die inhaltliche Spezialisierung im Thema abbilden. |
| Evangelienbuch | 14 | Handschrift oder Textbestand mit den vier Evangelien. | Beibehalten. |
| Evangelistar | 1 | Perikopenbuch mit Evangelienlesungen für den Gottesdienst. | Mit „Perikopenbuch“ harmonisieren; „Evangelistar“ ggf. im Werkfeld belassen. |
| Florilegium | 1 | Auswahl von Exzerpten aus verschiedenen Autoren oder Werken. | Beibehalten. |
| Florilegium / Exzerptwerk | 1 | Exzerptsammlung mit florilegischem Charakter. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Fragment | 1 | Unvollständig erhaltener Textbestand, dessen Gattung nicht genauer bestimmt ist. | Nicht als Buchgattung verwenden, wenn die Sachgattung bestimmbar ist; Fragment besser im Werktyp. |
| Genealogie | 1 | Abstammungs- oder Verwandtschaftsdarstellung, meist in Listen- oder Tabellenform. | Beibehalten. |
| Geographie / Naturkunde | 1 | Text zu räumlicher Weltbeschreibung und naturkundlichen Gegenständen. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Geschichtswerk | 17 | Darstellung historischer Ereignisse mit narrativem oder systematischem Anspruch. | Beibehalten. |
| Glossar | 2 | Alphabetisches oder sachlich geordnetes Worterklärungsverzeichnis. | Beibehalten. |
| Glossar / Enzyklopädie | 1 | Worterklärungsverzeichnis mit enzyklopädischem Sachwissen. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Glossar / Enzyklopädische Sammlung | 1 | Glossarischer Sammeltext mit enzyklopädischem Charakter. | Mit „Glossar / Enzyklopädie“ vereinheitlichen. |
| Glossen | 3 | Kurze Wort-, Sach- oder Stellenkommentare zu einem Text oder Themenbestand. | Beibehalten. |
| Grammatik | 11 | Lehrtext zur Sprachlehre, Formenlehre, Syntax oder grammatischen Terminologie. | Beibehalten. |
| Grammatik / Rhetorik | 1 | Textbestand, der grammatische und rhetorische Kategorien verbindet. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Hagiographie | 5 | Literatur über Heilige, Wunder, Reliquien oder heilige Lebensführung. | Beibehalten. |
| Hagiographie / Vita | 1 | Vita eines Heiligen oder einer heiligen Person. | Mit „Vita“ vereinheitlichen, wenn es sich um eine einzelne Lebensbeschreibung handelt. |
| Hagiographische Sammlung | 2 | Sammlung mehrerer hagiographischer Texte. | Beibehalten. |
| Homilie | 1 | Einzelne Predigt oder Auslegungspredigt. | Beibehalten. |
| Homilien | 11 | Predigten oder Homilien, einzeln oder gesammelt; keine eigene Trennung zwischen Einzelhomilie und Homiliensammlung. | Normwert. `Homiliensammlung` und `Homilie` hierher ziehen. |
| Homilien / Bibelauslegung | 1 | Nicht normgerechte Mischform: predigtförmige Auslegung biblischer Texte. | Nach dominierender Form durch `Homilien` oder `Bibelexegese` ersetzen. |
| Homiliensammlung | 3 | Sammlung von Homilien verschiedener oder eines Autors. | Durch `Homilien` ersetzen; Sammlungseigenschaft bei Bedarf in Werktyp oder Bemerkungen erfassen. |
| Inschriftensammlung | 1 | Sammlung von Inschriften oder inschriftlichen Texten. | Beibehalten. |
| Kalender | 2 | Kalendarischer Text, oft mit Heiligenfesten, Monatsdaten und computistischen Zusätzen. | Beibehalten. |
| Kanonessammlung | 2 | Sammlung kirchlicher Normen, Konzilsbeschlüsse oder kanonischer Rechtssätze. | Beibehalten. |
| Kanonistische Sammlung | 3 | Sammlung kirchenrechtlicher Materialien. | Beibehalten. |
| Kanonistische Sentenzen | 1 | Kurzsätze oder Autoritätenauszüge mit kirchenrechtlicher Funktion. | Beibehalten. |
| Kirchengeschichte | 3 | Geschichtswerk über Entstehung, Entwicklung oder Konflikte der Kirche. | Beibehalten. |
| Kirchenrecht | 6 | Rechtstext oder Rechtskompilation mit kirchlichem Normbestand. | Beibehalten. |
| Klagevers | 1 | Knapper vers- oder satzförmiger Klage- oder Memorialtext. | Beibehalten. |
| Kommentar | 18 | Auslegung oder Erläuterung eines Ausgangstextes. | Beibehalten. |
| Kommentar / Exzerpt? | 2 | Unsichere Bezeichnung für einen kommentierenden oder exzerpierenden Textbestand. | Kommentar als Buchgattung setzen; Exzerpt/Unsicherheit im Werktyp oder in Bemerkungen. |
| Kommentar / Glossenapparat | 1 | Kommentarbestand in Form von Interlinear- und Marginalglossen. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Konzilsakten | 1 | Überlieferung von Beschlüssen, Akten oder Dokumenten eines Konzils. | Beibehalten. |
| Kosmographie | 1 | Weltbeschreibung mit geographischen, ethnographischen oder kosmologischen Anteilen. | Beibehalten. |
| Lehrbuch | 1 | Didaktisch geordneter Text zur Einführung in ein Wissensgebiet. | Beibehalten. |
| Lehrgedicht | 1 | Didaktische Dichtung, die Wissen in Versform vermittelt. | Beibehalten. |
| Lehrnotiz | 1 | Kurzer didaktischer Text oder Merkstück. | Beibehalten. |
| Lehrschema | 1 | Schematische oder tabellarische Wissensordnung. | Beibehalten. |
| Lehrschrift | 10 | Didaktische Abhandlung zu einem Fachgebiet; bezeichnet die didaktische Form, nicht das Fach. | Beibehalten, aber fachlich über `Sub-Gattung` differenzieren, z. B. `Arithmetik`, `Computus`, `Liturgik`, `Theologische Lehrschrift`. |
| Lexikon / Auslegungshilfe | 1 | Hilfsmittel zur Erklärung von Namen, Begriffen oder biblischen Wörtern. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Liste | 1 | Listenförmiger Text ohne ausgeprägte narrative Struktur. | Beibehalten. |
| Literaturgeschichtlicher Katalog | 1 | Katalogartige Darstellung von Autoren oder Schriften. | Beibehalten. |
| Liturgik | 2 | Lehr- oder Erklärungstext zu Gottesdienst, Ritus und kirchlicher Ordnung. | Nicht als Buchgattung fortführen; je nach Form `Lehrschrift` oder `Traktat`, dazu `Sub-Gattung = Liturgik` und `Thema = Liturgie`. |
| Liturgische Notiz | 1 | Kurze Notiz mit liturgischem Inhalt oder liturgischer Deutung. | Beibehalten. |
| Liturgische Ordnung | 1 | Ordnungstext, der Ablauf oder Struktur eines liturgischen Vollzugs regelt. | Zu `Liturgisches Buch` mit `Sub-Gattung = Ordo` normieren; in `v6-3` für `Ordo Romanus` materialisiert. |
| Liturgischer Text | 1 | Einzelner liturgischer Gebrauchstext, der nicht als eigenes liturgisches Buch bestimmt ist. | Beibehalten. |
| Liturgisches Buch | 12 | Liturgisches Gebrauchsbuch für Vollzug, Formulare, Gebete, Ordnungen oder Riten. | Als Buchgattung beibehalten, aber nicht für erklärende Texte über Liturgie verwenden; Spezialformen ggf. später als `Sub-Gattung` erfassen. |
| Martyrologium | 3 | Verzeichnis von Märtyrern und Heiligen nach Kalendertagen. | Als spezifische liturgische Buchgattung beibehalten; nicht auf „Liturgisches Buch“ zurückverallgemeinern. |
| Medizinisches Handbuch | 11 | Sammlung oder Lehrtext medizinischer Rezepte, Diagnosen oder Behandlungsanweisungen. | Beibehalten. |
| Messbuch | 2 | Buch für die Messliturgie. | Zu `Liturgisches Buch` mit `Sub-Gattung = Messbuch` normieren; in `v6-3` materialisiert. |
| Messerklärung | 1 | Auslegung des Messritus und seiner Zeichen. | Eher als `Sub-Gattung` unter `Lehrschrift` oder `Traktat` führen; `Thema = Liturgie / Messe`. |
| Mirakelbuch | 1 | Sammlung von Wundererzählungen. | Beibehalten. |
| Musiktheoretischer / liturgischer Text | 2 | Textbestand an der Grenze von Musiktheorie und liturgischem Gebrauch. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Mythographische Schrift | 1 | Darstellung und Deutung paganer Mythen. | Beibehalten. |
| Mönchsliteratur | 5 | Texte zur monastischen Lebensform, Askese oder geistlichen Übung. | Beibehalten. |
| Naturkundliche Schrift | 1 | Text über Naturphänomene, Kosmos, Tiere, Pflanzen oder physische Welt. | Beibehalten. |
| Nekrolog | 1 | Memorialverzeichnis Verstorbener, meist für liturgisches Gedenken. | Beibehalten. |
| Papstchronik | 1 | Chronikartige Darstellung der Päpste und ihrer Amtszeiten. | Beibehalten. |
| Perikopenbuch | 4 | Liturgisches Lesungsbuch mit ausgewählten biblischen Perikopen. | Als spezifische liturgische Buchgattung beibehalten; nicht auf „Liturgisches Buch“ zurückverallgemeinern. |
| Philosophischer Dialog | 2 | Philosophischer Text in Dialogform. | Beibehalten. |
| Philosophischer Dialog / Prosimetrum | 1 | Philosophischer Text, der dialogische Prosa und metrische Partien verbindet. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Philosophischer Text | 1 | Allgemeine Bezeichnung für philosophischen Einzeltext. | Beibehalten. |
| Philosophischer Traktat | 3 | Lehrhafte philosophische Abhandlung. | Beibehalten. |
| Polemischer Traktat | 1 | Argumentative Abhandlung gegen eine Lehre, Person oder Gruppe. | Optional auf „Traktat“ vereinheitlichen und die inhaltliche Spezialisierung im Thema abbilden. |
| Pontifikale | 1 | Liturgisches Buch für bischöfliche Amtshandlungen. | Zu `Liturgisches Buch` mit `Sub-Gattung = Pontifikale` normieren; in `v6-3` materialisiert. |
| Predigt | 1 | Einzelne homiletische Rede. | Beibehalten. |
| Predigten | 3 | Mehrere homiletische Reden. | Beibehalten. |
| Psalmenkommentar | 2 | Auslegung der Psalmen oder eines Psalmenabschnitts. | Beibehalten. |
| Rechtstext | 2 | Normativer weltlicher oder kirchlicher Rechtstext. | Beibehalten. |
| Regel | 1 | Normativer Text zur Ordnung einer geistlichen Gemeinschaft. | Beibehalten. |
| Rhetorik | 1 | Lehrtext zur Redekunst. | Beibehalten. |
| Rhetoriklehrbuch | 1 | Didaktischer Rhetoriktext. | Beibehalten. |
| Rätseldichtung | 1 | Dichtung in Form von Rätseln. | Beibehalten. |
| Sakramentar | 2 | Liturgisches Buch mit priesterlichen Gebeten der Messe und anderer Feiern. | Zu `Liturgisches Buch` mit `Sub-Gattung = Sakramentar` normieren; in `v6-3` materialisiert. |
| Sammelhandschrift | 7 | Codex oder Eintrag mit mehreren, noch nicht einzeln erschlossenen Texten. | Nur als Platzhalter behalten, bis Einzeltexte erschlossen sind. |
| Sammlung | 2 | Allgemeiner Sammelbegriff für mehrere zusammengehörige Texte oder Exzerpte. | Wenn möglich präzisieren: Anthologie, Florilegium, Homilien, Kanonessammlung usw. |
| Satire | 1 | Literarischer Text mit satirischem Charakter. | Beibehalten. |
| Sequenz | 1 | Liturgische Dichtung, besonders im Messproprium. | Beibehalten. |
| Sequenzen | 1 | Mehrere liturgische Sequenzen oder Sequenzsammlung. | Für Sammlungen besser „Sequenzensammlung“ einführen; für Einzeltexte „Sequenz“. |
| Theologischer Traktat | 1 | Lehrhafte theologische Abhandlung. | Optional auf „Traktat“ vereinheitlichen und die inhaltliche Spezialisierung im Thema abbilden. |
| Traktat | 33 | Lehrhafte Abhandlung zu einem abgegrenzten Thema. | Beibehalten. |
| Traktat / Bibelauslegung | 2 | Nicht normgerechte Mischform: Traktat mit exegetischer Funktion oder biblischer Auslegung. | Nach Schwerpunkt durch `Traktat` oder `Bibelexegese` ersetzen; bei fortlaufender Auslegung ggf. `Bibelkommentar`. |
| Traktat / Dialog | 1 | Abhandlung in dialogischer Form. | Besser „Traktat“ oder „Dialog“ nach dominanter Form. |
| Urkunde / Testament | 1 | Rechtsförmiger Text mit testamentarischem oder urkundlichem Charakter. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Urkundenbuch | 1 | Sammlung oder Kopialbuch von Urkunden. | Beibehalten. |
| Vergilkommentar / Allegorese | 1 | Auslegung Vergils mit allegorischer Deutung. | Nur behalten, wenn beide Komponenten gleichrangig sind; sonst auf den dominanten Gattungsbegriff normieren. |
| Vita | 2 | Lebensbeschreibung, meist hagiographisch. | Beibehalten. |
| Vita / Autorenbiographie | 1 | Biographischer Beitext zu einem Autor. | Für Autorenbeitexte beibehalten; nicht mit Heiligenvita vermischen. |

## Werktypen

| Begriff | Häufigkeit | Arbeitsdefinition | Homogenisierungsvorschlag |
| --- | ---: | --- | --- |
| Adaption | 1 | Bearbeitende Aneignung eines älteren Textes mit eigener Form oder Zielsetzung. | Beibehalten. |
| Anthologie | 7 | Auswahl mehrerer Texte oder Textauszüge, die als Sammlung angeordnet ist. | Beibehalten. |
| Bearbeitung | 2 | Textform mit erkennbarer Umformung, Kürzung, Erweiterung oder Anpassung einer Vorlage. | Beibehalten. |
| Beitext | 2 | Begleittext zu einem Hauptwerk, etwa Vita, Schreiberverse oder erläuternde Zusätze. | Beibehalten. |
| Beitext / Marginalglosse | 1 | Begleittext, der in marginaler oder glossenartiger Form überliefert ist. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Einschub / Originalwerk | 1 | Eigenständiger Text, der in einen größeren Überlieferungszusammenhang eingeschoben ist. | Beibehalten, wenn beide Informationen wichtig sind; alternativ „Einschub“ als eigenen Werktyp einführen. |
| Exzerpt | 8 | Auszug aus einem größeren Werk. | Beibehalten. |
| Exzerpt / Bearbeitung | 1 | Auszug, der zugleich umgestellt, gekürzt oder redaktionell bearbeitet ist. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Fragment | 5 | Unvollständig erhaltener Text. | Beibehalten. |
| Fragment / Ergänzung | 1 | Fragmentarischer oder ergänzender Textbestand in einem Codex. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Fragment / Nachtrag | 1 | Nachgetragener, zugleich unvollständiger Textbestand. | Reihenfolge mit „Nachtrag / Fragment“ vereinheitlichen. |
| Glossierung | 3 | Glossenapparat oder stellenbezogene Erläuterung zu einem Grundtext. | Beibehalten. |
| Glossierung / Kompilation | 4 | Glossarischer Bestand, der aus mehreren Quellen zusammengestellt ist. | Reihenfolge mit „Kompilation / Glossierung“ vereinheitlichen. |
| Glossierung / Nachtrag | 1 | Nachträglich eingetragener Glossenbestand. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Kommentar / Glossierung | 1 | Kommentierende Auslegung in Form von Interlinear- oder Marginalglossen. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Kompilation | 33 | Zusammenstellung mehrerer Vorlagen oder Textteile zu einem neuen Bestand. | Beibehalten. |
| Kompilation / Glossierung | 3 | Kompilierter Glossen- oder Erklärungstext. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Kompilation / Nachtrag | 2 | Nachgetragene Zusammenstellung mehrerer Materialien. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Nachtrag | 5 | Später eingetragener Text gegenüber dem Hauptbestand der Handschrift. | Beibehalten. |
| Nachtrag / Fragment | 2 | Später eingetragener, unvollständig erhaltener Text. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Originalwerk | 226 | Eigenständiges Werk in überlieferter Form, nicht primär als Exzerpt, Nachtrag oder Übersetzung erfasst. | Beibehalten. |
| Originalwerk / Kommentar | 1 | Eigenständiger Kommentar als Werk eines Autors. | Beibehalten nur, wenn der Kommentar als eigenständiges Werk gemeint ist; sonst „Originalwerk“. |
| Redaktion | 40 | Textfassung, die durch Auswahl, Ordnung oder liturgische/kanonische Bearbeitung geprägt ist. | Beibehalten. |
| Redaktion / Kompilation | 1 | Redaktionell geordnete Zusammenstellung mehrerer Vorlagen. | Bei Endredaktion entscheiden, ob der Ordnungsakt („Redaktion“) oder die Quellenmischung („Kompilation“) dominiert. |
| Sammlung | 1 | Mehrere Texte oder Einheiten, die als zusammengehöriger Bestand geführt werden. | Wenn möglich durch „Kompilation“ oder eine spezifischere Kategorie ersetzen. |
| Teilüberlieferung | 1 | Nur ein Teil eines größeren Werkes oder Corpus ist überliefert. | Beibehalten. |
| Teilüberlieferung / Glossierung | 1 | Teil eines größeren Werkes mit Glossenapparat. | Prüfen, ob eine Komponente in Buchgattung oder Bemerkungen verschoben werden kann. |
| Traktat / Nachtrag | 1 | Nachgetragener traktatförmiger Text. | Besser „Nachtrag“ als Werktyp; „Traktat“ gehört eher zur Buchgattung. |
| unsicher | 3 | Platzhalter, wenn die Werkfunktion noch nicht verlässlich bestimmt ist. | Nach Möglichkeit durch geprüften Werktyp ersetzen. |
| Volltext | 26 | Vollständige oder intendiert vollständige Überlieferung eines Textes bzw. Buches. | Beibehalten. |
| Übersetzung | 18 | Text in lateinischer Übersetzung aus einer anderen Sprache, meist Griechisch. | Beibehalten. |
| Übersetzung / editio composita | 1 | Zusammengesetzte lateinische Fassung aus Übersetzungstraditionen, etwa bei Aristoteles Latinus. | Besser „Übersetzung“ als Werktyp; „editio composita“ in Bemerkungen belassen. |

## Themata

| Begriff | Häufigkeit | Arbeitsdefinition | Homogenisierungsvorschlag |
| --- | ---: | --- | --- |
| Anthropologie / Morallehre | 1 | Lehre vom Menschen, seiner Seele, Tugenden oder moralischen Ordnung. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Arithmetik | 2 | Zahlenlehre als Teil des Quadriviums. | Beibehalten. |
| Artes liberales | 5 | Schulwissen der sieben freien Künste oder einzelner artes. | Beibehalten. |
| Artes liberales / Astronomie | 1 | Freie Künste mit besonderem astronomischem Schwerpunkt. | Bei eindeutig astronomischem Schwerpunkt „Astronomie“, sonst „Artes liberales“. |
| Askese / Jungfräulichkeit | 1 | Thema asketischer Lebensführung, besonders virginitas. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Asketik | 4 | Lehre und Praxis geistlicher Selbstdisziplin. | Beibehalten. |
| Astronomie | 2 | Kosmische Ordnung, Sternkunde und astronomische Modelle. | Beibehalten. |
| Autobiographie | 1 | Selbstdeutung und Lebensrückblick. | Beibehalten. |
| Bibel | 22 | Biblischer Textbestand als solcher. | Mit „Biblische Überlieferung“ abgleichen; möglichst trennscharf verwenden. |
| Bibliothekswesen | 6 | Bücherverzeichnisse, Bibliotheksordnung, Buchbestand oder Überlieferung von Katalogen. | Beibehalten. |
| Biblische Überlieferung | 5 | Überlieferung biblischer Texte, Lesungen oder Bibelcodices. | Mit „Bibel“ abgleichen: „Bibel“ für Textbestand, „Biblische Überlieferung“ für Überlieferungs-/Buchkontext verwenden. |
| Biographie | 1 | Lebensbeschreibung als Thema. | Beibehalten. |
| Briefliteratur | 13 | Epistolarische Kommunikation und Briefsammlungen. | Beibehalten. |
| Chronographie | 7 | Zeitordnung, Weltalter, Chroniken und historische Datierung. | Beibehalten. |
| Computus | 6 | Zeitrechnung, Kalenderberechnung und Osterrechnung. | Beibehalten. |
| Dialektik | 2 | Logik, Argumentationslehre und aristotelisch-boethianische Begriffslehre. | Beibehalten. |
| Dialektik / Rhetorik | 1 | Verbindung logischer und rhetorischer Topik oder Argumentationslehre. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Dichtung | 4 | Versliteratur als Gegenstandsbereich. | Beibehalten. |
| Dichtung / Buchkultur | 1 | Dichtung mit Bezug auf Schreiben, Schreiber oder Buchgebrauch. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Dichtung / Moral | 1 | Moralisch-didaktische Versliteratur. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Dogmatik | 7 | Glaubenslehre und kontroverstheologische Lehrfragen. | Beibehalten. |
| Enzyklopädie / Artes liberales | 1 | Enzyklopädische Ordnung schulischer Wissensgebiete. | Eventuell auf „Artes liberales“ vereinheitlichen; Enzyklopädie eher in Buchgattung. |
| Eschatologie | 1 | Lehre von den letzten Dingen, Endzeit oder Jenseitshoffnung. | Beibehalten. |
| Exegese | 75 | Auslegung biblischer oder theologischer Texte. | Beibehalten. |
| Exegese / Liturgie | 1 | Biblische oder theologische Auslegung mit liturgischem Schwerpunkt. | Nach Schwerpunkt auf „Exegese“ oder „Liturgie“ reduzieren. |
| Exzerptliteratur | 2 | Auswahl, Ordnung und Weitergabe von Textauszügen. | Beibehalten. |
| Geschichte | 30 | Historische Darstellung, Ereignisgeschichte und Geschichtsschreibung. | Beibehalten. |
| Grammatik | 12 | Sprachlehre, Worterklärung und grammatische Systematik. | Beibehalten. |
| Grammatik / Rhetorik | 1 | Übergangsbereich von Sprachlehre und Redekunst. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Hagiographie | 15 | Heiligenleben, Wunder, Reliquien und Heiligenverehrung. | Beibehalten. |
| Homiletik | 13 | Predigtwesen und homiletische Bibelauslegung. | Beibehalten. |
| Kanonistik | 1 | Systematische Beschäftigung mit kirchlichen Normen und Kanones. | Beibehalten. |
| Kirchenrecht | 14 | Kirchliches Recht und normative kirchliche Ordnung. | Beibehalten. |
| Klostergeschichte | 2 | Geschichte eines Klosters oder monastischer Institutionen. | Beibehalten. |
| Kosmologie | 1 | Lehre von Weltbau, Elementen und Ordnung des Kosmos. | Beibehalten. |
| Lexikographie | 2 | Worterklärung, Glossare und lexikalische Ordnung. | Beibehalten. |
| Literatur | 18 | Literarische Texte der klassischen oder mittelalterlichen Tradition. | Beibehalten. |
| Liturgie | 37 | Gottesdienst, Sakramente, Ritus und liturgische Bücher. | Beibehalten. |
| Liturgie / Dichtung | 1 | Liturgisch verwendete oder liturgisch geprägte Dichtung. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Liturgie / Eucharistie | 1 | Eucharistie und Messopfer als liturgisch-theologisches Thema. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Liturgie / Kirchenjahr | 1 | Liturgische Zeitordnung und Jahreskreis. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Medizin | 17 | Heilkunst, Arzneien, Diätetik und medizinisches Wissen. | Beibehalten. |
| Metrik | 2 | Verslehre und metrische Regeln. | Beibehalten. |
| Musik | 2 | Musiktheorie, Tonordnung oder liturgische Musikpraxis. | Beibehalten. |
| Mönchtum | 8 | Monastische Lebensform, Regeln, Askese und geistliche Praxis. | Beibehalten. |
| Naturkunde | 5 | Wissen über Natur, Pflanzen, Tiere, Elemente und Himmelserscheinungen. | Beibehalten. |
| Philosophie | 8 | Philosophische Lehre, Ethik, Logik oder Naturphilosophie. | Beibehalten. |
| Philosophie / Astronomie | 1 | Philosophisch-kosmologische Astronomie. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Philosophie / Exegese eines Schultextes | 1 | Auslegung eines philosophischen Schultextes. | Eventuell zu „Philosophie / Logik“ ziehen; Schultextstatus in Werktyp/Bemerkungen. |
| Philosophie / Logik | 2 | Logische Philosophie, Kategorienlehre und Kommentartradition. | Doppelkategorie nur behalten, wenn beide Themen für die Auswertung wichtig sind. |
| Recht | 2 | Weltliches oder allgemeines Recht. | Beibehalten. |
| Rhetorik | 2 | Redekunst, Stil- und Argumentationslehre. | Beibehalten. |
| Theologie | 26 | Lehre über Gott, Kirche, Glaubenspraxis oder christliche Wahrheit. | Beibehalten. |
| Urkundenwesen | 1 | Urkunden, Testamente und rechtlich-dokumentarische Schriftlichkeit. | Beibehalten. |
| verschieden | 4 | Platzhalter für thematisch nicht einheitlich erschlossene Sammelbestände. | Bei weiterer Erschließung durch konkretes Thema ersetzen. |
| Wissenschaftstheorie | 1 | Ordnung, Einteilung und Begründung von Wissensgebieten. | Beibehalten. |

## Überlieferungslinien

| Begriff | Häufigkeit | Arbeitsdefinition | Homogenisierungsvorschlag |
| --- | ---: | --- | --- |
| Angelsächsisch-karolingische Glossentradition | 1 | Glossarische oder exegetische Überlieferung mit angelsächsischer Herkunft und karolingischer Weiterverarbeitung. | Beibehalten. |
| Angelsächsische Gelehrsamkeit | 18 | Text- und Bildungstradition angelsächsischer Autoren oder Schulen, besonders Beda und Aldhelm. | Beibehalten. |
| Antike Naturphilosophie | 1 | Antike Erklärung von Natur, Körper, Kosmos und physischer Ordnung. | Mit „Antike Philosophie“ abgleichen; Speziallinie nur bei naturphilosophischem Schwerpunkt. |
| Antike Philosophie | 1 | Griechisch-römische philosophische Tradition, besonders Aristoteles und seine lateinische Rezeption. | Beibehalten. |
| Bibel | 5 | Primäre biblische Textüberlieferung. | Mit „Biblische Überlieferung“ abgleichen; als Linie besser „Biblische Überlieferung“ verwenden. |
| Biblische Glossentradition | 2 | Tradition der Bibelglossen, besonders frühmittelalterlicher Schul- und Auslegungsglossen. | Beibehalten. |
| Biblische Glossentradition; Karolingische Gelehrsamkeit | 1 | Gemischte Angabe für Bibelglossen, die zugleich in karolingischem Gelehrtenkontext stehen. | Keine Semikolon-Doppellinie: bevorzugt „Biblische Glossentradition“; karolingischen Kontext ggf. in Bemerkungen. |
| Biblische Überlieferung | 25 | Überlieferung biblischer Texte und biblisch-liturgischer Lesebestände. | Beibehalten. |
| Boethius-Überlieferung | 1 | Überlieferung von Boethius-Texten, Boethius-Viten, Kommentaren oder boethianischen Schulzusammenhängen. | Beibehalten. |
| Frühmittelalterliche Gelehrsamkeit | 9 | Gelehrte Textproduktion und Wissensordnung des Frühmittelalters. | Beibehalten. |
| Frühmittelalterliche Medizin | 10 | Medizinische Text- und Rezepttradition des Frühmittelalters. | Beibehalten. |
| Frühmittelalterliche Theologie | 1 | Theologische Textbildung des Frühmittelalters. | Eventuell zu „Frühmittelalterliche Gelehrsamkeit“ ziehen, falls keine eigene theologische Linie benötigt wird. |
| Griechische Patristik | 14 | Griechischsprachige Kirchenväter und ihre lateinische Übersetzung oder Rezeption. | Beibehalten. |
| Hellenistisch-jüdische Tradition | 2 | Jüdisch-hellenistische Texte und deren lateinische Überlieferung. | Beibehalten. |
| Hochmittelalter | 8 | Textproduktion oder Überlieferung des Hochmittelalters. | Beibehalten. |
| Humanismus | 1 | Humanistische Text- und Rezeptionskultur des Spätmittelalters/frühen Humanismus. | Beibehalten. |
| Karolingische Gelehrsamkeit | 66 | Gelehrte Textproduktion, Redaktion und Schultradition des karolingischen Umfelds. | Beibehalten. |
| Kirchenrechtliche Tradition | 7 | Normative kirchliche Rechtstradition, Kanones und Dekretalüberlieferung. | Beibehalten. |
| Klassische lateinische Literatur | 30 | Lateinische Literatur der römischen Antike und ihre mittelalterliche Überlieferung. | Beibehalten. |
| Lateinische Patristik | 114 | Lateinische Kirchenväter und spätantike christliche Autoren des Westens. | Beibehalten. |
| Liturgische Tradition | 28 | Überlieferung liturgischer Texte, Bücher, Kalender und Riten. | Beibehalten. |
| Lorscher Überlieferung | 1 | Text- oder Gebrauchszusammenhang, der spezifisch auf Lorsch verweist. | Nur verwenden, wenn der Textbestand selbst spezifisch Lorscher Traditionswert hat, nicht bloß Provenienz. |
| Mittelalterliche Gelegenheitsdichtung | 1 | Situationsbezogene mittelalterliche Dichtung ohne feste große Traditionslinie. | Eher Thema/Buchgattung als Überlieferungslinie; ggf. zu „Frühmittelalterliche Gelehrsamkeit“ oder „Hochmittelalter“. |
| Mittelalterliche Schreibkultur | 1 | Tradition von Schreibervermerken, Kolophonen und buchbezogenen Beitexten. | Als Speziallinie nur für Schreiberverse/Kolophone behalten. |
| Oribasianische Tradition | 2 | Lateinische Überlieferung des medizinischen Corpus um Oribasius. | Beibehalten. |
| Ottonische Gelehrsamkeit | 1 | Gelehrte Text- und Buchkultur des ottonischen Umfelds. | Beibehalten. |
| Sprachlogische Tradition | 1 | Logisch-grammatische oder sprachphilosophische Schultradition. | Beibehalten. |
| Spätantike Gelehrsamkeit | 49 | Nicht spezifisch patristische gelehrte Literatur der Spätantike, einschl. artes und Enzyklopädie. | Beibehalten. |
| Spätantike Medizin | 2 | Medizinische Literatur und Heilkundetradition der Spätantike. | Beibehalten. |
| St. Galler Sequenztradition | 1 | Liturgisch-poetische Sequenztradition im Umfeld St. Gallens. | Beibehalten. |

## Arbeitsnotiz für die nächste Handbuchfassung

Für `Handbuch_v2` wäre sinnvoll, die oben genannten Homogenisierungsvorschläge in echte Normlisten umzusetzen: eine kontrollierte Liste für jede der vier Spalten, dazu eine Migrationsliste „alter Wert → normierter Wert“. Die Forschungstabelle sollte erst danach verändert werden.

---

## Nachtrag zu v9: Materialisierung des Redaktionsblocks `Fachtext`, Homilien und biblische Auslegung

**Stand:** 2026-07-07  
**Bezugstabelle nach Umsetzung:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-2.md`

### 1. Neue Großgattung `Fachtext`

`Fachtext` ist die vorläufige Großgattung für gelehrte, erklärende, praktische und fachbezogene Sachtexte. Die nähere Textform wird in der Spalte `Sub-Gattung` erfasst; das Fachgebiet bleibt im Feld `Thema`.

Beispiele:

| Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- |
| `Fachtext` | `Handbuch` | `Medizin` |
| `Fachtext` | `Lehrschrift` | `Arithmetik`, `Computus`, `Metrik`, `Dialektik` usw. |
| `Fachtext` | `Traktat` | `Theologie`, `Dogmatik`, `Philosophie`, `Mönchtum` usw. |
| `Fachtext` | `Glossar` | `Lexikographie`, `Grammatik`, `Medizin` usw. |
| `Fachtext` | `Liturgik` | `Liturgie` |
| `Fachtext` | `Messerklärung` | `Liturgie` |

### 2. Liturgik und Messerklärung

`Liturgik` bezeichnet erklärende, systematische oder lehrhafte Texte über Liturgie und ist keine Buchgattung. In der Tabelle gilt daher:

| Fall | Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- | --- |
| allgemeiner erklärender Text über Liturgie | `Fachtext` | `Liturgik` | `Liturgie` |
| Text, der speziell die Messe erklärt | `Fachtext` | `Messerklärung` | `Liturgie` |

Eine Messerklärung gehört sachlich zur Liturgik, wird in der Spalte `Sub-Gattung` aber mit dem präziseren Begriff `Messerklärung` geführt.

### 3. Homilien

`Homiliensammlung` und `Homilie` werden nicht als eigene Normwerte fortgeführt. Für einzelne und gesammelte Homilien gilt vorläufig der Normwert `Homilien`. Ein eigener Wert `Homiliar` bleibt nur ein später zu prüfender Sonderfall für ausdrücklich liturgisch geordnete Gebrauchsbücher.

### 4. Biblische Auslegung

`Bibelauslegung` wird zu `Bibelexegese` normiert. Slash-Formen wie `Bibelglossen / Kommentar` oder `Bibelkommentar / Homilien` werden auf einen einfachen Normwert reduziert, je nach dominierender Form des jeweiligen Textes.

### 5. Noch nicht materialisierte Bereiche

Nicht in v6-2 generalisiert wurden u. a. grammatische, rhetorische, computistische, philosophische und liturgische Spezialgattungen, soweit sie noch keine besprochene eindeutige Zuordnung erhalten haben. Diese Bereiche bleiben für spätere Redaktionsblöcke offen.
