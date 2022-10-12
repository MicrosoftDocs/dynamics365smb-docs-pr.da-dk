---
title: Søge efter bestemte data
description: Hvis du skal finde en bestemt post, kan du bruge Søg.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: data, search, record
ms.search.form: ''
ms.date: 09/20/2022
ms.author: bholtorf
ms.openlocfilehash: a97668a12b6571b11b21a56f0737a8aea9387b01
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608137"
---
# <a name="search-for-a-record-in-your-data"></a>Søge efter en post i data

Når du vil finde en bestemt post eller værdi, skal du bruge funktionen **Søg efter data** til at søge efter den. Start en søgning i rollecenteret på følgende måder:

* Bruge funktionen **Søg efter data**
* Brug genvejstast kombinationen ctrl + alt + F.

## <a name="how-search-works"></a>Sådan fungerer søgning

Når du har angivet nøgleordene, starter [!INCLUDE[prod_short](includes/prod_short.md)] søgningen i baggrunden og gennemgår hver tabel én ad gangen. Søgeresultaterne begynder for at blive vist, når det er færdigt hver tabel. 

Hvis du indtaster mere end ét nøgleord, vil resultaterne kun indeholde de poster, der indeholder alle ordene i de valgte felter.

Resultat siden viser de tre senest opdaterede poster. Hvis der er mere end tre, kan du vælge **Vis alle** for at få dem vist.

Hver gang du vælger et søgeresultat, øger du tabellens popularitet, og den vil fremstå højere oppe i resultaterne. Derudover bliver posten fundet hurtigere, hvis du søger efter den i fremtiden.

> [!NOTE]
> Hoveder på salgs-, købs-og servicedokumenter repræsenterer faktisk forskellige dokumenttyper, f. eks. rekvisitioner, fakturaer og ordrer. Headere behandles, som om de var tabeller. Hvis dit nøgleord blev fundet på en linje i et af disse dokumenter, og du vælger søgeresultatet, siden for dokumentet vises, og ikke kun linjen.

## <a name="getting-started"></a>Introduktion

Du kan øge resultaterne hurtigere ved at vælge de felter på tabellerne, som du vil medtage i søgningerne. De tabeller og felter, du kan vælge mellem, varierer, afhængigt af dit rollecenter. Alle tabeller og felter vælges som standard, hvilket kan gøre søgningen langsommere. Det anbefales, at du udelukker lige så mange tabeller og felter, som du kan.

## <a name="see-also"></a>Se også

[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Angivelse af data](ui-enter-data.md)  
