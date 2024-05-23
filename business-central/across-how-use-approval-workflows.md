---
title: Godkende eller afvise dokumenter i workflows
description: 'Du kan anmode om, afvise eller uddelegere en godkendelse af f.eks. et købs- eller salgsdokument som en del af et workflow.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Sådan bruges godkendelsesworkflows

Når en post, f.eks et købsdokument eller et debitorkort, skal godkendes af en person i organisationen, sendes en godkendelsesanmodning som en del af en arbejdsgang. Afhængigt af hvordan arbejdsgangen er konfigureret, får den relevante godkender derefter besked om, at posten kræver godkendelse.

Du kan konfigurere godkendelsesworkflows på siden **Workflow**. Du skal også angive godkendelses brugere, herunder eventuelle relevante beløbsgrænser, på siden **Brugeropsætning af godkendelser**. Flere oplysninger i [Konfigurere godkendelsesworkflows](across-set-up-workflows.md).  

Ud over godkendelsesworkflows, der er beskrevet i denne artikel, kan du udføre forskellige andre opgaver i workflowet. Flere oplysninger i [Bruge godkendelsesworkflows](across-use-workflows.md).

Grundlæggende godkendelsesworkflows for købsdokumenter, salgsdokumenter, udbetalingskladder, debitorkort og varekort er klar til brug som vejledninger. Flere oplysninger i [Blive køreklar](ui-get-ready-business.md).

## Anmode om godkendelse af en post

Følgende opgave udføres af en godkendelsesbruger.

1. På siden, hvor posten vises, kan du vælge handlingen **Send godkendelsesanmodning**.
2. Hvis du vil se alle dine godkendelsesanmodninger, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Godkendelsesanmodningsindgange**, vælg derefter det relaterede link.  

Godkendelsespostens status opdateres fra **Oprettet** til **Åben**. Postens status, som f.eks. en købsfaktura, opdateres fra **Åben** til **Afventer godkendelse** og forbliver låst mod behandling, indtil alle godkendere har godkendt posten.

Når alle de ønskede godkendere har godkendt posten, ændres status til **Frigivet**. Du kan derefter fortsætte med at arbejde med posten.

## Annuller godkendelsesanmodninger

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

En kunde vil måske ændre en ordre, efter at den er sendt til godkendelse. I så fald kan du annullere godkendelsesprocessen og foretage de nødvendige ændringer i ordren, inden du anmoder om godkendelse igen.

- På siden, der viser posten, kan du vælge handlingen **Annuller godkendelsesanmodning**.

Når godkendelsesanmodningen er annulleret, ændres statussen for den relaterede godkendelsespost til **Annulleret**. Postens status opdateres fra **Afventer godkendelse** til **Åben**. Herefter kan godkendelsesprocessen starte igen.

## Godkende eller afvise anmodninger om godkendelse

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Du kan behandle godkendelsesanmodninger på siden **Anmodninger til godkendelse** for eksempel for at godkende flere anmodninger ad gangen. Du kan også godkende individuelle poster ved at vælge hyperlinket i den notifikation, du modtager.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anmodninger til godkendelse**, og vælg derefter det relaterede link.
2. Vælg en eller flere linjer for den eller de poster, du vil godkende eller afvise.
3. Vælg handlingerne **Godkend**, **Afvis** eller **Uddeleger**.

Når en post er blevet godkendt eller afvist, ændres godkendelsesstatussen i feltet **Status** til henholdsvis **Godkendt** eller **Afvist**.

Hvis der er konfigureret et godkenderhierarki, er poststatussen **Afventer godkendelse**, indtil alle godkendere, der anmoder, har godkendt posten. Derefter ændres postens status til **Frigivet**.

På samme tid ændres godkendelsespostens status fra **Oprettet** til **Åben**, så snart der oprettes en godkendelsesanmodning for posten. Hvis anmodningen afvises, ændres godkendelsesstatusen til **Afvist**. Statussen forbliver **Åben** eller **Afvist**, indtil alle godkendere har godkendt anmodningen.

## Uddelegere anmodninger om godkendelse

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

For at forhindre, at poster hober sig op eller på anden måde blokerer arbejdsgangen, kan godkenderen og godkendelsesaministratoren uddelegere en godkendelsesanmodning til en stedfortrædende godkender. Stedfortræderen kan enten være en angivet stedfortræder, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du bruger typisk denne funktion, hvis en godkender ikke til stede og ikke kan godkende anmodninger inden forfaldsdatoen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anmodninger til godkendelse**, vælg derefter det relaterede link.
2. Vælg en eller flere linjer for de godkendelsesanmodninger, som du vil uddelegere til en stedfortrædende godkender, vælg derefter handlingen **Uddeleger**.

En notifikation til at godkende anmodningen sendes til en anden foruddefineret stedfortrædende godkender.

## Administrere forfaldne godkendelsesanmodninger

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Du skal med jævne mellemrum få brug for at minde brugere om forfaldne godkendelsesanmodninger. Du skal bruge funktionen **Send beskeder med forfaldne godkendelser** for at gøre det.

Funktionen **Send notifikationer om forfaldne godkendelser** tjekker for alle åbne anmodninger, der aktuelt er forfaldne. Hver godkender med mindst én forfalden godkendelsespost modtager en notifikation med listen over deres forfaldne godkendelsesanmodninger. Notifikationen sendes også til deres godkender og alle anmodere om de forfaldne godkendelser. Det sidste trin kan være en hjælp, hvis den forfaldne godkendelsespost skal uddelegeres til en anden godkender.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Overskredne anmodninger om godkendelsesfrist**, og vælg derefter det relaterede link.
2. På siden **Forfaldne godkendelsesanmodninger** skal du vælge handlingen **Send notifikationer om forfaldne godkendelser**.

## Se også

[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Arbejdsproces](across-workflow.md)  
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Salg](sales-manage-sales.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
