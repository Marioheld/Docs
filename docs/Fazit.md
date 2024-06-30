# Fazit
**Jannis Gröger**

## Zusammenfassung

Das Projekt zur Entwicklung eines Low Power Raumdisplays war in mehrern Hinsichten ein klarer Erfolg. Das Hauptziel, eine energieeffizientes Informationsanzeige zu entwickeln, wurde erfüllt und kann, wie in den Anforderungen vgl [Kapitel 6.3](Systemkonzept.md#potentielle-einsatzgebiete-der-low-power-raumanzeige) beschrieben, nicht nur an Hochschulen, sondern auch in Firmen, an Messeständen und in Privathaushalten genutzt werden. 

Das Display zeichnet sich mit einer langen Akkuklaufzeit und sehr geringer Leistungsaufnahme durch die durchdachte Auswahl stromsparender Komponenten wie das E-Paper Display und softwareseitige Hardwareverwaltung wie die Implementierung des Deepsleeps. Durch die Aufbauen eines eigenes WLAN Acces Points des Mikrocontrollers und die Stromversorgung per Akku ist das Displaymodul komplett autark von Stromnetz und Netzwerk, was den Einsatzbereich und die Anwendungsszenarien deutlich erweitert.  

Zudem lässt sich die Raumanzeige durch den frontseitigen Benutzerknopf und die implementierte Website sehr leicht steuern und einfach bedienen. Die Verwaltung mehrerer Displays im Server-Modus geschieht ebenfalls über eine Website, die sich in der Struktur sehr ähnlich sind, was die Benutzerfreundlichkeit steigert.

Das schlanke und durchdachte Design des Gehäuses ermöglicht nicht nur eine einfache Montage, sondern auch ein leichtes Austauschen der Akkupacks beim Laden, ein Zurücksetzen des Displaymoduls ohne viel Aufwand und ein Debugging oder Systemflash durch die Zugänglichkeit zum Mikrocontroller.

Insgesamt bietet das entwickelte Low Power Raumdisplay eine zukunftsweisende Lösung für verschiedene Einsatzszenarien, von Bürogebäuden über öffentliche Einrichtungen bis hin zu privaten Haushalten. Es trägt zur Reduzierung des Energieverbrauchs bei und unterstützt damit nachhaltige und umweltfreundliche Technologien.

Abschließend kann festgehalten werden, dass die Projektarbeit nicht nur zur Weiterentwicklung technischer Kompetenzen beigetragen hat, sondern auch einen praktischen Nutzen bietet, der im Einklang mit den heutigen Anforderungen an Energieeffizienz und Benutzerfreundlichkeit steht. Die positiven Testergebnisse und das Feedback aus ersten praktischen Anwendungen bestätigen den Erfolg des Projekts und zeigen das Potential für eine breite Markteinführung.

## Ausblick

Da die Projektarbeit in ihrem zeitlichen Rahmen begrenzt ist, ist eine Beschränkung auf eine begrenzte Anzahl an Features nicht nur sinnvoll, sondern auch essentiell. Im Folgenden werden mögliche Erweiterungen und Verbesserungen der Low Power Raumanzeige genannt, die bei einer Weiterentwicklung berücksichtigt werden können. 

Eine interessante Information über das Display selbst ist der momentane Akkustand, dass verhindert werden kann, dass das Display nicht mehr mit Strom versorgt wird und seine Funktion damit verliert. Denkbar wäre hier die Messung der Akkukapazität und das Anzeigen dieser auf dem Display, sodass der Betreiber einen einfachen Überblick darüber bekommt, wann er die Akkus eines Moduls tauschen oder laden muss. 

Zudem ist eine Verbesserung der entworfenen Platine eine Erweiterung, die in Betracht gezogen werden kann. Durch das Anbringen von so genannten Mounting Holes, könnte die Platine leichter im Gehäuse befestigt werden, und das feste Verlöten des Mikrocontrollers auf der Platine würde die gesamte Dicke des PCBs verringern. Dadurch könnten entsprechende Veränderungen am Design des Gehäuses vorgenommen werden, um ein noch dünneres und robusteres Modul zu bekommen.

Eine weitere mögliche Verbesserung ist die Implementierung eines Light Sleeps, der es ermöglicht, das Display jeder Zeit erreichbar zu machen. So kann beispielsweise im Netzwerk Modus nicht nur eine Bildaktualisierung vorgenommen werden, wenn der Benutzer auf den Refresh Knopf drückt, sondern auch dann, wenn der Betreiber ein neues Bild über die Website hochlädt.

Die momentane Erstellung von Anzeigebilder aus vorhanden Templates, in die der Betreiber des Displays Daten händisch einträgt, könnte in Zukunft automatisiert passieren. Damit könnte eine Erstellung eines Zeitplans aus externen Quellen wie zum Beispiel einem Kalender per CalDAV realisiert werden. Zudem könnte auch aus Raumbelegungsdaten einer Software wie Beispielsweise WebUntis ein Zeitplan erstellt, was für Bildungseinrichtungen von großem Interesse sein kann.

Die Funktion des frontseitigen Benutzerknopfes sind auch vielseitig erweiterbar. Beispielsweise das Wechseln zwischen mehreren Anzeigebildern oder das Buchen eines Raumes, welches dann auch in einem Raumbelegungsplan angezeigt wird, sind vorstellbare Verbesserungen.

Das momentane unterstützte 7.3-Zoll-Display benötigt für jede Bildaktualisierung eine längere Zeit und flackert stark, um die Pigmente des E-Papers richtig zu platzieren. Dies ist nicht nur umständlich für den Benutzer, sondern kann auch ein möglicher Trigger für Menschen mit photosensitiver Epilepsie sein. Beim 9.7-Zoll-Display ist die Aktualisierung um einiges schneller mit eine Zeit von unter einer Sekunde, jedoch werden hierbei keine Farben unterstützt. Eine Verbesserung wäre die Nutzung eines Displays, welches die sogenannte "Fast Refresh" Technologie des 9.7-Zoll-Displays wie auch eine Farbunterstützung ähnlich wie bei dem 7.3-Zoll-Display besitzt.

Die genannten Verbesserungs- und Erweiterungsmöglichkeiten bieten die Chance auf eine noch bessere Benutzerfreundlichkeit und leichtere Bedienung, um die Anwendungsfälle zu optimieren und das Einsatzspektrum zu erweitern.