# **dcrwallet Einrichtungsanleitung**

Diese Seite wurde zuletzt für die Version v0.8.2 aktualisiert.

Diese Anleitung hilft Ihnen bei der Einrichtung der `dcrwallet` Anwendung mit Hilfe der [Startparameter](/getting-started/startup-basics.md#startparameter). 

**Vorbereitung:**

- Nutzen Sie entweder die aktuellste Version von [dcrinstall](/getting-started/install-guide.md#dcrinstall) oder [Binary Release archive](/getting-started/install-guide.md#binary-releases) zum Installieren von `dcrwallet`.
- Prüfen Sie die korrekten Kommandos zum Starten abhängig vom Betriebssystem und der Kommandozeile in (Windows) und Bash (OSX/Linux) Shell und der jeweiligen Unterschiede [hier](/getting-started/cli-differences.md).
- [dcrd Einrichten](/getting-started/user-guides/dcrd-setup.md) und im Hintergrund laufen lassen.

---

`dcrwallet` ist der Daemon zur Verwaltung Ihres Decred Wallet. Er verwaltet Ihre Accounts, Adressen und Transaktionen; Zeichnet Ihr Guthabenverlauf über all Ihre Adressen auf und ermöglicht Inhabern von DCR die Teilnahme am Proof-of-Stake Voting.

---

## **Wichtiger Hinweis**

Während Sie Ihr Wallet einrichten erhalten Sie einen sogenannten Seed mit 33 Worten auch 'Seed Phrase' genannt. Diese Seed Phrase ist Ihr privater Schlüssel zu Ihren Wallet. Sie können diese Seed Phrase nutzen um Ihr Wallet jederzeit wiederherstellen zu können, Ihren Transaktionsverlauf einzusehen und Ihr Guthaben auf einen beliebigen Computer nutzen zu können.

Dies bedeutet das *jeder* der diesen Seed kennt die privaten Schlüssel, Ihre Transaktionshistorie und das Guthaben Ihres Wallets wiederherstellen auf einen Computer wiederherstellen kann. Daher ist es unerlässlich das Sie Ihren Seed geheim halten und diesen an einen sicheren Ort aufbewahren. Behandeln Sie diesen Seed also wie einen Schlüssel zu Ihren Safe. Wenn Sie Ihren Seed verlieren sind Sie unwiederbringlich aus den Zugriff auf Ihr Wallet und somit auf das Guthaben welchen in diesen Wallet enthalten ist. Es ist für niemanden möglich diesen Seed wiederherzustellen, auch nicht durch die Decred Entwickler. Es wird empfohlen das Sie Ihren Seed auf ein Blatt niederzuschreiben und dieses Papier an einen sicheren Ort aufzubewahren. Wenn Sie sich dazu entscheiden Ihren Seed auf einen Computer zu verwahren sollten Sie dafür Sorge tragen das diese Datei nur verschlüsselt auf Ihren Computer liegt (vergessen Sie das Passwort zu dieser Datei nicht) um sich im Falle eines Diebstahls dieser Datei oder Ihres Computers vor Verlusten zu schützen.

Jede Seed Phrase ist auch mit einen 64 Zeichen landen Seed Hex verknüpft. Dieser Seed Hex erfüllt die selbe Funktion wie Ihre Seed Phrase - `dcrwallet` wird auch diesen Hex akzeptieren um Ihr Wallet wiederherzustellen. Es ist also genau so wichtig, dass Sie diesen Hex sicher aufbewahren.

**ERINNERUNG: NIEMALS, UNTER KEINEN UMSTÄNDEN, SOLLTEN SIE IHREN SEED ODER DEN DAMIT VERKNÜPFTEN HEX JEMANDEN MITTEILEN! NICHTMALS DEN DECRED ENTWICKLERN!**

---

## **Ein neues Wallet erstellen**

Um ein neues Wallet zu erstellen starten Sie  mit dem `dcrwallet --create` Kommando, vergeben Sie Ihr privates Password, optional vergeben Sie zusätzlich ein öffentliches Passwort und notieren Sie sich Ihren Seed. Nachfolgend eine erklärung zu den einzelnen Schritten.

> Starten Sie mit dem Kommando zum Erstellen eines neuen Wallet

1. Wenn Ihr `dcrd` Daemon im Hintergrund läuft (wie unter 'Vorbereitung' erwähnt) öffnen Sie eine weitere Shell (Bash/Command Prompt/etc,..).
2. Wechseln Sie in das Verzeichnis Ihrer `dcrwallet` Installation
3. Starten Sie mit dem Kommando `dcrwallet --create` (prüfen Sie die unter 'Vorbereitung' genannten Punkte wenn Sie sich unsicher sind ob Sie `./dcrwallet` oder `dcrwallet.exe` für das genannte Kommando nutzen müssen). 

> Vergeben Sie ein Passwort für Ihr Wallet

Wenn das `dcrwallet --create` erfolgreich durchgeführt wurde sollte folgender Text erscheinen:

```no-highlight
Enter the private passphrase for your new wallet:
```

Dieses erste Passwort, Ihr privates Passwort, ist das Passwort um Transaktionen durchführen zu können oder um zu Voten wenn Sie am Proof-of-Stake Voting teilnehmen möchten. Bitte nutzen Sie ein exklusives Passwort. Dieses Passwort schützt die privaten Schlüssel Ihrer Walletdatei um Sie vor Diebstahl zu schützen.

Nachdem Sie Ihr privates Passwort durch eine zweite Eingabe bestätigt haben erscheint folgende Zeile:

```no-highlight
Do you want to add an additional layer of encryption for public data? (n/no/y/yes) [no]:
```

Die Vergabe des öffentlichen Passworts ist optional. Es wird genutzt um all Ihre öffentlichen Daten Ihres Wallets zu verschlüsseln (Transaktionen und Empfangsadressen). Bei Diebstahl des öffentlichen Passworts kann ein Angreifer Einsicht in die von Ihnen getätigten Transaktionen erlangen.

> Notieren Sie Ihren Seed

Befor Sie einen neuen Seed für Ihr Wallet erstellen lesen Sie bitte den [Wichtigen Hinweis](/getting-started/user-guides/dcrwallet-setup.md#wichtiger-hinweis).

Nachdem Sie Ihr privates Passwort und optional Ihr öffentliches Passwort vergeben haben erscheint folgende Zeile:

```no-highlight
Do you have an existing wallet seed you want to use? (n/no/y/yes) [no]:
```

In dieser Anleitung gehen wir davon aus das Sie ein neues Wallet erstellen und Ihr Wallet nicht von einen bestehenden Seed wiederherstellen wollen, daher drücken Sie einfach auf `Enter` was dazu führt das Sie die Frage mit der Standardantwort `[no]` beantworten. HINWEIS: Wenn Sie ein Wallet mit einen Seed wiederherstellen wollen beantworten Sie die Frage mit `[yes]` und folgen Sie den nachfolgenden Anweisungen.

Nachdem Sie mit `[no]` geantwortet haben wird Ihnen Ihr Seed (Seed zum Wiederherstellen Ihres Wallets) und der dazugehörige Hex angezeigt. Bitte lesen Sie den Hinweis unter IMPORTANT.

Es kann nicht oft genug erwähnt werden wie wichtig es ist Ihren Seed sicher aufzubewahren. Wenn Sie diesen Fakt noch nicht verinnerlicht haben lesen Sie bitte nochmals den [Wichtigen Hinweis](/getting-started/user-guides/dcrwallet-setup.md#wichtiger-hinweis).

Haben Sie sich den Seed und den Hex notiert schreiben Sie in Grossbuchstaben `OK` und drücken `Enter`. HINWEIS: haben Sie sich Ihren Seed nicht notiert müssen Sie an dieser Stelle von neuen beginnen [von neuen beginnen](/getting-started/user-guides/dcrwallet-setup.md#ein-neues-wallet-erstellen) nachdem Sie Ihre [Wallet Datei gelöscht](/advanced/deleting-your-wallet.md) haben.

Nachdem Sie `Enter` gedrückt haben erscheint folgende Nachricht:

```no-highlight
Creating the wallet...
The wallet has been created successfully.
```

Das Wallet wird nun erstellt. Dies kann auf langsamen Computern einige Minuten in Anspruch nehmen.

## **Verbinden Sie dcrwallet mit dcrd**

Nachdem Sie Ihr [neues Wallet erstellt](#ein-neues-wallet-erstellen) und Sie Ihren [dcrd Daemon mit dem Decred Netzwerk verbunden](/getting-started/user-guides/dcrd-setup.md#connect-to-the-decred-network) haben müssen Sie nun `dcrwallet` mit dem Decred Netzwerk verbinden indem Sie eine Verbindung zum `dcrd` Daemon aufbauen um DCR zu empfangen und am PoS Mining teilzunehmen.

> Starten Sie dcrwallet mit den für dcrd hinterlegten Usernamen und Passwort

Öffnen Sie eine weitere Shell in Ihren Decred Verzeichnis (oder nutzen Sie das bestehende Fenster wenn Sie Ihr Wallet erfolgreich erstellt haben). Das nachfolgende Kommando startet dcrwallet, bitte ändern Sie die in eckigen Klammern angegebenen Werte entsprechend Ihren Einstellungen:

```no-highlight
dcrwallet -u [wallet username] -P [wallet password] --dcrdusername=[rpcuser] --dcrdpassword=[rpcpass]
```

* Der **Wallet Username** wurde von Ihnen noch nicht vergeben, also vergeben Sie nun einen. Er wird lediglich dazu genutzt um `dcrctl` mit Ihren `dcrwallet` Daemon zu verbinden und Kommandos an das Wallet zu schicken.
* Das **Wallet Password** wurde von Ihnen auch noch nicht vergeben, also vergeben Sie nun eines. Es wird ausschließlich dazu genutzt `dcrctl` mit Ihren `dcrwallet` Daemon zu verbinden und Kommandos an das Wallet zu schicken. Achten Sie auf das grosse P, bei diesen Parameter ist die Gross und Kleinschreibung zu beachten.
* Als dritter und vierter Parameter geben Sie den `rpcuser` und das `rpcpass`, welches Sie bei der [Einrichtung des dcrd Daemon](/getting-started/user-guides/dcrd-setup.md#connect-to-the-decred-network) vergeben haben an.
* Alternativ können Sie die gleiche username/password Kombination für dcrd und dcrwallet vergeben. In diesen Fall können Sie sich die Angabe des `--dcrdusername` und des `--dcrdpassword` sparen und einfach die Parameter `-u` und `-P` benutzen.

Ihr `dcrwallet` wird nun eine Verbindung zum Netzwerk mit Hilfe des `dcrd` Daemons aufnehmen. Es wird damit anfangen das Netzwerk nach die von Ihnen genutzten Adressen zu durchsuchen was auf langsamen Computern ein paar Minuten in Anspruch nehmen kann. Möglicherweise sehen Sie ähnliche Zeilen wie die nachfolgende:

```no-highlight
[INF] WLLT: Connecting block 0000000000002004ea8fa74af334cb291a22832642b5be603995683534bbb97b, height 9990
```

Dies bedeutet Ihr Wallet ist erfolgreich mit dem Netzwerk über den `dcrd` Daemon verbunden.

---

Um mehr über die Nutzung von `dcrd` und  `dcrwallet` zu erfahren lesen Sie die [dcrctl Basics](/getting-started/user-guides/dcrctl-basics.md) Anleitung. Sie werden dort erfahren wie Sie Ihr Wallet für Transaktionen entsperren, DCR empfangen, Ihr Guthaben überprüfen und verschiedene Netzwerkstatistiken einsehen können.
