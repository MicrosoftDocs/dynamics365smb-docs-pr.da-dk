---
title: Oprette nye virksomheder ved hjælp af en assisterende opsætningsvejledning
description: 'Det er nemt at oprette en ny, tom virksomhed i Business Central. En assisterede opsætningsvejledning hjælper dig gennem trinene, og du kan indlæse forretningsdata.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# Opret nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] bliver beholderen til forretningsdata, der hører til en afdeling eller en juridisk enhed, kaldet en *virksomhed*. Når du logger på [!INCLUDE[prod_short](includes/prod_short.md)], får du angivet et demoregnskab og en tom virksomhed, *Min virksomhed*. Det er nemt at skifte mellem virksomhederne: Du skal bare gå til **Mine indstillinger** og flytte til den anden virksomhed. Men du kan også oprette nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)], afhængigt af dine forretningsmæssige behov.  

> [!NOTE]
> Hvis du vil oprette en ny virksomhed, skal du have tildelt tilladelsessættet **Super**.

Når du opretter en ny virksomhed, hjælper en assisterede opsætningsvejledning dig med at få styr på det grundlæggende. Du kan derefter indlæse data fra dit gamle system eller en anden virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Vælge den rigtige skabelon

Hvis du vil indsætte en virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruge den assisterende opsætningsvejledning **Opret ny virksomhed** for at komme i gang. Opsætningsvejledningen er tilgængelig fra siden **Virksomheder** og fra opslag i feltet **Virksomhed** på siden **Mine indstillinger**.  

Installationsguiden har tre skabeloner og en tom indstilling:

- **Evaluering – Eksempeldata**  
    Opret en virksomhed, der ligner demoregnskabet med eksempeldata og opsætningsdata. Denne type virksomhed er tilgængelig uden at skifte til en 30-dages prøveperiode, som de andre typer gør.  
- **Avanceret evaluering - komplette eksempeldata** Opret en virksomhed med omfanget af avanceret funktionalitet, som har alt hvad du behøver for at evaluere produktet for virksomheder med avancerede processer. Denne type virksomhed er tilgængelig uden at skifte til en 30-dages prøveperiode, som de andre typer gør.
- **Produktion – Kun opsætning af data**  
    Oprette et regnskab, der ligner **Mit firma**, med opsætningsdata, f.eks. en kontoplan, betalingsmetoder og definitioner af økonomiske rapporter, men uden eksempeldata. Du kan bruge denne virksomhed i en 30-dages prøveperiode.
- **Opret ny – Ingen data**  
    Opret en tom virksomhed uden opsætningsdata. Du kan bruge denne virksomhed i en 30-dages prøveperiode.  

Hvis du vil komme hurtigt i gang med en ny virksomhed, kan du vælge **Produktion - Kun konfigurationsdata** og derefter importere dine egne forretningsdata, som f.eks. debitorer, varer og kreditorer. Vælg skabelonen **Ny**, hvis du vil oprette alt fra bunden. I så fald kan du bruge den assisterende opsætningsvejledning **Virksomhedsopsætning** til at hjælpe dig i gang med de vigtige opsætningsdata.  

> [!NOTE]  
> Når du opretter en ny virksomhed, tager det nogle minutter, før du kan få adgang til den i [!INCLUDE[prod_short](includes/prod_short.md)]. Opsætningsstatussen på siden **Virksomheder** vises som standard, når den nye virksomhed er klar til dig. Derefter kan du skifte til den nye virksomhed ved hjælp af **Mine indstillinger**.  

Under din 30-dages prøveperiode kan du oprette et ubegrænset antal nye virksomheder, men de er kun tilgængelige under prøveperioden. Kontakt din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for at få yderligere oplysninger. Se også artiklen om [Dynamics 365 Business Central-prøveversionen, ofte stillede spørgsmål](trial-faq.md).  

Administratoren kan få mere at vide om forsøg og abonnement [her](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## Kopiér virksomhed

På siden **Virksomheder** kan du bruge handlingen **Kopiér** til at oprette endnu en virksomhed baseret på indholdet af en eksisterende virksomhed. Det er f.eks. nyttigt at kopiere en virksomhed, hvis du vil teste en virksomhed uden at afbryde produktionsdata.

> [!Important]
> Brug ikke kopieringshandlingen til at tage en sikkerhedskopi af et firma. Når du tager en sikkerhedskopi, skal du starte med at eksportere databasen som en. bacpac-fil. Du kan finde flere oplysninger i [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjælpen til udvikling og administration.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Konfigurere virksomheden

Når du logger på en ny virksomhed, vil den assisterede opsætningsguide **Virksomhedsopsætning** hjælpe dig i gang. Guiden vil bede dig om at angive oplysninger om virksomheden, f.eks. adresse, bankoplysninger og lagerets kostmetode. Disse oplysninger danner grundlag for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], så du ikke behøver at konfigurere dem manuelt.  

F.eks. omfatter [!INCLUDE [prod_short](includes/prod_short.md)] din firmaadresse i fakturaer og andre dokumenter og bankoplysninger i betalinger. Kostmetoden bruges til at beregne priser og lagerværdi.  

Når du har styr på det grundlæggende, kan du oprette de resterende centrale områder. Du er klar til at tilføje forretningsdata, f.eks. debitorer og kreditorer. Du kan finde flere oplysninger i [Konfiguration [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## Virksomheder og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Du kan finde flere oplysninger i [Skifte til en anden virksomhed eller et andet miljø](ui-organization-switch.md). Du kan finde flere oplysninger om miljøer i [Beskrivelse af infrastruktur i Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (kun engelsk version).  

## Ændring af et virksomhedsnavn

Når du opretter en virksomhed, kan du ikke ændre navnet. Men du kan ændre det **Visningsnavn**, som er tekst, der vises for virksomheden i hele programmet.  

> [!TIP]
> Du kan omdøbe et regnskab, hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## Tilføj Contoso Coffee

Contoso Coffee-app indeholder demonstrationsdata, som du kan bruge til at undersøge de avancerede muligheder i [!INCLUDE [prod_short](includes/prod_short.md)]. Find appen i AppSource, og Installer den i en tom virksomhed, f. eks. en virksomhed i et sandkassemiljø. Du kan finde flere oplysninger i [Introduktion til Contoso Coffee - demodata](contoso-coffee/contoso-coffee-intro.md).  

## Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Forståelse af infrastrukturen i Business central online (kun engelsk)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
