---
title: Business Central og OneDrive for Business Integration
description: Du kan bruge OneDrive til Business til at gemme, administrere og dele filer, f.eks. rapporter eller vedhæftede filer. Hvis du har stavet det One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 06adf2a30a7487fa3bc66e1aebec42e6c55184e2
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227414"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive for Business Integration

OneDrive for Business er en skylagringstjeneste, der er inkluderet i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] gør det nemt at gemme, administrere og dele filer med andre personer via OneDrive. Når der er en fil i din OneDrive, kan du nyde de omfattende samarbejdsoplevelser fra onlineversionerne af Microsoft-produkter, f.eks. Word, Excel og PowerPoint. Du kan f.eks. dele et Word-dokument, og så kan du og dine kolleger redigere det sammen i realtid. OneDrive giver dig også mulighed for at åbne andre filtyper, f.eks. PDF'er. 

## <a name="get-started"></a>Kom i gang

Vi har skabt forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] online og OneDrive, så det er nemt at komme i gang. Det eneste krav er, at brugerne har åbnet OneDrive mindst én gang. 

På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke eller filer, der er vedhæftet til poster, finder du en **Åbn i OneDrive**- og **Dele**-handling.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger med rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger til vedhæftede filer":::

|Vælg...|Til...|Se flere oplysninger...|
|---------|-----|----------------|
|Åbne i OneDrive|Kopier filen til en Business Central-mappe i OneDrive, og åbn filen.|[Åbn i OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Fordeling|Kopier filen til din OneDrive, og del den med andre.|[Del i OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> Du kan også tilslutte det [!INCLUDE[prod_short](includes/prod_short.md)]-lokale miljø til OneDrive. Der er dog et par ting at gøre for at få det til at fungere. Du kan finde flere oplysninger i [Tilpasning af Business Central i det lokale miljø](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Se også

[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)