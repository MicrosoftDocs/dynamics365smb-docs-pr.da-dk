---
author: brentholtorf
ms.topic: include
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

På købsdokumenter og kladder kan du angive et bilagsnummer, der henviser til kreditorens nummereringssystem. Du kan bruge dette felt til at registrere det nummer, som kreditoren har tildelt ordren, fakturaen eller kreditnotaen. Du kan derefter bruge nummeret, hvis du har brug for at søge efter den bogførte kladdelinje ved hjælp af det eksterne bilagsnummer.

Feltet **udv. doc. Obligatorisk** på opsætningssiden **Køb og kreditorstyring** angiver, om der skal angives et eksternt bilagsnummer i følgende situationer:

* I feltet **Kreditors fakturanr.**, **Kreditors ordrenr.** I feltet eller **Kreditors kr.notanr.** Feltet på et købshoved.

* I feltet **Eksternt bilagsnr.** på en finanskladdelinje, hvor oplysningerne i feltet **Bilagstype** er angivet til *Faktura*, *Kreditnota* eller *Rentenota*, og **Kontotype** er angivet til *Kreditor*.

Hvis du markerer afkrydsningsfeltet, vil det ikke være muligt at bogføre en faktura, en kreditnota eller den type finanskladdelinje, der er beskrevet ovenfor, uden et eksternt bilagsnummer.

Det eksterne bilagsnummer indgår i bogførte dokumenter, hvor du kan søge efter det relevante nummer. Du kan også bruge det eksterne bilagsnummer, når du navigerer på kreditorposter.

Du kan håndtere eksterne bilagsnumre på en anden måde ved at bruge feltet **Reference**. Hvis du bruger feltet **Reference**, medtages nummeret i bogførte bilag, og du kan søge på den samme måde som for værdier fra feltet **Eksternt bilagsnr.**. Men feltet er ikke tilgængeligt på kladdelinjer.
