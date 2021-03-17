---
title: Opsætning af fakturaafrunding | Microsoft Docs
description: Du kan afrunde fakturabeløb, når du opretter fakturaer. Derudover kan lokale regler eller skikke kræve, at du afrunder på en bestemt måde, f.eks. til et beløb, der er deleligt med 0,05.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 59be392bd10805728af2c060e8a2ea2ecab6bb73
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392270"
---
# <a name="set-up-invoice-rounding"></a>Opsætning af fakturaafrunding
Hvis du vil afrunde fakturabeløb, når du opretter fakturaer, kan du bruge funktionen til automatisk afrunding. Når en faktura afrundes, tilføjes en ekstra linje med afrundingsbeløbet og bogføres sammen med de andre fakturalinjer.

> [!NOTE]  
>  Lokale regler eller skikke kan kræve, at fakturaen afrundes på en bestemt måde, f.eks. til et beløb, der er deleligt med 0,05.  

Når du vil bruge automatisk fakturaafrunding, skal du:  

* Angive de finanskonti, som afrundingsdifferencerne bogføres til.  
* Definere regler for afrunding af fakturaer i lokal valuta og i udenlandsk valuta.  
* Aktivere funktionen.  

> [!NOTE]  
>  Ud over funktionerne til fakturaafrunding kan du afrunde beløb på fakturaer vha. funktionen pris-afrundingspræcision og afrundingsfunktionen.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Opsætte finanskonti til fakturaafrundingsdifferencer
Du skal oprette finanskonti eller konti, hvor afrundingsdifferencer kan bogføres, for at bruge den automatiske fakturaafrundingsfunktion. Du skal først oprette momsproduktbogføringsgrupper. Du kan finde flere oplysninger i [Konfigurer moms](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Sådan opsættes finanskonti til fakturaafrundingsdifferencer  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. På siden **Kontoplan** skal du opsætte kontoen og kalde den **Fakturaafrunding** eller noget tilsvarende. [!INCLUDE[prod_short](includes/prod_short.md)] bruger kontonavnet som tekst på fakturaer, der afrundes.  
3. Afhængigt af om du bruger moms eller sales tax, skal du i feltet **Momsproduktbogf.gruppe** eller **Momsprod.bogf.gruppe** vælge en bogføringsgruppe til afrundede beløb. Du kan oprette en ny gruppekode, som kan anvendes til fakturaafrunding.
4. Lad feltet **Bogføringstype** og enten feltet **Momsvirksomhedsbogf.gruppe** eller **Momsvirk.bogf.gruppe** stå tomme. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Du kan nu knytte fakturaafrundingskontoen til bogføringsgrupper på siden **Kreditorbogføringsgrupper**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Oprette afrunding for fremmed og lokal valuta
Før du kan bruge den automatiske fakturaafrundingsfunktion, skal du oprette afrundingsregler for fremmed og lokal valuta.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Sådan oprettes afrundingsregler for fremmed valuta  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutaer**, og vælg derefter det relaterede link.  
2. På siden **Valutaer** skal du vælge den udenlandske valuta for at åbne **Valutakort**, og udfyld derefter felterne **Afrundingspræcision**, **Pris-afrundingspræcision**, **Fakturaafrundingspræcision** og **Fakturaafrundingsretning**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Sådan oprettes afrunding for lokal valuta
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. På siden **Opsætning af Finans** på oversigtspanelet **Generelt** skal du udfylde feltet **Fakturaafrundingspræcision** og **Fakturaafrundningsretning**.  

## <a name="activate-the-invoice-rounding-function"></a>Aktivere fakturaafrundingsfunktionen  
For at sikre, at salgs- og købsfakturaer afrundes automatisk, skal du aktivere fakturaafrundingsfunktionen. Du aktiverer fakturaafrunding separat for salgs- og købsfakturaer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsopsætning** eller **Købsopsætning**, og vælg derefter det relaterede link.  
2. På oversigtspanelet **Generelt** skal du vælge afkrydsningsfeltet **Fakturaafrunding**.  

## <a name="see-also"></a>Se også  
[Fakturere salg](sales-how-invoice-sales.md)  
[Registrere køb](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]