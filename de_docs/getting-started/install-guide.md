# Installationsanleitung

Diese Anleitung wurde zuletzt zur v0.8.2 überarbeitet

---

Es gibt vier verschiedene Möglichkeiten die Decred Software herunterzuladen und zu installieren. Die erste Variante wäre der Download von dcrinstall (cross-plattform), eine weitere Möglichkeit ist der Windows Installer (Nur für Windows und zur Zeit die einzige Möglichkeit Paymetheus v0.8.2 zu installieren), eine weitere Möglichkeit ist der Download der vorkompilierten Binärdateien (plattformübergreifend) und zu guter letzt die Software im Quelltext herunterzuladen und selbst zu kompilieren (cross-plattform). Die ersten drei Methoden werden nachfolgend beschrieben, eine Anleitung zur Kompilierung folgt zu einem späteren Zeitpunkt.

---

## **Paymetheus** 

The Windows Installer (`.msi` file) is located here: [https://github.com/decred/decred-binaries/releases](https://github.com/decred/decred-binaries/releases). It will install Paymetheus to your computer's Program Files folder. Installation is pretty straightforward, but instructions are provided below:

1. Download the correct file:

    For 32-bit computers, download the `decred_0.8.2-beta_x86.msi` file. <br />
    For 64-bit computers, download the `decred_0.8.2-beta_x64.msi` file.

2. Navigate to download location and double click the `.msi` file.

3. Follow the installation steps. Within this process you'll be prompted to accept an End-User License Agreement.

4. After setup, the features should be installed to your `..\Program Files\Decred\` folder and accessible through the Start Menu (look for `Decred` in the Program list)

---

## **dcrinstall**

`dcrinstall` steht zur automatischen Installation und zum Update der Decred Software bereit. Die aktuellste Version kann hier heruntergeladen werden: [https://github.com/decred/decred-release/releases](https://github.com/decred/decred-release/releases). Binärdateien werden für Windows, OSX/macOS, Linux, OpenBSD und FreeBSD angeboten. Wenn die Installation durchgeführt wird werden `dcrd`, `dcrwallet`, und `dcrctl` auf dem Zielsystem installiert. Anleitungen für die Installation auf dem Mac, Linux und Windows werden nachfolgend beschrieben (Wir gehen davon au dass *BSD Nutzer selbstständig klar kommen).

> OSX/macOS:

1. Lade die für dein Betriebssystem korrekte Datei herunter:

    Für 32-bit Computer, lade `dcrinstall-darwin-386-v0.8.2` herunter. <br />
    Für 64-bit Computer, lade `dcrinstall-darwin-amd64-v0.8.2` herunter.

2. Mache dcrinstall-darwin-xxxx-vx.x.x ausführbar über die Befehlszeile:

    Wechsle in das Verzeichnis in dem sich die dcrinstall Datei befindet indem du mit dem `cd` Kommando dorthin wechselst, führe chmod mit den Parametern u+x aus um die dcrinstall Datei ausführbar zu machen und starte die ausführbare Datei anschließend. Nachfolgend ein Beispiel für die Kommandos (passe die Verzeichnis- und Dateinamen entsprechend an):
    
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

2. Mache dcrinstall-linux-amd64-v0.8.2 ausführbar über die Befehlszeile:

    Navigate to the directory where the dcrinstall file was downloaded using the `cd` command, run chmod with u+x mode on the dcrinstall file, and run the executable that is created. Below is an example of the commands (change directories or filename as needed):
    
    `cd ~/Downloads/` <br />
    `chmod u+x dcrinstall-darwin-amd64-v0.8.2` <br />
    `./dcrinstall-darwin-amd64-v0.8.2` 
    
3. The binaries for `dcrd`, `dcrwallet`, and `dcrctl` can then be found in the `~/decred/` directory.

> Windows:

1. Download the correct file:

    For 32-bit computers, download the `dcrinstall-windows-386-v0.8.2.exe` file. <br /> 
    For 64-bit computers, download the `dcrinstall-windows-amd64-v0.8.2.exe` file. <br />

2.  Run the dcrinstall executable file.

    You can either double click it or run it from the Command Prompt. 
    
3. The binaries for `dcrd`, `dcrwallet`, and `dcrctl` can then be found in the `%HOMEPATH%\decred\` directory (usually %HOMEPATH% is `C:\Users\username`).

---

## **Binary Releases**

The newest Binary Releases can be found here: [https://github.com/decred/decred-binaries/releases](https://github.com/decred/decred-binaries/releases). With the exception of the `.msi` and `.dmg` files, they are archives of the latest executable binaries for each release. Although most of this will be unzip and go, instructions are provided for Mac, Linux, and Windows below (assumed proficiency for *BSD users).

> OSX/macOS

1. Download the correct file:

    For 32-bit computers, download the `decred-darwin-386-v0.8.2.tar.gz` file. <br />
    For 64-bit computers, download the `decred-darwin-amd64-v0.8.2.tar.gz` file.

2. Navigate to download location and extract the .tar.gz file:

    Finder: simply double click on the .tar.gz file. <br />
    Terminal: use the `tar -xvzf filename.tar.gz` command. 

    **NOTE**: If you are using Safari on macOS Sierra and have the 'Open "safe" files after downloading' preference enabled, .gz and .zip files are automatically uncompressed after download. The `tar -xvzf filename.tar.gz` command results in this error: `tar: Error opening archive: Failed to open 'filename.tar.gz'`. Use `tar -xvzf filename.tar` instead (remove the .gz from the previous command).
    
    Both of these should extract the tar into a folder that shares the same name. (`e.g. tar -xvzf decred-darwin-amd64-v0.8.2.tar.gz` should extract to `decred-darwin-amd64-v0.8.2`). It should include `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, and `sample-dcrwallet.conf`.


> Linux

1. Download the correct file:

    For 32-bit computers, download the `decred-linux-386-v0.8.2.tar.gz` file. <br />
    For 64-bit computers, download the `decred-darwin-amd64-v0.8.2.tar.gz` file. <br />
    For 32-bit ARM computers, download the `decred-linux-arm-v0.8.2.tar.gz` file. <br />
    For 64-bit ARM computers, download the `decred-linux-arm64-v0.8.2.tar.gz` file.

2. Navigate to download location and extract the .tar.gz file:

    Finder: simply double click on the .tar.gz file. <br />
    Terminal: use the `tar -xvzf filename.tar.gz` command. 
    
    Both of these should extract the tar.gz into a folder that shares the same name. (`e.g. tar -xvzf decred-darwin-amd64-v0.8.2.tar.gz` should extract to `decred-darwin-amd64-v0.8.2`). It should include `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, and `sample-dcrwallet.conf`.

> Windows

Note: Windows 7/8/10 natively provides support for `.zip` files, therefore it is preferable to use the `.zip` file so that third-party applications aren't required for the `.tar.gz` file. Instructions are provided for the `.zip` file.

1. Download the correct file:

    For 32-bit computers, download the `decred-windows-386-v0.8.2.zip` file. <br />
    For 64-bit computers, download the `decred-windows-amd64-v0.8.2.zip` file.

2. Navigate to download location and unzip the `.zip` file:

    File Explorer: Right click on the .zip file, select "Extract All.." and a prompt should open asking for the directory to use. The default will extract the `.zip` to a folder with the same name. It should include `dcrctl`, `dcrd`, `dcrwallet`, `sample-dcrctl.conf`, `sample-dcrd.conf`, and `sample-dcrwallet.conf`.

If you decide to download the `.tar.gz` file, it will require two separate extractions in some third-party application (7-zip, winRAR, etc..) to get to the actual binaries.

-----------------------
