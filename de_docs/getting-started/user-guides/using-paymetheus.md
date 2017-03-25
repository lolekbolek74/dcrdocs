# **Das Paymetheus Windows Wallet** #
Diese Anleitung geht davon aus, das Sie die Paymetheus Software bereits installiert und Ihr Wallet, wie in [dieser Anleitung](paymetheus.md) beschrieben, eingerichtet haben.

---

## **Overview** ##
Der Bereich 'Overview' zeigt Ihnen eine Übersicht Ihres DCR Guthabens (spendable und locked), Anzahl der Accounts und Transaktionen sowie eine Transaktionsübersicht Ihrer letzten Transaktionen  

![Overview tab](/img/Paymetheus-overview.png)  

---


## **Accounts** ##
Der Bereich 'Accounts' zeigt Ihnen alle Accounts Ihres Wallets und bietet Ihnen die Möglichkeit weitere Accounts zu erstellen.
Accounts bei Decred ähneln Bankkonten. Sie ermöglichen Ihnen seperate Verwaltung Ihrer DCR. Diese Funktionalität dient vor allem
Unternehmungen die separate Konten zur Verwaltung Ihrer Finanzen benötigen. Transaktionen von einen in den anderen Account resultieren in einer Buchung die in der Blockchain gespeichert wird.

![Overview tab](/img/Paymetheus-accounts.png)  

---


## **Scripts** ##
Derzeit wird die Funktionalität von Skripten lediglich beim PoS mining mit einen Stakepool genutzt. Mit version 0.8.0
wurde das Einrichten der Skripte für das PoS mining mit einen Stakepool automatisiert. Werfen Sie einen Blick in den unten stehenden 'Purchase Tickets' Bereich um weitere Informationen zu erhalten.
Diese Funktionalität wird in Zukunft für weitere Funktionen genutzt werden.

![Scripts tab](/img/Paymetheus-import-script.png)  

---


## **Create Transaction** ##
Dieser Bereich wird zum versenden von DCR genutzt. Kopieren Sie hierzu einfach die Empfängeradresse in das Eingabefeld
und legen Sie die Menge der zu transferierenden DCR fest.
Die Höhe der veranschlagten Transaktionsgebühren wird auch angezeigt. Bei Bedarf können Sie auf das '+' Symbol klicken um Ihre DCR
an mehrere Empfängeraddressen in einer Transaktion zu transferieren.

![Create transaction tab](/img/Paymetheus-send.png)  

---


## ** Purchase Tickets ** ##

Paymetheus ermöglicht Ihnen den Kauf von Tickets zur Teilnahme am Proof of Stake mining indem Sie die Funktion des manuellen Ticketkaufs nutzen.
Es muss an dieser Stelle erwähnt werden das Sie mit Paymatheus lediglich Tickets kaufen können, aber das eigentliche Voting kann Paymetheus nicht übernehmen.
Zu diesen Zweck müssen Sie entweder das [solo PoS](/mining/proof-of-stake) einrichten oder sie nutzen einen [stake pool](/mining/proof-of-stake.md#sign-up-for-a-stake-pool).

> Um einen Pool zu nutzen müssen Sie diesen Ihre 'public key address' übermitteln die dazu genutzt werden kann ein
> 1-of-2 multisignature Skript zu erstellen. Das multisignature Skript wird durch den Pool generiert und Ihnen zusammen mit der
> P2SH Adresse zurückgegeben damit Sie das Recht zum Voting beim Ticketkauf an den Stakepool übergeben können.

Zerbrechen Sie sich nicht den Kopf, wenn Sie dieses Zitat nicht direkt verstehen.
Im Grunde erstellen Sie eine Empfangsadresse auf die von zwei verschiedenen Wallets zugegriffen werden kann.
Lediglich eines der beiden Wallets muss online sein um auf diese Adresse zuzugreifen. Daraus ergibt sich das
der Pool für Sie das Voting übernehmen kann und Sie wiederrum das Voting mit Ihren eigenen Wallet übernehmen können
falls der Pool nicht mehr online sein sollte.

Der Pool hat dadurch KEINEN ZUGRIFF auf Ihre DCR. Sie weisen dem Pool lediglich das Recht zu an Ihrer Stelle das Voting durchzuführen. Dabei
erlangt der Pool hat zu keinen Zeitpunkt Zugriff auf Ihre DCR.

Es wird empfohlen einen neuen Account für das Votingrecht des Stakepools zu erstellen. Im Falle eines Totalausfalls des Stakepools können Sie
so bedenkenlos das Votingrecht und den dazu benötigten privaten Schlüssel für diesen Account an einen anderen Stakepool weitergeben, solange
dieser Account lediglich für das Voting genutzt wird und nichts anderes.

Zu einer Übersicht der offiziellen Stakepools gelangen Sie [hier](/mining/proof-of-stake#sign-up-for-a-stake-pool).
Alle Stakepools laufen auf der selben Codebasis, können sich jedoch in Serverstruktur und Redundanz unterscheiden.
Mehr Redundanz resultiert in geringerer Chance Ihre Votes zu verpassen. Auch Stakepools verpassen Votes, allerdings sind viele verpasste Votes
mit dem Verhalten der PoW Miner begründet (manchmal finden PoW Miner neue Blöcke so schnell das die Zeiten für das Übermitteln der Votes durch die Stakepools nicht ausreicht).
Um sicherzustellen das ein Pool nicht zu groß wird empfehlen wir Ihnen einen kleineren Stakepool zu wählen. Ein Pool hat zwar keinen Zugriff auf Ihre DCR,
kann jedoch gegen Ihren Willen das Stimmrecht Ihrer Votes missbrauchen. Dies würde zwar relativ schnell auffallen und dazu führen das dieser Pool
gebrandmarkt wird und auf die schwarzen Liste kommt, allerdings würde eine faire Verteilung der Stimmrechte über die verschiedenen Pools sicherstellen das kein Pool eine Wahl signifikant beeinflussen könnte. Tickets gleichmässig über die Pools zu verteilen dient gleichzeitig der Dezentralisierung des Netzwerks.

![Creating voting account](/img/Paymetheus-create-voting-account.png)  

Beim Kauf von Tickets gibt es einige Einstellungen zu berücksichtigen die wir Ihnen nachfolgend näher bringen wollen.

* **Ticket difficulty** - Der derzeitige Preis für ein Ticket.
* **Blocks until retarget** - Wenn diese 0 erreicht wird ein neuer Ticketpreis errechnet.
* **Source account** - Dieser Account wird das Ticket kaufen und die Belohnung für den Vote erhalten.
* **Tickets to purchase** - Die Anzahl der zu kaufenden Tickets.
* **Ticket fee (DCR/kB)** - Ticketkäufe werden von den PoW Minern in die neuen Blöcke geschrieben. Die Reihenfolge wird hier durch die 'Ticket fee' bestimmt.
                        Wenn viele Ticketkäufe vorhanden sind müssen Sie diese Gebühr für die PoW Miner erhöhen um ihnen einen Anreiz zu geben Ihr Ticketkauf in einen Block aufzunehmen.
						Sie können die derzeitigen Ticket Fees [hier](https://www.dcrstats.com) einsehen.
* **Split fee (DCR/kB)** - Paymetheus nutzt eine “split” Transaktion um eine Blockierung Ihres Guthabens zu verhindern.
                        Hierzu generiert Paymetheus eine Transaktion mit exaktem Ticketpreis und belastet somit nicht weitere DCR in Ihrem Wallet. 
                        Diese “split” Transaktion benötigt mindestens eine Bestätigung bevor Sie Ihr Guthaben wieder verwenden können. Dies kann dazu führen, 
                        dass Ihr gesamtes Guthaben für mehrere Minuten blockiert ist bis diese Bestätigung vom Netzwerk eintrifft. Ohne diese “split” Transaktion
                        müssten Sie bis zur Bestätigung des erfolgreichen Ticketkaufs warten, was möglicherweise mehrere Stunden in Anspruch nehmen kann.
                        Diesen Wert können Sie stetig auf 0.01 belassen, es hat keinen Einfluss darauf ob Ihr Ticketkauf erfolgreich ist oder wie schnell das Ticket zum Vote aufgefordert wird.
* **Expiry (blocks)** - Während eines Preisfensters können die Ticket Fees sehr stark schwanken und es könnte sein das Sie die Ticket Fees Ihrer Ticketkäufe 
                        nachjustieren möchten. Durch das setzen des 'Expiry' werden nicht erfolgreiche Ticketkäufe nach der angegebenen Anzahl Blöcke abgebrochen so dass Sie einen weiteren Versuch mit höheren Ticket Fees starten können. Wenn Sie keine Anzahl angeben bleibt Ihr Ticketkauf bestehen bis zum Ende des Preisfensters.
* **Stake pool preference** - Automatisches Einrichten und Verbinden mit einen Stakepool. Weitere Informationen hierzu weiter unten.
* **Voting address** - Die Decred Adresse die das Voting übernimmt. Lediglich sinnvoll für Solo Miner und eigenen PoS Miner mit eigenen Pool.
* **Pool fee address** - Für PoS Miner mit eigenen Pool.
* **Pool fees (%)** - Für PoS Miner mit eigenen Pool.

![Purchasing tickets](/img/Paymetheus-ticket-purchasing.png)  

Um das Einbinden eines Stakepools zu konfigurieren klicken Sie auf den 'Manage pools button'. Wenn nicht bereits
geschehen registrieren Sie sich bei einen Stakepool (siehe oben). Sobald Sie sich registriert haben loggen Sie sich ein,
schauen Sie auf der Pool Webseite in den Unterpunkt "Settings" und kopieren Sie sich Ihren Api Token. Nun wählen Sie in Paymetheus
den Pool in dem Sie sich registriert haben aus dem Drop Down Menü aus. Fügen Sie Ihren Api Token in das Eingabefeld 'API key' ein und klicken
Sie anschließend auf 'Save'. Anschließend sehen Sie im zweiten Eingabefeld automatisch eine Buchstaben und Zahlenkombination erscheinen.
Klicken Sie nun auf 'Close'. Nun können Sie Tickets kaufen indem Sie auf den 'Purchase' Button drücken, vergessen Sie im oberen Dropdown nicht
Ihren Pool beim Kauf eines Tickets auszuwählen um das Stimmrecht der zu kaufenden Tickets an den Pool zu übergeben.

![Manage stake pools](/img/Paymetheus-manage-stake-pool.png)
			
HINWEIS: Sie können mit Paymetheus Tickets kaufen, Sie können allerdings nicht Voten. Sie müssen entweder einen Stakepool verwenden oder ein eigenens
Wallet zum Voten betreiben welches 24/7 online ist. Wenn Sie es bevorzugen Solo PoS Voting zu betreiben lesen Sie bitte das [dcrd Setup Guide](/getting-started/user-guides/dcrd-setup.md), [dcrwallet Setup Guide](/getting-started/user-guides/dcrd-setup.md) und [PoS Mining Guide](/mining/proof-of-stake.ms) um weitere Informationen zu erhalten.

---

## **Request Payment** ##
In diesen Bereich können Sie neue Empfangsadressen generieren um diese anderen Personen
mitzuteilen damit diese Ihnen DCR transferieren können. Wählen Sie einfach im oberen Pulldown Menü
den Account aus für den eine neue Adresse erstellt werden soll und klicken Sie anschließend auf 'Generate Address'.
Kopieren Sie sich die Empfangsadresse (fängt mit den Buchstaben Ds an) und teilen Sie diese der anderen Person mit.

Decred Adressen können Sie so oft Sie wollen wiederverwenden, allerdings wird aus Gründen der Privatsphäre empfohlen
für jede Transaktion eine neue Adresse zu generieren. Es gibt insgesamt 1.4E48 (das ist eine 14 gefolgt von 47 Nullen)
mögliche Adressen die Sie mit Ihren Wallet generieren können, somit ist sichergestellt das Ihnen Ihre Adressen so schnell nicht ausgehen werden.

![Request Payment](/img/Paymetheus-receive.png)  

---


## **Transaction History** ##
Dieser Bereich zeigt Ihnen alle stattgefundenen Transaktionen an. Der Transaktionshash kann mit dem 
[block explorer](/getting-started/using-the-block-explorer.md) eingesehen werden um weitere Informationen über die Transaktion zu erhalten.

![Transaction History](/img/Paymetheus-transactions.png)  

---


## **Stake Mining** ##
Dieser Bereich zeigt Ihnen Statistiken zum PoS Netzwerk an:

Eintrag                        | Beschreibung
:-----------------------------:|:------------------------------------------------------------:
Number of live tickets       | Anzahl der Tickets die aktuell im Netzwerk zum Voten bereit stehen
Number of tickets in mempool | Anzahl der Ticketkäufe die darauf warten in den Ticketpool aufgenommen zu werden
Ticket difficulty            | Der aktuelle Ticketpreis (wird Ihnen bei einem vote/expiry zurückerstattet)
Owned tickets in mempool     | Anzahl der Tickets im mempool
Owned live tickets           | Anzahl Ihrer Tickets die zum Voten bereit stehen
Owned immature tickets       | Anzahl Ihrer Tickets die erfolgreich gekauft wurden und in Kürze 'Live' werden und zum Voting bereit stehen (256 blocks, ~17 hours)
Tickets missed               | Anzahl Ihrer Tickets die ihre Chance zum Voting verpasst haben, entweder weil das Votingwallet oder der Stakepool offline waren oder der PoW Miner diesen Vote nicht richtig angenommen hat
Tickets revoked              | Tickets die ihre Chance zum Voting verpasst haben und deren Ticketpreis Sie bereits rückerstattet bekommen haben (abzüglich der Ticket Fee), sollte im Regelfall der Anzahl der 'Tickets missed' entsprechen
Tickets voted                | Alle Tickets die während der Lebenszeit Ihres Wallets erfolgreich gevotet haben
Total subsidy earned         | Die DCR die Sie während der Lebenszeit Ihres Wallets bereits durch das Voting verdient haben
