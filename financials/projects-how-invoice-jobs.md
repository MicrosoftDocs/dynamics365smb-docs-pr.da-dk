---
title: "Fremgangsmåde: Fakturere sager | Microsoft Docs"
description: "Beskriver, hvordan du fakturerer debitorer for diverse udgifter, efterhånden som en sag skrider frem."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 28fae2b706873420761f7ce6330df25b280aea44
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-invoice-jobs"></a>Fremgangsmåde: Fakturere sager
I løbet af projektet kan der akkumuleres sagsomkostninger fra ressourceforbrug, materialer og sagsrelaterede indkøb. Efterhånden som status for sagen ændrer sig, bogføres disse transaktioner i sagskladden. Det er vigtigt, at alle omkostninger er registreret i sagskladden, før du fakturerer kunden.

Du kan fakturere hele sagen fra vinduet **Sagsopgavelinjer** eller kun fakturere de valgte fakturerbare linjer fra vinduet **Planlægningslinjer**. Faktureringen kan foretages, når sagen er afsluttet, eller med bestemte intervaller, efterhånden som status for sagen ændres, baseret på en faktureringsplan.

**Bemærk**: Hvis du vælger **Fakturerbar** i feltet **Linjetype for sag** på købsdokumenter for sagsrelaterede indkøb, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger i [Fremgangsmåde: Administrere projektforsyninger](projects-how-manage-project-supplies.md).

## <a name="to-create-and-post-a-job-sales-invoice"></a>Sådan oprettes og bogføres en salgsfaktura for en sag
Du kan oprette en faktura for en sag eller for en eller flere sagsopgaver for en debitor, når det arbejde, der skal faktureres, er udført, eller når den fakturadato, som er angivet i et fakturaskema, nås.

Fra vinduet **Sager** kan du fakturere en kunde ved at markere sagen og derefter vælge handlingen **Opret salgsfaktura for sag**. Følgende procedure viser, hvordan du kan bruge en kørsel til at fakturere flere sager.  

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Opret salgsfaktura for sag** og derefter vælge det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan angive filtre, hvis du vil begrænse de sager, som kørslen skal behandle.
4. Vælg **OK** for at starte oprette fakturaen.  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a>Sådan opretter du flere salgsfakturaer fra sagsplanlægningslinjer
Du kan oprette en faktura ud fra en sagsplanlægningslinje, og på det tidspunkt angive antallet af varen, ressourcen eller finanskontoen, som du vil fakturere.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Sager** og derefter vælge det relaterede link.
2. Åbn en relevant sag.
3. Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
4. Angiv antallet af varen, ressourcen og finanskontotype, som du vil fakturere, i feltet **Antal til overførsel til faktura** i en sagsplanlægningslinje.  
5. Vælg handlingen **Opret salgsfaktura**.
6. I vinduet **Opret salgsfaktura** skal du angive bogføringsdatoen, og om du vil oprette en ny faktura eller føje denne faktura til en eksisterende.
7. Vælg knappen **OK**.  

    Du kan se antallet på sagsplanlægningslinjen i feltet **Antal overført til faktura**.
8. I vinduet **Sagsplanlægningslinjer** skal du vælge **Salgsfakturaer/kreditnotaer**.

    Vinduet **Salgsfaktura** åbnes og viser det antal, du har overført til fakturaen.  
9. Foretag yderligere ændringer, og vælg derefter handlingen **Bogfør**.

**Bemærk**: Ovenstående fremgangsmåde er ens for at oprette, gennemse og bogføre en sagsrelateret salgskreditnota.

## <a name="to-calculate-and-post-job-completion-entries"></a>Sådan beregnes og bogføres sagsafslutningsposter
Når du har fuldført alle aktiviteter for en sag, inklusive bogføring og fakturering af forbrug, skal du opdatere sagen for at få **status** **Afsluttet**. Derefter skal du tilbageføre alt igangværende arbejde, som er blevet bogført i finansregnskabet.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Sager** og derefter vælge det relaterede link.  
2. Vælg en åben sag, og vælg derefter handlingen **Rediger**.
3. I feltet **Status** skal du vælge **Fuldført**.
4. Følg hjælpetrinnene for at beregne og bogføre igangværende arbejde. Du kan også følge trin 5 og 6 for at gøre det manuelt.  
5. Vælg handlingen **Beregn igangværende arbejde**.
6. I vinduet **Beregn VIA for sag** skal du udfylde felterne efter behov.  

     Posterne for igangværende arbejde for sagen, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.  
7. Vælg handlingen **Bogfør VIA - finansafstemning**.
8. I vinduet **Bogfør VIA - finansafstemning** skal du udfylde felterne efter behov.  

     Sagens VIA-finansposter, som blev oprettet ved at udføre kørslen, vil nu være markeret i feltet **Sagen er fuldført** for at vise, at de er færdiggørelsesposter.

## <a name="see-also"></a>Se også
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

