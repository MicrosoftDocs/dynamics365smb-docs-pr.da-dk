---
title: Konfigurere OneDrive-integration med Business Central On-premises
description: 'Få mere at vide om, hvordan du kan konfigurere Business Central on-premises til at integrere med OneDrive for Business.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 09/06/2022
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a><a name="configuring-onedrive-integration-with-business-central-on-premises"></a><a name="configuring-onedrive-integration-with-business-central-on-premises"></a>Konfigurere OneDrive-integration med Business Central On-premises

I denne artikel forklares det, hvordan du konfigurerer OneDrive-integration med Business Central on-premises. Til forskel for [!INCLUDE[prod_short](includes/prod_short.md)] online er forbindelsen mellem Business Central og OneDrive for Business ikke konfigureret automatisk. Hvis forbindelsen ikke er konfigureret, kan brugere ikke bruge funktionerne til OneDrive.

Der er to opgaver, der skal udføres for at konfigurere OneDrive-integrationen.

- Den første opgave omfatter registrering af et program (app) på din Azure Active Directory-lejer i Microsoft 365-planen. Den registrerede app bruges til godkendelsesformål. Denne opgave udføres typisk i Azure-portalen og i Business Central-webklienten.
- Den anden opgave omfatter oprettelse af forbindelsen til OneDrive-URL-adressen og aktivering af OneDrive-funktionerne i Business Central. Denne opgave udføres i Business Central-webklienten. Den gøres anderledes i version 21 end for version 19 og 20. Version 21 introducerer en ny **OneDrive-opsætning**, der erstatter **SharePoint-forbindelsesopsætningen**.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises kan kun være tilsluttet OneDrive, der er hostet af Microsoft i skyen. Tilslutning af [!INCLUDE[prod_short](includes/prod_short.md)] på stedet til lageret for mit websted for SharePoint-serveren understøttes ikke.

## <a name="register-an-app-in-azure-ad-for-onedrive-integration"></a><a name="register-an-app-in-azure-ad-for-onedrive-integration"></a><a name="register-an-app-in-azure-ad-for-onedrive-integration"></a><a name="registerapp"></a>Registrere en app i Azure AD til OneDrive-integration

I denne opgave skal du tilføje et registreret program for Business Central i din Azure AD-lejer med din Microsoft 365-plan. Ligesom andre Azure-tjenester, der fungerer sammen med Business Central, kræver OneDrive en appregistrering i Azure Active Directory (Azure AD). Appregistreringen leverer godkendelses- og autorisationstjenester mellem Business Central og SharePoint, der anvendes af OneDrive.

Du kan finde detaljerede trin til, hvordan du udfører dette trin, i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) i hjælpen til udviklere og it-fagfolk.

Når du registrerer programmet, skal du overveje følgende:

- Hvis du allerede har registreret et program som en del af integrationen med et andet Microsoft-produkt, f.eks. Power BI, kan du genbruge denne appregistrering. I så fald skal du blot angive SharePoint-tilladelserne for den eksisterende registrerede app.

- Konfigurer den registrerede app med følgende uddelegerede tilladelser til SharePoint-API:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    For Business central 2021 udgivelsesbølge 2 (version 19) skal du angive disse tilladelser i stedet for:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Hvis du bruger Business Central version 19 eller 20, skal du kopiere det **Program-id (klient)** og den **klienthemmelighed**, der bruges af den registrerede app. Du skal bruge disse oplysninger i næste opgave.

## <a name="get-your-onedrive-url"></a><a name="get-your-onedrive-url"></a><a name="get-your-onedrive-url"></a><a name="url"></a>Hent din OneDrive-URL-adresse

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a><a name="set-up-the-onedrive-connection-in-version-21-and-later"></a><a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>Konfigurere OneDrive-forbindelsen i version 21 og nyere

Brug denne fremgangsmåde, hvis du bruger Business Central 2022 udgivelsesbølge 2 (version 21) eller nyere.

### <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger

- Indirekte, redigere- og slette-tilladelse på tabellen **Dokumentservicescenarie** som minimum

### <a name="run-onedrive-setup"></a><a name="run-onedrive-setup"></a><a name="run-onedrive-setup"></a>Køre Opsætning af OneDrive

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **OneDrive-konfiguration**, og vælg derefter det relaterede link.
2. Første gang du kører den assisterede opsætning, kan du se **Dine personlige oplysninger**. Læs siden, og hvis du kan acceptere vilkårene, skal du vælge **Acceptér** for at fortsætte.
3. På siden **Konfigurer filhåndtering** kan du vælge mellem følgende indstillinger:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. På siden **Konfigurer Business Central** skal du indtaste URL-adressen til OneDrive i feltet **OneDrive-URL-adresse**.

   [Hvordan finder jeg URL-adressen til OneDrive?](#url)
5. Vælg **Test forbindelse**, og vent på resultaterne.
   - Hvis testen lykkes, skal du vælge **Udført**, og så er du klar til at gå i gang.
   - Hvis testen mislykkes, får du vist en meddelelse om problemet. Problemet vedrører som regel den URL-adresse, du har angivet. Vælg **OK** for at vende tilbage til siden **Konfigurer Business Central**, bekræft URL-adressen, og prøv igen.
   - Hvis du ikke allerede har installeret den Azure AD-registrerede app, åbnes vejledningen **Konfigurer Azure Active Directory**.
6. Når den er fuldført, er meddelelsen om beskyttelse af personlige oplysninger for OneDrive-integration accepteret for alle brugere. Hvis du vil ændre den, så brugerne skal acceptere eller afvise den selv, skal du gå til siden **Status for meddelelser om beskyttelse af personlige oplysninger** og vælge **Lad brugeren bestemme** for OneDrive-integrationen. Brugerne bliver derefter bedt om at acceptere eller afvise erklæringen om beskyttelse af personlige oplysninger, første gang de bruger OneDrive-funktionerne. Du kan finde flere oplysninger i [Meddelelser om beskyttelse af personlige oplysninger](privacy-notices-status.md).

## <a name="set-up-the-connection-in--version-19-and-20"></a><a name="set-up-the-connection-in--version-19-and-20"></a><a name="set-up-the-connection-in--version-19-and-20"></a>Konfigurere forbindelsen i [!INCLUDE[prod_short](includes/prod_short.md)] version 19 og 20

Brug denne fremgangsmåde, hvis du bruger Business Central 2022 udgivelsesbølge 1 (version 20) eller 2021 udgivelsesbølge 2 (version 19).
> [!IMPORTANT]
> Ved at konfigurere denne funktion kan du også aktivere ældre funktioner, som sender filer til OneDrive.  
>
>* Funktionen Åbn i Excel kopierer automatisk Excel-filen til OneDrive og åbner den i Excel online. 
>* Når du eksporterer en rapport til en fil, vil filen automatisk blive kopieret til OneDrive og derefter åbne den i Excel online, Word online eller OneDrive. 
>* Andre funktioner kan også blive åbnet automatisk i OneDrive.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikonet, skriv **Microsoft SharePoint-forbindelseskonfiguration**, og vælg derefter det relaterede link.
2. Indtast i feltet **Beskrivelse** en beskrivelse til forbindelsen, f.eks. **OneDrive**.
3. Skriv **Business Central** i feltet **Mappe**.
4. Angiv URL-adressen til OneDrive i feltet **Placering**.

   [Hvordan finder jeg URL-adressen til OneDrive?](#url)
5. I feltet **Klient-id** skal du angive klient-id'et fra din registrerede app.
6. I feltet **Klienthemmelighed** skal du angive hemmeligheden fra din registrerede app. 

> [!IMPORTANT]
> Siden **Konfiguration af SharePoint-forbindelse** bruges til at konfigurere flere ældre funktioner. I sektionen **Generelt** konfigureres forbindelsen til OneDrive, og afsnittet **Delte dokumenter** omdirigerer filerne til SharePoint i stedet for. **Konfiguration af SharePoint-forbindelse** er udfaset, og den fjernes i en kommende version. Det anbefales, at du ikke konfigurerer afsnittet **Delte dokumenter**. Du kan finde flere oplysninger i [Udfasede funktioner i basisappen](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a><a name="after-upgrade-to-version-21"></a><a name="after-upgrade-to-version-21"></a>Efter opgradering til version 21

Når du opgraderer til version 21 eller nyere, vil den eksisterende forbindelse til OneDrive, der er konfigureret på siden **Konfiguration af SharePoint-forbindelse**, stadig fungere. Men da siden **Konfiguration af SharePoint-forbindelse** fjernes i version 23, anbefales det, at du skifter til den nye OneDrive-integration som beskrevet i næste afsnit. Hvis du foretager dette skifte nu, bliver det nemmere, når **Opsætning af SharePoint-forbindelse** bliver fjernet. Desuden giver det dig mulighed for at bruge assisteret opsætning af **OneDrive** til at administrere de OneDrive-funktioner, som brugerne har adgang til.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a><a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a><a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Skifte fra ældre SharePoint til ny OneDrive-integration

Hvis du vil skifte til den nye OneDrive-integration, skal du køre den assisterede opsætningsvejledning til **OneDrive**, som du kan åbne direkte eller fra den ældre side **Konfiguration af SharePoint-forbindelse**. Den assisterede opsætning af **OneDrive** vil føre dig gennem overgangen, så du kan angive oplysninger om de ændringer, der er foretaget undervejs.

Før du begynder med omskiftet, eller mens du gør det, skal du se næste afsnit for at lære mere om nogle aspekter og overvejelser om processen. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="about-switching-to-the-new-onedrive-integration"></a><a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Om at skifte til den nye OneDrive-integration

Ud over OneDrive-integration kan Business Central også integreres med andre servicer, f.eks. Power BI og Universaludskrivning. Integration med disse andre tjenester kræver også en registreret Azure AD-app til godkendelse. Den Azure AD-app, som bruges af disse andre tjenester, er konfigureret i den assisterede opsætning **Konfigurer dine Azure Active Directory-konti**. Når du skifter fra den ældre opsætning af SharePoint-forbindelsen, ændrer den nye assisterede opsætning af **OneDrive** din OneDrive-integration til også at bruge den assisterede opsætning **Konfigurer dine Azure Active Directory-konti**, så alle integrationer bruger den samme Azure AD-app.

Denne ændring har betydning, når der skiftes til den nye OneDrive-integration, afhængigt af om der allerede er konfigureret en Azure AD-app i den assisterede opsætning **Konfigurer dine Azure Active Directory-konti**. 

> [!IMPORTANT]
> Når du har skiftet til den nye OneDrive-opsætning, kan du ikke længere bruge siden **Konfiguration af SharePoint-forbindelse** til at konfigurere OneDrive-integrationen.

#### <a name="how-the-changes-affect-the-integration"></a><a name="how-the-changes-affect-the-integration"></a><a name="how-the-changes-affect-the-integration"></a>Sådan påvirker ændringerne integrationen

Den assisterede opsætning af **OneDrive** vil altid bruge den app, der er konfigureret i den assisterede opsætning **Konfigurer dine Azure Active Directory-konti**, hvis der er en sådan. Når du kører den assisterede opsætning af **OneDrive**, sammenlignes den app, der er konfigureret i **Konfigurer dine Azure Active Directory-konti** med din aktuelle app, der er konfigureret i **Konfiguration af SharePoint-forbindelse**.

> [!TIP]
> På siden **Konfiguration af SharePoint-forbindelse** og **Konfigurer dine Azure Active Directory-konti** med assisteret opsætning, identificeres Azure AD-appen af **klient-id'et**.

- Hvis appen i **Konfigurer dine Azure Active Directory-konti** er anderledes end appen i **Konfiguration af SharePoint-forbindelse**, vil OneDrive-integrationen skifte, så den bruger appen i **Konfigurer dine Azure Active Directory-konti**.

   I **Opsætning af OneDrive** får du ved skiftet vist en meddelelse i stil med følgende: 

  `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` repræsenterer klient-id'et for appen i **Konfigurer dine Azure Active Directory-konti**, som OneDrive-integration er skiftet til. 

  > [!IMPORTANT]
  > Hvis den nye OneDrive-integration skal virke, efter at du har foretaget skiftet, skal du give appen tilladelse til SharePoint-API'et i Azure-portalen. Du kan udføre dette trin, før eller efter du skifter til den nye OneDrive-opsætning. Du kan finde flere oplysninger i afsnittet [Registrere en app i Azure AD til OneDrive-integration](#registerapp).

- Hvis appen i **Konfigurer dine Azure Active Directory-konti** er den samme som appen i **Konfiguration af SharePoint-forbindelse**, vil OneDrive-integrationen bruge den samme app som før, bortset fra konfigurationen under opsætningen **Konfigurer dine Azure Active Directory-konti**.

   I **Opsætning af OneDrive** får du ved skiftet vist en meddelelse i stil med følgende:

    `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Hvis der ikke er konfigureret en app i opsætningen **Konfigurer dine Azure Active Directory-konti**, vil OneDrive -integrationen bruge den samme app som før.

   Den assisterede opsætning af **OneDrive** vil kopiere appkonfiguration til **Konfigurer dine Azure Active Directory-konti**, så den bruges til andre integrationer, der kan konfigureres senere.

   I **Opsætning af OneDrive** får du ved skiftet vist en meddelelse i stil med følgende:

   `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a><a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a><a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Kør OneDrive-opsætningen for at skifte til den nye OneDrive-integration

1. Åbn enten siden **Opsætning af OneDrive** eller **Konfiguration af SharePoint-forbindelse**.
2. Hvis du bruger siden **Konfiguration af SharePoint-forbindelse**, skal du vælge **Gå til ny OneDrive-konfiguration** i meddelelsen øverst på siden.
3. Følg vejledningen i den assisterede opsætning af **OneDrive**.
4. Når du kommer til siden **Konfigurer filhåndtering**, skal du vælge en af følgende indstillinger for at aktivere funktioner:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. Siden **Konfigurer Business Central** viser den samme URL-adresse, som bruges af den eksisterende OneDrive-integration. Om nødvendigt kan du ændre URL-adressen.
6. Vælg **Test forbindelse**, og følg instruktionerne.

   Hvis testen lykkes, skal du vælge **Udført**, og så er du klar til at gå i gang. Ellers kan du bruge meddelelserne på siden til at løse problemet.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Business Central og OneDrive for Business Integration](across-onedrive-overview.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)

