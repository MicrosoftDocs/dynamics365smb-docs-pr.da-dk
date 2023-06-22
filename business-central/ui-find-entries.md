---
title: Finde relaterede poster for dokumenter
description: 'Få mere at vide om, hvordan du finder dokumenter, forretningskontaktpersoner og vareposter, der er relateret til hinanden.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
---
# <a name="finding-related-entries-for-documents" />Finde relaterede poster for dokumenter

Lær, hvordan du finder dokumenter og poster, der er relateret til hinanden, på basis af fælles oplysninger, f.eks.:

- Bilagsnummer eller bogføringsdato.
- Forretningskontakttype, nummer eller eksternt bilagsnummer.
- Vareserienummer eller lotnummer.

Funktionen er især nyttig til at finde finansposter, der er oprettet som resultat af bestemte transaktioner. Når du søger efter dokumentnummer, kan du udskrive oversigten fra rapporten **Bilagsposter**.

## <a name="get-started" />Kom i gang

Du kan hurtigt finde funktionen Find poster fra næsten alle sider ved at trykke på tasterne <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd>. På sider, der specifikt viser bogførte dokumenter eller bogførte bilagsposter&mdash;for både lister og kort&mdash;kan du også åbne funktionen ved at vælge handlingen **Find poster**.

Siden **Find poster** indeholder alle relaterede dokumenter og poster, der er baseret på bilagsnr. og bogføringsdato. Siden er inddelt i tre sektioner:

- Den øverste del viser de felter og handlinger, du kan bruge til at filtrere din søgning.
- Den midterste del viser relaterede dokumenter, der er baseret på søgningen.
- Den nederste del indeholder oplysninger om kildedokumentet, som blev fundet ved søgning.

## <a name="search-for-entries" />Søg efter poster

Du kan søge efter poster på grundlag af oplysninger om enten dokument-, forretningskontaktperson- eller var referencen. I den øverste sektion skal du vælge en af følgende indstillinger baseret på den type oplysninger, du har:

|Handling|Beskrivelse|
|------|-----------|
| **Søg efter dokumenter** | Få vist poster baseret på et bestemt bilagsnummer eller bogføringsdato. |
| **Søg efter forretningskontakter** | Få vist poster, der er baseret på en bestemt kontakttype, kontaktnummer og/eller eksternt bilagsnummer. Denne sidste indstilling giver dig mulighed for at søge efter kreditor-eller debitor dokumenter ved at bruge det nummer, som er tildelt af kontakten. |
| **Søg efter varereferencer** | Få vist poster baseret på et serienummer eller lotnummer. Du kan angive lotnummer eller serienummer eller filtrere på de serie- eller lotnumre, du vil søge efter. Handlingen er nyttig, hvis du vil se, hvor et bestemt varesporingsnummer blev brugt, hvilken leverandør det kom fra, eller hvilken kunde varen med det varenummer blev solgt til. |

Når du har foretaget en markering, skal du indtaste de relevante søgeoplysninger i felterne øverst på siden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Når du er færdig, skal du vælge **Find** for at starte søgningen. Hvis du ændrer nogen af filtrene, skal du vælge **Find** igen.

> [!TIP]
> Du kan finde et par eksempler på brug af **Find poster** under [Sporing af varesporede elementer](inventory-how-to-trace-item-tracked-items.md) og [Gennemgang: Sporing af serie-/lotnumre](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-microsoft-trainingtrainingmodulesuser-interface-dynamics--business-centralindex" />Se relateret [Microsoft-træning](/training/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Spore vare via varesporing](inventory-how-to-trace-item-tracked-items.md)  
[Finde bogførte dokumenter uden indgående bilagsposter](across-how-find-posted-documents-without-income-document-records.md)  
[Tilgængelighedsfunktioner og tastaturgenveje](ui-accessibility.md)  
[Arbejde med Business Central](ui-work-product.md)  
[Føje en sidehandling til rollecenteret](ui-bookmarks.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Søge efter sider med Rollestifinder](ui-role-explorer.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
