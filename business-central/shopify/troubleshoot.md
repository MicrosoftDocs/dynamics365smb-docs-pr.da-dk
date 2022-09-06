---
title: Fejlfinding af Shopify og Business Central-synkronisering
description: Få mere at vide om, hvad du skal gøre, hvis noget er galt under synkronisering af data mellem Shopify Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30118, 30119, 30120,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 47b0d72283b4d017bb522c3e71f6c61501b59d5b
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361937"
---
# <a name="troubleshooting-shopify-and-business-central-synchronization"></a>Fejlfinding af Shopify og Business Central-synkronisering

Det er muligt at køre i situationer, hvor du skal foretage fejlfinding af problemer ved synkronisering af data mellem Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne side definerer trin til fejlfinding i forbindelse med almindelige scenarier, der kan opstå.

## <a name="logs"></a>Logfiler

Hvis en synkroniseringsopgave mislykkes, kan du aktivere logføring ved at aktivere til/fra-feltet **Log aktiveret** på siden **Shopify-butikskortet**. Udløs derefter synkroniseringsopgaven manuelt, og gennemgå logfiler manuelt.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify-logposter**, og vælg det relaterede link.
2. Vælg den relaterede logpost, og åbn siden **Shopify-logpost**.
3. Gennemsynsanmodning, statuskode og beskrivelse og svarværdier.

Husk at slå logføring fra for at undgå negativ påvirkning af ydeevnen og øge databasens størrelse.

Fra siden **Shopify-logposter** kan du udløse sletning af alle logposter eller filer, der er ældre end syv dage.

## <a name="data-capture"></a>Dataregistrering

Uanset hvilken indstilling der er aktiveret for **Log aktiveret** vil nogle svar fra Shopify altid være logført, som du kan kontrollere eller hente i vinduet **Liste over registrerede data**.

Vælg handlingen **Hentet Shopify-data** på en af følgende sider:

- **Shopify-ordre**
- **Shopify-ordreopfyldning**
- **Shopify-ordreforsendelsesomkostninger**
- **Shopify-ordretransaktioner**
- **Shopify-udbetalinger**
- **Shopify-betalingstransaktioner**
- **Shopify-transaktioner**

## <a name="reset-sync"></a>Nulstil synkronisering

For at opnå optimal ydeevne importerer connectoren kun kunder, produkter og ordrer, der er oprettet eller ændret siden sidste synkronisering. På siden **Shopify-butikskort** er der funktioner, der kan ændres seneste synkroniseringsdato/-tidspunkt eller helt nulstille. Denne funktion sikrer, at alle data synkroniseres og ikke kun ændringerne siden den seneste synkronisering, når synkroniseringen køres.

Denne funktion gælder kun for synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Det kan være nyttigt, hvis du har brug for at gendanne slettede data, f. eks. produkter, kunder eller slettede ordrer.

## <a name="request-the-access-token"></a>Anmode om adgangstoken

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke kan oprette forbindelse til din Shopify-konto, kan du prøve at nulstille dette adgangstoken fra Shopify. Denne anmodning kan være nødvendig, hvis der er en rotation af sikkerhedsnøgler eller ændringer af nødvendige tilladelser (områder).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butikker**, og vælg det relevante link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge på din Shopify-konto.

Funktionen **Vis Accesskey** vil blive aktiveret.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Kontrollere og aktivere tilladelser til at foretage http-anmodninger, når der køres i et ikke-produktionsmiljø

Hvis Shopify-connector-udvidelsen skal fungere korrekt, kræver det, at du har tilladelse til at foretage http-anmodninger. Når der testes i sandkasse, er http-anmodninger forbudt for alle udvidelser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **udvidelsesstyring**, og vælg derefter det relaterede link.
2. Vælg udvidelsens *Shopify Connector*.
3. Vælg handlingen **Konfigurer** for at åbne siden **Udvidelsesindstilling**.
4. Kontroller, at funktionen **Tillad HTTPClient-anmodninger** er aktiveret.

## <a name="rotate-the-shopify-access-token"></a>Rotere Shopify-adgangstoken

Følgende procedurer beskriver, hvordan du kan rotere det adgangstoken, der bruges af Shopify-connector, til at få adgang til dit Shopify online Center.

### <a name="in-shopify"></a>I Shopify

1. Fra din **Shopify Admin** skal du gå til [Apps](https://www.shopify.com/admin/apps).
2. I rækken med **Dynamics 365 Business Central**-appen skal du vælge **Slet**.
3. I meddelelsen, der vises, skal du vælge **Slet**.

### <a name="in-prod_short"></a>I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](../media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Shopify Butikker**, og vælg det relevante link.
2. Marker den butik, for hvilken du vil have adgangstoken til at åbne siden **Shopify-butikskort**.
3. Vælg handlingen **Anmod om adgang**.
4. Hvis du bliver bedt om det, skal du logge ind på din Shopify-konto, gennemse personlige oplysninger og tilladelser og derefter vælge knappen **Installer app**.

## <a name="known-issues"></a>Kendte problemer

Feltet *Virksomhedsbogføringsgruppen* må ikke være nul eller tom. der skal være en værdi i feltet kunde. Sådan rettes:

Udfyld feltet **Debitorskabelonkode** på siden **Shopify Butikskort** med den skabelon, som har udfyldt **Virksomhedsbogføringsgruppe**. Debitorskabelon bruges ikke kun til oprettelse af debitorer, men også til beregning af salgspris og ved oprettelse af salgsdokumenter.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Import af data til din Shopify-butik er ikke aktiveret. Gå til butikskortet for at aktivere det

I vinduet **Shopify-butikskort** skal du slå **Tillad datasynkronisering med Shopify** til.  Denne til/fra-funktion er beregnet til at beskytte onlinebutikken mod at hente demonstrationsdata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Kom i gang med Connectoren til Shopify](get-started.md)