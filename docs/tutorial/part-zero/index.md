---
title: Setz deine eigene Entwicklungsumgebung auf
typora-copy-images-to: ./
disableTableOfContents: true
---

Bevor du anfängst deine erste Seite mit Gatsby zu bauen, solltest du dich mit einigen Kern-Webtechnologien vertraut machen und sicherstellen, dass alle notwendigen Softwarewerkzeuge installiert sind.

## Mache dich mit der Kommadozeile vertraut

Die Kommandozeile ist eine textbasierte Schnittstelle, die zum Ausführen von Kommandos auf deinem Computer da ist. Diese wird des Öfteren auch
Terminal genannt. In dieser Anleitung werden wir beide Begriffe abwechselnd verwenden. Es ist der Verwendung von Finder auf einem Mac, oder dem
Explorer auf Windows ähnlich. Finder und Explorer sind Beispiele einer grafischen Benutzerobefläche (GUI). Die Kommandozeile ist ein mächtiges, textbasierte Werkzeug, um mit deinem Computer zu interagieren.

Nimm dir einen Moment Zeit, um die Kommandozeilenschnittstelle (CLI) auf deinem Computer zu finden. Abhängig von deinem Betriebssystem, orientiere dich an [**Anleitung für Mac**](http://www.macworld.co.uk/feature/mac-software/how-use-terminal-on-mac-3608274/), [**Anleitung für Windows**](https://www.quora.com/How-do-I-open-terminal-in-windows) oder [**Anleitung für Linux**](https://www.howtogeek.com/140679/beginner-geek-how-to-start-using-the-linux-terminal/).

## Installieren von Homebrew für Node.js

Für die Installation von Gatsby und Node.js, ist die Nutzung von [Homebrew](https://brew.sh/) ratsam. Die Einrichtung am Anfang kann dich vor späteren Kopfzerbrechen bewahren!

Wie installierst, oder verifizierst du Homebrew auf deinem Computer:

1. Öffne dein Terminal.
1. Überprüfe ob Homebrew bereits installiert ist, in dem du `brew -v` ausführst. Du solltest dann "Homebrew" und eine Versionsnummer sehen.
1. Wenn nicht, lade und installiere [Homebrew mit der passenden Anleitung](https://docs.brew.sh/Installation) für dein Betriebssystem (Mac, Linux oder Windows).
1. Nach dem du Homebrew installiert hast, wiederhole Schritt 2 um dies sicherzustellen.

### Mac Nutzer: Installation von Xcode Command Line Tools

1. Öffne dein Terminal.
1. Installiere die Xcode Command Line Tools durch das Ausführen von `xcode-select --install` auf einem Mac.
   1. Wenn dies nicht gelingt, lade dir diese [direkt von der Apple Website](https://developer.apple.com/download/more/) herunter, nach dem du dich mit einem Apple Entwicklerkonto angemeldet hast.
1. Nach der Aufforderung zum Starten der Installation, wirst du erneut Aufgefordert die Softwarelizenz für die zu installierenden Tools zu akzeptieren.

## ⌚ Installiere Node.js und npm

Node.js ist eine Umgebung, die JavaScript außerhalb eines Web-Browsers ausführen kann. Gatsby wurde mit Node.js gebaut. Damit du Startklar für Gatsby bist, sollte eine neuere Version auf deinem Computer installiert sein.

_Hinweis: Gatsby's minimal unterstützte Node.js Version ist Node 8, du kannst aber ruhig eine neuere Version verwenden._

1. Öffne dein Terminal.
1. Führe `brew update` aus, um sicherzustellen, dass du die neueste Version von Homebrew hast.
1. Führe folgenden Befehl aus, um Node und npm in einem Zug zu installieren: `brew install node`

Sobald du die Installationsschritte abgeschlossen hast, stelle sicher dass alles ordentlich installiert wurde:

### Überprüfe deine Node.js Installation

1. Öffne dein Terminal.
2. Führe `node --version` aus. (Wenn du noch nicht mit der Kommandozeile vertraut bist, "Führe `Kommando` aus" bedeutet "Tippe `node --version` in die Kommandozeile ein und drücke die Enter Taste".
Ab hier ist es das, was wir mit "Führe `Kommando` aus" meinen).
3. Führe `npm --version` aus.

Die Ausgabe der einzelnen dieser Kommandos sollte eine Versionsnummer sein. Deine Versionen könnten nicht mit den unten gezeigten übereinstimmen! Wenn die Eingabe dieser Kommandos, dir keine Versionsnummer zeigt, gehe zurück und stelle sicher, dass du Node.js installiert hast.

![Überprüfen von node und npm Versionen im Terminal](01-node-npm-versions.png)

## Installiere Git

Git ist ein freies, Open-Source Versionsverwaltungssystem, welches für schnelle und effiziente Abwicklung von kleinen und großen Projekten gestaltet wurde. Wenn du eine Gatsby "starter" Seite installierst, wird Git von Gatsby im Hintergrund verwendet, um die notwendigen Dateien herunterzuladen und zu installieren. Du wirst Git benötigen, um deine erste Gatsby Seite aufsetzen zu können.

Die Schritte für das Herunterladen und Installieren von Git, hängen von deinem Betriebssystem ab. Folge der für dein System passender Anleitung:

- [Installieren von Git auf macOS](https://www.atlassian.com/git/tutorials/install-git#mac-os-x)
- [Installieren von Git auf Windows](https://www.atlassian.com/git/tutorials/install-git#windows)
- [Installieren von Git auf Linux](https://www.atlassian.com/git/tutorials/install-git#linux)

## Nutzung der Gatsby CLI

Das Gatsby CLI Tool ermöglicht dir das schnelle Erstellen neuer Gatsby-betriebenen Seiten und das Ausführen von Kommandos für die Entwicklung von Gatsby Seiten. Es ist ein veröffentlichtes npm Paket.

Das Gatsby CLI is via npm verfügbar und sollte global, durch das Ausführen von `npm install -g gatsby-cli`, installiert werden.

_**Hinweis**: Wenn du Gatsby installierst und zum ersten Mal ausführst, wirst du eine kurze Nachricht sehen, die dich über anonyme Verwendung von Daten, die für Gatsby Kommandos gesammelt werden, informiert. Du kannst mehr über die Art und Weise der Datenerfassung, sowie den Verwendungszweck der Daten in der [Telemetriedokumentation](/docs/telemetry) nachlesen._

Um zu sehen welche Kommandos dir zur Verfügung stehen, führe den Befehl `gatsby --help` aus.

![Überprüfe die Gatsby Kommandos im Terminal](05-gatsby-help.png)

> 💡 Wenn es dir nicht gelingen sollte, Gatsby CLI wegen Probleme mit den Zugriffsrechten auszuführen, könntest du dir die [npm Dokumentation über die Reparatur der Zugriffsrechte](https://docs.npmjs.com/getting-started/fixing-npm-permissions), oder [diese Anleitung](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md) ansehen.

## Erstellen einer Gatsby Seite

Jetzt bist du für die Nutzung des Gatsby CLI Tools für die Erstellung deiner ersten Gatsby Seite bereit. Mithilfe des Tools, kannst du sogenannte Vorlagen ("starters") herunterladen (teilweise aufgebaute Seiten mit vordefinierter Konfiguration), um mit dessen Hilfe einen schnellen Start bei der Erstellung einer bestimmten Seitenart zu gewährleisten. Die "Hello World" Vorlage im folgenden Beispiel beinhaltet nur das Notwendigste für eine Gatsby Seite.

1. Öffne dein Terminal.
2. Führe `gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world` aus. (_Hinweis: Die benötigte Zeit für diesen Vorgang ist von deiner Download-Geschwindigkeit abhängig. Der Kürze halber, wurde das gif unterhalb während der Installation pausiert_).
3.  Führe `cd hello-world` aus.
4.  Führe `gatsby develop` aus.

<video controls="controls" autoplay="true" loop="true">
  <source type="video/mp4" src="./03-create-site.mp4" />
  <p>Entschuldige! Dein Browser unterstützt dieses Video nicht.</p>
</video>

Was ist gerade passiert?

```shell
gatsby new hello-world https://github.com/gatsbyjs/gatsby-starter-hello-world
```

- `new` is ein gatsby Befehl um ein neues Gatsby Projekt anzulegen.
- In diesem Beispiel, ist `hello-world` ein willkürlicher Titel - du kannst einen beliebigen wählen. Das CLI Tool wird den Quellcode für deine neue Seite in einen neuen Ordner namens "hello-world" platzieren.
- Abschließend, die angegebene GitHub URL verweist auf ein Quellcode-Repository, welches den Quellcode der von dir benutzten Vorlage beinhaltet.

```shell
cd hello-world
```

- Dies bedeutet 'Ich will einen Verzeichniswechsel (`cd`) ins "hello-world" Unterverzeichnis durchführen'. Immer wenn du Kommandos für deine Seite ausführen möchtest, musst du dich im Kontekt für diese Seite befinden (d.h. dein Terminal muss auf das Verzeichnis gerichtet werden, wo sich der Quellcode deiner Seite befindet).

```shell
gatsby develop
```

- Dieser Befehl startet den Entwicklungsserver. Dadurch hast du die Möglichkeit, deine neue Seite in der lokalen (auf deinem Computer, nicht im Internet veröffentlicht) Entwicklungsumgebung zu sehen und damit zu interagieren.

### Schau dir deine Seite lokal an

Öffne einen neuen Tab in deinem Browser und navigiere zu [**http://localhost:8000**](http://localhost:8000/).

![Schau dir die Homepage an](04-home-page.png)

Gratulation! Dies ist der Anfang deiner ganz ersten Gatsby Seite! 🎉

Du hast die Möglichkeit deine Seite lokal auf [**_http://localhost:8000_**](http://localhost:8000/) aufzurufen, solange dein Entwicklungsserver in Betrieb ist. Das ist der Prozess, den du durch das Ausführen von `gatsby develop` gestartet hast. Um die Ausführung des Prozesses zu beenden (oder um den "Betrieb des Entwicklungsservers einzustellen"), gehe zurück zum Terminalfenster, halte die "Steuerung" Taste gedrückt und drücke danach "C" (Strg-C). Für ein erneutes Starten, führe wieder `gatsby develop` aus!

**Note:** Wenn du ein Setup aus virtuellen Umgebungen (VM) wie `vagrant` hast und/oder der Server auf deine lokale IP-Adresse verweisen soll, führe `gatsby develop -- --host=0.0.0.0` aus. Jetzt wird der Server sowohl auf `localhost`, als auch auf deine lokale IP reagieren.

## Quellcode-Editor einrichten

Ein Quellcode-Editor ist eine Anwendung, die speziell für die Bearbeitung von Computer-Code konzipert wurde. Es gibt viele großartige da draußen.

### Herunterladen von VS Code

Gatsby Dokumentation enthält manchmal Screenshots, die innerhalb von VS Code gemacht wurden. Falls du noch keinen Quellcode-Editor bevorzugst, wird die Nutzung von VS Code dafür sorgen, dass dein Bildschirm genauso aussieht wie in den Screenshots in der Anleitung und der Dokumentation. Wenn du dich dazu entscheidest VS Code zu nutzen, besuche die [VS Code Website](https://code.visualstudio.com/#alt-downloads) und lade die geeignete Version für dein Betriebssystem herunter.

### Installiere die Prettier Erweiterung

Wir empfehlen die Nutzung von [Prettier](https://github.com/prettier/prettier), ein Tool welches dir hilft deinen Quellcode zu formatieren, um Fehler zu vermeiden.

Du kannst Prettier direkt in deinem Editor mit Hilfe von [Prettier VS Code Erweiterung](https://github.com/prettier/prettier-vscode) nutzen:

1.  Öffne die Erweiterungen Ansicht in VS Code (Viewe => Extensions) .
2.  Suche nach "Prettier - Code formatter".
3.  Klicke "Installieren". (Nach der Installation wirst du aufgefordert VS Code neuzustarten, um die Erweiterung zu aktivieren. Neuere Versionen von VS Code aktivieren die Erweiterung automatisch nach dem Herunterladen.)

> 💡 Wenn du VS Code nicht nutzt, schau dir die Prettier Dokumentation für [Installationsanweisungen](https://prettier.io/docs/en/install.html) oder [Integration mit einem anderen Editor](https://prettier.io/docs/en/editors.html) an.

## ➡️ Wie geht es weiter?

Zusammenfassend, in diesem Abschnitt hast du:
- Über die Kommandozeile und dessen Anwendung gelernt
- Node.js, npm CLI Tool, Versionsverwaltungssystem Git und das Gatsby CLI Tool, installiert und kennengelernt.
- Eine neue Gatsby Seite mit Hilfe des Gatsby CLI Tools generiert
- Den Gatsby Entwicklungsserver ausgeführt und deine Seite lokal besucht
- Einen Quellcode-Editor heruntergeladen
- Einen Quellcode-Formatierer namens Prettier installiert

Jetzt, geht es weiter mit dem [**Kennenlernen der Gatsby Bausteine**](/tutorial/part-one/).

## Referenzen

### Übersicht der Kern-Technologien

Es ist nicht notwendig ein Experte in folgenden Gebieten zu sein - wenn du keiner bist, mach dir keine Sorgen! Du wirst viel im Laufe dieser Anleitung lernen. Folgend sind einige Kern-Webtechnologien, die du nutzen wirst, wenn du eine Seite mit Gatsby baust:

- **HTML**: Eine Auszeichnungssprache die jeder Browser versteht. Die Abkürzung steht im Englischen für HyperText Markup Language. HTML verschafft deinen Webinhalten eine Informationsstruktur, die durch das Definieren von Überschriften, Paragraphen und weiteren Elementen, entsteht.
- **CSS**: Eine repräsentative Sprache, die für das Aussehen deiner Webinhalte (Schriften, Farben, Layout, etc.). Das Akronym steht für Cascading Style Sheets.
- **JavaScript**: Eine Programmiersprache die uns hilft, das Web dynamisch und interaktiv zu gestalten.
- **React**: Eine Quellcode-Bibliothek (gebaut mit JavaScript) für die Erstellung von Benutzeroberflächen. Es ist ein Framework welches von Gatsby für die Erstellung von Seiten und strukturierten Inhalten verwendet wird.
- **GraphQL**: Eine Abfragensprache, die es ermöglicht, deine Website mit Daten zu versorgen. Es ist die Schnittstelle, die von Gatsby für das Verwalten von Seitendaten verwendet wird.

### Was ist eine Website?

Für eine umfassende Einführung zum Thema Website--inklusive einer Intro zu HTML und CSS--siehe “[**Baue deine erste Website**](https://learn.shayhowe.com/html-css/building-your-first-web-page/)”. Es ist ein idealer Ausgangspunkt, um über das Web zu lernen. Für etwas praktische Einführung zu [**HTML**](https://www.codecademy.com/learn/learn-html), [**CSS**](https://www.codecademy.com/learn/learn-css), und [**JavaScript**](https://www.codecademy.com/learn/introduction-to-javascript), siehe die Tutorials von Codecademy. [**React**](https://reactjs.org/tutorial/tutorial.html) und [**GraphQL**](http://graphql.org/graphql-js/) haben ebenso ihre eigenen Tutorials zur Einführung.

### Lerne mehr über die Kommandozeile

Für eine tolle Einführung zur Kommandozeile, siehe [**Codecademy’s Kommandozeile-Tutorial**](https://www.codecademy.com/courses/learn-the-command-line/lessons/navigation/exercises/your-first-command) für Mac und Linux Nutzer, und [**dieses Tutorial**](https://www.computerhope.com/issues/chusedos.htm) for Windows Nutzer. Selbst wenn du ein Windows Nutzer bist, die erste Seite des Codecademy Tutorials ist sehr lesenswert. Darin wird auch die Kommandozeile selbst und nicht nur die Interaktion mit dieser, erklärt.

### Lerne mehr über npm

npm ist ein JavaScript Paketmanager. Ein Paket ist ein Quellcode-Modul, welches du in deinen Projekten einbinden kannst. Wenn du nur Node.js heruntergeladen und installiert hast, dann wurde npm auch mitinstalliert!

npm besteht aus drei unterschiedlichen Komponenten: die npm Website, das npm Register und die npm Kommandozeilenschnittstelle (CLI).

- Auf der npm Website kannst du nachsehen, welche JavaScript Pakete im npm Register verfügbar sind.
- Das npm Register ist eine große Datenbank, die Informationen über die auf npm verfügbaren JavaScript Pakete, beinhaltet.
- Sobald du ein gewünschtes Paket gefunden hast, kannst du die npm CLI nutzen, um es in deinem Projekt oder global (sowie andere CLI Tools), installieren. Die npm CLI ist das Sprachrohr zum Register - grundsätzlich, interagierst du nur mit der npm Website oder der npm CLI.

> 💡 Schau dir die npm Einführung zu “[**Was ist npm?**](https://docs.npmjs.com/getting-started/what-is-npm)” an.

### Lerne mehr über Git

Du wirst Git nicht brauchen um dieses Tutorial abzuschließen, es ist jedoch ein sehr praktisches Hilfsmittel. Wenn du interessiert bist, mehr über Versionskontrolle, Git und Github zu lernen, schau dir das [Git Handbuch](https://guides.github.com/introduction/git-handbook/) von GitHub an.
