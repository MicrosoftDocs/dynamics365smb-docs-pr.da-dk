---
title: Om opsætning af moms | Microsoft Docs
description: Sørg for at beregne, bogføre og rapportere moms på køb og salg korrekt.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/13/2020
ms.author: bholtorf
ms.openlocfilehash: 1bdd140e43a29894978f7fa0f0a88957d7e102c3
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030144"
---
# <a name="set-up-value-added-tax"></a>Konfigurere moms
Forbrugere og virksomheder betaler moms, når de køber varer eller tjenesteydelser. Momsbeløbet, der skal betales, kan variere afhængigt af flere faktorer. I [!INCLUDE[d365fin](includes/d365fin_md.md)] konfigurerer du moms til at angive de satser, der bruges til at beregne momsbeløb baseret på følgende:

* Hvem du sælger til  
* Hvem du køber fra  
* Hvad du sælger  
* Hvad du køber.  

Du kan konfigurere momsberegninger manuelt, men der kan være svært og tidskrævende. For at gøre det nemt for dig har vi lavet en assisteret opsætningsvejledning, **Momsopsætning**, der hjælper dig med fremgangsmåden. Du anbefales at bruge den assisterede opsætningsvejledning, når du konfigurerer moms.

> [!NOTE]  
>   Du kan kun bruge vejledningen, hvis du har oprettet Min virksomhed og ikke har bogført transaktioner, der omfatter moms. Ellers kan du nemt komme til at bruge forskellige momssatser utilsigtet og gøre rapporter vedrørende moms unøjagtige.  

Hvis du selv vil konfigurere momsberegninger eller bare vil vide mere om de enkelte trin, indeholder i dette emne beskrivelser af de enkelte trin.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Sådan bruges den assisterede momsopsætningsvejledning til at konfigurere moms (anbefales)
Du anbefales at bruge den assisterede momsopsætningsvejledning, når du konfigurerer moms i [!INCLUDE[d365fin](includes/d365fin_md.md)].

For at starte vejledningen skal du gøre følgende:
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), og angiv **Assisteret opsætning**.  
2. Vælg **Konfigurer moms**, og fuldfør trinnene.
3. Når du har fuldført den assisterede opsætning, skal du gå til **Momsbogf.opsætning** og kontrollere, om du er nødt til at udfylde yderligere felter i henhold til din lokale landeversion. Du kan finde flere oplysninger i [Lokal funktionalitet i Business Central](about-localization.md)  

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>Sådan defineres momsregistreringsnumre for dit land eller område
For at sikre, at brugere angiver gyldige momsregistreringsnumre, kan du definere formater til momsregistreringsnumre, som bruges i de lande eller områder, hvor du handler. [!INCLUDE[d365fin](includes/d365fin_md.md)] viser en fejlmeddelelse, når en bruger laver en fejl eller bruger et format, der er forkert for landet eller området.

For at oprette momsregistreringsnumre, skal du gøre følgende:
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), og angiv **Lande/områder**.
2. Vælg landet eller området, og vælg derefter handlingen **SE/CVR-nr.formater**.
3. I feltet **Formater** skal du angive formatet ved at angive et eller flere af følgende tegn:  

* **#** Kræver et etcifret tal.  
* **@** Kræver et bogstav. Der skelnes ikke mellem store og små bogstaver.  
* **?** Tillader alle tegn.  

    > [!Tip]
    > Du kan bruge andre tegn, så længe de er altid findes i formatet for landet eller området. Hvis du f.eks. vil medtage et punktum eller en bindestreg mellem sæt af tal, kan du angive formatet som ##.####.### eller @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Sådan oprettes virksomhedsbogføringsgrupper
Formålet med momsvirksomhedsbogføringsgrupper er at repræsentere de markeder, hvor du handler med debitorer og kreditorer, og definere, hvordan moms beregnes og bogføres på hvert enkelt marked. Eksempler på momsvirksomhedsbogføringsgrupper er **Danmark** og **Den Europæiske Union (EU)**.  

Brug koder, der er lette at huske, og som beskriver virksomhedsbogføringsgruppen, f.eks. **EU**, **Ikke-EU** eller **Danmark**. Koden skal være entydig. Du kan oprette lige så mange koder, som du har brug for, men du kan kun bruge den samme kode én gang i en tabel.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsvirksomhedsbogf.gruppe**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

Du kan oprette standardmomsvirksomhedsbogføringsgrupper ved at linke dem til virksomhedsbogføringsgrupper. [!INCLUDE[d365fin](includes/d365fin_md.md)] tildeler automatisk momsvirksomhedsbogføringsgruppen, når du tildeler virksomhedsbogføringsgruppen til en debitor, kreditor eller finanskonto.

## <a name="to-set-up-vat-product-posting-groups"></a>Sådan oprettes momsproduktbogføringsgrupper
Momsproduktbogføringsgrupper repræsenterer de varer eller ressourcer, du køber eller sælger, og bestemmer, hvordan moms beregnes og bogføres i overensstemmelse med den type vare eller ressource, der købes eller sælges.  
Det anbefales at bruge koder, der er lette at huske, og som beskriver satsen, som f.eks. **FRITAGET** eller **Nul**, **MOMS10** eller **Reduceret** for 10 % moms og **MOMS25** eller **Standard** for 25 % moms.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Sådan kombineres momsbogføringsgrupper i momsbogføringsopsætninger
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner momsbeløb af køb og salg baseret på momsbogføringsgrupper, der er kombinationer af momsvirksomheds- og -produktbogføringsgrupper. For hver kombination kan du angive momsprocenten, momsberegningstypen og finanskontonumre for bogføring af købs-, salgs- og modtagermoms. Du kan også angive, om moms skal genberegnes, når en kontantrabat anvendes eller modtages.  

Du kan definere et ubegrænset antal kombinationer. Hvis du vil gruppere kombinationer af momsbogføringsopsætninger med lignende attributter, kan du angive et **Moms-id** for hver enkelt gruppe og tildele id'et til gruppemedlemmerne.

Hvis du vil kombinere momsbogføringsopsætninger, skal du gøre følgende:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Sådan tildeles momsbogføringsgrupper til flere enheder som standard
Hvis du vil anvende de samme momsbogføringsgrupper på flere enheder, kan du konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til at gøre det som standard. Dette kan gøres på flere måder:

* Du kan tildele momsvirksomhedsbogføringsgrupper til generelle virksomhedsbogføringsgrupper eller debitor- eller kreditorskabeloner
* Du kan tildele momsproduktbogføringsgrupper til generelle produktbogføringsgrupper  

Momsvirksomheds- eller produktbogføringsgruppen tildeles, når du vælger en virksomheds- eller produktbogføringsgruppe til en debitor, kreditor, vare eller ressource.

## <a name="assigning-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tildele momsbogføringsgrupper til konti, debitorer, kreditorer, varer og ressourcer
I følgende afsnit beskrives, hvordan du tildeler momsbogføringsgrupper til individuelle poster.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Sådan tildeles momsbogføringsgrupper til individuelle finanskonti
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. Åbn **Finanskonto**-kortet for kontoen.  
3. I oversigtspanelet **Bogføring** i feltet **Bogføringstype** skal du vælge enten **Salg** eller **Køb**.  
5. Vælg de momsbogføringsgrupper, du vil bruge til salgs- eller købskontoen.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Sådan tildeles momsvirksomhedsbogføringsgrupper til debitorer og kreditorer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.  
2. Udvid oversigtspanelet **Fakturering** på **Debitor**- eller **Kreditor**-kortet.  
3. Vælg momsvirksomhedsbogføringsgruppen.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Sådan tildeles momsproduktbogføringsgrupper til individuelle varer og ressourcer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Vare** eller **Ressource**, og vælg derefter det relaterede link.  
2. Gør ét af følgende:  

* På kortet **Vare** skal du udvide oversigtspanelet **Pris og bogføring** og derefter vælge **Vis mere** for at se feltet **Momsproduktbogf.gruppe**.  
* Udvid oversigtspanelet **Fakturering** på **Ressource**-kortet.  
3. Vælg momsproduktbogføringsgruppen.  

## <a name="setting-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Oprette klausuler, der forklarer momsfritagelse eller ikke-standard-momssatser
Du konfigurerer en momsklausul til at beskrive oplysninger om den moms, der skal anvendes. Oplysningerne kan være påkrævet som påbudt af myndighederne. Når du har konfigureret en momsklausul og tilknyttet den til en momsbogføringsgruppe, vises momsklausulen på udskrevne salgsdokumenter, der bruger momsbogføringsopsætningsgruppen.

Hvis det er nødvendigt, kan du også angive, hvordan momsklausuler skal oversættes til andre sprog. Når du derefter opretter og udskriver et salgsdokument, der indeholder et moms-id, vil det udskrevne dokument indeholde den oversatte momsklausul. Den sprogkode, der er angivet på debitorkortet, bestemmer sproget.

Når ikke-standard-momssatsen anvendes i forskellige typer dokumenter, f. eks. fakturaer eller kreditnotaer, skal virksomheder normalt angive en fritagelsestekst (momsklausul) om, hvorfor der er beregnet en nedsat moms eller ingen moms. Du kan definere forskellige momsklausuler, der skal indgå i forretningsdokumenter, f. eks. faktura eller kreditnota. Dette gøres på siden **Momsklausuler efter dok.type**.

Du kan redigere eller slette en momsklausul, og dine ændringer afspejles i en genereret rapport. Men [!INCLUDE[d365fin](includes/d365fin_md.md)] bevarer ikke en oversigt over ændringen. På rapporten udskrives og vises momsklausulbeskrivelserne for alle linjer i rapporten sammen med momsbeløbet og momsgrundbeløbet. Hvis en momsklausul ikke er defineret for alle linjer i salgsdokumentet, så udelades hele sektionen, når rapporten udskrives.

### <a name="to-set-up-vat-clauses"></a>Sådan konfigureres momsklausuler
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Oprette en ny linje på siden **Momsklausuler**.  
3. Angiv et id for klausulen i feltet **Kode**. Du bruger koden til at tildele klausulen til momsbogføringsgrupper.  
4. I feltet **Beskrivelse** skal du angive den momsfritagelse, du vil have vist i dokumenter, som kan inkludere moms. I feltet **Beskrivelse 2** skal du angive supplerende tekst, hvis det er nødvendigt. Teksten vises på nye dokumentlinjer.
5. Vælg handlingen **Beskrivelse efter dokumenttype**.
6. Udfyld felterne på siden **Momsklausuler efter dok.type** for at angive, hvilken momsfritagelsestekst der skal vises for hvilken dokumenttype.  
7. Valgfrit: Hvis du vil tildele momsklausulen til en momsbogføringsopsætning med det samme, skal du vælge **Opsætning** og derefter vælge klausulen. Hvis du vil vente, kan du tildele klausulen senere på siden **Momsbogf.opsætning**.  
8. Valgfrit: Hvis du vil angive, hvordan momsklausulen skal oversættes, skal du vælge handlingen **Oversættelser**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Sådan tildeles en momsklausul til en momsbogføringsopsætning
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
2. I kolonnen **Momsklausul** skal du vælge den klausul, der skal bruges til hver momsbogføringsopsætning, den gælder for.  

### <a name="to-specify-translations-for-vat-clauses"></a>Sådan angives oversættelser af momsklausuler
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Oversættelser**.  
3. I feltet **Sprogkode** skal du vælge det sprog, du vil oversætte til.  
4. I felterne **Beskrivelse** og **Beskrivelse 2** skal du angive oversættelserne af beskrivelserne. Teksten vises i de oversatte momsrapportdokumenter.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Sådan oprettes en momsbogføringsopsætning for at håndtere importmoms
Du kan bruge funktionen Importmoms, når du skal bogføre et dokument, hvor hele beløbet er moms. Du skal bruge funktionen, hvis du modtager en faktura fra skattemyndighederne for moms på importerede varer.  

Når du vil konfigurere koder for importmoms, skal du gøre følgende:  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. På siden Momsproduktbogf.grupper. skal du oprette en ny momsproduktbogføringsgruppe for importmoms.  
3. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
4. På siden Opsætning af momsbogføring skal du oprette en ny linje eller bruge en eksisterende momsvirksomhedsbogføringsgruppe kombineret med den nye momsproduktbogføringsgruppe til importmoms.  
5. I feltet **Momsberegningstype** skal du vælge **Momskorrektion**.  
6. Angiv den finanskonto, der skal bruges til bogføring af importmoms, i feltet **Købsmomskonto**. Alle andre konti er valgfrie.  


## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Sådan bruges modtagermoms for handel mellem EU-lande eller -områder
Nogle virksomheder skal bruge modtagermoms, når de handler med andre virksomheder. Denne regel gælder f.eks. for køb fra EU-lande/områder og salg til EU-lande/områder.  

> [!NOTE]  
> Reglen gælder, når der handles med de virksomheder, som er registreret som momspligtige i et andet EU-land. Hvis du handler direkte med forbrugere i andre EU-lande/område, skal du kontakte skattemyndighederne for at få oplyst de gældende momsregler.  

> [!TIP]  
> Du kan kontrollere, at en virksomhed er registreret som momspligtig i et andet EU-land ved hjælp af tjenesten til kontrol af SE/CVR-nr. for EU. Tjenesten er tilgængelig og gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i afsnittet _Kontrollere SE/CVR-numre_ i dette emne.

### <a name="sales-to-eu-countries-or-regions"></a>Salg til EU-lande eller -områder
Moms beregnes ikke på salg til momspligtige virksomheder i andre EU-lande/regioner. Du skal rapportere værdien af disse salg til EU-lande/områder separat på momsangivelsen.  

For at beregne moms på salg til EU-lande/områder korrekt, skal du:  

* Opret linjer for salg med de samme oplysninger for køb. Hvis du allerede har oprettet linjer på siden Momsbogf.opsætning for køb fra EU-lande/områder, kan du også bruge disse linjer til salg.  
* Tildele momsvirksomhedsbogføringsgrupperne i feltet **Momsvirksomhedsbogf.gruppe** på oversigtspanelet **Fakturering** på kreditorkort for hver EU-kreditor. Du skal også angive debitorens CVR-nummer i feltet **SE/CVR-nr.** på oversigtspanelet **Udenrigshandel**.  

Når du bogfører salg til en debitor i et andet EU-land/område, beregnes momsbeløbet, og der oprettes en momspost med oplysningerne om modtagermomsen og momsgrundbeløbet, som er det beløb, der bruges til at beregne momsbeløbet. Der bogføres ingen poster på momskontoen i finansposterne.

## <a name="understanding-vat-rounding-for-documents"></a>Om momsafrunding for bilag
Beløb i de bilag, som endnu ikke er blevet bogført, afrundes og vises, så de svarer til de endelige afrundingsbeløb, som bogføres. Moms beregnes for et helt dokument, hvilket betyder, at moms, der beregnes, er baseret på summen af alle linjer med samme moms-id i dokumentet.




## <a name="see-also"></a>Se også
[Konfigurere momsangivelsestyper og momsangivelsesnavne](finance-how-setup-vat-statement.md)   
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)      
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)      
[Arbejde moms af salg og køb](finance-work-with-vat.md)    
[Arbejde med Momssatsændringsværktøj](finance-how-use-vat-rate-change-tool.md)    
[Kontrollere SE/CVR-numre](finance-how-validate-vat-registration-number.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learnlearnpathsprocess-vat-dynamics-365-business-central"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)
