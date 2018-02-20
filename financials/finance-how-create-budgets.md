---
title: Oprette finansbudgetter | Microsoft Docs
description: Beskriver, hvordan du opretter finansbudgetter for at estimere forskellige finansielle aktiviteter og tildele dimensioner i forbindelse med business intelligence.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="create-gl-budgets"></a>Oprette finansbudgetter
Du kan have flere budgetter for identiske tidsperioder ved at oprette budgetter med separate navne. Ført opretter du budgetnavnene og angiver budgettal. Derefter medtages budgetnavnene på alle de budgetposter, du opretter.  

 Når du opretter et budget, kan du definere fire dimensioner for hvert budget. Disse budgetspecifikke dimensioner kaldes budgetdimensioner. Du kan vælge budgetdimensioner fra hvert budget blandt de dimensioner, du allerede har oprettet. Budgetdimensioner kan bruges til at angive filtre for et budget og til at tilføje dimensionsoplysninger til budgetposter. Du kan finde flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

 Budgetter spiller en vigtig rolle i business intelligence, f.eks. i finansregnskab, der er baseret på kontoplaner, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen. Du kan finde flere oplysninger i [Business Intelligence](bi.md).

 Budgetter spiller en vigtig rolle i business intelligence, f.eks. i finansregnskab, der er baseret på kontoplaner, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen. Du kan finde flere oplysninger i [Business Intelligence](bi.md).

I Omkostningsberegning arbejder du med omkostningsbudgetter på samme måde. Du kan finde flere oplysninger i [Oprette omkostningsbudgetter](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Sådan oprettes et nyt finansbudget  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansbudgetter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Rediger liste**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Rediger budget**.
4. Øverst i vinduet **Budget** skal du udfylde felterne efter behov for at definere, hvad der vises.  

    Kun de poster, der indeholder det budgetnavn, du har angivet i feltet **Budgetnavn** vises. Fordi budgetnavnet lige er oprettet, er der ikke nogen poster, der passer til filtret. Vinduet er derfor tomt.  
5. Angiv et beløb ved at vælge den relevante celle i matrixen. Vinduet **Finansbudgetposter** åbnes.  
6. Opret en ny linje, og udfyld feltet **Beløb**. Luk vinduet **Finansbudgetposter**.  
7. Gentag trin 5 og 6, indtil du har indtastet alle budgetbeløbene.  

> [!NOTE]  
>  I oversigtspanelet **Filtre** kan du filtrere budgetoplysningerne efter de budgetdimensioner, du har oprettet under budgetnavnet.   

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Business Intelligence](bi.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

