---
title: Om beregning af standardkostpris | Microsoft Docs
description: "Et system til standardkostpriser bestemmer lagerkostprisen på basis af nogle rimelige historiske eller forventede omkostninger. Undersøgelser af tidligere og fremtidige omkostningsdata kan derefter danne grundlag for standardkostpriser."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: be73736f4c56ea78ef2bb2b736b76db0569312ec
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="about-calculating-standard-cost"></a>Om beregning af standardomkostning
Mange produktionsvirksomheder vælger en værdiansættelse for standardkostpriser. Dette gælder også for virksomheder, der udfører let produktion som montage og kitting. Et system til standardkostpriser bestemmer lagerkostprisen på basis af nogle rimelige historiske eller forventede omkostninger. Undersøgelser af tidligere og fremtidige omkostningsdata kan derefter danne grundlag for standardkostpriser. Standardkostpriserne er fastfrosne, indtil der træffes en beslutning om, at de skal ændres. De faktiske omkostninger til at fremstille et produkt kan afvige fra de forventede standardomkostninger. Af hensyn til styringen sammenlignes den faktiske kostpris med standardkostprisen for en bestemt vare, og forskellene, eller *afvigelser*, identificeres og analyseres.  

Standardkostpriserne kan opretholdes for varer, der genopfyldes via indkøb, montage og produktion. For hver genbestillingsmetode kan standardkostpriserne bestå af følgende elementer.  

|Genbestillingssystem|Standardkostpriselementer|  
|--------------------------|----------------------------|  
|**Køb**|Direkte materialeomkostninger og faste materialeomkostninger efter behov.|  
|**Montage**|Direkte materialeomkostninger, direkte eller faste arbejdsomkostninger og faste omkostninger.|  
|**Prod.ordre**|Direkte materialeomkostninger, arbejdsomkostninger, underleverandøromkostninger og faste omkostninger.|  

## <a name="setting-up-standard-costs"></a>Oprette standardkostpriser  
Da standardkostprisen for en fremstillet vare eller en montagevare kan bestå af flere kostelementer, herunder materialeomkostninger, kapacitetsomkostninger (arbejdskraft) og direkte og faste underleverandøromkostninger, skal der oprettes standardkostpriser for hvert af disse elementer.  

Opgaven for en fremstillingsvirksomhed, der bruger standardkostpriser, består af:  

-   At anslå en standardkostpris for den færdig vare og at oprette den på varekortet.  
-   At registrere og allokere de faktiske omkostninger til de vigtigste omkostningselementer og tage højde for afvigelser.  

Alle komponentomkostninger skal lægges sammen for at bestemme den direkte kostpris for en færdig vare. En samlet eller produceret vare kan omfatte underordnede samlinger, som også består af flere komponenter.  

Følgende vigtigste omkostningselementer udgør den samlede direkte omkostning for en færdig produktionsvare:  

-   Materialekostpriser.  
-   Kapacitetskostpris.  
-   Underleverandøromkostninger for kun producerede varer.  

### <a name="material-costs"></a>Materialeomkostninger  
 Materialekostpriser, der er forbundet med underordnede samlinger og indkøbte råvarer. Materialekostprisen kan bestå af direkte og indirekte kostelementer.  

-   Direkte materialeomkostninger repræsenterer et faktureret beløb for købte råmaterialer eller omkostningen til fremstilling af en underordnet samling.  
-   Indirekte materialeomkostninger, eller *faste omkostninger* kan være elementer som f.eks. lageromkostninger for den færdige vare, efter at den er fremstillet.  

Opsætningen af materialeomkostninger for købte varer, der påvirker direkte og indirekte omkostninger, afhænger af den kostmetode, der er valgt for den pågældende vare. Du kan oprette omkostningsoplysninger for hver kostmetode på varekortet. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

Omkostningen til spild (kun produktion) er en anden faktor, du skal overveje, når du beregner den samlede materialeomkostning. Når en bestemt mængde råmateriale går til spilde under montage eller fremstilling af en vare, medfører det generelt en forøgelse af de komponenter, der skal bruges til fremstilling af varen. Dette medfører desuden en stigning i materialeomkostningerne for de komponenter, der bruges under fremstilling af den overordnede vare. Du opretter spildomkostninger for materialer på enten produktionsstyklisten eller produktionsruten.  

Materialeomkostningerne for en fremstillet vare kan repræsenteres på to måder, der svarer til følgende kostprisberegninger.  

|Kostprisberegningsgrundlag|Materialekostprisberegning|  
|----------------------------|-------------------------------|  
|Enkelt niveau|Produceret vare er lig med det samlede kostbeløb af alle varer, der er indkøbte eller underordnede samlinger, på denne vares produktionsstykliste.|  
|Akkumuleret niveau eller flere niveauer|Den fremstillede vare er summen af materialeomkostningerne for alle underordnede samlinger på varens stykliste og omkostningerne for alle købte varer på varens produktionsstykliste.|  

### <a name="capacity-costs"></a>Kapacitetsomkostninger  
Kapacitetsomkostninger er omkostninger, der er knyttet til intern arbejdskraft og maskinomkostninger. Du skal angive disse omkostninger for hver ressource (i montagestyring) og arbejds- eller produktionscenter på ruten (i produktion). Som med materialer kan du identificere både direkte og indirekte elementer af kapacitetsomkostninger. Den direkte omkostning for et arbejdscenter kan f.eks. være den fastsatte produktionstakst for udførelse af en bestemt funktion. Den indirekte omkostning for et arbejdscenter kan repræsentere nogle generelle fremstillingsomkostninger, f.eks. lys, varme osv. Som med materialeomkostninger kan indirekte kapacitetsomkostninger udtrykkes som en indirekte omkostningsprocent eller en fast sats.  

Oprettelsen af kapacitetsomkostningerne for montagevarer består af følgende elementer:  

-   Direkte og indirekte kostpris for ressourcen.  
-   Type af fast eller direkte ressourceforbrug.  

Oprettelsen af kapacitetsomkostningerne for fremstillede varer består af følgende elementer:  

-   Direkte og indirekte kostpris for produktions- eller arbejdscentret.  
-   Oprettelse af tid og lotstørrelsen.  

Hvis du vil beregne standardkapacitetsomkostningerne, skal du etablere de standardtimesatser, der kræves for at foretage opgaver i maskin- og arbejdscentre. Den samlede tid til at færdiggøre en operation består som regel af tid til opstilling og kørsel samt vente- og flyttetid.  

Du opretter satserne for hver tidstype for hver maskine eller hvert arbejdscenter på en individuel rute.  

> [!NOTE]  
>  Mens timesatserne for kørsel gælder pr. fremstillet vare, gælder timesatserne for opstilling pr. lot. Derfor skal rutens opstillingstid for hver operation fordeles over lotstørrelsen. Du skal angive lotstørrelsen i det tilsvarende felt i oversigtspanelet **Bestilling** på varekortet.  

Hvis du vil angive opstillingstiden på ruten af hensyn til planlægningen, men ikke vil medtage denne omkostning i standardkostprisberegningen, skal du fjerne markeringen i feltet **Kostpris inkl. opstilling** på siden **Produktionsopsætning**.  

På enkeltniveaubasis er det den arbejdsomkostning, der kræves til fremstilling af den færdige vare, og den angives på fremstillingsvarens rute. På akkumuleret niveau er dette den kapacitetsomkostning, der er angivet for hver enkelt fremstillet vare, der er medtaget på den overordnede vares stykliste.  

### <a name="subcontractor-costs"></a>Underleverandøromkostninger  
Underleverandøromkostningerne er de omkostninger, der er knyttet til serviceydelser, der leveres af en virksomheds eksterne leverandører eller underleverandører. Ligesom for materiale- og kapacitetsomkostninger kan underleverandøromkostninger bestå af både direkte og indirekte omkostninger. Direkte underleverandøromkostninger repræsenterer det faktiske beløb for hver serviceenhed, der leveres. Faste underleverandøromkostninger kan f.eks. repræsentere fragtomkostninger og håndteringsomkostninger i forbindelse med en ordre til en underleverandør.  

Da underleverandøropgaver er en udliciteret kapacitet, skal du oprette omkostningerne for både direkte og indirekte underleverandørtjenester på det arbejdscenterkort, der repræsenterer underleverandøroperationen.  

## <a name="updating-standard-costs"></a>Opdatere standardkostpriser  
Hvis du vil opdatere eller beregne standardkostprisen for montageelementer, skal du bruge funktionen fra varekortet.  

Processen med at opdatere eller beregne standardkostpriser består typisk af følgende opgaver:  

1.  Opdatering af omkostninger på komponent- og kapacitetsniveau. Du kan finde flere oplysninger i kørslerne **Foreslå kostpris (standard)** og **Foreslå kapacitetskostpris (standard)**.  
2.  Konsolidering og akkumulering af komponent- og kapacitetsomkostninger til beregning af den samlede montage eller de samlede fremstillingsomkostninger for varerne. Du kan finde flere oplysninger i afsnittet "Sådan beregnes kostprisen for et montageelement" i [Arbejde med styklister](inventory-how-work-BOMs.md).  
3.  Implementering af de standardkostpriser, der angives, når du kører de tidligere kørsler. Standardkostpriserne træder ikke i kraft, før de er implementeret. Du kan finde flere oplysninger i kørslen **Implementer std.kostprisændringer**.  
4.  Implementering af ændringer for at opdatere feltet **Kostpris** på varekortet og udførsel af lagerværdiregulering. Du kan finde flere oplysninger under [Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

## <a name="see-also"></a>Se også  
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md)   
 [Arbejde med styklister](inventory-how-work-BOMs.md)   
 [Opdatere standardkostpriser](finance-how-to-update-standard-costs.md)   
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)

