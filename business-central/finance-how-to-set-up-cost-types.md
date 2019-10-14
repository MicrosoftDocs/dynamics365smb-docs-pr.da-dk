---
title: Sådan konfigureres et diagram over omkostningstyper | Microsoft Docs
description: Diagrammet over omkostningstyper ligner kontoplanen i regnskabet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: d9a2c6efcee13564edbe9b108c831a1e9fbb7d93
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301957"
---
# <a name="set-up-cost-types"></a>Oprette omkostningstyper
Diagrammet over omkostningstyper ligner kontoplanen i finansregnskabet. Du kan angive diagrammet over omkostningstyper på følgende måder:  

-   Strukturen af diagrammet over omkostningstyper ligner resultatopgørelseskontiene i finanskontoplanen. Herefter kan du overføre finanskontoplanen til diagrammet over omkostningstyper. Du kan foretage de nødvendige justeringer efter overførslen.  
-   Opret et nyt diagram over omkostningstyper, eller tilføj nye omkostningstyper til det eksisterende diagram over omkostningstyper. Du skal oprette hver ny omkostningstype individuelt.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Sådan overføres finanskontoplanen til diagrammet over omkostningstyper  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningstyper**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent omkostningstyper fra kontoplan**. I dialogboksen skal du trykke på knappen **Ja** for at bekræfte overførslen. Funktionen bruger kontoplanen til at oprette et diagram over omkostningstyper  

    Diagrammet over omkostningstyper indeholder nu alle resultatopgørelseskonti i regnskabet og omfatter overskrifter og subtotaler. Du kan ændre diagrammet over omkostningstyper, hvis det er nødvendigt. For eksempel kan du slette dobbelte omkostningstyper.  

    > [!IMPORTANT]  
    >  Funktionen **Registrer omkostningstyper i kontoplanen** opdaterer forholdet mellem kontoplanen og diagrammet over omkostningstyper. Feltet **Nummer** feltet udfyldes og bekræftes for at sikre, at hver finanskonto kun er relateret til én kostpristype. Funktionen kører automatisk, før den overfører finansposter til omkostningsregnskabet.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Sådan oprettes nye omkostningstyper på siden Omkostningstyper  
1.  Åbn siden **Omkostningstyper** i redigeringstilstand.  
2.  Udfyld felterne som beskrevet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan oprette og vedligeholde omkostningstyper enten på siden **Omkostningstypekort** eller på siden **Omkostningstyper**. I denne procedure opretter du omkostningstyper på siden **Omkostningstyper**.

3.  Når du har oprettet alle omkostningstyper, skal du vælge handlingen **Indryk omkostningstyper**. I dialogboksen skal du trykke på knappen **Ja**.  
4.  Sammenkæd den nye pristype til den tilsvarende finanskonto.  

    > [!IMPORTANT]  
    >  Hvis du har angivet definitioner i felterne **Sammentælling** for linjetypen **Til-sum**, før du kører funktionen **Indryk omkostningstyper**, skal du angive definitionerne igen, fordi funktionen overskriver værdierne i alle felter af typen **Til-sum**.  

## <a name="to-update-cost-types"></a>Sådan opdateres omkostningstyper  
1.  På siden **Konfiguration af omkostningsregnskab** skal du vælge, om du ønsker, at omkostningstypeplanen automatisk opdateres, når kontoplanen ændres.  
2.  Du kan vælge mellem følgende indstillinger i feltet **Opdater finanskonto**.  

- **Ingen justering** der er ingen tilsvarende ændring i diagrammet over omkostningstyper, når du ændrer kontoplanen.  
- **Automatisk** - en tilsvarende ændring foretages i diagrammet over omkostningstyper, når du ændrer kontoplanen.  
- **Spørg** - der vises en meddelelse, hvor du bliver spurgt, om du vil foretage en tilsvarende ændring i diagrammet typer omkostninger, når du ændrer kontoplanen.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Definition af omkostningssteder og omkostningsobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldi mellem omkostningstype, omkostningssted og omkostningsobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
[Om omkostningsregnskab](finance-about-cost-accounting.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
