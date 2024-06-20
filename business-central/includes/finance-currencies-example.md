---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Når du modtager en faktura fra en virksomhed i en udenlandsk valuta, er det forholdsvis nemt at beregne fakturaens lokale valuta (RV) på basis af den aktuelle valutakurs. Fakturaen leveres imidlertid ofte med betalingsbetingelser, så du kan udskyde betalingen til en senere dato, hvilket indebærer en anden valutakurs. Dette problem kombineret med, at valutakurser altid er forskellige fra de officielle valutakurser gør, at det ikke er muligt at forudsige det nøjagtige beløb i den lokale valuta (RV), der er nødvendig for at dække fakturaen. Hvis fakturaens forfaldsdato går til næste måned, skal du muligvis også revaluate det lokale valuta beløb i slutningen af måneden. Kursreguleringen er nødvendig, fordi den nye RV-værdi, der skal dække fakturabeløbet, kan være anderledes, og firmaets gæld til leverandøren er potentielt ændret. Det nye RV-beløb kan være højere eller lavere end det forrige beløb og vil derfor være et tab eller et tab. Men da fakturaen endnu ikke er betalt, anses gevinsten eller tabet for at være *Urealiseret*. Senere betales fakturaen, og banken har returneret den faktiske valutakurs for betalingen. Det antages ikke, at det *realiserede* gevinst-eller tabsbeløb beregnes. Denne urealiserede gevinst eller gevinst tilbageføres derefter, og realiseringen af gevinsten eller tabet bogføres i stedet.

I følgende eksempel modtages en faktura den 1. januar med Valutabeløbet på 1000. På det tidspunkt er valutakursen 1.123.

|Dato|Handling|Valutabeløb|Bilagskurs|RV-beløb på dokument|Justeringskurs|Ikke-realiseret finansgevinstbeløb|Betalingssats|Realiseret finansbeløb|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Faktura**|1000|1.123|1123|||||
|1/31|**Regulering**|1000||1125|1.125|2|||
|2/15|**Tilbagebetaling af betalingsregulering**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1.120|-3|

Ved udgangen af måneden udføres der en kursregulering, hvor kursreguleringen er angivet til 1,125, hvilket udløser en Urealiseret gevinst på 2.

På betalingstidspunktet viser den faktiske valutakurs, der er registreret for bank transaktionen, en valutakurs på 1,120.

Der er en urealiseret transaktion, som derfor bliver tilbageført sammen med betalingen.

Endelig registreres betalingen, og det faktiske tab bogføres på den realiserede tabskonto.
