---
title: "Oprette nye virksomheder ved hjælp af en assisterende opsætningsvejledning | Microsoft Docs"
description: "Det er nemt at oprette en ny, tom virksomhed i Dynamics 365 Business edition. En assisterede opsætningsvejledning hjælper dig gennem trinene, og du kan indlæse eksisterende forretningsdata."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c4152a77fcd3e5995aaf09c17b0a3a2c227aa2fa
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="creating-new-companies-in-included365finlongincludesd365finlongmdmd"></a>Oprettelse af nye virksomheder i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
I [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver beholdere til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*. Når du logger på [!INCLUDE[d365fin](includes/d365fin_md.md)], får du angivet en demonstrationsvirksomhed og en tom virksomhed, *Min virksomhed*. Det er nemt at skifte mellem virksomhederne – du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed. Men du kan også oprette nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)], afhængigt af dine forretningsmæssige behov. Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende. Du kan derefter indlæse relevante data fra dit gamle system eller en anden virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Opret ny virksomhed
Hvis du vil indsætte en virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge den assisterende opsætningsguide **Opret ny virksomhed** for at komme i gang. Opsætningsguiden er tilgængelig fra vinduet **Virksomheder** og fra opslag i feltet **Virksomhed** i **Mine indstillinger**.  

Opsætningsguiden indeholder tre skabeloner:

-   **Suite-evaluering**  
    Den opretter en virksomhed, der ligner demonstrationsvirksomheden med eksempeldata og opsætningsdata.  
-   **Suite-produktion**  
    Den opretter en virksomhed, der ligner **Min virksomhed** med opsætningsdata, men uden eksempeldata.  
-   **Nyt**  
    Der oprettes en tom virksomhed uden opsætningsdata.  

Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Suite-produktion** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer. Vælg skabelonen **Nyt**, hvis du vil oprette alt fra bunden. I så fald kan du bruge den assisterende opsætningsguide **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.  

> [!NOTE]  
>   Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Opsætningsstatussen i vinduet **Virksomheder** vises som standard, når den nye virksomhed er klar til dig. Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.  

Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden. Kontakt din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner for at få yderligere oplysninger.  

## <a name="company-setup"></a>Virksomhedsopsætning
Når du logger på en ny virksomhed, kører guiden **Virksomhedsopsætning** automatisk og hjælper dig i gang. Du bliver bedt om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode. Vi beder dig om disse oplysninger, fordi de bruges som udgangspunkt for mange områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du så derefter ikke behøver at oprette manuelt senere.  

Din virksomhedsadresse medtages f.eks. i fakturaer og andre dokumenter, bankoplysningerne bruges i betalinger, og kostmetoden bruges til at beregne priser samt lagerværdi.  

Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder. Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer. Du kan finde flere oplysninger i [Konfigurere Dynamics 365 Business edition](setup.md).  

## <a name="see-also"></a>Se også
[Konfigurere Dynamics 365 Business edition](setup.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

