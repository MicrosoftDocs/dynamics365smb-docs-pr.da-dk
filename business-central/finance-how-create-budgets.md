---
title: Oprette finansbudgetter
description: 'Beskriver, hvordan du opretter finansbudgetter for at estimere forskellige finansielle aktiviteter og tildele dimensioner i forbindelse med business intelligence.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="create-gl-budgets"></a>Oprette finansbudgetter

Du kan have flere budgetter for identiske tidsperioder ved at oprette budgetter med separate navne. Ført opretter du budgetnavnene og angiver budgettal. Derefter medtages budgetnavnene på alle de budgetposter, du opretter.  

Når du opretter et budget, kan du definere budgetspecifikke dimensioner, kaldet budgetdimensioner, for det. Du kan bruge budgetdimensioner til at angive filtre for et budget og til at tilføje dimensionsoplysninger til budgetposter. Flere oplysninger i [Arbejde med dimensioner](finance-dimensions.md).

Budgetter spiller en vigtig rolle i Business Intelligence. F.eks. i finansregnskab, der er baseret på finansrapporter, der indeholder budgetposter, eller når du analyserer budgetterede vs. faktiske beløb i kontoplanen. Få mere at vide om [Business Intelligence](bi.md).

I Omkostningsberegning arbejder du med omkostningsbudgetter på samme måde. Flere oplysninger i [Oprette omkostningsbudgetter](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Sådan oprettes et nyt finansbudget

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finansbudgetter** og vælg derefter det relaterede link.  
2. Vælg handlingen **Rediger liste**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Rediger budget**.
4. Øverst på siden **Budget** skal du udfylde felterne efter behov for at definere, hvad der vises.  

   Denne side viser kun de poster, der indeholder det budgetnavn, du har angivet i feltet **Budgetnavn**. Fordi budgetnavnet lige er oprettet, er der ikke nogen poster, der passer til filtret. Siden er derfor tom.  
5. Angiv et beløb ved at vælge den relevante celle i matrixen. Siden **Finansbudgetposter** åbnes.  
6. Opret en ny linje, og udfyld feltet **Beløb**. Luk siden **Finansbudgetposter**.  
7. Gentag trin 5 og 6 for alle beløb i budgettet.  

> [!NOTE]  
> I oversigtspanelet **Filtre** kan du filtrere budgetoplysningerne efter de budgetdimensioner, du har oprettet under budgetnavnet.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Eksportere og importere finansbudgetter med Excel

Som for praktisk talt alle andre sider kan du eksportere data på budgetsider til Microsoft Excel til yderligere behandling eller analyse. Flere oplysninger i [Eksportere dine forretningsdata til Excel](about-export-data.md).

> [!NOTE]
> Kontoplanen, som finansbudgetterne er baseret på, indeholder linjer af kontotypen Overskrift. Disse linjer indeholder summen af linjerne under den. Når du eksporterer et finansbudget, eksportere du data på alle linjer uanset kontotypen. Du kan dog kun indlæse data på linjer med kontotypen Bogføring.

Tilsvarende du indlæser et finansbudget, slettes eventuelle værdier derfor på overskriftslinjer. De slettes for at undgå forkerte totaler, når du har importeret data, der er oprettet eller redigeret i Excel.

### <a name="scenario"></a>Scenarie

Du ved, at de nye budgetterede lønomkostninger vil være 1.200.000 i den lokale valuta. Du vil tillade lønafdelingens budget for de tre specifikke linjer (af kontotypen Bogføring) for fuldtidsmedarbejdere, deltidsmedarbejdere og midlertidig hjælp. De tre linjer er grupperet under overskriftslinjen Løn.

Du indtaster 1.200.000 på overskriftslinjen, eksporterer budgettet til Excel og sender det derefter til lønafdelingen og beder dem om at fordele 1.200.000.

Lønafdelingen fordeler beløbet på de tre bogføringskonti. Når du importerer tilbage i finansbudgettet, udfyldes de tre konti med de nye Excel-data, der tilsammen giver RV 1.200.000, og overskriftslinjen er tom.

## <a name="see-also"></a>Se også

[Eksportere dine forretningsdata til Excel](about-export-data.md)  
[Finans](finance.md)  
[Business Intelligence](bi.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
