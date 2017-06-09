---
title: "Fremgangsmåde: Administrere budgetter for anlægsaktiver | Microsoft Docs"
description: "Beskriver, hvordan du budgetterer for anlægsaktiver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 99df89d29271b7c8426959019dc52ece42525709
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-budgets-for-fixed-assets"></a>Fremgangsmåde: Administrere budgetter for anlægsaktiver
Du kan konfigurere budgetterede anlægsaktiver. Du kan f.eks. inkludere forventede anskaffelser og salg i rapporterne.  

Hvis du vil forberede din budgetterede resultatopgørelse, balance og kontantbudget, skal du bruge oplysninger om fremtidige investeringer, salg og afskrivning på anlægsaktiver. Du kan få disse oplysninger fra rapporten **Anlæg - forventet værdi**. Inden du udskriver rapporten, skal du have forberedt budgettet.  

**Bemærk**: Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Sådan budgetteres anskaffelsesprisen for et anlægsaktiv
Når du skal forberede et budget, skal du oprette anlægskort for de anlægsaktiver, du har planlagt at købe. De budgetterede anlægsaktiver oprettes som almindelige anlægsaktiver, men de skal være angivet til ikke at blive bogført i finansregnskabet.

Når du bogfører anskaffelsesprisen, skal du angive nummeret på det budgetterede anlægsaktiv i feltet **Budgetanlægsnr.** . Dermed bogføres automatisk en anskaffelsespris med modsat fortegn for budgetanlægget. Det betyder, at de samlede anskaffelsesomkostninger for budgetanlægget er forskellen mellem den budgetterede og den faktiske anskaffelsesomkostning.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anlægsaktiver** og derefter vælge det relaterede link.
2. Vælg handlingen **Ny** for at oprette et nyt anlægskort for det budgetterede anlægsaktiv.
3. Markér afkrydsningsfeltet **Budgetanlæg** for at forhindre bogføring i finansregnskabet.
4. Udfyld resten af felterne, tildel en afskrivningsprofil, og bogfør derefter den første anskaffelsespris for det budgetterede anlægsaktiv, der er angivet i feltet **Budgetanlægsnr.** på kladdelinjen. Du kan finde flere oplysninger i [Fremgangsmåde: Anskaffe anlægsaktiver](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Sådan budgetteres salget af et anlægsaktiv
Hvis du planlægger at sælge anlæg inden for budgetperioden, kan du angive oplysninger om salgspris og -dato.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anlægsaktiver** og derefter vælge det relaterede link.
2. Vælg det anlægsaktiv, der skal sælges, og vælg derefter handlingen **Afskrivningsprofiler**.
3. I vinduet **Anlægsafskrivningsprofiler** skal du udfylde felterne **Forventet salgsdato** og **Forventet salgspris**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Sådan vises forventede salgsværdier
Hvis du vil have vist de forventede salgsværdier og beregne gevinst eller tab, kan du bruge rapporten **Anlæg - forventet værdi**.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anlæg - forventet værdi** og derefter vælge det relaterede link.
2. Udfyld felterne efter behov.
3. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="to-budget-depreciation"></a>Sådan budgetteres afskrivning
Du kan bruge rapporten **Anlæg - forventet værdi** til at beregne den fremtidige afskrivning. I rapporten vises bogført værdi og akkumuleret afskrivning i starten af den valgte periode og ved ændringer i løbet af perioden, og den bogførte værdi og den akkumulerede afskrivning vises ved slutningen af den valgte periode.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anlæg - forventet værdi** og derefter vælge det relaterede link.
2. Udfyld felterne efter behov.
3. Hvis du vil have vist de samlede værdier for alle aktiver, skal du rydde afkrydsningsfeltet **Udskrift pr. anlæg**.
4. Lad oversigtspanelet **Anlæg** stå tomt, hvis alle anlægsaktiver skal inkluderes. I feltet **Budgetanlæg** skal du angive **Nej** for at udelukke budgetanlæg eller **Ja** for kun at få vist budgetanlæg.
5. Vælg knappen **Udskriv** eller **Vis udskrift**.

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

