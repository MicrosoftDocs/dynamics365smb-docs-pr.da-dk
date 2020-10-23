---
title: Administration af formål med adgang til databaser i Business Central | Microsoft Docs
description: Ændring af formålet til adgang til databaser for rapporter, API-sider og forespørgsler.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 98105cb3e3634169b31a850f20a65a3854b006b4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911551"
---
# <a name="managing-database-access-intent"></a>Administration af formål med adgang til database 

Som superbruger eller administrator kan du ændre formålet med adgang til databaser for rapporter, sider af typen API og forespørgsler for at forbedre tjenestens ydeevne.

## <a name="overview"></a>Oversigt

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan konfigureres til at bruge skrivebeskyttede kopier af den primære database (læse-skrive). Hvis du bruger kopien af brugerdatabasen, reduceres den primære databases belastning. I nogle tilfælde vil det også forbedre ydeevnen, når data vises i klienten. Kopier er nyttige for objekter, f. eks. rapporter, forespørgsler og API-sider, som kun bruges til at se data, ikke til at ændre data.

Når objekter køres, bestemmer formålet med adgang til databasen, om der skal bruges en skrivebeskyttet kopi, hvis den er tilgængelig, eller den primære database. Rapporter, API-sider og forespørgsler udvikles med et foruddefineret formål med adgang til databasen (få flere oplysninger i [egenskaben DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

På siden **Liste over formål med adgang til database** kan du tilsidesætte det foruddefinerede formål med adgang til database for objekter, når de køres.

I databaseterminologi kaldes denne funktion ofte for *read scale-out*. Du kan få flere oplysninger om read-scale out og formål med adgang til databaser i [!INCLUDE[prodshort](includes/prodshort.md)] i [Sådan bruger du read scale-out til at forbedre ydeevnen](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prodshort](includes/prodshort.md)] Hjælp til udviklere og administratorer.

## <a name="to-change-the-database-access-intent"></a>Sådan ændrer du formålet med adgang til databaser

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Liste over formål med adgang til database**, og vælg derefter det relaterede link.

    Siden viser alle rapporter, sider og forespørgsler. Kolonnen **Formål med adgang** indeholder en af følgende værdier:

    |**Indstilling**|**Beskrivelse**|  
    |------------|-------------|  
    |**Standard**|Angiver, at objektet bruger det foruddefinerede formål med adgang til database.|
    |**Tillad skrivning**|Indstiller objektet til at bruge den primære database, så brugeren kan ændre data.|
    |**Skrivebeskyttet**|Angiver, at objektet skal bruge kopien af databasen, hvilket betyder, at brugeren kun kan se data, ikke ændre data.|

2. Vælg handlingen **Rediger liste**.

3. På siden **Rediger – liste over formål med adgang til database** skal du redigere feltet **Formål med adgang** for objekterne.

    > [!NOTE]
    > Hvis et objekt, der kan redigeres (f.eks. Kundekort) er **Skrivebeskyttet**, vil den primære database stadig blive brugt, uanset adgangsformålet, så brugerne kan foretage ændringer som normalt.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Forretningsfunktioner](across-business-functionality.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Introduktion](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
