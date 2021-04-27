---
title: Arbejde med finansielle oversigter i Excel
description: Få mere at vide om, hvordan du kan åbne regnskabsopgørelser i Microsoft Excel fra Business Central for bedre analyse.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 69aaeb21bec95d41aab338caa3013a0947de9ef9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780878"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analysere regnskaber i Microsoft Excel

I [!INCLUDE [prod_short](includes/prod_short.md)] kan du se KPI'er og få vist en oversigt over virksomhedens økonomiske tilstand. Du kan også åbne lister i Excel og analysere dataene der. Men du kan også eksportere tunge regnskabsopgørelser, f.eks. balancen eller resultatopgørelsen, til Excel, analysere dataene og udskrive rapporterne.  

I Business Manager og rollecentrene Regnskabsmedarbejder kan du vælge, hvilke regnskaber du vil have vist i Excel fra en rullemenu i området Rapporter på båndet. Når du vælger et kontoudtog, åbnes det i Excel eller Excel Online. Et tilføjelsesprogram forbinder dataene til [!INCLUDE [prod_short](includes/prod_short.md)]. Du skal dog logge på med den samme konto, der bruges i forbindelse med [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Få oversigten og detaljerne i Excel

Vælg den ønskede Excel-rapport på båndet, og åbn den, så du kan få den oversigt, du søger efter. I denne version af [!INCLUDE [prod_short](includes/prod_short.md)] tilbyder vi følgende rapporter i Excel:

- Balance  
- Resultatopgørelse  
- Pengestrømsopgørelse  
- Opgørelse over overført resultat  
- Aldersfordelt gæld  
- Aldersfordelte tilgodehavender  

Lad os antage, at du vil lære mere om din pengestrøm. Du kan åbne rapporten **Pengestrømsopgørelse** i Excel, men det, der egentlig sker, er, at vi eksporterer de relevante data for dig og opretter en Excel-projektmappe, der er baseret på en foruddefineret skabelon fra Business Manager eller rollecenteret Regnskabsmedarbejder. Afhængigt af din webbrowser kan du blive bedt om at åbne eller gemme projektmappen.  

I Excel kan se du en fane, hvor dataene er opstillet for dig i det første regneark. De data, der blev eksporteret, findes også i andre regneark i de tilfælde, der er behov for. Du kan udskrive rapporten med det samme, eller du kan ændre den, indtil du har den oversigt og de oplysninger, du skal bruge. Brug tilføjelsesprogrammet [!INCLUDE [prod_short](includes/prod_short.md)] Excel til at filtrere og analysere data.  

### <a name="understanding-the-excel-templates"></a>Om Excel-skabeloner

De foruddefinerede Excel-rapporter er baseret på dataene i det aktuelle regnskab. Demoregnskabet har f.eks. oprettet kontoplanen, så du kan få vist tre kontantkonti under de *Aktuelle aktiver*: 10100 **Checkkonto**, 10200 **Opsparingskonto** og 10300 **Kontantbeholdning**. Felterne **Konto underkategori** er angivet til *Kontant*, og det samlede beløb, der vises som *Kontant* i Excel-rapporten **Balance**.  

Yderligere ark i Excel-projektmappen viser dataene bag rapporten. Men hvis du vil se, hvad der skjules bag grupperinger i Excel-rapporterne, kan du f.els. gå tilbage til [!INCLUDE [prod_short](includes/prod_short.md)] og angive filtre til listerne.  

## <a name="the-prod_short-excel-add-in"></a>Tilføjelsesprogrammet [!INCLUDE [prod_short](includes/prod_short.md)]-Excel

Din [!INCLUDE [prod_short](includes/prod_short.md)]-oplevelse indeholder et tilføjelsesprogram til Excel. Afhængigt af dit abonnement er du logget på automatisk, eller du skal angive de samme login-oplysninger, du bruger til [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

Med tilføjelsesprogrammet kan du få nye data fra [!INCLUDE [prod_short](includes/prod_short.md)], og du kan overføre ændringerne tilbage i [!INCLUDE [prod_short](includes/prod_short.md)]. Men muligheden for at sende data tilbage til databasen er deaktiveret for Excel-regnskabsrapporter på listen ovenfor.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Visning og redigering i Excel fra Business Central](across-work-with-excel.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Arbejde med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]