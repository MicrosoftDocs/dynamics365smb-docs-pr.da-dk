---
title: Registrere fakturerbart og budgetteret forbrug for sagsressourcer | Microsoft Docs
description: Beskriver, hvordan du registrerer forbrug af varer eller ressourcer på sager for at gøre projektstyringen nemmere.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: f1b3864eadd616273c3a4a7d061623dab701d01e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792809"
---
# <a name="record-usage-for-jobs"></a>Registrere forbrug for sager
På siden **Sagsplanlægningslinjer** kan du gennemse og registrere forbrug på forskellige dele af din sag, der automatisk opdateres, når du ændrer eller overfører oplysninger mellem sag og sagskladder eller sagsfakturaer. Dette kræver, at du har oprettet en sag, så **Anvend anvendelseslink som standard** er aktiveret. Der er flere oplysninger i [Konfigurere sager](projects-how-setup-jobs.md).  

F.eks. kan du angive antallet af en ressource, og hvilken mængde, der skal overføres til sagskladden, for planlægningslinjer af typen **Budget**. Hvis planlægningslinjens type er **Fakturerbar**, kan du angive antallet af ressourcen, og angive hvilket antal, der skal overføres til en faktura. Ved at sammenligne det antal, der er blevet overført til kladden eller fakturaen med restantallet, kan du hurtigt gennemgå anvendelsesoplysninger.

Følgende procedurer beskrives, hvordan du kan registrere faktiske (fakturerbare) eller budgetterede sagspriser og -omkostninger. Du kan finde oplysninger om vurdering af budgetterede værdier under planlægning under [Administrere sagsbudgetter](projects-how-manage-budgets.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Sådan registreres forbrug for en sagsplanlægningslinje af typen Budget
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Sagsplanlægningslinjer**.
3. Vælg en sagsplanlægningslinje af typen **Budget** eller **Både budget og fakturerbar**, som du vil registrere forbruget for.
4. I feltet **Antal, der skal overføres til kladde** skal du angive det nummer, du vil overføre. Standardantallet er den værdi, du angiver i feltet **Antal**.

    Feltet **Restantal** viser det antal, der mangler for at afslutte sagen og blive overført til kladden.  
5. Vælg handlingen **Opret sagskladdelinjer**.
6. På siden **Kopier sag til sagsplanlægningslinje** skal du udfylde felterne efter behov og derefter vælge knappen **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Vælg handlingen **Åbn sagskladde**.  
8. På siden **Sagskladde** skal du markere den relevante linje, og derefter vælge handlingen **Bogfør**.
9. På siden **Sagsplanlægningslinjer** skal du gennemgå det registrerede forbrug ved at holde øje felterne **Antal**, **Restantal** og **Antal, der skal overføres til kladde**.  
10. Gentag trin 3 til 8 for at registrere ekstra forbrug.  

## <a name="to-record-usage-for-a-job-planning-line-of-type-billable"></a>Sådan registreres forbrug for en sagsplanlægningslinje af typen Fakturerbar
I den næste opgave kan du også registrere forbrug, men for en sagsplanlægningslinje af typen **Fakturerbar**. I dette tilfælde skal du typisk fakturere dit forbrug, men du kan også overføre det til en kladde. Men, hvis du gør det, oprettes der en sagsplanlægningslinje af typen **Budget**, der skal svare til den fakturerbare linje. Du kan finde flere oplysninger i [Administrere sagsbudgetter](projects-how-manage-budgets.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.
2. Markér den relevante sag, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
3. Vælg en sagsplanlægningslinje af typen **Fakturerbar**, som du vil registrere forbruget for.
4. I feltet **Antal, der skal overføres til faktura** skal du angive det nummer, du vil overføre. Standardantallet er den værdi, du angiver i feltet **Antal**.

    Feltet **Antal til fakturering** viser det antal, der mangler for at afslutte sagen og blive faktureret.  
5. Vælg handlingen **Opret salgsfaktura**.
6. På siden **Kopier til salgsfaktura for sag** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.
7. På siden **Sagplanlægningslinjer** skal du markere den relevante linje, og derefter vælge handlingen **Bogfør**.
8. Gennemgå det registrerede forbrug ved at observere felterne **Antal**, **Antal til fakturering**, **Antal til overførsel til faktura** og, hvis salgsfakturaen er blevet bogført, feltet **Fakt. antal**.
9. Gentag trin 3 til 8 for at registrere ekstra forbrug.  
10. For at gennemse en relateret bogført salgsfaktura skal du vælge handlingen **Salgsfakturaer/kreditnotaer**.  
11. Vælg den relevante faktura på siden **Sagsfakturaer**, og vælg derefter **Åbn salgsfaktura/-kreditnota**.         

## <a name="to-create-job-journal-lines-from-job-planning-lines"></a>Sådan oprettes sagskladdelinjer fra sagsplanlægningslinjer
Når du er klar til at bogføre finansielle oplysninger for sager, skal du oprette sagskladdelinjer, som du kan bogføre.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Markér en relevant åben sag, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
3. På siden **Sagsplanlægningslinjer**, på en relevant sagsplanlægningslinje i feltet **Antal, der skal overføres til kladde**, skal du angive det antal, du vil overføre til en sagskladde.  
4. Vælg handlingen **Opret sagskladdelinjer**.
5. På siden **Kopier sag til sagsplanlægningslinje** skal du udfylde felterne efter behov.  
6. Vælg knappen **OK**. Sagskladdelinjer oprettes.
7. Hvis du vil kontrollere overførslen, skal du åbne det relevante sagskladdenavn og kontrollere posterne.  
8. Når sagskladdelinjerne er fuldført, skal du vælge handlingen **Bogfør**.  

## <a name="to-create-job-journal-lines-manually"></a>Sådan oprettes sagskladdelinjer manuelt
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladder**, og vælg derefter det relaterede link.  
2. I feltet **Kladdenavn** skal du vælge et relevant sagskladdenavn.  
3. På en ny linje skal du angive bilagsnummer, sagsnummer, sagsopgavenummer, type og mængde af den type, der forbruges.  
4. Når sagskladdelinjerne er fuldført, skal du vælge handlingen **Bogfør**.  

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Sådan gennemgås planlægningslinjerne for en sagspost
Når du har bogført sagskladdelinjer, kan du se de planlægningslinjer, der er knyttet til posterne i sagskladden, der er blevet bogfør.

> [!NOTE]  
>   Dette kræver, at afkrydsningsfeltet **Anvend anvendelseslink som standard** er blevet valgt til sagen eller er standardindstillingen for alle sager i organisationen. Der er flere oplysninger i [Konfigurere sager](projects-how-setup-jobs.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant sagskladde, og vælg derefter handlingen **Poster**.  
3. På siden **Sagsposter** skal du vælge handlingen **Vis tilknyttede sagsplanlægningslinjer**.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
