---
title: Konfigurere og administrere et budget for en sag | Microsoft Docs
description: "Beskriver, hvordan du planlægger ressourcer og estimerer og styrer omkostningerne for et projekt ved at oprette et budget for hver sag."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0e480c67ddb2acd5e98799c98cb1cd9d972889df
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-job-budgets"></a>Fremgangsmåde: Administrere sagsbudgetter
Du kan oprette et budget for hver sag. Budgettet bruges til at planlægge de ressourcer, som du kan allokere til en sag. Budgettet kan enten være generelt med få poster, eller det kan indeholde flere poster, der er inddelt i aktivitetsniveauer. Du kan derefter sammenligne de budgetterede beløb med det faktiske forbrug som registreret i sagskladden. Ved at overvåge forskellene mellem det faktiske forbrug og det budgetterede forbrug kan du kontrollere et igangværende projekt og forbedre kvaliteten af fremtidige sager ved at reducere risikoen for at undervurdere omkostningerne.

Følgende fremgangsmåde beskriver, hvordan du vurderer budgetterede omkostninger under planlægningen. Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Sådan gør du: Registrere forbrug for sager](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Sådan vurderes de budgetterede omkostninger for en sag
Når en debitor vil have oplyst prisen for en sag, som faktureres på basis af forbrug, skal du bestemme det budgetterede kostbeløb for sagen. Det gør du i vinduet **Sagsopgavelinjer**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Åbn en relevant sag.
3. Vælg en opgavelinje af typen Bogføring, og vælg derefter handlingen **Sagsplanlægningslinjer**.
4. Udfyld felterne på en ny linje efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

For feltet **Linjetype** skal du se følgende oplysninger.  

| Linjetype | Beskrivelse |
| --- | --- |
| **Både budget og fakturerbar** |De kost- og prisbeløb, der er angivet på planlægningslinjen, er de budgetterede kostbeløb for netop denne planlægningslinje. Prisbeløbet vil blive faktureret. |
| **Budget** |Kunden faktureres ikke for forbruget. Forbrug overføres ikke til en faktura, men vil stadig blive brugt i VIA-beregningen. |
| **Fakturerbar** |Kunden faktureres for forbruget. Forbrug overføres til fakturaen, baseret på det antal, der er angivet i feltet Antal, der skal overf. til faktura. |

> [!NOTE]  
>   Feltet **Planlægningsdato** for planlægningslinjen er den dato, hvor forbrug, der vedrører planlægningslinjen, forventes at fuldføres. Det er også den dato, hvor planlægningslinjen kan overføres til en salgsfaktura og bogføres.  

> [!NOTE]  
>   Når du udfylder feltet **Antal**, beregnes og udfyldes alle oplysninger om salgsbeløb og kostbeløb for planlægningslinjen. Du kan redigere dem når som helst.

I vinduet **Jobkort** , kan du nu se en oversigt over de samlede budgetterede omkostninger, budgetteret pris, fakturerbare omkostninger og fakturerbar pris for hver opgave.

Du kan finde oplysninger om registrering af budgetterede og faktiske sagspriser og -omkostninger i [Sådan gør du: Registrere forbrug for sager](projects-how-record-job-usage.md).

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

