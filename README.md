# Überversorgung auf dem Papier – Mangel in der Realität
## Eine datenbasierte Analyse der psychotherapeutischen Versorgung in Nordbayern

Dieses Projekt untersucht die Diskrepanz zwischen offiziellen Versorgungskennzahlen und dem tatsächlichen Zugang zu psychotherapeutischer Behandlung. Während administrative Daten oft eine Überversorgung suggerieren, zeigen reale Wartezeiten ein gänzlich anderes Bild.

---

## Übersicht
Das Ziel dieser Arbeit ist es, den Widerspruch zwischen dem offiziellen Versorgungsgrad und den realen Wartezeiten für Patientinnen und Patienten in Nordbayern räumlich sichtbar zu machen. Die Analyse konzentriert sich auf die Regierungsbezirke Ober-, Mittel- und Unterfranken sowie die Oberpfalz.

* **Forschungsfrage:** Wie unterscheiden sich offizielle Kennzahlen von realen Zugangsindikatoren?
* **Untersuchungsraum:** Nordbayern auf Kreisebene (Landkreise und kreisfreie Städte).

---

## Repositorystruktur

Das Repository ist wie folgt strukturiert:

* **data/**: Enthält alle verwendeten Rohdaten und die finalen bereinigten Datensätze sowie die entsprechenden Quellnachweise.
* **figures/**: Beinhaltet die aus den Daten generierten Visualisierungen.
* **notebooks/**: Enthält die Python-Notebooks, die für die Datenaufbereitung, das Merging und die Voranalyse genutzt wurden.
* **reports/**: Dokumentiert den gesamten Analyseprozess, von der methodischen Herleitung bis hin zu den Endergebnissen.
* **tests/**
* **README.md**

---

## Methodik und Datengrundlage
Die Analyse basiert auf der Zusammenführung und Harmonisierung von drei zentralen Datensäulen:

1. **Bevölkerungsdichte (Nachfrage-Indikator):**
Datenquelle ist der INKAR-Datensatz des Bundesinstituts für Bau-, Stadt- und Raumforschung. Verwendet wurden Einwohnerzahl, Fläche und der Amtliche Gemeindeschlüssel (AGS).

2. **Versorgungsgrad (System-Perspektive):**
Diese offizielle Kennzahl der Kassenärztlichen Vereinigung Bayern (KVB) beschreibt das Verhältnis von Kassensitzen zum rechnerischen Bedarf. Werte über 110 Prozent gelten als Überversorgung.

3. **Wartezeiten (Realitäts-Indikator):**
Konsolidierte Daten der KVB und ergänzende Recherchen bilden die Grundlage. Als statistischer Wert wurde der Median der Wartezeit in Tagen auf Kreisebene gewählt.

---

## Visualisierungskonzept
Das Projekt nutzt gezielte visuelle Brüche, um die inhaltliche Diskrepanz zwischen den Datensätzen zu verdeutlichen.

**Visualisierung 1: Bevölkerungsdichte**
Die Darstellung erfolgt als Choroplethenkarte mit einer Gelb-Roten Farbskala. Sie dient zur Identifikation von Verdichtungsräumen und stellt die neutrale Perspektive der Nachfrage dar.

**Visualisierung 2: Versorgungsgrad**
Die Wahl einer monochromen Skala in Medical Blue spiegelt die administrative Sicht wider. Die kühle Farbe suggeriert Stabilität und Ordnung innerhalb der System-Logik.

**Visualisierung 3: Wartezeiten**
Hier wird eine aggressive Farbskala von Warn-Orange bis zu tiefem Bordeaux verwendet. Das visuell unruhiges Kartenbild macht die emotionale Belastung und die Willkür des Systemzugangs für Betroffene spürbar.

---

## Technische Umsetzung

* **Datenverarbeitung:** Die Harmonisierung erfolgte skriptbasiert mittels Python in der Entwicklungsumgebung Positron.
* **Zusammenführung:** Die Datensätze wurden über einen Merge-Prozess basierend auf dem Amtlichen Gemeindeschlüssel (AGS) verknüpft.
* **Kartografie:** Die Erstellung der Karten erfolgte über Datawrapper unter Nutzung der digitalen Geometriedaten VG250 des BKG.

---

## Zentrale Ergebnisse
Die Analyse belegt einen systematischen Widerspruch: In den urbanen Zentren trifft eine hohe Bevölkerungsdichte auf eine offiziell ausgewiesene Überversorgung. Gleichzeitig erreichen jedoch die realen Wartezeiten in genau diesen Regionen kritische Werte. Das Fazit der Untersuchung unterstreicht, dass der Versorgungsgrad als alleinige Steuerungsgröße unzureichend ist und durch Zugangsindikatoren wie Wartezeiten ergänzt werden muss.

---

Generative KI wurde unterstützend bei der Strukturierung der Analyse, der Textformulierung sowie bei der Entwicklung von Code-Skeletten eingesetzt. Alle Ergebnisse wurden von Arina Rukina und Renata Figueroa überprüft und eigenständig interpretiert.
