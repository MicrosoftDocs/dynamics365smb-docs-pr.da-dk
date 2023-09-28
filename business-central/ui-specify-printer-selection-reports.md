---
title: Angive en standardprinter
description: 'Få mere at vide om forskellige måder at konfigurere, hvilke printere der skal bruges som standard til udskriftsjob.'
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer"></a><a name="default"></a>Angive en standardprinter

Når der er oprettet printere i Business central, kan du angive, hvilken printer du vil bruge som standard. Du kan konfigurere, hvilke printere der skal bruges som standard til rapporter og andre udskriftsjobs. En standardprinter er nyttig, hvis du arbejder med forskellige rapporter, som kræver forskellige printere på grund af deres placering i virksomheden eller deres udskrivningsmuligheder.

> [!IMPORTANT]
> De eneste printere, som du kan angive som standard, er **Microsoft-udskrift til PDF** og cloudprintere, der allerede er indstillet til brug i Business central, f.eks. mailprintere og universelle udskriftsprintere. Cloud-printere konfigureres typisk af en administrator. Du kan finde flere oplysninger i [Printeropsætning og styring](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Angive en printer som standardprinter for alle udskriftsjob

På siden **Printerstyring** kan du konfigurere en printer som standardprinter for alle udskriftsjob. Du kan kun angive printeren som standardprinter for dig eller for alle brugere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Printerstyring**, vælg derefter det relaterede link.

    > [!TIP]
    > Du kan også åbne siden **Printerstyring** på siden **Printervalg** ved at vælge **Printerstyring**.  
2. På siden **Printerstyring** skal du vælge en printer på listen, vælge **Administrer** og derefter vælge **Angiv som min standardprinter** eller **Angiv som standardprinter til alle brugere**.

> [!NOTE]
> Hvis du angiver en standardprinter fra **Printerstyring**, tilføjes der en post i **Printervalg**.

## <a name="set-a-default-printer-for-specific-reports"></a>Angive en standardprinter for specifikke rapporter

På siden **Printervalg** kan du angive den printer, som en rapport skal bruge som standard. Standardprintere er angivet på basis af brugerkonti. Du kan angive en standardprinter udelukkende for dig selv, en anden bruger eller alle brugere.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Printervalg**, og vælg derefter det relaterede link. Du kan også vælge en printer på siden **Printerstyring** og derefter vælge handlingen **Printervalg**.
2. Vælg handlingen **Ny** for at tilføje et printervalg til en bestemt rapport.
3. Udfyld felterne efter behov.

Den angivne rapport er nu indstillet til at blive udskrevet på den valgte printer som standard.

> [!NOTE]
> Når du udskriver den pågældende rapport, kan du vælge en anden ved at bruge feltet **Udskriv** på rapportanmodningssiden.

> [!NOTE]
> Hvis du ikke angiver en rapport for en bestemt printer på siden **Printervalg**, udskrives den på virksomhedens standardprinter i henhold til definitionen på siden **Printerstyring**.

Du eller administratoren kan også bruge siden **Printervalg** til at angive andre variationer af udskrivningen for brugere og rapporter. I følgende tabel beskrives den kombination af værdier, som skal bruges til at angive forskellige printeropsætninger for en rapport.

|Til                                                 |Angiv følgende værdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Udskriv en rapport til en bestemt printer for alle brugere |Angiv værdier i felterne **Rapport-id** og **Printernavn**, og lad feltet **Bruger-id** stå tomt.|
|Udskriv alle rapport til en bestemt printer for en bestemt bruger|Angiv værdier i felterne **Bruger-id** og **Printernavn**, og lad feltet **Rapport-id** stå tomt. Denne post fungerer på samme måde som handlingen **Angiv som min standardprinter** på siden **Udskriftsstyring**.|
|Angive standardprinteren for alle rapporter for alle brugere|Angiv en værdi i feltet **Printernavn**, og lad felterne **Bruger-id** og **Rapport-id** stå tomme. Denne post fungerer på samme måde som handlingen **Angiv som standardprinter til alle brugere** på siden **Udskriftsstyring**.|
|Udskriv en bestemt rapport til brugerens standardprinter|Angiv en værdi i feltet **Rapport-id**, og lad felterne **Printernavn** og **Bruger-id** stå tomme.|
|Udskriv en bestemt rapport til en bestemt printer for en bestemt bruger|Angiv værdier i alle tre felter.|

> [!NOTE]
> Mere bestemte printervalg tilsidesætter mere generelle printervalg. Et printervalg, der har værdier i felterne **Bruger-id**, **Rapport-id**og **Printernavn**, har f.eks. højere prioritet end et printervalg, hvor der ikke er angivet værdier i felterne **Bruger-ID** eller **Rapport-ID**.

## <a name="choosing-the-printer-when-running-a-report"></a>Vælge printeren, når en rapport køres

I stedet for at bruge standardprinteren, når du kører en rapport, kan du tilsidesætte denne indstilling fra anmodningssiden. Du skal blot vælge den printer, du vil bruge til denne aktivering af rapporten, i rullemenuen **Printer**.

## <a name="sizing-print-jobs"></a>Ændring af udskriftsjob

Cloud-udskrivning er udviklet til dokumenter med en rimelig størrelse. De fleste cloud-tjenester, herunder PrintNode og HP ePrint, har en begrænsning på 10 MB pr. job. Hvis du skal udskrive større rapporter, skal du muligvis opdele dem i flere udskrifter.

## <a name="see-also"></a>Se også

[Printerstyring](admin-printer-setup-overview.md)  
[Konfigurere printere til Universaludskrivning](admin-printer-setup-universal-print.md)  
[Konfigurere e-mailprintere](admin-printer-setup-email.md)  
[Udskrive en rapport](ui-work-report.md#PrintReport)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Afvikle kørsler](ui-how-run-batch-jobs.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
