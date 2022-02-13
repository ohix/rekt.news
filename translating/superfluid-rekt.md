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

**8,7 Millionen US-Dollar wurden von Superfluid abgezogen.**

_Das Krypto-Streaming-Protokoll wurde am 08.02.22 um 06:17 UTC gehackt._

Andere Projekte, die den Dienst für Beitragszahlungen oder Investoren-Treuhandverträge nutzten, erlitten negative Preisauswirkungen, als der Angreifer ihre nativen Token ablud.

Zu den betroffenen Protokollen gehörten Mai Finance ([QI](https://www.coingecko.com/en/coins/qi-dao)), Stacker Ventures ([STACK](https://www.coingecko.com/en/coins/stackos)), Stake DAO ([SDT](https://www.coingecko.com/en/coins/stake-dao)) und Museum of Crypto Art ([MOCA](https://www.coingecko.com/en/coins/museum-of-crypto-art)).

QI war der am stärksten betroffene Token und fiel nach dem Dump zunächst um fast 80%, hat sich aber seitdem auf ~62 % seines Preises vor dem Hack erholt.

[@francescorenzia](https://twitter.com/francescorenzia) von Superfluid sagte gegenüber rekt.news, dass sich der Angriff nur auf die größeren Wallet-Guthaben der Plattform konzentriert habe. In der Zeit vor dem flicken der Schwachstelle ließ der Hacker jede Menge ETH, USDC und DAI unangetastet, vermutlich weil der Angreifer „_die Nase voll hatte_“.

_Wie ist es passiert?_

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/09/rekt-investigates-linebreak.png)

**Adresse des Angreifers:** [0x1574f7f4c9d3aca2ebce918e5d19d18ae853c090](https://polygonscan.com/address/0x1574f7f4c9d3aca2ebce918e5d19d18ae853c090)

**Exploit Transaktion:** [0xdee86cae2e1bab16496a49...](https://polygonscan.com/tx/0xdee86cae2e1bab16496a49b2ec61aae0472a7ccf06f79744d42473e96edd6af6)

**Entnommenes Vermögen:**

19.4 Millionen QI (Wert vor dem Hack: 24 Millionen US-Dollar) [wurden](https://polygonscan.com/tx/0xc37151aaefa7e937c97156ca43e3d486299aa89a603d22355592ddd00bfe687a) [in](https://polygonscan.com/tx/0x741908f9707d9dd3a52525380d69f9e74a26d52350308227b84c3ad2db45449f) [vier](https://polygonscan.com/tx/0x026032084b3f7c658b7c3467d8567922e3ad93c755669ab0d92f01f040a18dea) [Transaktionen](https://polygonscan.com/tx/0x8dd5e00a54742f182eee7277a3326efd434f893fd94f5473f9ca1f0fd0358577) für insgesamt 2.300 WETH (~6,2 Millionen US-Dollar) verkauft.

24,4 WETH – (~76.000 US-Dollar)

563.000 USDC [wurden für 173 WETH](https://polygonscan.com/tx/0x9fdbcaefcd2bae1d873720ae8dfb741986818bfc1b5cf8af0a891b99b7bd14b1) verkauft.

45.000 SDT – [verkauft für ~17 WETH](https://polygonscan.com/tx/0xd12c38ce2346bbc29a845dd9099a8d3626ad12e74579be46485e31653a3888bc) – (~54.000 US-Dollar)

24.000 STACK – [verkauft für ~6,2 WETH](https://polygonscan.com/tx/0x32df8bbeba3a8fcdba51c2a7daa316078cd65345a74b765b8fa2ce6787c91f28) – (~19.000 US-Dollar)

39.000 sdam3CRV - getauscht zu [am3CRV](https://polygonscan.com/tx/0x0553be6c6f969c4f91850532f68f4e8bae5824392140edb13c3bfd6f6cb8d35e), dann zu ~44.000 [amDAI](https://polygonscan.com/tx/0x7a9b9ad4634fea8681e34c150ef561bf0ced199a3347888dfc448e4164583f7d)

1,5 Mio. MOCA – [1 Mio. von 1,5 Mio. verkauft](https://polygonscan.com/tx/0x554f5688fb8d31bcd9affc90d16f0326a8d09b0469dbb581580c7187201ef6ba) für 173 WETH (~500.000 US-Dollar)

11k MATIC - Noch nicht verkauft

>Insgesamt - ~8,7 Millionen US-Dollar

**~6 Stunden nach dem Angriff hat Superfluid den Fehler mit Hilfe von [Mudit Gupta](https://twitter.com/Mudit__Gupta) geflickt.**

[_Den Patch finden Sie hier_](https://github.com/superfluid-finance/protocol-monorepo/commit/4048fbc66c144e1afd5ae68b21160e1b25d96270).

>Der folgende Text stammt aus [Superfluids eigenem Post-Mortem](https://medium.com/superfluid-blog/08-02-22-exploit-post-mortem-15ff9c97cdd).

**Erklärung der Schwachstelle**

Superfluid.sol, bekannt als der Host-Contract, ist der Contract, der zusammensetzbare Superfluid-Contracts _(ConstantFlowAgreement, InstantDistributionAgreement)_ in einer einzigen Transaktion ermöglicht. Die zusammengesetzten Systeme werden oft als Super Apps bezeichnet.

Um jedoch während der gesamten Transaktion zwischen verschiedenen Vereinbarungsaufrufen einen vertrauenswürdigen und gemeinsam genutzten Zustand zu haben, wird ein Konzept namens „_ctx_“ (ein vom Host-Contract verwalteter serialisierter Zustand) eingeführt.

Das „ctx“ enthält den gesamten Kontext, den eine Vereinbarungsfunktion kennen muss, insbesondere, wer der „_msg.sender_“ des ersten Anrufs ist.

Dort wurde eine unglückliche Schwachstelle ausgenutzt.

**Der Angreifer war in der Lage, _calldata_ geschickt so zu manipulieren, dass der Prozess der Serialisierung im Host-Contract und die anschließende Deserialisierung im Vereinbarungs-Contract dazu führten, dass der Vereinbarungs-Contract auf einem Kontextobjekt operierte, das speziell dafür geschaffen wurde, andere Konten zu imitieren.**

Dieser Mechanismus wurde verwendet, um IDA-Indizes „im Auftrag“ anderer Konten zu erstellen und ihre Tokens auf diese Weise zu extrahieren.

**Der Exploiter Contract:**

Der folgende Exploiter-Contract zeigt, wie die Schwachstelle genutzt werden könnte, um andere Konten vorzutäuschen, um deren offenen Streams zu schließen.

Bei der eigentlichen [Exploit-Transaktion](https://polygonscan.com/tx/0x396b6ee91216cf6e7c89f0c6044dfc97e84647f5007a658ca899040471ab4d67) nutzte der Angreifer den IDA-Contract, um mit derselben Technik Gelder von anderen Konten abzuziehen:

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-badcall-code.png)

**Kette von Funktionsaufrufen**

**deleteAnyFlowBad**

Die Konvention von callAgreement besteht darin, den Platzhalter ctx zu verwenden, damit ein späterer Vereinbarungscode von solidity ihn direkt als Argument „ctx“ lesen kann.

_Weitere Informationen zu diesem Konzept finden Sie unter [About-Placeholder-Ctx](https://github.com/superfluid-finance/protocol-monorepo/wiki/About-Placeholder-Ctx)_.

Hier gelang es dem Angreifer, ein gefälschtes „ctx“ einzuschleusen, wo ein beliebiger Absender gesetzt werden konnte.

**Superfluid.callAgreement**

Im Normalfall erstellt Superfluid.callAgreement den ctx und versieht ihn mit einem Stempel (speichert seinen Hash in einer Zustandsvariable), sodass er mit _Superfluid.isCtxValid_ validiert werden kann.

**ConstantFlowAgreementV1.createFlow**

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-createflow-code.png)

Die Vereinbarung verwendet dann AgreementLibrary.authorizeTokenAccess, um zu überprüfen, ob der aufrufende Host-Contract berechtigt ist, Zustandsänderungsaufrufe für den Token-Contract durchzuführen.

**AgreementLibrary.authorizeTokenAccess**

Sobald der aufrufende Host authentifiziert ist, würde die Vereinbarung transitiv auch dem übergebenen ctx vertrauen und es in eine Speicherstruktur dekodieren (deserialisieren).

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2022/02/superfluid-authorize-code.png)

**Aber Fake Ctx!**

Das Problem war, dass man wie in der Exploit-Funktion _deleteAnyFlowBad_, einen gefälschten ctx einschleusen kann.

Nachdem es von _Superfluid.replacePlaceholderCtx_ zu einem Byte-Objekt zusammengeführt wurde (der Host macht keine Annahmen über vereinbarungsspezifische Daten), enthält das resultierende _dataWithCtx_ nun 2 ctx-Varianten, die _legitime_ und die _injizierte_.

**Wenn der Vereinbarungsvertrag diese Daten decodiert, nimmt der abi-Decoder die erste (injizierte) Variante und ignoriert die verbleibenden Daten, die das legitime ctx enthalten.**

Um dies zu lösen, fügte Superfluid dem Vereinbarungsvertrag einen Verifizierungsschritt hinzu:

_ISuperfluid.isCtxValid._ Dieser verifiziert den decodierten ctx durch Vergleich seines im Hostvertrag gespeicherten Stempels (Hash).

Diese Überprüfung war bereits für die Verarbeitung von ctx-Daten vorhanden, die von SuperApp-Callbacks bereitgestellt wurden, war jedoch nicht vorhanden für Daten, die vom vertrauenswürdigen Host-Contract übergeben wurden.

![](https://raw.githubusercontent.com/RektHQ/Assets/main/images/2021/03/rekt-linebreak.png)

Superfluid hat sich an den Angreifer in der Chain [gewandt](https://polygonscan.com/tx/0x5f9fd626df2fcfef5899c10cea2ec329e76dc0d4350b4c8cf28ce776785e1952), und laut Post-Mortem bleibt ein Kopfgeld von 1 Million Dollar als Gegenleistung für die Rückgabe des Geldes auf dem Tisch.

Das Team gibt auch an, dass die meisten betroffenen Konten bereits erstattet wurden, während die größeren QI- und MOCA-Verluste schrittweise kompensiert werden.

Obwohl dies nicht der größte Exploit war (Nummer 42 auf unserer [Rangliste](https://rekt.news/leaderboard/)) und keine Nutzergelder verloren gingen, ist er bemerkenswert für die Art und Weise, wie er andere Protokolle beeinflusste.

Der wachsende Bereich der DAO-Infrastruktur bietet mehr Ziele für die anonymen Angreifer, die in DeFi so weit verbreitet sind.

**Das gestohlene Geld befindet sich immer noch in der Wallet des Angreifers.**

_Werden sie das Kopfgeld nehmen oder Superfluid im trockenen lassen?_
