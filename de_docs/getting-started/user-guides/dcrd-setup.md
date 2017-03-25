# **dcrd Einrichtungsanleitung**

Diese Seite wurde zuletzt für die Version v0.8.2 aktualisiert.

Diese Anleitung dient Ihnen als Hilfe zur Einrichtung der `dcrd` Anwendung mit Hilfe von [Startparametern](/getting-started/startup-basics.md#startup-command-flags). 

**Vorbereitungen:**

- Nutzen Sie entweder die aktuelle Version von [dcrinstall](/getting-started/install-guide.md#dcrinstall) oder die [Binärversionen](/getting-started/install-guide.md#binary-releases) um `dcrd` zu installieren.
- Vergewissern Sie sich über die individuellen Varianten Ihrer Kommandozeile für (Windows) und Bash (OSX/Linux) und deren Unterschiede [hier](/getting-started/cli-differences.md).

---

`dcrd` ist der Daemon zur Verwaltung Ihres Netzknoten für Decred. Ein Daemon ist ein Programm welches im Hintergrund läuft und Dienste zur Verfügung stellt. Sie werden also nicht direkt mit dem Daemon interagieren sondern diesen lediglich starten und im Hintergrund laufen lassen. `dcrd` verwaltet das komplette Decred Kontobuch mit allen Transaktionen der Vergangenheit (blockchain) und kümmert sich um die Vermittlung der Netzwerkkommunikation der Netzwerkknoten des weltweiten Decred Netzwerks. Der 'dcrd' Daemon ist also bildlich gesprochen Ihr persönlicher Decred Blockchain Server.

**Fortgeschrittene Nutzer: Wenn Sie im headless Modus via SSH arbeiten,** empfehlen wir Ihnen die Nutzung eines Terminal multiplexers wie [screen](http://www.howtogeek.com/howto/ubuntu/keep-your-ssh-session-running-when-you-disconnect/)
oder [tmux](https://tmux.github.io/). Wenn Sie nachfolgend die Aufforderung sehen eine weitere Shell zu nutzen müssen Sie ein neues Fenster in `screen`
oder `tmux` öffnen.

---

## **<i class="fa fa-cloud"></i> Mit dem Decred Netzwerk verbinden**

> Starten Sie dcrd mit den --rpcuser und --rpcpass Parametern

Bevor Sie beginnen wählen Sie einen Unsername und ein Passwort. Sie brauchen sich nirgendwo registrieren, Sie können diese Logindaten jederzeit ändern denn diese Daten werden ausschließlich von `dcrwallet` und `dcrctl` genutzt um mit dem `dcrd` Daemon zu kommunizieren. Anstatt eines Startparameters können Sie den Usernamen und das Passwort auch in der Konfigurationsdatei oder in individuellen Skripten hinterlegen (lesen sie hierzu: [Logindaten hinterlegen](/advanced/storing-login-details.md)).

1. Wählen Sie einen Usernamen und ein Passwort wie oben erwähnt
2. Navigieren Sie in das Verzeichnis `dcrd` ausführbar über die Kommandozeile (Eingabeaufforderung/Bash/etc).
3. Geben Sie das Kommando `dcrd --rpcuser [dcrdusername] --rpcpass [dcrdpassword]` ein (bitte überprüfen Sie die Anleitung zu Ihren jeweiligen Betriebssystem um zu entscheiden ob Sie `./dcrd` oder `dcrd.exe` angeben müssen).

> Warten Sie bis sich dcrd vollständig mit der Decred Blockchain synchronisiert hat

Wenn `dcrd` erfolgreich gestartet wurde sollte sich Ihre Shell mit Nachrichten des Daemons füllen und Ihnen Auskunft darüber geben das der Daemon eine Verbindung mit dem Netzwerk aufgebaut hat und anfängt Blöcke der Blockchain zu verarbeiten. Warten Sie bis die Verarbeitung der Blöcke abgeschlossen ist - die komplette Blockchain wird in das `dcrd` data Verzeichnis heruntergeladen. 

Sie sehen eine Zeile ähnlich dieser:

```no-highlight
22:58:04 2016-02-09 [INF] BMGR: Syncing to block height 617 from peer 104.236.167.133:9108
```

Anschließend wird der Download der Blöcke fortgesetzt und Sie erhalten Zeilen wie diese:

```no-highlight
22:58:16 2016-02-09 [INF] BMGR: Processed 321 blocks in the last 10.03s (544 transactions, height 322, 2016-02-09 09:50:34 +1000 EST)
```

Die Blockchain wird sich vollständig synchronisiert haben wenn Ihnen die aktuelle Blockhöhe erreicht wurde. Sie können die aktuelle Blockhöhe erfahren indem Sie die Angabe des Datums und der Uhrzeit in der Log Nachricht beobachten oder Sie die Blockhöhe mit der Blockhöhe im [offiziellen Block Explorer](https://mainnet.decred.org/) vergleichen.  

Beachten Sie das dieser Netzknoten zukünftig für den Betrieb von Decred genutzt wird. Daher müssen Sie Ihre `dcrd` Instanz im Hintergrund laufen lassen um im nächsten Schritt `dcrwallet` erfolgreich zu betreiben.

---

Nachdem Sie nun `dcrd` erfolgreich eingerichtet haben lesen Sie die [dcrwallet Anleitung](/getting-started/user-guides/dcrwallet-setup.md).