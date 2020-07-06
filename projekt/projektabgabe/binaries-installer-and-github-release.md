# 🚩📖 Binaries, Installer & GitHub Release

## Binaries

Binaries sind die Dateien, welche zur Ausführung des Programmes benötigt werden. Bei WinForms sind folgende Dateitypen in den Binaries zu finden:

* .exe - Ausführbare Datei
* .dll - Code-Library
* .pdb - Debug-Informationen
* .exe.config - Config-Datei für .exe
* .xml - Hier: XML-Kommentare

Diese Binaries liegen, nachdem man im Visual Studio den Build ausgeführt hat, entweder unter `bin\Debug` oder `bin\Release`. Der Ort hängt von der Build-Konfiguration ab. Diese kann wie folgt eingestellt werden:

![Einstellung Debug oder Release](../../.gitbook/assets/grafik%20%285%29.png)

Der Release-Build ist besser optimiert als der Debug-Build, kann jedoch weniger gut debugged werden. Empfohlen für die Abgabe ist der Release Build.

![Beispiel der Binaries des Projekts M318.Exercises.Nr5 in der Projektmappe M318.Exercises](../../.gitbook/assets/grafik%20%289%29.png)

### Installer

Der Installer ist ein Bonuspunkt für schnelle. Dieser muss ohne Unterstützung des Kursleiters/der Kursleiterin umgesetzt werden.

## GitHub Release

Die Binaries oder der Installer müssen für den Kursleiter/die Kursleiterin öffentlich zugänglich zur Verfügung gestellt werden. Die Empfohlene Variante ist GitHub Release. [Hier ](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository)kann eine Anleitung dazu gefunden werden. Die Binaries oder der Installer sollen in einer .zip-Datei hochgeladen werden.

