# Überversorgung auf dem Papier – eingeschränkter Zugang in der Realität
## Eine datenbasierte Analyse der psychotherapeutischen Versorgung in Nordbayern

### Methodische Dokumentation

**Arina Rukina**  
**Renata Figueroa**  
Visualisierung / Technische Hochschule Nürnberg – Ohm / WS 25/26

---

## 1. Einleitung

Die psychotherapeutische Versorgung in Deutschland wird offiziell anhand des sogenannten Versorgungsgrades bewertet. Diese Kennzahl bildet die Grundlage der Bedarfsplanung und entscheidet darüber, wo neue Kassensitze geschaffen werden dürfen. In vielen urbanen Regionen, insbesondere in Städten, weist der Versorgungsgrad eine sogenannte Überversorgung aus. Gleichzeitig berichten Betroffene von monatelangen Wartezeiten auf einem Therapieplatz – auch in genau diesen Regionen.

Diese Diskrepanz wirft die Frage auf, inwieweit die offizielle Statistik die tatsächliche Versorgungssituation widerspiegelt. Die vorliegende Arbeit untersucht diesen Widerspruch anhand einer datenbasierten Visualisierungsanalyse für Nordbayern. Ziel ist es nicht, einzelne Regionen normativ zu bewerten, sondern transparent darzustellen, wie unterschiedliche Kennzahlen zu unterschiedlichen Aussagen über Versorgung führen.

Der Schwerpunkt dieser Arbeit liegt auf der methodischen Herleitung der Visualisierungen: von den Rohdaten über die Datenaufbereitung bis zur finalen kartografischen Darstellung. Die Analyse folgt einem reproduzierbaren Vorgehen, sodass die Ergebnisse nachvollzogen und überprüft werden können.

---

## 2. Zielsetzung

Ziel dieser Arbeit ist es, anhand reproduzierbarer Datenverarbeitung und kartografischer Visualisierung zu zeigen, dass die offiziell ausgewiesene „Überversorgung“ in der psychotherapeutischen Versorgung nicht zwangsläufig mit der realen Zugänglichkeit für Patient:innen übereinstimmt.

Im Mittelpunkt steht dabei nicht die Bewertung einzelner Regionen, sondern die methodische Frage, wie unterschiedliche Kennzahlen, insbesondere der Versorgungsgrad und die Wartezeiten, unterschiedliche Perspektiven auf Versorgung eröffnen.

**Zentrale Forschungsfrage:**

> Wie unterscheiden sich offizielle Versorgungskennzahlen von realen Zugangsindikatoren, und inwiefern lassen sich diese Unterschiede datenbasiert und räumlich sichtbar machen?

---

## 3. Festlegung des Analyse- und Untersuchungsraums

### 3.1 Definition der räumlichen Abgrenzung – Geodaten

Zu Beginn wurde der Untersuchungsraum eindeutig festgelegt.  
Als kartografische Basis dienten die digitalen Geometriedaten **VG250 (Verwaltungsgebiete 1:250.000)** des Bundesamtes für Kartographie und Geodäsie (BKG).

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

**Ausgewählte Variablen:**

- Einwohnerzahl  
- Fläche in Quadratkilometern  
- Kreisschlüssel (Amtlicher Gemeindeschlüssel, AGS)

Die Daten lagen im CSV-Format vor und beziehen sich auf die Verwaltungsebene der Landkreise und kreisfreien Städte.

---

### 3.4 Wartezeiten- und Versorgungsdaten (KBV)

Die versorgungsrelevanten Daten wurden aus den Veröffentlichungen und Statistiken der **Kassenärztlichen Vereinigung Bayerns (KVB)** bezogen. Dieser Datensatz ist zentral für die Untersuchung, da er die offizielle administrative Sicht der Realität des Versorgungsalltags gegenüberstellt.

**Zentrale Komponenten des Datensatzes:**

- **Versorgungsgrad:**  
  Diese Kennzahl gibt das Verhältnis zwischen der Anzahl der niedergelassenen Psychotherapeut:innen mit Kassenzulassung und der gesetzlich festgelegten Einwohnerzahl pro Sitz an. Sie bildet die rechtliche Grundlage für die Bedarfsplanung und Zulassungsbeschränkungen.

- **Wartezeiten bis zum Erstgespräch bzw. Behandlungsbeginn:**  
  Ergänzend zum Versorgungsgrad wurden Daten zu den tatsächlichen Wartezeiten erhoben. Diese dienen als *Realitätsindikator*, da sie den praktischen Zugang zur Versorgung aus Patient:innensicht abbilden.

---

### 3.5 Zeitliche Einordnung und Belastbarkeit der Daten

Bei der Zusammenführung der Datensätze ergeben sich unterschiedliche Zeitstände (2021 bis 2025). Diese methodische Entscheidung wurde bewusst getroffen und lässt sich wie folgt begründen:

- **Versorgungsgrad (2025):**  
  Verwendung der aktuellsten verfügbaren Daten der KVB, da diese Kennzahl die rechtliche Grundlage der Bedarfsplanung bildet.

- **Bevölkerungsdichte (2023):**  
  Aktuellster verfügbarer Stand aus dem INKAR-Datensatz. Veränderungen der Bevölkerungsstruktur auf Kreisebene sind über kurze Zeiträume marginal.

- **Wartezeiten (2021):**  
  Letzter vollständiger Datensatz für ganz Nordbayern. Studien der BPtK zeigen, dass sich die Wartezeitensituation seither nicht verbessert, sondern eher verschärft hat.

Die zeitliche Diskrepanz führt nicht zu einer Verzerrung, sondern stellt eine konservative Schätzung dar. Es ist davon auszugehen, dass die reale Diskrepanz heute größer ist.

---

## 4. Datengrundlage

### 4.1 Bevölkerungsdaten (INKAR)

Die Bevölkerungsdaten stammen aus dem INKAR-Datensatz (Indikatoren und Karten zur Raum- und Stadtentwicklung).

**Relevante Merkmale:**

- Verwaltungsebene: Landkreise und kreisfreie Städte  
- Format: CSV  
- Variablen: Einwohnerzahl, Fläche in km², Kreisschlüssel (AGS)

---

### 4.2 Versorgungsgrad Psychotherapie

Der Versorgungsgrad ist eine offizielle Kennzahl der KVB.

**Klassifizierung:**

- < 90 %: Unterversorgung  
- 90–110 %: Regelversorgung  
- > 110 %: Überversorgung  

---

### 4.3 Wartezeiten auf einen Psychotherapieplatz

Die Wartezeiten wurden aus öffentlich zugänglichen Quellen der KVB sowie ergänzender Recherche erhoben.

**Merkmale:**

- Maßeinheit: Tage  
- Statistische Grundlage: Median (Kreisebene)  
- Zweck: Abbildung des tatsächlichen Zugangs zur Versorgung  

---

## 5. Datenaufbereitung

Alle Datensätze wurden auf Kreisebene harmonisiert und über den amtlichen Kreisschlüssel (AGS) zusammengeführt.

**Methodische Qualitätssicherung:**

- Vollständige Datensätze für den gesamten Untersuchungsraum  
- Keine Schätzungen oder Imputationen notwendig  

---

## 6. Visualisierungskonzept

### 6.1 Visualisierung 1: Bevölkerungsdichte – Wo sind die Menschen?

Darstellung als Choroplethenkarte mit Gelb–Rot-Skala.  
Fokus: räumliche Verteilung der potenziellen Nachfrage.

---

### 6.2 Visualisierung 2: Versorgungsgrad – Die offizielle Bewertung

Darstellung in Blautönen.  
Fokus: formale Systemlogik der Bedarfsplanung.

---

### 6.3 Visualisierung 3: Wartezeiten – Die Realität des Zugangs

Darstellung in Orange–Bordeaux.  
Fokus: zeitliche Zugänglichkeit aus Patient:innensicht.

---

### 6.4 Auswahl der Kartenform

Die Kartenvisualisierung ermöglicht den direkten räumlichen Vergleich identischer Regionen aus unterschiedlichen Perspektiven und macht strukturelle Widersprüche sichtbar.

---

## 7. Technische Umsetzung

### 7.1 Software und Datenverarbeitung

- Python (Datenaufbereitung, Merging)  
- Positron (IDE)  
- Datawrapper (Visualisierung)

---

### 7.2 Skalierung und Legende

- Bevölkerungsdichte: kontinuierliche Skala  
- Versorgungsgrad & Wartezeiten: gestufte Skalen  
- Klassifizierung: Natural Jenks

---

## 8. Ergebnisse: Der visuelle Widerspruch

Die Visualisierungen zeigen einen systematischen Widerspruch zwischen formaler Versorgungsbewertung und realem Zugang zur psychotherapeutischen Versorgung.

---

## 9. Fazit und Ausblick

Der Versorgungsgrad allein reicht nicht aus, um die tatsächliche Versorgung realistisch abzubilden. Ergänzende Zugangsindikatoren wie Wartezeiten sind notwendig, um Versorgung realitätsnäher zu bewerten.

Zukünftige Arbeiten könnten weitere Indikatoren wie Therapiedauer, Abbruchquoten oder regionale Erreichbarkeit einbeziehen.
