---
title: Konfigurere e-mailprintere
description: Beskrivelse
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers"></a><a name="set-up-email-printers"></a><a name="set-up-email-printers"></a>Konfigurere e-mailprintere

I denne artikel forklares det, hvordan du konfigurerer e-mailaktiverede printere i [!INCLUDE[prod_short](includes/prod_short.md)]. Med disse printere sender [!INCLUDE[prod_short](includes/prod_short.md)] udskriftsjob til printeren ved hjælp af printerens mailadresse.

> [!TIP]
> Hvis du vil have oplysninger om andre printermuligheder, skal du gå til [Oversigt over printerstyring](admin-printer-setup-overview.md). 

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 udgivelsesbølge 1 eller nyere
- Udvidelsen **Send til mailprinter** er installeret

    Denne udvidelse er installeret som standard. Få mere at vide om at installere udvidelser i [installere og afinstallere udvidelser i Business Central](ui-extensions-install-uninstall.md).
- Mailfunktionaliteten er konfigureret.

   Flere oplysninger i [Konfigurer e-mail](admin-how-setup-email.md).

## <a name="add-an-email-printer"></a><a name="add-an-email-printer"></a><a name="add-an-email-printer"></a>Tilføj en mailprinter.

På siden **Printerstyring** vises de printere, der er konfigurerede i øjeblikket. Siden giver dig også adgang til siden **Indstillinger** for hver printer, hvor du kan redigere en eksisterende konfiguration eller installere en ny printer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Printerstyring**, vælg derefter det relaterede link.
2. Vælg **Mailudskrift**, og vælg derefter **Tilføj en mailprinter**.
3. Udfyld felterne på siden **Indstillinger for mailprinter** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du skal vælge den relevante papirstørrelse til en printer manuelt, da der ikke kan gemmes en lokal printer eller brugerindstillinger.
    >
    > Vær opmærksom på, at udvidelsen E-mailprinter som standard er indstillet til **A4**-papirformat, som ikke passer til f.eks. USA.

## <a name="privacy-notice"></a><a name="privacy-notice"></a><a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Hvis du bruger udvidelsen Mailprinter, sendes alle eller nogle udskriftsjob til den mailadresse, der er konfigureret for printeren. Det anbefales på det kraftigste, at et entydigt mail-id kun knyttes til en printerenhed ved hjælp af hardwareproducentens officielle tjenester, f.eks. HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Træf alle nødvendige forholdsregler for at beskytte personlige oplysninger, herunder sikre, at mailudskriftsløsningen har korrekt konfigurerede tilladelser, indstillinger for beskyttelse af personlige oplysninger og opbevaringspolitikker. Det er dit ansvar at angive en korrekt, bekræftet og aktiv mailadresse. Få mere at vide om [Microsoft erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps"></a><a name="next-steps"></a><a name="next-steps"></a>Næste trin

[Konfiguration af standardprintere](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Oversigt over projektadministration](admin-printer-setup-overview.md)  
[Konfigurere universelle udskriftsprintere](admin-printer-setup-universal-print.md)
[Udskrive en rapport](ui-work-report.md#PrintReport)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Afvikle kørsler](ui-how-run-batch-jobs.md)  
