# Handbuch

## Aufsetzen des Linux Servers
**Mario Wegmann**

In der folgenden Anleitung werden Platzhalter mit <Platzhaltername> markiert. 
### Grundinstallation
// TODO
NETDATA

sudo apt-get install git

### Testumgebung für Entwicklung
// TODO
Zu beginn muss Node.js installiert werden. 
Da über den apt Packetmanager nur veraltete Versionen von Node.js bereitgestellt werden, wird hier der Node Version Manager verwendet. 

Dieser lässt sich über folgendes Bash Skript installieren. 
`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash`
Nach der Installation empfiehlt es sich die SSH Sitzung neu zu starten, damit der `nvm` Befehl auch erkannt wird. 
Anschließend kann mit `nvm install 20` die LTS-Version Node.js 20 installiert werden. 
Mit Node.js kommt auch der `npm` Packetmanager. Mit disem lässt sich React und Next.js installieren. 
`npm install next@latest react@latest react-dom@latest`

Als nächstes muss ein SSH Key für Github hinterlegt werden, damit das Repository geklont werden kann. 
Dafür wird als erstet ein SSH Key generiert. 
Es empfiehlt sich dabei auch ein Passphrase zu vergeben und beim Speicherort einen eindeutigen Namen zu vergeben. 
`ssh-keygen -t ed25519 -C "<Github E-Mail Adresse>"`
Als nächstes wird der SSH Agent einmal gestartet um anschließend den SSH Key beim SSH Agent hinterlegen zu können. 
`eval "$(ssh-agent -s)"`
Beim hinzufügen muss auch die zuvor festgelegte Passpharse eingegeben werden. 
`ssh-add <Speicherort des zuvor erstellten SSH Keys angeben>`

Der Public Teil des SSH Keys muss auch im Github Account hinterlegt werden. 
Dafür die URL https://github.com/settings/keys aufrufen und einen neuen SSH Key hinzufügen. 

Nun kann das Repository der Webanwendung geklont werden. 
`git clone git@github.com:THA-LPRD/web.git lprd`

Danach wird das Verzeichnis von der Next.js Anwendung betreten.
`cd lprd/lprd-server`

Die Anwendung verwendet die offizielle Schriftart der THA. Die Schriftart TWK Everett darf wegen der, von der THA erworbenen, Lizenz jedoch nur Studierenden und Mitarbeitern der Technischen Hochschule Augsburg zur verfügung gestellt werden. Die Schriftart lässt sich unter folgender URL herunterladen: https://www.tha.de/Kommunikation/Corporate-Design.page 
Anschließend müssen die zwei Schriftfamilien TWKEverett-Bold-web.ttf und TWKEverett-Medium-web.ttf TWKEverett-Medium-web.ttf müssen im Ordner lprd-server/components/fonts kopiert werden. 

Als nächstes kann die PostgreSQL Datenbank aufgesetzt werden. 
Dafür kann das Docker Image oder auch ein bestehender PostgreSQL Server verwendet werden. 
`sudo docker run --name lprd-postgres -p 5432:5432 -e POSTGRES_PASSWORD=<SicherersDatenbankPasswort> -d postgres`

Die URL der Datenbank muss auch noch der Next.js Anwendung bekannt gemacht werden, dies geschieht über die .env Datei. 
Diese sollte neue angelegt werden und den folgenden Inhalt enthalten: 
`DATABASE_URL="postgresql://<PostgresUser>:<PostgresUserPassword>@<PostgresServerIP/Hostname>:5432"`

Nach der Installation der Datenbank kann diese mit Prisma mit den notwendigen Tabellen befüllt werden. 

`npx prisma migrate dev --name init`

Die Vorbereitungen sind somit abgeschlossen und der Developmentserver kann gestartet werden.

`npm run dev`

Unter http://localhost:3000 ist der Server nun erreichbar. 

Der Developmentserver kann mit dem Tastenkürze Ctrl+C beendet werden. 

### Produktivumgebung bauen

// TODO Was mit Font?
docker build -t nextjs-docker .
docker run -p 80:3000 nextjs-docker

### Produktivumgebung starten

// TODO
CADDY
Cert

sudo apt-get install docker

## Verwenden der Webanwendung
**Mario Wegmann**

### Unterseiten

Nachdem die Anwendung gestartet wurde kann die Adresse im Browser eingegeben werden. Die Startseite zeigt das Menü für die Unterseiten an. Es gibt zwei Unterseiten, unter "Displays" werden alle bereits bekannten Displays aufgelistet. In der Unterseite "Assets" werden alle vorhanden Assets angezeigt.

// TODO Grafik

### Neues Asset erstellen

Es gibt zwei Möglichkeiten ein Asset zu erstellen, es kann entweder ein fertiges PNG hochgeladen werden, oder ein PNG aus einem HTML Code erstellt werden. 

// TODO Grafik


**PNG hochladen**

Ein PNG kann auf der Unterseite Assets über den "Hochladen"-Knopf hochgeladen werden. 
Bei hochladen muss darauf geachtet werden, dass das PNG in der richtigen Auflösung für das Display ist, welches später das Asset anzeigen soll. Ebenso kann ein Name für das Asset und wie lange es angezeigt werden soll angegeben werden. Das hochladen beginnt mit einem Druck auf den "Hochladen"-Knopf.  

// TODO Grafik

**PNG aus HTML erstellen**
Auf der Unterseite Assets gibt es auch den "Erstellen aus HTML"-Knopf, dieser öffnet ein Formular, in dem der Assetname, die Anzeigedauer und der HTML Code eingegeben werden kann. Nach dem druck auf den "Generieren"-Knopf wird ein PNG erstellt und lokal abgelegt. 


// TODO Grafik

### Vorhandenes Asset bearbeiten

In der "Assets" Übersichtsseite kann jedes vorhandene Asset ausgewählt werden um eine Detailansicht anzuzeigen. Dort können der Name, die Anzeigedauer und der HTML Code bearbeitet werden. 
Ebenso kann ein Asset auch gelöscht werden. 

### Neues Displaymodul verbinden

Beim erstmaligen einschalten eines Displaymoduls, nach dem flashen, kann in der Einrichtungsseite des Displaymoduls der Servermodus als Betriebsmodus ausgewählt werden. Ebenso kann die Server URL im dazugehörigen Textfeld angegeben werden. 

Die weiteren Einstellungen verhalten sich gleich wie auch bei der Einrichtung vom Netzwerkmodus bereits erläutert wurde. 

Nachdem die Erstkonfiguration gespeichert und das Displaymodul neu gestartet wurde, versucht es sich automatisch mit dem eingetragenen WLAN und anschlißend mit dem eingetragenen Server zu verbinden. 

Falls das Displaymodul sich zum ersten mal mit diesem Server verbindet, wird es automatisch in der Datenbank eingetragen, anschließend geht das Display in den Deep-sleep Modus. 

// TODO Grafik


### Neues Asset auf dem Display anzeigen

Sobald ein Displaymodul sich in der Webanwendung registriet hat, kann in der Webanwendung das Display ausgewählt werden. Hier können grundlegene Informationen zum Display bearbeitet und ein neues aktives Asset gesetz werden. 

Mit einem Tastendruck auf den vorderseitigen Knopf, kann das Display aus dem Deep-sleep Modus wieder aufgeweckt werden. Immer nach dem Aufwecken versucht das Displaymodul sich mit dem Server zu verbinden und eine neue Konfiguration zu erhalten. Die Konfiguration enthält die URL des aktuell anzuzeigenden Assets und eine Dauer in Sekunden, die angiebt, wie lange das Asset angezeigt werden soll. 

Das Displaymodul lädt anschließend das Asset von der angegebenen URL herunter, zeigt es an und versetzt sich anschließend wieder in den Deep-sleep Modus. Zusätzlich wird noch ein Wakeup Timer auf die angegebene Dauer gesetzt. Dieser Timer weckt somit das Displaymodul automatisch nach ablauf der Anzeigedauer auf, damit sich das Displaymodul ein neues anzuzeigendes Asset herunterlädt.  

### Vorhandenes Display bearbeiten

Ähnlich wie bei der Assets Übersicht, können auch die Displays in der "Display"-Unterseite bearbeitet werden. In der Detailansicht eines Displays kann die MAC-Adresse und der Zeitpunkt, zu dem sich das Display zum letzen mal beim Server gemeldet hat, eingesehen werden. Der Name des Displays und die Auflösung können bearbeitet werden. 

Zuletzt kann ein Display auch wieder gelöscht werden. 

## Quellen
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux#generating-a-new-ssh-key 
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
