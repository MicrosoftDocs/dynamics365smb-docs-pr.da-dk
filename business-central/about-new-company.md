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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7724afe2cbc8872fe71f881e436f175668d09a9e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753588"
---
# <a name="creating-new-companies-in-prod_short"></a>Oprettelse af nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] bliver beholderen til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*. Når du logger på [!INCLUDE[prod_short](includes/prod_short.md)], får du angivet et demoregnskab og en tom virksomhed, *Min virksomhed*. Det er nemt at skifte mellem virksomhederne: Du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed. Men du kan også oprette nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)], afhængigt af dine forretningsmæssige behov. Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende. Du kan derefter indlæse relevante data fra dit gamle system eller en anden virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="creating-a-new-company"></a>Oprette en ny virksomhed

Hvis du vil indsætte en virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge den assisterende opsætningsvejledning **Opret ny virksomhed** for at komme i gang. Opsætningsguiden er tilgængelig fra siden **Virksomheder** og fra opslag i feltet **Virksomhed** på siden **Mine indstillinger**.  

Installationsguiden har tre skabeloner og en tom indstilling:

- **Evaluering - eksempeldata**  
    Den opretter en virksomhed, der ligner demoregnskabet med eksempeldata og opsætningsdata.  
- **Produktion - kun opsætningsdata**  
    Den opretter en virksomhed, der ligner **Min virksomhed** med opsætningsdata, men uden eksempeldata.
- **Avanceret evaluering - komplette eksempeldata** Der oprettes en virksomhed med opsætningsdata og komplette eksempeldata til alle funktioner, herunder produktion og service.
- **Opret ny - Ingen data**  
    Der oprettes en tom virksomhed uden opsætningsdata.  

Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Produktion - Kun konfigurationsdata** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer. Vælg skabelonen **Nyt**, hvis du vil oprette alt fra bunden. I så fald kan du bruge den assisterende opsætningsvejledning **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.  

> [!NOTE]  
> Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[prod_short](includes/prod_short.md)]. Opsætningsstatussen på siden **Virksomheder** vises som standard, når den nye virksomhed er klar til dig. Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.  

Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden. Kontakt din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for at få yderligere oplysninger.  

## <a name="copying-a-company"></a>Kopiere et regnskab

På siden **Virksomheder** kan du bruge handlingen **Kopiér** til at oprette endnu en virksomhed baseret på indholdet af en eksisterende virksomhed. Det er f. eks. nyttigt, hvis du vil teste en virksomhed uden at afbryde produktionsdata.

> [!Important]
> Denne funktion kan ikke bruges til at tage en sikkerhedskopi af en virksomhed. Når du tager en sikkerhedskopi af virksomheden, begynder den at eksportere databasen som en. bacpac-fil. Du kan finde flere oplysninger under [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjælpen til udvikling og administration.

## <a name="company-setup"></a>Virksomhedsopsætning

Når du logger på en ny virksomhed, kører guiden **Virksomhedsopsætning** automatisk og hjælper dig i gang. Du bliver bedt om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode. Vi beder dig om disse oplysninger, fordi de bruges som udgangspunkt for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], som du så derefter ikke behøver at oprette manuelt senere.  

Din virksomhedsadresse medtages f.eks. i fakturaer og andre dokumenter, bankoplysningerne bruges i betalinger, og kostmetoden bruges til at beregne priser samt lagerværdi.  

Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder. Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer. Du kan finde flere oplysninger i [Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Virksomheder og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Du kan finde flere oplysninger under [Skifte til en anden virksomhed eller et andet miljø](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Ændring af et virksomhedsnavn

Du kan ikke ændre navnet, når først du har oprettet en virksomhed. Men du kan ændre det **Visningsnavn**, som er tekst, der vises for virksomheden i hele programmet.  

> [!TIP]
> Du kan omdøbe et regnskab, hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importer virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Introduktion](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]