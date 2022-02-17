---
title: Superfluid - REKT
date: 02/09/2022
rekt:
  amount: 8700000
  audit: Peckshield
  date: 02/08/2022
tags:
  - Superfluid
  - REKT
excerpt: 8,7 Millionen US-Dollar wurden von Superfluid abgezogen. Das Krypto-Streaming-Protokoll wurde von einem anonymen Angreifer ausgenutzt, wodurch mehrere andere DAOs Kollateralschäden erlitten.
banner: https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-header.png
---
![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-header.png)

**8,7 Millionen US-Dollar von Superfluid abgezogen.**

_Das Krypto-Streaming-Protokoll wurde am 08.02.2022 um 06:17 UTC gehackt._

Andere Projekte, die den Dienst für Zahlungen an Mitwirkende oder Treuhandverträge für Investoren nutzten, erlitten negative Preisauswirkungen, da der Angreifer ihre nativen Tokens abwarf.

Zu den betroffenen Protokollen gehörten Mai Finance ([QI](https://www.coingecko.com/en/coins/qi-dao)), Stacker Ventures ([STACK](https://www.coingecko.com/en/coins/stackos)), Stake DAO ([SDT](https://www.coingecko.com/en/coins/stake-dao)) und Museum of Crypto Art ([MOCA](https://www.coingecko.com/en/coins/museum-of-crypto-art)).

QI war der am stärksten betroffene Token und fiel nach dem Dump zunächst um fast 80%, hat sich aber seitdem auf ~62% seines Preises vor dem Hack erholt.

Superfluid's [@francescorenzia](https://twitter.com/francescorenzia) sagte gegenüber rekt.news, dass sich der Angriff nur auf die größeren Wallet-Guthaben der Plattform konzentrierte. In der Zeit, bevor die Schwachstelle gepatcht wurde, ließ der Hacker viele ETH, USDC und DAI unangetastet, vermutlich weil der Angreifer „_genug hatte_“.

_Wie ist es dazu gekommen?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**Die Adresse des Angreifers:** [0x1574f7f4c9d3aca2ebce918e5d19d18ae853c090](https://polygonscan.com/address/0x1574f7f4c9d3aca2ebce918e5d19d18ae853c090)

**Exploit Transaktion:** [0xdee86cae2e1bab16496a49...](https://polygonscan.com/tx/0xdee86cae2e1bab16496a49b2ec61aae0472a7ccf06f79744d42473e96edd6af6)

**Erbeutetet Assets:**

19.4 Millionen QI (Wert vor dem Hack: 24 Millionen US-Dollar) [wurden](https://polygonscan.com/tx/0xc37151aaefa7e937c97156ca43e3d486299aa89a603d22355592ddd00bfe687a) [in](https://polygonscan.com/tx/0x741908f9707d9dd3a52525380d69f9e74a26d52350308227b84c3ad2db45449f) [vier](https://polygonscan.com/tx/0x026032084b3f7c658b7c3467d8567922e3ad93c755669ab0d92f01f040a18dea) [Transaktionen](https://polygonscan.com/tx/0x8dd5e00a54742f182eee7277a3326efd434f893fd94f5473f9ca1f0fd0358577) für insgesamt 2.300 WETH (~6,2 Millionen US-Dollar) verkauft.

24,4 WETH – (~76.000 US-Dollar)

563.000 USDC [wurden für 173 WETH](https://polygonscan.com/tx/0x9fdbcaefcd2bae1d873720ae8dfb741986818bfc1b5cf8af0a891b99b7bd14b1) verkauft.

45.000 SDT – [verkauft für ~17 WETH](https://polygonscan.com/tx/0xd12c38ce2346bbc29a845dd9099a8d3626ad12e74579be46485e31653a3888bc) – (~54.000 US-Dollar)

24.000 STACK – [verkauft für ~6,2 WETH](https://polygonscan.com/tx/0x32df8bbeba3a8fcdba51c2a7daa316078cd65345a74b765b8fa2ce6787c91f28) – (~19.000 US-Dollar)

39.000 sdam3CRV - getauscht zu [am3CRV](https://polygonscan.com/tx/0x0553be6c6f969c4f91850532f68f4e8bae5824392140edb13c3bfd6f6cb8d35e), dann zu ~44.000 [amDAI](https://polygonscan.com/tx/0x7a9b9ad4634fea8681e34c150ef561bf0ced199a3347888dfc448e4164583f7d)

1,5 Millionen MOCA – [1 Mio. von 1,5 Mio. verkauft](https://polygonscan.com/tx/0x554f5688fb8d31bcd9affc90d16f0326a8d09b0469dbb581580c7187201ef6ba) für 173 WETH (~500.000 US-Dollar)

11.000 MATIC - Noch nicht verkauft

>Insgesamt - ~8,7 Millionen US-Dollar

**~6 Stunden nach dem Angriff hat Superfluid den Fehler mit Hilfe von [Mudit Gupta](https://twitter.com/Mudit__Gupta) gepatcht.**

_[Der Patch kann hier gefunden werden](https://github.com/superfluid-finance/protocol-monorepo/commit/4048fbc66c144e1afd5ae68b21160e1b25d96270)._

>Der folgende Text stammt aus [Superfluids eigenem Post-Mortem](https://medium.com/superfluid-blog/08-02-22-exploit-post-mortem-15ff9c97cdd).

**Erläuterung der Schwachstelle**

Superfluid.sol, bekannt als der Host-Contract, ist der Contract, der zusammensetzbare Superfluid-Contracts _(ConstantFlowAgreement, InstantDistributionAgreement)_ in einer einzigen Transaktion ermöglicht. Die zusammengesetzten Systeme werden oft als Super Apps bezeichnet.

Um jedoch einen vertrauenswürdigen und gemeinsam genutzten Zustand während der gesamten Transaktion zwischen verschiedenen Vertragsaufrufen zu haben, wird ein Konzept namens _„ctx“_ (ein serialisierter Zustand, der vom Host-Contract verwaltet wird) eingeführt.

Das „ctx“ enthält den gesamten Kontext, den eine Vereinbarungsfunktion kennen muss, insbesondere, wer der „_msg.sender_“ des ersten Anrufs ist.

Hier wurde eine unglückliche Sicherheitslücke ausgenutzt.

**Der Angreifer war in der Lage, die _calldata_ so zu manipulieren, dass der Prozess der Serialisierung im Host-Contract und der anschließenden De-Serialisierung im Vereinbarungs-Contract dazu führte, dass der Vereinbarungs-Contract mit einem Kontextobjekt arbeitete, das speziell für die Identifizierung anderer Konten gefälscht wurde.**

Dieser Mechanismus wurde genutzt, um IDA-Indizes „im Namen“ anderer Konten zu erstellen und deren Token auf diese Weise zu übertragen.

**Der Exploiter-Contract:**

Der folgende Exploiter-Contract zeigt, wie die Schwachstelle genutzt werden kann, um sich als andere Konten auszugeben und deren offene Streams zu schließen.

In der eigentlichen [Exploit-Transaktion](https://polygonscan.com/tx/0x396b6ee91216cf6e7c89f0c6044dfc97e84647f5007a658ca899040471ab4d67) verwendete der Angreifer den IDA-Contract, um mit der gleichen Technik Geld von anderen Konten abzuziehen:

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-badcall-code.png)

**Kette von Funktionsaufrufen**

**deleteAnyFlowBad**

Die Konvention für _callAgreement_ ist die Verwendung des Platzhalters ctx, so dass späterer agreement solidity Code diesen direkt als Argument „ctx“ lesen kann.

_Um mehr über dieses Konzept zu erfahren, siehe [About-Placeholder-Ctx](https://github.com/superfluid-finance/protocol-monorepo/wiki/About-Placeholder-Ctx)._

Hier ist es dem Angreifer gelungen, ein gefälschtes „ctx“ zu injizieren, in dem ein beliebiger Absender gesetzt werden konnte.

**Superfluid.callAgreement**

Im Normalfall erstellt Superfluid.callAgreement das ctx und versieht es mit einem Stempel (speichert seinen Hash in einer Zustandsvariablen), so dass es mit _Superfluid.isCtxValid_ validiert werden kann.

**ConstantFlowAgreementV1.createFlow**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-createflow-code.png)

Die Vereinbarung verwendet dann AgreementLibrary.authorizeTokenAccess, um zu überprüfen, ob der aufrufende Host-Contract berechtigt ist, zustandsändernde Aufrufe des Token-Contracts durchzuführen.

**AgreementLibrary.authorizeTokenAccess**

Sobald der aufrufende Host authentifiziert ist, würde die Vereinbarung transitorisch auch dem übergebenen ctx vertrauen und es in eine Speicherstruktur dekodieren (de-serialisieren).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-authorize-code.png)

**Aber Fake Ctx!**

Das Problem war, dass man, wie bei der Exploit-Funktion _deleteAnyFlowBad_, eine gefälschte ctx einschleusen kann.

Nach dem Zusammenführen in ein Byte-Objekt durch _Superfluid.replacePlaceholderCtx_ (der Host macht keine Annahmen über vertragsspezifische Daten), enthält das resultierende _dataWithCtx_ nun 2 ctx-Varianten, die legitime und die injizierte.

**Wenn der Vereinbarungs-Contract diese Daten dekodiert, nimmt der abi-Decoder die erste (injizierte) Variante und ignoriert die restlichen Daten, die das legitime ctx enthalten.**

Um dieses Problem zu lösen, fügte Superfluid einen Überprüfungsschritt in den Contract ein:

_ISuperfluid.isCtxValid_. Damit wird die dekodierte ctx überprüft, indem ihr im Host-Contract gespeicherter Stempel (Hash) verglichen wird.

Diese Prüfung war bereits für die Behandlung von ctx-Daten vorhanden, die von SuperApp-Callbacks bereitgestellt wurden, aber nicht für Daten, die vom vertrauenswürdigen Host-Contract übergeben wurden.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png) 

**Superfluid hat sich mit dem Angreifer [on-Chain](https://polygonscan.com/tx/0x5f9fd626df2fcfef5899c10cea2ec329e76dc0d4350b4c8cf28ce776785e1952) in Verbindung gesetzt, und laut dem Post-Mortem liegt ein Kopfgeld von 1 Million US-Dollar auf dem Tisch, wenn er das gestohlene Geld zurückgibt.**

Das Team gibt außerdem an, dass die meisten der betroffenen Konten bereits erstattet wurden, während die größeren QI- und MOCA-Verluste nach und nach ausgeglichen werden.

Obwohl es sich nicht um den größten Exploit handelte _(Platz 42 auf unserer [Rangliste](https://rekt.news/leaderboard/))_ und keine Gelder der Nutzer verloren gingen, ist er aufgrund der Art und Weise, wie er andere Protokolle betraf, bemerkenswert.

Der wachsende Bereich der DAO-Infrastruktur bietet mehr Ziele für die anonymen Angreifer, die in DeFi so weit verbreitet sind.

**Das gestohlene Geld befindet sich noch immer in der Wallet des Angreifers.**

_Werden sie die Prämie annehmen oder Superfluid auf dem Trockenen sitzen lassen?_
