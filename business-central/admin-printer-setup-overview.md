---
title: Oversigt over printeropsætning og -styring
description: 'Få mere at vide om, hvad de forskellige printer muligheder i Business central'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview"></a><a name="printer-setup-and-management-overview"></a>Oversigt over printeropsætning og -styring

Udskrivning af dokumenter og rapporter fra [!INCLUDE[prod_short](includes/prod_short.md)] er en vigtig opgave for virksomhedsbrugere. Du vil typisk sende udskriftsjob direkte til en af organisationens printere - uanset hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-klient eller -app de bruger. Da [!INCLUDE[prod_short](includes/prod_short.md)] Online er en skytjeneste, kan den ikke nå direkte ud til lokale printere, der er tilsluttet brugernes enheder, men den kan oprette forbindelse til skyaktiverede printere.

## <a name="what-are-your-printer-possibilities-in-business-central"></a><a name="what-are-your-printer-possibilities-in-business-central"></a>Hvad er dine printer muligheder i Business central?

For at understøtte dine udskrivningsbehov tilbyder [!INCLUDE[prod_short](includes/prod_short.md)] følgende funktioner:

|Funktion|Beskrivelse|Webklient| Mobilapp|App til Teams|
|-------|-----------|----------|-----------|--------------|
|Universaludskrivning|Universaludskrivning er en printerstyringsløsning, der er tilgængelig som skytjeneste fra Microsoft. Med denne funktion kan du konfigurere printerne i Universaludskrivning og derefter registrere dem med henblik på brug i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funktion kræver et abonnement på Universaludskrivning og udvidelsen **Integration af universaludskrivning**.|![arbejder online.](media/check.png)|![arbejder online.](media/check.png)|![arbejder online](media/check.png)|
|Mailudskrift|Med denne funktion kan du konfigurere mailaktiverede printere. [!INCLUDE[prod_short](includes/prod_short.md)] sender derefter udskriftsjob til en printer ved hjælp af printerens mailadresse. Denne funktion kræver mailaktiverede printere og udvidelsen **Send til mail-printer**.|![arbejder online.](media/check.png)|![arbejder online](media/check.png)|![arbejder online](media/check.png)|
|Browserudskrivning|Udskriftsjob håndteres af udskrivningsfunktionen i brugerens browser. Hvis der ikke er installeret og konfigureret en cloudprinter, eller hvis der opstår fejl på en installeret printer, vil udskrivningen som standard benytte browserens udskriftsindstillinger. Feltet **Printer** på rapportanmodningssiden viser *(Håndteres af browseren)*.|![arbejder online](media/check.png)|||

Det meste af arbejdet med at konfigurere printere kan udføres fra siden **Printeradministration** i [!INCLUDE[prod_short](includes/prod_short.md)]. Selvom du har universelle udskriftsprintere, skal du muligvis også arbejde i Microsoft 365 Administrationscenter eller Azure-portalen.

> [!IMPORTANT]
> For Business central lokalt kræver universel udskrivning og e-mailudskrift at Azure Active Directory bruger (AD) eller NavUserPassword-godkendelse.

## <a name="custom-printer-extensions"></a><a name="custom-printer-extensions"></a>Brugerdefinerede printerudvidelser

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter andre brugerdefinerede printerudvidelser, der tilføjer endnu flere udskrivningsfunktioner. Så hvis der er installeret brugerdefinerede printerudvidelser, kan du muligvis medtage udskrivningsfunktioner, der ikke er beskrevet i denne artikel.

Hvis du er AL-udvikler og vil lære mere om, hvordan du opretter printerudvidelser, skal du gå til [udvikling af printerudvidelser i Business central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps"></a><a name="next-steps"></a>Næste trin

- [Konfigurere printere til Universaludskrivning](admin-printer-setup-universal-print.md)  
- [Konfigurere e-mailprintere](admin-printer-setup-email.md)  
- [Konfiguration af standardprintere](ui-specify-printer-selection-reports.md)
