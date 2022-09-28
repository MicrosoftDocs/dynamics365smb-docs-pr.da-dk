---
title: Oprette nye virksomheder ved hjælp af en assisterende opsætningsvejledning
description: Det er nemt at oprette en ny, tom virksomhed i Business Central. En assisterede opsætningsvejledning hjælper dig gennem trinene, og du kan indlæse eksisterende forretningsdata.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 19340305e2d39ce0626b3d6cb10974556c24b70f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531535"
---
# <a name="create-new-companies-in-prod_short"></a>Opret nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] bliver beholderen til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*. Når du logger på [!INCLUDE[prod_short](includes/prod_short.md)], får du angivet et demoregnskab og en tom virksomhed, *Min virksomhed*. Det er nemt at skifte mellem virksomhederne: Du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed. Men du kan også oprette nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)], afhængigt af dine forretningsmæssige behov.  

Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende. Du kan derefter indlæse relevante data fra dit gamle system eller en anden virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template"></a>Vælge den rigtige skabelon

Hvis du vil indsætte en virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge den assisterende opsætningsvejledning **Opret ny virksomhed** for at komme i gang. Opsætningsguiden er tilgængelig fra siden **Virksomheder** og fra opslag i feltet **Virksomhed** på siden **Mine indstillinger**.  

Installationsguiden har to skabeloner og en tom indstilling:

- **Evaluering - eksempeldata**  
    Den opretter en virksomhed, der ligner demoregnskabet med eksempeldata og opsætningsdata. Denne type virksomhed er tilgængelig uden at skifte til en 30-dages prøveperiode, som de andre typer gør.  
- **Produktion - kun opsætningsdata**  
    Den opretter en virksomhed, der ligner **Min virksomhed** med opsætningsdata, men uden eksempeldata. Du kan bruge denne virksomhed i en prøveperiode på 30 dage.  
- **Opret ny - Ingen data**  
    Der oprettes en tom virksomhed uden opsætningsdata. Du kan bruge denne virksomhed i en prøveperiode på 30 dage.  

Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Produktion - Kun konfigurationsdata** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer. Vælg skabelonen **Ny**, hvis du vil oprette alt fra bunden. I så fald kan du bruge den assisterende opsætningsvejledning **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.  

> [!NOTE]  
> Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[prod_short](includes/prod_short.md)]. Opsætningsstatussen på siden **Virksomheder** vises som standard, når den nye virksomhed er klar til dig. Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.  

Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden. Kontakt din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for at få yderligere oplysninger. Se også artiklen om [Dynamics 365 Business Central-prøveversionen, ofte stillede spørgsmål](trial-faq.md).  

Administratoren kan få mere at vide om forsøg og abonnement [her](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## <a name="copy-a-company"></a>Kopiér virksomhed

På siden **Virksomheder** kan du bruge handlingen **Kopiér** til at oprette endnu en virksomhed baseret på indholdet af en eksisterende virksomhed. Det er f.eks. nyttigt, hvis du vil teste en virksomhed uden at afbryde produktionsdata.

> [!Important]
> Denne funktion kan ikke bruges til at tage en sikkerhedskopi af en virksomhed. Når du tager en sikkerhedskopi af virksomheden, begynder den at eksportere databasen som en. bacpac-fil. Du kan finde flere oplysninger i [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjælpen til udvikling og administration.

## <a name="set-up-the-company"></a>Konfigurere virksomheden

Når du logger på en ny virksomhed, kører guiden **Virksomhedsopsætning** automatisk og hjælper dig i gang. Du bliver bedt om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode. Vi beder dig om disse oplysninger, fordi de bruges som udgangspunkt for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], som du så derefter ikke behøver at oprette manuelt senere.  

F.eks. omfatter [!INCLUDE [prod_short](includes/prod_short.md)] din firmaadresse i fakturaer og andre dokumenter og bankoplysninger i betalinger. Kostmetoden bruges til at beregne priser og lagerværdi.  

Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder. Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer. Du kan finde flere oplysninger i [Konfiguration [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Virksomheder og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Du kan finde flere oplysninger i [Skifte til en anden virksomhed eller et andet miljø](ui-organization-switch.md). Du kan finde flere oplysninger om miljøer i [Beskrivelse af infrastruktur i Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (kun engelsk version).  

## <a name="changing-a-companys-name"></a>Ændring af et virksomhedsnavn

Du kan ikke ændre navnet, når først du har oprettet en virksomhed. Men du kan ændre det **Visningsnavn**, som er tekst, der vises for virksomheden i hele programmet.  

> [!TIP]
> Du kan omdøbe et regnskab, hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## <a name="add-contoso-coffee"></a>Tilføj Contoso Coffee

Contoso Coffee-app indeholder demonstrationsdata, som du kan bruge til at undersøge de avancerede muligheder i [!INCLUDE [prod_short](includes/prod_short.md)]. Find appen i AppSource, og Installer den i en tom virksomhed, f. eks. en virksomhed i et sandkassemiljø. Du kan finde flere oplysninger i [Introduktion til Contoso Coffee - demodata](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Forståelse af infrastrukturen i Business central online (kun engelsk)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
