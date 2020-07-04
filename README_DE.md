# Die Siedler 4: Siedlerlimit Entferner Mod

Standardmäßig können maximal nur 2500 Siedler produziert werden. Diese Modifikation versucht, die Beschränkung aufzuheben, sodass große Armeen erschaffen werden können.

Für dieses README gibt es eine [englische Version](README.md). Bitte beachte, dass die deutsche Übersetzung ggf. veraltet sein kann.



## Features

* Erhöhe das globale Siedlerlimit von 10000 auf 65535 Siedler.
* Erhöhe die maximale Anzahl der Träger von 999 auf 32767.
* Kompatibilität: Die Mod läuft sowohl mit der Gold Edition als auch der History Edition von Die Siedler 4.
* Open Source: Die meisten Teile des Projekts, einschließlich Muster, Offsets, Enums und Structs sind quelloffen!



## Installation

Du benötigst einen ASI Loader um die Mod zu nutzen. Ich empfehle den [The Settlers 4: ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader), da er gut mit der Gold und History Edition von Die Siedler 4 funktioniert und keinerlei Konfiguration erfordert. Wenn Du bereits einen ASI-Loader installiert hast, überspringe die ersten Schritte und fahre direkt mit Schritt 5 fort.

1. Navigiere zum Installationsverzeichnis des Spiels.
2. Suche eine Datei namens `binkw32.dll` und benennen sie in `binkw32Hooked.dll` um. (Bei der Gold Edition befindet sie sich in einem Unterverzeichnis namens `Exe`)
3. Lade ein [Release des ASI Loaders](https://github.com/nyfrk/Settlers4-ASI-Loader/releases) herunter und entpacke die `binkw32.dll` in dasselbe Verzeichnis.
4. Erstellen ein Verzeichnis namens `plugins` neben der `S4_Main.exe`.
5. Lade eine Version des [Siedlerlimit Entferner Mod](https://github.com/nyfrk/S4_SettlerLimitRemover/releases) herunter. Entpacke die Datei `S4_SettlerLimitRemover.asi` in das Verzeichnis `plugins`. 
6. Starte das Spiel. Die Mod sollte nun automatisch geladen werden.

Um die Mod zu deinstallieren, entferne die `S4_SettlerLimitRemover.asi` aus dem `plugins`-Verzeichnis. Wenn Du den ASI-Loader nicht mehr verwenden möchtest, kannst Du einfach alle Schritte wieder rückgängig machen. 



## Bekannte Probleme

* Mehrspieler-Interoperabilität: **Alle Teilnehmern einer Multiplayer-Session müssen die Mod nutzen**. Andernfalls kommt es zu DESYNCs.



## Probleme und Fragen

Das Projekt verwendet den Github Issue Tracker. Bitte öffne [hier](https://github.com/nyfrk/S4_SettlerLimitRemover/issues) ein Ticket für dein Anliegen. 



## Mitmachen

Das offizielle Repository dieses Projekts ist unter https://github.com/nyfrk/S4_SettlerLimitRemover verfügbar. Du kannst auf die folgenden Arten einen Beitrag leisten:

* Beantworte Fragen
* Fehler melden oder bei der Verifizierung dieser helfen
* Code sichten und die vorgeschlagenen Korrekturen testen
* Pull Requests einreichen

##### Kompilieren

Lade Visual Studio 2017 oder 2019 mit der C++-Toolchain herunter. Das Projekt ist so konfiguriert, dass es mit der Windows XP-kompatiblen **v141_xp**-Toolchain gebaut wird. Du solltest jedoch die Toolchain nach Belieben ändern können. Es sind keine zusätzlichen Bibliotheken erforderlich, sodass das Projekt ohne weiteres gebaut werden kann. 



## Lizenz

Das Projekt ist unter der [MIT](LICENSE.md)-Lizenz lizenziert. 



## Danksagungen

Special thanks to [xmorphyx](https://www.gog.com/forum/the_settlers_series/settlers_iv_settler_limit_mod) for the contributions of the AOB Patterns.