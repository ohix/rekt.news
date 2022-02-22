---
title: Overcompensated
date: 09/30/2021
tags:
  - Compound
excerpt: Ein Compound-Governance-Vorschlag enthielt einen Fehler, der die Ausschüttung von ~80 Millionen US-Dollar an überhöhten COMP-Rewards ermöglichte. Es wurden Fehler gemacht, aber wer ist der Verlierer?
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-header.png)
**Es wurden Fehler gemacht, aber wer ist der Verlierer?**

Ein von der Community geführter _(aber professionell geprüfter)_ [Vorschlag](https://compound.finance/governance/proposals/62) enthielt einen Fehler, der die Verteilung von ~80 Millionen US-Dollar an überschüssigen [COMP-Rewards](https://twitter.com/compoundfinance/status/1443359184897069060?s=20) ermöglichte.

Ab ~22:20 UTC am 29. September konnten bestimmte Nutzer Rewards beanspruchen, die sie nicht verdient hatten.

**Wie eine „infinite mint“, aber nicht ganz so tödlich, der verursachte Schaden war indirekt.**

Die einzigen Opfer waren die Inhaber von COMP-Tokens, die vorübergehend eine schnellere Verwässerung erlitten, als sie erwartet hatten.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-price.png)

**Selbst angesichts der übermäßigen Verwässerung kann man kaum von einem Crash sprechen.**

Große Player wie Compound haben sich das Vertrauen der Community verdient, so dass dieses 80-Millionen-US-Dollar-Missgeschick wie ein Tropfen auf den heißen Stein erscheint.

Das Compound-Team tat seinen Teil getan, um die Situation [herunterzuspielen](https://twitter.com/compoundfinance/status/1443359184897069060), während Robert Leshner sich schnell von dem Vorfall [distanzierte](https://twitter.com/rleshner/status/1443380524567912448).

Compound Labs kann sich jedoch nicht aus der Verantwortung stehlen, da ihnen eindeutig die Überprüfung des fehlerhaften Codes [zugeschrieben wurden](https://compound.finance/governance/proposals/62), bevor er eingesetzt wurde.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

[Compound: Comptroller Contract](https://etherscan.io/address/0x3d9819210a31b4961b30ef54be2aed79b9c9cd3b)

Der Fehler befand sich in den Berechnungen der [_comptrollerImplementation_](https://etherscan.io/address/0x374abb8ce19a73f2c4efad642bda76c797f19233#code#F4#L1217) für Langzeitnutzer, die vor der Festlegung des _compInitialIndexes_ Geld lieferten oder ausliehen.

[Kurt Barry](https://twitter.com/Kurt_M_Barry/status/1443414565878910976?s=20) identifizierte die Ursache der Schwachstelle auf Twitter;

>_Smart Contracts verzeihen auch die kleinsten Fehler nicht... Der COMP-Bug ist ein tragischer Fall von ">" anstelle von ">=" (an zwei Stellen im Code)._

**Eine vollständige Aufschlüsselung finden Sie in Mudit Guptas [Thread](https://twitter.com/Mudit__Gupta/status/1443454935639609345).**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/compcont-code1.png)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/comcont-code2.png)

**Diejenigen, die früh reagierten, konnten enorm [aufgeblähte](https://etherscan.io/tx/0xbc246c878326f2c128462d08a0b74048b1dbee733adde8863f569c949c06422a) Rewards kassieren, aber als die Mittel des Comptrollers schwanden, konnten die Nachzügler nur noch die [Reste](https://etherscan.io/tx/0xed77e2c4c5573392cfe680fed6201c8b052b5a9d19203fcd28539911ab798679) einsacken.**

Ein weiterer Community-[Vorschlag](https://compound.finance/governance/proposals/63) zur Deaktivierung von COMP-Rewards und zum Stoppen von Verlusten wurde gestartet, aber mit nur noch etwa 250.000 US-Dollar im Comptroller Contract scheint es zu spät zu sein.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

Wenn man die negativen Auswirkungen auf die Token-Inhaber mit dem Glück der Nutzer vergleicht, die ihre Rewards „gewonnen“ haben, dann scheint dies keine Katastrophe zu sein. Eine Wiederholung wäre jedoch nicht nachhaltig.

Wie 0xngmi auf Twitter anmerkte, sind die Folgen noch nicht vollständig bekannt. Vielleicht waren die Nutzer, die fälschlicherweise Rewards beanspruchen konnten, nicht daran gewöhnt, ihre Spuren zu verwischen.

>Eine der Personen, die @compoundfinance ausgenutzt haben, hat ihre 10 Millionen US-Dollar in COMP genommen und sie auf OKEX und Huobi für Stablecoins abgeladen und dann angefangen, mit ihnen Curve zu farmen.

>[Sein Konto] muss KYC'd sein, weil er Millionen von diesen CEXs abgezogen hat.

>_Ser_, ich habe schlechte Nachrichten für dich.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**Dies ist eine Geschichte des Systemversagens, an der keine einzelne Partei schuld ist.**

Viele Personen waren in ein komplexes, gemeinschaftliches Projekt involviert, aber am Ende läuft es auf folgendes hinaus:

>Zwei Sonderzeichen, zig Millionen an Wert verloren[.](https://twitter.com/Kurt_M_Barry/status/1443414565878910976?s=20)

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
