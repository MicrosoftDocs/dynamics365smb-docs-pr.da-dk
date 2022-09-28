---
title: Find poster
description: I denne artikel beskrives det, hvordan du kan se de relaterede dokumenter og poster
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
ms.openlocfilehash: 3c89d9f3044a8fd0d0fa7f811f1b2f01978e4302
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532372"
---
# <a name="finding-related-entries-for-posted-documents"></a>Finde relaterede poster for bogførte bilag 

I denne artikel kan du læse, hvordan du finder dokumenter og poster, der er relateret til hinanden, på basis af fælles oplysninger, f.eks.:

- Bilagsnummer eller bogføringsdato
- Forretningskontakttype, nummer eller eksternt bilagsnummer
- Vareserienummer eller lotnummer

Funktionen er især nyttig til at finde finansposter, der er oprettet som resultat af bestemte transaktioner. Når du søger efter dokumentnummer, kan du udskrive oversigten fra rapporten Bilagsposter.

## <a name="get-started"></a>Kom i gang

Du kan hurtigt finde funktionen Find poster fra næsten alle sider ved at trykke på tasterne Ctrl + Alt + Q. På sider, der specifikt viser bogførte dokumenter eller bogførte Bilagsposter&mdash;for både lister og kort&mdash;kan du også åbne funktionen ved at vælge handlingen **Find poster**.

Siden **Find poster** indeholder alle relaterede dokumenter og poster, der er baseret på bilagsnr. og bogføringsdato. Siden er inddelt i tre sektioner:

- Den øverste del viser de felter og handlinger, du kan bruge til at filtrere din søgning.
- Den midterste del viser relaterede dokumenter, der er baseret på søgningen.
- Den nederste del indeholder oplysninger om kildedokumentet, som blev fundet ved søgning.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Søg efter poster

Du kan søge efter poster på grundlag af oplysninger om enten dokument-, forretningskontaktperson- eller var referencen. Hvis du vil ændre søgningen, skal du vælge **Handlinger**, **Find efter** og derefter en af følgende handlinger:

|Handling|Beskrivelse|
|------|-----------|
|Søg efter dokument|Få vist poster baseret på et bestemt bilagsnummer eller bogføringsdato.|
|Forretningskontakt |Få vist poster, der er baseret på en bestemt kontakttype, kontaktnummer, ANR/eller eksternt bilagsnummer. Du kan indtaste de dokumentoplysninger, der er tildelt af en kreditor eller en debitor. Brug de tilgængelige felter til at lede efter kreditorbilag vha. de samme tal som kreditor har givet dokumenterne.|
|Varereference|Få vist det hele baseret på et serienummer eller lotnummer. Du kan angive lotnummer eller serienummer eller filtrere på de serie- eller lotnumre, du vil søge efter. Handlingen er nyttig, hvis du vil se, hvor et bestemt varesporingsnummer blev brugt, hvilken leverandør det kom fra, eller hvilken kunde varen med det varenummer blev solgt til.|

Når du har foretaget en markering, skal du indtaste de relevante søgeoplysninger i felterne øverst. Brug værktøjstip i felterne som hjælp. Når du er færdig, skal du vælge **Find** for at starte søgningen. Hvis du ændrer nogen af filtrene, skal du vælge **Find** igen.

> [!TIP]
> Du kan se et par eksempler på brug af **Søg poster** under [Sporing af varesporede elementer](inventory-how-to-trace-item-tracked-items.md) <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Arbejde med Business Central](ui-work-product.md)  
[Føje en sidehandling til rollecenteret](ui-bookmarks.md)  
[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
