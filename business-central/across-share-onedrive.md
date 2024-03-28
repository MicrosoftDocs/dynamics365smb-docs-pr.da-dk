---
title: Åbner Business Central-filer i OneDrive
description: 'Få mere at vide om, hvordan du kan dele Business Central-data fra virksomheden OneDrive.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Åbning og deling af Business Central-filer i Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] gør det nemt at gemme, administrere og dele filer med andre personer via Microsoft OneDrive for Business. På de fleste sider, hvor filer er tilgængelige, som f.eks. Rapportindbakke, eller når filer er vedhæftet poster, finder du **Åbn i OneDrive**- og **Del**-handlinger.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger med rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingerne Åbn OneDrive, og del handlinger til vedhæftede filer":::


## Åbne i OneDrive

Handlingen **Åbn i OneDrive** kopierer filen til din OneDrive og åbner filen i et program som f.eks. Microsoft Excel online, Microsoft Word online eller Microsoft PowerPoint online. 

<!--## Working with different types of files-->

Når du vælger **Åbn i OneDrive**, identificerer [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word-og PowerPoint-filer og åbner dem i deres onlineprogrammer, dvs. Excel online, Word online og PowerPoint online. 

Du kan bruge onlineversioner af disse programmer til at anmærke, redigere og samarbejde med andre uden at forlade browseren.

I forbindelse med andre populære filtyper, f. eks. PDF-filer, tekstfiler og billeder, viser OneDrive filvisninger, som tilbyder funktioner til udskrivning, deling og mere. Hvis en fil ikke kan vises i OneDrive, kan du blive bedt om at hente den.

## Fordeling

**Del**-handlingen kopierer filen til din OneDrive, så du kan se, hvem den allerede er delt med, og dele filen med andre personer. Når du vælger handlingen **Del**, åbnes følgende side.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Del fil i OneDrive":::

Du genkender måske ovennævnte side, hvis du har kendskab til OneDrive. Du kan se to forskellige muligheder for deling: **Send link** og **Kopiér link**.

- **Send hyperlink** kan du dele filer med bestemte personer. De personer, som du deler filen med, får en e-mail med et link til filen. Filen vises også i den **fælles** sektion af deres OneDrive. Start med at skrive e-mail-adresser eller kontaktpersonnavne i feltet **navn, gruppe eller e-mailadresse**. Medtag en meddelelse i feltet **Navn, gruppe eller mail**, hvis du vil.

  > [!TIP]
  > Hvis du vil skrive din meddelelse i Outlook, skal du vælge knappen **Outlook**. Linket indsættes i en kladdemail, og alle, du har angivet til at dele med, er på listen **Til**. Med denne indstilling kan du oprette mails ved hjælp af alle funktionerne i Outlook, herunder formatering af tekst, tilføjelse af andre vedhæftede filer, indsættelse af billeder eller tabeller og tilføjelse af CC-eller BCC-modtagere.

- **Kopiér link** kopierer et fillink, som du kan bruge til at dele filen via applikationer som f.eks. Facebook, Twitter eller mail. 

Før du sender eller kopierer et fillink, skal du angive tilladelsesniveauet, som andre skal have. Du kan se den aktuelle indstilling under **Send link** eller **Kopiér link**. I de fleste tilfælde vil det være **Enhver med linket kan redigere**, afhængigt af din administrators indstillinger. Hvis du vil ændre tilladelserne, skal du markere linket og foretage ændringer på siden med **Linkindstillinger**.

Delings funktionen i Business Central er baseret på OneDrive. Du kan finde flere oplysninger om OneDrive-deling og -tilladelser i [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Handlingen **Dele** er ikke tilgængelig i Business central-appen til mobilenheder.

## Log på første gang fra Business central

Når du bruger handlingen **Åbn i OneDrive** eller **Del** første gang, gør [!INCLUDE[prod_short](includes/prod_short.md)] følgende ting:

1. Åbner siden **Gennemse vilkår og betingelser**. Læs siden, og hvis du kan acceptere vilkårene og betingelserne, skal du vælge **Accepter** for at fortsætte.
2. Opretter en mappe med navnet [!INCLUDE[prod_short](includes/prod_short.md)] in OneDrive. 
3. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen oprettes en anden mappe med samme navn som det firma, du arbejder i. Hvis du arbejder i mere end én virksomhed, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en mappe til hver virksomhed, du arbejder i, når du bruger handlingen **Åbn i OneDrive** eller **Del**. 
4. Placerer en kopi af den fil, du har valgt i mappen med virksomhedsnavnet, og åbner derefter filen. 

Næste gang du bruger handlingen **Åbn i OneDrive** eller **Del**, kopierer og åbner [!INCLUDE[prod_short](includes/prod_short.md)] kun filen. 

## Administrere flere kopier af en fil

Når du vælger **Åbn i OneDrive** eller **Del**, kopieres filen fra [!INCLUDE[prod_short](includes/prod_short.md)] til din mappe i OneDrive. Hvis du redigerer filen i OneDrive, vil filen være anderledes end [!INCLUDE[prod_short](includes/prod_short.md)]-filen. Hvis du vil opdatere [!INCLUDE[prod_short](includes/prod_short.md)] med den seneste filversion, skal du fjerne den eksisterende fil fra [!INCLUDE[prod_short](includes/prod_short.md)] og derefter overføre den seneste kopi.

Hvis der allerede findes en fil med dette navn i OneDrive, får du følgende muligheder:

- **Brug eksisterende**

  Denne indstilling åbner eller deler den fil, der allerede er gemt i OneDrive, i stedet for at kopiere filen fra Business Central.
  
- **Erstat**
  
  Denne indstilling erstatter den eksisterende fil i OneDrive med den fil, du valgte i Business Central. Den oprindelige fil går ikke tabt. Du kan se og gendanne den ved hjælp af versionsoversigten i OneDrive. Få mere at vide i [Gendanne en tidligere version af en fil, der er gemt i OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive-159cad6d-d76e-4981-88ef-de6e96c93893).

- **Behold begge**

  Denne indstilling bevarer den eksisterende fil, som den er, og gemmer den fil, du har valgt i Business Central, under et andet navn. Det nye navn ligner det eksisterende navn, undtagen med et suffiksnummer, f.eks. "Varer (2).xlsx".

## Om din Business Central-mappe på OneDrive

Mappen og dens indhold er private, indtil du beslutter dig for at dele dem med andre. Så du kan f.eks. beslutte at dele indhold med en eller flere af dine kolleger eller endda personer uden for organisationen. 

Du kan få adgang til OneDrive fra siden **Indstillinger** ved at klikke på hyperlinket i feltet **Skylager**. Få mere at vide i [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Feltet Skylager i mine Mine indstillinger":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## Se også

[Business Central og OneDrive-integration](across-onedrive-overview.md)  
[Administration af OneDrive-integration med Business Central](admin-onedrive-integration.md)  
[OneDrive Ofte stillede spørgsmål](admin-onedrive-faq.md)
