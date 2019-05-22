---
title: Sådan monterer du varer | Microsoft Docs
description: Hvis feltet **Genbestillingssystem** på varekortet indeholder **Montage**, er standardmetoden til at levere varen at montere den fra definerede komponenter og potentielt af en ressource, der er defineret.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 55d0ed4110796fa9f037e066d56be9efdd6649a4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247348"
---
# <a name="assemble-items"></a>Montere elementer
Hvis feltet **Genbestillingssystem** på varekortet indeholder **Montage**, er standardmetoden til at levere varen at montere den fra definerede komponenter og potentielt af en ressource, der er defineret.  

Komponenter og ressourcer, der indgår i denne form for montageelement, skal være defineret i en montage stykliste. Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).  

Montageelementer kan angives for to forskellige montageprocesser:  

-   Montage til lager.  
-   Montage efter ordre.  

Du bruger typisk **Montage til lager** for de varer, du vil montere forud for salg, f.eks for at forberede en pakkekampagne og beholde på lager, indtil de bestilles. Disse varer er som regel standardvarer som emballerede pakker, du ikke tilbyder at tilpasse efter kundens behov.  

Du bruger typisk **Montage efter ordre** for varer, som du ikke ønsker på lager, fordi du forventer at tilpasse dem til debitoranmodninger, eller fordi du vil minimere de generelle lageromkostninger ved at levere dem på det rigtige tidspunkt. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Du kan finde flere oplysninger om opsætning af et montageelement i [Om montage til ordre eller montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

Disse opsætningsindstillinger er standardindstillinger, der styrer, hvordan salgs- og montageordrelinjer behandles indledningsvis. Du kan fravige disse standarder og levere montageelementet på den mest optimale måde under behandlingen af et salg. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) og [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Montagekomponenter håndteres på en særlig måde i grundlæggende lageropsætninger. Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).   

I denne procedure skal du oprette og behandle en montageordre for montage til lager-varer, hvilket betyder uden en sammenkædet salgsordre. Fremgangsmåden omfatter start af montageordren, håndtering af potentielle problemer med komponenttilgængeligheden og delvis bogføring af afgang for montageelement.

## <a name="to-assemble-an-item"></a>Sådan monteres et element  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Montageordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**. Siden **Ny montageordre** åbnes.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Vælg det montageelement, som skal behandles, i feltet **Varenr.**. Feltet er filtreret, så det kun viser elementer, der er konfigureret for montage, hvilket betyder, at de har tildelte montagestyklister.  
5.  I feltet **Antal** skal du angive, hvor mange enheder af varen, der skal monteres.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter ikke er tilgængelige for at opfylde det angivne montageelement på den definerede forfaldsdato, åbnes siden **Montagedisponering** automatisk med detaljerede oplysninger om, hvor mange montageelementer der kan monteres baseret på komponenttilgængeligheden. Du kan finde flere oplysninger i [Vise tilgængeligheden af varer](inventory-how-availability-overview.md). Når du lukker siden, oprettes montageordren med beskeder om tilgængelighed på de berørte komponentlinjer.  

    Montageordrelinjerne udfyldes automatisk med indholdet af montagestyklisten og linjemængder i henhold til montageordrehovedet.  

    > [!NOTE]  
    >  Hvis siden **Montagedisponering** åbnes, når du har udfyldt montageordrehovedet, indeholder hver berørt montageordrelinje et **Ja** i feltet **Disponeringsadvarsel** med et link til yderligere disponeringsoplysninger. Du kan finde flere oplysninger i Check varebeholdning Du kan løse et problem med komponenttilgængelighed ved at udsætte startdatoen, erstatte komponenten med en anden vare eller vælge en tilgængelig erstatningsvare, hvis der er defineret en.  

6.  I feltet **Antal til montage** skal du angive, hvor mange enheder af montageelementet, du vil bogføre som afgang, næste gang du bogfører montageordren. Dette antal kan være lavere end værdien i feltet **Antal** som afspejling af en delvis afgangsbogføring.  

    > [!NOTE]  
    >  For at sikre, at bogføringen af komponentforbruget svarer til bogføringen af montageelementafgangen, reguleres antalsfelterne i montageordrelinjerne automatisk til den værdi, du angiver i feltet **Antal til montage**.  
7.  På montageordrelinjer af typen **Vare** eller **Ressource** skal du i feltet **Antal til forbrug** angive, hvor mange enheder du vil bogføre som forbrugte, næste gang du bogfører montageordren.
8.  Når du er klar til at bogføre helt eller delvist, kan du vælge handlingen **Bogfør**.  

    > [!NOTE]  
    >  Hvis der stadig findes advarsler i nogen af montageordrelinjerne, blokeres bogføringen. Der vises en meddelelse om, hvilke komponenter der ikke er på lager.  

Når bogføringen er udført, bogføres montageelementet som afgang til den lokationskode og potentielle placeringskode, der er defineret på montageordren. For manuelt oprettede montageordrer kopieres placeringen evt. fra opsætningsfeltet **Standardlokation for ordrer**. Ved montage efter ordre-forløb kopieres lokationskoden evt. fra salgsordrelinjen.  

## <a name="see-also"></a>Se også
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
