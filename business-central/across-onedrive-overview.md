---
title: Business Central og OneDrive for Business Integration
description: Du kan bruge OneDrive til Business til at gemme, administrere og dele filer, f.eks. rapporter eller vedhæftede filer.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: 8965fe1c0f04c3b12fef984e71b7f2643f7f11c2
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012571"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Business Central og OneDrive for Business Integration
OneDrive for Business er en skylagringstjeneste, der er inkluderet i Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] gør det nemt at gemme, administrere og dele filer med andre personer via OneDrive. Når der er en fil i din OneDrive, kan du nyde de omfattende samarbejdsoplevelser fra onlineversionerne af Microsoft-produkter, f.eks. Word, Excel og PowerPoint. Du kan f.eks. dele et Word-dokument, og så kan du og dine kolleger redigere det sammen i realtid. OneDrive giver dig også mulighed for at åbne andre filtyper, f.eks. PDF'er. 

## <a name="getting-started"></a>Introduktion
Vi har skabt forbindelsen mellem [!INCLUDE[prod_short](includes/prod_short.md)] online og OneDrive, så det er nemt at komme i gang. Det eneste krav er, at brugerne har åbnet OneDrive mindst én gang. 

På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke eller filer, der er vedhæftet til poster, finder du en **Åbn i OneDrive**-handling.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="Åbn i OneDrive-handlingen":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Dele vedhæftede filer i OneDrive":::

Når du bruger handlingen **Åbn i OneDrive** første gang, gør [!INCLUDE[prod_short](includes/prod_short.md)] følgende i OneDrive:

1. Opretter en mappe med navnet [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen oprettes en anden mappe med samme navn som det firma, du arbejder i. Hvis du arbejder i mere end ét regnskab, oprettes der en mappe til det firma, du arbejder i, når du bruger handlingen **Åbn i OneDrive**. 
3. Placerer en kopi af den fil, du har valgt i mappen, og åbner derefter filen. Næste gang du bruger handlingen, kopieres og åbnes filen. 

Mappen og dens indhold er private, indtil du beslutter dig for at dele dem med andre. Du kan f.eks. beslutte at dele indhold med en eller flere af dine kolleger eller endda personer uden for organisationen. Du kan få flere oplysninger i [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Du kan også tilslutte det [!INCLUDE[prod_short](includes/prod_short.md)]-lokale miljø til OneDrive. Der er dog et par ting at gøre for at få det til at fungere. Du kan finde flere oplysninger i [Tilpasning af Business Central i det lokale miljø](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Se også
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[Åbner Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)