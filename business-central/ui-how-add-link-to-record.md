---
title: Føje vedhæftede filer, links og noter til poster | Microsoft Docs
description: Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 84d9c0768a457fd13a73b3d70d2b8c329098fe82
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953271"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Administrere vedhæftede filer, links og noter på kort og dokumenter

I faktaboksen på de fleste kort og i dokumenter kan du vedhæfte filer, tilføje links og skrive noter. Ved links og noter kan du også gøre dette på listesiden ved først at vælge den relaterede linje.

Hvis du vil have vist eller ændre nogen af disse typer vedhæftede oplysninger, skal du først åbne fanen **Vedhæftede filer** i faktaboksen. Nummeret bag fanetitlen angiver, hvor mange vedhæftede filer, links eller noter der findes for kortet eller dokumentet.

Vedhæftede filer, links og noter forbliver tilknyttede, når kortet eller dokumentet behandles i andre tilstande, f.eks. fra en igangværende salgsordre til en bogført salgsfaktura. Ingen af de vedhæftede filtyper er dog output fra systemet, f.eks. ved udskrivning eller lagring til en fil.

> [!NOTE]
> Når du delvist sender og fakturerer en salgsordre eller indkøbsordre, knyttes den vedhæftede fil kun til den endelige faktura for den pågældende ordre. På samme måde knyttes den vedhæftede fil kun til finansposterne for dokumentet, men ikke til periodiseringsposterne, når du fakturerer ved hjælp af funktionen Udskydelser.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Sådan vedhæftes en fil til en købsfaktura
Du kan vedhæfte alle filtyper, der indeholder tekst, billeder eller video, på et kort eller et dokument. Det er nyttigt, når du f.eks. vil gemme en kreditorfaktura som PDF-fil på den relaterede købsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Filer, der er vedhæftet med funktionen Indgående bilag, medtages ikke under fanen **Vedhæftede filer**. Du kan finde flere oplysninger i [Indgående bilag](across-income-documents.md).

Følgende procedure er baseret på en salgsordre. Trinene er de samme for alle andre understøttede dokumenter og kort.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsordre, som du vil vedhæfte en fil til.
3. Åbn fanen **Vedhæftede filer** i faktaboksen.
4. Vælg værdien bag feltet **Dokumenter**, f.eks. "0".
5. På siden **Vedhæftede bilag** i feltet **Vedhæftet fil** skal du vælge knappen **Vælg fil**.
5. Vælg en fil fra en placering, og vælg derefter knappen **Åbn**.

Filen er nu vedhæftet til købsfakturaen.

## <a name="to-add-a-link-from-an-item-card"></a>Sådan tilføjes et link fra et varekort
Du kan føje et link fra et kort eller et dokument til en hvilken som helst URL-adresse eller sti. Det er nyttigt, når du f.eks. vil knytte et varekort til leverandørens varekatalog.

Den følgende procedure er baseret på et varekort. Trinene er de samme for alle andre understøttede kort og dokumenter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Marker den vare, du vil tilføje en kæde fra, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.
3. Vælg ikonet **+** i **Links**.
4. I feltet **Hyperlinkadresse** skal du angive linket.

    Linket skal være en gyldig URL-adresse til internettet eller intranettet.

5. Angiv eventuelle oplysninger om linket i feltet **Beskrivelse**.  
6. Vælg knappen **OK**.

Linket er nu knyttet til varekortet.  

## <a name="to-write-a-note-on-a-sales-order"></a>Sådan skrives en note i en salgsordre
Du kan skrive en note til et dokument eller et kort, for f.eks. at kommunikere særlige instruktioner til andre brugere af dokumentet eller kortet. Du kan medtage fillinks og URL-adresser i noter.

> [!NOTE]
> Noterne under fanen **Vedhæftede filer** er ikke relateret til interne notefunktioner, som hovedsageligt bruges til kommunikation mellem brugere af arbejdsgangen. Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md).

Følgende procedure er baseret på en salgsordre. Trinene er de samme for alle andre understøttede dokumenter og kort.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.
2. Marker den salgsordre, du vil skrive en note om, og vælg derefter fanen **Vedhæftede filer** i faktaboksen.
3. Vælg ikonet **+** i sektionen **Noter**.
4. Skriv en tekst i feltet **Note**, f.eks. "Dette er en vigtig bestilling".
5. Vælg knappen **OK**.

Noten knyttes nu til salgsordren.

## <a name="see-also"></a>Se også  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Indgående bilag](across-income-documents.md)  
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)  
