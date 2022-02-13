---
title: Wormhole - REKT
date: 02/03/2022
rekt:
  amount: 326000000
  audit: Neodyme
  date: 02/02/2022
tags:
  - Wormhole
  - Solana
  - REKT
excerpt: Wurmloch hatte ein Schlupfloch... Ein Hacker verzerrte das Gefüge von Solanas Raumzeit und erzielte dabei einen Nettogewinn von 326 Millionen US-Dollar. Wie hat Wormhole so schnell so viel ETH zurückgegeben?
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/wormhole-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/wormhole-header.png)

**Wurmloch hatte ein Schlupfloch...**

_Ein Hacker verzerrte das Gefüge von Solanas Raumzeit und erzielte dabei einen Nettogewinn von 326 Millionen US-Dollar._

Beim zweiten Brücken-Exploit in [weniger als einer Woche](https://rekt.news/qubit-rekt/) landet Solana's Wormhole direkt auf Platz 2 unserer [Rangliste](https://rekt.news/leaderboard/).

Minuten nachdem [samczsun](https://twitter.com/samczsun/status/1488974372756987906) auf ein Problem hingewiesen hatte, [erklärte](https://twitter.com/wormholecrypto/status/1488976115750383626) das Wormhole-Team, dass das Netzwerk einfach „_wegen Wartungsarbeiten heruntergefahren_“ sei, während es einen „_potenziellen Exploit_“ untersuchte.

Der Exploit wurde später [direkt angesprochen](https://twitter.com/wormholecrypto/status/1489001949881978883), mit dem kühnen Versprechen, die Gelder zurückzuerstatten:

>Das Wurmloch-Netzwerk wurde für 120.000 wETH ausgenutzt. ETH wird in den nächsten Stunden hinzugefügt, um sicherzustellen, dass wETH 1:1 hinterlegt ist.

**Weniger als 24 Stunden später [war die Sicherheit wiederhergestellt](https://twitter.com/wormholecrypto/status/1489232008521859079).**

_Wo hat Wormhole 326 Millionen US-Dollar gefunden?__

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**Quelle:** [@samczsun](https://twitter.com/samczsun/status/1489044939732406275?s=20&t=_rQJze06-VjgQls6hu73wA), [@gf_256](https://twitter.com/gf_256), [@ret2jazzy](https://twitter.com/ret2jazzy), [@kelvinfichter](https://twitter.com/kelvinfichter)

**Adresse des Angreifers:** [0x629e7da20197a5429d30da36e77d06cdf796b71a](https://etherscan.io/address/0x629e7da20197a5429d30da36e77d06cdf796b71a)

**Das Wurmloch, Solanas Brücke, wurde dahingehend manipuliert, dass 120.000 ETH als auf Ethereum hinterlegt gutgeschrieben wurden, was es dem Hacker ermöglichte, das Äquivalent in umhüllter whETH _(Wormhole ETH)_ auf Solana zu prägen.**

**1:** Mit einem _SignatureSet_, das in einer [früheren Transaktion](https://solscan.io/tx/5fKWY7XyW6PTzjviTDvCTpsqgfoGAAqUs1mC6w4DZm25Ppw7fX7aWDmrnkknewyZ81qMSix3c18ZuvjoZUF34tpa) erstellt wurde, war der Angreifer zunächst in der Lage, die „Wächter“ von Wormhole zu umgehen – (eingesetzt, um Übertragungen zwischen Chains zu überprüfen) und „[_verify_signatures_](https://solscan.io/tx/25Zu1L2Q9uk998d5GMnX43t9u9eVBKvbVtgHndkc2GmUFed8Pu73LGW6hiDsmGXHykKUTLkvUdh4yXPdL3Jo4wVS)“ auf der Hauptbrücke aufzurufen.

**2:** Die Funktion „_verify_signatures_“ des Contracts delegiert dann die eigentliche Prüfung des „_SignatureSet_“ an ein separates Secp256k1-Programm. Aufgrund einer Diskrepanz zwischen „solana_program::sysvar::instructions“ (einer Art Vorkompilierung) und dem von Wormhole verwendeten „solana_program“ verifizierte der Contract die angegebene Adresse nicht korrekt, und der Angreifer konnte eine Adresse angeben mit nur 0,1 ETH.

**3:** Unter Verwendung eines Stunden zuvor erstellten Kontos mit einer einzigen serialisierten Anweisung, die dem Sep256k1-Contract entsprach, war [der Angreifer](https://etherscan.io/address/0x629e7da20197a5429d30da36e77d06cdf796b71a#internaltx) in der Lage, das „_SignatureSet_“ zu fälschen, „_complete_wrapped_“ aufzurufen und 120.000 whETH auf Solana unter Verwendung der VAA-Verifizierung auf [betrügerische weise zu prägen](https://solscan.io/tx/2zCz2GgSoSS68eNJENWrYB48dMM1zmH8SZkgYneVDv2G4gRsVfwu5rNXtK5BKFxn7fSqX9BvrBc1rdPAeBEcD6Es), die in einer [vorherigen Transaktion](https://solscan.io/tx/2SohoVoPDSdzgsGCgKQPByKQkLAXHrYmvtE7EEqwKi3qUBTGDDJ7DcfYS7YJC2f8xwKVVa6SFUpH5MZ5xcyn1BCK) erstellt worden war.

**4:** 93.750 ETH wurden im Laufe von 3 Transaktionen ([eins](https://etherscan.io/tx/0x4d5201dd4a377f20e61fb8f42e6f929ec16bcec918f0584e39241d15b254a80f), [zwei](https://etherscan.io/tx/0xd31b155e259a403ebe69831fae0ec2b4bd33dfa090c43b605a57d5c72c4fbbc7), [drei](https://etherscan.io/tx/0xacd309b02e4b533484d148de9ab0adf367ed4e70ed751d1ff036152dc3bc0479)) zurück zu Ethereum überbrückt, wo sie immer noch in der [Wallet des Hackers](https://etherscan.io/address/0x629e7da20197a5429d30da36e77d06cdf796b71a) verbleiben. Die verbleibenden ~36.000 whETH wurden auf Solana in USDC und SOL liquidiert.

**Eine [Nachricht](https://etherscan.io/tx/0x2d8b7901bff18ae6abe1a50aebe44b70559f39ff357b21340843d368b9486859) wurde auf der Chain von Certus One, dem Team hinter der Wurmholebrücke, an den Hacker gesandt:**

>Dies ist der Wormhole Deployer:
>
>Wir haben festgestellt, dass du die Solana-VAA-Verifizierung ausnutzen und Tokens prägen konntest. Wir möchten dir eine Whitehat-Vereinbarung anbieten und dir eine Bug-Prämie von 10 Millionen US-Dollar für Exploit-Details und die Rückgabe der von Ihnen geprägten wETH präsentieren. Sie erreichen uns unter contact@certus.one.

**Eine Bug-Prämie von 10 Millionen US-Dollar ist die größte, die wir je gesehen haben.**

**Bewahre deine Unschuld, plus 10 Millionen Dollar, oder gehe mit 326 Millionen Dollar auf die Flucht.**

_Wie würdest du dich entscheiden?_

Da Wormhole noch keine Antwort auf ihr Angebot erhalten hat, scheint der Angreifer den kriminellen Weg gewählt zu haben...

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

**Wir haben mit den Gründern von Wormhole gesprochen und gefragt, wie sie es geschafft haben, so viel ETH so schnell zu ersetzen.**

_Nach einiger Wartezeit teilten sie uns nur mit, dass sie derzeit einen detaillierteren Vorfallbericht verfassen._

**Für Solana war es kein guter Start ins Jahr.**

In den letzten Monaten kam es im Netzwerk zu einer Reihe von Ausfällen und Unterbrechungen. Beim jüngsten Absturz im Januar konnten die Benutzer jedoch ihre Sicherheiten [nicht aufladen](https://twitter.com/solendprotocol/status/1485315186797936646) um eine Liquidation vermeiden, da [Oracle-Probleme](https://twitter.com/solendprotocol/status/1485315192716083202) zu weiteren fehlerhaften Liquidationen führten.

Davon abgesehen ist Solana noch nicht das kampferprobte Netzwerk, zu dem Ethereum herangewachsen ist. Jeder Exploit bietet trotz all des Schadens, den er anrichtet, eine Lektion darüber, wie man ein sich entwickelndes Ökosystem sichert. Neuere L1 werden ins kalte Wasser geworfen, in eine Welt altgedienter Ausbeuter, in der sie entweder untergehen oder schwimmen lernen.

Angesichts der Ernsthaftigkeit dieses Vorfalls, zusammen mit dem [Qubit-Exploit](https://rekt.news/qubit-rekt/) in der vergangenen Woche und dem Mammutangriff auf das [Poly Network](https://rekt.news/polynetwork-rekt/) im vergangenen Sommer scheint Vitalik Buterin mit seinen jüngsten [Sicherheitsbedenken](https://twitter.com/vitalikbuterin/status/1479501366192132099) in Bezug auf cross-chain Protokolle Recht behalten zu haben.

Im Rennen durch das Kryptoversum, um experimentelle und lukrativere Möglichkeiten zu erreichen, sind viele bereit, auf neuere Technologien zu vertrauen. Aber wenn eines dieser Portale ausfällt, kann der Schaden immens sein.

**Es bleibt abzuwarten, ob die Zukunft von DeFi Cross-Chain oder „Multi-Chain“ sein wird, aber so oder so wird der Weg dorthin lang und gefährlich sein.**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/08/rekt-outline-conc.png)
