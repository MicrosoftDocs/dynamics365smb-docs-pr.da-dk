---
title: Konfigurere printere til Universaludskrivning
description: 'Få mere at vide om, hvordan du kan bruge Universaludskrift til at levere Cloud-udskrivning i Business central.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers" />Konfigurere printere til Universaludskrivning

Universaludskrivning er en Microsoft 365-abonnementsbaseret tjeneste, der udelukkende kører på Microsoft Azure. Den giver dig centraliseret printerstyring via portalen for Universaludskrivning. [!INCLUDE[prod_short](includes/prod_short.md)] gør det muligt at konfigurere printere i Universaludskrivning for klientbrugere via udvidelsen **Integration af Universaludskrivning**.

![Konfiguration af Universaludskrivning.](media/Universal-Print-arch.png)

Den komplette konfiguration kræver, at du arbejder i både Microsoft Azure ved hjælp af [Azure-portalen](https://portal.azure.com) og i [!INCLUDE[prod_short](includes/prod_short.md)]. Opsætningen er opdelt i to hovedopgaver som beskrevet i denne artikel:

1. I Microsoft Azure skal du konfigurere Universaludskrivning og tilføje de printere, du vil bruge i Business Central for at dele udskrivning. Gå til [dette afsnit](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Tilføj printerne fra printerdelinger i Universal udskrivning i [!INCLUDE[prod_short](includes/prod_short.md)]. Gå til [denne sektion](#add-printers-in-business-central-online) for at finde online eller [her](#add-printers-in-business-central-on-premises) for lokalt.

## <a name="prerequisites" />Forudsætninger

- Understøttede printere

  [!INCLUDE[prod_short](includes/prod_short.md)] understøtter de samme printere som Universaludskrivning, som enten kan være kompatible med Universaludskrivning eller ikke. Ikke-kompatible printere kan ikke kommunikere direkte med Universaludskrivning, så de kræver ekstra connectorsoftware, som leveres af Universaludskrivning. Nogle ældre printere understøttes muligvis ikke. 

- Universaludskrivning:

  - Et abonnement/en licens til Universaludskrivning for din organisation.

    Få mere at vide om [Universaludskrivning](/universal-print/fundamentals/universal-print-license).

  - Du har rollerne **Printerstyring** (eller Printer Manager) og **Global administrator** i Azure.

    Hvis du vil administrere Universaludskrivning, skal din konto omfatte rollerne **Printerstyring** (eller Printer Manager) og **Global administrator** i Azure AD. Disse roller er kun nødvendige for at administrere Universaludskrivning. Brugerne behøver ikke at konfigurere og bruge printerne fra [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online og i det lokale miljø:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 udgivelsesbølge 1 eller nyere.
  - Udvidelsen **Integration af Universaludskrivning** er installeret.

    Denne udvidelse udgives og installeres som standard som en del af [!INCLUDE[prod_short](includes/prod_short.md)] online og i det lokale miljø. Du kan kontrollere, om den er installeret på siden **Udvidelsesstyring**. Få mere at vide om at [installere og fjerne udvidelser i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] kun lokalt:
  - Godkendelse af typen Azure Active Directory (AD) eller NavUserPassword er konfigureret.
    > [!NOTE]
    >  Universal print Extension understøtter ikke service-to-service (S2S)-godkendelse. Den kræver, at en bruger er logget på for at sende udskriftsjob til Universal print service via Graph API.
  - Registrering som bruger af Business Central foregår i din Azure AD-lejer og [!INCLUDE[prod_short](includes/prod_short.md)].

    Ligesom andre Azure-tjenester, der fungerer sammen med [!INCLUDE[prod_short](includes/prod_short.md)], kræver Universaludskrivning en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Azure AD. Appregistreringen leverer godkendelses- og autorisationstjenester mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Universaludskrivning.

    Din installation bruger muligvis allerede en appregistrering for andre Azure-tjenester, f.eks. Power BI. Hvis det er tilfældet, skal du bruge den eksisterende appregistrering for Universaludskrivning i stedet for at tilføje en ny. Det eneste, du skal gøre, er i dette tilfælde at ændre appregistreringen, så den indeholder de relevante udskrivningstilladelser til Microsoft Graph API: **PrinterShare.ReadBasic.All**, **PrintJob.Create** og **PrintJob.ReadBasic.** 

    Hvis du vil registrere en app og angive de rette tilladelser, skal du følge den fremgangsmåde, der er beskrevet i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## <a name="set-up-universal-print-and-printers-in-microsoft-azure" />Konfigurere Universaludskrivning og printere i Microsoft Azure

Før du kan begynde at administrere printere for Universaludskrivning i Business Central, skal du udføre flere opgaver for at Universaludskrivning til at køre i Azure sammen med de printere, du vil bruge.

Du kan finde detaljerede instruktioner i konfigurationen i [Introduktion: Konfigurere Universaludskrivning](/universal-print/fundamentals/universal-print-getting-started) i dokumentationen til Universaludskrivning. Her er en oversigt over de trin, du skal udføre. De fleste af disse trin udføres på Azure-portalen.

1. Tildel licenser til Universaludskrivning til dig selv og andre brugere.

    Hvordan du tildeler licensen, afhænger af, om Universaludskrivning skal integreres i Business Central online eller i det lokale miljø.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] Online tildeler du licenser gennem Microsoft 365 Administration.

      Flere oplysninger i [Hjælp til Microsoft Administration - Tildele licenser til brugere](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø tildeler du licenser i din Azure-lejer via Azure-portalen.

      Flere oplysninger i [Azure Directory – Tildele eller fjerne licenser på Azure Active Directory-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installer connectoren for Universaludskrivning med henblik på registrering af printere, der ikke kan kommunikere direkte med Universaludskrivning.

    Installer connectoren for Universaludskrivning med henblik på registrering af printere, der ikke kan kommunikere direkte med Universaludskrivning. Flere oplysninger i [Installation af connectoren for Universaludskrivning](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrer dine printere i Universaludskrivning.

    Registrering af en printer gør Universaludskrivning opmærksom på printeren.

    - For printere, der kan kommunikere direkte med Universaludskrivning, skal du følge den fremgangsmåde, som producenten af printeren har leveret.

    - For andre printere skal du registrere printerne ved hjælp af connectoren for Universaludskrivning. 

      Få mere at vide om [printerregistrering](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Ændre printeregenskaber (valgfrit)

    Når en printer er registreret, kan du få vist og ændre printeregenskaberne, f.eks. standardindstillinger.

    Flere oplysninger i [Administrere printerindstillinger med den universelle udskrivningsportal](/universal-print/portal/configure-printer-settings).

5. Del printere med brugere.

    Alle printere, du vil bruge i [!INCLUDE[prod_short](includes/prod_short.md)], skal føjes til en *printerdeling* i Universaludskrivning. Alle brugere, som skal have adgang til printeren, skal tilføjes som medlem af printerdeling. Få mere at vide om [Dele en printer](/universal-print/portal/share-printers).

    > [!TIP]
    > Du kan altid tilføje eller fjerne brugere senere. Få mere at vide om [printertilladelser](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Aktiver dokumentkonvertering.

    Universaludskrivning gengiver indholdet til udskrivning i XPS-format. Nogle ældre printere på markedet understøtter ikke gengivelse af XPS-indhold&mdash;og i mange tilfælde kun PDF-format. Udskrivning til disse printere vil mislykkes, medmindre Universaludskrivning er konfigureret til at konvertere dokumenter til printerens understøttede format.

    Flere oplysninger i [Dokumentkonverteringsoversigt](/universal-print/portal/document-conversion).

Nu er du klar til at føje printerne til [!INCLUDE[prod_short](includes/prod_short.md)], konfigurere standardprintere for rapporter og udskrive.  

## <a name="add-printers-in-business-central-online" />Tilføj printere i Business central online

Når printere er konfigureret og delt i Universaludskrivning, er du klar til at tilføje dem i [!INCLUDE[prod_short](includes/prod_short.md)] til brug. Du kan tilføje printere for Universaludskrivning på to måder. Du kan tilføje printerne samlet eller hver for sig.

Tilføjelse af printere hver for sig gør det muligt installere den samme printer for Universaludskrivning i [!INCLUDE[prod_short](includes/prod_short.md)] mere end én gang. For hver tilføjet printer kan du derefter ændre udskriftsindstillingerne, f.eks. papirbakke, størrelse og retning. På den måde kan du konfigurere printere til forskellige rapporter og dokumenter ifølge deres særlige krav til udskrivningen.

> [!NOTE]
> Bruger du [!INCLUDE[prod_short](includes/prod_short.md)] lokalt? Hvis det er tilfældet, skal du gå til [næste afsnit](#add-printers-in-business-central-on-premises), første gang opsætningen er lidt anderledes.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Printerstyring**, vælg derefter det relaterede link.
2. Vælg **Universaludskrivning**, og vælg derefter en af følgende muligheder:

   - **Tilføj alle printere til Universaludskrivning** for at tilføje alle printere, som ikke allerede er tilføjet. Du kan bruge denne indstilling, selvom der allerede er tilføjet printere.
   - **Tilføj en printer for Universaludskrivning** for at tilføje en bestemt printer.  
3. Du skal blot følge vejledningen på skærmen.

    - Hvis du vælger **Tilføj alle printere for Universaludskrivning**, starter konfigurationen af **Tilføj printere for Universaludskrivning**. 

    - Hvis du vælger **Tilføj en printer for Universaludskrivning**, vises siden **Indstillinger for Universaludskrivning**. Udfyld feltet **Navn**, vælg **...** ud for feltet **Udskriftsdeling i Universaludskrivning** for at vælge printeren for Universaludskrivning. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Når der er tilføjet en printer, kan du få vist og ændre indstillingerne for den i **Printerstyring**. Du skal bare vælge printeren og derefter vælge **Rediger printerindstillinger**.

## <a name="add-printers-in-business-central-on-premises" />Tilføj printere i Business central lokalt

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Før en bruger kan tilføje eller bruge Universaludskrivnings Business central, skal de give adgang til Azure-tjenesterne, som bruges af Universaludskrivning, og give dem tilladelse til data og handlinger som f. eks.:

- Logge på og læse brugerprofil
- Læse grundlæggende oplysninger om udskriftsoplysninger
- Oprette udskriftsjob

Dette gøres typisk første gang, der oprettes forbindelse til den Azure-registrerede app, som bruges til Universaludskrivning. I Business central online gennemføres dette godkendelsesforløb uden brugerinput. Men Business Central lokalt fungerer anderledes. Det kræver, at du eller en anden bruger, der vil bruge Universaludskrivning, starter godkendelsesprocessen - normalt én gang. Den nemmeste metode er beskrevet i følgende trin. En mindre direkte måde er at oprette forbindelse til en anden integreret tjeneste, der bruger den samme Azure-registrerede app, f.eks. Power BI eller OneDrive. Denne opgave skal typisk kun udføres af en bruger én gang.

> [!NOTE]
> Hvis du er administrator, anbefales det, at du udfører denne opgave før andre brugere. Derefter skal du underrette brugerne om, hvem der skal bruge universaludskriftsprintere, når de skal gøre. Hvis den Azure-registrerede app til Universaludskrivning kræver administrator samtykke til API-tilladelser, er det nemmere, hvis du giver samtykke på vegne af organisationen. Du kan tildele administratorsamtykke fra Azure-portalen, eller når du udfører de trin, der følger efter. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time" />Tilslutte til Universaludskrivning for første gang

Gennemfør disse trin for at oprette forbindelse til den universaludskrivningstjeneste første gang.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Printerstyring**, vælg derefter det relaterede link.
2. Vælg **universaludskrivning** > **Tilføj alle universaludskrivningsprintere** for at starte assisteret opsætningsguide til **Tilføj universaludskrivningsprinter**.
3. Følg vejledningen på skærmen, indtil du kommer til siden AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS.

    <!--The AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Azure AD setup, checking your Universal Print license, and then adding the printers.-->

   ![Viser siden AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS](media/azure-ad-services-permissions.png "Viser siden AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS")

4. Vælg linket **Autoriserede Azure Services**.

   1. Hvis siden **Tilladelse anmodet** vises, skal du læse den omhyggeligt og vælge **Accepter** og fortsætte. Hvis du kører som administrator, kan du vælge **Samtykke på vegne af organisation**, hvis du vil have samtykke til alle brugere.

      ![Viser siden tilladelser til Azure-anmodning](media/azure-ad-permissions-requested.png "Siden med tilladelser til Azure-anmodning").

   2. Hvis du bliver bedt om det, skal du logge på med dit navn og din adgangskode.

5. Når godkendelsen er fuldført, vises siden **Tilføj universaludskrivningsprintere**. Vælg **Næste** > **Afslut** for at fuldføre opsætningen.

Når der er tilføjet en printer, kan du få vist og ændre indstillingerne for den i **Printerstyring**. Du skal bare vælge printeren og derefter vælge **Rediger printerindstillinger**.

Når du har fuldført første logon, kan du bruge de universelle udskrivningsprintere til at udskrive rapporter og andre udskriftsjob. Du kan få flere oplysninger i [Udskrive en rapport](ui-work-report.md#PrintReport). Hvis du vil tilføje, fjerne eller ændre en printer, skal du bare gå tilbage til siden **Udskriftsstyring** og vælge **Universaludskrivning**.

## <a name="common-problems-and-resolutions" />Almindelige problemer og løsninger

I dette afsnit skal du lære om de almindelige problemer, som brugere kan opleve, når du forsøger at installere eller bruge universaludskrivningsprintere.

### <a name="you-dont-have-access-to-the-printer-your-printer" />Du har ikke adgang til printeren \<your-printer\>.

Hvis en bruger får denne meddelelse, når du forsøger at udskrive et dokument på en universaludskrivningsprinter, kan det skyldes et af følgende forhold:

- Brugeren har ikke tildelt en universaludskrivningslicens til sin Microsoft 365- eller Azure-Active Directory-konto. 
- Brugeren er ikke tildelt printerdeling i Universaludskrivning.
- (Lokalt) Den Azure-app-registrering, der bruges til universaludskrivning, fungerer ikke eller er ændret for nylig siden den sidste gang, brugeren loggede på.
- (Lokalt) Brugeren er endnu ikke logget på Azure-registreret app til Universaludskrivnings-app og har godkendt for første gang.

## <a name="there-was-an-error-fetching-printers-shared-to-you" />Der opstod en fejl under hentning af printere, der er delt til dig.

Hvis en bruger får denne meddelelse, når du forsøger at tilføje en universaludskrivningsprinter fra siden **Printerstyring**, skyldes det typisk, at du endnu ikke har logget på Azure registreret app til Universaludskrivnings-app og har godkendt for første gang. 
<!--
### <a name="troubleshooting" />Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the" />You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer" />You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-50" />Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps" />Næste trin
[Konfiguration af standardprintere](ui-specify-printer-selection-reports.md).

## <a name="see-also" />Se også

[Oversigt over printere](admin-printer-setup-overview.md)  
[Konfigurere e-mailprintere](admin-printer-setup-email.md)
[Udskrive en rapport](ui-work-report.md#PrintReport)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Afvikle kørsler](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
