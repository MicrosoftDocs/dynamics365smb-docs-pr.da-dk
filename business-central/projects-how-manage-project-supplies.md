---
title: Købe varer eller tjenester til en sag og administrere forsyningerne | Microsoft Docs
description: Bruges til at administrere forsyning og køb af materialer og tjenester til sager.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7b3abf9ae0cb07e6b3e79fc21ee10467f4f611b6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748939"
---
# <a name="manage-job-supplies"></a>Administrere sagsforsyninger
Administration af projektforsyninger i form af varer, tjenester og udgifter er et integreret og vigtigt aspekt af udførelse af alle sager. Du kan benytte lagerbeholdningsantal eller oprette sagsspecifikke køb vha. købsordrer eller købsfakturaer. Et servicejob på en computer kræver f.eks. en ny disk. Du opretter en købsfaktura for at købe en ny disk og registrerer den sag, disken skal bruges i.

Hvis købsprocessen ikke kræver, at den fysiske transaktion registreres separat, kan købet behandles på siden **Finanskladde for sag**. Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Sådan køber du varer eller tjenesteydelser for en sag
Følgende procedure viser, hvordan du bruger en købsfaktura til at købe produkter for en sag. Samme fremgangsmåde anvendes, når du anvender en købsordre.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld felterne efter behov. Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).
3. I felterne **Sagsnr.** og **Sagsopgavenr.** skal du vælge oplysningerne, for den sag, som du vil købe varer eller tjenester til. Brug tilpasningsværktøjerne, hvis et felt ikke er synligt. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

    Den værdi, du har valgt i feltet **Sagslinjetype**, angiver, om der oprettes en planlægningslinje, når du bogfører forbruget af varen. Hvis feltet indeholder **Fakturerbar**, oprettes der sagsplanlægningslinjer, som er klar til blive faktureret til kunden. Du kan finde flere oplysninger i [Fakturere sager](projects-how-invoice-jobs.md).
4. Vælg handlingen **Bogfør**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Sådan får du vist værdien for køb for en sag
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.
2. Åbn et relevant sagskort.

    På oversigtspanelet **Opgaver** viser feltet **Udestående ordrer** det samlede udestående beløb i lokal valuta for lagervarer og tjenester på købsdokumenter for sagsopgavelinjen.  

    Feltet **Modt. beløb (ufakt.)** viser værdien af de varer, der er leveret på købsdokumenter, men endnu ikke faktureret.  
3. Vælg et af felterne for at åbne siden **Købslinjer**, hvor kan du gennemse oplysninger om de relaterede købsdokumentlinjer, herunder hvilke varer eller tjenesteydelser der er modtaget.

## <a name="to-post-a-job-related-expense"></a>Sådan bogføres en sagsrelateret udgift
Hvis der påløber specielle udgifter eller engangsudgifter, kan du bruge siden **Finanskladde for sag** til at bogføre dem direkte til den relevante sagskonto.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagsfinanskladder**, og vælg derefter det relaterede link.  
2. Opret en ny linje, og angiv oplysninger om udgiften, inklusive oplysninger i felterne **Sagsnr.** og **Sagsopgavenr**.  
3. Når kladden er fuldført, skal du vælge handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]