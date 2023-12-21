---
title: Fejlfinding af forbindelse
description: 'Beskriver, hvordan du kan bruge siden fejlfinding af forbindelser til at identificere og løse problemer med at oprette forbindelse til Business central online.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 11/24/2023
ms.author: jswymer
ROBOTS: NOINDEX
---

# <a name="troubleshoot-connectivity-for-business-central"></a>Fejlfinding i forbindelse med Business central

> **GÆLDER FOR:** [!INCLUDE[prod_short](includes/prod_short.md)] online
>
> Denne funktion findes i øjeblikket kun som forhåndsversion. Funktionaliteten og dokumentationen kan ændres i senere versioner. Hvis du vil bidrage til dokumentation, der er baseret på dine egne resultater, skal du vælge ![Rediger artikel i GitHub.](media/github-edit-pencil.png) **Rediger**, og foreslå ændringer. Så kigger vi på det!

[!INCLUDE[prod_short](includes/prod_short.md)] Online indeholder siden **Fejlfinding i forbindelser**, som du kan bruge til at identificere problemer med din forbindelse til onlinetjenesten. Der er flere ting, der påvirker forbindelsen til Business central, som f. eks. firewallindstillingerne for konfigurationen af netværks-eller domænenavnetjenesten. På siden kan du køre en liste med Kontroller, der diagnosticerer Business Central-forbindelsesproblemer. Du kan bruge oplysningerne til at forsøge at løse problemerne selv eller videresende den til din supportmedarbejder.

> [!NOTE]
> Siden **Fejlfinding i forbindelser** tester ikke netværkets ydeevne eller pålidelighed, som f. eks. hastigheden på forbindelsen. Den kontrollerer kun forbindelsen til forskellige ressourcer.

## <a name="start-the-connectivity-check"></a>Start forbindelseskontrol

1. Åbn en Internet-browser.
2. I adressen skal du angive den URL-adresse, du bruger til at åbne Business central og tilføje `/connectivity` i slutningen. 

    Hvis du f. eks. bruger `https://businesscentral.dynamics.com`, skal du skrive:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Hvis URL-adressen indeholder lejer-id'et `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, skal du f. eks. angive:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Vælg **Start check** på siden **fejlfinding af forbindelser**.

    Der udføres en række kontroller, og resultatet af hver kontrol vises:

    - ![Forbindelsen blev kontrolleret.](media/connectivity-check.png) Angiver, at kontrollen lykkedes.
    - ![Kontrol af forbindelsen mislykkedes.](media/connectivity-failed.png) Angiver, at kontrollen mislykkedes. Gennemgå meddelelsen under kontrollen, hvis du ønsker flere oplysninger.
    - ![Forbindelseskontrol blev ikke kørt.](media/connectivity-blocked.png) Angiver, at kontrollen ikke blev udført, typisk pga. en tidligere kontrol. Gennemgå meddelelsen under kontrollen, hvis du ønsker flere oplysninger.

4. Vælg genstart check for at udføre **Genstarte kontrollen**.

I følgende afsnit forklares de kontroller, der er udført, og du kan angive nogle tip til, hvordan du løser eventuelle problemer.

## <a name="basic-internet-connectivity"></a>Grundlæggende internetforbindelse

Kontroller, at du har forbindelse til internettet, ved at kontrollere, at du kan få adgang til et kendt offentligt domæne, f.eks. www.bing.com.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Browseren understøtter ikke denne kontrol|Åbn siden i en understøttet browser, og prøv igen. Du kan finde en liste over understøttede browsere under [Minimumskrav til brug af Business Central - Browsere](product-requirements.md#browsers)|
|Serveren kunne ikke pinges på følgende URL-adresse: {url}|Kontrollér dine firewallindstillinger.|

## <a name="cdn-content-delivery-network-resources-loading"></a>CDN (Content Delivery Network)-ressourcer indlæser

[!INCLUDE[prod_short](includes/prod_short.md)] bruger Azure-Content Delivery Network (CDN) til at levere ressourcer, der er nødvendige for at køre Business central-webklient. Denne kontrol kontrollerer, at de nødvendige ressourcer er tilgængelige og tilgængelige, når der sendes pingsignal til Business Central-forekomsten i CDN.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Browseren understøtter ikke denne kontrol|Se **Grundlæggende internetforbindelse**-kontrol.|
|Serveren kunne ikke pinges på følgende URL-adresse: {url}|Kontrollér dine firewallindstillinger.|

## <a name="user-authentication"></a>Brugergodkendelse

Kontrollerer, at den aktuelle bruger har logget på en gyldig Business Central-konto.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Ingen bruger er godkendt i øjeblikket|Log på Business central med gyldigt brugernavn og adgangskode.|

## <a name="business-central-environments-discovery"></a>Business central-miljøer

Kontrol af Business Central-miljøer, som er tilgængelige for en godkendt bruger, og kontroller derefter, om brugeren kan godkendes i miljøet.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Ingen godkendt bruger skal kunne udføre denne kontrol for|Se **brugergodkendelse**-kontrol.|
|De tilgængelige miljøer for din konto kunne ikke hentes.|Se oversigten over tilgængelige miljøer i Business Central Administration.|
|Dit brugernavn eller din adgangskode er forkert, eller du har ikke en gyldig konto.| Kontroller, at du logger på med det korrekte brugernavn og den korrekte adgangskode.|

## <a name="application-service-connectivity"></a>Tilslutning af programtjeneste

Kontrollerer, at den godkendte bruger kan oprette forbindelse til et fundet miljø, hvilket typisk starter med produktionsmiljøet.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Ingen godkendt bruger skal kunne udføre denne kontrol for|Se **brugergodkendelse**-kontrol.|
|De tilgængelige miljøer for din konto kunne ikke hentes.|Se **Business central-miljøer**.|
|Ingen klyngeadresse til at udføre denne kontrol for|Se oversigten over tilgængelige miljøer i Business Central Administration.|
|Versions slutpunktet findes ikke|Se oversigten over tilgængelige miljøer i Business Central Administration.|

## <a name="web-server-connectivity"></a>Webserverforbindelse

Kontrollerer, at den godkendte bruger kan oprette forbindelse til webserveren.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Ingen godkendt bruger kan udføre denne kontrol for|Se **brugergodkendelse**-kontrol.|
|De tilgængelige miljøer for din konto kunne ikke hentes.|Se **Business central-miljøer**.|
|Ingen klyngeadresse til at udføre denne kontrol for|Se oversigten over tilgængelige miljøer i Business Central Administration.|
|Der kunne ikke oprettes forbindelse til webserveren|Ryd cachen, og genindlæs siden.|

## <a name="service-health-status"></a>Status for tjenestetilstand

Rapporterer status for Business Centrals servicetilstand ved at kontrollere, om der er angivet udfald.

|Problem|Metoder, du kan prøve|
|-------|-------------|
|Ingen godkendt bruger kan udføre denne kontrol for|Se **brugergodkendelse**-kontrol.|
|Business Central er desværre ikke tilgængelig i øjeblikket. Prøv igen senere.|Prøv igen senere.|

## <a name="see-also"></a>Se også

[Ressourcer til hjælp og support](product-help-and-support.md)  
[Oversigt over opgaver til opsætning af Business Central](setup.md)  
[Ofte stillede spørgsmål om brugen af Business Central](across-faq.yml)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
