---
title: Business Central og OneDrive for Business Integration
description: 'Du kan bruge OneDrive til Business til at gemme, administrere og dele filer, f.eks. rapporter eller vedhæftede filer. Hvis du har stavet det One Drive.'
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: null
ms.date: 02/28/2022
ms.author: jswymer
---

# Business Central og OneDrive for Business Integration

OneDrive for Business er en skylagringstjeneste, der er inkluderet i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] gør det nemt at gemme, administrere og dele filer med andre personer via OneDrive. Når der er en fil i din OneDrive, får du de omfattende samarbejdsoplevelser fra onlineversionerne af Microsoft-produkter, f.eks. Word, Excel og PowerPoint. Du kan f.eks. dele et Word-dokument, og så kan du og dine kolleger redigere det sammen i realtid. OneDrive giver dig også mulighed for at åbne andre filtyper, f.eks. PDF'er. 

## Kom i gang med OneDrive-funktioner

Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] online, har vi allerede skabt forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] online og OneDrive, så det er nemt at komme i gang. Det eneste krav er, at brugerne har åbnet OneDrive mindst én gang. Med [!INCLUDE[prod_short](includes/prod_short.md)] i det lokale miljø skal en administrator konfigurere forbindelsen, før du kan komme i gang. Få mere at vide i [Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md).

<!-- We've created the connection between [!INCLUDE[prod_short](includes/prod_short.md)] online and OneDrive, so it's easy to get started. The only requirement is that users have opened OneDrive at least one time. -->

### Åbne og dele i OneDrive

På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke eller filer, der er vedhæftet til poster, finder du en **Åbn i OneDrive**- og **Dele**-handling.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger med rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger til vedhæftede filer":::

|Vælg...|Til...|Se flere oplysninger...|
|---------|-----|----------------|
|Åbne i OneDrive|Kopier filen til en Business Central-mappe i OneDrive, og åbn filen.|[Åbn i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Fordeling|Kopier filen til din OneDrive, og del den med andre.|[Del i OneDrive](across-share-onedrive.md#share) |

### Gemme Excel-projektmapper og -rapportfiler i OneDrive

Når OneDrive-integration er konfigureret, vil et par andre velkendte funktioner automatisk bruge OneDrive til at gemme filer i stedet for at gemme filer på din enhed:

- Funktionen **Åbn i Excel** og **Rediger i Excel** på listesider kopierer automatisk Excel-filen til OneDrive og åbner den i Excel Online. Du kan finde flere oplysninger i [Vise og redigere i Excel](across-work-with-excel.md).
- Når du sender en rapport til en Excel- eller Word-fil, vil filen automatisk blive kopieret til OneDrive og derefter åbnes i Excel eller Word Online. Du kan få flere oplysninger i [Gemme en rapport i en fil](ui-work-report.md#saving-a-report-to-a-file).

Disse funktioner er ikke aktiveret som standard. Men som administrator kan du nemt slå dem til ved hjælp af **OneDrive-installationens** vejledning til assisteret opsætning.

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan også tilslutte det [!INCLUDE[prod_short](includes/prod_short.md)]-lokale miljø til OneDrive. Der er dog et par ting at gøre for at få det til at fungere. Du kan finde flere oplysninger i [Konfigurere Business Central lokalt](admin-onedrive-integration-onpremises.md).

## Se også

[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)  
