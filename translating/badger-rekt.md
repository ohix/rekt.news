---
title: Badger - REKT
date: 12/02/2021
rekt:
  amount: 120000000
  audit: Unaudited
  date: 12/02/2021
tags:
  - Badger
  - REKT
excerpt: rekt roadkill. 120 Millionen US-Dollar wurden bei einem Front-End-Angriff erbeutet, was Badger auf Platz vier der Rangliste bringt. rekt wiederholt; „Unbegrenzte Zustimmung bedeutet unbegrenztes Vertrauen.“
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/badger-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/badger-header.png)

**rekt Roadkill.**

_Der Dachs ist tot._

[120 Millionen US-Dollar](https://twitter.com/peckshield/status/1466356911842856967) in verschiedenen Formen von wBTC und ERC20 erbeutet.

**Ein Front-End Angriff bringt Badger DAO auf Platz vier der [Rangliste](https://rekt.news/leaderboard/).**

[rekt.news wiederholt](https://rekt.news/furucombo-rekt/):

>_Unbegrenzte Zustimmung bedeutet unbegrenztes Vertrauen - etwas, von dem wir wissen, dass wir es in DeFi nicht tun sollten._

**Aber sollte man von normalen Nutzern erwarten, dass sie einen illegitimen Contract über Wallet-Genehmigungen erkennen, wenn das Front-End kompromittiert ist?**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**Eine unbekannte Partei fügte zusätzliche Genehmigungen ein, um die Tokens der Nutzer an ihre eigene Adresse zu senden. Ab 00:00:23 UTC am 02.12.2021 nutzte der Angreifer dieses gestohlene Vertrauen, um seine eigene Wallet zu füllen.**

Als die Nachricht, dass die Adressen der Nutzer geleert wurden, Badger erreichte, gab das Team bekannt, dass sie die Smart Contracts des Projekts [pausiert](https://twitter.com/BadgerDAO/status/1466263899498377218) hatten wonach die böswilligen Transaktionen (etwa 2 Stunden und 20 Minuten nach Beginn) fehlschlugen.

Das Ziel von BadgerDAO ist es, Bitcoin zu DeFi zu bringen. Das Projekt besteht aus verschiedenen Vaults, mit denen die Nutzer Renditen für verpackte BTC-Varianten auf Ethereum erzielen können.

Die überwiegende Mehrheit der [gestohlenen](https://twitter.com/peckshield/status/1466286523729383427) Assets waren Vault-Deposit-Tokens, die dann ausgezahlt wurden, wobei die zugrundeliegenden BTC zurück in das Bitcoin-Netzwerk _gebridged_ wurden und alle ERC20-Token auf Ethereum verblieben.

_Die aktuellen Standorte der gestohlenen Gelder sind [hier](https://twitter.com/peckshield/status/1466356911842856967) zusammengefasst._

Es kursieren Gerüchte, dass das Cloudflare-Konto des Projekts kompromittiert wurde, ebenso wie [andere](https://twitter.com/SlowMist_Team/status/1466359656981225475) [Sicherheitsschwachstellen](https://twitter.com/SlowMist_Team/status/1466361705571618817).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/badger-discord.png)

**Die Genehmigungen präsentierten sich, wenn Nutzer versuchten, legitime Einzahlungs- und Belohnungstransaktionen durchzuführen, und bauten eine Basis unlimitierter Wallet-Genehmigungen auf, die es dem Angreifer ermöglichten, BTC bezogene Tokens direkt von der Adresse des Nutzers in seine zu übertragen.**

Die erste Genehmigung für die Adresse des Hackers wurde laut [Peckshield](https://twitter.com/peckshield/status/1466317257085227012) vor fast zwei Wochen erteilt. Jeder, der seither mit der Plattform interagiert hat, könnte dem Angreifer versehentlich erlaubt haben, Gelder abzuziehen.

**Über [500 Adressen](https://bloxy.info/txs/references_address/0x1fcdb04d0c5364fbd92c73ca8af9baa72c269107?argument=spender&signature_id=5) haben die Adresse des Hackers genehmigt: [0x1fcdb04d0c5364fbd92c73ca8af9baa72c269107](https://etherscan.io/address/0x1fcdb04d0c5364fbd92c73ca8af9baa72c269107)**

**Überprüfe deine Genehmigungen und widerrufe sie hier: [etherscan.io/tokenapprovalchecker](https://etherscan.io/tokenapprovalchecker)**

**[Beispieltransaktion](https://etherscan.io/tx/0x951babdddbfbbba81bbbb7991a959d9815e80cc5d9418d10e692f41541029869): Entleeren von ~900 byvWBTC im Wert von über 50 Millionen US-Dollar.** Das [Opfer](https://etherscan.io/address/0x53461e4fddcc1385f1256ae24ce3505be664f249) hatte etwa 6 Stunden zuvor über die Funktion _increaseAllowance()_ [freigegeben](https://etherscan.io/tx/0x5e4c7966b0eaddaf63f1c89fc1c4c84812905ea79c6bee9d2ada2d2e5afe1f34) unbegrenzt Geld auszugeben

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/12/badger-inputdata.png)

**Dank einer „[_ungewöhnlichen_](https://mobile.twitter.com/flashfish0x/status/1466369783016869892)“ Funktion in Badgers _transferFrom()_ Funktion war das Team schließlich in der Lage, alle Aktivitäten zu unterbrechen und weitere Geldverluste zu stoppen.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

Wenn langjährige Projekte mit einem so guten Ruf wie Badger rekt gehen können und einige der größten Namen im Spiel ihre [Beinaheunfälle](https://governance.aave.com/t/analysis-of-xsushis-incident/6335) haben, können sich DeFi Nutzer nicht zurücklehnen wenn es um die Sicherheit ihrer größten Assets geht. Diversifikation ist der Schlüssel zum Überleben.

Trotz all der Betonung, die man normalerweise auf die Überprüfung der URL legt und sicherstellt, dass man mit den richtigen Kanälen interagiert, hätte dies den Nutzern in diesem Fall nicht geholfen.

**Das Frontend wurde [vor mindestens 12 Tagen](https://twitter.com/peckshield/status/1466317257085227012) manipuliert.**

_Wie konnte Badger dies nicht bemerken?_

**Ein Nutzer [meldete](https://twitter.com/0xMoves/status/1466275399944445952) die verdächtige _increaseAllowance()_-Zulassung in Discord.**

_Warum haben sich die Badger-Entwickler nicht darum gekümmert?_

Für erfahrene Benutzer sind solche gefälschten Genehmigungen leicht zu erkennen, und die Überprüfung der Gültigkeit eines Contracts ist einfach genug, indem man die Adresse in Etherscan kopiert und einfügt, bevor man die Transaktion signiert.

Aber damit DeFi eine „Massenakzeptanz“ erreicht, müssen diese zusätzlichen Vorsichtsmaßnahmen vereinfacht werden.

Bis dahin können wir nur eine gute [Wallet- und Zulassungshygiene](https://twitter.com/CryptoCatVC/status/1466380960648380419) praktizieren.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
