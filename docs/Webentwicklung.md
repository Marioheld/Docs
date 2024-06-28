# Webentwicklung
 
## Framework und Library Auswahl

## Konvertierungsverfahren (HTML → PNG → Bitmap)

## Web Bneutzer Oberfläche

## Linux Server 
**Mario Wegmann**

### Verwendete Technologien

Wie im Kapitel [3.9.1 Webtechnologien](PraktischeUTheoretischeGrund.md#webtechnologien) bereits erläutert ist es für die Entwicklung einer komplexeren Webanwendung sehr sinnvoll ein Webframework einzusetzen. 
Hierbei gibt es eine große Auswahl an möglichen Frameworks und auch Serverseitigen Programmiersprachen. Da JavaScript bereits im Standalone-Modus, wie auch im Netzwerk-Modus, verwendet wird um die Interaktion mit dem Displaymodul zu realisieren, ist es naheliegend, auch auf dem Server JavaScript zu nutzen. Diese Entscheidung ermöglichte eine einheitliche Codebasis sowohl im Frontend als auch im Backend, was die Entwicklung effizienter und die Wartung der Anwendung einfacher macht und zuletzt auch das erlernen neuer Programmiersprachen auf eine reduziert. Zudem wurde die Möglichkeit genutzt TypeScript anstatt Vanilla JavaScript zu verwenden, um die Vorteile zu nutzen, welche ebenso bereits im Kapitel [3.9.1 Webtechnologien](PraktischeUTheoretischeGrund.md#webtechnologien) erwähnt wurden. 

Für das Frontend wurde React ausgewählt. Durch React lassen sich Komponenten realisieren, welche modular wiederverwendet werden können. Dadurch wird es vermieden doppelten Code zu verfassen und Änderungen an einer Komponente werden global in der gesamten Webanwendung wiedergespiegelt. 

Als Webframework wurde Next.js ausgewählt, da es React unter anderem um serverseitiges Rendering erweitert. Darüber hinaus bietet Next.js eine nahtlose Integration von API-Routen und Middleware, was die Entwicklung von Full-Stack-Anwendungen erleichtert. 

Für das speichern der Daten wurde PostgresSQL als Datenbank ausgewählt. Hierbei wird Prisma ORM als Zwischenschicht eingesetzt, damit die Modelle der Relationanlen Datenbank als Objekte mit statischen Typen generiert werden. 

Für den Webserver wurden Linux und Docker verwendet. Das quelloffene Linux ist bekannt für seine Stabilität, Sicherheit und Performance, was es zu einer idealen Wahl für den Einsatz als Webserver macht. Docker ergänzt diese Vorteile durch die Bereitstellung einer containerisierten Umgebung, die eine konsistente und isolierte Ausführung von Anwendungen ermöglicht. Dies erleichtert die Skalierung und Verwaltung der Anwendung erheblich und sorgt dafür, dass sie in unterschiedlichen Umgebungen gleichbleibend funktioniert. Docker-Container bieten zudem eine einfache Möglichkeit, Abhängigkeiten zu verwalten und die Bereitstellung von Updates zu automatisieren. 

Die Kombination dieser Technologien ermöglich effizient eine benutzerfreundliche, performante und wartbare Webanwendung zu entwicklen.

Wie die Einzelkomponenten zusammenspielen ist in (#_fig_MW_techstack) ersichtlich.

Figure: Der Techstack der Webanwendung { #_fig_MW_techstack }

![](img/Techstack.png){ width=60% }

### Testumgebung

Als Testumgebung wurde beim Rechenzentrum (RZ) eine Linux VM beantragt. Die vom Rechenzentrum erhaltene VM weißt die in []( #_tab_MW_01 ) genannten Eigenschaften auf

Table: Die Systemeigenschaften der vom RZ erhaltenen VM.  { #_tab_MW_01 }

| Eigenschaft | Wert |
|-------|------|
| Betriebssysrtem | Debian 12 (bookworm) |
| Prozessor-Cores | 2x 2,9 GHz |
| Arbeitsspeicher | 2 GB |
| Hauptspeicher | 30 GB |
| Hostname | lprd |

Zudem wurde vom RZ auch gleich ein DNS Eintrag gesetzt und die Domain lprd.informatik.tha.de verweist auf diese VM. 
Neben dem Betriebssystem liefert die VM auch gleich noch eine Firewall standardmäßig mit, hier setzt das RZ die Variante arno-iptables ein [[MW_01]](Quellenverzeichnis.md#MW_01). 

### Ersteinrichtung

Der administrative Zugriff auf die VM erfolgt über SSH. 
Nach der Übergabe wurden zuerst die standard Zugangsdaten der VM durch neue Zugangsdaten ersetzt und die SSH Anmeldung des root Benutzer gesperrt. Ebenso wurden für die Personen, welche Zugriff auf die VM benötigen jeweils neue Benuzter angelegt. Dabei wurde als Benutzerauthentifizierung SSH-Keys als Authentifizierungsmethode verwendet. 
Anschließend wurden die installierten Pakete mit dem Advanced Packaging Tool (apt) Paketmanager auf die neuste Version aktualisiert. 

Damit die VM während der Dauer des Projekts zuverlässig läuft und Probleme frühzeitig erkannt werden wurde eine Monitoring Lösung aufgesetzt und mit dem Discord Server der Projektgruppe verbunden. Die hier eingesetzte Lösung nennt sich Netdata. Der Netdata Agent ist opensource und kann kostenlos eingesetzt werden, dieser bringt von Haus aus viele Vorlagen mit um das Gesamtsystem gut zu überwachen und Warnungen, sowie Fehler proaktiv an die Administratoren zu melden. Taucht ein Fehler auf dem Server auf, so wird in der hier verwendenten Konfiguration, direkt eine Nachricht auf dem Discord der Projektgruppe gesendet.  

### Einrichtung der Webanwendung

Nach der erfolgreichen Grundinstallation kann mit dem Aufsetzen der Testumgebung der Webanwendung begonnen werden. 
Dafür werden zuerst die Pakete git und docker über den apt Packetmanager installiert. 


Docker

### Datensicherung und Monitoring
Der Zweck der VM ist primär die Entwicklung der Webanwendung und somit nicht der produktive Einsatz. Da der Quellcode der Webanwendung über Git verwaltet wird und die Daten innerhalb der Datenbank reine Testdaten sind, wurde auf das einrichten einer Datensicherung verzichtet. 

Für eine produktive Umgebung ist eine sorgfältig überlegte Backupstrategie unabdingbar. Hierbei sollte genaustens überlegt werden, wie der Backupprozess implementiert und automatisiert wird und wie erstellte Backups auf Konsistenz und wiederherstellbarkeit überprüft werden können. Auch der Speicherort von Backups sollte bedacht werden und der 3-2-1 Regel folgen. 

Auch wurde keine Monitoringlösung verwendet um den Zustand der VM und der darauf laufenden Dienste zu überwachen, auch hier ist es sinnvoll ein Konzept für die Produktivumgebung auszuarbeiten. 

