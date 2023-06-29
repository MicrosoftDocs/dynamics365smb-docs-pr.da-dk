---
title: Dele og eksportere rapporter med rapportindbakken
description: 'Brug siden indbakke for rapport til at downloade, dele og eksportere rapporter i Business central.'
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: a-reishima
---
# <a name="share-and-export-reports-with-the-report-inbox"></a><a name="share-and-export-reports-with-the-report-inbox"></a>Dele og eksportere rapporter med rapportindbakken

**rapportindbakke**-siden viser planlagte rapporter, der er genereret af brugeren i [!INCLUDE[prod_short](includes/prod_short.md)], og den kan kun bruges til at få adgang til de genererede rapporter, men også til at dele og åbne filerne i OneDrive for Business.

> [!TIP]
> Følgende handlinger er også tilgængelige i **rapportindbakke** i rollecenter. Hvis delen ikke vises i brugergrænsefladen, skal du lære, hvordan du tilpasser dit rollecenter her: [Tilpas arbejdsområdet](ui-personalization-user.md).

## <a name="download-generated-reports"></a><a name="download-generated-reports"></a>Download genererede rapporter

Hvis du vil gemme tidligere rapporter, skal du åbne siden **rapportindbakke** ved at benytte følgende fremgangsmåde:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Rapportindbakke**, vælg derefter det relaterede link.  
2. Vælg den ønskede rapport på siden **rapportindbakke**.

> [!NOTE]
> Siden viser ikke tidligere rapporter, der er oprettet ved hjælp af handlingen **Udskriv**, eller som gemmes som en fil i menuen **Rapporter**.
>
> De genererede filer gemmes i det format, der er defineret ved planlægning af rapporten, og kan ændres på siden **Opgavekøposter** sammen med gentagelsen og andre indstillinger. Få mere at vide om, hvordan du ændrer formatet for rapportfilen og angiver yderligere indstillinger på [Administrer planlagte, tilbagevendende rapporter](ui-work-report.md#manage-scheduled-recurring-reports).

## <a name="open-generated-reports-in-onedrive"></a><a name="open-generated-reports-in-onedrive"></a>Åbne genererede rapporter i OneDrive

Hvis du vil eksportere rapportfilen til Microsoft OneDrive for Business, skal du vælge rapporten på siden **Rapportindbakke** og vælge feltet **Åbn i OneDrive**-handlingen. Rapporten kopieres derefter til [!INCLUDE[prod_short](includes/prod_short.md)]-mappen i OneDrive og åbnes i et nyt browservindue, hvor du kan udskrive og administrere dokumentfilen.

> [!IMPORTANT]
>
> Rapporter, der er indstillet til at udløbe på siden **Planlæg en rapport**, og kopieres til OneDrive, fjernes ikke automatisk fra den delte mappe.

## <a name="share-scheduled-reports"></a><a name="share-scheduled-reports"></a>Dele planlagte rapporter

Det er også muligt at dele rapporter med samarbejdspartnere på siden **Rapportindbakke**. Vælg rapporten og vælg handlingen **Del**. På siden **Send hyperlink** skal du vælge, hvem der må åbne filen, definere redigering af tilladelser og derefter vælge **Send** for at sende et link for at få adgang til den gemte rapport.

> [!NOTE]
> Hvis du vil vide mere om OneDrive-integration og funktioner på [!INCLUDE[prod_short](includes/prod_short.md)], herunder indstilling af førstegangsinstallation og-parametre, der omhandler konflikter mellem filnavne, skal du læse artiklen [åbning og deling af filer i OneDrive](across-share-onedrive.md).
>
> Hvis du bruger handlingen **Del**, bliver den genererede rapportfil kun tilgængelig til andre brugere på OneDrive til Business, og den planlagte rapport vises ikke i **Rapportindbakken**.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/paths/build-reports/).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Køre og udskrive rapporter](ui-work-report.md)  
[Tilgængelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Brug rapporter i dagligt arbejde](reports-use-reports.md)  
[Oversigt over Business Intelligence og rapportering](reports-bi-reporting.md)  
[Installation af printere](ui-specify-printer-selection-reports.md)  
[Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentlayout](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive-integration](across-onedrive-overview.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
