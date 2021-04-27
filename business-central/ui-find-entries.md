---
title: Finde poster | Microsoft Docs
description: I denne artikel beskrives det, hvordan du kan se de relaterede dokumenter og poster
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5f8ddd7176e69c9d1eb3b8d8ff98c93695d50993
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771157"
---
# <a name="finding-related-entries-for-posted-documents"></a>Finde relaterede poster for bogførte bilag 

I denne artikel kan du læse, hvordan du finder dokumenter og poster, der er relateret til hinanden, på basis af fælles oplysninger, f.eks.:

- Bilagsnummer eller bogføringsdato
- Forretningskontakttype, nummer eller eksternt bilagsnummer
- Vareserienummer eller lotnummer

Funktionen er især nyttig til at finde finansposter, der er oprettet som resultat af bestemte transaktioner. Når du søger efter dokumentnummer, kan du udskrive oversigten fra rapporten Bilagsposter.

## <a name="get-started"></a>Kom i gang

Du kan få adgang til funktionen Find poster på de fleste sider, hvor der vises bogførte dokumenter eller bogførte bilag, for både lister og kort. Det første trin er at åbne en af disse sider. Derefter skal du enten vælge handlingen **Find poster** eller trykke på alt+G-tasterne.

Siden **Find poster** indeholder alle relaterede dokumenter og poster, der er baseret på bilagsnr. og bogføringsdato. Siden er inddelt i tre sektioner:

- Den øverste del viser de felter og handlinger, du kan bruge til at filtrere din søgning.
- Den midterste del viser relaterede dokumenter, der er baseret på søgningen.
- Den nederste del indeholder oplysninger om kildedokumentet, som blev fundet ved søgning.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Søg efter poster

Du kan søge efter poster på grundlag af oplysninger om enten dokument-, forretningskontaktperson- eller var referencen. Hvis du vil ændre søgningen, skal du vælge **Handlinger**, **Find efter** og derefter en af følgende handlinger:

|Handling|Description|
|------|-----------|
|Søg efter dokument|Få vist poster baseret på et bestemt bilagsnummer eller bogføringsdato.|
|Forretningskontakt |Få vist poster, der er baseret på en bestemt kontakttype, kontaktnummer, ANR/eller eksternt bilagsnummer. Du kan indtaste de dokumentoplysninger, der er tildelt af en kreditor eller en debitor. Brug de tilgængelige felter til at lede efter kreditorbilag vha. de samme tal som kreditor har givet dokumenterne.|
|Varereference|Få vist det hele baseret på et serienummer eller lotnummer. Du kan angive lotnummer eller serienummer eller filtrere på de serie- eller lotnumre, du vil søge efter. Handlingen er nyttig, hvis du vil se, hvor et bestemt varesporingsnummer blev brugt, hvilken leverandør det kom fra, eller hvilken kunde varen med det varenummer blev solgt til.|

Når du har foretaget en markering, skal du indtaste de relevante søgeoplysninger i felterne øverst. Brug værktøjstip i felterne som hjælp. Når du er færdig, skal du vælge **Find** for at starte søgningen. Hvis du ændrer nogen af filtrene, skal du vælge **Find** igen.

> [!TIP]
> Du kan finde et par eksempler på brug af **Find poster** under [Sporing af varesporede elementer](inventory-how-to-trace-item-tracked-items.md) og [Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Arbejde med Business Central](ui-work-product.md)  
[Føje en sidehandling til rollecenteret](ui-bookmarks.md)  
[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]