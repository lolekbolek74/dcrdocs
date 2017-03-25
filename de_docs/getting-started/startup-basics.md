# Startup Basics

Diese Seite wurde zuletzt für die Version v0.8.2 aktualisiert.

---

Diese Anleitung ist für Nutzer der Kommandozeile gedacht. Paymetheus Nutzer können das Anpassen der Konfigurationsdateien ignorieren - Paymetheus kümmert sich selbstständig um die Konfiguration. Es ist weiterhin zu erwähnen das einige Anleitungen sich auf die Konfigurationsdateien und andere sich wiederrum auf die Startparameter der Kommandos beziehen. 

---

## Konfigurationsdateien

Die Decred Software liest beim start Konfigurationsdateien ein um zu bestimmen unter welchen Einstellungen es jeweilige Funktionen aktivieren/deaktivieren soll. Alle Startparameter können entweder als Parameter zum Start mitgegeben werden `(z.B. dcrwallet --testnet)` oder wahlweise in der jeweiligen Konfigurationsdatei hinterlegt werden `(z.B. dcrwallet --testnet könnte mit dem Parameter testnet=1 in der Konfigurationsdatei dcrwallet.conf ersetzt werden)`.

Diese Konfigurationsdateien befinden sich im jeweiligen Anwendungsverzeichnis. Der Ort dieses Anwendungsverzeichnis für Windows, macOS/OSX, und Linux wird nachfolgend aufgelistet:

Windows:

    C:\Users\<username>\AppData\Local\Dcrwallet\
    C:\Users\<username>\AppData\Local\Dcrd\
    C:\Users\<username>\AppData\Local\Dcrctl\ 

macOS: 

    ~/Library/Application Support/Dcrwallet/
    ~/Library/Application Support/Dcrd/
    ~/Library/Application Support/Dcrctl/
    
Linux: 
    
    ~/.dcrwallet/
    ~/.dcrd/
    ~/.dcrctl/

Jedes dieser Verzeichnisse enthält die jeweilige `.conf` Datei, benannt nach der jeweiligen Anwendung (`z.B. dcrd nutzt die Konfigurationsdatei dcrd.conf`). Es ist weiterhin anzumerken das `Dcrd` und `Dcrwallet` die jeweiligen Anwendungsverzeichnisse zur Speicherung der Konfigurationsdateien beim ersten Start selbstständig erstellt. Das Anwendungsverzeichnis für `Dcrctl` müssen Sie selbstständig anlegen um eine Konfigurationsdatei zu hinterlegen.

Die [dcrinstall](/getting-started/install-guide.md#dcrinstall) und [Binary Release](/getting-started/install-guide.md#binary-releases) Version enthalten bereits Beispielkonfigurationen. Es wird empfohlen diese Beispielkonfigurationen in die oben erwähnten Verzeichnisse zu kopieren und diese Umzubenennen, entfernen Sie dazu das vorangehende 'sample-' im Dateinamen. Diese Konfigurationsdateien haben viele Einstellungen auskommentiert (Kommentare werden durch die Software ignoriert beim Start ignoriert) so das alle Einstellungen zu anfang deaktiviert sind. Sie können diese vorgefertigten Einstellungen aktivieren indem Sie das Semikolon am jeweiligen Zeilenanfang entfernen.

---

## Startparameter

Der Grossteil der Einstellungen kann über die Konfigurationsdateien bestimmt werden oder als Parameter zum Start der Anwendung mitgegeben werden. Nachfolgend ein Beispiel eines Startparameters für das jeweilige Betriebssystem um `dcrd` im Testnet zu starten, als Alternative kann `testnet=1` in der Konfigurationsdatei von `dcrd` hinterlegt werden:

    Windows: dcrd.exe --testnet
    macOS: ./dcrd --testnet
    Linux: ./dcrd --testnet

Dieses Beispiel würde zuerst die `dcrd` Konfigurationsdatei mit den jeweiligen Einstellungen einlesen und anschließend diese mit den mitgegebenen Startparametern überschreiben.

---

## Fortgeschrittene Nutzung

[Logindaten in den Konfigurationsdateien hinterlegen](/advanced/storing-login-details.md)

[Eine komplette Übersicht der Optionen für jede Anwendung](/advanced/program-options.md)
