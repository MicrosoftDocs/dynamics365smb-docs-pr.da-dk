---
title: "Fremgangsmåde: Administrere sagsforsyninger | Microsoft Docs"
description: Beskriver, hvordan materialer og tjenester leveres til sager.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f52fa9545b50038c1d28daa164add07915ef2656
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-supplies"></a>Fremgangsmåde: Administrere sagsforsyninger
Administration af projektforsyninger i form af varer, tjenester og udgifter er et integreret og vigtigt aspekt af udførelse af alle sager. Du kan benytte lagerbeholdningsantal eller oprette sagsspecifikke køb vha. købsordrer eller købsfakturaer. Et servicejob på en computer kræver f.eks. en ny disk. Du opretter en købsfaktura for at købe en ny disk og registrerer den sag, disken skal bruges i.

Hvis købsprocessen ikke kræver, at den fysiske transaktion registreres separat, kan købet behandles i vinduet **Finanskladde for sag**. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere Registrere forbrug for sager](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Sådan køber du varer eller tjenesteydelser for en sag
Følgende procedure viser, hvordan du bruger en købsfaktura til at købe produkter for en sag. Samme fremgangsmåde anvendes, når du anvender en købsordre.  

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Købsfakturaer** og derefter vælge det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).
3. I felterne **Sagsnr.** og **Sagsopgavenr.** skal du vælge oplysningerne, for den sag, som du vil købe varer eller tjenester til. Brug funktionen **Vis kolonner**, hvis feltet ikke vises. Du kan finde flere oplysninger under [Brugertilpasning](ui-user-personalization.md).

    Den værdi, du har valgt i feltet **Sagslinjetype**, angiver, om der oprettes en planlægningslinje, når du bogfører forbruget af varen. Hvis feltet indeholder **Fakturerbar**, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere sager](projects-how-invoice-jobs.md).
4. Vælg handlingen **Bogfør**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Sådan får du vist værdien for køb for en sag
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Sager** og derefter vælge det relaterede link.
2. Åbn et relevant sagskort.

    På oversigtspanelet **Opgaver** viser feltet **Udestående ordrer** det samlede udestående beløb i lokal valuta for lagervarer og tjenester på købsdokumenter for sagsopgavelinjen.  

    Feltet **Modt. beløb (ufakt.)** viser værdien af de varer, der er leveret på købsdokumenter, men endnu ikke faktureret.  
3. Vælg et af felterne for at åbne vinduet **Købslinjer**, hvor kan du gennemse oplysninger om de relaterede købsdokumentlinjer, herunder hvilke varer eller tjenesteydelser der er modtaget.

## <a name="to-post-a-job-related-expense"></a>Sådan bogføres en sagsrelateret udgift
Hvis der påløber specielle udgifter eller engangsudgifter, kan du bruge vinduet **Finanskladde for sag** til at bogføre dem direkte til den relevante sagskonto.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Sagsfinanskladde** og derefter vælge det relaterede link.  
2. Opret en ny linje, og angiv oplysninger om udgiften, inklusive **Sagsnr.** og **Sagsopgavenr.**.  
3. Når kladden er fuldført, skal du vælge handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

