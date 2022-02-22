---
title: Compound - REKT
date: 10/04/2021
rekt:
  amount: 147000000
  audit: Unaudited 
  date: 09/29/2021
tags:
  - Compound
  - REKT
excerpt: Es ist schlimmer als wir dachten. Letzte Woche wurden ~80 Millionen US-Dollar an überschüssigem COMP fälschlicherweise verteilt. Jetzt wurden weitere 68,8 Millionen US-Dollar in den gefährdeten Vault geschickt, und noch mehr COMP wird verschenkt.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/comp2-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/comp2-header.png)
**Es ist schlimmer als wir dachten.**

[Letzte Woche](https://www.rekt.news/overcompensated/) wurde eine Schwachstelle im [aktualisierten](https://compound.finance/governance/proposals/62) Compound Comptroller Vault gefunden, und ~80 Millionen US-Dollar an überschüssigem COMP wurden fälschlicherweise verteilt.

Das Compound-Team versuchte, den _wahrgenommenen_ Schaden so gering wie möglich zu halten, aber sie wussten, dass es nur noch schlimmer werden konnte.

Jetzt wurden weitere 68,8 Millionen US-Dollar in den gefährdeten Vault geschickt, und es wird noch mehr COMP verschenkt.

_Wie konnte es für Compound so schief laufen?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**Als ob der anfängliche Verlust nicht schon schlimm genug wäre, konnte Compound einen fortgesetzten Angriff nicht verhindern.**

Jeder Nutzer konnte _drip()_ auf Compound's Reservoir Vault aufrufen, was den Comptroller wieder auffüllte und noch mehr falsche COMP-Verteilung ermöglichte.

Das Reservoir akkumuliert 0,5 COMP pro Block. Zum Zeitpunkt des ersten Vorfalls war er seit etwa 2 Monaten nicht mehr geleert worden.

Mit über 200.000 COMP (~68 Millionen US-Dollar) im Reservoir konnte das Compound-Team nur abwarten und [hoffen](https://twitter.com/rleshner/status/1444691278986457095), dass niemand entdecken würde, dass der Schaden noch lange nicht behoben war.

Während sie auf die Verabschiedung von [Vorschlag 64](https://compound.finance/governance/proposals/64) warteten, der eine Korrektur des ursprünglichen Fehlers enthielt, hatten [Robert Leshner](https://twitter.com/rleshner) und das Team eine angespannte Woche vor sich.

Doch nur dreieinhalb Tage nach dem ersten Vorfall war das [Geheimnis gelüftet](https://twitter.com/bantg/status/1444643482216304641?s=19), der Comptroller wurde wieder [aufgefüllt](https://etherscan.io/tx/0x02ba168f4d4fc313d095e9f0711447e8b96b26421539bd40be58243cd80a73cd) und weitere 68,8 Millionen US-Dollar wurden in den gefährdeten Vault geschickt.

**Wie [Banteg](https://twitter.com/bantg/status/1444685796632670213?s=20) schrieb;**

>Wenn man die anfänglichen 80 Millionen US-Dollar, die 22 Millionen US-Dollar, die nach dem Drip bereits in Anspruch genommen wurden, und die 45 Millionen US-Dollar, die derzeit in Gefahr sind, zusammenzählt, beläuft sich der Bug auf 147 Millionen US-Dollar.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/10/comp2-price.png)

Obwohl es sich eher um einen „Bankfehler" als um einen Exploit handelte, ist es nur fair, dass Compound einen Platz in unserer [Rangliste](https://www.rekt.news/leaderboard/) einnimmt, wo wir sehen können, dass dieser Fall nicht ohne Präjudiz ist.

Im Fall des fehlgeschlagenen Alchemix-Experiments erlitt das Protokoll aufgrund eines eigenen Fehlers einen Verlust von 6,5 Millionen US-Dollar.

Wie Leshner [appellierte auch Alchemix](https://twitter.com/scupytrooples/status/1443741220384043020) an seine Nutzer, die Gelder zurückzugeben, war dabei aber erfolgreicher.

55% der Alchemix-Gelder wurden zurückgegeben, ein Betrag, der für Compound derzeit unerreichbar scheint.

Es überrascht nicht, dass die Nutzer eher bereit sind, das „_Richtige_“ zu tun, wenn sie „[nett gebeten](https://twitter.com/scupytrooples/status/1443741220384043020)“ werden, als wenn ihnen mit den Behörden gedroht wird.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**In [Curve Wars](https://www.rekt.news/curve-wars/) haben wir uns an die Worte von Robert Leshner [erinnert](https://twitter.com/rleshner/status/1405337567139139584?s=20);**

>Das Schreien vor den Gerichten des _Meatspace_ untergräbt die Prinzipien von „Code ist Gesetz“, auf denen DeFi gegründet wurde.

>Wenn du willst, dass Gerichte und Politiker dich schützen und kontrollieren, dann gibt es „Finanzen“. Wenn du ein widerstandsfähiges, autarkes, offenes und aufrüstbares System willst, dann gibt es DeFi.

Nun vergleichen wir diese Worte mit seinem [aggressiven Appell](https://twitter.com/rleshner/status/1443730726751506432?s=20);

>Wenn du einen großen, falschen Betrag an COMP vom Compound Protokollfehler erhalten hast:

>Bitte gib es an das Compound Timelock (0x6d903f6003cca6255D85CcA4D3B5E5146dC33925) zurück. Behalte 10% als White-Hat.

>Andernfalls wird es der IRS als Einkommen gemeldet, und die meisten von euch werden _gedoxxt_.

War das eine Drohung oder ein Angebot? Geben Sie das „gestohlene“ Geld zurück und behalte reine 10%, oder zahle 40% an das Finanzamt und behalte reine 60%...

**Diese unsinnigen Drohungen haben dem Ruf von Compound möglicherweise mehr geschadet als der Verlust von mehreren Millionen US-Dollar.**

_Leshner hat sich inzwischen für seine Worte [entschuldigt](https://twitter.com/rleshner/status/1443759189722116097?s=20), aber kann sein Ruf wiederhergestellt werden?_

**Es ist immer noch nicht klar, wie (oder ob) die bestehenden Rechts- und Finanzsysteme mit dem neuen Konzept des dezentralen Finanzwesens zurechtkommen werden, aber für den Moment...**

_Wenn du DeFi wirklich willst, dann musst du die damit verbundene Verantwortung übernehmen._

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
