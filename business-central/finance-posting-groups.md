---
title: Opsætning af bogføringsgrupper | Microsoft Docs
description: Oversigt over de bogføringsgrupper, du kan bruge til at spare tid og undgå fejl, når du bogfører transaktioner.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 12/17/2021
ms.author: bholtorf
ms.openlocfilehash: ed369b94948846ca380a3480e79660a6aafe292a
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940747"
---
# <a name="setting-up-posting-groups"></a>Konfigurere bogføringsgrupper
Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. De sparer tid, og du undgå nemmere fejl, når du bogfører transaktioner. Transaktionsværdier går til de konti, der er angivet i bogføringsgruppen for den pågældende enhed. Det eneste krav er, at du har en kontoplan. Du kan finde flere oplysninger i [Konfigurere kontoplanen](finance-setup-chart-accounts.md).  

Bogføringsgrupper inddeles i tre hovedgrupper:  

* Generel - Angiv, hvem du sælger til og køber fra, og hvad du sælger og køber. Du kan også kombinere grupper for at angive ting som de resultatopgørelseskonti, der skal bogføres på, eller du kan bruge grupper til at filtrere rapporter.  
* Specifik - Brug f.eks. salgsdokumenter i stedet for at bogføre direkte til finansposterne. Når du opretter debitorposter, oprettes de tilsvarende poster i finansposterne.  
* Skat – Definer de momsprocenter og beregningstyper, der gælder for dem, du sælger til og køber fra, og hvad du sælger og køber.

I følgende tabeller beskrives bogføringsgrupperne under de respektive hovedgrupper.  

| Generelle bogføringsgrupper | Beskrivelse |
| --- | --- |
| Virksomhedsbogføringsgrupper |Tildel denne gruppe til debitorer og kreditorer for at angive, hvem du sælger til, og hvem du køber fra. Konfigurer dem på siden **Virksomhedsbogføringsgrupper**. Når du gør det, skal du tænke på, hvor mange grupper du skal bruge for at opdele køb og salg. Du kan f.eks. gruppere debitorer og kreditorer efter geografisk område eller efter type virksomhed. |
| Produktbogføringsgrupper |Tildel denne gruppe til varer og ressourcer for at angive, hvad du sælger, og hvad du køber. Konfigurer dem på siden **Produktbogføringsgrupper**. Når du gør det, skal du overveje, hvor mange grupper du skal bruge for at opdele salg efter produkt (varer og ressourcer) og køb efter vare. Opdel f.eks. disse grupper efter råvarer, detail, ressourcer, kapacitet osv. |
| Bogføringsopsætninger |Kombiner virksomheds- og produktbogføringsgrupper, og vælg de konti, der skal bogføres på. Du kan for hver kombination af virksomheds- og produktbogføringsgrupper tildele et sæt finanskonti. Det betyder, at du f.eks. kan bogføre salget af samme vare på forskellige salgskonti i finansposterne, fordi debitorer tilknyttes til forskellige virksomhedsbogføringsgrupper. Du kan konfigurere dem på siden **Bogføringsopsætning**. |

| Specifikke bogføringsgrupper | Beskrivelse |
| --- | --- |
| Debitorbogføringsgrupper |Definer de konti, der skal bruges, når du bogfører transaktioner for tilgodehavender. Hvis du bruger lagerbeholdning med tilgodehavender, vil den virksomhedsbogføringsgruppe, der er tildelt debitorerne, og den produktbogføringsgruppe, der er tildelt lagervaren, bestemme, hvilke konti salgsordrelinjeposterne skal bogføres på. Se "Virksomhedsbogføringsgrupper" og "Produktbogføringsgrupper" under **Generelle bogføringsgrupper** ovenfor. Konfigurer grupperne på siden **Debitorbogføringsgrupper**. |
| Kreditorbogføringsgrupper |Angiv, hvor der skal bogføres transaktioner for samlekonti, gebyrkonti og kontantrabatkonti. Dette minder om debitorbogføringsgrupper. Konfigurer grupperne på siden **Kreditorbogføringsgrupper**. |
| Varebogføringsgrupper |Definer varebogføringsgrupper, som du derefter skal tildele til de relevante varekonti på siden **Varebogføringsopsætning**. Det betyder, at når du bogfører poster, der vedrører en vare, bliver de automatisk bogført til den finanskonto, der er defineret for den kombination af varebogføringsgruppe og lokation, som er sammenkædet med varen. Varebogføringsgrupper er også en god måde at organisere lageret på, så du kan adskille varer efter deres bogføringsgrupper, når du opretter rapporter. Konfigurer grupperne på siden **Varebogføringsgrupper**. |
| Bankkontobogføringsgrupper |Angiv bankkonti for bankkonti. Dette kan f.eks. forenkle processer til sporing af transaktioner og afstemning af bankkonti. Konfigurer dem på siden **Bankkontobogføringsgrupper**. |
| Anlægsbogføringsgrupper |Angiv konti for forskellige typer udgifter og omkostninger, f.eks. anskaffelser, akkumulerede afskrivningsbeløb, anskaffelse ved afgang, afskrivning ved afgang, gevinst ved afgang, tab ved afgang, reparationer og afskrivning ved drift. Konfigurer grupperne på siden **Anlægsbogføringsgrupper**. |

| Momsbogføringsgruppe | Beskrivelse |
| --- | --- |
| Momsvirksomhedsbogføringsgrupper |Bestem, hvordan salgsmoms skal beregnes og bogføres for debitorer og kreditorer. Konfigurer dem på siden **Momsvirksomhedsbogf.grupper**. Når du gør det, skal du overveje, hvor mange grupper du har brug for. Det kan f.eks. afhænge faktorer som lokal lovgivning, og om du handler både nationalt og internationalt. |
| Momsproduktbogføringsgrupper |Angiv momsberegninger, der er nødvendige for de typer varer eller ressourcer, du køber eller sælger. |
| Momsbogføringsopsætning |Kombiner momsvirksomhedsbogføringsgrupper og momsproduktbogføringsgrupper. Når du udfylder en finanskladdelinje, købslinje eller salgslinje, ser vi på kombination for at identificere, hvilke konti der skal bruges. |

## <a name="example-of-linking-posting-groups"></a>Eksempel på sammenkædning af bogføringsgrupper
Her er et scenarie.  

Disse bogføringsgrupper er valgt på debitorkortet:  

* Virksomhedsbogføringsgruppe
* Debitorbogføringsgruppe  

Disse bogføringsgrupper er valgt på varekortet:  

* Produktbogføringsgrupper  
* Varebogføringsgruppe  

Når du opretter et salgsdokument, bruges oplysningerne fra debitorkortet ind i salgshovedet, og oplysningerne fra varekortet bruges i salgslinjerne.  

* Bogføringen af indtægter (resultatopgørelsen) bestemmes af kombinationen af virksomhedsbogføringsgruppen og produktbogføringsgruppen.  
* Bogføringen af tilgodehavender (balancen) bestemmes af debitorbogføringsgruppen.  
* Bogføringen af lager (balancen) bestemmes af varebogføringsgruppen.  
* Bogføringen af kostprisen for solgte varer (resultatopgørelsen) bestemmes af kombinationen af virksomhedsbogføringsgruppen og produktbogføringsgruppen.  

Din opsætning bestemmer, hvornår bogføringen foretages. For eksempel afhænger timingen af, hvornår du udfører periodiske aktiviteter, f.eks. bogfører lagerværdien eller regulerer kostværdi-vareposter.

## <a name="copying-posting-setup-lines"></a>Kopiere bogføringsopsætningslinjer
Jo flere produkt- og virksomhedsbogføringsgrupper, du har, jo flere linjer ser du på siden Bogføringsopsætning. Dette kan betyde en masse dataangivelse for at konfigurere bogføringsopsætningen for virksomheden. Selvom der muligvis er mange forskellige kombinationer af virksomheds- og produktbogføringsgrupper, kan forskellige kombinationer stadig bogføre til de samme finanskonti. Hvis du vil begrænse mængden af manuel dataangivelse, skal du kopiere finanskontiene fra en eksisterende linje på siden **Bogføringsopsætning**.

## <a name="set-up-posting-groups-on-the-go"></a>Konfigurere bogføringsgrupper på farten

Brugere kan komme hurtigere i gang med [!INCLUDE[prod_short](includes/prod_short.md)], der giver mulighed for at hjælpe via meddelelser om manglende finanskonti i de forskellige opsætninger af bogføringsgrupper i dokumenter. Hvis du vil have vist disse notifikationer, skal du kontrollere, at **Finanskontoen mangler i bogføringsgruppe eller installationsmeddelelse** er valgt på siden **Mine notifikationer**, som du kan få adgang til fra feltet **Rediger, når jeg modtager notifikationer** på siden **Mine indstillinger**.  

På den måde får du besked, når du arbejder på et dokument, der bruger en bogføringsgruppe eller en opsætning, der mangler en nødvendig finanskonto. Vælg linket i notifikationen Åbn en side, hvor du kan foretage de relevante ændringer, hvis du har tilladelse til det.  

> [!NOTE]
> Hvis du vil føre dig direkte til den bogføringsgruppe eller opsætning, der mangler en finanskonto, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en pladsholder til bogføringsgruppe eller opsætning. Bogføringsgrupper og opsætninger er en måde, som bogholderen kan bruge til at styre, hvordan poster bogføres i finansregnskabet, så det er muligt, at du ikke kan oprette just-in-time-bogføringsgrupper og -opsætninger i din organisation.  
> 
> Hvis det er tilfældet, skal du deaktivere notifikationen **Finanskonto mangler i bogføringsgruppe eller opsætning**, og du skal derefter samarbejde med bogholderen for at foretage de relevante ændringer af bogføringsgruppen, opsætningen eller dokumentet. Dette er et vigtigt trin, fordi når dokumenterne er bogført, kan alle ukorrekte bogføringsgrupper eller opsætninger ikke slettes, da der er oprettet finansposter til dem. 

## <a name="troubleshooting-posting-group-errors"></a>Fejlfinding i forbindelse med bogføringsgruppefejl
Bogføringsgrupper er et af de mere avancerede begreber, der skal konfigureres i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis de ikke er konfigureret korrekt, kan der opstå fejl ved bogføring af dokumenter eller kladdelinjer. Disse fejl skyldes f.eks. typisk en fejl i, hvordan finanskonti tildeles, eller hvordan bogføringsgrupper kombineres.

Når der er noget galt, viser [!INCLUDE[prod_short](includes/prod_short.md)] siden **Fejlmeddelelser**. Siden **Fejlmeddelelser** kan gøre det nemmere at identificere og løse problemet. Siden indeholder en beskrivelse af den fejl, der påpeger den bogføringsgruppeopsætning, der kræver opmærksomhed. Meddelelsen kan f.eks. lyde "Salgsforudbetalingskontoen mangler en bogføringsopsætning". Der er også et link til at åbne siden, der er kilden til problemet, så du hurtigt kan løse det.  

> [!NOTE]
> Den fejlhåndtering, der er beskrevet ovenfor, er ikke tilgængelig i vare-, ressource-, medarbejder- og anlægsaktivkladder eller for finanskonti, der er tilføjet i lokale versioner af bogføringsgrupper.

## <a name="see-also"></a>Se også
[Finans- og kontoplanen](finance-general-ledger.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
