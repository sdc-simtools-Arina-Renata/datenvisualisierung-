# Überversorgung auf dem Papier – eingeschränkter Zugang in der Realität
## Eine datenbasierte Analyse der psychotherapeutischen Versorgung in Nordbayern

### Methodische Dokumentation

**Arina Rukina**  
**Renata Figueroa**  
Visualisierung / Technische Hochschule Nürnberg – Ohm / WS 25/26

---

## 1. Einleitung

Die psychotherapeutische Versorgung in Deutschland wird offiziell anhand des sogenannten Versorgungsgrades bewertet. Diese Kennzahl bildet die Grundlage der Bedarfsplanung und entscheidet darüber, wo neue Kassensitze geschaffen werden dürfen. In vielen urbanen Regionen, insbesondere in Städten, weist der Versorgungsgrad eine sogenannte Überversorgung aus. Gleichzeitig berichten Betroffene von monatelangen Wartezeiten auf einem Therapieplatz, auch in genau diesen Regionen.

Diese Diskrepanz wirft die Frage auf, inwieweit die offizielle Statistik die tatsächliche Versorgungssituation widerspiegelt. Die vorliegende Arbeit untersucht diesen Widerspruch anhand einer datenbasierten Visualisierungsanalyse für Nordbayern. Ziel ist es nicht, einzelne Regionen normativ zu bewerten, sondern transparent darzustellen, wie unterschiedliche Kennzahlen zu unterschiedlichen Aussagen über Versorgung führen.

Der Schwerpunkt dieser Arbeit liegt auf der methodischen Herleitung der Visualisierungen: von den Rohdaten über die Datenaufbereitung bis zur finalen kartografischen Darstellung. Die Analyse folgt einem reproduzierbaren Vorgehen, sodass die Ergebnisse nachvollzogen und überprüft werden können.

---

## 2. Zielsetzung

Ziel dieser Arbeit ist es, anhand reproduzierbarer Datenverarbeitung und kartografischer Visualisierung zu zeigen, dass die offiziell ausgewiesene „Überversorgung“ in der psychotherapeutischen Versorgung nicht zwangsläufig mit der realen Zugänglichkeit für Patient:innen übereinstimmt.

Im Mittelpunkt steht dabei nicht die Bewertung einzelner Regionen, sondern die methodische Frage, wie unterschiedliche Kennzahlen, insbesondere der Versorgungsgrad und die Wartezeiten, unterschiedliche Perspektiven auf Versorgung eröffnen.

**Die zentrale Forschungsfrage lautet:**

Wie unterscheiden sich offizielle Versorgungskennzahlen von realen Zugangsindikatoren, und inwiefern lassen sich diese Unterschiede datenbasiert und räumlich sichtbar machen?

---

## 3. Festlegung des Analyse- und Untersuchungsraums

### 3.1 Definition der räumlichen Abgrenzung – Geodaten
Zu Beginn wurde der Untersuchungsraum eindeutig festgelegt. 
Als kartografische Basis dienten die digitalen Geometriedaten VG250 (Verwaltungsgebiete 1:250.000) des Bundesamtes für Kartographie und Geodäsie (BKG). 
Der Datensatz wurde auf den gesamten Untersuchungsraum Nordbayern (Regierungsbezirke):
- Oberfranken 
- Mittelfranken
- Unterfranken
- Oberpfalz 
zugeschnitten.

Diese Abgrenzung ist fachlich sinnvoll, da sie sowohl urbane Zentren als auch ländlich geprägte Regionen umfasst und damit strukturelle Unterschiede sichtbar macht.

Als räumliche Analyseeinheit wurden Landkreise und kreisfreie Städte gewählt. Diese Ebene stellt einen Kompromiss zwischen Detailtiefe und Vergleichbarkeit dar und entspricht zudem der Aggregationsebene der meisten verfügbaren Versorgungsdaten.

---

### 3.2 Bevölkerungsdaten (INKAR)
Aus dem INKAR-Datensatz wurden ausschließlich Merkmale ausgewählt, die für die Berechnung der Bevölkerungsdichte notwendig sind. Ziel war es, einen möglichst einfachen und transparenten Nachfrageindikator zu verwenden.

Ausgewählte Variablen:
	•	Einwohnerzahl
	•	Fläche in Quadratkilometern
	•	Kreisschlüssel (Amtlicher Gemeindeschlüssel, AGS)
Die Daten lagen im CSV-Format vor und beziehen sich auf die Verwaltungsebene der Landkreise und kreisfreien Städte.

---

### 3.4 Wartezeiten- und Versorgungsdaten (KBV)
Die versorgungsrelevanten Daten wurden aus den Veröffentlichungen und Statistiken der Kassenärztlichen Bundesvereinigung (KBV) bezogen. Dieser Datensatz ist zentral für die Untersuchung, da er die offizielle administrative Sicht der Realität des Versorgungsalltags gegenüberstellt.
Zentrale Komponenten des Datensatzes:

- Der Versorgungsgrad: Diese Kennzahl gibt das Verhältnis zwischen der Anzahl der niedergelassenen Psychotherapeut:innen mit Kassenzulassung und der gesetzlich festgelegten Einwohnerzahl pro Sitz an. Er bildet die rechtliche Grundlage für die Bedarfsplanung und Zulassungsbeschränkungen.

- Wartezeiten bis zum Erstgespräch/Behandlungsbeginn: Ergänzend zum Versorgungsgrad wurden Daten zu den tatsächlichen Wartezeiten erhoben. Diese dienen als „Realitätsindikator“, da sie den praktischen Zugang zur Versorgung aus Patient:innensicht messen.

---

### 3.5 Zeitliche Einordnung und Belastbarkeit der Daten
Bei der Zusammenführung der Datensätze ergeben sich unterschiedliche Zeitstände (2021 bis 2025). Diese methodische Entscheidung wurde bewusst getroffen und lässt sich wie folgt begründen:

- Versorgungsgrad (2025): Hier wurden die aktuellsten verfügbaren Daten der KBV verwendet. Da diese Kennzahl die rechtliche Grundlage für die Bedarfsplanung bildet, ist ihre Aktualität entscheidend für die Analyse der gegenwärtigen Systemlogik.

- Bevölkerungsdichte (2023): Dies ist der aktuellste verfügbare Stand aus dem INKAR-Datensatz zum Zeitpunkt der Analyse. Da sich die Bevölkerungsstruktur und -dichte auf Kreisebene über kurze Zeiträume (2–3 Jahre) nur marginal verändern, bleibt die Aussagekraft als Indikator für die regionale Nachfrage voll erhalten.

- Wartezeiten (2021): Diese Daten stellen den aktuellsten verfügbaren, vollständigen Datensatz für ganz Nordbayern dar. Obwohl die Daten von 2021 stammen, behalten sie ihre Relevanz für die aktuelle Analyse. Fachberichte der BPtK (Bundespsychotherapeutenkammer) und aktuelle Studien zeigen, dass sich die Wartezeitensituation seit 2021 nicht verbessert hat, sondern durch die Nachwirkungen der Corona-Pandemie und den Fachkräftemangel sogar verschärft wurde.

Die zeitliche Diskrepanz zwischen 2021 und 2025 führt nicht zu einer Verzerrung, sondern bildet eher eine „konservative Schätzung“ ab. Es ist davon auszugehen, dass die reale Diskrepanz zwischen dem offiziellen Versorgungsgrad (2025) und der tatsächlichen Wartezeit heute noch größer ist, als es die Daten von 2021 visualisieren können.


---

## 4. Datengrundlage

### 4.1 Bevölkerungsdaten (INKAR)
Die Bevölkerungsdaten stammen aus dem INKAR-Datensatz (Indikatoren und Karten zur Raum- und Stadtentwicklung). Sie enthalten Angaben zur Einwohnerzahl und zur Fläche auf Kreisebene. Diese Daten werden genutzt, um die Bevölkerungsdichte zu berechnen, die als Annäherung an die räumliche Nachfrage nach psychotherapeutischer Versorgung dient.

Relevante Merkmale:

- Verwaltungsebene: Landkreise und kreisfreie Städte
- Format: CSV
- Variablen: Einwohnerzahl, Fläche in Quadratkilometern, Kreisschlüssel (AGS)

---

### 4.2 Versorgungsgrad Psychotherapie
Der Versorgungsgrad ist eine offizielle Kennzahl der Kassenärztlichen Bundesvereinigung (KBV). Er beschreibt das Verhältnis zwischen vorhandenen Kassensitzen und dem rechnerisch ermittelten Bedarf. Die Berechnungslogik basiert auf bundesweit einheitlichen Richtwerten der Bedarfsplanung.

Die Klassifizierung erfolgt nach festgelegten Schwellenwerten:

- unter 90 %: Unterversorgung
- 90–110 %: Regelversorgung
- über 110 %: Überversorgung

Diese Kennzahl bildet die Grundlage für politische und administrative Entscheidungen zur Zulassung neuer Praxen.

---

### 4.3 Wartezeiten auf einen Psychotherapieplatz
Die Wartezeiten auf einen Therapieplatz wurden aus öffentlich zugänglichen Quellen der KBV sowie ergänzender Recherche zusammengetragen und in einer CSV-Datei konsolidiert. Sie geben an, wie viele Tage Patient:innen durchschnittlich auf den Beginn einer psychotherapeutischen Behandlung warten müssen. Die Wartezeiten stellen kein vollständiges Abbild aller individuellen Erfahrungen dar, dienen jedoch als aggregierter Indikator für den realen Zugang zur Versorgung.

Merkmale:
- Maßeinheit: Tage
- Statistische Grundlage: Median (auf Kreisebene)
- Zweck: Abbildung des tatsächlichen Zugangs zur Versorgung

Die Wartezeiten dienen in dieser Arbeit als Realitätsindikator, da sie unmittelbar die Erfahrung der Betroffenen widerspiegeln.

---

## 5. Datenaufbereitung
Alle Datensätze wurden auf die gleiche räumliche Ebene (Landkreise und kreisfreie Städte) gebracht und über den amtlichen Kreisschlüssel zusammengeführt. Dieser Schritt stellt sicher, dass alle Kennzahlen für exakt dieselben geografischen Einheiten vorliegen und somit eine direkte räumliche Korrelation möglich ist.

Methodische Qualitätssicherung:
- Vollständigkeit der Daten: Die Analyse konnte auf Basis lückenloser Datensätze für den gesamten Untersuchungsraum Nordbayern durchgeführt werden. Da keine fehlenden Werte auftraten, ist eine flächendeckende und repräsentative Darstellung der Versorgungslage gewährleistet.

- Datenintegrität: Durch die Verwendung vollständiger Primärdaten der KBV und des INKAR-Datensatzes waren weder Schätzungen noch statistische Interpolationen (Imputationen) erforderlich. Dies garantiert eine unverfälschte Abbildung der Realität.


---

## 6. Visualisierungskonzept

### 6.1 Visualisierung 1: Bevölkerungsdichte – Wo sind die Menschen?
Die erste Karte zeigt die Bevölkerungsdichte in Nordbayern. Sie stellt dar, wo viele Menschen leben und wo entsprechend eine höhere potenzielle Nachfrage nach psychotherapeutischer Versorgung besteht.

Die Darstellung erfolgt als Choroplethenkarte mit einer Gelb-Roten Farbskala, bei der dunklere Rottöne eine höhere Bevölkerungsdichte anzeigen. Urban geprägte Regionen werden dadurch als räumliche Konzentrationen deutlich sichtbar. Städte wie Nürnberg, Fürth, Erlangen, Regensburg und Würzburg treten als Ballungsräume klar hervor.

Die Farbskala dient der rein quantitativen Darstellung der Bevölkerungsverteilung und enthält keine wertende Aussage über Versorgung oder Belastung. Sie bildet die Perspektive der potenziellen Nachfrage ab und fungiert als analytischer Ausgangspunkt der Arbeit.

Diese Visualisierung etabliert damit die erste Ebene der Analyse: die räumliche Verteilung der Bevölkerung als Grundlage für jede Form von Versorgungsplanung.

---

### 6.2 Visualisierung 2: Versorgungsgrad – Die offizielle Bewertung
Die zweite Karte zeigt den offiziellen Versorgungsgrad für psychotherapeutische Versorgung.

Die Darstellung erfolgt in harmonischen Blautönen, die die Perspektive der formalen Bedarfsplanung widerspiegeln. Dunklere Blautöne kennzeichnen Regionen mit höheren Versorgungsgrad, hellere Töne entsprechend niedrigere Werte.

Diese Farbwahl orientiert sich bewusst an einer neutralen, systemischen Darstellung. Blau vermittelt Stabilität und Sachlichkeit und unterstützt damit die offizielle Lesart der Kennzahl, nach der viele Regionen als ausreichend oder sogar überversorgt gelten.

Insbesondere in städtischen Regionen wird häufig eine Überversorgung ausgewiesen. Aus Sicht der Bedarfsplanung signalisiert diese Darstellung, dass kein zusätzlicher Handlungsbedarf besteht.

Die Karte bildet damit die formale Bewertung der Versorgungslage ab, ohne Aussagen zur tatsächlichen Erreichbarkeit einzelner Therapieplätze zu treffen.

---

### 6.3 Visualisierung 3: Wartezeiten – Die Realität des Zugangs
Die dritte Karte visualisiert die Wartezeiten auf einen psychotherapeutischen Behandlungsplatz.

Die Farbskala reicht von Warn-Orange bis zu tiefem Bordeaux. Diese Farbabstufung dient der Hervorhebung besonders langer Wartezeiten und lenkt gezielt Aufmerksamkeit auf Regionen mit hohem Versorgungsdruck.

Im bewussten Kontrast zu den vorherigen Karten wirkt diese Visualisierung deutlich unruhiger. Während die Blautöne der Versorgungsgradkarte Stabilität suggerieren, markieren Orange- und Rottöne steigende zeitliche Belastung und eingeschränkte Zugänglichkeit.

Die Karte bildet damit die Perspektive der Patient:innen ab und fungiert als Realitätsindikator. Sie zeigt nicht formale Kapazitäten, sondern den tatsächlichen zeitlichen Zugang zur Versorgung.

Durch den visuellen Kontrast zu den vorherigen Darstellungen wird der zentrale Widerspruch dieser Arbeit unmittelbar erfahrbar.

---

### 6.4 Auswahl der Kartenform
Für die Darstellung der psychotherapeutischen Versorgung wurde bewusst die Kartenvisualisierung gewählt. Der zentrale Grund dafür liegt in der räumlichen Natur der untersuchten Fragestellung. Sowohl Versorgung, Nachfrage als auch Wartezeiten sind nicht abstrakt, sondern lokal gebunden. Sie betreffen konkrete Regionen, in denen Menschen leben, Hilfe suchen und auf Versorgung angewiesen sind.

Andere Visualisierungsformen wie Tabellen oder Balkendiagramme können zwar absolute Werte oder Rangfolgen darstellen, sind jedoch nicht in der Lage, räumliche Muster sichtbar zu machen. Erst durch Karten wird erkennbar, wo sich Überlagerungen, Widersprüche oder Konzentrationen ergeben. Die Karte erlaubt es, regionale Zusammenhänge unmittelbar zu erfassen und benachbarte Gebiete direkt miteinander zu vergleichen.

Ein weiterer entscheidender Faktor ist die Vergleichbarkeit. Alle verwendeten Datensätze liegen auf derselben räumlichen Ebene (Landkreise und kreisfreie Städte) vor. Durch die Nutzung identischer geografischer Geometrien in allen drei Visualisierungen wird sichergestellt, dass die dargestellten Unterschiede nicht aus methodischen Abweichungen resultieren, sondern aus den zugrunde liegenden Kennzahlen selbst. Die Karten machen somit nicht nur einzelne Werte sichtbar, sondern ermöglichen den direkten Vergleich derselben Regionen aus unterschiedlichen Perspektiven.

Die Wahl der Kartenform ist damit keine ästhetische Entscheidung, sondern eine analytische. Sie bildet die Voraussetzung dafür, den zentralen Widerspruch dieser Arbeit, zwischen offizieller Versorgungsbewertung und realem Zugang, räumlich nachvollziehbar darzustellen.

---

## 7. Technische Umsetzung

### 7.1 Software und Datenverarbeitung
- Datenaufbereitung & Merging: Die Harmonisierung und Zusammenführung der Datensätze (INKAR und KBV) erfolgte skriptbasiert mittels der Programmiersprache Python. Als Entwicklungsumgebung (IDE) kam Positron zum Einsatz. Dies ermöglichte die transparente Zusammenführung der Daten über den Amtlichen Gemeindeschlüssel (AGS).

- Visualisierung: Die Erstellung der Karten erfolgte in Datawrapper.

---

### 7.2 Skalierung und Legende
Für die Darstellung der Werte wurden in Datawrapper spezifische Skalentypen und Klassifizierungsmethoden gewählt:

- Bevölkerungsdichte: Nutzung einer kontinuierlichen Farbskala (Continuous), um die fließenden Übergänge zwischen ländlichen und urbanen Räumen abzubilden.

- Versorgungsgrad & Wartezeiten: Nutzung von gestuften Skalen (Steps). Für die Einteilung der Klassen wurde der Algorithmus Natural Jenks (Natürliche Unterbrechungen) verwendet. Diese Methode minimiert die Abweichungen innerhalb der Klassen und maximiert die Unterschiede zwischen den Klassen, was eine datengestützte und objektive Gruppenbildung gewährleistet.

---

## 8. Ergebnisse: Der visuelle Widerspruch
Die Gegenüberstellung der drei Karten zeigt einen systematischen Widerspruch zwischen offizieller Versorgungsbewertung und tatsächlichem Zugang zur Versorgung. Während der Versorgungsgrad rechnerisch eine ausreichende oder sogar überdurchschnittliche Versorgung signalisiert, deuten die Wartezeiten auf eine strukturelle Unterversorgung hin.

Besonders in urbanen Regionen wird dieser Widerspruch sichtbar: Eine hohe Bevölkerungsdichte trifft auf ausgewiesene Überversorgung, gleichzeitig bleiben Wartezeiten lang. Die Visualisierungen machen deutlich, dass der Versorgungsgrad als alleinige Kennzahl den realen Zugang zur psychotherapeutischen Versorgung nicht ausreichend abbildet.

---

## 9. Fazit und Ausblick
Die Analyse zeigt, dass der Versorgungsgrad als alleinige Steuerungsgröße nicht ausreicht, um die tatsächliche Versorgungssituation realistisch zu erfassen. Zwar liefert er eine formale Bewertung der Kapazitäten, berücksichtigt jedoch nicht den tatsächlichen Zugang für Patient:innen.

Die Visualisierungen legen nahe, dass ergänzende Indikatoren, insbesondere Wartezeiten, notwendig sind, um die Versorgung realitätsnäher zu beurteilen. Für zukünftige Planungsmodelle könnte die Integration solcher Zugangsindikatoren einen wichtigen Beitrag leisten.

Zukünftige Arbeiten könnten zudem untersuchen, inwiefern weitere Indikatoren wie Therapiedauer, Abbruchquoten oder regionale Erreichbarkeit die Bewertung der Versorgung weiter differenzieren.






