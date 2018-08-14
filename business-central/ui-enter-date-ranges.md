---
title: Angive datointervaller i Business Central | Microsoft Docs
description: "Få mere at vide om, hvordan du i en rapport kan få vist data fra bestemte tidsperioder, ved at bruge datointervaller i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: da-dk
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Angive datointervaller
Du kan angive filtre, der indeholder en startdato og en slutdato for kun at få vist dataene for dette dato- eller tidsinterval. Der gælder særlige regler for den måde, du angiver datointervaller på. Lad os tage **Debitor - top 10** som eksempel:

![Angive et datointerval på anmodningssiden for Debitor - top 10-liste](./media/ui-enter-date-ranges/customer-top10-list.png)

Her kan du begrænse rapporten til et bestemt datointerval, f.eks. de seneste to uger eller i alt 6 uger, eller det interval, du ønsker. Når du vil angive datointervaller, angiver du datoer og bruger enten **..** eller **|** til at vælge intervallet. I eksemplet for at få vist top 10 debitorer i de første to uger i maj, skal du indstille filteret til *01 05 17..14 05 17*.
Her er nogle andre eksempler:

| Betyder | Eksempel | Forklaring |
|---|---|---|
|Lig med| 15 12 16 |Kun dem, der er bogført den 15. december 2016.|
|Interval| 15 12 16..15 01 17<br /><br />..15 12 16|Dem, der er bogført fra den 15. december 2016 til og med 15. januar 2017.<br /><br />Dem, der er bogført den 15. december 2016 eller tidligere.|
|Enten/ eller|15 12 16&#124;16 12 16|Dem, der er bogført enten den 15. december eller 16. december 2016. Hvis der er bogført poster på begge dage, vises de ikke.|

Du kan også kombinere de forskellige formattyper.

| Eksempel | Forklaring |
|---|---|
|15 12 16&#124;01 12 16..31 05 17 | Poster, som er bogført enten den 15. december 2016 eller på datoen fra den 1. december 2016 til og med den 31. maj 2017. |
|..14 12 16&#124;30 12 16.. | Poster bogført den 14. december eller tidligere, eller poster bogført den 30. december eller tidligere - dvs. alle poster undtagen dem, der er bogført på datoer mellem og inklusive den 15. og 29. december. |

Bemærk, at vi har brugt det amerikanske format MMDDYY her. Efterhånden som [!INCLUDE[d365fin](includes/d365fin_md.md)] bliver tilgængeligt på andre markeder, du vil kunne bruge de formater, som du plejer.

## <a name="using-date-formulas"></a>Bruge datoformler
En datoformel er en kort, forkortet kombination af bogstaver og tal, der angiver, hvordan datoer skal beregnes. Du kan indtaste datoformler i forskellige datoberegningsfelter og i gentagelsesintervalfelter i gentagelseskladder.

> [!NOTE]
>  I alle formlens datafelter indgår en dag automatisk til at dække i dag som den dag, hvor perioden starter. Tilsvarende, hvis du f.eks. indtaster **1U**, så er perioden faktisk otte dage, fordi i dag er inkluderet. Du skal indtaste **6D** eller **1U\-1D** for at angive en periode på syv dage (en hel uge), der medtager periodens startdato.

Her følger et par eksempler på brugen af datoformler:

-   Datoformlen i gentagelsesintervalfeltet i en gentagelseskladde afgør, hvor tit posten på kladdelinjen skal bogføres.

-   Datoformlen i feltet **Respitperiode** for et bestemt rykkerniveau afgør det tidsrum, der skal gå fra forfaldsdatoen (eller fra forfaldsdatoen for den forrige rykker), før der oprettes en rykker.

-   Datoformlen i feltet **Forfaldsdatoformel** afgør, hvordan forfaldsdatoen på rykkeren beregnes.

Datoformlen kan indeholde op til 20 tegn (både tal og bogstaver). Du kan bruge følgende bogstaver som forkortelser for tidsangivelser.

|  Bogstav  |  Tidsangivelse  |
|----------|----------------------|
|U|Løbende|
|D|Dag\(e\)|
|V|Uge\(r\)|
|M|Måned\(er\)|
|K|Kvartal\(er\)|
|Å|År\(\)|

Datoformlen kan opbygges på tre måder.

Følgende eksempel viser, hvordan du skal bruge **A** for aktuel og en tidsenhed.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|LU|Løbende uge|
|cm|Løbende måned|

Følgende eksempel viser, hvordan du skal bruge et tal og en tidsenhed. Tallet må ikke være større end 9999.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|10D|10 dage fra i dag|
|2U|2 uger fra i dag|

Følgende eksempel viser, hvordan du skal bruge en tidsenhed og et tal.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|D10|Den næste 10. dage i en måned|
|UD4|Den næste 4. dag i en uge \(torsdag\)|

Følgende eksempel viser, hvordan du kan kombinere de tre formler efter behov.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|LM\+10D|Løbende måned \+ 10 dage|

Følgende eksempel viser, hvordan du kan bruge et minustegn til at angive en dato i fortiden.

|  Udtryk  |  Betyder  |
|--------------|-----------|
|-1Å|1 år siden fra i dag|

> [!IMPORTANT]
>  Hvis lokationen bruger en basiskalender, fortolkes den datoformel, du f.eks. indtaster i feltet **Transporttid**, i overensstemmelse med kalenderens arbejdsdage. For eksempel betyder **1U** syv arbejdsdage.

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)  
[Indtaste kriterier i filtre](ui-enter-criteria-filters.md)  

