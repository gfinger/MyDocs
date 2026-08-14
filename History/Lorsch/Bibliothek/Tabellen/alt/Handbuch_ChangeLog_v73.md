# Änderungsprotokoll zum Handbuch der Lorsch-Forschungstabelle

**Version:** ChangeLog_v23  
**Stand:** 2026-07-07  
**Bezugstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md`  
**Prinzip:** Dieses Dokument protokolliert Normierungsentscheidungen. Es protokolliert sowohl noch offene Normierungsentscheidungen als auch bereits materialisierte Schema-/Tabellenänderungen.

## Arbeitsregel

Nicht nach jeder einzelnen terminologischen Entscheidung eine neue Forschungstabelle erzeugen. Stattdessen:

1. Entscheidung im Handbuch formulieren.
2. Entscheidung im Änderungsprotokoll mit Zielwert und betroffenen Ausgangswerten festhalten.
3. Nach Abschluss eines Redaktionsblocks alle beschlossenen Änderungen gesammelt auf die Forschungstabelle anwenden und daraus eine neue Tabellenversion erzeugen.

## Beschlossene Änderungen

| ID | Feld | Ausgangswert / Problemform | Zielwert / Normwert | Entscheidung | Status Forschungstabelle |
| --- | --- | --- | --- | --- | --- |
| HB-001 | Buchgattung | `Bibelauslegung` | `Bibelexegese` | `Bibelexegese` ist der bevorzugte Oberbegriff für allgemeine biblische Auslegung. | noch nicht umgesetzt |
| HB-002 | Buchgattung | `Bibelglossen / Kommentar` | `Bibelglossen` oder `Bibelkommentar` | Slash-Mischform auflösen; Entscheidung je nach dominierender Form des Textes. | noch nicht umgesetzt |
| HB-003 | Buchgattung | `Bibelglossen / liturgisch-theologischer Exzerpt` | `Bibelglossen` | Buchgattung nicht mit Exzerpt-/Sonderbestandteilen vermischen; Exzerptcharakter in Werktyp oder Bemerkungen erfassen. | noch nicht umgesetzt |
| HB-004 | Buchgattung | `Bibelkommentar / Homilien` | `Bibelkommentar` oder `Homilien` | Keine Untergattung für Bibelkommentare; nach dominierender Form entscheiden. | noch nicht umgesetzt |
| HB-005 | Buchgattung | `Bibelkommentar / Predigten` | `Bibelkommentar`, `Homilien` oder `Predigten` | Keine Untergattung für Bibelkommentare; Predigtcharakter gegebenenfalls als eigene Gattung wählen oder in Bemerkungen erfassen. | noch nicht umgesetzt |
| HB-006 | Buchgattung | `Homilien / Bibelauslegung` | `Homilien` oder `Bibelexegese` | `Bibelauslegung` nicht weiterführen; homiletische Form und exegetischer Inhalt trennen. | noch nicht umgesetzt |
| HB-007 | Buchgattung | `Traktat / Bibelauslegung` | `Traktat`, `Bibelexegese` oder ggf. `Bibelkommentar` | `Bibelauslegung` nicht weiterführen; nach dominierender Form entscheiden. | noch nicht umgesetzt |
| HB-008 | Buchgattung | mögliche Zusammenlegung `Bibel mit Glosse` → `Bibeltext` | `Bibel mit Glosse` bleibt erhalten | Eigener Normbegriff für biblischen Grundtext mit beigegebener Glosse; reine Glossenbestände bleiben `Bibelglossen`. | keine Änderung nötig, soweit bereits korrekt verwendet |

| HB-009 | Schema / Buchgattung | `Bibeltext`, `Bibel mit Glosse`, `Evangelienbuch`, `Perikopenbuch`, `Evangelistar` als gleichrangige Buchgattungen | `Bibeltext` als Hauptgattung; konkrete Form in neuer Spalte `Sub-Gattung` | Biblische Primärtexte werden zweistufig erfasst: Hauptgattung `Bibeltext`; Sub-Gattung nur bei klarer Gebrauchsform (`Evangelienbuch`, `Evangelistar`, `Perikopenbuch`, `Bibel mit Glosse`). `Einzelbuch` und `Teilbibel` werden nicht als Sub-Gattungen eingeführt. | umgesetzt in `v6-1` |
| HB-010 | Buchgattung / Sub-Gattung | `Liturgik` als Buchgattung | `Lehrschrift` oder `Traktat`; `Sub-Gattung = Liturgik`; `Thema = Liturgie` | `Liturgik` bezeichnet erklärende, systematische oder lehrhafte Texte über Liturgie und wird nicht mit `Liturgisches Buch` gleichgesetzt. | noch nicht umgesetzt |
| HB-011 | Buchgattung | unscharfe Verwendung von `Liturgisches Buch` für alles Liturgische | `Liturgisches Buch` nur für liturgische Gebrauchsbücher | `Liturgisches Buch` bleibt Buchgattung für Vollzug, Formulare, Gebete, Ordnungen und Riten; erklärende Texte über Liturgie werden nicht darunter subsumiert. | noch nicht umgesetzt |
| HB-012 | Buchgattung / Sub-Gattung | undifferenzierte `Lehrschrift` | durch HB-015 ersetzt | Frühere Zwischenentscheidung: `Lehrschrift` sollte Hauptgattung bleiben und fachlich über `Sub-Gattung` differenziert werden. Diese Regel ist durch den neuen Zwischenstand `Fachtext` abgelöst. | abgelöst, nicht umgesetzt |
| HB-013 | Buchgattung | mögliche Einführung `Theologie` | keine Buchgattung `Theologie` | `Theologie` wird nicht als Buchgattung eingeführt; theologische Inhalte werden über `Sub-Gattung`, `Thema` und `Überlieferungslinie` erfasst. | keine Tabellenänderung, soweit nicht verwendet |
| HB-014 | Buchgattung | `Homiliensammlung`; ggf. `Homilie` | `Homilien` | `Homiliensammlung` wird nicht als eigener Normbegriff fortgeführt. `Homilien` genügt vorläufig für Einzelhomilien und Sammlungen; ein möglicher `Homiliar`-Sonderfall wird nur bei sicher liturgisch geordnetem Gebrauchsbuch später geprüft. | noch nicht umgesetzt |
| HB-015 | Buchgattung / Sub-Gattung / Thema | zu viele fachlich spezifizierte Buchgattungen, z. B. `Medizinisches Handbuch`, `Medizinische Rezepte`, `Medizinische Lehrschrift`, und zu breite Verwendung von `Lehrschrift` | `Buchgattung = Fachtext`; nähere Textform in `Sub-Gattung`; Fachgebiet in `Thema` | `Fachtext` wird als vorläufige breite Hauptgattung für fachbezogene Sachtexte eingeführt. `Lehrschrift`, `Handbuch`, `Rezeptsammlung`, `Traktat`, `Ars`, `Messerklärung`, `Glossar` usw. sind eher Sub-Gattungen; `Medizin`, `Arithmetik`, `Grammatik`, `Computus`, `Liturgie`, `Theologie` usw. gehören ins Thema. | noch nicht umgesetzt |

## Offene Redaktionsfragen

- Ob ein ausdrücklich liturgisch geordnetes Homilienbuch später als `Liturgisches Buch` mit `Sub-Gattung = Homiliar` geführt werden soll, bleibt offen; `Homiliensammlung` wird jedoch nicht als eigener Normwert fortgeführt.
- Ob `Psalmenkommentar` als Sonderfall von `Bibelkommentar` erhalten bleiben soll oder später zu `Bibelkommentar` normiert wird.
- Ob `Bibelbezogene Quaestionen` als eigene Gattung erhalten bleibt oder zu `Bibelexegese` gezogen wird.
- Weitere Befüllung der Spalte `Sub-Gattung` außerhalb der biblischen Primärtexte erst nach gesonderter Normierungsentscheidung.
- Konkrete Umsetzung von `Fachtext`: Welche bisherigen Buchgattungen werden darunter zusammengeführt, und welche Werte werden als Sub-Gattungen geführt (`Lehrschrift`, `Handbuch`, `Rezeptsammlung`, `Traktat`, `Ars`, `Messerklärung`, `Glossar` usw.)?
- Ob Spezialformen liturgischer Gebrauchsbücher langfristig als eigene Buchgattungen stehen bleiben oder als `Sub-Gattung` unter `Liturgisches Buch` geführt werden, bleibt offen.

## In v6-1 materialisierte Änderungen

| ID | Datei | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-001 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | Spalte `Sub-Gattung` direkt nach `Buchgattung` eingefügt. | 404 Tabellenzeilen |
| UM-002 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Evangelienbuch` von `Buchgattung` nach `Sub-Gattung` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 14 Zeilen |
| UM-003 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Evangelistar` bzw. als `Perikopenbuch` geführte Evangelistare nach `Sub-Gattung = Evangelistar` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 5 Zeilen |
| UM-004 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Bibel mit Glosse` von `Buchgattung` nach `Sub-Gattung` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 2 Zeilen |

Nicht umgesetzt in `v6-1`: die weitere Homogenisierung der biblischen Auslegungstexte (`Bibelauslegung` → `Bibelexegese`, Slash-Formen bei `Bibelglossen`/`Bibelkommentar` usw.). Diese bleibt als offener Redaktionsblock im Protokoll stehen.


## Zwischenstand v6 des ChangeLogs: `Fachtext`

Die bisherige Tendenz, jede fachliche Differenz bereits in der Buchgattung auszudrücken, wird zugunsten eines schlankeren Modells korrigiert. Die neue Spalte `Sub-Gattung` soll nicht das `Thema` wiederholen, sondern die nähere Textform oder Gebrauchsform erfassen.

Beispiel:

| Buchgattung | Sub-Gattung | Thema |
| --- | --- | --- |
| `Fachtext` | `Rezeptsammlung` | `Medizin` |
| `Fachtext` | `Handbuch` | `Medizin` |
| `Fachtext` | `Lehrschrift` | `Arithmetik` |
| `Fachtext` | `Messerklärung` | `Liturgie` |

Damit wird die ältere Zwischenentscheidung, `Lehrschrift` als breite Hauptgattung zu verwenden, ersetzt. `Lehrschrift` bleibt aber als Sub-Gattung möglich.


---

## In v6-2 materialisierte Änderungen

**Neue Tabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-2.md`  
**Ausgangstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md`

In v6-2 wurden die bisher beschlossenen Normierungsentscheidungen zu `Fachtext`, Homilien, Liturgik/Messerklärung und biblischen Auslegungstexten umgesetzt. Die Änderung erfolgte konservativ: Nur bereits besprochene und hinreichend klare Fälle wurden materialisiert.

### Umfang

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 404 |
| Spalten | 13 |
| geänderte Tabellenzeilen | 87 |
| geänderte Zellen | 160 |
| unterschiedliche Buchgattungen vorher | 124 |
| unterschiedliche Buchgattungen nachher | 99 |
| unterschiedliche Sub-Gattungen vorher | 4 |
| unterschiedliche Sub-Gattungen nachher | 13 |

### Buchgattungsänderungen

| Ausgangswert | Ziel-Buchgattung | Anzahl Zeilen |
| --- | --- | ---: |
| `Bibelauslegung` | `Bibelexegese` | 2 |
| `Bibelglossen / Kommentar` | `Bibelglossen` | 1 |
| `Bibelglossen / liturgisch-theologischer Exzerpt` | `Bibelglossen` | 1 |
| `Bibelkommentar / Homilien` | `Homilien` | 1 |
| `Bibelkommentar / Predigten` | `Bibelkommentar` | 2 |
| `Dogmatischer Traktat` | `Fachtext` | 2 |
| `Eucharistischer Traktat` | `Fachtext` | 1 |
| `Glossar` | `Fachtext` | 2 |
| `Glossar / Enzyklopädie` | `Fachtext` | 1 |
| `Glossar / Enzyklopädische Sammlung` | `Fachtext` | 1 |
| `Homilie` | `Homilien` | 1 |
| `Homilien / Bibelauslegung` | `Homilien` | 1 |
| `Homiliensammlung` | `Homilien` | 3 |
| `Lehrbuch` | `Fachtext` | 1 |
| `Lehrnotiz` | `Fachtext` | 1 |
| `Lehrschema` | `Fachtext` | 1 |
| `Lehrschrift` | `Fachtext` | 10 |
| `Liturgik` | `Fachtext` | 2 |
| `Medizinisches Handbuch` | `Fachtext` | 11 |
| `Messerklärung` | `Fachtext` | 1 |
| `Philosophischer Traktat` | `Fachtext` | 3 |
| `Polemischer Traktat` | `Fachtext` | 1 |
| `Rhetoriklehrbuch` | `Fachtext` | 1 |
| `Theologischer Traktat` | `Fachtext` | 1 |
| `Traktat` | `Fachtext` | 33 |
| `Traktat / Bibelauslegung` | `Bibelexegese` | 2 |

### Neu bzw. zusätzlich befüllte Sub-Gattungen

| Sub-Gattung | Anzahl befüllter Zeilen |
| --- | ---: |
| `Ars` | 1 |
| `Glossar` | 4 |
| `Handbuch` | 11 |
| `Lehrnotiz` | 1 |
| `Lehrschema` | 1 |
| `Lehrschrift` | 11 |
| `Liturgik` | 2 |
| `Messerklärung` | 1 |
| `Traktat` | 41 |

### In v6-2 bewusst noch offen gelassen

- `Bibelbezogene Quaestionen`: noch nicht auf `Bibelexegese` reduziert, weil die Quaestio-Frage gesondert entschieden werden sollte.
- `Psalmenkommentar`: noch nicht zu `Bibelkommentar` normiert.
- Grammatische und rhetorische Spezialformen (`Grammatik`, `Rhetorik`, `Grammatik / Rhetorik` usw.) bleiben für einen eigenen Redaktionsblock offen.
- Computistische und kalendarische Spezialformen bleiben für einen eigenen Redaktionsblock offen.
- Philosophische Dialoge und philosophische Einzeltexte bleiben vorerst unverändert, soweit sie nicht ausdrücklich als Traktat erfasst waren.
- Spezialformen liturgischer Gebrauchsbücher (`Sakramentar`, `Messbuch`, `Pontifikale`, `Liturgisches Buch` usw.) bleiben für einen eigenen Redaktionsblock offen.

### Prüfdatei

Eine maschinenlesbare Änderungsübersicht wurde zusätzlich erzeugt: `materialisierung_v6-2_aenderungen.tsv`.


## v8 – Materialisierung liturgischer Gebrauchsbücher

**Status:** umgesetzt in `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-3.md`.

**Regel:** `Liturgisches Buch` bleibt die Buchgattung für liturgische Gebrauchsbücher. Die konkrete liturgische Gebrauchsform wird in `Sub-Gattung` geführt.

| bisheriger Wert / Befund | Buchgattung nach v6-3 | Sub-Gattung nach v6-3 |
| --- | --- | --- |
| `Sakramentar` / `Sacramentarium` | `Liturgisches Buch` | `Sakramentar` |
| `Messbuch` / `Missale` | `Liturgisches Buch` | `Messbuch` |
| `Pontifikale` / `Pontificale` | `Liturgisches Buch` | `Pontifikale` |
| `Benedictionale` | `Liturgisches Buch` | `Benedictionale` |
| `Ordo Romanus` / liturgische Ordnung | `Liturgisches Buch` | `Ordo` |

**Abgrenzung:** Erklärende Texte über Liturgie bleiben `Fachtext` mit Sub-Gattungen wie `Liturgik`, `Messerklärung` oder `Traktat`. Liturgisch gebrauchte biblische Lesetexte bleiben `Bibeltext` mit Sub-Gattungen wie `Evangelistar` oder `Perikopenbuch`.

**Materialisierung:** 18 Zeilen geändert, 25 Zellen geändert; Details in `materialisierung_v6-3_aenderungen.tsv`.

## v9 – Normierungsentscheidung: `Bücherverzeichnis` → `Katalog`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Bücherverzeichnis` und `Katalog` werden nicht als getrennte Buchgattungen geführt. Normwert ist künftig `Katalog`.

| Ausgangswert | Zielwert | Feld | Bemerkung |
| --- | --- | --- | --- |
| `Bücherverzeichnis` | `Katalog` | `Buchgattung` | Betrifft Bücher- bzw. Textverzeichnisse; weitere Präzisierung bleibt über `Text`, `Werk`, `Thema` und ggf. `Bemerkungen` möglich. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Bücherverzeichnis`-Einträge zu `Katalog` vereinheitlichen. Eine weitergehende Vereinheitlichung von `Bibliothekskatalog` oder `Literaturgeschichtlicher Katalog` ist damit noch nicht automatisch beschlossen und kann gesondert entschieden werden.

## v10 – Normierungsentscheidung: `Brief` / `Briefsammlung` → `Briefe`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Brief` und `Briefsammlung` werden nicht als getrennte Buchgattungen geführt. Normwert ist künftig `Briefe`.

| Ausgangswert | Zielwert | Feld | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | ---: | --- |
| `Brief` | `Briefe` | `Buchgattung` | 7 | Singularform wird vermieden. |
| `Briefsammlung` | `Briefe` | `Buchgattung` | 13 | Sammlungseigenschaft bei Bedarf in `Werktyp`, `Werk` oder `Bemerkungen`. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Brief`- und `Buchgattung = Briefsammlung`-Einträge zu `Briefe` vereinheitlichen.



## v11 – Normierungsentscheidung: `Sequenz` / `Sequenzen` → `Dichtung` mit Sub-Gattung `Sequenz`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Sequenz` wird nicht als eigene Buchgattung geführt. Sequenzen gehören zur Großgattung `Dichtung`; die konkrete poetisch-liturgische Form wird in `Sub-Gattung` erfasst.

| Ausgangswert | Zielwert Buchgattung | Zielwert Sub-Gattung | Feld(er) | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | --- | ---: | --- |
| `Sequenz` | `Dichtung` | `Sequenz` | `Buchgattung`, `Sub-Gattung` | 1 | Singularform wird als Sub-Gattung erhalten. |
| `Sequenzen` | `Dichtung` | `Sequenz` | `Buchgattung`, `Sub-Gattung` | 1 | Pluralform wird auf den Sub-Gattungs-Normwert `Sequenz` reduziert. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Sequenz`- und `Buchgattung = Sequenzen`-Einträge zu `Buchgattung = Dichtung`, `Sub-Gattung = Sequenz` vereinheitlichen. Das Thema bleibt je nach Eintrag erhalten bzw. kann bei Bedarf auf `Liturgie / Dichtung` geprüft werden.


## v12 – Normierungsentscheidung: `Genealogie` → `Geschichtswerk` mit Sub-Gattung `Genealogie`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Genealogie` wird nicht als eigene Buchgattung geführt. Genealogische Texte gehören zur Großgattung `Geschichtswerk`; die konkrete historische Form wird in `Sub-Gattung` erfasst.

| Ausgangswert | Zielwert Buchgattung | Zielwert Sub-Gattung | Feld(er) | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | --- | ---: | --- |
| `Genealogie` | `Geschichtswerk` | `Genealogie` | `Buchgattung`, `Sub-Gattung` | 1 | Betrifft aktuell `Genealogia Karolinorum`; genealogische Form bleibt in der Sub-Gattung sichtbar. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Genealogie`-Einträge zu `Buchgattung = Geschichtswerk`, `Sub-Gattung = Genealogie` vereinheitlichen.


## v13 – Normierungsentscheidung: `Predigt` / `Predigten` → `Homilien`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Predigt` und `Predigten` werden nicht als eigene Buchgattungen neben `Homilien` geführt. Normwert ist künftig `Homilien`.

| Ausgangswert | Zielwert Buchgattung | Feld | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | ---: | --- |
| `Predigt` | `Homilien` | `Buchgattung` | 1 | Singularform wird vermieden. |
| `Predigten` | `Homilien` | `Buchgattung` | 3 | Predigtsammlungen werden nicht als eigene Gattung von Homilien getrennt. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Predigt`- und `Buchgattung = Predigten`-Einträge zu `Buchgattung = Homilien` vereinheitlichen. Die genaue Predigt- oder Sammlungssituation kann bei Bedarf in `Werk`, `Werktyp`, `Thema` oder `Bemerkungen` stehen.


## v14 – Normierungsentscheidung: bibelbezogene `Quaestiones`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** Bibelbezogene `Quaestiones` werden nicht als `Bibeltext` geführt und nicht pauschal als `Bibelkommentar`. Normwert ist `Buchgattung = Bibelexegese`; die Form wird in `Sub-Gattung = Quaestiones` erfasst.

| Ausgangswert / Befund | Zielwert Buchgattung | Zielwert Sub-Gattung | Feld(er) | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | --- | ---: | --- |
| `Bibelbezogene Quaestionen` | `Bibelexegese` | `Quaestiones` | `Buchgattung`, `Sub-Gattung` | 1 | Direkte Vereinheitlichung. |
| Werktitel `Quaestiones ...` bei biblischem Bezug | einzeln prüfen: meist `Bibelexegese` | meist `Quaestiones` | `Buchgattung`, `Sub-Gattung` | 3 weitere Kandidaten | Nicht automatisch ändern, wenn der Eintrag als fortlaufender Kommentar organisiert ist. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung mindestens `Buchgattung = Bibelbezogene Quaestionen` zu `Buchgattung = Bibelexegese`, `Sub-Gattung = Quaestiones` ändern. Weitere quaestionenartige Bibelauslegung einzeln prüfen, insbesondere ob `Bibelkommentar` in einzelnen Fällen zu allgemein oder zu eng ist.


## v15 – Normierungsentscheidung: `Grammatik` → `Fachtext` mit Sub-Gattung `Grammatik`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** `Grammatik` wird nicht als eigene Buchgattung geführt. Grammatische Texte gehören zur Großgattung `Fachtext`; die konkrete grammatische Form wird in `Sub-Gattung = Grammatik` erfasst. Das Thema bleibt `Grammatik`.

| Ausgangswert | Zielwert Buchgattung | Zielwert Sub-Gattung | Feld(er) | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | --- | ---: | --- |
| `Grammatik` | `Fachtext` | `Grammatik` | `Buchgattung`, `Sub-Gattung` | 11 | Thema `Grammatik` bleibt erhalten. |
| `Grammatik / Rhetorik` | noch prüfen | noch prüfen | `Buchgattung`, `Sub-Gattung` | 1 | Nicht automatisch ändern; Rhetorik-Block gesondert entscheiden. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung alle aktuellen `Buchgattung = Grammatik`-Einträge zu `Buchgattung = Fachtext`, `Sub-Gattung = Grammatik` ändern. Den Mischwert `Grammatik / Rhetorik` gesondert prüfen, sobald die Normierung für rhetorische Texte beschlossen ist.


## v16 – Normierungsentscheidung: Artes liberales, Computus und Medizin als `Fachtext`

**Status:** beschlossen, noch nicht in der Forschungstabelle materialisiert.

**Regel:** Texte der Artes liberales und verwandter fachbezogener Wissensbereiche werden künftig einheitlich als `Buchgattung = Fachtext` geführt. Die fachliche Texttradition steht in `Sub-Gattung`; der Gegenstand bleibt in `Thema` sichtbar.

| Ausgangswert / Bereich | Zielwert Buchgattung | Zielwert Sub-Gattung | Feld(er) | aktuelle Treffer in v6-3 | Bemerkung |
| --- | --- | --- | --- | ---: | --- |
| `Grammatik` | `Fachtext` | `Grammatik` | `Buchgattung`, `Sub-Gattung` | 11 | Bereits beschlossen; nun in die Artes-Regel integriert. |
| `Rhetorik` | `Fachtext` | `Rhetorik` | `Buchgattung`, `Sub-Gattung` | 1 | Analog zu Grammatik. |
| `Grammatik / Rhetorik` | `Fachtext` | `Grammatik / Rhetorik` oder fallweise Auflösung | `Buchgattung`, `Sub-Gattung` | 1 | Bei Materialisierung prüfen, ob auf zwei Werte aufzulösen ist. |
| arithmetische Texte | `Fachtext` | `Arithmetik` | `Buchgattung`, `Sub-Gattung` | 0 als Buchgattung; 2 im Thema | Boethius, `De institutione arithmetica`, ist bereits im Fachtext-Modell mitzudenken. |
| `Computistische Sammlung` | `Fachtext` | `Computus` | `Buchgattung`, `Sub-Gattung` | 1 | Computus wird wie artesbezogener Fachtext behandelt. |
| `Chronographie / Computus?` | einzeln prüfen | einzeln prüfen | `Buchgattung`, `Sub-Gattung` | 1 | Grenzfall zwischen Geschichtswerk/Chronographie und Computus. |
| `Kalender` | einzeln prüfen | `Kalender` oder `Computus` | `Buchgattung`, `Sub-Gattung` | 2 | Liturgische Kalender nicht automatisch mit technischen Computus-Texten gleichsetzen. |
| medizinische Fachtexte | `Fachtext` | `Medizin` | `Buchgattung`, `Sub-Gattung` | bereits teilweise materialisiert | Medizin wird nicht als fachadjektivische Hauptgattung geführt. |
| `Musiktheoretischer / liturgischer Text` | einzeln prüfen | `Musiktheorie` oder liturgische Sub-Gattung | `Buchgattung`, `Sub-Gattung` | 2 | Musiktheorie gehört zum Fachtext; liturgischer Gebrauch gesondert prüfen. |

**Vorgemerkte Umsetzung:** Bei der nächsten Materialisierung die Artes- und Fachwerte, soweit eindeutig, zu `Fachtext` mit entsprechender `Sub-Gattung` vereinheitlichen. Grenzfälle (`Chronographie / Computus?`, `Kalender`, `Musiktheoretischer / liturgischer Text`, medizinische Briefe) einzeln prüfen und nicht pauschal umsetzen.


---

## v17 – Materialisierung des aktuellen Normierungsstands als v6-5

**Status:** umgesetzt.  
**Neue Forschungstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-5.md`  
**Ausgangstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-4.md`  
**Zweck:** letzter inhaltlich normierter Stand im bisherigen 13-Spalten-Schema vor der geplanten Schema-Migration zu v7.

### Umfang

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 405 |
| Spalten | 13 |
| geänderte Zeilen gegenüber v6-4 | 87 |
| geänderte Zellen gegenüber v6-4 | 122 |
| Buchgattungen vorher | 94 |
| Buchgattungen nachher | 79 |
| Sub-Gattungen vorher | 19 |
| Sub-Gattungen nachher | 30 |
| fehlerhafte Tabellenzeilen | 0 |

### Umgesetzte Normierungsblöcke

| Block | Umsetzung in v6-5 |
| --- | --- |
| Kataloge | `Bücherverzeichnis` → `Katalog` |
| Briefe | `Brief` und `Briefsammlung` → `Briefe` |
| Sequenzen | `Sequenz` / `Sequenzen` → `Dichtung`, `Sub-Gattung = Sequenz` |
| Hagiographische Dialoge | `Dialog / Hagiographie` sowie hagiographische `Dialog`-Einträge → `Hagiographie`, `Sub-Gattung = Dialog` |
| Genealogie | `Genealogie` → `Geschichtswerk`, `Sub-Gattung = Genealogie` |
| Predigten | `Predigt` / `Predigten` → `Homilien` |
| Bibelbezogene Quaestiones | klare quaestionenartige Bibelauslegung → `Bibelexegese`, `Sub-Gattung = Quaestiones` |
| Grammatik / Rhetorik | `Grammatik`, `Rhetorik`, `Grammatik / Rhetorik` → `Fachtext` mit entsprechender Sub-Gattung |
| Artes / Computus / Medizin | eindeutige Fachtexte zu `Fachtext` mit Sub-Gattung `Arithmetik`, `Computus`, `Medizin`, `Musiktheorie` oder `Artes liberales` |

### Aggregierte Zelländerungen

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

### Prüfdatei

Die maschinenlesbare Änderungsübersicht steht in `materialisierung_v6-5_aenderungen.tsv`.

### Nicht erledigt in v6-5

Schemaänderungen wurden bewusst nicht durchgeführt. Spaltenumordnung, Umbenennung oder Löschung erfolgen erst in einer späteren Version `v7`.

## v18 – Schema-Migration zu Forschungstabelle v7 (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-5.md`  
**Ergebnis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7.md`

### Beschlossene Schemaänderungen

| alte Spalte | Aktion | neue Spalte / Position |
| --- | --- | --- |
| `Autor` | verschoben | direkt nach `Siegel` |
| `Lorsch-Bezug` | verschoben | ans Tabellenende |
| `Text` | gelöscht | entfällt |
| `Werk` | umbenannt | `Titel` |
| `Sub-Gattung` | umbenannt | `Untergattung` |
| `Werktyp` | gelöscht | entfällt; relevante Einzelinformationen künftig in `Bemerkungen` |

### Neues v7-Schema

`TXT-ID | LHS-ID | Siegel | Autor | Titel | Buchgattung | Untergattung | Thema | Überlieferungslinie | Bemerkungen | Lorsch-Bezug`

### Migrationsprinzipien

- Die neue Spalte `Titel` wurde aus den bisherigen Werten der Spalte `Werk` gebildet.
- Die bisherige Spalte `Text` wurde nicht übernommen.
- Die bisherige Spalte `Werktyp` wurde nicht pauschal in `Bemerkungen` kopiert, um die Bemerkungsspalte nicht mit Routinewerten wie `Originalwerk`, `Redaktion`, `Kompilation` usw. zu überladen.
- Zur Kontrolle wurde eine Audit-Datei mit den gelöschten Spaltenwerten erstellt: `schema_migration_v7_geloeschte_spalten_audit.tsv`.


## v19 – Schema-Migration zu Forschungstabelle v7-1: Spalte `Seiten` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7.md`  
**Ergebnis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-1.md`

### Beschlossene Schemaänderung

| Änderung | Umsetzung |
| --- | --- |
| neue Spalte `Seiten` | direkt nach `Siegel` eingefügt |
| Seiten-/Blattangaben in `Bemerkungen` | soweit eindeutig erkennbar nach `Seiten` extrahiert |
| Standardformel `Text [Nr.] nach Bibliotheca Laureshamensis` | aus `Bemerkungen` entfernt |
| Standardformel `Nachtrag [Nr.] nach Bibliotheca Laureshamensis` | bereinigt; `Nachtrag` bzw. `Nachtrag [Nr.]` bleibt erhalten, wenn sachlich sinnvoll |

### Umfang

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 405 |
| Spalten nach Migration | 12 |
| befüllte `Seiten`-Zellen | 66 |
| Zeilen mit geänderter `Bemerkungen`- oder neuer `Seiten`-Information | 66 |
| verbleibende Standardformeln | 0 |

### Prüfdatei

Die maschinenlesbare Kontrollübersicht steht in `schema_migration_v7-1_seiten_audit.tsv`.


## v20 – Normierung zu Forschungstabelle v7-2: Überlieferungslinie `Bibel` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-1.md`  
**Ergebnis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-2.md`

### Beschlossene Normierung

| Feld | bisheriger Wert | neuer Normwert |
| --- | --- | --- |
| `Überlieferungslinie` | `Biblische Überlieferung` | `Bibel` |

### Umfang

| Kennzahl | Wert |
| --- | ---: |
| geänderte Zeilen | 25 |
| verbleibende `Überlieferungslinie = Biblische Überlieferung` | 0 |
| Datenzeilen | 405 |
| Spalten | 12 |

Hinweis: Vorkommen von `Biblische Überlieferung` in anderen Spalten, besonders im Feld `Thema`, wurden durch diesen Schritt nicht automatisch geändert.


## v21 – Normierung zu Forschungstabelle v7-3: `Christlicher Kanon` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-2.md`  
**Ergebnis:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`

### Beschlossene Normierung

| Feld | bisheriger Wert | neuer Normwert |
| --- | --- | --- |
| `Überlieferungslinie` | `Bibel` | `Christlicher Kanon` |
| `Überlieferungslinie` | `Kirchenrechtliche Tradition` | `Christlicher Kanon` |
| `Thema` | `Biblische Überlieferung` | `Bibel` |

### Begründung

`Bibel` war als Überlieferungslinie zu eng und doppelte sich teilweise mit `Thema = Biblische Überlieferung`. Der neue Normwert `Christlicher Kanon` fasst die normative christliche Kanontradition zusammen: biblische Grundtexte, kanonische Normtexte, Konzilsbeschlüsse, Kanones und kirchenrechtliche Sammlungen. Das konkrete Sachgebiet wird weiterhin im Feld `Thema` differenziert, z. B. `Bibel` oder `Kirchenrecht`.

### Umfang

| Kennzahl | Wert |
| --- | ---: |
| geänderte Zeilen insgesamt | 37 |
| verbleibende `Thema = Biblische Überlieferung` | 0 |
| verbleibende `Überlieferungslinie = Bibel` | 0 |
| verbleibende `Überlieferungslinie = Kirchenrechtliche Tradition` | 0 |
| `Überlieferungslinie = Christlicher Kanon` | 37 |
| Datenzeilen | 405 |
| Spalten | 12 |


## v22 – Vorgemerkte Tabellenkorrektur: Cassian, Collationes in TXT0009/TXT0010 (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Vorgemerkte Änderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Bemerkung |
| --- | --- | --- | --- | --- |
| `TXT0009` | `Titel` | `Collationes` | `Collationes I–X` | Kapitel-/Buchumfang aus der bisherigen Bemerkung in den Titel aufnehmen. |
| `TXT0010` | `Titel` | `Collationes` | `Collationes XI–XVII` | Kapitel-/Buchumfang aus der bisherigen Bemerkung in den Titel aufnehmen. |

### Hinweis

Die bestehenden Bemerkungen `Teilüberlieferung I–X.` und `Teilüberlieferung XI–XVII.` werden vorerst nicht gelöscht. Bei der nächsten Materialisierung kann geprüft werden, ob sie wegen der Titelpräzisierung entfallen sollen oder als knappe Überlieferungsnotiz stehen bleiben.


## v23 – Vorgemerkte Normierung: `Oribasianische Tradition` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Vorgemerkte Änderung

| Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- |
| `Überlieferungslinie` | `Oribasianische Tradition` | `Spätantike Medizin` | `Oribasianische Tradition` ist zu speziell und wenig transparent; `Spätantike Medizin` bildet den medizinischen Traditionszusammenhang breiter ab. |

### Hinweis

Ein konkreter Bezug zu Oribasius kann, falls für eine bestimmte Zeile relevant, in `Titel` oder `Bemerkungen` erhalten bleiben. Die Normierung betrifft nur den Wert in der Spalte `Überlieferungslinie`.


## v24 – Vorgemerkte Normierung: Sequenz TXT0015-01 und überfeine Überlieferungslinien (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Vorgemerkte Änderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0015-01` | `Thema` | `Liturgie / Dichtung` | `Dichtung` | In diesem Kontext soll die Sequenz primär als Dichtung behandelt werden; der liturgische Bezug ist durch `Untergattung = Sequenz` bzw. ggf. Bemerkungen erkennbar. |
| `TXT0015-01` | `Überlieferungslinie` | `St. Galler Sequenztradition` | `Karolingische Gelehrsamkeit` | `St. Galler Sequenztradition` ist als Tabellenwert zu speziell und betrifft bislang nur diesen Eintrag. |

### Allgemeine Regel

Überlieferungslinien sollen keine einmaligen Sondertraditionen abbilden, die nur an einem einzelnen Werk oder einer einzelnen Zeile hängen. Spezifische Schul-, Kloster- oder Lokaltraditionen werden nur verwendet, wenn sie für mehrere Einträge analytisch tragfähig sind. Andernfalls ist ein breiterer Traditionswert zu bevorzugen; konkrete Besonderheiten können in `Bemerkungen` stehen.


## v25 – Vorgemerkte Normierung: Isidor nicht `Lateinische Patristik` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Vorgemerkte Änderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0008-02` | `Überlieferungslinie` | `Lateinische Patristik` | `Spätantike Gelehrsamkeit` | Isidor wird in dieser Tabelle nicht als lateinische Patristik im engeren Sinn geführt, sondern als spätantike Gelehrsamkeit. |

### Allgemeine Regel

Isidor von Sevilla bzw. isidorische Texte werden in der Spalte `Überlieferungslinie` grundsätzlich unter `Spätantike Gelehrsamkeit` geführt, nicht unter `Lateinische Patristik`. Konkrete Sonderfälle können in `Bemerkungen` erläutert werden.

### Prüfhinweis

Im Stand `v7-3` sind die expliziten Isidor-Zeilen überwiegend bereits korrekt als `Spätantike Gelehrsamkeit` geführt. Die vorgemerkte Änderung betrifft aktuell vor allem `TXT0008-02`.

## v26 – Vorgemerkte Normierung: Überlieferungslinie nach Textfunktion; Cassian `Collationes` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Methodische Regel

Die Spalte `Überlieferungslinie` wird nicht mechanisch vom Autor her bestimmt, sondern vom konkreten Text, seiner Funktion und seinem Überlieferungszusammenhang. Der Autor ist ein Hinweis, aber nicht allein ausschlaggebend.

### Beispiele

| Text / Zuschreibung | Überlieferungslinie | Begründung |
| --- | --- | --- |
| Cassianus, `Collationes` | `Monastische Tradition` | monastische Lehr- und Übungsliteratur |
| Gregorius Magnus (trad.), `Sacramentarium Gregorianum` | `Liturgische Tradition` | liturgisches Gebrauchsbuch; die traditionelle gregorianische Zuschreibung macht es nicht zu Patristik |
| Gregor der Große, `Moralia in Iob` | `Lateinische Patristik` | patristisch-exegetischer Text |
| Isidorische Wissenskompilationen | `Spätantike Gelehrsamkeit` | spätantike Wissens- und Kompilationstradition |

### Vorgemerkte Tabellenänderung

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0009` | `Überlieferungslinie` | `Lateinische Patristik` | `Monastische Tradition` | Cassians `Collationes I–X` sind primär monastische Tradition, nicht Patristik im engeren Sinne. |
| `TXT0010` | `Überlieferungslinie` | `Lateinische Patristik` | `Monastische Tradition` | Cassians `Collationes XI–XVII` sind primär monastische Tradition, nicht Patristik im engeren Sinne. |

### Hinweis

Diese Änderung ergänzt die bereits in v22 vorgemerkte Titelpräzisierung zu `TXT0009` und `TXT0010` (`Collationes I–X` bzw. `Collationes XI–XVII`). Eine neue Forschungstabellenversion wird erst nach Sammlung weiterer Änderungen erstellt.



## v27 – Vorgemerkte Korrektur: `Homiletik` bei LHS0017 (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Entscheidung

`Homiletik` wird nicht als Thema für konkrete Homilienbestände verwendet. Der Begriff bezeichnet eher die Lehre bzw. Theorie der Predigt. Für LHS0017 ist deshalb `Homilien` der bessere Themenwert.

### Vorgemerkte Tabellenänderung

| TXT-ID | LHS-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- | --- |
| `TXT0018` | `LHS0017` | `Thema` | `Homiletik` | `Homilien` | Der Titel lautet `Homiliae`; es handelt sich um konkrete Homilien, nicht um eine theoretische Predigtlehre. |

### Allgemeine Regel

`Homiletik` bleibt nur für ausdrücklich theoretische, regelhafte oder reflexive Texte über Predigt bzw. Homilie möglich. Konkrete Homilien oder Homilienbestände erhalten als Thema `Homilien`; wenn der exegetische Charakter im Vordergrund steht, kann `Bibelexegese` passender sein.


## v28 – Vorgemerkte Normierung: Pseudo-Hegesippus nicht `Lateinische Patristik` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Entscheidung

Pseudo-Hegesippus, `De excidio Hierosolymitano`, wird in der Spalte `Überlieferungslinie` nicht unter `Lateinische Patristik` geführt. Der künftige Normwert ist `Spätantike Gelehrsamkeit`.

### Vorgemerkte Tabellenänderung

| TXT-ID | LHS-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- | --- |
| `TXT0021` | `LHS0020` | `Überlieferungslinie` | `Lateinische Patristik` | `Spätantike Gelehrsamkeit` | `De excidio Hierosolymitano` ist in dieser Tabelle als spätantikes Geschichtswerk relevant, nicht als Patristik im engeren Sinn. |

### Hinweis

Die Buchgattung `Geschichtswerk` und das Thema `Geschichte` bleiben für diese Zeile plausibel. Falls der Josephus-/Hegesippus-Bezug analytisch wichtig ist, gehört er eher in `Bemerkungen` als in eine eigene Überlieferungslinie.


## v29 – Vorgemerkte Normierung: `Hellenistisch-jüdische Tradition` zu `Antik-jüdische Literatur` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Entscheidung

`Hellenistisch-jüdische Tradition` wird in der Spalte `Überlieferungslinie` künftig zu `Antik-jüdische Literatur` vereinheitlicht.

### Vorgemerkte Tabellenänderungen

| TXT-ID | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- |
| `TXT0028` | `Überlieferungslinie` | `Hellenistisch-jüdische Tradition` | `Antik-jüdische Literatur` | Philo von Alexandria gehört zur antik-jüdischen Literatur in hellenistisch-römischer Rezeption. |
| `TXT0250` | `Überlieferungslinie` | `Hellenistisch-jüdische Tradition` | `Antik-jüdische Literatur` | Flavius Josephus wird durch den breiteren Begriff besser erfasst als durch die engere Bezeichnung `hellenistisch-jüdisch`. |

### Allgemeine Regel

`Antik-jüdische Literatur` bezeichnet jüdische Autoren und Werke der hellenistischen und römischen Zeit, die in lateinischer bzw. christlicher Rezeption überliefert sind. Der Wert ist spezifisch genug für Philo und Josephus, aber weniger eng und weniger sperrig als `Hellenistisch-jüdische Tradition`.


## v30 – Vorgemerkte Normierung: Gregor von Tours nicht `Lateinische Patristik` (2026-07-08)

**Ausgangspunkt:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-3.md`  
**Status:** vorgemerkt, noch nicht in einer neuen Forschungstabellenversion materialisiert.

### Entscheidung

Gregor von Tours wird in der Spalte `Überlieferungslinie` nicht unter `Lateinische Patristik` geführt. Künftiger Normwert für die aktuell betroffenen Zeilen: `Frühmittelalterliche Gelehrsamkeit`.

### Vorgemerkte Tabellenänderungen

| TXT-ID | LHS-ID | Titel | Feld | bisheriger Wert | künftiger Wert | Begründung |
| --- | --- | --- | --- | --- | --- | --- |
| `TXT0034` | `LHS0032` | `Historia Francorum` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Frühmittelalterlich-fränkisches Geschichtswerk, nicht Patristik im engeren Sinn. |
| `TXT0310` | `LHS0283` | `Libri miraculorum` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Hagiographische Mirakelüberlieferung Gregors von Tours; das Thema `Hagiographie` bleibt ausreichend spezifisch. |
| `TXT0342` | `LHS0312` | `Werk unbestimmt` | `Überlieferungslinie` | `Lateinische Patristik` | `Frühmittelalterliche Gelehrsamkeit` | Bei unbestimmtem Werk ist die breitere frühmittelalterliche Linie passender als Patristik. |

### Hinweis

Es wird vorläufig kein eigener Normwert wie `Merowingische Historiographie` eingeführt, weil wir Speziallinien vermeiden, solange sie nicht mehrere analytisch tragfähige Einträge bündeln. Die konkrete Textform bleibt über `Buchgattung`, `Untergattung`, `Thema` und `Bemerkungen` sichtbar.

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

## v32 – Tabellenkorrektur LHS0034

- Ausgangspunkt: Forschungstabelle v7-4.
- Für `LHS0034` wird die pauschale Sammelzeile `TXT0038` (`mehrere Autoren` / `mehrere Werke`) gelöscht. Sie beruhte vermutlich auf dem pauschalen `etc.` in Bischoff und soll nicht als eigener Texteinteilungseintrag geführt werden.
- Die verbleibenden Zeilen `TXT0036` und `TXT0037` bleiben vorläufig erhalten; die endgültige Behandlung von `LHS0034` wird später bestimmt.
- `Lorsch-Bezug` bleibt bei `LHS0034` leer, da der Codex keinen Lorsch-Bezug hat.



## v33 – Materialisierung TXT0039: Homiletik → Homilien

Status: in Forschungstabelle v7-6 materialisiert.

| TXT-ID | Feld | bisher | neu | Begründung |
|---|---|---|---|---|
| TXT0039 | Thema | Homiletik | Homilien | `Homiletik` bezeichnet eher die Lehre/Theorie der Homilie; bei einem Titel `Homiliae` und Buchgattung `Homilien` ist `Homilien` als Thema konsistenter. |


## v34 / vorgemerkte und materialisierte Korrektur TXT0042

Materialisiert in `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-7.md`:

| TXT-ID | Feld | bisher | neu |
|---|---|---|---|
| TXT0042 | Buchgattung | Glossen | Bibelglossen |
| TXT0042 | Überlieferungslinie | Karolingische Gelehrsamkeit | Biblische Glossentradition |

Hinweis: Das Thema `Exegese` blieb bestehen. Die Korrektur betrifft die Einordnung als biblischer Glossenbestand und die zu enge bzw. unpassende Traditionslinie.

## v35 – Korrektur und Splitting `LHS0038 / TXT0042`

Quelle: BL-Beschreibung Karlsruhe, Badische Landesbibliothek, St. Peter perg. 87.

Entscheidung:

- Die vorherige Zeile `TXT0042` wird ersetzt durch fünf Einträge auf oberster Ebene des BL-Inhaltsverzeichnisses.
- `Biblische Glossentradition` wird nicht als Überlieferungslinie beibehalten.
- Die Lorscher Faszikel des 11. Jh. erhalten breit `Frühmittelalterliche Gelehrsamkeit`.
- Die Datierung „Mitte oder 3. Viertel 11. Jh.“ wird nicht als streng ottonisch interpretiert; sie gehört eher in den frühsalischen Kontext, wird aber wegen der Reduktionsmaxime nicht als eigene Traditionslinie eingeführt.
- Faszikel II (`Glossarium Latinum`, 14. Jh., Entstehungsort unbekannt) erhält keinen `Lorsch-Bezug`.

Umsetzung in der Forschungstabelle v7-8:

| alt | neu |
|---|---|
| `TXT0042` | `TXT0042-01` bis `TXT0042-05` |
| `Glossae in Bibliam` | fünf BL-Haupttexte |
| `Biblische Glossentradition` | nicht fortgeführt |



## v36 – Materialisierung: Entfernung `TXT0042-05` aus `LHS0038`

Status: in Forschungstabelle `v7-9` materialisiert.

Ausgangspunkt: Forschungstabelle `v7-8`.

Entscheidung:

- `TXT0042-05` (`Glossarium Latinum`, 3ra-57vb) wird gelöscht.
- Begründung: Der BL-Eintrag weist diesen Abschnitt als Faszikel II aus: Entstehungsort unbekannt, 14. Jh.; er gehört nicht zum Lorscher Faszikel I und hat keinen Lorsch-Bezug.
- Die Forschungstabelle soll hier auf die Lorscher bzw. Lorsch-bezogenen Teile begrenzt bleiben.

Gelöschte Zeile:

| TXT-ID | LHS-ID | Titel | Grund |
|---|---|---|---|
| `TXT0042-05` | `LHS0038` | `Glossarium Latinum` | Faszikel II, 14. Jh., Entstehungsort unbekannt, kein Lorsch-Bezug |

Prüfung der Forschungstabelle `v7-9`:

| Kennzahl | Ergebnis |
|---|---:|
| Datenzeilen | 407 |
| Spalten | 12 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |

## v37 / v7-10 – Slash-Werte in Buchgattung und Untergattung bereinigt

Materialisiert in: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-10.md`

Ausgangspunkt: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-9.md`

Umsetzung:

- Alle 17 Werte mit `/` in `Buchgattung` wurden bereinigt.
- Alle 2 Werte mit `/` in `Untergattung` wurden bereinigt.
- Danach verbleiben keine Schrägstrich-Werte mehr in `Buchgattung` oder `Untergattung`.
- `Thema` wurde bewusst nicht pauschal bereinigt.
- In wenigen Fällen wurde die frühere Unsicherheit bzw. sekundäre Charakterisierung in `Bemerkungen` gesichert, z. B. `Exzerptcharakter unsicher`, `Computus-Bezug unsicher` oder `Enzyklopädischer Dialog`.

Audit-Datei: `materialisierung_v7-10_slash_gattungen_aenderungen.tsv`



## v38 / v7-11 – Untergattungen `Vita` und `Schreiberverse` entfernt

Materialisiert in: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-11.md`

Ausgangspunkt: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-10.md`

Entscheidung:

- `Vita` wird vorläufig nicht als eigene Untergattung geführt. Bei hagiographischen Lebensbeschreibungen genügt `Buchgattung = Hagiographie`; der konkrete Vita-Charakter ist im Titel sichtbar.
- `Schreiberverse` wird vorläufig nicht als eigene Untergattung geführt. Gemeint sind kurze metrische Schreibervermerke bzw. Verse im Umfeld des Schreibvorgangs; für die Tabelle genügt `Buchgattung = Dichtung`, während Einzelheiten in Titel oder Bemerkungen stehen.
- `Allegorese` wurde erklärt, aber noch nicht geändert. Der Wert bleibt vorerst Gegenstand einer gesonderten Entscheidung.

Umsetzung:

| TXT-ID | Feld | vorher | nachher |
|---|---|---|---|
| `TXT0031` | `Untergattung` | `Vita` | leer |
| `TXT0289-02` | `Untergattung` | `Vita` | leer |
| `TXT0289-05` | `Untergattung` | `Schreiberverse` | leer |

Audit-Datei: `materialisierung_v7-11_untergattung_vita_schreiberverse.tsv`

## v39 / v7-12 – `Allegorese` und `Schreiberverse` in Bemerkungen verschoben

Materialisiert in: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-12.md`

Ausgangspunkt: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-11.md`

Entscheidung:

- `Allegorese` wird nicht als Untergattung geführt, sondern in `Bemerkungen` gesichert.
- `Schreiberverse` wird nicht als Untergattung geführt, sondern in `Bemerkungen` gesichert.

Umsetzung:

| TXT-ID | Änderung |
|---|---|
| `TXT0287` | `Untergattung = Allegorese` gelöscht; `Bemerkungen = Allegorese.` |
| `TXT0289-05` | `Bemerkungen` mit dem Hinweis `Schreiberverse` eingeleitet |

Audit-Datei: `materialisierung_v7-12_allegorese_schreiberverse.tsv`



## v40 – Materialisierung Pal. lat. 1588 / LHS0264

Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-12.md`

Zieltabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-13.md`

Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1588.

Umsetzung:

| Aktion | Beschreibung |
|---|---|
| ersetzt | `TXT0290 | LHS0264 | Chirius Fortunatianus | Ars rhetorica | ... etc.` |
| eingefügt | `TXT0290-01` Consultus Fortunatianus, `Ars rhetorica` |
| eingefügt | `TXT0290-02` Augustinus (?), `De rhetorica sive Principia rhetorices` |
| eingefügt | `TXT0290-03` Augustinus (?), `De dialectica sive Principia dialecticae` |
| eingefügt | `TXT0290-04` Cassiodor, `De rhetorica excerptum Cassiodori ex Institutionibus` |
| eingefügt | `TXT0290-05` Marius Victorinus, `Explanationes in Ciceronis rhetoricam cum additamento` |
| eingefügt | `TXT0290-06` Censorinus, `De die natali` |
| eingefügt | `TXT0290-07` Pseudo-Censorinus, `Fragmentum Censorini quod vocatur` |

Prüfung: 413 Datenzeilen, 12 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs.

Audit-Datei: `materialisierung_v7-13_pal_lat_1588_aenderungen.tsv`

## v41 – Materialisierung Pal. lat. 824 / LHS0231

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-13.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-14.md`.
- Ersetzt: `TXT0252 | LHS0231 | Cassiodor | Historia tripartita`.
- Neu: `TXT0252-01 | LHS0231 | bav_pal_lat_824 | 1v-168v | Epiphanius scholasticus / Cassiodor | Historia ecclesiastica tripartita e Socrate scholastico, Sozomeno et Theodoreto collecta et e Graeco in Latinum versa | Kirchengeschichte | Geschichte | Spätantike Gelehrsamkeit`.
- Neu: `TXT0252-02 | LHS0231 | bav_pal_lat_824 | 168v | Bernardus Claraevallensis | Epistula 238 | Briefe | Kirchenpolitik / Papsttum | Mittelalterliche Gelehrsamkeit | Nachtrag; unvollständig.`
- Begründung: BL weist neben dem Haupttext auf 168v einen eigenständigen, unvollständigen Nachtrag Bernhards von Clairvaux aus. Für diesen Nachtrag wird der breite Normwert `Mittelalterliche Gelehrsamkeit` verwendet.



## v42 / Materialisierung v7-15: Pal. lat. 273 / LHS0191

Quelle: BL-Eintrag zu Vatikan, BAV, Pal. lat. 273.

- `TXT0210 | LHS0191 | Cassiodor | Variae` ersetzt durch fünf Einträge:
  - `TXT0210-01` Ps.-Ausonius, `Septem sapientium sententiae`
  - `TXT0210-02` Cassiodor, `Variae`
  - `TXT0210-03` Marbodus Redonensis, `De ornamentis verborum`
  - `TXT0210-04` Anonymus, `De Homeri centone et Eudoxia augusta`
  - `TXT0210-05` Anonymus, `Versus de terra et firmamento una cum tractatulo de ventis XII`
- Neue Einträge mit `Siegel = bav_pal_lat_273`.
- `Lorsch-Bezug = ja` beibehalten, da die Handschrift bzw. ein gleichinhaltiger Bestand in der Lorscher Überlieferung/Katalogtradition steht.


## v43 / Materialisierung v7-16 – Pal. lat. 814 / LHS0229

- `TXT0250` wurde anhand des BL-Begleittexts zu `bav_pal_lat_814` aktualisiert.
- `Siegel`: ergänzt zu `bav_pal_lat_814`.
- `Seiten`: ergänzt zu `2r-145ra`.
- `Titel`: präzisiert zu `Antiquitates Iudaicae (libb. I-XII) curis Cassiodori e Graeco versae`.
- `Bemerkungen`: ergänzt um frühe Lorscher Datierung um 800, Zugehörigkeit zur `incomplete family` der northern group, Lücken in lib. IV und IX sowie zeitweilige Ausleihe nach Fulda.
- Keine Aufspaltung vorgenommen, da BL nur eine oberste Text-/Inhaltseinheit ausweist.


## v44 / Materialisierung v7-17 – Pal. lat. 24 / LHS0132 und neue Spalte `palimpsestiert`

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-16.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-17.md`.
- Schemaänderung: neue Spalte `palimpsestiert` unmittelbar vor `Lorsch-Bezug`.
- Regel: `palimpsestiert = ja` nur dann, wenn der konkrete Texteintrag zur älteren, radierten Schrift gehört; sonst bleibt das Feld leer.
- Ersetzt: `TXT0145`, `TXT0146`, `TXT0147` zu `LHS0132`.
- Neu: `TXT0145-01` bis `TXT0145-05` für die jüngere biblische Schrift.
- Neu: `TXT0145-06` bis `TXT0145-17` für die älteren radierten Untertexte aus Seneca, Lucanus, Hyginus, griechischen medizinischen Fragmenten, Fronto, oratorischen Fragmenten, Aulus Gellius, Livius und Cicero; diese Zeilen erhalten `palimpsestiert = ja`.
- Audit-Datei: `materialisierung_v7-17_pal_lat_24_palimpsest_aenderungen.tsv`.

## v45 / Materialisierung v7-18 – Pal. lat. 1519 / LHS0257

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-17.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-18.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1519.
- Ersetzt: `TXT0281 | LHS0257 | Cicero | De natura deorum` und `TXT0282 | LHS0257 | Walahfrid Strabo | Hortulus`.
- Neu: `TXT0281-01` Cicero, `De natura deorum`, `1r-40v`.
- Neu: `TXT0281-02` Cicero, `De divinatione`, `40ar-85v`.
- Neu: `TXT0281-03` Walahfridus Strabo, `De cultura hortorum sive Hortulus`, `85va-88vb`.
- `palimpsestiert` bleibt in allen drei neuen Einträgen leer.
- Audit-Datei: `materialisierung_v7-18_pal_lat_1519_aenderungen.tsv`.

Prüfung: 433 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs.

## v46 / Materialisierung v7-19 – Pal. lat. 1513 / LHS0256

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-18.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-19.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1513.
- Aktualisiert: `TXT0280 | LHS0256 | Cicero | De finibus bonorum et malorum`.
- `Siegel` ergänzt zu `bav_pal_lat_1513`.
- `Seiten` ergänzt zu `1va-44rb`.
- `Titel` präzisiert zu `De finibus bonorum et malorum (unvollständig)`.
- `Bemerkungen` ergänzt: ältester überlieferter Textzeuge; Zugehörigkeit zur sog. deutschen Familie bzw. zu den codices meliores; Text bricht 44rb vor dem Seitenende abrupt ab; Entstehung Westdeutschland bzw. Mainz, 11. Jh.; Lorsch-Provenienz nach Bischoff/Krämer.
- Keine Aufspaltung vorgenommen, da BL nur eine oberste Text-/Inhaltseinheit ausweist.
- `palimpsestiert` bleibt leer.
- Audit-Datei: `materialisierung_v7-19_pal_lat_1513_aenderungen.tsv`.

Prüfung: 433 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs.



## v48 / Materialisierung v7-21 – Rollback der Fehlzuordnung Zürich, Ms. C 132

- `v7-20` wurde als Fehlzuordnung verworfen.
- Fehler: `Zürich, Zentralbibliothek, Ms. C 132` wurde irrtümlich `LHS0127` zugeordnet.
- Korrektur: `LHS0127` ist nach der Bischoff-Ausgangstabelle `Vat. lat. 11506`, nicht Zürich Ms. C 132.
- Wiederhergestellt aus `v7-19`:
  - `TXT0138 | LHS0127 | Cicero | De inventione`
  - `TXT0139 | LHS0127 | Priscian | Werk unbestimmt`
- Entfernt aus `LHS0127`:
  - `zbz_msc132 | Sacramentarium (Fragment)`
  - `zbz_msc132 | Cicero, Rhetorici libri qui vocantur de inventione`
  - `zbz_msc132 | Anonymus (Pseudo-Cicero), Rhetorica ad C. Herennium`
  - `zbz_msc132 | Index verborum, nominum et rerum`
- Validierung: 433 Datenzeilen, 13 Spalten, keine fehlerhaften Zeilen, keine doppelten TXT-IDs.
- Audit-Datei: `materialisierung_v7-21_rollback_zbz_msc132.tsv`.

## v49 / Materialisierung v7-22 – Pal. lat. 1756 / LHS0276

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-21.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-22.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1756.
- Ersetzt: `TXT0303 | LHS0276 | Pompeius | Commentum artis Donati`.
- Neu: `TXT0303-01` Pompeius grammaticus, `Commentum artis Donati`, `1r-157v`.
- Neu: `TXT0303-02` Anonymus (Pseudo-Cicero), `Rhetorica ad C. Herennium`, `168ra-190rb`.
- Neu: `TXT0303-03` Anonymus, `Exercitationes rhetoricae`, `190va-191vb`.
- `Lorsch-Bezug` bleibt bei allen drei Einträgen leer, da BL ausdrücklich festhält, dass fraglich ist, ob diese Handschrift oder einer ihrer Teile jemals in Lorsch war.
- `palimpsestiert` bleibt bei allen drei Einträgen leer: Faszikel II ist zwar auf palimpsestiertem Pergament geschrieben, aber die ältere radierte Schrift ist nicht als eigener Text identifiziert.
- Audit-Datei: `materialisierung_v7-22_pal_lat_1756_aenderungen.tsv`.

Prüfung: 435 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs.



## v50 – Nebenliste: nicht bei Bischoff bestätigte Lorscher Identität

- Haupttabelle bleibt: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-22.md`.
- Neu angelegt:
  - `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v1.md`
  - `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v1.tsv`
- Aufgenommen:
  - `LHS0231 / bav_pal_lat_824`, zwei Einträge, Haupttabelle v7-22, `Lorsch-Bezug` leer.
  - `LHS0276 / bav_pal_lat_1756`, drei Einträge, Haupttabelle v7-22, `Lorsch-Bezug` leer.
  - `zbz_msc132`, vier Einträge als nicht geführter außerbischofflicher Fall ohne LHS-ID.
- Grundsatz präzisiert: Schreibort Lorsch, ähnliche Inhalte oder Handschriften gleichen Inhalts begründen keine LHS-Zuordnung, solange Bischoff-/LHS-Identität nicht gesichert ist.

## v51 / Materialisierung v7-23 – Auslagerung der Nebenlisten-Einträge

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-22.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-23.md`.
- Entfernt aus der Haupttabelle:
  - `TXT0252-01 | LHS0231 | bav_pal_lat_824 | Historia ecclesiastica tripartita`.
  - `TXT0252-02 | LHS0231 | bav_pal_lat_824 | Bernardus Claraevallensis, Epistula 238`.
  - `TXT0303-01 | LHS0276 | bav_pal_lat_1756 | Pompeius grammaticus, Commentum artis Donati`.
  - `TXT0303-02 | LHS0276 | bav_pal_lat_1756 | Rhetorica ad C. Herennium`.
  - `TXT0303-03 | LHS0276 | bav_pal_lat_1756 | Exercitationes rhetoricae`.
- Neue Nebenliste: `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v2.md` und `.tsv`.
- In der Nebenliste entfällt die Spalte `Haupttabelle`.
- Audit-Datei: `materialisierung_v7-23_entfernung_nebenliste_aus_haupttabelle.tsv`.

## v52 / Materialisierung v7-24 – Pal. lat. 889 / LHS0243

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-23.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-24.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 889.
- Sichere Identität: Bischoff-Ausgangstabelle führt `LHS0243` als `Pal. lat. 889 | Sallustius | X | Lorsch | Lorsch`; BL bestätigt Entstehungsort Lorsch, ca. Mitte 10. Jh., und mehrere Lorscher Besitzvermerke.
- Ersetzt: `TXT0265 | LHS0243 | Sallust | Opera`.
- Neu: `TXT0265-01` Hymnus de oratione dominica, ungezähltes Bl. vor Bl. 1r.
- Neu: `TXT0265-02` Iuvenalis, `De Catilina, Cicerone et Mario excerpta IV ex Saturis`, ungezähltes Bl. vor Bl. 1r.
- Neu: `TXT0265-03` Anonymus, `Accessus in Sallustium`, ungezähltes Bl. vor Bl. 1v.
- Neu: `TXT0265-04` Sallustius, `De coniuratione Catilinae cum glossis`, ungezähltes Bl. vor Bl. 1v und 1r-35v.
- Neu: `TXT0265-05` Sallustius, `De bello Iugurthino`, ungezähltes Bl. vor Bl. 1v und 35v-102v.
- Neu: `TXT0265-06` Anonymus, `Translatio sanctorum Benedicti et Scholasticae in Galliam`, 102v-103v.
- `palimpsestiert` bleibt bei allen sechs Einträgen leer.
- Audit-Datei: `materialisierung_v7-24_pal_lat_889_aenderungen.tsv`.

Prüfung: 435 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal.

## v53 / Materialisierung v7-25 – Pal. lat. 492 / LHS0211

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-24.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-25.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 492.
- Sichere Identität: Bischoff-Ausgangstabelle führt `LHS0211` als `Pal. lat. 492 | Albertus de Ferrariis; Eberhardus praep. Laur. | XV | Lorsch`; BL bestätigt Provenienz Lorsch und erschließt sie aus Briefen u. Ä. des Lorscher Propstes Eberhard.
- Ersetzt: `TXT0232 | LHS0211 | Albertus de Ferrariis | Werk unbestimmt`.
- Neu: `TXT0232-01` Albertus Trottus (de Ferrariis), `De horis canonicis`, `2r-19v`.
- Neu: `TXT0232-02` Iohannes Serra, `Ars nova epistolarum`, `25v-54r`.
- Neu: `TXT0232-03` Eberhardus praepositus Laureshamensis, `Epistulae et testimonium de visitatione a. 1467-1469`, `54v-60r`.
- Neu: `TXT0232-04` Balthasar Rasinus, `Epistulae`, `61r-78r`.
- Neu: `TXT0232-05` Cicero, `Epistulae ad familiares selectae`, `79r-111r`.
- Neu: `TXT0232-06` Eberhardus praepositus Laureshamensis, `Testimonium de visitatione a. 1469`, `111v-112v`.
- Neu: `TXT0232-07` Guarinus Veronensis und andere, `Epistulae et orationes`, `115r-213v`.
- Neu: `TXT0232-08` Homerus Latinus (Baebius Italicus ?), `Ilias Latina`, `215r-233v`.
- `palimpsestiert` bleibt bei allen acht Einträgen leer.
- Audit-Datei: `materialisierung_v7-25_pal_lat_492_aenderungen.tsv`.

Prüfung: 442 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal.



## v54 / Materialisierung v7-26 – Pal. lat. 1741 in Nebenliste ausgelagert

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-25.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-26.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1741.
- Befund: BL nennt Provenienz `Lorsch (?) (LEHMANN 1911); Heidelberg`; der Laurissano-Hinweis betrifft den von Sichardus überlieferten Terentius-Scaurus-Text, nicht die gesicherte Lorscher Identität der gesamten Sammelhandschrift.
- Entfernt aus der Haupttabelle: `TXT0299 | LHS0272 | Terentius Scaurus | Werk unbestimmt`.
- Neue Nebenliste: `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v3.md` und `.tsv`.
- In der Nebenliste ergänzt: 17 oberste BL-Inhaltseinheiten `TXT0299-01` bis `TXT0299-17` zu Pal. lat. 1741.
- Audit-Datei: `materialisierung_v7-26_pal_lat_1741_nebenliste.tsv`.

Prüfung: 441 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal. Nebenliste: 26 Einträge.


## v55 – Nebenliste v4: Häse 328 zu `Commentum artis Donati`

- Haupttabelle bleibt unverändert: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-26.md`.
- Neue Nebenliste: `lorsch_nebenliste_nicht_bischoff_bestaetigte_lorsch_identitaet_v4.md` und `.tsv`.
- Geändert: `TXT0303-01 | LHS0276 | bav_pal_lat_1756 | Pompeius grammaticus | Commentum artis Donati`.
- Ergänzung im Feld `Unsicherheitsgrund`: Nach BL ist in den karolingischen Lorscher Bibliothekskatalogen laut HÄSE 2002, Nr. 328, eine Handschrift gleichen Inhalts belegt.
- Interpretation: Textbestandsparallele, aber keine gesicherte Identität von Pal. lat. 1756 mit einem Lorscher Codex; deshalb bleibt der Eintrag in der Nebenliste und nicht in der Haupttabelle.
- Audit-Datei: `nebenliste_v4_commentum_artis_donati_haese328.tsv`.

## v56 / Materialisierung v7-27 – Pal. lat. 1753 / LHS0274

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-26.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-27.md`.
- Quelle: BL-Begleittext zu Vatikan, BAV, Pal. lat. 1753.
- Sichere Identität: Bischoff-Ausgangstabelle führt `LHS0274` als `Pal. lat. 1753 | Marius Victorinus, Gramm., etc. | VIII/IX | Lorsch`; BL bestätigt Entstehungsort Lorsch, um 800, Älterer Lorscher Stil, Provenienz Lorsch und HÄSE 2002, Nr. 334.
- Ersetzt: `TXT0301 | LHS0274 | Marius Victorinus | Ars grammatica`.
- Neu: 13 Einträge `TXT0301-01` bis `TXT0301-13` nach den obersten BL-Inhaltseinheiten.
- `palimpsestiert` bleibt bei allen neuen Einträgen leer.
- Audit-Datei: `materialisierung_v7-27_pal_lat_1753_aenderungen.tsv`.

Prüfung: 453 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal.



## In v7-28 materialisierte Änderungen

**Neue Tabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-28.md`  
**Ausgangstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-27.md`

| ID | Datei | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-154 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-28.md` | `LHS0013 / TXT0014 / Magnus Felix Ennodius / Epistulae` nach BL zu `kbr_ms9845-48` ersetzt. | 1 Altzeile |
| UM-155 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-28.md` | Ennodius-Hauptbestand als `TXT0014-01 / Opera omnia` erfasst; Nachtrag `Officium in natale XI milium virginum` als `TXT0014-02` ergänzt. | 2 Neuzeilen |

Die Haupttabelle enthält damit 454 Datenzeilen. Die Spalte `palimpsestiert` bleibt unverändert bei 12 Markierungen.


## v58 / Materialisierung v7-29 – Bereinigung `Sammlung` in der Buchgattung

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-28.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-29.md`.
- Anlass: `Sammlung` ist keine tragfähige Buchgattung, sondern beschreibt nur einen Sammel- bzw. Überlieferungszustand.
- `LHS0013 / TXT0014 / kbr_ms9845-48`: Die v7-28-Zeilen `TXT0014-01` und `TXT0014-02` wurden durch 14 gattungsfähige Einträge ersetzt.
- Neu gegliedert: Ennodius `Epistularum libri IX`, `Dictiones 28`, `Carminum et hymnorum libri II` sowie die zehn `Opuscula` und der Nachtrag `Officium in natale XI milium virginum`.
- Zusätzlich wurden ältere Buchgattungswerte mit `Sammlung` oder `Sammelhandschrift` bereinigt: `Sammlung`, `Kanonistische Sammlung`, `Kanonessammlung`, `Hagiographische Sammlung`, `Inschriftensammlung`, `Biographiensammlung`, `Sammelhandschrift`.
- Audit-Datei: `materialisierung_v7-29_sammlung_buchgattung_normierung.tsv`.

Prüfung: 466 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal. In der Spalte `Buchgattung` kommt `Sammlung` oder `Sammelhandschrift` nicht mehr vor.


---

## In v7-30 materialisierte Änderungen

**Neue Tabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-30.md`  
**Ausgangstabelle:** `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-29.md`  
**Auditdatei:** `materialisierung_v7-30_pal_lat_1449_aenderungen.tsv`

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-30-001 | `LHS0255 / Pal. lat. 1449` | Alte Platzhalter `TXT0278` und `TXT0279` entfernt. | 2 Zeilen |
| UM-v7-30-002 | `LHS0255 / Pal. lat. 1449` | BL-Inhaltseinheiten als `TXT0278-01` bis `TXT0278-20` neu eingefügt. | 20 Zeilen |
| UM-v7-30-003 | Klassifikation | Sammelcharakter nicht als `Buchgattung`; konkrete Gattungen `Fachtext`, `Briefe`, `Dichtung`, `Chronik` verwendet. | 20 Zeilen |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 484 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


## v60 / Materialisierung v7-31 – Normierung `Iatromathematik`

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-30.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-31.md`.
- Geändert: `TXT0278-20 / LHS0255 / Sphaera Pythagorae philosophi quam Apologius descripsit`.
- Vorher: `Untergattung = Iatromathematik`, `Thema = Medizin`, `Überlieferungslinie = Astrologische Tradition`.
- Nachher: `Untergattung = Prognostik`, `Thema = Medizinische Astrologie`, `Überlieferungslinie = Frühmittelalterliche Gelehrsamkeit`.
- `Iatromathematik` bleibt nur erklärend in `Bemerkungen`.
- Audit-Datei: `materialisierung_v7-31_iatromathematik_normierung.tsv`.

Prüfung: 484 Datenzeilen, 13 Spalten, keine fehlerhaften Tabellenzeilen, keine doppelten TXT-IDs, `palimpsestiert = ja` 12-mal.


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


## v62 / Materialisierung v7-33 – Pal. lat. 169

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-32.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-33.md`.
- Audit-Datei: `materialisierung_v7-33_pal_lat_169_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-33-001 | `LHS0142 / Pal. lat. 169` | `Ambrosiaster`-Eintrag mit BL-Siegel, Seiten, genauerem Titel und Interpolationsbemerkung aktualisiert. | 1 Zeile |
| UM-v7-33-002 | `LHS0143 / Pal. lat. 169` | `Mönchsliste` als `Nomina Laureshamensis monasterii fratrum` mit Seitenangabe und normalisierter Klassifikation aktualisiert. | 1 Zeile |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 485 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |


## v63 / Materialisierung v7-34 – Graz, UB, Ms. 1703/124

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-33.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-34.md`.
- Audit-Datei: `materialisierung_v7-34_ubg_ms1703_124_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-34-001 | `LHS0028 / Graz, UB, Ms. 1703/124` | `Priscianus`-Eintrag mit BL-Siegel, Seiten, Fragmenttitel und genauer Bemerkung aktualisiert. | 1 Zeile |
| UM-v7-34-002 | Klassifikation | Nach Artes-Regel v7-32 geführt: `Fachtext / Artes liberales / Grammatik / Spätantike Gelehrsamkeit`. | 1 Zeile |

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

## v64 / Materialisierung v7-35 – Zürich, Zentralbibliothek, Ms. Car. C 131

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-34.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-35.md`.
- Audit-Datei: `materialisierung_v7-35_zbz_mscarc131_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-35-001 | `LHS0317 / Zürich, Zentralbibliothek, Ms. Car. C 131` | `Didymus Alexandrinus`-Eintrag mit BL-Siegel, Seiten, präzisem Titel und Bemerkung zur Hieronymus-Übersetzung aktualisiert. | 1 Zeile |
| UM-v7-35-002 | Klassifikation | Bestehende Klassifikation `Fachtext / Traktat / Dogmatik / Griechische Patristik` bestätigt; Übersetzungsbefund nicht als eigene Zeile abgespalten. | 1 Zeile |

### Validierung

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
| UM-v7-36-002 | Klassifikation | `Retractationes II,4,30` werden wegen Benutzerentscheidung in `Bemerkungen` festgehalten und nicht als eigene Textzeile geführt. | 1 Zeile |

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
- Audit-Datei: `materialisierung_v7-37_pal_lat_886_1578_1579_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-37-001 | `LHS0240 / Pal. lat. 886, Bll. 125-164` | Macrobius- und Historia-Augusta-Exzerpte mit BL-Siegel, Seiten, Faszikelangaben, HÄSE-Bezug Nr. 320 und präzisierten Klassifikationen aktualisiert. | 2 Zeilen |
| UM-v7-37-002 | `LHS0241 / Pal. lat. 886, Bll. 165-189` | Fulgentius, `De aetatibus mundi et hominis`, mit BL-Siegel, Seiten, Abbruchbefund und HÄSE-Bezug Nr. 72 aktualisiert. | 1 Zeile |
| UM-v7-37-003 | `LHS0260 / Pal. lat. 1578` | Der bisherige Fulgentius-Mythologiae-Platzhalter wurde nach BL in drei Textzeilen aufgespalten: `Mythologiae`, `Expositio sermonum antiquorum`, `Expositio Virgilianae continentiae`. | 1 → 3 Zeilen |
| UM-v7-37-004 | `LHS0261 / Pal. lat. 1579, Bll. 1-15` | Fulgentius, `Expositio Virgilianae continentiae`, mit BL-Siegel, Seiten und Bemerkung zu Textklasse/Korrekturen aktualisiert. | 1 Zeile |
| UM-v7-37-005 | `LHS0262 / Pal. lat. 1579, Bl. 16` | Gregorius-Magnus-Nachtrag als `Dialogorum ex libro II excerptum`, 16r, mit Nachtragsbefund einer Lorscher Hand des 10. Jh. aktualisiert. | 1 Zeile |
| UM-v7-37-006 | Klassifikation | Allegorese bleibt bei Fulgentius in `Bemerkungen`; sie wird nicht als `Untergattung` verwendet. `Expositio sermonum antiquorum` wird als lexikographischer Fachtext geführt. | 6 betroffene Ausgangszeilen |

### Validierung

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
- Audit-Datei: `materialisierung_v7-38_pal_lat_200_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-38-001 | `LHS0157 / Pal. lat. 200` | Der bisherige Einzelplatzhalter `TXT0175 / Augustinus, De civitate Dei` wurde nach BL in Haupttext und liturgischen Nachtrag aufgespalten. | 1 → 2 Zeilen |
| UM-v7-38-002 | `TXT0175-01` | Augustinus, `De civitate Dei (libb. XVIII-XXII)`, mit BL-Siegel, Seiten, Capitula-Befund, Donadeus-Kolophon, Besitzvermerk und HÄSE-Bezug Nr. 80 aktualisiert. | 1 Zeile |
| UM-v7-38-003 | `TXT0175-02` | Nachtrag `Lectio officii in sabbato sancto ad matutinum` als liturgische Offiziumslektion des 12. Jh. mit Neumen aufgenommen. | 1 Zeile |
| UM-v7-38-004 | Klassifikation | Capitula/Breviculus nicht abgespalten; die Karsamstagslektion wird als `Liturgischer Text / Offiziumslektion` geführt, nicht als `Liturgisches Buch`. | 2 Zeilen |

### Validierung

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
- Audit-Datei: `materialisierung_v7-39_blb_augperg105_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-39-001 | `LHS0036 / Karlsruhe, BLB, Aug. perg. 105` | Der bisherige Einzelplatzhalter `TXT0040 / Hieronymus, Epistulae` wurde nach BL in einen Hieronymus-Haupteintrag und separate Isidor- und Damasus-Einträge aufgespalten. | 1 → 4 Zeilen |
| UM-v7-39-002 | `TXT0040-01` | Hieronymus-Hauptbestand als `Hieronymi epistulae et opuscula` mit BL-Siegel, Seiten und Bemerkung zu Nachtrag aus `Adversus Rufinum`, `Adversus Helvidium`, `Contra Vigilantium` und weiteren Stücken aktualisiert. | 1 Zeile |
| UM-v7-39-003 | `TXT0040-02` | Isidor von Sevilla, `De differentiis rerum sive Differentiae theologicae vel spiritales (Auszug)`, 3r/v, als eigener Nachtrag aufgenommen. | 1 Zeile |
| UM-v7-39-004 | `TXT0040-03` | Damasus papa, `Epistula ad Hieronymum (ep. 8 = Hier. ep. 19)`, 41v und 47rb/va, als ein Text mit Wiederholung dokumentiert. | 1 Zeile |
| UM-v7-39-005 | `TXT0040-04` | Damasus papa, `Epistula ad Hieronymum (ep. 9 = Hier. ep. 35)`, 46va-47rb, separat aufgenommen. | 1 Zeile |
| UM-v7-39-006 | Klassifikation | Isidor nach Projektregel nicht als `Lateinische Patristik`, sondern als `Spätantike Gelehrsamkeit`; Damasus-Briefe als `Lateinische Patristik`. | 3 neue Autorenzeilen |

### Validierung

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
- Audit-Datei: `materialisierung_v7-40_pal_lat_829_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-40-001 | `LHS0233 / Pal. lat. 829` | Der bisherige Einzelplatzhalter `TXT0254 / Orosius, Historiae adversus paganos` wurde nach BL in Haupttext, Ps.-Sulpicius-Severus-Briefe und T-O-Weltkarte aufgespalten. | 1 → 3 Zeilen |
| UM-v7-40-002 | `TXT0254-01` | Orosius, `Historiae adversum paganos (unvollständig)`, mit BL-Siegel, Seiten, Verlustbefund, Fehlbindung von Bl. 93, Schriftbefund, althochdeutscher Glosse und HÄSE-Bezug Nr. 64 aktualisiert. | 1 Zeile |
| UM-v7-40-003 | `TXT0254-02` | Ps.-Sulpicius Severus, `Epistulae`, 113r-115r, als eigener Briefbestand aufgenommen; ep. 7 als Ps.-Pelagius in den Bemerkungen dokumentiert. | 1 Zeile |
| UM-v7-40-004 | `TXT0254-03` | Anonymus, `Tabula circularis orbis terrae`, 115v, als kosmographischer Nachtrag aufgenommen. | 1 Zeile |
| UM-v7-40-005 | Klassifikation | Die T-O-Weltkarte wird nicht als Geschichtswerk, sondern als `Fachtext / Kosmographie / Geographie / Mittelalterliche Gelehrsamkeit` geführt. | 1 Zeile |

### Validierung

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
- Audit-Datei: `materialisierung_v7-41_pal_lat_1635_1646_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-41-001 | `LHS0266 / Pal. lat. 1635` | `TXT0292 / Vergil, Opera` wurde nach BL in `Eclogae sive Bucolica`, `Georgica` und `Aeneis` jeweils mit Servius-Glossen und ggf. metrischen Argumenta aufgespalten. | 1 → 3 Zeilen |
| UM-v7-41-002 | `TXT0293 / LHS0266` | `(Ps.-)Seneca philosophus, Tragoediae cum argumentis et glossis`, 284r-486r, mit pseudo-senecanischen Stücken in den Bemerkungen präzisiert. | 1 Zeile |
| UM-v7-41-003 | `LHS0267 / Pal. lat. 1646` | `TXT0294 / Servius, Commentarius in Vergilium` wurde nach BL in Servius-Haupttext und zwei Nachträge aufgespalten. | 1 → 3 Zeilen |
| UM-v7-41-004 | `TXT0294-01` | Servius als `Fachtext / Artes liberales / Grammatik / Spätantike Gelehrsamkeit` klassifiziert; Kommentarform bleibt im Titel und in den Bemerkungen. | 1 Zeile |
| UM-v7-41-005 | `TXT0294-02` | Anonymus, `Versus de ortu mundi`, als kosmologisches Lehrgedicht aufgenommen. | 1 Zeile |
| UM-v7-41-006 | `TXT0294-03` | Anonymus, `Passio cuiusdam monachi secundum luxuriam`, als parodistischer Nachtrag aufgenommen. | 1 Zeile |

### Validierung

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
- Audit-Datei: `materialisierung_v7-42_pal_lat_46_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-42-001 | `LHS0133 / Pal. lat. 46` | Der bisherige Platzhalter `TXT0148 / Evangelia` wurde nach BL in sechs Einheiten aufgespalten: zwei Hieronymus-Prologe, Kanontafeln, pseudo-hieronymisches Argumentum, Evangelia IV und Capitulare evangeliorum. | 1 → 6 Zeilen |
| UM-v7-42-002 | `TXT0148-01` | Hieronymus, `Praefatio in evangelio (Novum opus)`, 1r-3r, als biblischer Prolog aufgenommen. | 1 Zeile |
| UM-v7-42-003 | `TXT0148-02` | Hieronymus, `Commentarius in Mattheum, Praefatio (Auszug; Plures fuisse)`, 3r-4v, als biblischer Prolog aufgenommen. | 1 Zeile |
| UM-v7-42-004 | `TXT0148-03` | Anonymus, `Canones evangeliorum`, 4v/5r-9r, als `Bibelexegese / Kanontafeln / Evangelienharmonie` klassifiziert. | 1 Zeile |
| UM-v7-42-005 | `TXT0148-04` | Ps.-Hieronymus, `Argumentum in canones evangeliorum (Sciendum tamen)`, 9v, separat vom Kanontafelblock erfasst. | 1 Zeile |
| UM-v7-42-006 | `TXT0148-05` | `Evangelia IV cum argumentis ac capitulis`, 10r-137v, als eigentlicher Bibeltext geführt; Textverluste und Jonathan-Kolophon in den Bemerkungen dokumentiert. | 1 Zeile |
| UM-v7-42-007 | `TXT0148-06` | `Capitulare evangeliorum`, 137v-149r, als liturgischer Gebrauchstext aufgenommen. | 1 Zeile |
| UM-v7-42-008 | Lorsch-Bezug | Lorsch-Bezug bleibt `ja`, aber die Unsicherheit wird in den Bemerkungen festgehalten: Entstehungsraum nicht sicher Lorsch, Provenienz `Lorsch (?)`, Katalogverweise HÄSE 2002, Nr. 15-18, wahrscheinliche Lorscher Korrekturen im 9. Jh., später Frankenthal. | 6 Zeilen |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 501 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |



## Umsetzung v7-43: Leiden, UB, BPL 36 / LHS0041

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-42.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-43.md`.
- Audit-Datei: `materialisierung_v7-43_ublei_bpl36_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-43-001 | `LHS0041 / Leiden, UB, BPL 36` | Der bisherige Platzhalter `TXT0047 / Martianus Capella / De nuptiis Philologiae et Mercurii` wurde nach BL in Martianus-Haupttext mit Glossen und Lupus-Nachtrag aufgespalten. | 1 → 2 Zeilen |
| UM-v7-43-002 | `TXT0047-01` | Martianus Capella, `De nuptiis Philologiae et Mercurii cum glossis`, 1r-129v, als `Fachtext / Artes liberales / Sieben freie Künste` geführt. | 1 Zeile |
| UM-v7-43-003 | `TXT0047-02` | Lupus Ferrariensis, `Epistula respondens ad quaestionem: Quid sit ceroma (ep. add. 6)`, 130r, als gelehrter Briefeintrag mit Thema `Worterklärung` aufgenommen. | 1 Zeile |
| UM-v7-43-004 | Nichtaufnahme | Das Fragment Gregorius Magnus, `Moralia sive Expositio in Iob`, 131ra-vb, wurde nicht in die Haupttabelle aufgenommen, da BL es als Nachstoßblatt aus Frankreich (?) des 12. Jh. beschreibt und kein gesicherter Lorscher Textbestand vorliegt. | 0 Zeilen |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 502 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

---

## v73 / Materialisierung v7-44 – Pal. lat. 1877

- Ausgangstabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-43.md`.
- Neue Tabelle: `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v7-44.md`.
- BL-Grundlage: `bav_pal_lat_1877.pdf`.
- Audit-Datei: `materialisierung_v7-44_pal_lat_1877_aenderungen.tsv`.

| ID | Bereich | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-v7-44-001 | `LHS0279 / Pal. lat. 1877, Bll. 1-34` | `TXT0306` wurde als `Catalogus codicum monasterii Laureshamensis (HÄSE C)` präzisiert; Gerward-Bücherliste in den Bemerkungen dokumentiert. | 1 Zeile |
| UM-v7-44-002 | `LHS0280 / Pal. lat. 1877, Bll. 44-66` | `TXT0307` wurde als `Catalogus codicum monasterii Laureshamensis (HÄSE B) (unvollständig)` präzisiert; Lokalisierungsunsicherheit in den Bemerkungen dokumentiert. | 1 Zeile |
| UM-v7-44-003 | `LHS0281 / Pal. lat. 1877, Bll. 67-79` | `TXT0308` wurde als `Catalogus codicum monasterii Laureshamensis (HÄSE A) (unvollständig)` präzisiert. | 1 Zeile |
| UM-v7-44-004 | `Faszikel II / Bll. 35-43` | Fuldaer Bibliothekskatalog nicht in die Haupttabelle aufgenommen, da BL Entstehungsort und Provenienz Fulda nennt und Lorsch nur unsicher bleibt. | 0 Zeilen |

### Validierung

| Kennzahl | Wert |
| --- | ---: |
| Datenzeilen | 502 |
| Spalten | 13 |
| fehlerhafte Tabellenzeilen | 0 |
| doppelte TXT-IDs | 0 |
| `palimpsestiert = ja` | 12 |
| `Sammlung` / `Sammelhandschrift` in `Buchgattung` | 0 |

