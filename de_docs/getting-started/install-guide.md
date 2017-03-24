# Installationsanleitung

Diese Anleitung wurde zuletzt zur v0.8.2 überarbeitet

---

Es gibt vier verschiedene Möglichkeiten die Decred Software herunterzuladen und zu installieren. Die erste Variante wäre der Download von dcrinstall (plattformübergreifend), eine weitere Möglichkeit ist der Windows Installer (Nur für Windows und zur Zeit die einzige Möglichkeit Paymetheus v0.8.2 zu installieren), eine weitere Möglichkeit ist der Download der vorkompilierten Binärdateien (plattformübergreifend) und zu guter letzt die Software im Quelltext herunterzuladen und selbst zu kompilieren (plattformübergreifend). Die ersten drei Methoden werden nachfolgend beschrieben, eine Anleitung zur Kompilierung folgt zu einem späteren Zeitpunkt.

---

## **Paymetheus** 

Die Installationssoftware für Windows (`.msi` Datei) kann hier heruntergeladen werden: [https://github.com/decred/decred-binaries/releases](https://github.com/decred/decred-binaries/releases). Paymetheus wird auf deinem Computer im Programme Ordner installiert. Die Installation ist unkompliziert, nachfolgend eine kurze Anleitung:

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `decred_0.8.2-beta_x86.msi` herunter. <br />
    Für 64-bit Computer, lade `decred_0.8.2-beta_x64.msi` herunter.

2. Navigiere in das Verzeichnis deines Downloads und starte die `.msi` Datei mit einen Doppelklick.

3. Der Installationsassistent wird dich durch den Installationsprozess führen. Während der Installation wirst du aufgefordert die Nutzungs- und Lizenzbedingungen zu akzeptieren.

4. Nach der Installation sollte die Software im `..\Program Files\Decred\` Verzeichniss installiert sein. Es wird eine Verknüpfung im Startmenü hinterlegt (schaue nach der `Decred` Verknüpfung in deiner Programmliste)

---

## **dcrinstall**

`dcrinstall` steht zur automatischen Installation und zum Update der Decred Software bereit. Die aktuellste Version kann hier heruntergeladen werden: [https://github.com/decred/decred-release/releases](https://github.com/decred/decred-release/releases). Binärdateien werden für Windows, OSX/macOS, Linux, OpenBSD und FreeBSD angeboten. Wenn die Installation durchgeführt wird werden `dcrd`, `dcrwallet`, und `dcrctl` auf dem Zielsystem installiert. Anleitungen für die Installation auf dem Mac, Linux und Windows werden nachfolgend beschrieben (Wir gehen davon au dass *BSD Nutzer selbstständig klar kommen).

> OSX/macOS:

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `dcrinstall-darwin-386-v0.8.2` herunter. <br />
    Für 64-bit Computer, lade `dcrinstall-darwin-amd64-v0.8.2` herunter.

2. Mache dcrinstall-darwin-xxxx-vx.x.x ausführbar über die Befehlszeile:

    Wechsel in das Verzeichnis in dem sich die dcrinstall Datei befindet indem du mit dem `cd` Kommando dorthin wechselst, führe chmod mit den Parametern u+x aus um die dcrinstall Datei ausführbar zu machen und starte die ausführbare Datei anschließend. Nachfolgend ein Beispiel für die Kommandos (passe die Verzeichnis- und Dateinamen entsprechend an):
    
    `cd ~/Downloads/` <br />
    `chmod u+x dcrinstall-darwin-amd64-v0.8.2` <br />
    `./dcrinstall-darwin-amd64-v0.8.2`
    
3. Die Binärdateien für `dcrd`, `dcrwallet`, und `dcrctl` können nach der Installation im Verzeichnis `~/decred/` gefunden werden.

> Linux:

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `dcrinstall-linux-386-v0.8.2` herunter. <br />
    Für 64-bit Computer, lade `dcrinstall-linux-amd64-v0.8.2` herunter. <br />
    Für 32-bit ARM Computer, lade `dcrinstall-linux-arm-v0.8.2` herunter. <br />
    Für 64-bit ARM Computer, lade `dcrinstall-linux-arm64-v0.8.2` herunter.

2. Mache dcrinstall-linux-xxxxx-vx.x.x ausführbar über die Befehlszeile:

    Wechsel in das Verzeichnis in dem sich die dcrinstall Datei befindet indem du mit dem `cd` Kommando dorthin wechselst, führe chmod mit den Parametern u+x aus um die dcrinstall Datei ausführbar zu machen und starte die ausführbare Datei anschließend. Nachfolgend ein Beispiel für die Kommandos (passe die Verzeichnis- und Dateinamen entsprechend an):
    
    `cd ~/Downloads/` <br />
    `chmod u+x dcrinstall-linux-amd64-v0.8.2` <br />
    `./dcrinstall-linux-amd64-v0.8.2` 
    
3. Die Binärdateien für `dcrd`, `dcrwallet`, und `dcrctl` können nach der Installation im Verzeichnis `~/decred/` gefunden werden.

> Windows:

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit computers, lade `dcrinstall-windows-386-v0.8.2.exe` herunter. <br /> 
    Für 64-bit computers, lade `dcrinstall-windows-amd64-v0.8.2.exe` herunter. <br />

2.  Starte die ausführbare dcrinstall Datei.

    Du kannst die Datei entweder per Doppelklick starten oder über die Eingabeaufforderung starten. 
    
3. Die Binärdateien für `dcrd`, `dcrwallet`, und `dcrctl` können nach der Installation im Verzeichnis `%HOMEPATH%\decred\` gefunden werden (in der Regel ist %HOMEPATH% das Verzeichnis `C:\Users\username`).

---

## **Binary Releases**

Die neuesten vorkompilierten Binärdateien können hier gefunden werden: [https://github.com/decred/decred-binaries/releases](https://github.com/decred/decred-binaries/releases). Mit Ausnahme der `.msi` und `.dmg` Dateien, diese sind selbstenpackende Archive der aktuellsten Binärdateien für jeden Release. Obwohl der grösste Teil lediglich ein Entpacken mit zip ist werden nachfolgend die Anleitungen für Mac, Linux und Windows beschrieben (Wir gehen davon au dass *BSD Nutzer selbstständig klar kommen).

> OSX/macOS

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `decred-darwin-386-v0.8.2.tar.gz` herunter. <br />
    Für 64-bit Computer, lade `decred-darwin-amd64-v0.8.2.tar.gz` herunter.

2. Wechsel in das Verzeichnis in dem sich die heruntergeladene Datei befindet und entpacke die .tar.gz Datei:

    Finder: einfach ein Doppelklick auf die .tar.gz Datei. <br />
    Terminal: benutze folgendes Kommando `tar -xvzf filename.tar.gz`.

    **HINWEIS**: Falls du Safari unter macOS Sierra benutzt und die 'Open "safe" files after downloading' Einstellung aktiviert hast werden .gz und .zip Dateien automatisch entpackt nachdem der Download abgeschlossen ist. Das Kommando `tar -xvzf filename.tar.gz` resultiert in nachfolgender Fehlerausgabe: `tar: Error opening archive: Failed to open 'filename.tar.gz'`. Benutze stattdessen das Kommando `tar -xvzf filename.tar` (entferne das .gz vom vorherigen Kommando).
    
    Nachdem das Archiv erfolgreich entpackt wurde sollten nun Verzeichnisse mit selbigen Namen vorliegen. (`z.B. tar -xvzf decred-darwin-amd64-v0.8.2.tar.gz` sollte in das Verzeichnis `decred-darwin-amd64-v0.8.2` entpackt werden). Folgende Binärdateien sollten nun in dem Verzeichnis liegen `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, und `sample-dcrwallet.conf`.


> Linux

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `decred-linux-386-v0.8.2.tar.gz` herunter. <br />
    Für 64-bit Computer, lade `decred-darwin-amd64-v0.8.2.tar.gz` herunter. <br />
    Für 32-bit ARM Computer, lade `decred-linux-arm-v0.8.2.tar.gz` herunter. <br />
    Für 64-bit ARM Computer, lade `decred-linux-arm64-v0.8.2.tar.gz` herunter.

2. Wechsel in das Verzeichnis in dem sich die heruntergeladene Datei befinden und entpacke die .tar.gz Datei:

    Finder: einfach ein Doppelklick auf die .tar.gz Datei. <br />
    Terminal: benutze folgendes Kommando `tar -xvzf filename.tar.gz`. 
    
    Nachdem das Archiv erfolgreich entpackt wurde sollten nun Verzeichnisse mit selbigen Namen vorliegen. (`z.B. tar -xvzf decred-darwin-amd64-v0.8.2.tar.gz` sollte in das Verzeichnis `decred-darwin-amd64-v0.8.2` entpackt werden). Folgende Binärdateien sollten nun in dem Verzeichnis liegen `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, und `sample-dcrwallet.conf`.

> Windows

Hinweis: Windows 7/8/10 unterstützen von Haus aus das entpacken von `.zip` Dateien, daher sollten die Dateien mit der Endung `.zip` als Download bevorzugt werden, da das Entpacken der `.tar.gz` ein Programm zur entpacken voraussetzt. Die nachfolgende Anleitung bezieht sich auf das Entpacken der `.zip` Dateien.
<<<<<<< HEAD

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `decred-windows-386-v0.8.2.zip` herunter. <br />
    Für 64-bit Computer, lade `decred-windows-amd64-v0.8.2.zip` herunter.

2. Wechsel in das Verzeichnis in dem sich die heruntergeladene Datei befinden und entpacke die `.zip` Datei:

    File Explorer: Rechte Maustaste auf die .zip Datei, "Alles entpacken.." auswählen und eine Fenster zum Auswählen des Ziels des Entpackvorgangs sollte erscheinen. Die Voreinstellung wird die `.zip` Datei in ein Verzeichnis mit selbigen Namen entpacken. In dem Verzeichnis sollten sich nun folgende Dateien befinden `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, und `sample-dcrwallet.conf`.

Wenn du dich dazu entschieden hast die `.tar.gz` herunterzuladen, wirst du das Archiv zwei mal entpacken müssen. Hierzu wird eine extra Software benötigt, da Windows von Haus aus keine `.tar.gz` Dateien unterstützt (7-zip, winRAR, etc..).
