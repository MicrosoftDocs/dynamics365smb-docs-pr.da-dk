---
title: Oprette en sagssalgsfaktura for at fakturere for en sag
description: Beskriver, hvordan du fakturerer debitorer for diverse udgifter, efterhånden som et projekt skrider frem og omkostningerne stiger.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.search.form: 1002, 1007,
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: d2d2437028c5d7e7f8ad4bc613e4f6bf1dc06de3
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146302"
---
# <a name="invoice-jobs"></a>Fakturere sager
I løbet af projektet kan der akkumuleres sagsomkostninger fra ressourceforbrug, materialer og sagsrelaterede indkøb. Efterhånden som status for sagen ændrer sig, bogføres disse transaktioner i sagskladden. Det er vigtigt, at alle omkostninger er registreret i sagskladden, før du fakturerer kunden.

> [!NOTE]
> Du kan også købe eksterne ressourcer uden relation til en sag, f.eks. for at fakturere en kreditor for udført arbejde. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md).

Du kan fakturere hele sagen fra siden **Sagsopgavelinjer** eller kun fakturere de valgte fakturerbare linjer fra siden **Planlægningslinjer**. Faktureringen kan foretages, når sagen er afsluttet, eller med bestemte intervaller, efterhånden som status for sagen ændres, baseret på en faktureringsplan.

> [!NOTE]  
> Hvis du vælger **Fakturerbar** i feltet **Linjetype for sag** på købsdokumenter for sagsrelaterede indkøb, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger i [Administrere projektforsyninger](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Sådan opretter du flere salgsfakturaer for sager
Du kan oprette en faktura for en sag eller for en eller flere sagsopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, nås.

Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere sager.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret salgsfaktura for sag**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan angive filtre, hvis du vil begrænse de sager, som kørslen skal behandle.
4. Vælg **OK** for at starte oprette fakturaen.  

Du kan gennemse og bogføre oprettede fakturaer i vinduet **Salgsfakturaer**.

> [!NOTE]
> Du kan også fakturere en kunde ved at markere sagen og derefter vælge handlingen **Opret salgsfaktura for sag**. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Sådan opretter og bogfører du salgsfakturaer for sager fra sagsplanlægningslinjer
Du kan oprette en faktura ud fra en sagsplanlægningslinje, og på det tidspunkt angive antallet af varen, ressourcen eller finanskontoen, som du vil fakturere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.
2. Åbn en relevant sag.
3. Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
4. Angiv antallet af varen, ressourcen og finanskontotype, som du vil fakturere, i feltet **Antal til overførsel til faktura** i en sagsplanlægningslinje.  
5. Vælg handlingen **Opret salgsfaktura**.
6. På siden **Opret salgsfaktura** skal du angive bogføringsdatoen, og om du vil oprette en ny faktura eller føje denne faktura til en eksisterende.
7. Vælg knappen **OK**.  
8. På siden **Sagsplanlægningslinjer** skal du vælge **Salgsfakturaer/kreditnotaer**.

    Siden **Salgsfaktura** åbnes og viser det antal, du har overført til fakturaen.
9. Foretag yderligere ændringer, og vælg derefter handlingen **Bogfør**.

> [!NOTE]  
>   Ovenstående fremgangsmåde er ens for at oprette, gennemse og bogføre en sagsrelateret salgskreditnota.


## <a name="see-also"></a>Se også
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
