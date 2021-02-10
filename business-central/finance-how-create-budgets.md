---
title: Oprette finansbudgetter | Microsoft Docs
description: Beskriver, hvordan du opretter finansbudgetter for at estimere forskellige finansielle aktiviteter og tildele dimensioner i forbindelse med business intelligence.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6018edd9d7d324c827c6c338ec700492b39bf56d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747012"
---
# <a name="create-gl-budgets"></a>Oprette finansbudgetter
Du kan have flere budgetter for identiske tidsperioder ved at oprette budgetter med separate navne. Ført opretter du budgetnavnene og angiver budgettal. Derefter medtages budgetnavnene på alle de budgetposter, du opretter.  

Når du opretter et budget, kan du definere fire dimensioner for hvert budget. Disse budgetspecifikke dimensioner kaldes budgetdimensioner. Du kan vælge budgetdimensioner fra hvert budget blandt de dimensioner, du allerede har oprettet. Budgetdimensioner kan bruges til at angive filtre for et budget og til at tilføje dimensionsoplysninger til budgetposter. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Budgetter spiller en vigtig rolle i business intelligence, f.eks. i finansregnskab, der er baseret på kontoplaner, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen. Du kan finde flere oplysninger i [Business Intelligence](bi.md).

I Omkostningsberegning arbejder du med omkostningsbudgetter på samme måde. Du kan finde flere oplysninger i [Oprette omkostningsbudgetter](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Sådan oprettes et nyt finansbudget  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Finansbudgetter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Rediger liste**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Rediger budget**.
4. Øverst på siden **Budget** skal du udfylde felterne efter behov for at definere, hvad der vises.  

    Kun de poster, der indeholder det budgetnavn, du har angivet i feltet **Budgetnavn** vises. Fordi budgetnavnet lige er oprettet, er der ikke nogen poster, der passer til filtret. Siden er derfor tom.  
5. Angiv et beløb ved at vælge den relevante celle i matrixen. Siden **Finansbudgetposter** åbnes.  
6. Opret en ny linje, og udfyld feltet **Beløb**. Luk siden **Finansbudgetposter**.  
7. Gentag trin 5 og 6, indtil du har indtastet alle budgetbeløbene.  

> [!NOTE]  
>  I oversigtspanelet **Filtre** kan du filtrere budgetoplysningerne efter de budgetdimensioner, du har oprettet under budgetnavnet.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Eksportere og importere finansbudgetter med Excel
Som for praktisk talt alle andre sider kan du eksportere data på budgetsider til Excel til yderligere behandling eller analyse. Du kan finde flere oplysninger under [Eksportere forretningsdata til Excel](about-export-data.md).

> [!NOTE]
> Den kontoplanen, som finansbudgetter er baseret på, har linjer kontotypen Overskrift, der indeholder summen af linjerne nedenunder. Når du eksporterer et finansbudget, eksporteres data på alle linjer uanset kontotypen. Det er dog kun data på linjer med kontotypen Bogføring, der kan importeres tilbage. Tilsvarende: <br /><br /> **Når du importerer et finansbudget, slettes alle de værdier, der findes på overskriftslinjer.** <br /><br /> Dette sker for at undgå forkerte totaler efter import af data, der er oprettet eller redigeret i Excel.<br /><br /> **Scenarie**: Du ved, at de nye budgetterede lønomkostninger vil være RV 1.200.000. Du vil tillade lønafdelingens budget for de tre specifikke linjer (af kontotypen Bogføring) for fuldtidsmedarbejdere, deltidsmedarbejdere og midlertidig hjælp. De tre linjer er grupperet under overskriftslinjen Løn.<br /><br />Du indtaster 1.200.000 i overskriftslinjen, eksporterer budgettet til Excel og sender det derefter til lønafdelingen og beder dem om at fordele RV 1.200.000.<br /><br /> Lønafdelingen fordeler beløbet på de tre bogføringskonti. Når du importerer tilbage i finansbudgettet, udfyldes de tre konti med de nye Excel-data, der tilsammen giver RV 1.200.000, og overskriftslinjen er tom.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Eksportere forretningsdata til Excel](about-export-data.md)  
[Finans](finance.md)  
[Business Intelligence](bi.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
