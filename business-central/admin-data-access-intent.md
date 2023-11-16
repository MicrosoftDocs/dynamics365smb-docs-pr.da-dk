---
title: Administration af formål med adgang til databaser i Business Central
description: 'Ændring af formålet til adgang til databaser for rapporter, API-sider og forespørgsler.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="managing-database-access-intent"></a>Administration af formål med adgang til database

Som superbruger eller administrator kan du ændre formålet med adgang til databaser for rapporter, sider af typen API og forespørgsler for at forbedre tjenestens ydeevne.

## <a name="overview"></a>Oversigt

[!INCLUDE[prod_short](includes/prod_short.md)] kan konfigureres til at bruge skrivebeskyttede kopier af den primære database (læse-skrive). Hvis du bruger kopien af brugerdatabasen, reduceres den primære databases belastning. I nogle tilfælde vil det også forbedre ydeevnen, når data vises i klienten. Kopier er nyttige for objekter, f.eks. rapporter, forespørgsler og API-sider, som kun bruges til at se data, ikke til at ændre data.

Når objekter køres, bestemmer formålet med adgang til databasen, om der skal bruges en skrivebeskyttet kopi, hvis den er tilgængelig, eller den primære database. Rapporter, API-sider og forespørgsler udvikles med et foruddefineret formål med adgang til databasen (få flere oplysninger i [egenskaben DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

På siden **Liste over formål med adgang til database** kan du tilsidesætte det foruddefinerede formål med adgang til database for objekter, når de køres.

I databaseterminologi kaldes denne funktion ofte for *read scale-out*. Du kan få flere oplysninger om read-scale out og formål med adgang til databaser i [!INCLUDE[prod_short](includes/prod_short.md)] i [Sådan bruger du read scale-out til at forbedre ydeevnen](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)] Hjælp til udviklere og administratorer.

## <a name="to-change-the-database-access-intent"></a>Sådan ændrer du formålet med adgang til databaser

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **listen database-adgangsmetode**, og vælg derefter det relaterede link.

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

## <a name="see-also"></a>Se også
[Forretningsfunktioner](across-business-functionality.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Blive køreklar](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
