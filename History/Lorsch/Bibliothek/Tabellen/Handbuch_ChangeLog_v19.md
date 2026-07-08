# Änderungsprotokoll zum Handbuch der Lorsch-Forschungstabelle

**Version:** ChangeLog_v19  
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
