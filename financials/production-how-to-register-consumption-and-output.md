---
title: "Sådan registreres forbrug og afgang for én produktionsordre | Microsoft Docs"
description: "Denne udførelsesopgave udføres fra vinduet **Produktionskladde**. Kladden kombinerer funktionaliteten ved forbrugskladden og afgangskladden til én kladde. Der er direkte adgang til den kombinerede kladde fra en frigivet produktionsordre. Dens vigtigste formål er manuelt at bogføre forbruget af komponenter, antallet af producerede færdige varer og den tid, der bruges på operationerne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a60e63e9741f81aa6efcf8b6a4780b5b464fe440
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-register-consumption-and-output-for-one-released-production-order-line"></a>Fremgangsmåde: Registrere forbrug og afgang for én frigivet produktionsordrelinje
Denne udførelsesopgave udføres fra vinduet **Produktionskladde**. Kladden kombinerer funktionaliteten ved forbrugskladden og afgangskladden til én kladde. Der er direkte adgang til den kombinerede kladde fra en frigivet produktionsordre. Dens vigtigste formål er manuelt at bogføre forbruget af komponenter, antallet af producerede færdige varer og den tid, der bruges på operationerne. Værdierne bogføres til poster under den frigivne produktionsordre. Forbrugsantallene bogføres som negative vareposter, afgangsantal bogføres som positive poster, og den forbrugte tid bogføres som kapacitetsposter. Disse bogførte værdier vises også nederst i kladden som faktiske mængder.  

> [!NOTE]  
>  Eftersom forbrugsdata behandles sammen med afgangsdata, kan kladden benyttes til at vise bundne komponenter og operationer i en logisk processtruktur. Komponenter er indrykket under deres tilhørende operation. Dette kræver, at du bruger rutebindingskoder.  

> [!NOTE]  
>  Komponenter uden rutebindingskoder angives først i kladden.  

## <a name="to-register-consumption-and-output"></a>Sådan registreres forbrug og afgang  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Frigivne prod.ordrer**, og vælg derefter det relaterede link.  
2.  Åbn den frigivne produktionsordrelinje, der er klar til registrering. I oversigtspanelet **Linjer** skal du derefter vælge handlingen **Linje** og derefter handlingen **Produktionskladde**.  

    Vinduet **Produktionskladde** åbnes med kladdelinjer for produktionsordrelinjen i henhold til vinduerne **Produktionsordrekomponent** og **Prod.ordrerute**. Disse linjer, der stammer fra den produktionsstykliste og rute, der er tildelt den vare, der produceres. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette produktionsstyklister](production-how-to-create-routings.md).  

3.  I feltet **Bogføringsdato** øverst i kladden kan du angive en bogføringsdato, der gælder for alle linjer. Arbejdsdatoen angives som standard. Feltet er beregnet til at gøre det muligt hurtigt at justere bogføringsdatoer på alle linjer, hvis det er relevant.  

    > [!NOTE]  
    >  Bogføringsdatoer, der angives på enkelte linjer, tilsidesætter feltet.  

4.  I filtreringsfeltet **Trækmetode** øverst i kladden kan du vælge også at få vist forbrug og afgang, der bogføres automatisk i overensstemmelse med de trækmetoder, der er defineret for henholdsvis varen og ressourcen.  

    Det er kun de relevante felter, der vises på hver type linje i kladden. Resten er tomme og skrivebeskyttede.  

    Når kladden åbnes, er den udfyldt med de antal, der skal bogføres. Hvis der endnu ikke er bogført noget, indeholder antalfelterne som standard de forventede antal, som er overført fra produktionsordren. Hvis der er udført delvise bogføringer, viser antalfelterne de resterende antal. Allerede bogførte antal og tider for ordren vises nederst i kladden som faktiske indgange.  

    For antallene i feltet **Afgangsantal** har du mulighed for at angive, hvilke værdier der skal vises, første gang kladden åbnes. Det gør du i feltet **Forudindstillet afgangsantal** i oversigtspanelet **Generelt** i vinduet **Produktionsopsætning**. 

5.  Fortsæt med at angive de relevante forbrugs- og afgangsmængder i de felter, der kan redigeres.  

    > [!NOTE]  
    >  Det er kun afgangsantallet på den sidste kladdelinje af posttypen **Afgang**, der regulerer lagerniveauet, når du bogfører kladden. Derfor skal du ikke bogføre kladden med det forventede afgangsantal forudindstillet på den sidste afgangslinje, før alle varerne faktisk er produceret.  

6.  Vælg feltet **Færdig** for afgangslinjerne, hvis du vil angive, at operationen er færdig. Feltet "kommunikerer" med feltet **Rutestatus** på en rutelinje i en produktionsordre.  
7.  Vælg handlingen **Bogfør** for at registrere de antal, du har angivet, og derefter lukke kladden.  

Hvis værdier skal bogføres, indeholder kladden disse resterende værdier næste gang den åbnes. Bogførte værdier vises som faktiske værdier nederst i kladden.  

> [!NOTE]  
>   Hvis en vare, der forbruges, er blokeret, bogfører kladden ikke forbrugsantal for denne vare. Hvis en maskine eller et arbejdscenter er blokeret, bogfører kladden ikke afgangsantal eller procestider for den pågældende afgangslinje.  

> [!NOTE]  
>  Hvis du lukker kladden uden at bogføre, går ændringerne tabt.  

> [!WARNING]  
>  Vinduet **Produktionskladde** kan ikke bruges af to brugere på én gang. Det betyder, at hvis Bruger 2 åbner vinduet og indtaster data, når Bruger 1 allerede arbejder i vinduet, kan Bruger 2 miste data, når Bruger 1 lukker vinduet.  

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

