---
title: Godkende eller afvise dokumenter i workflows | Microsoft Docs
description: Du kan anmode om, afvise eller uddelegere en godkendelse af f.eks. et købs- eller salgsdokument som en del af et workflow.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: 55e7861d479ee5d4415ca776f969b722464ddcc3
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531913"
---
# <a name="use-approval-workflows"></a>Bruge godkendelsesworkflows

Når en post, f.eks et købsdokument eller et debitorkort, skal godkendes af en person i organisationen, sendes en godkendelsesanmodning som en del af en arbejdsgang. Afhængigt af hvordan arbejdsgangen er konfigureret, får den relevante godkender derefter besked om, at posten kræver godkendelse.

Du kan konfigurere godkendelsesworkflows på siden **Workflow**. Du skal også angive godkendelses brugere, herunder eventuelle relevante beløbsgrænser, på siden **Brugeropsætning af godkendelser**. Du kan finde flere oplysninger i [Opsætte workflows](across-set-up-workflows.md).  

Ud over godkendelsesworkflows, der er beskrevet i denne artikel, kan du udføre forskellige andre opgaver i workflowet. Der er flere oplysninger i [Brug arbejdsgange](across-use-workflows.md).

Grundlæggende godkendelsesworkflows for købsdokumenter, salgsdokumenter, udbetalingskladder, debitorkort og varekort er klar til brug som vejledninger. Du kan finde flere oplysninger i [Blive køreklar](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>Sådan anmodes om godkendelse af en post

Følgende opgave udføres af en godkendelsesbruger.

1. På siden, hvor posten vises, kan du vælge handlingen **Send godkendelsesanmodning**.
2. Hvis du vil se alle dine godkendelsesanmodninger, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Godkendelsesanmodningsindgange**, og vælg derefter det relaterede link.  

Godkendelsespostens status opdateres fra **Oprettet** til **Åben**. Postens status, f.eks. en købsfaktura, opdateres fra **Åben** til **Afventer godkendelse** og forbliver låst mod behandling, indtil alle godkendere har godkendt posten.

Når alle de ønskede godkendere har godkendt posten, ændres status til **Frigivet**. Du kan derefter fortsætte dine opgaver med posten.

## <a name="to-cancel-requests-for-approval"></a>Sådan annulleres godkendelsesanmodninger

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

En kunde vil måske ændre en ordre, efter at den er sendt til godkendelse. I så fald kan du annullere godkendelsesprocessen og foretage de nødvendige ændringer i ordren, inden du anmoder om godkendelse igen.

- På siden, hvor posten vises, kan du vælge handlingen **Annuller godkendelsesanmodning**.

Når godkendelsesanmodningen er annulleret, ændres statussen for den relaterede godkendelsespost til **Annulleret**. Postens status opdateres fra **Afventer godkendelse** til **Åben**. Godkendelsesprocessen kan derefter starte igen.

## <a name="to-approve-or-reject-requests-for-approval"></a>Sådan godkendes eller afvises anmodninger om godkendelse

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Du kan behandle godkendelsesanmodninger på siden **Anmodninger til godkendelse** for eksempel for at godkende flere anmodninger ad gangen. Alternativt kan du behandle hver anmodning i den relaterede post, f.eks siden **Købsfaktura**, ved at klikke på linket i meddelelsen, som du modtager.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anmodninger til godkendelse**, og vælg derefter det relaterede link.
2. Vælg en eller flere linjer for den eller de poster, du vil godkende eller afvise.
3. Vælg handlingerne **Godkend**, **Afvis** eller **Uddeleger**.

Når en post er blevet godkendt eller afvist, ændres godkendelsesstatussen i feltet **Status** til **Godkendt** eller **Afvist**.

Hvis der er konfigureret et godkenderhierarki, er poststatussen **Afventer godkendelse**, indtil alle godkendere har godkendt posten. Derefter ændres postens status til **Frigivet**.

På samme tid ændres godkendelsespostens status fra **Oprettet** til **Åben**, så snart der oprettes en godkendelsesanmodning for posten. Hvis anmodningen afvises, ændres godkendelsesstatusen til **Afvist**. Statussen forbliver **Åben** eller **Afvist**, indtil alle godkendere har godkendt anmodningen.

## <a name="to-delegate-requests-for-approval"></a>Sådan uddelegeres godkendelsesanmodninger

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

For at forhindre, at dokumenter hober sig op eller på anden måde blokerer arbejdsgangen, kan godkenderen og godkendelsesaministratoren uddelegere en godkendelsesanmodning til en stedfortrædende godkender. Stedfortræderen kan enten være en angivet stedfortræder, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du bruger typisk denne funktion, hvis en godkender ikke til stede og ikke kan godkende anmodninger inden forfaldsdatoen.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anmodninger til godkendelse**, og vælg derefter det relaterede link.
2. Vælg en eller flere linjer for de godkendelsesanmodninger, som du vil uddelegere til en stedfortrædende godkender, og vælg derefter handlingen **Uddeleger**.

En notifikation til at godkende anmodningen sendes til en anden foruddefineret stedfortrædende godkender.

## <a name="to-manage-overdue-approval-requests"></a>Sådan administreres forfaldne godkendelsesanmodninger

Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Med jævne mellemrum skal du minde brugerne i en godkendelsesarbejdsgang om forfaldne godkendelsesanmodninger, de skal reagere på. Du bruger funktionen **Send notifikationer om forfaldne godkendelser** for at påminde brugere.

Funktionen **Send notifikationer om forfaldne godkendelser** tjekker for alle åbne anmodninger, der aktuelt er forfaldne. Hver godkender, der har mindst én forfalden godkendelsespost, modtager en notifikation med listen over deres forfaldne godkendelsesanmodninger. Notifikationen sendes også til deres godkender og alle anmodere om de forfaldne godkendelser. Det sidste trin kan være en hjælp, hvis den forfaldne godkendelsespost skal uddelegeres til en anden godkender.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Overskredne anmodninger om godkendelsesfrist**, og vælg derefter det relaterede link.
2. På siden **Forfaldne godkendelsesanmodninger** skal du vælge handlingen **Send notifikationer om forfaldne godkendelser**.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/use-approval-workflows/)

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Salg](sales-manage-sales.md)  
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
