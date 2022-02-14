---
title: Qubit Finance - REKT
date: 01/28/2022
rekt:
  amount: 80000000
  audit:  Unaudited
  date: 01/28/2022
tags:
  - Qubit Finance
  - BSC
  - REKT
excerpt: Weitere Neuigkeiten... Qubit Finance, ein Protokoll des Teams hinter dem Wiederholungstäter PancakeBunny, ist Opfer eines 80-Millionen-Dollar-Exploits geworden. Aber wird sich irgendjemand nächste Woche noch daran erinnern?
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/01/qubit-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/01/qubit-header.png)

**In anderen Nachrichten...**

[Qubit Finance](https://qbt.fi/), ein BSC-basiertes Kreditprotokoll, das vom Team hinter dem Wiederholungstäter ([1](https://rekt.news/pancakebunny-rekt/), [2](https://rekt.news/pancakebunny2-rekt/)) PancakeBunny [gestartet wurde](https://pancakebunny.medium.com/introducing-qubit-qbt-innovating-lending-and-borrowing-on-the-bsc-9f3fe6438f44), ist Opfer eines 80 Millionen US-Dollar Exploits geworden.

Das ist die Nummer sieben auf unserer [Rangliste](https://rekt.news/leaderboard/).

_Aber wird sich irgendjemand nächste Woche noch daran erinnern?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

Qubit ermöglicht eine [chainübergreifende Besicherung](https://docs.qbt.fi/protocol/bridge) und sperrt Assets auf Ethereum, um sie über die QBridge-Einzahlungsfunktion auf BSC auszuleihen.

Der Angreifer nutzte einen Logikfehler im Code aus, der xETH für die Verwendung auf BSC verfügbar machte, ohne ETH auf Ethereum hinterlegt zu haben.

Die Ethereum [Adresse](https://etherscan.io/address/0xd01ae1a708614948b2b5e0b7ab5be6afa01325c7) des Angreifers wurde kurz vor Beginn des Exploits am 27.01.2022 um ca. 21:30 UTC aus Tornado Cash [finanziert](https://etherscan.io/tx/0x8d2e9fd13c3e3f59eac17ff55bb0a0b10eee965a2e768e60832b1b3d5b80ebfb).

Aus dem [Post-Mortem](https://medium.com/@QubitFin/protocol-exploit-report-305c34540fa3) des Qubit-Teams:

**1.** Der Angreifer hat die QBridge-Einzahlungsfunktion im Ethereum-Netzwerk aufgerufen, die wiederum die Einzahlungsfunktion QBridgeHandler aufruft.

**2.** QBridgeHandler sollte das WETH-Token empfangen, das die ursprüngliche _tokenAddress_ ist, und wenn die Person, die die Transaktion durchgeführt hat, kein WETH-Token hat, sollte die Übertragung nicht stattfinden.

**3.** tokenAddress.safeTransferFrom(Einzahler, Adresse(this), Betrag);

**4.** Im obigen Code ist tokenAddress 0, also ist safeTransferFrom nicht fehlgeschlagen und die Einzahlungsfunktion wurde unabhängig vom Wert des Betrags normal beendet.

**5.** Außerdem war tokenAddress die WETH-Adresse, bevor depositETH hinzugefügt wurde, aber wenn depositETH hinzugefügt wird, wird sie durch die Nulladresse ersetzt, die die tokenAddress von ETH ist.

**6.** Zusammenfassend war die Deposit-Funktion eine Funktion, die nach der Neuentwicklung von depositETH nicht genutzt werden sollte, aber im Contract verblieb.

Nach Certiks [Analyse](https://certik.medium.com/qubit-bridge-collapse-exploited-to-the-tune-of-80-million-a7ab9068e1a0):

>_Eine der Hauptursachen für die Schwachstelle war die Tatsache, dass tokenAddress.safeTransferFrom() nicht zurückgesetzt wird, wenn die tokenAddress die Nulladresse (0x0...000) ist._

Obwohl keine ETH im Ethereum-Contract eingeschlossen waren, hatte die BSC-Adresse des Angreifers nun Zugriff auf [77.162 qXETH](https://bscscan.com/tx/0x50946e3e4ccb7d39f3512b7ecb75df66e6868b9af0eee8a7e4b61ef8a459518e) (185 Millionen US-Dollar), die als Sicherheit für Kredite auf Qubit verwendet werden konnten.

Sie nutzten diese Sicherheiten, um WETH, BTC-B, US-Dollar-Stablecoins, CAKE, BUNNY und MDX zu leihen, bevor sie alles gegen insgesamt 200.000 BNB (~80 Millionen US-Dollar) tauschten, die nach wie vor in der [BSC-Adresse](https://bscscan.com/address/0xd01ae1a708614948b2b5e0b7ab5be6afa01325c7) verbleiben.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Laut den Qubit-Unterlagen wurde die Cross-Chain-Kollateral-Funktion im Dezember 2021 geprüft.**

Die gesamte X-Kollateral-Funktion (einschließlich Contracts und Skripte) wurde von Theori, einer professionellen Auditierungsfirma, geprüft. Das Prüfungsergebnis ist hier [veröffentlicht](https://github.com/PancakeBunny-finance/qubit-finance/blob/master/audits/mound_qubit_xChain_audit_rev1.1.pdf).

Das Projekt hat eine maximale Prämie von 250.000 US-Dollar für [Immunefi](https://immunefi.com/bounty/qubit/), aber das Qubit-Team scheint zu Verhandlungen [bereit](https://twitter.com/QubitFin/status/1486984216072318977) zu sein.

Bereits im Mai 2021 [schenkte](https://twitter.com/RektHQ/status/1397195892327858181) uns der Pancake Bunny Hacker 100.000 DAI.

Wir haben das Geld zurückgegeben und dem Team [gesagt](https://twitter.com/RektHQ/status/1399714766785028098?s=20), „dieses Mal nicht zu verlieren“, aber hier sind wir wieder.

Unsere Spendenadresse ist unten aufgeführt.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/7/pancbunny2-conc.png)
