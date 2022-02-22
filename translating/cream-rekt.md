---
title: Cream Finance - REKT
date: 08/30/2021
rekt:
  amount: 18800000
  audit: Unaudited
  date: 08/30/2021
tags:
  - Cream
  - REKT
excerpt: Inspector rekt wieder im Einsatz. 18,8 Millionen US-Dollar verloren an einen Ghostface-Killer, diesmal durch ein DeFi-Protokoll der alten Schule.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-header.png)
**Inspektor rekt wieder im Einsatz.**

_18,8 Millionen US-Dollar verloren an einen Ghostface-Killer, diesmal durch ein DeFi-Protokoll der alten Schule._

[Cream Finance](https://twitter.com/peckshield/status/1432224092275548160?s=20) wurde am 28.01.2021 von [Trail of Bits](https://docs.cream.finance/audit-report) (einem der wenigen Prüfer, die in unserer [Rangliste](https://www.rekt.news/leaderboard/) fehlen) geprüft.

**Allerdings wird selbst die stärkste Prüfung irrelevant, sobald das Protokoll geändert wird.**

Am 10.02.2021 trat der [Cream-Vorschlag](https://forum.cream.finance/t/proposal-add-amp-as-a-collateral-asset/387) zum Hinzufügen des [AMP-Tokens](https://twitter.com/CreamdotFinance/status/1359348996032974852?s=20) in Kraft, und das Hintertürchen öffnete sich.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-investigates.png)
_Quelle: [@peckshield](https://twitter.com/peckshield/status/1432249600002478081)_

418.311.571 AMP-Tokens und 1.308,09 ETH gingen beim Cream Finance AMP-Token-Contract verloren.

Der AMP-Token-Vertrag implementiert den ERC77-basierten ERC1820, der über die **_callPreTransferHooks** für Reentrancy verfügt.

Die Reentrancy-Schwachstelle innerhalb des [AMP-Token-Contracts](https://etherscan.io/address/0xff20817765cb7f73d4bde2e66e067e58d11095c2#code) ermöglichte es dem Ausbeuter, eine zweite _borrow()_ Funktion in die Token _transfer()_ Funktion zu verschachteln, bevor die anfängliche _borrow()_ Funktion aktualisiert wurde:

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-reentry.png)
**[Beispiel einer Exploit-Transaktion](https://etherscan.io/tx/0xa9a1b8ea288eb9ad315088f17f7c7386b9989c95b4d13c81b69d5ddad7ffe61e) (eine von 17)**

Angriffscontracts: [A](https://etherscan.io/address/0x38c40427efbaae566407e4cde2a91947df0bd22b), [B](https://etherscan.io/address/0x0ec306d7634314d35139d1df4a630d829475a125) und [Exploiter Wallet](https://etherscan.io/address/0xce1f4b4f17224ec6df16eeb1e3e5321c54ff6ede).

Im obigen Beispiel hat der Hacker:

**1:** Verwendet Vertrag A, um einen Flash-Loan von 500 WETH aufzunehmen, um ihn als Sicherheit für Cream zu verwenden, wodurch 24,17.000 crETH geprägt werden

**2:** Leiht 19,48 Millionen AMP gegen crETH

**3:** Nutzt den Reentrancy-Bug aus, indem eine weitere borrow() Funktion in die Token-Übertragung eingefügt wird, wodurch weitere 355 ETH genommen werden, bevor der anfängliche borrow() aktualisiert wurde.

**4:** Erstellt Contract B, der mit der Hälfte (9,74 Millionen) der geliehenen AMP von A finanziert wird

**5:** Contract B liquidiert dann einen Teil des Darlehens von A, löst 187 WETH ein und überträgt es zurück an Vertrag A.

**6:** Contract A verwendet dann die über Reentrancy geliehenen ETH, um den Rest des Flash-Loans zurückzuzahlen, wobei ein Überschuss von 41 ETH und 9,74 AMP als Gewinn für diese Transaktion verbleibt.

Ein ähnlicher Prozess wurde über 17 Transaktionen angewendet, wodurch insgesamt fast 6.000 ETH angesammelt wurden.

Zum Zeitpunkt des Verfassens dieses Artikels verbleiben die gestohlene ETH (derzeit etwas mehr als 18 Millionen US-Dollar wert) in der Adresse des Ausbeuters: [0xce1f4b4f17224ec6df16eeb1e3e5321c54ff6ede](https://etherscan.io/address/0xce1f4b4f17224ec6df16eeb1e3e5321c54ff6ede)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-parental-advisory-linebreak.png)
**Creme hatte noch nie einen guten Ruf. Vielleicht glaubten deshalb viele, dass dies ihr zweites oder drittes Mal war, dass sie rekt wurden.**

Obwohl sie in den [Alpha Finance-Vorfall](https://rekt.news/alpha-finance-rekt/) verwickelt waren, ist dies tatsächlich der erste direkte Angriff auf Cream Finance.

Unabhängig von der Reputation können sogar bewährte Protokolle durch die [Integration eines anfälligen Tokens](https://www.youtube.com/watch?v=6GaCt_lM_ak) untergraben werden.

Wie @muditgupta jedoch betonte;

>... scheint [Cream] sicher gewesen zu sein, wenn sie ihre Ausleih-/Leihfunktion mit einem Schutz gegen Reentrancy versehen hätten.

_Kann das alles so einfach sein?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/cream-conclusion.gif)

