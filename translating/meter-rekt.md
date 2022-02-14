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
excerpt: Brücken bauen ist ein gefährliches Geschäft. Bei einem weiteren Angriff werden Meter.io auf BSC 4,4 Millionen US-Dollar abgenommen, wodurch Hundred Finance 3,3 Millionen US-Dollar an Kollateralschäden verliert.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-header.png)
**Brücken bauen ist ein gefährliches Geschäft.**

Bei einem weiteren Angriff werden [Meter.io](https://meter.io/) auf BSC 4,4 Millionen US-Dollar abgenommen, wodurch [Hundred Finance](https://hundred.finance/) 3,3 Millionen US-Dollar an Kollateralschäden verliert.

Dies ist der siebte _Bridge_-Angriff auf unserer [Rangliste](https://rekt.news/leaderboard/), der einen steigenden Trend in der Cross-Chain-Kriminalität zeigt.

**Wie lange wird es dauern, die Technologie zu perfektionieren, um diese Verluste zu verhindern?**

_Der Zähler läuft._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

_Quelle: [@ishwinder](https://twitter.com/ishwinder/status/1490227406824685569?s=20&t=XsNHTZUI5AEDEppn3xxwUQ)_

Der Angriff begann am 05.02.2022 um ca. 14:00 Uhr UTC, als [der Angreifer](https://etherscan.io/address/0x8d3d13cac607B7297Ff61A5E1E71072758AF4D01) böswillig eine beträchtliche Menge an BNB- und wETH-Tokens prägte und die Bridgereserve seiner BNB und wETH entleerte, bevor alle Bridgetransaktionen von [Meter gestoppt](https://twitter.com/Meter_IO/status/1490103308421255168) werden konnten.

Meter_io Passport ist ein ChainBridge Fork von [ChainSafe](https://twitter.com/ChainSafeth), jedoch mit einer Änderung, die an der Einzahlungsmethode der ERC20 _Handler_ vorgenommen wurde.

>Diese Änderung geht grundsätzlich davon aus, dass, wenn der Token, der _gebridged_ wird, ein wrapped nativer Token ist, dieser nicht verbrannt oder gesperrt wird, da der wrapped native Token bereits unwrapped und der Betrag an den _Handler_-Contract übertragen wurde.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code1.png)

>Diese Annahme gilt für eine der Einzahlungsmethoden depositEth, die auch den Wert des Betrags in _calldata_ bestätigt (der dann letztendlich an die Einzahlungsmethode des Handlers weitergegeben wird):

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code2.png)

>Aber die Annahme gilt nicht für eine andere Einzahlungsmethode im selben Contract, die größtenteils unbewacht ist.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/meter-code3.png)

>Der Hacker bemerkt dies und sendet einen beliebigen Betrag in den _calldata_, der an die Einzahlung des Handlers weitergegeben wird.

>Die Beute wurde dann innerhalb einer Stunde über mehrere Transaktionen in Tornado Cash transferiert.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Dieser Angriff verursachte Kollateralschäden.**

**Hundred Finance verlor 3,3 Millionen US-Dollar aufgrund ihrer Abhängigkeit von der Meter Bridge**

Hundred Finance gab den Verlust in [einem Tweet](https://twitter.com/HundredFinance/status/1490394875459682309) bekannt.

> Heute war [@MoonriverNW](https://twitter.com/MoonriverNW) von Hundred Finance von einem Bridge-Angriff auf [@Meter_IO](https://twitter.com/Meter_IO), betroffen, der zu einer lokalen Abwertung des Kurses von BNB.bsc führte.

>Konten konnten BNB.bsc zu einem reduzierten Preis erwerben und diese Token als Sicherheiten zum globalen Chainlink-Preis verwenden, um unkompromittierte Assets auf unserer Plattform zu leihen. Von diesen sind derzeit MIM und FRAX betroffen.

>Wir möchten die Inhaber der Konten, die dies getan haben, bitten, die geliehenen Assets zurückzugeben, damit andere Nutzer auf ihre Liquidität zugreifen können. 1 Kontoinhaber hat dies bereits getan, und wir sind bereit, den übrigen 3 Kontoinhabern weitere Prämien zu zahlen, wenn sie dasselbe tun.

**Wir haben mit dem Gründer von Hundred Finance, [vfat](https://twitter.com/vfat0/status/1490398279267495944?s=20&t=dNKrs_3KbNuPpRTC5jPs5A), gesprochen:**

**rekt:**

Wird Hundred Finance nach diesem Vorfall irgendwelche Änderungen vornehmen? Sie erwähnen, dass Sie mit Meter an einer möglichen Lösung arbeiten - können Sie weitere Einzelheiten nennen?

**vfat:**

>Hallo, also ja, natürlich ist dies ein Problem, dessen wir uns nur allzu bewusst sind. Jede neue Chain/Bridge die wir hinzufügen, birgt ihre eigenen Risiken, und ein Kreditprotokoll ist ein natürliches Ziel für Bridgeangreifer.

>Wir haben Meter verwendet, da sie die Hauptquelle für ümhülltem BTC auf Moonriver waren. Zusammen mit der nativen Bridge und Multichain sind wir damit bei 3 Bridges auf dieser Chain, was das Maximum ist, das wir verwenden würden. In Zukunft werden wir strenger sein und detailliertere Informationen darüber veröffentlichen, welche Bridges für welche Assets verwendet werden. Wir werden auch eine zusätzliche Überwachung für mögliche Angriffe wie diesen in Betracht ziehen.

>Meter hat natürlich die Verantwortung für diesen Hack übernommen und beabsichtigt, ihren eigenen Token für die Rückerstattung zu verwenden, soweit es ihm möglich ist; derzeit befinden wir uns in der Phase des Sammelns von Adressen und Beträgen.

>Interessant ist, dass es bei Hundred insgesamt 4 opportunistische Darlehen gab, von denen die ersten beiden zurückgezahlt wurden, so dass es für die anderen beiden noch einen Funken Hoffnung gibt.

>Der derzeitige Verlust für Hundred Nutzer beträgt 3,3 Millionen US-Dollar.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Die freiwilligen Rückzahlungen der „opportunistischen Kredite“, die bei Hundred Finance aufgenommen wurden, sind ein seltener Anblick, und es ist lobenswert, dass Meter die volle Verantwortung für alle Verluste übernimmt.**

Meter behauptet, [einige Beweise für die Identität des Hackers](https://twitter.com/Meter_IO/status/1490103313521524738) zu haben, und hat erklärt, dass sie mit Behörden zusammenarbeiten, um Gerechtigkeit zu schaffen.

**Kriminalität auf der Chain hat jedoch selten Folgen im echten Leben, und es wird nicht lange dauern, bis wir einen weiteren Angriff dieser Art sehen.**

**Es wird mehr Anschläge auf Brücken geben, und mehr Nutzer werden Geld verlieren, aber irgendwann wird es jemandem gelingen, eine sichere Brücke zu bauen.**

_Es ist noch zu früh, um risikofrei zu sein, aber das bedeutet nur mehr Chancen._

