# Siedler 4 Auswahllimit-Entferner

Standardmäßig können maximal nur 100 Einheiten selektiert werden. Diese Modifikation versucht, die Beschränkung aufzuheben, sodass große Armeen mit Leichtigkeit verwaltet werden können.

![186-units-selected](units-selected.png)

Für dieses README gibt es eine [englische Version](README.md). Bitte beachte, dass die deutsche Übersetzung ggf. veraltet sein kann.



## Features

* Erhöhe das Einheitenauswahllimit auf 2500 Einheiten pro Auswahl
* Erhalte neue Filtermöglichkeiten für Auswahlen:
  * Du kannst mit der rechten oder linken Maustaste auf Einheiten-Icons im Menü klicken, um sie in die Auswahl ein- oder auszuschließen.
  * Du kannst mit der rechten Maustaste auf die rote Plus-Taste klicken, um alle verwundeten Einheiten abzuwählen (ein Linksklick dagegen wählt alle verwundeten Einheiten aus).
  * Du kannst mit der rechten Maustaste auf die Gruppen-Menüschaltfläche klicken, um alle Einheiten abzuwählen, die bereits einer Gruppe zugeordnet sind.
* Kompatibilität: Die Mod läuft sowohl mit der Gold Edition als auch der History Edition von Die Siedler 4
* Mehrspieler-Interoperabilität: Du kannst im Mehrspieler-Modus mit Teilnehmern spielen, die diesen Mod nicht verwenden.
* Open Source: Die meisten Teile des Projekts, einschließlich Muster, Offsets, Enums und Structs, werden bald quelloffen sein!



## Installation

Es gibt zwei Methoden, wie Du diesen Mod verwenden kannst. Wenn Du ein Entwickler bist oder die Mod nur schnell ausprobieren möchtest, solltest Du den mitgelieferten Injektor verwenden (Methode 1). Der Injector richtet sich hauptsächlich an Entwickler, um ein schnelles Laden und Entladen der Mod zu ermöglichen, ohne dass das Spiel für jeden Build neu gestartet werden muss. Methode 2 ist eher für Endbenutzer geeignet, die möchten, dass die Mod immer dann geladen wird, wenn das Spiel startet. Du kannst dafür einen ASI-Loader verwenden. 

#### Methode 1: Injector

1. [Lade ein Release hier herunter](https://github.com/nyfrk/S4_UnlimitedSelection/releases), entpacke es und kopiere die Dateien wohin Du möchtest. Die enthaltenen Dateien `Injector.exe` und `S4_UnlimitedSelection.asi` müssen lediglich im selben Verzeichnis liegen. 
2. Starte die Datei `Injector.exe` durch einen Doppelklick. Ein Konsolenfenster öffnet sich.
3. Starte das Spiel und warte, bis das Konsolenfenster eine erfolgreiche Injektion bestätigt.
4. Schließe das Konsolenfenster. Die Mod wird weiterhin aktiv bleiben. 

Der Injektor beginnt mit der Injektion der DLL, sobald das Spiel gestartet wird. Achte darauf, dass die Datei `S4_UnlimitedSelection.asi` **nicht umbenannt** wird, wenn Du meinen Injektor verwendest. Andernfalls wird der Injektor sie nicht finden.

#### Methode 2: ASI Loader

Der Vorteil der Verwendung eines ASI-Loaders besteht darin, dass Du mehrere Mods installieren kannst, indem Du sie einfach in ein festgelegtes Verzeichnis einfügst. Ich empfehle den [The Settlers 4: ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader), da er gut mit der Gold und History Edition von Die Siedler 4 funktioniert und keinerlei Konfiguration erfordert. Wenn Du bereits einen ASI-Loader installiert hast, überspringe die ersten Schritte und fahre direkt mit Schritt 5 fort.

1. Navigiere zum Installationsverzeichnis des Spiels.
2. Suche eine Datei namens `binkw32.dll` und benennen sie in `binkw32Hooked.dll` um. (Bei der Gold Edition befindet sie sich in einem Unterverzeichnis namens `Exe`)
3. Lade ein [Release des ASI Loaders](https://github.com/nyfrk/Settlers4-ASI-Loader/releases) herunter und entpacke die `binkw32.dll` in dasselbe Verzeichnis.
4. Erstellen ein Verzeichnis namens `plugins` neben der `S4_Main.exe`.
5. Lade eine Version des [Unlimited Selection Mod](https://github.com/nyfrk/S4_UnlimitedSelection/releases) herunter. Entpacke die Datei `S4_UnlimitedSelection.asi` in das Verzeichnis `plugins`. Beachte, dass die `Injector.exe` nicht erforderlich ist. 
6. Starte das Spiel. Die Mod sollte nun automatisch geladen werden.

Um die Mod zu deinstallieren, entferne die `S4_UnlimitedSelection.asi` aus dem `plugins`-Verzeichnis. Wenn Du den ASI-Loader nicht mehr verwenden möchtest, kannst Du einfach alle Schritte wieder rückgängig machen. 



## Bekannte Probleme

* Gruppenzuweisungen sind nach wie vor auf maximal 100 Einheiten pro Gruppe beschränkt.
* Uplay stört die Injektion bei Spielbeginn. Sollte die Mod nicht geladen werden, starte den Injektor einfach nochmal, nachdem das Spiel gestartet ist.



## Probleme und Fragen

Das Projekt verwendet den Github Issue Tracker. Bitte öffne [hier](https://github.com/nyfrk/Settlers4-UnlimitedSelectionMod/issues) ein Ticket für dein Anliegen. 



## Mitmachen

Das offizielle Repository dieses Projekts ist unter https://github.com/nyfrk/Settlers4-UnlimitedSelectionMod verfügbar. Du kannst auf die folgenden Arten einen Beitrag leisten:

* Beantworte Fragen
* Fehler melden oder bei der Verifizierung dieser helfen
* Code sichten und die vorgeschlagenen Korrekturen testen
* Pull Requests einreichen

##### Kompilieren

Lade Visual Studio 2017 oder 2019 mit der C++-Toolchain herunter. Das Projekt ist so konfiguriert, dass es mit der Windows XP-kompatiblen **v141_xp**-Toolchain gebaut wird. Du solltest jedoch die Toolchain nach Belieben ändern können. Es sind keine zusätzlichen Bibliotheken erforderlich, sodass das Projekt ohne weiteres gebaut werden kann. Wenn Du Rendering-Funktionen (wie für Menüs, Text usw.) verwenden möchtest, musst Du das [neueste DirectX 9 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=6812) installieren. Dennoch kann der Code auch ohne das SDK kompiliert werden, da die Rendering-Teile einfach übersprungen werden, falls das SDK fehlt. 

##### Zukünftige Arbeit

* Ein Framework. Einige Hooks sind auch für andere Mods interessant. Vor allem der Tick Hook, mit dem man eigene Events auslösen kann. 

  Es ist eine gute Idee, eine shared Library und eine API für Plugins zu erstellen. Das Erstellen von Plugins würde einfacher werden, da das Framework alle Hooks, Patches und das Struct-Mapping verwalten könnte, während Plugin-Entwickler nur auf die API des Frameworks zugreifen müssten. Dies würde Inkompatibilitäten zwischen Mods verringern, da die shared Lib die Hooks an mehrere Plugins delegieren könnte. Wenn Du also Teile dieses Projekts (insbesondere dieselben Hooks/Patches) für Dein eigenes Projekt verwendest, ziehen bitte in Betracht, es auch open source zu machen, damit wir später alles auf eine shared Lib umrüsten können. 



## Lizenz

Das Projekt ist unter der [MIT](LICENSE.md)-Lizenz lizenziert. 

