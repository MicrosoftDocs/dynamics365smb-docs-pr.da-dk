---
title: "Sådan sælger du en vare, der er monteret til ordre | Microsoft Docs"
description: "Hvis varen er konfigureret til montage til ordre, forventes varen derefter ikke at være på lager, og den skal samles specifikt til en salgsordre. Når du indtaster varen på en salgsordrelinje, bliver der automatisk oprettet en montageordre, hvorefter den knyttes til salgsordren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b03cc5a21ca49f85fa859736b074bd72cb5c6499
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="sell-items-assembled-to-order"></a>Sælge varer, der er monteret til ordre
Hvis feltet **Montagepolitik** på varekortet til et montageelement er **Montage efter ordre**, kan varen ikke forventes at være på lager og skal samles specifikt til en salgsordre. Når du indtaster varen på en salgsordrelinje, bliver der automatisk oprettet en montageordre, hvorefter den knyttes til salgsordren.  

> [!NOTE]  
>  Hvis nogle montage efter ordre-elementer allerede findes i lageret, kan de fratrække mængden fra montageordre og reservere den fra lageret. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I denne procedure behandler du salg af et element, der skal samles i henhold til specifikationer, der er anmodet af debitor. Fremgangsmåden omfatter start af salgsordrelinje, tilpasning af montageelement ved at redigere dens komponenter og ressourcer, kontrol af tilgængelighed til at fastsætte en leveringsdato og frigive salgsordre skal samles og leveres med det samme.  

> [!NOTE]  
>  Følgende procedure omfatter ikke standardsalgsordretrin før det trin, hvor du indtaster montage efter ordre-elementer på en salgsordrelinje.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Sådan sælger du en vare, der er samlet til ordre  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Oprette en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  
3.  I feltet **Nummer** skal du angive en vare, der er indstillet til at samles til ordre.  
4.  I feltet **Lokationskode** skal du definere, hvilken lokation varen sælges fra. Montageprocessen vil forekomme på denne placering.  
5.  I feltet **Antal** skal du angive, hvor mange enheder, der skal sælges.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter af antallet af anmodede montageelementer ikke er tilgængelige, åbnes et vindue med en detaljeret tilgængelighedsadvarsel. Du kan finde flere oplysninger i Montagedisponering  

    Der oprettes nu ikke automatisk en montageordre med tilknytning til salgsordrelinjen. Forfaldsdato for denne montageordre er synkroniseret med afsendelsesdato for salgsordrelinjen.  

    Antal, der skal sælges, kopieres til feltet **Antal til montage efter ordre**, som angiver, at vareopsætningen forventer, at hele mængden på salgslinjen skal samles til ordren. Du kan reducere antallet til montage efter ordre, hvis du f.eks ved, at nogle elementer allerede er tilgængelige. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  For at vise, at debitor ønsker yderligere et element i en pakke, skal du på oversigtspanelet **Linjer** vælge handlingen **Linje**, vælge handlingen **Montage til ordre** og derefter vælge handlingen **Montage til ordre-linjer** for at få vist og ændret standardmontagekomponenterne. Du kan også vælge feltet **Antal til montage efter ordre**.  
7.  I vinduet **Montage efter ordre-linjer** oprettes en ny linje af typen **Element** for det ønskede ekstra pakkeindhold. Linjen repræsenterer en ekstra montagekomponent.  

    Du kan også tilpasse rækkefølgen ved at øge antallet af ét standardelement i pakken. Du kan gøre dette ved at forøge værdien i feltet **Mængde pr.** på den pågældende montageordrelinje.  

    > [!NOTE]  
    >  Vinduet **Montage efter ordre-linjer** indeholder kun de vigtigste felter, som en sælger forventes at bruge til at tilpasse komponentoversigten, tilføje varesporingsnumre eller løse problemer med komponentdisponibilitet. Hvis du vil have vist flere montageordreoplysninger, f.eks. montageordrens startdato, skal du vælge handlingen **Vis dokumenter**. Dette åbner en komplet visning af den montageordre, der er tilknyttet salgsordrelinjen. Du kan ikke ændre indholdet af de fleste felter i montageordrehovedet, og du kan ikke bogføre montageafgange, fordi du skal benytte leverancebogføringen fra salgsordrelinjen.  
    >   
    >  På sidehovedet i sammenkædede montageordrer, er det kun feltet **Startdato**, der kan ændres for at få montagearbejdere til at angive en dato, der ligger før forfaldsdato, når de starter processen. Alle felter på linjerne i den tilknyttede montageordre kan ændres, så lagermedarbejdere kan indtaste tallene for forbrug under processen.  

8.  Gennemse eller reager på problemer med tilgængeligheden af komponenter. Vælg f.eks. en tilgængelig erstatningsvare, eller fastsæt en senere forfaldsdato.  
9. Luk vinduet **Montage efter ordre-linjer**. Den tilknyttede montageordre er nu klar til at begynde samling af de tilpassede elementer efter forfaldsdato.  
10. På salgsordren skal du vælge handlingen **Frigiv** for at advisere montageafdelingen om, at montageprocessen kan startes.  
11. I samleafdelingen, skal du udføre trinnene med samling af de elementer, der sælges i denne procedure. Du kan finde flere oplysninger i [Montere varer](assembly-how-to-assemble-items.md).  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

