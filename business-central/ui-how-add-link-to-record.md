---
title: 'Føje vedhæftede filer, links og noter til poster'
description: 'Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms-service: dynamics-365-business-central
---
# Administrere vedhæftede filer, links og noter på kort og dokumenter

I **faktaboksen** på de fleste kort og i dokumenter kan du vedhæfte filer, tilføje links og skrive noter i fanen **Vedhæftede filer**. Nummeret bag fanetitlen angiver, hvor mange vedhæftede filer, links eller noter der findes for kortet eller dokumentet.

I oversigtspanelet **Linjer** kan du også bruge handlingen **Vedhæftede filer** til at vedhæfte dokumenter til en bestemt linje. Du kan f. eks. knytte design specifikationer til en vare på en købsfaktura.

Vedhæftede filer, links og noter forbliver vedhæftet på kortet eller dokumentet, mens det er forarbejdet i andre stater. Fra en igangværende salgsordre til en bogført salgsfaktura. Ingen af de vedhæftede filtyper er dog output fra systemet, f.eks. ved udskrivning eller lagring til en fil.

Du kan også føje vedhæftede filer til de mails, du sender fra [!INCLUDE [prod_short](includes/prod_short.md)]. Når du sender en e-mail direkte fra et dokument, f. eks. et salgstilbud, kan du med handlingen **Tilføj filer fra kildedokument**. Du kan kun vælge filer, der er vedhæftet dokumentet. Du kan kun vælge filer, der er vedhæftet linjer.

> [!NOTE]
> Når du delvist sender og fakturerer en salgs- eller købsordre, knyttes den vedhæftede fil kun til den endelige faktura for ordren. På samme måde knyttes den vedhæftede fil til finansposterne for dokumentet, men ikke til periodiseringsposterne, når du fakturerer periodiseringer.
>
> Hvis du sletter en ordre, før den faktureres, skal du også fjerne den vedhæftede fil.
>
> Når du bruger handlingen **Hent købsleverancelinjer** på en købsfaktura, føjes den vedhæftede fil på den relaterede købsordre, til købsfakturaen.

## Sådan vedhæftes en fil til en købsfaktura

Du kan vedhæfte alle filtyper, der indeholder tekst, billeder eller video, på et kort eller et dokument. Det er nyttigt, når du f.eks. vil gemme en kreditorfaktura som PDF-fil på den relaterede købsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Filer, der er vedhæftet med funktionen Indgående bilag, medtages ikke under fanen **Vedhæftede filer**. Du kan finde flere oplysninger i [Indgående bilag](across-income-documents.md). Det samme gælder for filer, der er knyttet til linjer på dokumenter.

Følgende procedure er baseret på en købsfaktura. Trinene er de samme for alle andre understøttede dokumenter og kort.

> [!TIP]
> Hvis den vedhæftede fil er specifik for en linje i et dokument, kan du knytte den til linjen. Vælg linjen med fordelingen og vælg derefter handlingen **Vedhæftede filer**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Åbn den købsordre, som du vil vedhæfte en fil til.
3. Åbn fanen **Vedhæftede filer** i **faktaboksen**.
4. Vælg værdien bag feltet **Dokumenter**, f.eks. "0".
5. I feltet **Vedhæftet fil** på siden **Vedhæftede bilag**.
6. Benyt en af følgende fremgangsmåder i dialogboksen **Vedhæft et dokument** for at vedhæfte en fil:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Filen er nu vedhæftet til købsfakturaen.

## Sådan ser du en vedhæftet fil

1. Åbn fanen **Vedhæftede filer** i faktaboksen.
2. Vælg værdien bag feltet **Dokumenter**, f.eks. "1".
3. På siden **Vedhæftede bilag** skal du vælge handlingen **Eksempel**.
4. Åbne den overførte file.

## Sådan gemmer du et dokument som en vedhæftet PDF-fil

Når du har brug for at gemme et dokument som en fil, kan du bruge handlingen **Vedhæft som PDF** til at hente det aktuelle dokumentindhold som en PDF-fil, der er vedhæftet dokumentets faktaboks. Det er f.eks. nyttigt, når dokumenter følger flere trin i en proces, f.eks. en salgsproces eller en godkendelsesproces, og du vil henvise til en udskrift af det forrige trin.

Følgende procedure er baseret på en salgsordre. Fremgangsmåden er den samme for alle understøttede dokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg en salgsordre, og vælg derefter handlingen **Vedhæft som PDF**.

En PDF-fil med det aktuelle indhold i salgsordren tilføjes på fanen **Vedhæftede filer** i faktaboksen.

## Sådan tilføjes et link fra et varekort

Du kan føje et link fra et kort eller et dokument til en hvilken som helst URL-adresse. Det er nyttigt, når du f.eks. vil knytte et varekort til leverandørens varekatalog.

Den følgende procedure er baseret på et varekort. Trinene er de samme for alle andre understøttede kort og dokumenter.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Marker den vare, du vil tilføje en kæde fra, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.
3. Vælg ikonet **+** i **Links**.
4. I feltet **Hyperlinkadresse** skal du angive linket.

    Linket skal være en gyldig URL-adresse til internettet eller intranettet.

5. Angiv eventuelle oplysninger om linket i feltet **Beskrivelse**.  
6. Vælg knappen **OK**.

Linket er nu knyttet til varekortet.  

## Sådan skrives en note i en salgsordre

Du kan skrive en note til et dokument eller et kort, for f.eks. at kommunikere særlige instruktioner til andre brugere af dokumentet eller kortet. Du kan medtage fillinks og URL-adresser i noter.

> [!NOTE]
> Noterne under fanen **Vedhæftede filer** er ikke relateret til interne notefunktioner, som hovedsageligt bruges til kommunikation mellem brugere af arbejdsgangen. Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md).

Følgende procedure er baseret på en salgsordre. Trinene er de samme for alle andre understøttede dokumenter og kort.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Marker den salgsordre, du vil skrive en note om, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.
3. Vælg ikonet **+** i sektionen **Noter**.
4. Skriv en tekst i feltet **Note**, f.eks. "Dette er en vigtig bestilling".
5. Vælg knappen **OK**.

Noten knyttes nu til salgsordren.

## Se også  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Indgående bilag](across-income-documents.md)  
[Konfiguration af workflownotifikationer](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
