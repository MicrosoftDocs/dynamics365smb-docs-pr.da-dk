---
title: Åbner Business Central-filer i OneDrive
description: Få mere at vide om, hvordan du kan dele Business Central-data fra virksomheden OneDrive.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516417"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Åbning og deling af Business Central-filer i OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] gør det nemt at gemme, administrere og dele filer med andre personer via OneDrive for Business. På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke eller filer, der er vedhæftet til poster, finder du en **Åbn i OneDrive**- og **Dele**-handling.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger med rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger til vedhæftede filer":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Åbne i OneDrive

Funktionen **Åbne i OneDrive** kopierer filen til din OneDrive og åbner filen i online-programmer, f. eks. Excel online, Word online og PowerPoint online. 

<!--## Working with Different Types of Files-->

Når du vælger **Åbn i OneDrive**, identificerer [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word-og PowerPoint-filer og åbner dem i deres onlineprogrammer, dvs. Excel online, Word online og PowerPoint online. Du kan anmærke, redigere og samarbejde med andre uden at forlade browseren.

I forbindelse med andre populære filtyper, f. eks. PDF-filer, tekstfiler og billeder, viser OneDrive filvisninger, som tilbyder funktioner til udskrivning, deling og mere. Hvis en fil ikke kan vises i OneDrive, kan du blive bedt om at hente den.

## <a name="share"></a>Fordeling

**Del**-handlingen kopierer filen til din OneDrive, så du kan dele filen med andre personer og se, hvem du allerede har delt filen. Når du vælger handlingen **Del**, åbnes følgende side.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Dele fil i OneDrive":::

Du kan genkende siden, hvis du har kendskab til OneDrive. Du kan dele filen med to forskellige muligheder: **Send link**, og **Kopier link**.

- **Send hyperlink** kan du dele filer med bestemte personer. De personer, som du deler filen med, får en e-mail med et link til filen. Filen vises også i den **fælles** sektion af deres OneDrive. Start med at skrive e-mail-adresser eller kontaktpersonnavne i feltet **navn, gruppe eller e-mailadresse**.

- **Kopier hyperlink** kopierer et hyperlink til filen, OneDrive, så du kan bruge hyperlinket i andre adresser, f. eks Facebook, Twitter eller e-mails. 

Før du sender eller kopierer hyperlinket, skal du angive tilladelsen til den fil, som andre skal have. Du kan se den aktuelle indstilling under **Send hyperlink** og **Kopier**. I de fleste tilfælde vil det være **enhver, der har kæden til at åbne hyperlinket**, afhængigt af de indstillinger, der er angivet af administratoren. Hvis du vil ændre tilladelserne, skal du markere linket og foretage ændringer på siden med **Linkindstillinger**.

Delings funktionen i Business Central er baseret på OneDrive. Du kan finde flere oplysninger om deling og tilladelse i [Dele OneDrive-filer og mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Handlingen **Dele** er ikke tilgængelig i Business central-appen til mobilenheder.

## <a name="first-time-sign-in-from-business-central"></a>Log på første gang fra Business central

Når du bruger handlingen **Åbn i OneDrive** eller **Del** første gang, gør [!INCLUDE[prod_short](includes/prod_short.md)] følgende ting:

1. Åbner siden **Gennemse vilkår og betingelser**. Læs siden, og hvis du kan acceptere vilkårene og betingelserne, skal du vælge **Accepter** for at fortsætte.
2. Åbner siden **Vælg en konto**, vælg din konto, eller **brug en anden konto**, hvis du ikke kan se din egen, skal du angive brugernavn og adgangskode, når du bliver bedt om det.
3. Opretter en mappe med navnet [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
4. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen oprettes en anden mappe med samme navn som det firma, du arbejder i. Hvis du arbejder i mere end ét regnskab, oprettes der en mappe til det firma, du arbejder i, når du bruger handlingen **åbne i OneDrive** og **Del**. 
5. Placerer en kopi af den fil, du har valgt i mappen, og åbner derefter filen. Næste gang du bruger handlingen, kopieres og åbnes filen. 

## <a name="managing-multiple-copies-of-a-file"></a>Administrere flere kopier af en fil

Når du vælger **Åbn i OneDrive** eller **Del**, kopieres filen fra [!INCLUDE[prod_short](includes/prod_short.md)] til din mappe i OneDrive. Hvis du redigerer filen i OneDrive, vil kopierne af filen være anderledes. Hvis du vil opdatere [!INCLUDE[prod_short](includes/prod_short.md)] med den seneste fil, skal du fjerne den eksisterende fil fra [!INCLUDE[prod_short](includes/prod_short.md)] og derefter overføre den seneste kopi.

Desuden, når der allerede findes en fil med dette navn i OneDrive, angiver [!INCLUDE[prod_short](includes/prod_short.md)] at erstatte filen eller at beholde begge filer. Hvis du vælger at beholde begge filer, kopieres den nye fil til OneDrive og tildeles et filnavn med suffiksnummer, f. eks. "items (2).xlsx". Den oprindelige fil ændres ikke. 

Hvis du vælger at erstatte filen, føjes den nye fil til versionshistorikken for filen. Den oprindelige fil går ikke tabt, og du kan få vist eller gendanne tidligere versioner af filen. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Om din Business Central-mappe på OneDrive

Mappen og dens indhold er private, indtil du beslutter dig for at dele dem med andre. Du kan f.eks. beslutte at dele indhold med en eller flere af dine kolleger eller endda personer uden for organisationen. Du kan få adgang til OneDrive fra siden **Indstillinger** ved at klikke på hyperlinket i feltet **Skylager**. Du kan få flere oplysninger i [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Feltet Skylager i mine Mine indstillinger":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Se også
[Business Central og OneDrive-integration](across-onedrive-overview.md)  
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)