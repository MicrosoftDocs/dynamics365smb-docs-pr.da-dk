---
title: Konfigurere og administrere et budget for en sag
description: 'Beskriver, hvordan du planlægger ressourcer og estimerer og styrer omkostningerne for et projekt ved at oprette et budget for hver sag.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manage-job-budgets"></a>Administrere sagsbudgetter

Du kan oprette et budget for hver sag. Budgettet bruges til at planlægge de ressourcer, som du kan allokere til en sag. Budgettet kan enten være generelt med få poster, eller det kan indeholde flere poster, der er inddelt i aktivitetsniveauer. Du kan derefter sammenligne de budgetterede beløb med det faktiske forbrug som registreret i sagskladden. Ved at overvåge forskellene mellem det faktiske forbrug og det budgetterede forbrug kan du kontrollere et igangværende projekt og forbedre kvaliteten af fremtidige sager ved at reducere risikoen for at undervurdere omkostningerne.

Følgende fremgangsmåde beskriver, hvordan du vurderer budgetterede omkostninger under planlægningen. Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Registrere forbrug for sager](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a>Sådan vurderes de budgetterede omkostninger for en sag
Når en debitor vil have oplyst prisen for en sag, som faktureres på basis af forbrug, skal du bestemme det budgetterede kostbeløb for sagen. Det gør du på siden **Sagsopgavelinjer**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Åbn en relevant sag.
3. Vælg en opgavelinje af typen Bogføring, og vælg derefter handlingen **Sagsplanlægningslinjer**.
4. Udfyld felterne på en ny linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

For feltet **Linjetype** skal du se følgende oplysninger.  

| Linjetype | Beskrivelse |
| --- | --- |
| **Både budget og fakturerbar** |De kost- og prisbeløb, der er angivet på planlægningslinjen, er de budgetterede kostbeløb for netop denne planlægningslinje. Prisbeløbet vil blive faktureret. |
| **Budget** |Kunden faktureres ikke for forbruget. Forbrug overføres ikke til en faktura, men vil stadig blive brugt i VIA-beregningen. |
| **Fakturerbar** |Kunden faktureres for forbruget. Forbrug overføres til fakturaen, baseret på det antal, der er angivet i feltet Antal til overførsel til faktura. |

> [!NOTE]  
> Feltet **Planlagt leveringsdato** for planlægningslinjen er den dato, hvor forbrug, der vedrører planlægningslinjen, forventes at fuldføres. Det er også den dato, hvor planlægningslinjen kan overføres til en salgsfaktura og bogføres. <br /><br /> I den underliggende sagsopgave på siden **Jobkort** indeholder felterne **Startdato** og **Slutdato** værdien af feltet **Planlagt leveringsdato** på de tidligste og seneste sagsplanlægningslinjer på den tilhørende **Sagsplanlægningslinjer**-side.

> [!NOTE]  
>   Når du udfylder feltet **Antal**, beregnes og udfyldes alle oplysninger om salgsbeløb og kostbeløb for planlægningslinjen. Du kan redigere dem når som helst.

På siden **Jobkort** , kan du nu se en oversigt over de samlede budgetterede omkostninger, budgetteret pris, fakturerbare omkostninger og fakturerbar pris for hver opgave.

Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Registrere forbrug for sager](projects-how-record-job-usage.md).

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/set-up-job-planning-lines/)

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
