---
title: Sælge varer, der er monteret til ordre
description: Hvis varen er konfigureret til montage til ordre, forventes varen derefter ikke at være på lager, og den skal samles specifikt til en salgsordre.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting, substitute items
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 07/29/2021
ms.author: edupont
ms.openlocfilehash: ab94626b300a1f022b95770fe8e83fd8d80c9885
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381508"
---
# <a name="sell-items-assembled-to-order"></a>Sælge varer, der er monteret til ordre
Hvis feltet **Montagepolitik** på varekortet til et montageelement er **Montage efter ordre**, kan varen ikke forventes at være på lager og skal samles specifikt til en salgsordre. Når du indtaster varen på en salgsordrelinje, bliver der automatisk oprettet en montageordre, hvorefter den knyttes til salgsordren.  

> [!NOTE]  
>  Hvis nogle montage efter ordre-elementer allerede findes i lageret, kan de fratrække mængden fra montageordre og reservere den fra lageret. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I denne procedure behandler du salg af et element, der skal samles i henhold til specifikationer, der er anmodet af debitor. Fremgangsmåden omfatter start af salgsordrelinje, tilpasning af montageelement ved at redigere dens komponenter og ressourcer, kontrol af tilgængelighed til at fastsætte en leveringsdato og frigive salgsordre skal samles og leveres med det samme.  

> [!NOTE]  
>  Følgende procedure omfatter ikke standardsalgsordretrin før det trin, hvor du indtaster montage efter ordre-elementer på en salgsordrelinje.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Sådan sælger du en vare, der er samlet til ordre  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Oprette en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  
3.  I feltet **Nummer** skal du angive en vare, der er indstillet til at samles til ordre.  
4.  I feltet **Lokationskode** skal du definere, hvilken lokation varen sælges fra. Montageprocessen vil forekomme på denne placering.  
5.  I feltet **Antal** skal du angive, hvor mange enheder, der skal sælges.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter af antallet af anmodede montageelementer ikke er tilgængelige, åbnes en side med en detaljeret tilgængelighedsadvarsel. Du kan finde flere oplysninger i Montagedisponering  

    Der oprettes nu ikke automatisk en montageordre med tilknytning til salgsordrelinjen. Forfaldsdato for denne montageordre er synkroniseret med afsendelsesdato for salgsordrelinjen.  

    Antal, der skal sælges, kopieres til feltet **Antal til montage efter ordre**, som angiver, at vareopsætningen forventer, at hele mængden på salgslinjen skal samles til ordren. Du kan reducere antallet til montage efter ordre, hvis du f.eks ved, at nogle elementer allerede er tilgængelige. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  For at vise, at debitor ønsker yderligere et element i en pakke, skal du på oversigtspanelet **Linjer** vælge handlingen **Linje**, vælge handlingen **Montage til ordre** og derefter vælge handlingen **Montage til ordre-linjer** for at få vist og ændret standardmontagekomponenterne. Du kan også vælge feltet **Antal til montage efter ordre**.  
7.  På siden **Montage efter ordre-linjer** oprettes en ny linje af typen **Element** for det ønskede ekstra pakkeindhold. Linjen repræsenterer en ekstra montagekomponent.  

    Du kan også tilpasse rækkefølgen ved at øge antallet af ét standardelement i pakken. Du kan gøre dette ved at forøge værdien i feltet **Mængde pr.** på den pågældende montageordrelinje.  

    > [!NOTE]  
    >  Siden **Montage efter ordre-linjer** indeholder kun de vigtigste felter, som en sælger forventes at bruge til at tilpasse komponentoversigten, tilføje varesporingsnumre eller løse problemer med komponentdisponibilitet. Hvis du vil have vist flere montageordreoplysninger, f.eks. montageordrens startdato, skal du vælge handlingen **Vis dokumenter**. Dette åbner en komplet visning af den montageordre, der er tilknyttet salgsordrelinjen. Du kan ikke ændre indholdet af de fleste felter i montageordrehovedet, og du kan ikke bogføre montageafgange, fordi du skal benytte leverancebogføringen fra salgsordrelinjen.  
    >   
    >  På sidehovedet i sammenkædede montageordrer, er det kun feltet **Startdato**, der kan ændres for at få montagearbejdere til at angive en dato, der ligger før forfaldsdato, når de starter processen. Alle felter på linjerne i den tilknyttede montageordre kan ændres, så lagermedarbejdere kan indtaste tallene for forbrug under processen.  

8.  Gennemse eller reager på problemer med tilgængeligheden af komponenter. Vælg f.eks. en tilgængelig erstatningsvare, eller fastsæt en senere forfaldsdato.  
9. Luk siden **Montage efter ordre-linjer**. Den tilknyttede montageordre er nu klar til at begynde samling af de tilpassede elementer efter forfaldsdato.  
10. På salgsordren skal du vælge handlingen **Frigiv** for at advisere montageafdelingen om, at montageprocessen kan startes.  
11. I samleafdelingen, skal du udføre trinnene med samling af de elementer, der sælges i denne procedure. Du kan finde flere oplysninger i [Montere varer](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Vær opmærksom på, at erstatningsvarer ikke automatisk medfører, at en vare erstattes af en anden vare, f. eks. når der oprettes en salgsordre eller en stykliste. I stedet bliver du advaret om, at der er en erstatningsvare tilgængelig.

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Warehouse Management](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Registrere nye varer](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]