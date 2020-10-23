---
title: Afskrivningsmetoder | Microsoft Docs
description: Få mere at vide om de forskellige metoder til at afskrive eller nedskrive anlægsaktiver.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a1278b344efef1df243d4f82e9d463f8faf9a259
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920793"
---
# <a name="depreciation-methods"></a>Afskrivningsmetoder
Der er otte tilgængelige metoder til afskrivning:  

* Lineær  
* Saldo 1  
* Saldo 2  
* Saldo 1/Lineær  
* Saldo 2/Lineær  
* Brugerdefineret  
* Manuelt  

  > [!NOTE]  
  >   Brug denne metode til anlægsaktiver, der ikke afskrives, f.eks. jord. Du skal angive afskrivningen i anlægskassekladden. Kørslen **Beregn afskrivninger** medtager ikke de anlægsaktiver, hvor denne afskrivningsmetode bruges.  
* Halvårlig afskrivning  

  > [!NOTE]  
  >    Når du bruger denne metode, afskrives et anlægsaktiv med det samme beløb hvert år.  

## <a name="straight-line-depreciation"></a>Lineær afskrivning
Når du bruger den lineære metode, skal du angive en af følgende indstillinger i anlægsafskrivningsprofilen:  

* Afskrivningsperioden (år eller måneder) eller en afskrivningsslutdato  
* En fast årlig procent  
* Et fast årligt beløb  
* Afskrivningsperiode  

### <a name="depreciation-period"></a>Afskrivningsperiode
Hvis du angiver afskrivningsperioden (antal afskrivningsår, antal afskrivningsmåneder eller afskrivningsslutdatoen), beregner følgende formel afskrivningsbeløbet:  

*Afskrivningsbeløb = ((Bogført værdi - Skrapværdi) x Antal afskrivningsdage) / Resterende afskrivningsdage*  

De resterende afskrivningsdage beregnes som antallet af afskrivningsdage minus antallet af dage mellem afskrivningens startdato og datoen for den sidste anlægspost.  

Den bogførte værdi kan reduceres med beløb for bogført afskrivning, nedskrivning, bruger 1 og bruger 2, afhængigt af om feltet **Del af afskrivningsberegning** er deaktiveret, og om feltet **Del af bogført værdi** på siden **Anlægsbogf.typeopsætning** er aktiveret. Med denne beregning sikres det, at anlægsaktivet et fuldstændigt afskrevet ved slutdatoen for afskrivningen.  

### <a name="fixed-yearly-percentage"></a>Fast årlig procent
Hvis du har angivet en fast årlig procent, bruges følgende formel til at beregne afskrivningsbeløbet:  

Afskrivningsbeløb = (Lineær pct. x Afskrivningsgrundlag x Antal afskrivningsdage) / (100 x 360)  

### <a name="fixed-yearly-amount"></a>Fast årligt beløb
Hvis du angiver et fast årligt beløb, bruges denne formel til at beregne afskrivningsbeløbet:  

Afskrivningsbeløb = (Fast afskrivningsbeløb x Antal afskrivningsdage) / 360  

### <a name="example---straight-line-depreciation"></a>Eksempel – Lineær afskrivnings
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Den anslåede levetid er otte år. Kørslen **Beregn afskrivninger** køres to gange om året.  

I dette eksempel ser anlægsposten sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelse |* |100,000.00 |100,000.00 |
| 30-06-10 |Afskrivninger |180 |-6.250,00 |93,750.00 |
| 31-12-10 |Afskrivninger |180 |-6.250,00 |87,500.00 |
| 30-06-11 |Afskrivninger |180 |-6.250,00 |81,250.00 |
| 31-12-11 |Afskrivninger |180 |-6.250,00 |75,000.00 |
| 30-06-17 |Afskrivninger |180 |-6.250,00 |6,250.00 |
| 31-12-17 |Afskrivninger |180 |-6.250,00 |0 |

* Afskrivningens startdato  

## <a name="declining-balance-1-depreciation"></a>Saldo 1-afskrivning
Denne hurtige afskrivningsmetode allokerer den største del af omkostningerne ved et anlægsaktiv til de første år af anlæggets nyttige levetid. Hvis du bruger denne metode, skal du angive en fast årlig procent.  

Følgende formel beregner afskrivningsbeløb:  

*Afskrivningsbeløb = (Saldoprocent x Antal afskrivningsdage x Afskrivningsgrundlag) / (100 x 360)*  

Afskrivningsgrundlaget beregnes som den bogførte værdi minus bogført afskrivning efter startdatoen på det aktuelle regnskabsår.  

Det bogførte afskrivningsbeløb kan indeholde poster med forskellige bogføringstyper (nedskrivning, bruger1 og bruger2) efter startdatoen på det aktuelle regnskabsår. Disse bogføringstyper er inkluderet i det bogførte afskrivningsbeløb, hvis afkrydsningsfelterne **Afskrivningstype** og **Del af bogført værdi** er markeret på siden **Anlægsbogf.typeopsætning**.  

### <a name="example---declining-balance-1-depreciation"></a>Eksempel – Saldo 1 afskrivning
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Feltet **Saldopct.** er angivet til 25. Kørslen **Beregn afskrivninger** køres to gange om året.  

Følgende tabel viser, hvordan de tilhørende anlægsposter ser ud.  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelser |* |100,000.00 |100,000.00 |
| 30-06-10 |Afskrivninger |180 |-12.500,00 |87,500.00 |
| 31-12-10 |Afskrivninger |180 |-12.500,00 |75,000.00 |
| 30-06-11 |Afskrivninger |180 |-9.375,00 |65,625.00 |
| 31-12-11 |Afskrivninger |180 |-9.375,00 |56,250.00 |
| 30-06-12 |Afskrivninger |180 |-7.031,25 |49,218.75 |
| 31-12-12 |Afskrivninger |180 |-7.031,25 |42,187.50 |
| 30-06-13 |Afskrivninger |180 |-5.273,44 |36,914.06 |
| 31-12-13 |Afskrivninger |180 |-5.273,44 |31,640.62 |
| 30-06-14 |Afskrivninger |180 |-3.955,08 |27,685.54 |
| 31-12-14 |Afskrivninger |180 |-3.955,08 |23,730.46 |

* Afskrivningens startdato  

    Beregningsmetode:  

    *Første år: 25 % af 100.000 = 25.000 = 12.500 +12.500*

    *Andet år: 25 % af 75.000 = 18.750 = 9.375 + 9.375*

    *Tredje år: 25 % af 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

    Beregningen fortsætter, indtil den bogførte værdi er lig med det endelige afrundingsbeløb eller den skrapværdi, du har angivet.   

## <a name="declining-balance-2-depreciation"></a>Saldo 2-afskrivning
Med Saldo 1- og Saldo 2-metoderne beregnes det samme totale afskrivningsbeløb for hvert år. Men hvis du udfører kørslen **Beregn afskrivning** mere end én gang om året, vil Saldo 1-metoden resultere i lige store afskrivningsbeløb for hver afskrivningsperiode. Med Saldo 2-metoden bliver resultatet derimod afskrivningsbeløb, der bliver mindre og mindre for hver periode.  

### <a name="example---declining-balance-2-depreciation"></a>Eksempel – Saldo 2 afskrivning
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Feltet **Saldopct.** er angivet til 25. Kørslen **Beregn afskrivninger** køres to gange om året. Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelser |* |100,000.00 |100,000.00 |
| 30-06-10 |Afskrivninger |180 |-13.397,46 |86,602.54 |
| 31-12-10 |Afskrivninger |180 |-11.602,54 |75,000.00 |
| 30-06-11 |Afskrivninger |180 |-10.048,09 |64,951.91 |
| 31-12-11 |Afskrivninger |180 |-8.701,91 |56,250.00 |

* Afskrivningens startdato  

Beregningsmetode:  

* BV = Bogført værdi  
* AD = Antal afskrivningsdage  
* DBP = Saldopct.  
* P = DBP/100  
* D = ND/360  

Formlen for beregning af afskrivningsbeløbet er:  

*AB = BV x (1 – (1 –P)<sup>D<sup>*  

Afskrivningsværdierne er:  

| Dato | Beregning |
| --- | --- |
| 30-06-10 |AB = 100.000,00 x (1-(1 - 0,25)<sup>0,5<sup>) = 13.397,46 |
| 31-12-10 |AB = 86.602,54 x (1-(1 - 0,25)<sup>0,5<sup>) = 11.602,54 |
| 30-06-11 |AB = 75.000,00 x (1-(1 - 0,25)<sup>0,5<sup>) = 10.048,09 |
| 31-12-11 |AB = 64.951,91 x (1-(1 - 0,25)<sup>0,5<sup>) = 8.701,91 |

## <a name="db1sl-depreciation"></a>Afskrivning med Saldo 1/Lineær
Saldo1/Lin. er et forkortet udtryk for Saldo 1 og Lineær. Beregningen fortsætter, indtil den bogførte værdi er lig med det endelige afrundingsbeløb eller den skrapværdi, du har angivet.  

Ved kørslen **Beregn afskrivning** beregnes et lineært beløb og et saldobeløb, men kun det største af de to overføres til kladden.  

Du kan bruge forskellige procentsatser til saldoberegninger.  

Hvis du bruger denne metode, skal du angive den anslåede levetid og en saldoprocent på siden **Anlægsafskrivningsprofiler**.  

### <a name="example---db1-sl-depreciation"></a>Eksempel – Afskrivning med Saldo 1/Lineær
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. På siden **Anlægsafskrivningsprofiler** står der 25 i feltet **Saldopct.** og 8 i feltet **Antal afskrivningsår**. Kørslen **Beregn afskrivninger** køres to gange om året.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelser |* |100,000.00 |100,000.00 |
| 30-06-10 |Afskrivninger |180 |-12.500,00 |87,500.00 |
| 31-12-10 |Afskrivninger |180 |-12.500,00 |75,000.00 |
| 30-06-11 |Afskrivninger |180 |-9.375,00 |65,625.00 |
| 31-12-11 |Afskrivninger |180 |-9.375,00 |56,250.00 |
| 30-06-12 |Afskrivninger |180 |-7.031,25 |49,218.75 |
| 31-12-12 |Afskrivninger |180 |-7.031,25 |42,187.50 |
| 30-06-13 |Afskrivninger |180 |-5.273,44 |36,914.06 |
| 31-12-13 |Afskrivninger |180 |-5.273,44 |31,640.62 |
| 30-06-14 |Afskrivninger |180 |-3.955,08 |27,685.54 |
| 31-12-14 |Afskrivninger |180 |-3.955,08 |23,730.46 |
| 30-06-15 |Afskrivninger |180 |-3.955,08 |19.775,38 Lin. |
| 31-12-15 |Afskrivninger |180 |-3.955,08 |15.820,30 Lin. |
| 30-06-16 |Afskrivninger |180 |-3.955,08 |11.865,22 Lin. |
| 31-12-16 |Afskrivninger |180 |-3.955,07 |7.910,15 Lin. |
| 30-06-17 |Afskrivninger |180 |-3.955,08 |3.955,07 Lin. |
| 31-12-17 |Afskrivninger |180 |-3.955,07 |0,00 Lin. |

* Afskrivningens startdato  

Hvis der står "Lineær" efter den bogførte værdi, er den lineære metode blevet brugt.  

Beregningsmetode:  

Første år:  

*Saldobeløb: 25% af 100.000 = 25.000=12.500+12.500*  

*Lineært beløb = 100.000/8=12.500=6.250+6.250*  

Saldobeløbet anvendes, fordi det er det største beløb af de to.  

Sjette år (2015):  

*Saldobeløb: 25% af 23,730.46 = 4,943.85=2,471.92+2,471.92*  

*Lineært beløb = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

Det lineære beløb anvendes, fordi det er det største af de to.  

## <a name="user-defined-depreciation"></a>Brugerdefineret afskrivning
Programmet indeholder en funktion, som gør det muligt for dig at konfigurere brugerdefinerede afskrivningsmetoder.  

Med en brugerdefineret metode skal du bruge siden **Afskrivningstabeller**, hvor du skal angive en afskrivningsprocent for hver periode (måned, kvartal, år eller regnskabsperiode).  

Formlen for beregning af afskrivningsbeløbet er:  

Afskrivningsbeløb = (Afskrivningsprocent x Antal afskrivningsdage x Afskrivningsgrundlag) / (100 x 360)  

### <a name="depreciation-based-on-number-of-units"></a>Afskrivning baseret på antal enheder
Denne brugerdefinerede metode kan også bruges til afskrivning baseret på antal enheder, f.eks. i forbindelse med produktionsmaskiner med fastlagt levetidskapacitet. På siden **Afskrivningstabeller** kan du angive antallet af enheder, der kan produceres i hver enkelt periode (måned, kvartal, år eller regnskabsperiode).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Sådan konfigureres brugerdefinerede afskrivningsmetoder
På siden **Afskrivningstabel** kan du oprette brugerdefinerede afskrivningsmetoder. For eksempel kan du konfigurere afskrivning baseret på antal enheder.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Afskrivningstabeller**, og vælg derefter det relaterede link.  
2. På siden **Afskrivningstabeloversigt** skal du vælge handlingen **Ny**.  
3. På siden **Afskrivningstabelkort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Eksempel - Brugerdefineret afskrivning
Du bruger en afskrivningsmetode, der gør det muligt at afskrive aktiver hurtigere af skattemæssige årsager.  

Til et anlægsaktiv med en levetid på tre år ville du af skattemæssige årsager anvende følgende afskrivningssatser:  

* År 1: 25%  
* År 2: 38%  
* År 3: 37%  

Anskaffelsesprisen er RV 100.000, og afskrivningslevetiden er fem år. Afskrivningen beregnes en gang om året.  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelse |* |100,000.00 |100,000.00 |
| 31-12-10 |Afskrivninger |360 |-25.000,00 |75,000.00 |
| 31-12-11 |Afskrivninger |360 |-38.000,00 |37,000.00 |
| 31-12-12 |Afskrivninger |360 |-37.000,00 |0 |
| 31-12-13 |Afskrivninger |Ingen |Ingen |0 |
| 31-12-14 |Afskrivninger |Ingen |Ingen |0 |

* Afskrivningens startdato  

Hvis du bruger en brugerdefineret metode, skal felterne **Første brugerdef. dato** og **Afskriv fra** udfyldes på siden **Anlægsafskrivningsprofiler**. Feltet **Første brugerdef. afskr.dato** og indholdet i feltet **Periodelængde** på siden **Afskrivningstabeller** bruges til at fastsætte tidsintervallerne til afskrivningsberegninger. Dermed sikres, at den angivne procentdel begynder at blive anvendt på samme dato for alle aktiver. Feltet **Afskriv fra den** bruges til at beregne antallet af afskrivningsdage.  

I det forrige eksempel indeholder både felterne **Første brugerdef. dato** og **Afskriv fra** 01-01-01. Hvis feltet **Første brugerdef. afskr.dato** imidlertid indeholdte 01/01/10, og feltet **Afskriv fra den** indeholdte 04/01/11, ville resultatet være:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-10 |Anskaffelse |* |100,000.00 |100,000.00 |
| 31-12-10 |Afskrivninger |270 |-18.750,00 |81,250.00 |
| 31-12-11 |Afskrivninger |360 |-38.000,00 |42,250.00 |
| 31-12-12 |Afskrivninger |360 |-37.000,00 |6,250.00 |
| 31-12-13 |Afskrivninger |90 |-6.250,00 |0 |
| 31-12-14 |Afskrivninger |Ingen |Ingen |0 |

* Afskrivningens startdato  

## <a name="half-year-convention-depreciation"></a>Half-Year Convention-afskrivning (US)
Metoden med det halvårlige afskrivningsprincip bliver kun anvendt, hvis du har markeret afkrydsningsfeltet **Brug Half-Year Convention (US)** på siden **Anlægsafskrivningsprofil**.  

Denne afskrivningsmetode kan bruges sammen med følgende afskrivningsmetoder i programmet:  

* Lineær  
* Saldo 1  
* Saldo 1/Lineær  

Når du anvender det halvårlige afskrivningsprincip, afskrives et anlægsaktiv i seks måneder i det første regnskabsår, uanset hvad der står i feltet **Afskrivningsstartdato**.  

> [!NOTE]  
>   Den anslåede levetid, der er tilbage for anlægsaktivet efter det første regnskabsår, vil altid indeholde et halvår, hvor det halvårlige afskrivningsprincip anvendes. Når således det halvårlige afskrivningsprincip skal anvendes korrekt, skal feltet **Afskrivningsslutdato** på siden **Anlægsafskrivningsprofil** altid indeholde en dato, der ligger nøjagtigt seks måneder inden den sidste dag i det regnskabsår, hvor anlægsaktivet bliver helt afskrevet.  

### <a name="example---half-year-convention-depreciation"></a>Eksempel – Half-Year Convention-afskrivning
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. I **Afskriv fra den** er datoen 01-03-10 angivet. Den anslåede levetid er fem år, så **Afskriv til den** skal angives til 30-06-15. Kørslen **Beregn afskrivning** udføres en gang om året. Dette eksempel er baseret på et kalenderregnskabsår.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-03-10 |Anskaffelse |* |100,000.00 |100,000.00 |
| 31-12-10 |Afskrivninger |270 |-10.000,00 |90,000.00 |
| 31-12-11 |Afskrivninger |360 |-20.000,00 |70,000.00 |
| 31-12-12 |Afskrivninger |360 |-20.000,00 |50,000.00 |
| 31-12-13 |Afskrivninger |360 |-20.000,00 |30,000.00 |
| 31-12-14 |Afskrivninger |360 |-20.000,00 |10,000.00 |
| 31-12-15 |Afskrivninger |180 |-10.000,00 |0.00 |

* Afskrivningens startdato  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Eksempel: Saldo1/Lineær afskrivning efter halvårsprincippet
Et anlægsaktiv har en anskaffelsespris på DKK 100.000. I **Afskriv fra den** er datoen 01-11-10 angivet. Den anslåede levetid er fem år, så **Afskriv til den** skal angives til 30-06-15. På siden **Anlægsafskrivningsprofiler** står der 40 i feltet **Saldopct.**. Kørslen **Beregn afskrivning** udføres en gang om året. Dette eksempel er baseret på et kalenderregnskabsår.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-11-10 |Anskaffelse |* |100,000.00 |100,000.00 |
| 31-12-10 |Afskrivninger |60 |-20.000,00 |80,000.00 |
| 31-12-11 |Afskrivninger |360 |-32.000,00 |48,000.00 |
| 31-12-12 |Afskrivninger |360 |-19.200,00 |28,800.00 |
| 31-12-13 |Afskrivninger |360 |-11.520,00 |17,280.00 |
| 31-12-14 |Afskrivninger |360 |-11.520,00 |5.760,00 Lin. |
| 31-12-15 |Afskrivninger |180 |-5.760,00 |0,00 Lin. |

* Afskrivningens startdato  

Hvis der står "Lineær" efter den bogførte værdi, er den lineære metode blevet brugt.  

Beregningsmetode:  

Første år:  

*Saldobeløb = Beløb for hele året = 40% af 100.000 = 40.000. For et halvt år således 40.000 / 2 = 20.000*  

*Lineært beløb = Beløb for hele året = 100,000 / 5 = 20.000. For et halvt år således = 20.000 / 2 = 10.000*  

Saldobeløbet anvendes, fordi det er det største beløb af de to.  

Femte år (2004):  

*Saldobeløb = 40 % af 17.280,00 = 6.912,00*  

*Lineært beløb = 28.800 / 1,5 = 11.520,00*  

Det lineære beløb anvendes, fordi det er det største af de to.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Kopiering af poster til andre afskrivningsprofiler
Hvis du har tre afskrivningsprofiler, B1, B2 og B3, og du vil kopiere poster fra B1 til B2 og B3, kan du markere afkrydsningsfeltet **Del af kopiliste** på afskrivningsprofilkortene for B2 og B3. Det kan være nyttigt, hvis afskrivningsprofil B1 er integreret med finansposterne og anvender anlægskassekladden, og afskrivningsprofil B2 og B3 ikke er integreret med finansposterne og anvender anlægskladden.  

Når du indtaster en post i B1 i anlægskassekladden og markerer afkrydsningsfeltet **Brug kopiliste**, kopieres posten i profil B2 og B3 i anlægskladden, når posten bogføres.  

> [!NOTE]  
>   Du kan ikke kopiere i samme kladde, som du kopierer fra. Hvis du bogfører poster i anlægskassekladden, kan du kopiere dem i anlægskladden eller i anlægskassekladden ved at bruge en anden kladde.  

> [!NOTE]  
>   Du kan ikke bruge samme nummerserie i anlægskassekladden og anlægskladden. Når du bogfører poster i anlægskassekladden, skal feltet **Bilagsnr.** være tomt. Hvis du indtaster et tal i feltet, kopieres tallet i anlægskladden. Du skal manuelt ændre bilagsnummeret, før du kan bogføre kladden.  

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
