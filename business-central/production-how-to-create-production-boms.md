---
title: Sådan oprettes produktionsstyklister | Microsoft Docs
description: En produktionsstykliste indeholder masterdata, som beskriver de komponenter og halvfabrikata, som anvendes til fremstilling af en overordnet vare. Så snart der oprettes en produktionsordre for den overordnede vare, bestemmer dens produktionsstykliste beregningen af materialebehov, som repræsenteret på siden **Prod.ordrekomponenter**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 10795ffc60861766f3fcc4aebcb086ab55a0094f
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779931"
---
# <a name="create-production-boms"></a>Oprette produktionsstyklister
En produktionsstykliste indeholder masterdata, som beskriver de komponenter og halvfabrikata, som anvendes til fremstilling af en overordnet vare. Så snart der oprettes en produktionsordre for den overordnede vare, bestemmer dens produktionsstykliste beregningen af materialebehov, som repræsenteret på siden **Prod.ordrekomponenter**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter også montagestyklister. Du kan bruge montageordrer til at oprette slutvarer fra komponenter i en enkel proces, der kan udføres af en eller flere grundlæggende ressourcer, som ikke er produktions- eller arbejdscentre, eller uden nogen ressourcer. En montageproces kunne f.eks. være at plukke to vinflasker og én kaffesæk og pakke dem som en gave. Du kan finde flere oplysninger i [Montagestykliste eller produktionsstyklister](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

Før du kan oprette en rute, skal følgende betingelser være opfyldt:  

- Der er oprettet varekort for overordnede varer, der indgår i produktionen. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).
- Produktionsressourcer er oprettet. Du kan finde flere oplysninger i [Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Sådan oprettes en produktionsstykliste  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsstykliste**, og vælg dernæst det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Du kan redigere styklisten ved at angive feltet **Status** til **Ny** eller **Under udvikling**. Du kan aktivere den ved at angive feltet **Status** til **Certificeret**.  

    Udfyld linjerne i produktionsstyklisten.
5. Vælg, om varen på denne produktionsstyklistelinje er en almindelig vare eller en produktionsstykliste, i feltet **Type**. Hvis varen på linjen er en produktionsstykliste, skal den findes i forvejen som en godkendt produktionsstykliste.  
6.  I feltet **Nummer** skal du søge efter og vælge den pågældende vare eller produktionsstykliste, eller du skal skrive den i feltet.  
7.  Angiv, hvor mange enheder af varen, der indgår i den overordnede vare, f.eks. fire hjul til en bil, i feltet **Antal pr**.  
8.  Angiv en fast procentdel af komponenterne, der går til spilde under produktionen, i feltet **Spildpct**. Når komponenterne er klar til forbrug i en frigivet produktionsordre, lægges denne procentdel til det forventede antal i feltet **Forbrugsantal** i en produktionskladde. Du kan finde flere oplysninger i [Registrere forbrug og afgang](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Denne spildprocent repræsenterer komponenter, der går til spilde under produktionen, når de tages fra lageret, mens spildprocenten på rutelinjer repræsenterer spild i output, før det lægges på lager.  

9.  I feltet **Rutebindingskode** skal du skrive en kode for at knytte komponenten til en bestemt operation. Du kan finde flere oplysninger i [Sådan oprettes rutebindinger](production-how-to-create-routings.md#to-create-routing-links).
10. Du kan kopiere linjer fra en eksisterende produktionsstykliste ved at vælge handlingen **Kopier stykliste** for at vælge eksisterende linjer.  
11.  Godkend produktionsstyklisten.  
12.  Du kan nu knytte den nye produktionsstykliste til kortet for den pågældende overordnede vare. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Hvis du vil genberegne varens standardkostpris fra varekortet, skal du vælge handlingen **Produktion** og derefter vælge handlingen **Beregn standardkostpris**.  

## <a name="to-create-a-new-versions-of-a-production-bom"></a>Sådan oprettes en ny version af en produktionsstykliste
Nye versioner af produktionsstyklister anvendes, når f.eks. en vare erstattes af en anden vare, eller når en kunde bestiller en speciel version af et produkt. Versionsprincippet gør det muligt at administrere flere versioner af en produktionsstykliste. Ruteversionens struktur svarer til rutens struktur. Forskellen ligger i versionernes tidsmæssige gyldighed. Gyldigheden bestemmes af startdatoen.  

Startdatoen angiver starten på en periode, hvor versionen er gyldig. I alle andre sammenhænge er startdatoen et filterkriterium for beregninger og vurderinger. Styklisteversionen er gyldig, til næste version bliver gyldig efter sin startdato.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Produktionsstykliste**, og vælg dernæst det relaterede link.  
2.  Vælg produktionsstyklisten, der skal kopieres, og vælg derefter handlingen **Versioner**.  
3.  Vælg handlingen **Ny**.  
4. Udfyld felterne efter behov.
5. I feltet **Versionskode** skal du angive en entydig identifikation af versionen. Alle kombinationer af tal og bogstaver er tilladt.  

    Den nyoprettede version tildeles automatisk status som **Ny**.
6. Når styklisteversionen er udført, angiver du feltet **Status** til **Certificeret**.  

Gyldigheden i tid for versionen angives i feltet **Startdato**.  

> [!NOTE]  
>  Hvis du vil bruge en vare fra varemasterdata i produktionsstyklisten skal du vælge indstillingen **Vare** i feltet **Type**. Hvis varen også har en produktionsstykliste, hvorved **Produktionsstyklistenr.** er udfyldt på kortet, tages denne produktionsstykliste også i betragtning.  
>   
>  Vælg indstillingen **Produktionsstykliste**, hvis du vil bruge en fantomproduktionsstykliste på linjen.  
>   
>  Fantomstyklister anvendes til at strukturere produkter. Denne produktionsstyklistetype fører aldrig til et færdigt produkt, men anvendes udelukkende til at bestemme afhængige behov. Fantomstyklister har ikke deres egne stamdata for varer.

## <a name="quantity-calculation-formula-on-production-boms"></a>Beregningsformel for mængde på produktionsstyklister  
Mængden beregnes under hensyntagen til forskellige dimensioner, der også er angivet på produktionsstyklistens linjer. Dimensionerne henviser til en ordreenhed for den pågældende vare. Længde, bredde, dybde og vægt kan angives som dimensioner.  

Kolonnerne Beregningsformel, Længde, Bredde, Dybde og Vægt vises ikke, fordi de kun anvendes af nogle brugere. Hvis du vil anvende beregninger af mængden, skal du først have vist disse kolonner.  

De enkelte komponenters relation defineres af beregningsformlen. Du kan vælge mellem følgende beregningsformler:  

-  **Tom** - Der anvendes ikke dimensioner. (Antal = Antal pr.)  
-  **Længde.** - Antal = Antal pr. * længde  
-  **Længde x bredde** - Antal = Antal pr. * længde x bredde  
-  **Længde x bredde x dybde** - Antal = Antal pr. x længde x bredde x dybde  
-  **Vægt** - Antal = Antal pr. x vægt  

### <a name="example"></a>Eksempel  
I en produktionsstykliste skal der anvendes 70 metaldele med dimensionerne længde = 0,20 m og bredde = 0,15 m. Værdierne angives sådan: Beregningsformel = Længde x bredde, længde = 20, bredde = 15, Antal pr. = 70. Antallet er givet af antal pr. x længde * bredde, det vil sige, antal = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Se også  
[Oprette ruter](production-how-to-create-routings.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
