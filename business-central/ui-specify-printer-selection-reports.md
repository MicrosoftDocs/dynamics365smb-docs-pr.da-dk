---
title: Oprette rapporter, der skal udskrives på bestemte printere | Microsoft Docs
description: Få mere at vide om, hvordan du angiver en printer til en rapport og bruger siden Printervalg.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/17/2020
ms.author: sgroespe
ms.openlocfilehash: dbfdb22447f20b4e4b811dc40cf892d9b971dc77
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3272082"
---
# <a name="set-up-printers"></a>Installation af printere
Da [!INCLUDE[prodshort](includes/prodshort.md)] er en cloud-tjeneste, kan den ikke nå lokale printere med forbindelse til brugernes maskiner. Men den kan oprette forbindelse til cloud-kompatible printere. I den generelle version af [!INCLUDE[prodshort](includes/prodshort.md)] er der installeret en cloud-printer med navnet **Mailprinter** som en udvidelse, og den er klar til brug efter den første installation.

Hvis der ikke er installeret og konfigureret en cloud-printer, eller hvis der opstår fejl på en installeret printer, vil udskrivningen som standard benytte browserens udskriftsindstillinger. Dette angives med denne værdi i feltet **Printer** på rapportanmodningssiden: *(ingen, håndteres af browseren)*.

På siden **Printerstyring** kan du se de printere, der er konfigurerede. Når du har installeret en eller flere printere, kan du åbne siden **Printervalg** og definere på din brugerkonto, hvilke specifikke rapporter der skal udskrives på hvilken printer.

Når en printer er konfigureret og knyttet til bestemte rapporter, kan du udskrive en rapport ved at trykke på knappen **Udskriv** på rapport anmodningssiden. Du kan få flere oplysninger [Udskrive en rapport](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Ændring størrelsen på udskriftsjob
Cloud-udskrivning er udviklet til dokumenter med en rimelig størrelse. De fleste cloud-tjenester, herunder PrintNode og HP ePrint, har en begrænsning på 10 MB pr. job. Hvis du skal udskrive større rapporter, skal du muligvis opdele dem i flere udskrifter.

## <a name="to-set-up-a-printer"></a>Sådan installerer du en printer
På siden **Printerstyring** kan du se de printere, der er installeret, og du kan få adgang til siden med **Indstillinger** for hver enkelt printer for at redigere en eksisterende opsætning eller installere en ny printer.

Følgende fremgangsmåde beskriver, hvordan du konfigurerer den eksisterende **Mailprinter**, som er en udvidelse, der er installeret i forvejen.

> [!NOTE]
> Mailfunktionen skal være konfigureret, før du kan bruge mailudskrivning. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printerstyring**, og vælg derefter det relaterede link.
2. Markér linjen for **Mailprinter**-printeren, og vælg derefter handlingen **Rediger printerindstillinger**.
3. På siden **Indstillinger** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du skal vælge den relevante papirstørrelse til en printer manuelt, da der ikke kan gemmes en lokal printer eller brugerindstillinger.
    >
    > Vær opmærksom på, at udvidelsen Mailprinter som standard er indstillet til **A4**-papirformat, som ikke passer til f.eks. USA.
4. Du kan vælge en standardprinter på siden **Printerstyring** ved at vælge **Angiv som min standardprinter**.

### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Hvis du bruger udvidelsen Mailprinter, sendes alle eller nogle udskriftsjob til den mailadresse, du har angivet under konfigurationen af printeren. Det anbefales på det kraftigste, at et entydigt mail-ID kun bindes til en printerenhed ved hjælp af hardwareproducentens officielle tjenester, f. eks. HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Du skal træffe alle de nødvendige forholdsregler for beskyttelse af personlige oplysninger, herunder sørge for, at mail-udskriftsløsningen har korrekt konfigurerede tilladelser, indstillinger for beskyttelse af personlige oplysninger og opbevaringspolitikker. Det er dit ansvar at angive en korrekt, bekræftet og aktiv mailadresse. Du kan finde flere oplysninger i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Sådan vælger du, hvilke printere der skal udskrives hvilke rapporter
På siden **Printervalg** kan du angive på din brugerkonto, hvilke rapporter der skal udskrives med hvilken printer. Dette er nyttigt, hvis du arbejder med forskellige rapporter, som kræver forskellige printere på grund af deres placering i virksomheden eller deres udskrivningsmuligheder.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Printervalg**, og vælg derefter det relaterede link. Du kan også vælge en printer på siden **Printerstyring** og derefter vælge handlingen **Printervalg**.
2. Vælg handlingen **Ny** for at tilføje et printervalg til en bestemt rapport.
3. Udfyld felterne efter behov.

Den angivne rapport er nu indstillet til at blive udskrevet på den valgte printer som standard.

> [!NOTE]
> Når du udskriver den pågældende rapport, kan du tilsidesætte denne opsætning ved at vælge en anden printer på anmodningssiden **Udskriftsindstillinger**.

> [!NOTE]
> Hvis du ikke angiver en rapport for en bestemt printer på siden **Printervalg**, udskrives den på virksomhedens standardprinter i henhold til definitionen på siden **Printerstyring**.

Du eller administratoren kan også bruge siden **Printervalg** til at angive andre variationer af udskrivningen for brugere og rapporter. I følgende tabel beskrives den kombination af værdier, som skal bruges til at angive forskellige printeropsætninger for en rapport.

|Hvis du vil                                                 |Angiv følgende værdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Udskriv en rapport til en bestemt printer for alle brugere |Angiv værdier i felterne **Rapport-id** og **Printernavn**, og lad feltet **Bruger-id** stå tomt.|
|Udskriv alle rapport til en bestemt printer for en bestemt bruger|Angiv værdier i felterne **Bruger-id** og **Printernavn**, og lad feltet **Rapport-id** stå tomt.|
|Angiv standardprinteren for alle rapporter|Angiv en værdi i feltet **Printernavn**, og lad felterne **Bruger-id** og **Rapport-id** stå tomme.|
|Udskriv en bestemt rapport til brugerens standardprinter|Angiv en værdi i feltet **Rapport-id**, og lad felterne **Printernavn** og **Bruger-id** stå tomme.|
|Udskriv en bestemt rapport til en bestemt printer for en bestemt bruger|Angiv værdier i alle tre felter.|

> [!NOTE]
> Mere bestemte printervalg tilsidesætter mere generelle printervalg. Et printervalg, der har værdier i felterne **Bruger-id**, **Rapport-id**og **Printernavn**, har f. eks. højere prioritet end et printervalg, hvor der ikke er angivet værdier i felterne **Bruger-ID** eller **Rapport-ID**.

## <a name="see-also"></a>Se også
[Udskrive en rapport](ui-work-report.md#PrintReport)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Afvikle kørsler](ui-how-run-batch-jobs.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
