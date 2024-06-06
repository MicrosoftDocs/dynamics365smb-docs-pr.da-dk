---
title: Konfigurere og administrere et budget for et projekt
description: 'Beskriver, hvordan du planlægger ressourcer og estimerer og styrer omkostningerne for et projekt ved at oprette et budget for hvert projekt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-budgets"></a>Administrere projektbudgetter

Du kan oprette et budget for hvert projekt. Budgettet bruges til at planlægge de ressourcer, som du kan allokere til et projekt. Budgettet kan enten være generelt med få poster, eller det kan indeholde flere poster, der er inddelt i aktivitetsniveauer. Du kan derefter sammenligne de budgetterede beløb med det faktiske forbrug som registreret i projektkladden. Ved at overvåge forskellene mellem det faktiske forbrug og det budgetterede forbrug kan du kontrollere et igangværende projekt og forbedre kvaliteten af fremtidige projekter ved at reducere risikoen for at undervurdere omkostningerne.

Følgende fremgangsmåde beskriver, hvordan du vurderer budgetterede omkostninger under planlægningen. Du kan finde oplysninger om registrering af budgetterede og faktiske projektpriser og -omkostninger i [Registrere forbrug for projekter](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-project"></a><a name="JobBudgetCosts"></a>Sådan vurderes de budgetterede omkostninger for et projekt

Når en debitor vil have oplyst prisen for et projekt, som faktureres på basis af forbrug, skal du bestemme det budgetterede kostbeløb for projektet. Det gør du på siden **Projektopgavelinjer**.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Åbn et relevant projekt.
3. Vælg en opgavelinje af typen Bogføring, og vælg derefter handlingen **Projektplanlægningslinjer**.
4. Udfyld felterne på en ny linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

For feltet **Linjetype** skal du se følgende oplysninger.  

| Linjetype | Beskrivelse |
| --- | --- |
| **Både budget og fakturerbar** |De kost- og prisbeløb, der er angivet på planlægningslinjen, er de budgetterede kostbeløb for netop denne planlægningslinje. Prisbeløbet vil blive faktureret. |
| **Budget** |Kunden faktureres ikke for forbruget. Forbrug overføres ikke til en faktura, men bruges til at beregne igangværende arbejde. |
| **Fakturerbar** |Kunden faktureres for forbruget. Forbrug overføres til fakturaen baseret på det antal, der er angivet i feltet **Antal til overførsel til faktura**. |

> [!NOTE]  
> Feltet **Planlagt leveringsdato** for planlægningslinjen er den dato, hvor forbrug, der vedrører planlægningslinjen, forventes at fuldføres. Det er også den dato, hvor planlægningslinjen kan overføres til en salgsfaktura og bogføres. <br /><br /> I den underliggende projektopgave på siden **Projektkort** indeholder felterne **Startdato** og **Slutdato** værdien af feltet **Planlagt leveringsdato** på de tidligste og seneste projektplanlægningslinjer på den tilhørende **Projektplanlægningslinjer**-side.

> [!NOTE]  
> Når du udfylder feltet **Antal**, beregnes og udfyldes alle oplysninger om salgsbeløb og kostbeløb for planlægningslinjen. Du kan redigere dem når som helst.

På siden **Projektkort** , kan du nu se en oversigt over de samlede budgetterede omkostninger, budgetteret pris, fakturerbare omkostninger og fakturerbar pris for hver opgave.

Du kan finde oplysninger om registrering af budgetterede og faktiske projektpriser og -omkostninger i [Registrere forbrug for projekter](projects-how-record-job-usage.md).

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
