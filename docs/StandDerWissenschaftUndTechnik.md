# Marktanalyse aktueller Trends und Technologien
**Julia Reuter**

Die Motivation des Projektteams lag bei erster Betrachtung des Projektes Low-Power Raumanzeige für die THA hauptsächlich in
der Steigerung der Effizienz und des eigenen Komforts. Das Projekt wurde also eher als Nischenprodukt für den internen
Gebrauch angesehen. Diese Einstellung änderte sich jedoch schnell nach einiger Recherche. 
Nicht nur ist der potenzielle Markt für eine Low-Power Raumanzeige aufgrund der vielfältigen Einsatzgebiete in unter anderem Büroräumen, Krankenhäusern oder
Bildungseinrichtungen relativ groß. Sondern auch im Hinblick auf das Thema Umwelt, Nachhaltigkeit und Digitalisierung stellt
die Raumanzeige eine attraktive Lösung dar. So wird beispielsweise eine effiziente Nutzung von Räumen durch klare
Erkennbarkeit der Belegung ermöglicht. Durch intelligente Verwaltungsmechanismen könnten sogar unnötige Heiz- und
Beleuchtungskosten reduziert werden, wenn der Raum gerade nicht genutzt wird. Darüber hinaus kann auf papierbasierte
Stundenpläne und Türschilder verzichtet werden. Der damit verbundene personelle Koordinationsaufwand zur Instandhaltung
wird deutlich verringert und Ressourcen wie Papier und Druckertinte werden eingespart.

All dieses Aspekte sind Merkmale für ein durchaus zukunfttaugliches Produkt und gerade deshalb gibt es bereits einige
Unternehmen, die dieses Potenzial erkannt und entsprechende Produkte entwickelt haben.
Im Folgenden werden nun vier hauptsächlich deutsche Unternehmen analysiert, welche als Inspiration für die eigene
Raumanzeige dienen und durch ihr breites Spektrum dem Team zu neuen Ansätzen und Ideen verhelfen.

## Übersicht einiger Konkurrenzprodukte

Bei den ausgewählten Unternehmen und Produkten handelt es sich um:

- **Wizepanel** der Firma Wilke Technology in Aachen [[JR_01]](Quellenverzeichnis.md#jr_01)
- **Digitales Türschild** der Firma digitalSIGNAGE in Hamburg [[JR_02]](Quellenverzeichnis.md#jr_02)
- **ROOMZ Display** der Firma ROOMZ in Freiburg (Schweiz) [[JR_03]](Quellenverzeichnis.md#jr_03)
- **Touchscreen-Display** der Firma Beetronics mit Sitz in Düsseldorf [[JR_04]](Quellenverzeichnis.md#jr_04)

Im Hinblick auf das eigene Projekt lag der Fokus der Recherche auf folgenden Aspekten, welche im Anschluss tabellarisch (s.
Tabelle 4.2) aufgelistet sind:

- Display Art (LCD oder E-Paper)
- Farbunterstützung
- Ansteuerung/Netzprotokoll
- Batterie und geschätzte Laufzeit
- Betrieb (Schnittstelle zum Kunden)
- Besondere Features

## Produktvergleich ausgewählter Unternehmen

Tabelle 4.2 Übersicht und Vergleich der 4 ausgewählten Raumanzeigen 

| Kategorie                                 | Wizepanel [[JR_05]](Quellenverzeichnis.md#jr_05)                                                                                                           | Digitales Türschild [[JR_06]](Quellenverzeichnis.md#jr_06)                                                       | ROOMZ [[JR_03]](Quellenverzeichnis.md#jr_03)                                                                                                            | Beetronics [[JR_07]](Quellenverzeichnis.md#jr_07)                                                          |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Display Art**                           | E-Paper                                                                                                                                                     | Touch-Screen (kein E-Paper)                                                                                       | E-Paper                                                                                                                                                     | High Brightness Full HD Touchscreen                                                                      |
| **Farbunterstützung**                     | Schwarz-Weiß, 16 Graustufen                                                                                                                                 | Farbe                                                                                                             | Schwarz-Weiß                                                                                                                                                 | Farbe                                                                                                     |
| **Ansteuerung/Netzprotokoll**             | 868 MHz Ultra Low Power Funk, eigene Funksender                                                                                                             | Ethernet, NFC-Option verfügbar                                                                                    | WLAN                                                                                                                                                         | Display Port, HDMI, VGA, USB-C, Unterstützung aller gängigen Betriebssysteme                              |
| **Batterie und geschätzte Laufzeit**      | 10 x AA-Lithium-Primärzellen, bis zu 20 Jahre                                                                                                               | Power over Ethernet (PoE) → Kabelanschluss nötig                                                                  | 8000mAh, 4 Jahre                                                                                                                                              | Netzteil (d.h. Stromanschluss) denn braucht 12.7W (Betrieb)/0.4W (Standby)                                |
| **Betrieb (Kundenschnittstelle)**         | Zentrale Serverkomponente: Inhaltsübertragung und Geräteverwaltung                                                                                          | Keine Angabe                                                                                                       | MyRoomz-App zur Buchung einzelner definierter Arbeitsbereiche [[JR_10]](Quellenverzeichnis.md#jr_10)                                                          | Einfaches Plug-and-Play, sonst eigener Treiber für verschiedene Betriebssysteme verfügbar                |
| **Besondere Features**                    | Bereits in den Server integrierte Adapter für MS Exchange, iCal/ICS, Google Calendars, Excel,... Auch WebUntis wird unterstützt [[JR_08]](Quellenverzeichnis.md#jr_08) | LEDs rund um Display (rot, gelb, grün) zur Hervorhebung der Raumbelegung, Sofortbuchung über Touch/NFC             | MyRoomz-App bietet Lageplanansicht des Gebäudes mit Übersicht aller Räume mit Markierung ob sie belegt sind oder nicht [[JR_10]](Quellenverzeichnis.md#jr_10), ROOMZ Sensor zur Vermeidung von Ghost-Meetings [[JR_09]](Quellenverzeichnis.md#jr_09), Sofortbuchung über Touchleiste am Gehäuse | Keine spezifischen Features angegeben, aber allgemein sehr vielfältig universell einsetzbar               |


## Auswertung der Rechercheergebnisse

### Vor- und Nachteile der einzelnen Produkte

Tabelle 4.3.1 Vor-und Nachteile der vier Displayprodukte

| Hersteller         | Vorteile                                                                                           | Nachteile                                                                                       |
| ------------------ | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Wizepanel**      | <ul><li>E-Paper-Technologie: Geringer Energieverbrauch</li><li>Lange Akkulaufzeit: Bis zu 20 Jahre</li><li>Ultra Low Power Funk: Energiesparende und drahtlose Kommunikation</li><li>Serverintegration: Unterstützung für gängige Kalender- und Verwaltungssysteme</li></ul> | <ul><li>Schwarz-weiß Display: Keine Farbdarstellung möglich</li><li>Eigene Funksender zur Datenübertragung werden benötigt: Abhängigkeit von zusätzlicher Hardware</li></ul> |
| **digitalSIGNAGE** | <ul><li>Touch-Screen und Farbe: Interaktive und ansprechende Benutzeroberfläche</li><li>NFC-Option und Ethernet: Flexibilität bei der Ansteuerung</li><li>LEDs zur Raumbelegung: Visuelle Hinweise zur Raumverfügbarkeit</li></ul> | <ul><li>Power over Ethernet (PoE): Benötigt eine Kabelverbindung, externe Abhängigkeit</li><li>Keine Angaben zur Akku-Laufzeit: Unklarheit über Energieeffizienz, vermutlich aber eher gering aufgrund der Displaytechnologie</li></ul> |
| **ROOMZ**          | <ul><li>E-Paper-Technologie: Geringer Energieverbrauch</li><li>WLAN: Einfache Integration in bestehende Netzwerke</li><li>Lange Akkulaufzeit: Bis zu 4 Jahre</li><li>MyRoomz-App: Umfassende Funktionen zur Raumbuchung und -verwaltung, auch über mobile Endgeräte</li></ul> | <ul><li>Schwarz-weiß Display: Keine Farbdarstellung möglich</li></ul> |
| **Beetronics**     | <ul><li>High Brightness Full HD Touchscreen: Hervorragende Bildqualität und interaktive Möglichkeiten</li><li>Vielseitige Anschlussmöglichkeiten: Unterstützung für Display Port, HDMI, VGA, USB-C; Flexibiliät in der Ansteuerung</li></ul> | <ul><li>Verhältnismäßig sehr hoher Energieverbrauch</li><li>Kabelgebunden: Abhängigkeit von ständiger Stromquelle</li></ul> |

### Abgeleitete Kriterien für das eigene Produkt

Basierend auf der Analyse der Vor- und Nachteile der Konkurrenzprodukte (vgl. Tabelle 4.3.1) sollten folgende Eigenschaften in
die eigene Low-Power Raumanzeige integriert werden, um auf dem aktuellen Markt konkurrenzfähig zu sein:

1. **E-Paper-Technologie:** Für minimalen Energieverbrauch und lange Akkulaufzeit
2. **Lange Akkulaufzeit:** Nutzung von effizienten Batterien/Akkus für eine wartungsarme Lösung und unabhängigen Betrieb
3. **Drahtlose Kommunikation:** WLAN oder Funk für flexible und einfache Installation sowie geringem Energieverbrauch
4. **Integration in bestehende Systeme:** Unterstützung für gängige Kalender- und Verwaltungssysteme (z.B. iCal/ICS oder WebUntis) über zentrale Serverkomponenten zur effizienten Verwaltung und Nutzung

### Ansätze zur Verbesserung der Konkurrenzfähigkeit auf dem Markt
Um sich von den zahlreichen Konkurrenzprodukten abzuheben, gibt es einige Ansätze, welche nach Möglichkeit in das System
integriert werden.

- **Interaktivität:** Auch wenn es sich um ein E-Paper Display handelt, besteht die Möglichkeit eine gewisse Benutzerinteraktion
für beispielsweise spontane Raumbuchungen zu integrieren. Eine Option, die energiesparend und auch ohne Touchfunktion
umsetzbar ist, ist das Integrieren von Knöpfen am Gehäuserand. Per Knopfdruck könnte so das Anzeigebild
oder die Ansicht gewechselt werden.

- **Farbunterstützung:** Ein E-Paper-Display mit Farbunterstützung trägt dazu bei, das eher schlichtes Produkt für den Kunden
optisch ansprechender zu gestalten und sich dabei von der Masse abzuheben. Auch ein E-Paper-Display mit Farbunterstützung
würde dazu beitragen das eher schlichtes Produkt für den Kunden optisch ansprechender zu gestalten und sich von der Masse
abzuheben.

- **Flexibilität:** Das zentrale Alleinstellungsmerkmal ist das Entwickeln eines möglichst generischen Konzeptes, das sehr flexibel
einsetzbar ist. Denn eine Einschränkung der obigen Systeme ist, dass alle zentral über eine Serverkomponente gesteuert
werden und teilweise sogar eigene Funkverteiler brauchen (vgl. Wizepanel). Dies ist für den Benutzer mit viel Aufwand und
Kosten verbunden, um die eigenen Infrastruktur so zu erweitern, damit Display-Module intergriert werden können. Diese
Maßnahmen lohnen sich nur für sehr große Organisationen mit ausreichend Budget. Die Zielgruppe ist also entsprechend
gering. Zudem ist man stets von einer externen Softwarekomponente abhängig. Die Display Ansteuerungsschnittstelle wird
ebenfalls vom Hersteller in Form von einem Server (vgl. Wizepanel) oder einer App (vgl. ROOMZ) geliefert. So ist das System
bei Ausfall oder Fehlverhalten nicht mehr einsatzfähig, bis das Problem durch eine externe Partie, sprich dem Hersteller,
behoben wurde.

Ziel ist es also ein Konzept umzusetzten, indem die Benutzergruppe möglichst breit ist und externe Abhängigkeiten so weit wie
möglich minimiert werden. Die eigene Raumanzeige soll also nicht zwingend eine zusätzliche externe Infrastruktur benötigen.
Sprich es wird eine Option für eine Standalone-Funktionalität geben, sodass das Low-Power Display völlig unabhängig von
jeglicher zusätzlicher Soft- und Hardware ist und autark funkionieren kann. Gleichzeitig besteht weiterhin die Möglichkeit eine
zentrale Verwaltungskomponente zu integrieren, um auch mehrere Displays verwalten zu können. Diese Flexibilität gekoppelt
mit der Prämisse, das System Open-Source zu gestalten, sorgt für eine hohe Konkurrenzfähigkeit auf dem Markt. Außerdem wird
versucht, ein möglichst großes Potenzial für Erweiterbarkeit zu schaffen, sodass beispielsweise ein externer Raumsensor (vgl.
ROOMZ Sensor) eingebunden werden kann. Dem Kunden werden somit alle Mittel an die Hand gegeben, um das System nach
Belieben anzupassen und zu erweitern.

Die Low-Power Raumanzeige ist somit nicht nur für die Hochschule attraktiv, sondern kann auch in kleinern Kreisen bis hin zum
privaten Gebrauch eingesetzt werden.