---
title: Konfigurerer din browser
description: 'Beskriver, hvordan du konfigurerer browsere til at arbejde med Business Central og produkter, der er integreret med den.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Konfigurere og foretage fejlfinding i browseren om, hvordan du arbejder med webklienten Business Central

I denne artikel forklares det, hvordan du konfigurerer din webbrowser, så [!INCLUDE[web_client](includes/web_client.md)] og alle funktionerne fungerer korrekt. Læs denne artikel, hvis du har problemer med at åbne [!INCLUDE[web_client](includes/web_client.md)], fordi nogle problemer kan være forårsaget af browserens indstillinger.

Artiklen indeholder oplysninger om, hvordan du kan konfigurere Microsoft Edge, men kravene til JavaScript, cookies og pop op-vinduer er de samme for alle understøttede browsere. Hvis du har andre browsere, skal du se vejledningen fra producenten.  

## <a name="use-a-supported-browser"></a><a name="use-a-supported-browser"></a><a name="use-a-supported-browser"></a>Brug en understøttet browser

Sørg for at bruge en af de understøttede browsere. Se [Minimumkrav til brug af Business Central](product-requirements.md#browsers).  

## <a name="allow-javascript-from-business-central"></a><a name="allow-javascript-from-business-central"></a><a name="allow-javascript-from-business-central"></a>Tillad JavaScript fra Business Central

*Problem:*

Hvis browseren ikke tillader JavaScript, kan du se **NotSupported/DisabledJavaScript** på adresselinjen og en **HTTP-fejl 404,0-ikke fundet**-meddelelse, når du forsøger at åbne [!INCLUDE[prod_short](includes/prod_short.md)], og den 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Ret:*

1. I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og websteds tilladelser** > **JavaScript**.
2. Gør ét af følgende: Vælg det trin, der anbefales af organisationen:

    - Flytte **Tilladt** til venstre mod venstre (Off). Derefter skal du vælge **Tilføj** og skrive adressen (URL-adressen) til [!INCLUDE[prod_short](includes/prod_short.md)] i feltet **Websted**. Vælg **Tilføj**, når du er færdig.
    - Flytte **Tilladt** til venstre mod højre (On).

## <a name="allow-cookies-from-business-central"></a><a name="allow-cookies-from-business-central"></a><a name="allow-cookies-from-business-central"></a>Tillad cookies fra Business Central

*Problem:*

Hvis browseren ikke tillader cookies, får du vist følgende fejlmeddelelse:

**Beklager, men siden blev ikke fundet. Kontroller adressen, og prøv igen.** 

*Ret:*

1. I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og webstedstilladelser** > **Cookies og webstedsdata**.
2. Flyt **Tillad websteder gemmer og læser cookiedata** til højre (On).  

## <a name="allow-pop-ups-from-business-central"></a><a name="allow-pop-ups-from-business-central"></a><a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Tillad pop-ops fra Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med flere produkter. I nogle tilfælde, som f.eks. med Microsoft Teams [!INCLUDE[prod_short](includes/prod_short.md)] åbnes, eller "pop op-vinduer", i produktet. Denne egenskab kræver, at browseren tillader pop op-vinduer [!INCLUDE[prod_short](includes/prod_short.md)].

*Problem:*

Hvis pop op-vinduer i [!INCLUDE[prod_short](includes/prod_short.md)] er blokeret, vises der en meddelelse, der ligner følgende meddelelse:

**Noget gik galt. Måske blokerer browseren pop op-vinduer, der kræves af Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Ret:*

1. I Microsoft Edge skal du gå til **Indstillinger** > **Cookies og webstedstilladelser** > **Pop op-vinduer og omdirigere**.
2. Flytte **Blokeret** til mod højre (On).
3. Vælg **Tilføj**. Skriv i feltet **Websted** `https://businesscentral.dynamics.com`, og vælg derefter **Tilføj**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Fejlfinding i Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
