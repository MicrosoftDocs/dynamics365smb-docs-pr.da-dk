---
title: Oprette nye virksomheder ved hjælp af en assisterende opsætningsvejledning | Microsoft Docs
description: Det er nemt at oprette en ny, tom virksomhed i Business Central. En assisterede opsætningsvejledning hjælper dig gennem trinene, og du kan indlæse eksisterende forretningsdata.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eae262341eb61e40f130caf45bb838a62aa67cf2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "916563"
---
# <a name="creating-new-companies-in-included365finincludesd365finmdmd"></a>Oprettelse af nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)]
I [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver beholdere til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*. Når du logger på [!INCLUDE[d365fin](includes/d365fin_md.md)], får du angivet et demoregnskab og en tom virksomhed, *Min virksomhed*. Det er nemt at skifte mellem virksomhederne – du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed. Men du kan også oprette nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)], afhængigt af dine forretningsmæssige behov. Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende. Du kan derefter indlæse relevante data fra dit gamle system eller en anden virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Opret ny virksomhed
Hvis du vil indsætte en virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge den assisterende opsætningsvejledning **Opret ny virksomhed** for at komme i gang. Opsætningsguiden er tilgængelig fra siden **Virksomheder** og fra opslag i feltet **Virksomhed** i **Mine indstillinger**.  

Opsætningsguiden indeholder tre skabeloner:

-   **Evaluering - eksempeldata**  
    Den opretter en virksomhed, der ligner demoregnskabet med eksempeldata og opsætningsdata.  
-   **Produktion - kun opsætningsdata**  
    Den opretter en virksomhed, der ligner **Min virksomhed** med opsætningsdata, men uden eksempeldata.
-   **Avanceret evaluering - komplette eksempeldata** Der oprettes en virksomhed med opsætningsdata og komplette eksempeldata til alle funktioner, herunder produktion og service.
-   **Opret ny - Ingen data**  
    Der oprettes en tom virksomhed uden opsætningsdata.  

Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Produktion - Kun konfigurationsdata** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer. Vælg skabelonen **Nyt**, hvis du vil oprette alt fra bunden. I så fald kan du bruge den assisterende opsætningsvejledning **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.  

> [!NOTE]  
>   Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Opsætningsstatussen på siden **Virksomheder** vises som standard, når den nye virksomhed er klar til dig. Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.  

Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden. Kontakt din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner for at få yderligere oplysninger.  

## <a name="company-setup"></a>Virksomhedsopsætning
Når du logger på en ny virksomhed, kører guiden **Virksomhedsopsætning** automatisk og hjælper dig i gang. Du bliver bedt om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode. Vi beder dig om disse oplysninger, fordi de bruges som udgangspunkt for mange områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du så derefter ikke behøver at oprette manuelt senere.  

Din virksomhedsadresse medtages f.eks. i fakturaer og andre dokumenter, bankoplysningerne bruges i betalinger, og kostmetoden bruges til at beregne priser samt lagerværdi.  

Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder. Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer. Du kan finde flere oplysninger i [Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).  

## <a name="see-also"></a>Se også
[Tilpasse Business Central](ui-customizing-overview.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Introduktion](product-get-started.md)  
