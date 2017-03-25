# **Command-Line Unterschiede bei verschiedenen Betriebssystemen**

Diese Seite wurde zuletzt für die Version v0.8.2 aktualisiert.

---

Diese Seite dient dazu Ihnen die Unterschiede bei der plattformübergreifenden Nutzung der Befehlszeile unter Windows, Linux, und macOS/OSX näher zu bringen.

---

> Start Kommandos

Der erste gravierende Unterschied der Anwendungen für die Befehlszeile (`dcrd`,) besteht darin, wie diese gestartet werden. Dieser Unterschied wird eher durch die unterschiedlichen Befehlszeilen des jeweiligen Betriessystem begründet. Unter Windows können Sie die Eingabeaufforderung oder die vorinstallierte PowerShell nutzen. macOS nutzt Bash innerhalb einer Terminalumgebung und viele Linux Distributionen nutzen Bash ebenfalls. Nachfolgend ein paar Beispiele für Kommandos in Bash und der Eingabeaufforderung.

**Eingabeaufforderung:** `dcrd.exe`, `dcrwallet.exe`, `dcrctl.exe` <br />
**Bash:** `./dcrd`, `./dcrwallet`, `./dcrctl`

Manche Anleitungen können OS-spezifische Varianten beinhalten. Wenn in einer Anleitung etwas wie `dcrctl --wallet getbalance` angegeben wird müssen Sie dieses Kommando also möglicherweise leicht verändern wie zum Beispiel `dcrctl.exe --wallet getbalance` für die Eingabeaufforderung und `./dcrctl --wallet getbalance` für Bash.

> Anwendungsverzeichnisse

Ein weiterer Unterschied in der Nutzung der Kommandozeile liegt in dem jeweiligen Speicherort Ihrer Daten (Blöcke, Wallets, Konfigurationsdateien werden alle innerhalb des 'Data' Verzeichnisses gespeichert). Nachfolgend eine Tabelle mit den Standartverzeichnissen für die Decred Software. 

| OS      | dcrd, dcrwallet, dcrctl App Directories      | 
| -------:|:--------------------------------------------- |
| Windows | `C:\Users\<your-username>\AppData\Local\dcrd\`      |
|         | `C:\Users\<your-username>\AppData\Local\dcrwallet\` | 
|         | `C:\Users\<your-username>\AppData\Local\dcrctl\`    |
| macOS   | `~/Library/Application Support/dcrd/`         |
|         | `~/Library/Application Support/dcrwallet/`    |
|         | `~/Library/Application Support/dcrctl/`       |
| Linux   | `~/.dcrd/`                                    |
|         | `~/.dcrwallet/`                               |
|         | `~/.dcrctl/`                                  |

