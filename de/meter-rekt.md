---
title: Meter - REKT
date: 02/07/2022
rekt:
  amount: 7700000
  audit: Unaudited
  date: 02/06/2022
tags:
  - Meter
  - Hundred
  - REKT
excerpt: Brücken bauen ist ein gefährliches Geschäft. Bei einem weiteren Angriff werden Meter.io auf BSC 4,4 Millionen USD abgenommen, wodurch Hundred Finance 3,3 Millionen USD an Kollateralschäden verliert.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-header.png)
**Brücken bauen ist ein gefährliches Geschäft.**

Bei einem weiteren Angriff werden [Meter.io](https://meter.io/) auf BSC 4,4 Millionen US-Dollar abgenommen, wodurch [Hundred Finance](https://hundred.finance/) 3,3 Millionen US-Dollar an Kollateralschäden verliert.

Dies ist der siebte Brücken-Angriff auf unserer [Rangliste](https://rekt.news/leaderboard/), der einen steigenden Trend in der Kreuz-Chain-Kriminalität zeigt.

**Wie lange wird es dauern, die Technologie zu perfektionieren um diese Verluste zu verhindern?**

_Der Zähler läuft._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

_Quelle: [@ishwinder](https://twitter.com/ishwinder/status/1490227406824685569?s=20&t=XsNHTZUI5AEDEppn3xxwUQ)_

Der Angriff begann am 05.02.2022 um ca. 14:00 Uhr UTC, als der [Angreifer](https://etherscan.io/address/0x8d3d13cac607B7297Ff61A5E1E71072758AF4D01) böswillig eine beträchtliche Menge an BNB- und wETH-Tokens prägte und die Brückenreserve seiner BNB und wETH entleerte, bevor alle Brückentransaktionen von [Meter gestoppt](https://twitter.com/Meter_IO/status/1490103308421255168) werden konnten.

Meter_io Passport ist ein Fork von ChainBridge von [ChainSafe](https://twitter.com/ChainSafeth), jedoch mit einer Änderung, die an der Einzahlungsmethode der ERC20 Handler vorgenommen wurde.

>Diese Änderung geht im Grunde davon aus, dass, wenn das zu überbrückende Tokens ein verpacktes natives Token ist, es nicht verbrannt oder gesperrt wird, da das verpackte native Token bereits entpackt ist und der Betrag an den Handler-Contract übertragen wird.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code1.png)

>Die Annahme gilt für die Einzahlungsmethode depositEth, die auch den Wert des Betrags in calldata geltend macht (der dann letztendlich an die Einzahlungsmethode des Handlers weitergegeben wird):

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code2.png)

>Aber die Annahme gilt nicht für eine andere Einzahlungsmethode im selben Contract, die größtenteils unbewacht ist.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code3.png)

>Hacker bemerkt dies und sendet einen beliebigen Betrag in den calldata, der an die Einlage des Händlers weitergegeben wird.

> Die Beute wurde dann über mehrere Transaktionen innerhalb einer Stunde in Tornado Cash transferiert.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Dieser Angriff verursachte Kollateralschäden.**

**Hundred Finance verlor 3,3 Millionen USD aufgrund ihrer Abhängigkeit von der Meter Brücke.**

Hundred Finance gab den Verlust in [einem Tweet](https://twitter.com/HundredFinance/status/1490394875459682309) bekannt.

>Heute war [@MoonriverNW](https://twitter.com/MoonriverNW) von Hundred Finance betroffen durch einen Brückenangriff auf [@Meter_IO](https://twitter.com/Meter_IO), der zu einer lokalen Abwertung des Preises von BNB.bsc führte.

>Konten konnten BNB.bsc zu einem reduzierten Preis kaufen und diese Tokens als Sicherheit zum globalen Chainlink-Preis verwenden, um unverfälschte Vermögenswerte auf unserer Plattform auszuleihen. Davon sind derzeit MIM und FRAX betroffen.

>Wir möchten die Eigentümer der Konten, die dies getan haben, bitten, die geliehenen Vermögenswerte zurückzugeben, damit andere Benutzer auf ihre Liquidität zugreifen können. 1 Konteninhaber hat dies bereits getan, und wir sind bereit, weitere Prämien an die verbleibenden 3 zu zahlen, wenn sie dasselbe tun.

**Wir haben mit dem Gründer von Hundred Finance, [vfat](https://twitter.com/vfat0/status/1490398279267495944?s=20&t=dNKrs_3KbNuPpRTC5jPs5A), gesprochen:**

**rekt:**

Wird Hundred Finance nach diesem Vorfall Änderungen vornehmen? Du hast erwähnt, dass du mit Meter an einer möglichen Lösung arbeitest – könntest du uns weitere Einzelheiten verraten?

**vfat:**

>Hallo, also ja, das ist natürlich ein Problem, dessen wir uns nur allzu bewusst sind, jede neue Chain / Brücke, die wir hinzufügen, hat ihre eigenen Risiken, und ein Leihprotokoll ist ein natürliches Ziel für Brückenangreifer.

>Wir haben Meter verwendet, da sie die Hauptquelle für wrapped BTC auf Moonriver waren, dies in Kombination mit der nativen Brücke und Multichain bringt uns auf 3 Brücken in dieser Kette, was uns an unser Maximum bringt. In Zukunft werden wir strenger vorgehen und detailliertere Informationen darüber veröffentlichen, welche Brücken für welche Assets verwendet werden. Wir werden auch eine zusätzliche Überwachung auf mögliche Angriffe wie diesen prüfen.

>Meter haben natürlich die Verantwortung für diesen Hack übernommen und beabsichtigen, ihren nativen Token für die Erstattung so weit wie möglich zu verwenden. Derzeit sind wir dabei, Adressen und Beträge zu sammeln.

>Eine interessante Sache ist, dass es bei Hundred insgesamt 4 opportunistische Kredite gab, und die ersten 2 wurden zurückgezahlt, sodass es für die anderen 2 noch ein gewisses Maß an Hoffnung gibt.

>Der aktuelle Verlust für Hundert Benutzer beträgt 3,3 Millionen US-Dollar.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Die freiwilligen Rückzahlungen der „opportunistischen Kredite“, die Hundred Finance aufgenommen hat, sind ein seltener Anblick, und es ist lobenswert, dass Meter die volle Verantwortung für alle Verluste übernimmt.**

Meter behauptet, [einige Beweise für die Identität](https://twitter.com/Meter_IO/status/1490103313521524738) des Hackers zu haben, und hat erklärt, dass sie mit Behörden zusammenarbeiten, um Gerechtigkeit zu schaffen.

**Kriminalität auf der Chain hat jedoch selten Folgen im echten Leben, und es wird nicht lange dauern, bis wir einen weiteren Angriff dieser Art sehen.**

**Es wird mehr Brückenangriffe geben und mehr Benutzer werden Geld verlieren, aber irgendwann wird es jemandem gelingen, eine sichere Brücke zu bauen.**

_Es ist noch zu früh, um risikofrei zu sein, aber das bedeutet nur mehr Chancen._

