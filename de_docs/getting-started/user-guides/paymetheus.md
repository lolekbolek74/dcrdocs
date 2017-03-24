# **Paymetheus Installationsanleitung** #

Paymetheus ist ein Decred Wallet mit grafischer Oberfläche. Sie können damit DCR senden und empfangen, Tickets zur Teilnahme am [PoS voting](/mining/proof-of-stake.md) kaufen und eine Transaktionshistorie all Ihrer getätigten Transaktionen einsehen.
Paymatheus übernimmt allerdings nicht das Voting, daher sind Sie darauf angewiesen sich bei einen Stakepool zu registrieren um am PoS Voting teilzunehmen.

---

## **Download und Installation** ##
Die Downloadlinks und eine Installationsanleitung finden Sie [hier](/getting-started/install-guide.md#windows-installer)

---

## **Paymetheus Starten** ##
Jetzt können Sie mit der Nutzung von Decred beginnen! Starten Sie das 'Decred' Programm. Als erstes sehen Sie den Verbindungsbildschirm:  

![Paymetheus connection screen](../../img/Paymetheus-dcrd-login.png)  

>Zwei Programme werden ausgeführt wenn Sie Decred starten. 'Paymetheus', das grafische Wallet und 'dcrd', der Daemon (DAY-mon ausgesprochen; Ein Programm
>das im Hintergrund läuft und mit dem der Nutzer nicht direkt interagiert), der die Verbindung zum Decred Netzwerk aufbaut. Das bedeutet, Sie könnten 'dcrd'
>auf einen weiteren Computer laufen lassen (zum Beispiel ein Server der immer angeschaltet ist) und Paymetheus konfigurieren um eine Verbindung zum 'dcrd' Daemon auf einen anderen Rechner aufzubauen.

Wir werden eine Verbindung zum lokalen 'dcrd' Daemon aufbauen der bereits durch Paymetheus im Hintergrund gestartet wurde und klicken daher auf Continue.

> Das erste mal wenn Paymetheus gestartet wird muss die Blockchain im Hintergrund heruntergeladen werden. Dies kann abhängig von Ihrer Internetverbindung bis zu einer Stunde dauern.

---

## **Wallet neu Erstellen oder mit einen Seed wiederherstellen** ##
Sie haben nun die Wahl ein neues Wallet zu erstellen oder mit einen bereits vorhandenen Seed wiederherzustellen. Wenn Sie diese Anleitung lesen werden Sie 
Wahrscheinlich ein neues Wallet erstellen wollen. Klicken Sie auf 'restore' werden Sie anschließend dazu aufgefordert Ihren Seed einzugeben. Erstellen Sie ein
ganz neues Wallet wird Ihnen Ihr neu erstellter Seed auf dem Bildschirm angezeigt. Die nachfolgenden Schritte sind in beiden Varianten die selben.
Klicken Sie auf "Create a new wallet". Sie werden folgenden Bildschirm sehen:  

![Paymetheus wallet creation screen](/img/Paymetheus-seed-window.png)  

<i class="fa fa-exclamation-triangle"></i> **STOP!!! HIER NICHT WEITERMACHEN!**  

Hier kommt der wichtigste Teil bei der Erstellung eines neuen Wallets. In dem weissen Feld wird Ihr neuer Seed angezeigt. Diese Worte sind Ihr Schlüssel zu 
Ihrem Wallet.  

<i class="fa fa-exclamation-triangle"></i> **OHNE DIESEN SEED ODER DEN DAZUGEHÖRIGEN HEX-CODE VERLIEREN SIE UNWIEDERBRINGLICH DEN ZUGRIFF AUF IHR WALLET!**  

**GEBEN SIE DEN SEED NIEMALS JEMAND ANDEREN, NICHT EINMAL DEN DECRED ENTWICKLERN!** Mit diesen Worten kann jemand Ihr Wallet auf einen anderen Computer 
wiederherstellen und Ihre Geld transferieren oder stehlen. Bei Decred lassen sich keine Transaktionen rückgängig machen, sobald jemand Ihre Decreds stiehlt 
haben Sie keine Möglichkeit dieses Geld zurückzuholen.

Decred und andere digitale Währungen werden oft mit einen Bankkonto verglichen. Dies ist nur teilweise wahr, denn ihr Decred Wallet ist auch vergleichbar mit
Ihrer Geldbörse. Verlieren Sie Ihre Geldbörse verlieren Sie auch den Zugriff auf das, was sich darin befunden hat und niemand, auch nicht die Decred Entwickler
kann diesen Verlust rückgängig machen. Also ist es sehr wichtig, das Sie sich die Zeit nehmen und diese Seite sehr ausführlich lesen und das Sie Ihren Seed
AUFSCHREIBEN und diese Notiz anschließend an einen sicheren Ort aufbewahren. Es bietet sich an den Seed auf ein Blatt Papier zu notieren und an einen geheimen 
Ort aufzubewahren und zusätzlich eine Kopie dieses Seeds VERSCHLÜSSELT auf dem Rechner zu speichern. Clouddienste wie Dropbox oder OneDrive sind nette Dienste
zum Speichern Ihrer Daten, seien Sie sich aber darüber bewusst, das andere Menschen auf diese Daten Zugriff haben. Daher verschlüsseln Sie bitte diese Daten,
wenn Sie diese in digitaler Form speichern möchten (MS Word oder Libre/OpenOffice haben Verschlüsselungsfunktionen für Dokumente).

Okay, Sie haben Ihren Seed nun an mindestens zwei verschiedenen Orten sicher verwahrt. Klicken Sie auf 'Continue'. Nun werden Sie dazu aufgefordert Ihren Seed
noch einmal einzugeben um sicherzustellen, dass Sie Ihren Seed korrekt notiert haben um Ihr Wallet zu einen späteren Zeitpunkt wiederherstellen zu können.
Sie können den Seed nicht einfach per 'copy paste' einfügen, Sie müssen diesen eintippen. Dies dient zur Absicherung, dass Sie Ihren Seed nicht einfach in die
Zwischenablage kopieren und einfügen sondern Ihn auch wirklich notiert haben. Tippen Sie Ihren Seed ein und klicken Sie anschließend auf 'Confirm'.

---

## **Wählen Sie ein privates Wallet Password** ##
Dieses Passwort wird benötigt wenn Sie Transaktionen ausführen möchten. Es gibt auch die Möglichkeit wahlweise ein öffentliches Passwort (public Password) zu vergeben. Das öffentliche Passwort verschlüsselt Ihre auf dem Computer gespeicherte Walletdatei. Es soll verhindern, dass jemand an Ihren Computer ohne Ihr Wissen ihr Wallet starten und einsehen kann. Solange Ihr Wallet sich im verschlossenen (locked) Modus befinden können keine Transaktionen durchgeführt werden. Für manche Nutzer ist die Nutzung von zwei Passwörtern zuviel des Guten, daher können Sie entscheiden ob Sie ein öffentliches (public) Passwort vergeben möchten. Haben Sie nun Ihr privates (und optional das öffentliche) Passwort vergeben können Sie auf 'Encrypt' klicken um den Vorgang abzuschließen.

Ihr Wallet wird nun auf Ihren Computer erstellt und es wird sich mit der Blockchain synchronisieren. Dies kann einige Minuten dauern. Es ist an dieser Stelle noch zu erwähnen, dass der von Ihnen notierte Seed auch in anderen Decred Anwendungen genutzt werden kann, nicht nur in Paymatheus.

Weiterlesen mit [Paymetheus Nutzung](using-paymetheus.md)