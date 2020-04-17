---
title: Få en oversigt over disponering | Microsoft Docs
description: Du kan få vist oplysninger om varedisponeringen eller -beholdningen på tværs af lokationer pr. salg eller købshændelser, efter en periode eller efter varens placering på en montage- eller produktionsstykliste.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 04/01/2020
ms.author: SorenGP
ms.openlocfilehash: fc7a0c6f750958cb35b2a85ed9d548f2e8219484
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182320"
---
# <a name="view-the-availability-of-items"></a>Vise varedisponering
Fra konteksten for en virksomhedsopgave kan du få avancerede oplysninger om, hvornår og hvor en vare er tilgængelig, f.eks, når du taler med en kunde om en leveringsdato.

Du kan få vist disponeringen for alle varer pr. lokation, og du kan få vist disponeringen for hver enkelt vare ud fra hændelse, periode eller lokation. En hændelse er enhver planlagt varetransaktion, f.eks en salgsleverance eller modtagelse af en indgående overflytning.

> [!NOTE]  
>   Visninger af tilgængelighed pr. lokation kræver, at du har lager på mere end én lokation. Der er flere oplysninger i [Opsætte lokationer](inventory-how-setup-locations.md).

Hvis du bruger lageraktivitet, varierer tilgængeligheden afhængigt af allokeringer på placeringsniveauet, når lageraktiviteter som pluk og bevægelser forekommer, og når lagerreservationssystemet pålægger begrænsninger, der skal overholdes. En meget kompleks algoritme kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb. Du kan finde flere oplysninger i [Designoplysninger: Tilgængelighed i lageret](design-details-availability-in-the-warehouse.md).

I [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængelighedstal typisk vist i to forskellige felter, med hver sin definition:

* Feltet **Lager**, som også kaldes **Lagerbeholdning**, viser den faktiske lagerbeholdning i dag ud fra de bogførte vareposter.
* Feltet **Planlagt disponibel balance** beregnes og viser lagerbeholdningen plus fastlagte tilgange minus bruttobehovet. (I [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer fastlagte tilgange antal på købsordrer og indgående overflytningsordrer. Bruttobehov omfatter antal på salgsordrer og udgående overflytningsordrer).

> [!TIP]  
>   Den planlagte disponible balance er især relevant at få vist på siderne **Varedisponering pr. periode** og **Varedisponering pr. hændelse**, da de indeholder datedimensionen.  

> [!NOTE]  
>   De følgende procedurer beskriver, hvordan du får vist avancerede tilgængelighedsoplysninger fra varelisten og varekortet. Du kan også få adgang til oplysninger fra salgsdokumentlinjer for varen på linjen. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Sådan får du vist tilgængeligheden for en vare, ud fra hvornår den er modtages eller leveres
Du får vist tilgængeligheden for en vare i overensstemmelse med planlagte varetransaktioner på siden **Disponering pr. hændelse**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist disponering for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Hændelse**.

    Siden **Varedisponering pr. hændelse** viser, hvordan lagerantallet for varen udvikler sig over tid i overensstemmelse med planlagt levering og modtagelse. Siden giver en komprimeret visning, der viser én linje med akkumulerede oplysninger pr. tidsinterval, hvor lagermængderne ændres. Tidsintervaller, hvor der ikke opstod nogen begivenheder, vises ikke. Du kan udvide hver linje for at få vist detaljer om den eller de begivenheder, der forårsagede det akkumulerede antal på linjen.
4. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Sådan får du vist disponeringen for en vare i forskellige perioder
Du får vist disponeringen for en vare over tid for angivne perioder på siden **Varedisponering pr. periode**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist disponering for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Periode**.

    Siden **Varedisponering pr. periode** viser, hvordan lagerbeholdningen for varen udvikler sig over tid, vist for en periode, du vælger, f.eks. Dag, Uge eller Kvartal.
4. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Sådan får du vist disponeringen for en vare på de lokationer, hvor den opbevares
På siden **Varedisponering pr. lokation** får du vist disponeringen for en vare på de forskellige steder, hvor den opbevares.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist disponering for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Lokation**.

    Siden **Varedisponering pr. lokation** viser, hvordan lagerbeholdningen for varen udvikler sig i fremtiden, vist for hver lokation, hvor varen opbevares.
4. Vælg værdien i feltet **Beholdning** for at få vist de vareposter, der udgør værdien.
5. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Sådan får du vist disponeringen for alle varer ud fra den lokation, hvor de opbevares
Du får vist disponeringen for alle dine varer på tværs af alle dine lokationer på siden **Varer pr. lokation**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Varer pr. lokation**.

    Siden **Varer pr. lokation** viser for alle varer, hvor mange er tilgængelige på hver enkelt lokation.
3. Vælg værdien i feltet **Beholdning** for at få vist de vareposter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Sådan får du vist tilgængeligheden af en vare ud fra brugen af den på montage- eller produktionsstyklister
Hvis en vare findes på montage- eller produktionsstyklister, enten som en overordnet vare eller som en komponent, kan du se, hvor mange enheder af den der er påkrævet, på siden **Varedisponering pr. styklisteniveau**. Siden angiver, hvor mange enheder af en overordnet vare, du kan fremstille, baseret på tilgængeligheden af underordnede varer eller underliggende linjer. En vare med en montage- eller produktionsstykliste vises på siden som en linje, der kan skjules. Du kan udvide denne linje for at få vist de underliggende komponenter og halvfabrikata på lavere niveau med deres egne styklister.

Du kan bruge siden til at finde ud af, om du kan opfylde en salgsordre for en vare på en bestemt dato ved at kigge på den aktuelle tilgængelighed og de mængder, der kan leveres med dens komponenter. Du kan også bruge siden til at identificere flaskehalse i relaterede styklister.

På hver linje på siden for både overordnede og underordnede varer angiver følgende nøglefelter tilgængelighedstallene. Du kan bruge disse tal til at love, hvor mange enheder af en overordnet vare, du kan levere, hvis du starter den relaterede montageproces.

|Felt|Beskrivelse|
|------|-----------|
|**Kan blive overordnet**|Viser, hvor mange enheder af halvfabrikata af topvaren, du kan fremstille. Feltet angiver, hvor mange umiddelbart overordnede enheder, du kan samle. Værdien er baseret på tilgængeligheden af varen på linjen.|
|**Kan blive topvare**|Viser, hvor mange enheder af topvaren, du kan fremstille. Feltet angiver, hvor mange enheder af styklistevaren på øverste linje, du kan samle. Værdien er baseret på tilgængeligheden af varen på linjen.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>Sådan vises disponeringen af en vare efter behov for dens overordnede
Siden **Varedisponering pr. styklisteniveau** viser oplysninger for varen på det kort eller den dokumentlinje, som siden åbnes for. Elementet vises altid på den øverste linje. Du kan få vist oplysninger for andre varer eller for alle varer ved at ændre værdien i feltet **Varefilter**.

> [!NOTE]  
>   Som standard viser tilgængelighedstallene på linjerne den samlede tilgængelighed af alle varer under topvaren. Disse tal vises i feltet **Disponibelt antal** og fokuserer på topvaren. Oplysninger om, hvor mange halvfabrikata, du kan fremstille kan dog blive skævt. Hvis du ønsker at få en angivelse af, hvor mange af de viste halvfabrikata, du kan fremstille, skal du rydde feltet **Vis samlet disponering** og derefter se tallet i feltet **Kan blive overordnet**.

Feltet **Flaskehals** angiver, hvilken vare i styklistestrukturen, der begrænser dig i at fremstille en større mængde end den mængde, der vises i feltet **Kan blive topvare**. For eksempel kan flaskehalsvaren være en købt komponent med en forventet modtagelsesdato, der er for sen til, at der kan oprettes supplerende enheder af topvaren efter datoen i feltet **Behovsdato**.

### <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>Sådan vises disponeringen for en vare pr. enhed
Siden **Disponering af vare efter enhed** viser disponeringen af en vare opdelt i de forskellige enheder, den opbevares i.

## <a name="assembly-availability-page"></a>Siden Montagedisponering
Siden **Montagedisponering** indeholder detaljerede disponeringsoplysninger for montageelementet. Vinduet åbnes:

- Automatisk fra en salgsordrelinje i montageordrescenarier, når du angiver et antal, der forårsager et problem med komponentdisponeringen.
- Automatisk fra et montageordrehoved, når du angiver en værdi i feltet Antal, der forårsager et problem med komponentdisponeringen.
- Manuelt, når du åbner den fra en montageordre. Under fanen Handlinger i gruppen Funktion skal du klikke på Vis disponering.

I oversigtspanelet **Detaljer** vises detaljerede disponeringsoplysninger for montageelementet, herunder, hvor mange af montageordreantallet kan monteres ved forfaldsdatoen, der er baseret på tilgængeligheden af de nødvendige komponenter. Dette vises i feltet Mulighed for montage i oversigtspanelet Detaljer.

Værdien i feltet **Mulighed for montage** vises med rød skrift, hvis mængden er lavere end mængden i feltet **Restantal**, hvilket angiver, at der ikke er nok tilgængelige komponenter til at montere hele mængden.

I oversigtspanelet **Linjer** vises detaljerede disponeringsoplysninger for montagekomponenterne.

Hvis en eller flere montagekomponenter ikke er tilgængelig, afspejles dette i feltet **Mulighed for montage** på den pågældende linje som en mindre mængde end mængden i feltet **Restantal** i oversigtspanelet **Detaljer**.

## <a name="see-also"></a>Se også
[Administrere lager](inventory-manage-inventory.md)  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)    
[Opsætte lokationer](inventory-how-setup-locations.md)  
[Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  
[Sælge produkter](sales-how-sell-products.md)      
[Arbejde med Business Central](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)
