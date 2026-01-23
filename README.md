# Überversorgung vs. Mangel in der Realität  
## Eine datenbasierte Analyse der psychotherapeutischen Versorgung in Nordbayern

Dieses Repository dokumentiert eine reproduzierbare Datenpipeline (Rohdaten → Aufbereitung → Kartenvisualisierungen), die den Widerspruch zwischen **offiziell ausgewiesenem Versorgungsgrad** (Bedarfsplanung) und **realem Zugang** (Wartezeiten) in der psychotherapeutischen Versorgung für **Nordbayern** sichtbar macht.

**Kernaussage:** Regionen können laut Versorgungsgrad „überversorgt“ erscheinen, während Patient:innen dort dennoch lange auf Therapieplätze warten.

-------------------------------------------------------------------------------------------------

## Projektfrage

**Wie unterscheiden sich offizielle Versorgungskennzahlen (Versorgungsgrad) von realen Zugangsindikatoren (Wartezeiten), und wie lassen sich diese Unterschiede datenbasiert und räumlich visualisieren?**

------------------------------------------------------------------------------------------------

## Datenquellen (Input)

- **INKAR** (BBSR) – Bevölkerungs- und Flächendaten auf Kreisebene  
  → wird genutzt zur Berechnung der **Bevölkerungsdichte** (Einwohner/km²) als Nachfrage-Proxy.
- **KVB (Kassenärztliche Vereinigung Bayerns)** – **Versorgungsgrad Psychotherapie (%)**  
  → offizielle Kennzahl der Bedarfsplanung inkl. Schwellenwerten (<90 / 90–110 / >110).
- **KVB + ergänzende Recherche** – **Wartezeiten** (Tage)  
  → Realitätsindikator für tatsächlichen Zugang zur psychotherapeutischen Versorgung.


------------------------------------------------------------------------------------------------

## Untersuchungsraum & räumliche Ebene

- **Nordbayern** (Oberfranken, Mittelfranken, Unterfranken)
- **Räumliche Ebene:** Landkreise und kreisfreie Städte  
- **Join-Key:** Kreisschlüssel / AGS (amtlicher Gemeindeschlüssel)

------------------------------------------------------------------------------------------------

## Methodischer Workflow (Kurz)

1. **Rohdaten importieren** (INKAR, KVB Versorgungsgrad, Wartezeiten)
2. **Harmonisierung** auf Kreisebene & Join über **AGS**
3. **Berechnung Bevölkerungsdichte**  
   `Bevölkerungsdichte = Einwohnerzahl / Fläche_km²`
4. **Klassifizierung für Karten**
   - Bevölkerungsdichte: quantilbasiert
   - Versorgungsgrad: KVB-Schwellen (<90 / 90–110 / >110)
   - Wartezeiten: Klassen in Tagen (z. B. <30, 30–60, 60–100, >100)
5. **Erstellung von Choroplethen-Karten** mit identischer Geometrie
6. **Vergleich** der Karten als Story-Sequenz:
   - Setup (Nachfrage): Bevölkerungsdichte
   - Illusion (Systemsicht): Versorgungsgrad
   - Twist (Realität): Wartezeiten

------------------------------------------------------------------------------------------------

## Ergebnisse / Visualisierungen

- **Karte 1:** Bevölkerungsdichte – „Wo sind die Menschen?“ (Blau)
- **Karte 2:** Versorgungsgrad – „Die offizielle Bewertung“ (Gelb/Grün)
- **Karte 3:** Wartezeiten – „Die Realität des Zugangs“ (Rot)

Besonders relevant sind Regionen, die in der Versorgungsgradkarte „grün“ (Überversorgung) erscheinen, aber in der Wartezeitkarte „rot“ (lange Wartezeiten).

------------------------------------------------------------------------------------------------

## Repository-Struktur 
data/
figures/
notebooks/
README.md

Generative KI wurde unterstützend bei der Strukturierung der Analyse, der Textformulierung sowie bei der Entwicklung von Code-Skeletten eingesetzt. Alle Ergebnisse wurden von Arina Rukina und Renata Figueroa überprüft und eigenständig interpretiert.
