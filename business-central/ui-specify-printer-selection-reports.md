---
title: Konfiguration af printere
description: Få mere at vide om konfiguration af printere, som du kan bruge til rapporter og dokumenter.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 69c5ab889ae1fe98d50c04e31f47ecc28cc0e1b0
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985408"
---
# <a name="set-up-printers"></a>Installation af printere

Udskrivning af dokumenter og rapporter fra [!INCLUDE[prod_short](includes/prod_short.md)] er en vigtig opgave for virksomhedsbrugere. Brugere vil typisk sende udskriftsjob direkte til en af organisationens printere&mdash;uanset hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-klient eller -app de bruger. Da [!INCLUDE[prod_short](includes/prod_short.md)] Online er en skytjeneste, kan den ikke nå direkte ud til lokale printere, der er tilsluttet brugernes enheder, men den kan oprette forbindelse til skyaktiverede printere.

For at understøtte dine udskrivningsbehov tilbyder [!INCLUDE[prod_short](includes/prod_short.md)] følgende funktioner:

|Funktion|Description|Webklient| Mobilapp|App til Teams|
|-------|-----------|----------|-----------|--------------|
|Universaludskrivning|Universaludskrivning er en printerstyringsløsning, der er tilgængelig som skytjeneste fra Microsoft. Med denne funktion kan du konfigurere printerne i Universaludskrivning og derefter registrere dem med henblik på brug i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funktion kræver et abonnement på Universaludskrivning og udvidelsen **Integration af universaludskrivning**|![arbejder online](media/check.png)|![arbejder online](media/check.png)|![arbejder online](media/check.png)|
|Mailudskrift|Med denne funktion kan du konfigurere mailaktiverede printere. [!INCLUDE[prod_short](includes/prod_short.md)] sender derefter udskriftsjob til en printer ved hjælp af printerens mailadresse. Denne funktion kræver mailaktiverede printere og udvidelsen **Send til mail-printer**.|![arbejder online](media/check.png)|![arbejder online](media/check.png)|![arbejder online](media/check.png)|
|Browserudskrivning|Udskriftsjob håndteres af udskrivningsfunktionen i brugerens browser. Hvis der ikke er installeret og konfigureret en cloudprinter, eller hvis der opstår fejl på en installeret printer, vil udskrivningen som standard benytte browserens udskriftsindstillinger. Feltet **Printer** på rapportanmodningssiden viser *(Håndteres af browseren)*.|![arbejder online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] understøtter også brugerdefinerede printerudvidelser, der tilføjer endnu flere udskrivningsfunktioner. Så hvis der er installeret brugerdefinerede printerudvidelser, kan du muligvis medtage udskrivningsfunktioner, der ikke er beskrevet i denne artikel. 

## <a name="set-up-universal-print"></a>Konfiguration af Universaludskrivning

Universaludskrivning er en Microsoft 365-abonnementsbaseret tjeneste, der udelukkende kører på Microsoft Azure. Den giver dig centraliseret printerstyring via portalen for Universaludskrivning. [!INCLUDE[prod_short](includes/prod_short.md)] gør det muligt at konfigurere printere i Universaludskrivning for klientbrugere via udvidelsen **Integration af Universaludskrivning**.

![Konfiguration af Universaludskrivning](media/Universal-Print-arch.png)

Den komplette konfiguration kræver, at du arbejder i både Microsoft Azure ved hjælp af [Azure-portalen](https://posrtal.azure.com) og i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Understøttede printere

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter de samme printere som Universaludskrivning, som enten kan være kompatible med Universaludskrivning eller ikke. Ikke-kompatible printere kan ikke kommunikere direkte med Universaludskrivning, så de kræver ekstra connectorsoftware, som leveres af Universaludskrivning. Nogle ældre printere understøttes muligvis ikke. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Forudsætninger

**For [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 udgivelsesbølge 1 eller nyere
- Udvidelsen **Integration af Universaludskrivning** er installeret

    Denne udvidelse udgives og installeres som standard som en del af [!INCLUDE[prod_short](includes/prod_short.md)] online og i det lokale miljø.  Du kan kontrollere, om den er installeret på siden **Udvidelsesstyring**. Du kan finde flere oplysninger i [Installation og fjernelse af udvidelser i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø:
  - Godkendelse af typen Azure Active Directory (AD) eller NavUserPassword er konfigureret
  - Registrering som bruger af Business Central foregår i din Azure AD-lejer og [!INCLUDE[prod_short](includes/prod_short.md)]

      Ligesom andre Azure-tjenester, der fungerer sammen med [!INCLUDE[prod_short](includes/prod_short.md)], kræver Universaludskrivning en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Active Directory (Azure AD). Appregistreringen leverer godkendelses- og autorisationstjenester mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Universaludskrivning.

      Din installation bruger muligvis allerede en appregistrering for andre Azure-tjenester, f.eks. Power BI. Hvis det er tilfældet, skal du bruge den eksisterende appregistrering for Universaludskrivning i stedet for at tilføje en ny. Det eneste, du skal gøre, er i dette tilfælde at ændre appregistreringen, så den indeholder de relevante udskrivningstilladelser til Microsoft Graph API.

      Hvis du vil registrere en app og angive de rette tilladelser, skal du følge den fremgangsmåde, der er beskrevet i [Registrere et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**For Universaludskrivning**

- Et abonnement/en licens til Universaludskrivning for din organisation.

    Du kan finde flere oplysninger i [Få licens til Universaludskrivning](/universal-print/fundamentals/universal-print-license).

- Du har rollerne **Printerstyring** og **Global administrator** i Azure.

    Hvis du vil administrere Universaludskrivning, skal din konto omfatte rollerne **Printerstyring** og **Global administrator** i Azure AD. Disse roller er kun nødvendige for at administrere Universaludskrivning. Brugerne behøver ikke at bruge printerne fra [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Konfigurere Universaludskrivning og tilføje printere i Microsoft Azure

Før du kan begynde at administrere printere for Universaludskrivning i Business Central, skal du udføre flere opgaver for at Universaludskrivning til at køre i Azure sammen med de printere, du vil bruge.

Du kan finde detaljerede instruktioner i konfigurationen i [Introduktion: Konfigurere Universaludskrivning](https://docs.microsoft.com/universal-print/fundamentals/universal-print-getting-started) i dokumentationen til Universaludskrivning. Her er en oversigt over de trin, du skal udføre. De fleste af disse trin udføres på Azure-portalen.

1. Tildel licenser til Universaludskrivning til dig selv og andre brugere.

    Hvordan du tildeler licensen, afhænger af, om Universaludskrivning skal integreres i Business Central online eller i det lokale miljø.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] Online tildeler du licenser gennem Microsoft 365 Administration.

      Du kan finde flere oplysninger i [Hjælp til Microsoft Administration - Tildele licenser til brugere](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø tildeler du licenser i din Azure-lejer via Azure-portalen.

      Du kan finde flere oplysninger i [Azure Directory – Tildele eller fjerne licenser på Azure Active Directory-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installer connectoren for Universaludskrivning med henblik på registrering af printere, der ikke kan kommunikere direkte med Universaludskrivning.

    De fleste printere på markedet kan ikke kommunikere direkte med Universaludskrivning. Du skal installere connectoren for Universaludskrivning for disse printere. Du kan finde flere oplysninger i [Installation af connectoren for Universaludskrivning](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrer dine printere i Universaludskrivning.

    Registrering af en printer gør Universaludskrivning opmærksom på printeren.

    - For printere, der kan kommunikere direkte med Universaludskrivning, skal du følge den fremgangsmåde, som producenten af printeren har leveret.

    - For andre printere skal du registrere printerne ved hjælp af connectoren for Universaludskrivning. 

      Du kan finde flere oplysninger i [Printerregistrering](/universal-print-connector-printer-registration).

4. Ændre printeregenskaber (valgfrit)

    Når en printer er registreret, kan du få vist og ændre printeregenskaberne, f.eks. standardindstillinger.

    Du kan finde flere oplysninger i [Administrere metadataindstillinger for printer](/universal-print/fundamentals/universal-print-printer-property-settings).

5. Giv brugere tilladelse til printerne.

    Du kan finde flere oplysninger i [Printertilladelser](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).

6. Del printerne.

    Alle printere, du vil bruge i [!INCLUDE[prod_short](includes/prod_short.md)], skal deles i Universaludskrivning.

    Du kan finde flere oplysninger i [Dele en printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer).

7. Aktiver dokumentkonvertering.

    Universaludskrivning gengiver indholdet til udskrivning i XPS-format. Nogle ældre printere på markedet understøtter ikke gengivelse af XPS-indhold&mdash;og i mange tilfælde kun PDF-format. Udskrivning til disse printere vil mislykkes, medmindre Universaludskrivning er konfigureret til at konvertere dokumenter til printerens understøttede format.

    Du kan finde flere oplysninger i [Oversigt over dokumentkonvertering](/universal-print/fundamentals/universal-print-document-conversion).

    > [!TIP]
    > Hvis ingen af printerne kræver indholdsgengivelse i PDF-format, anbefales det, at du ikke aktiverer dokumentkonvertering, da det kan påvirke udskriftskvaliteten.

Nu er du klar til at føje printerne til [!INCLUDE[prod_short](includes/prod_short.md)], konfigurere standardprintere for rapporter og udskrive.  

### <a name="add-universal-printer-printers-to-business-central"></a>Føje printere for Universaludskrivning til Business Central

Når printere er konfigureret og delt i Universaludskrivning, er du klar til at bruge dem i Business Central. Du kan tilføje printere for Universaludskrivning på to måder. Du kan tilføje printerne samlet eller hver for sig.

Tilføjelse af printere hver for sig gør det muligt installere den samme printer for Universaludskrivning i Business Central mere end én gang. For hver tilføjet printer kan du derefter ændre udskriftsindstillingerne, f.eks. papirbakke, størrelse og retning. På den måde kan du konfigurere printere til forskellige rapporter og dokumenter ifølge deres særlige krav til udskrivningen.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printerstyring**, og vælg derefter det relaterede link.
2. Vælg **Universaludskrivning**, og vælg derefter en af følgende muligheder:

    - **Tilføj alle printere til Universaludskrivning** for at tilføje alle printere, som ikke allerede er tilføjet. Du kan bruge denne indstilling, selvom der allerede er tilføjet printere. 

    - **Tilføj en printer for Universaludskrivning** for at tilføje en bestemt printer.  
3. Du skal blot følge vejledningen på skærmen.

    - Hvis du vælger **Tilføj alle printere for Universaludskrivning**, starter konfigurationen af **Tilføj printere for Universaludskrivning**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Hvis du vælger **Tilføj en printer for Universaludskrivning**, vises siden **Indstillinger for Universaludskrivning**. Udfyld feltet **Navn**, vælg **...** ud for feltet **Udskriftsdeling i Universaludskrivning** for at vælge printeren for Universaludskrivning. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Disse handlinger kontrollerer din Azure AD-installation (i det lokale miljø), kontroller, at du har licens til Universaludskrivning og tilføjer til sidst printerne.

    > [!NOTE]
    > Hvis det er første gang, du opretter forbindelse til Universaludskrivning i det lokale miljø, vises siden AZURE ACTIVE DIRECTORY-TJENESTETILLADELSER, og du bliver bedt om at give dig samtykke til Azure-tjenester. Du behøver kun at give dit samtykke én gang.

Når der er tilføjet en printer, kan du få vist og ændre indstillingerne for den i **Printerstyring**. Du skal bare vælge printeren og derefter vælge **Rediger printerindstillinger**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Konfigurere mailudskrift

### <a name="prerequisites"></a>Forudsætninger

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 udgivelsesbølge 1 eller nyere
- Udvidelsen **Send til mailprinter** er installeret

    Denne udvidelse er installeret som standard. Du kan finde flere oplysninger om installation af udvidelser i 
- Mailfunktionaliteten er konfigureret.

   Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Tilføje en mailprinter

På siden **Printerstyring** vises de printere, der er konfigurerede i øjeblikket. Siden giver dig også adgang til siden **Indstillinger** for hver printer, hvor du kan redigere en eksisterende konfiguration eller installere en ny printer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printerstyring**, og vælg derefter det relaterede link.
2. Vælg **Mailudskrift**, og vælg derefter **Tilføj en mailprinter**.
3. Udfyld felterne på siden **Indstillinger for mailprinter** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du skal vælge den relevante papirstørrelse til en printer manuelt, da der ikke kan gemmes en lokal printer eller brugerindstillinger.
    >
    > Vær opmærksom på, at udvidelsen Mailprinter som standard er indstillet til papirformatet **A4**, som f.eks. ikke egner sig til USA.

### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Hvis du bruger udvidelsen Mailprinter, sendes alle eller nogle udskriftsjob til den mailadresse, der er konfigureret for printeren. Det anbefales på det kraftigste, at et entydigt mail-id kun knyttes til en printerenhed ved hjælp af hardwareproducentens officielle tjenester, f.eks. HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Træf alle nødvendige forholdsregler for at beskytte personlige oplysninger, herunder sikre, at mailudskriftsløsningen har korrekt konfigurerede tilladelser, indstillinger for beskyttelse af personlige oplysninger og opbevaringspolitikker. Det er dit ansvar at angive en korrekt, bekræftet og aktiv mailadresse. Du kan finde flere oplysninger i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Konfiguration af standardprintere

Du kan konfigurere, hvilke printere der skal bruges som standard til udskriftsjob, på flere måder. En standardprinter er nyttig, hvis du arbejder med forskellige rapporter, som kræver forskellige printere på grund af deres placering i virksomheden eller deres udskrivningsmuligheder.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Angive en printer som standardprinter for alle udskriftsjob

På siden **Printerstyring** kan du konfigurere en printer som standardprinter for alle udskriftsjob. Du kan kun angive printeren som standardprinter for dig eller for alle brugere.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printerstyring**, og vælg derefter det relaterede link.

    > [!TIP]
    > Du kan også åbne siden **Printerstyring** på siden **Printervalg** ved at vælge **Printerstyring**.  
2. På siden **Printerstyring** skal du vælge en printer på listen, vælge **Administrer** og derefter vælge **Angiv som min standardprinter** eller **Angiv som standardprinter til alle brugere**.

> [!NOTE]
> Hvis du angiver en standardprinter fra **Printerstyring**, tilføjes der en post i **Printervalg**.

### <a name="set-a-default-printer-for-specific-reports"></a>Angive en standardprinter for specifikke rapporter

På siden **Printervalg** kan du angive den printer, som en rapport skal bruge som standard. Standardprintere er angivet på basis af brugerkonti. Du kan angive en standardprinter udelukkende for dig selv, en anden bruger eller alle brugere.

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø kan siden **Printervalg** kun bruges til cloudprintere, der er defineret af printerudvidelser som f.eks. printere for Mailudskrift og Universaludskrivning. Den kan ikke bruges til lokale printere.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printervalg**, og vælg derefter det relaterede link. Du kan i stedet vælge en printer på siden **Printerstyring** og derefter vælge handlingen **Printervalg**.
2. Vælg handlingen **Ny** for at tilføje et printervalg til en bestemt rapport.
3. Udfyld felterne efter behov.

Den angivne rapport er nu indstillet til at blive udskrevet på den valgte printer som standard.

> [!NOTE]
> Når du udskriver den pågældende rapport, kan du vælge en anden ved at bruge feltet **Udskriv** på anmodningssiden.

> [!NOTE]
> Hvis du ikke angiver en rapport for en bestemt printer på siden **Printervalg**, udskrives den på virksomhedens standardprinter i henhold til definitionen på siden **Printerstyring**.

Du eller administratoren kan også bruge siden **Printervalg** til at angive andre variationer af udskrivningen for brugere og rapporter. I følgende tabel beskrives den kombination af værdier, som skal bruges til at angive forskellige printeropsætninger for en rapport.

|Hvis du vil                                                 |Angiv følgende værdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Udskriv en rapport til en bestemt printer for alle brugere |Angiv værdier i felterne **Rapport-id** og **Printernavn**, og lad feltet **Bruger-id** stå tomt.|
|Udskriv alle rapport til en bestemt printer for en bestemt bruger|Angiv værdier i felterne **Bruger-id** og **Printernavn**, og lad feltet **Rapport-id** stå tomt. Denne post fungerer på samme måde som handlingen **Angiv som min standardprinter** på siden **Udskriftsstyring**.|
|Angive standardprinteren for alle rapporter for alle brugere|Angiv en værdi i feltet **Printernavn**, og lad felterne **Bruger-id** og **Rapport-id** stå tomme. Denne post fungerer på samme måde som handlingen **Angiv som standardprinter til alle brugere** på siden **Udskriftsstyring**.|
|Udskriv en bestemt rapport til brugerens standardprinter|Angiv en værdi i feltet **Rapport-id**, og lad felterne **Printernavn** og **Bruger-id** stå tomme.|
|Udskriv en bestemt rapport til en bestemt printer for en bestemt bruger|Angiv værdier i alle tre felter.|

> [!NOTE]
> Mere bestemte printervalg tilsidesætter mere generelle printervalg. Et printervalg, der har værdier i felterne **Bruger-id**, **Rapport-id** og **Printernavn**, har f.eks. højere prioritet end et printervalg, hvor der ikke er angivet værdier i felterne **Bruger-ID** eller **Rapport-ID**.

### <a name="sizing-print-jobs"></a>Ændring størrelsen på udskriftsjob

Cloud-udskrivning er udviklet til dokumenter med en rimelig størrelse. De fleste cloud-tjenester, herunder PrintNode og HP ePrint, har en begrænsning på 10 MB pr. job. Hvis du skal udskrive større rapporter, skal du muligvis opdele dem i flere udskrifter.

## <a name="see-also"></a>Se også

[Udskrive en rapport](ui-work-report.md#PrintReport)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Afvikle kørsler](ui-how-run-batch-jobs.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]