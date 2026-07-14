# Änderungsprotokoll zum Handbuch der Lorsch-Forschungstabelle

**Version:** ChangeLog_v5  
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
| HB-012 | Buchgattung / Sub-Gattung | undifferenzierte `Lehrschrift` | `Lehrschrift` plus fachliche `Sub-Gattung` | `Lehrschrift` bezeichnet die didaktische Form. Fachliche Spezialisierung erfolgt über `Sub-Gattung`, z. B. `Arithmetik`, `Computus`, `Liturgik`, `Theologische Lehrschrift`, `Eucharistietheologie`. | noch nicht umgesetzt |
| HB-013 | Buchgattung | mögliche Einführung `Theologie` | keine Buchgattung `Theologie` | `Theologie` wird nicht als Buchgattung eingeführt; theologische Inhalte werden über `Sub-Gattung`, `Thema` und `Überlieferungslinie` erfasst. | keine Tabellenänderung, soweit nicht verwendet |
| HB-014 | Buchgattung | `Homiliensammlung`; ggf. `Homilie` | `Homilien` | `Homiliensammlung` wird nicht als eigener Normbegriff fortgeführt. `Homilien` genügt vorläufig für Einzelhomilien und Sammlungen; ein möglicher `Homiliar`-Sonderfall wird nur bei sicher liturgisch geordnetem Gebrauchsbuch später geprüft. | noch nicht umgesetzt |

## Offene Redaktionsfragen

- Ob ein ausdrücklich liturgisch geordnetes Homilienbuch später als `Liturgisches Buch` mit `Sub-Gattung = Homiliar` geführt werden soll, bleibt offen; `Homiliensammlung` wird jedoch nicht als eigener Normwert fortgeführt.
- Ob `Psalmenkommentar` als Sonderfall von `Bibelkommentar` erhalten bleiben soll oder später zu `Bibelkommentar` normiert wird.
- Ob `Bibelbezogene Quaestionen` als eigene Gattung erhalten bleibt oder zu `Bibelexegese` gezogen wird.
- Weitere Befüllung der Spalte `Sub-Gattung` außerhalb der biblischen Primärtexte erst nach gesonderter Normierungsentscheidung.
- Konkrete Zuordnung der bisherigen `Lehrschrift`-Einträge zu Sub-Gattungen (`Arithmetik`, `Computus`, `Liturgik`, `Theologische Lehrschrift` usw.) noch prüfen.
- Ob Spezialformen liturgischer Gebrauchsbücher langfristig als eigene Buchgattungen stehen bleiben oder als `Sub-Gattung` unter `Liturgisches Buch` geführt werden, bleibt offen.

## In v6-1 materialisierte Änderungen

| ID | Datei | Änderung | Umfang |
| --- | --- | --- | ---: |
| UM-001 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | Spalte `Sub-Gattung` direkt nach `Buchgattung` eingefügt. | 404 Tabellenzeilen |
| UM-002 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Evangelienbuch` von `Buchgattung` nach `Sub-Gattung` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 14 Zeilen |
| UM-003 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Evangelistar` bzw. als `Perikopenbuch` geführte Evangelistare nach `Sub-Gattung = Evangelistar` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 5 Zeilen |
| UM-004 | `lorsch-forschung_gesamttabelle_102-135_arbeitsstand_v6-1.md` | `Bibel mit Glosse` von `Buchgattung` nach `Sub-Gattung` verschoben; `Buchgattung` auf `Bibeltext` gesetzt. | 2 Zeilen |

Nicht umgesetzt in `v6-1`: die weitere Homogenisierung der biblischen Auslegungstexte (`Bibelauslegung` → `Bibelexegese`, Slash-Formen bei `Bibelglossen`/`Bibelkommentar` usw.). Diese bleibt als offener Redaktionsblock im Protokoll stehen.
