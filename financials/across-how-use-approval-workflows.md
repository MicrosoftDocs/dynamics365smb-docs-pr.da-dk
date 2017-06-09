---
title: "Fremgangsmåde: Bruge godkendelsesworkflows | Microsoft Docs"
description: "Fremgangsmåde: Bruge godkendelsesworkflows"
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ed08fdb7f78c9f6c338e287cd4ef42d7ce0cb72c
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-approval-workflows"></a>Fremgangsmåde: Bruge godkendelsesworkflows
Når en post, f.eks et købsdokument eller et debitorkort, skal godkendes af en person i organisationen, sendes en godkendelsesanmodning som en del af en arbejdsgang. Afhængigt af hvordan arbejdsgangen er konfigureret, får den relevante godkender derefter besked om, at posten kræver godkendelse.

Du kan konfigurere godkendelsesworkflows i vinduet **Workflow**.

Grundlæggende godkendelsesworkflows for købsdokumenter, salgsdokumenter, udbetalingskladder, debitorkort og varekort er klar til brug som assisteret opsætning. Du kan finde flere oplysninger i [Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

**Bemærk**: Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Sådan anmodes om godkendelse af en post
Følgende opgave udføres af en godkendelsesbruger.

1. I det vindue, hvor posten vises, kan du vælge handlingen **Send godkendelsesanmodning**.
2. Hvis du vil se alle dine anmodninger om godkendelse, skal du i øverste højre hjørne vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Godkendelsesanmodningsposter** og derefter vælge det relaterede link.

Godkendelsespostens status opdateres fra **Oprettet** til **Åben**. Postens status, f.eks. en købsfaktura, opdateres fra **Åben** til **Afventer godkendelse** og forbliver låst mod behandling, indtil alle godkendere har godkendt posten.

Når godkenderen har godkendt posten, ændres status til **Frigivet**. Du kan derefter fortsætte dine opgaver med posten.

## <a name="to-cancel-requests-for-approval"></a>Sådan annulleres godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

En kunde vil måske ændre en ordre, efter at den er sendt til godkendelse. I så fald kan du annullere godkendelsesprocessen og foretage de nødvendige ændringer i ordren, inden du anmoder om godkendelse igen.

- I det vindue, hvor posten vises, kan du vælge handlingen **Annuller godkendelsesanmodning**.

Når godkendelsesanmodningen er annulleret, ændres statussen for den relaterede godkendelsespost til **Annulleret**. Postens status opdateres fra **Afventer godkendelse** til **Åben**. Godkendelsesprocessen kan derefter starte igen.

## <a name="to-make-minor-changes-to-approved-records"></a>Sådan foretages mindre ændringer i godkendte poster
Hvis du vil foretage en mindre ændring af en post, når den er blevet godkendt, kan du åbne posten igen, foretage ændringen og derefter frigive den. Mindre ændringer kan du udføre med knapperne **Genåbn** og **Frigiv**.

1. Åbn det vindue, der viser posten, f.eks en købsfaktura, og vælg derefter handlingen **Åbn igen**.

    Feltet **Bilagsstatus** skifter til **Åben**.
2. Foretag de nødvendige ændringer på posten, f.eks. kreditorens adresse.
3. Vælg handlingen **Frigivelse**.

Når du genåbner kildeposten, er statussen for den relaterede godkendelsespost stadig Godkendt i vinduet **Godkendelsesposter**.

## <a name="to-approve-or-reject-requests-for-approval"></a>Sådan godkendes eller afvises anmodninger om godkendelse
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Du kan behandle godkendelsesanmodninger i vinduet **Anmodninger til godkendelse** for eksempel for at godkende flere anmodninger ad gangen. Alternativt kan du behandle hver anmodning i den relaterede post, f.eks vinduet **Købsfaktura**, ved at klikke på linket i meddelelsen, som du modtager.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anmodninger til godkendelse** og derefter vælge det relaterede link.
2. Vælg en eller flere linjer for den eller de poster, du vil godkende eller afvise.
3. Vælg handlingerne **Godkend**, **Afvis** eller **Uddeleger**.

Når en post er blevet godkendt eller afvist, ændres godkendelsesstatussen i feltet **Status** til **Godkendt** eller **Afvist**.

Hvis der er konfigureret et godkenderhierarki, er poststatussen **Afventer godkendelse**, indtil alle godkendere har godkendt posten. Derefter ændres postens status til **Frigivet**.

På samme tid ændres godkendelsespostens status fra **Oprettet** til **Åben**, så snart der oprettes en godkendelsesanmodning for posten. Hvis anmodningen afvises, ændres godkendelsesstatusen til **Afvist**. Statussen forbliver **Åben** eller **Afvist**, indtil alle godkendere har godkendt anmodningen.

## <a name="to-delegate-requests-for-approval"></a>Sådan uddelegeres godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

For at forhindre, at dokumenter hober sig op eller på anden måde blokerer arbejdsgangen, kan godkenderen og godkendelsesaministratoren uddelegere en godkendelsesanmodning til en stedfortrædende godkender. Stedfortræderen kan enten være en angivet stedfortræder, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du bruger typisk denne funktion, hvis en godkender ikke til stede og ikke kan godkende anmodninger inden forfaldsdatoen.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Anmodninger til godkendelse** og derefter vælge det relaterede link.
2. Vælg en eller flere linjer for de godkendelsesanmodninger, som du vil uddelegere til en stedfortrædende godkender, og vælg derefter handlingen **Uddeleger**.

En notifikation til at godkende anmodningen sendes til en anden foruddefineret stedfortrædende godkender.

## <a name="to-manage-overdue-approval-requests"></a>Sådan administreres forfaldne godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Med jævne mellemrum skal du minde brugerne i en godkendelsesarbejdsgang om forfaldne godkendelsesanmodninger, de skal reagere på. Du bruger funktionen **Send notifikationer om forfaldne godkendelser** til dette.

Funktionen **Send notifikationer om forfaldne godkendelser** tjekker for alle åbne anmodninger, der aktuelt er forfaldne. Hver godkender, der har mindst én forfalden godkendelsespost, modtager en notifikation med listen over deres forfaldne godkendelsesanmodninger. Notifikationen sendes også til deres godkender og alle anmodere om de forfaldne godkendelser. Det kan være en hjælp, hvis den forfaldne godkendelsespost skal uddelegeres til en anden godkender.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Forfaldne godkendelsesanmodninger** og derefter vælge det relaterede link.
2. I vinduet **Forfaldne godkendelsesanmodninger** skal du vælge handlingen **Send notifikationer om forfaldne godkendelser**.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)    
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

