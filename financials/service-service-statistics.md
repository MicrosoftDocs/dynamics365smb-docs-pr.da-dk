---
title: Servicestatistik | Microsoft Docs
description: "Få et hurtigt overblik over indholdet af servicedokumenter, f.eks. ordrer, tilbud, fakturaer eller kreditnotaer, og detaljerne på de specifikke servicelinjer og serviceartiklerne."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e4cc14212f30c7b42aaf9d08c848488ab65444f6
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="viewing-service-statistics"></a>Visning af servicestatistik
Financials kan levere nogle statistikker, som du kan bruge til at analysere servicedokumenter og fastslå, hvor godt du administrerer dine serviceprocesser. Du kan analysere servicekontrakter, -artikler, -tilbud, -ordrer, -fakturaer og -kreditnotaer ved at vælge handlingen **Statistik**. For serviceartikler og -kontrakter, kan du også bruge vinduet **Serviceartikel - Trendscape** eller **Kontrakt - Trendscape** til at få vist en oversigt over serviceposterne for en bestemt serviceartikel.   

## <a name="viewing-statistics-for-service-orders"></a>Visning af statistik for serviceordrer
Funktionen Serviceordrestatistik giver dig et hurtigt overblik over indholdet af hele serviceordren, oplysningerne på de specifikke servicelinjer og oplysninger vedrørende fakturering, levering og forbrug og debitorens saldo.  

De statistiske data til en serviceordre vises i vinduet **Serviceordrestatistik** til den relevante ordre. Du kan åbne vinduet med relevante statistikker fra en serviceordre. I vinduet **Serviceordrer** skal du vælge **Statistik**. I oversigtspanelerne i dette vindue vises der oplysninger som mængde, beløb, moms, omkostninger, avance og debitorkreditmaksimum. Beløbene i vinduet er angivet i den valuta, der bruges i serviceordren, medmindre andet er angivet.  

### <a name="view-totals-for-a-service-order"></a>Vis totaler for en serviceordre  
Du kan få vist det samlede beløb på servicelinjerne, inklusive og eksklusive moms, momsdelen, kostbeløb og avance på servicelinjerne. Vinduet viser også varespecifikke oplysninger, f.eks. vægt, rumfang og antallet af kolli.  

### <a name="view-shipping-information"></a>Vis leveringsoplysninger  
Du kan se oplysninger om varerne, ressourcerne eller de kostbeløb, der skal leveres. De værdier, der er angivet i feltet **Lever (antal)**, bruges på hver servicelinje i ordren til angivelse af oplysninger.  

### <a name="view-order-details"></a>Vis ordredetaljer  
Du kan få vist oplysninger om de varer, ressourcetimer og kostbeløb, der skal faktureres og forbruges. Følgende tabel beskriver disse oplysninger.  

|Kolonne | Beskrivelse|  
|------------|---------------------------------------|  
|**Fakturering**|Viser beløb, der skal bogføres som faktureret fra serviceordren.|  
|**Forbrug**|Viser antal og udgifter på varer eller ressourcer, der skal bogføres som forbrugt.|  
|**I alt**|Viser de samlede beløb i serviceordren, der er resultatet, når faktureringsbeløbene lægges sammen med forbrugsbeløbene.|  

### <a name="analyze-service-order-lines"></a>Analysér serviceordrelinjer  
Du kan analysere oplysningerne efter typerne af servicelinjer, der er medtaget i serviceordren. Beløbene vises særskilt for:  

* Varer  
* Ressourcer  
* Omkostninger og finanskonti  

### <a name="view-customer-information"></a>Vis kundeoplysninger  
Se saldoen på debitorens konto i tillæg til det kreditmaksimum, der kan tildeles den kunde, som du oprettede servicedokumentet for.

## <a name="viewing-service-item-statistics"></a>Visning af serviceartikelstatistik
I vinduet **Serviceartikelstatistik** kan du få vist opdaterede oplysninger om en serviceartikel, baseret på følgende typer af serviceposter:  

* Ressourcer  
* Varer  
* Serviceomkostninger  
* Servicekontrakter  
* Sum  

For hver posttype kan du se det fakturerede beløb, forbrug (beløb), kostbeløb, antal, faktureret antal og forbrugt antal, avancebeløb og avanceprocent. Avanceprocenten beregnes i henhold til følgende formel:  

* (Faktureret beløb - Forbrug (varekostpris)) x 100 / Faktureret beløb  

## <a name="using-trendscapes"></a>Ved hjælp af Trendscapes
For serviceartikler og servicekontrakter giver vinduerne **Serviceartikel - Trendscape** eller **Servicekontrakt - Trendscape** en oversigt, du kan rulle op og ned i, over serviceposter i en periode for en bestemt serviceartikel eller -kontrakt. Hvis du vil have vist udviklingen, skal du åbne serviceartiklen eller servicekontrakten, vælge handlingen **statistik** og derefter klikke på **Trendscape**.

Når du ruller op og ned på listen, bliver tallene beregnet i den lokale valuta i overensstemmelse med til de angivne tidsintervaller. Alle beløb beregnes på grundlag af serviceposter, dvs. poster, der oprettes, når du bogfører serviceordrer eller servicefakturaer.

Du kan filtrere listen ved at angive de serviceartikler, der skal medtages.  

> [!Tip]  
>  Hvis du har sat tidsintervallet til **Dag**, og du har brug for at rulle langt frem eller tilbage i en periode, kan du gøre det hurtigere ved at angive et længere tidsinterval, f.eks. **Kvartal**. Når du har fundet frem til den ønskede periode, kan du skifte tilbage til det oprindelige interval for at få vist mere detaljerede oplysninger.   

## <a name="viewing-gains-and-losses-on-contracts"></a>Visning af gevinster og tab på kontrakter  
Der bliver genereret en gevinst/tabspost for kontrakten, når et kontrattilbud konverteres til en servicekontrakt, når kontraktlinjer tilføjes eller fjernes fra en servicekontrakt, eller når en kontrakt bliver annulleret. Du kan få vist kontaktgevinster eller -tab på følgende sider.  

|Side | Beskrivelse|  
|----------------|---------------------------------------|  
|**Kontraktgevinst/-tab (kontr.)**|Få vist kontraktgevinst/-tab efter servicekontrakt.|  
|**Kontraktgevinst/-tab (grupper)**|Sådan får du vist kontraktgevinst/-tab efter servicekontraktgruppe.|  
|**Kontraktgevinst/-tab (debitorer)**|Sådan får du vist kontraktgevinst/-tab efter kunde.|  
|**Kontraktgevinst/-tab (årsager)**|Sådan får du vist kontraktgevinst/-tab efter årsagskode.|  
|**Kontraktgevinst/-tab (ansv.cent.)**|Sådan får du vist kontraktgevinst/-tab efter ansvarscenter.|  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), skriv navnet på den side, der skal vises, og vælg derefter det relaterede link.  
2. Angiv de filterkriterier, du vil anvende. I vinduet **Kontraktgevinst/-tab (årsager)** skal du f.eks. vælge en værdi for **Årsagskodefilter**.  
3. Vælg handlingen **Vis matrix**.

## <a name="viewing-statistics-for-posted-service-documents"></a>Visning af statistik for bogførte servicedokumenter
Funktionen Servicestatistik bruges til at få et statistisk overblik over indholdet af bogførte servicedokumenter, f.eks. en bogført leverance, faktura og kreditnota.  

De statistiske oplysninger vises i statistikvinduet til det tilsvarende bogførte servicedokument. Du kan åbne det relevante statistikvindue fra bogført serviceleverance, bogført servicefaktura eller bogført servicekreditnota dokumenter. Vælg **Statistik** i gruppen **Proces** under fanen **Startside** for hver af disse dokumenttyper. F.eks. fra vinduet **Bogførte servicefakturaer** under fanen **Startside** i gruppen **Behandl** skal du vælge **Statistik**.  

### <a name="posted-service-shipment-statistics"></a>Statistik for bogførte serviceleverancer  
I vinduet **Statistik for serviceleverance** kan du se en oversigt over en bogført serviceleverance. Den omfatter oplysninger om det fysiske indhold af leverancen, f.eks. antallet af leverede varer, ressourcetidsforbrug eller omkostninger samt vægt og rumfang af de leverede varer.  

### <a name="posted-service-invoice-statistics"></a>Statistik for bogførte servicefakturaer  
Du kan få vist en statistisk oversigt over en bogført servicefaktura i vinduet **Statistik for servicefakturaer**. Du kan få vist totalerne for den bogførte servicefaktura. Dataene omfatter det samlede beløb på servicelinjerne (inklusive og eksklusive moms), der er bogført som faktureret, momsdelen, kostbeløb og avance i den bogførte faktura. I vinduet vises også oplysninger om følgende:  

* Varerne på servicefakturalinjerne, f.eks. vægt, rumfang og antallet af kolli.  
* Saldoen på debitorens konto samt det kreditmaksimum, du kan yde kunden.  

### <a name="posted-service-credit-memo-statistics"></a>Statistik for bogførte servicekreditnotaer  
Du kan bruge vinduet **Statistik for servicekreditnotaer** til at få et statistisk overblik over linjerne i en bogført servicekreditnota. Oversigten kan omfatte:

* De samlede beløb i den bogførte kreditnota vises som mængde, beløb, moms, omkostninger og avance. Der er også oplysninger om varerne på servicelinjerne i den bogførte kreditnota, f.eks. antal, vægt og rumfang.  
* Generelle oplysninger om debitoren, f.eks. debitorens kreditmaksimum og saldo på kontoen.  

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Oprette serviceordrer](service-how-to-create-service-orders.md)   
[Sådan gør du: Oprette serviceartikler](service-how-to-create-service-items.md)   
[Planlægning af service](service-plan-service.md)  

