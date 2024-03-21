---
title: Metoder til afskrivning af anlægsaktiver
description: Få mere at vide om de forskellige indbyggede metoder til at afskrive eller nedskrive anlægsaktiver.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'write down, depreciate, depreciation'
ms.search.form: '5629, 5633'
ms.date: 09/22/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Metoder til afskrivning af anlægsaktiver

Der er otte tilgængelige metoder til afskrivning i [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Lineær  
* Saldo 2  
* Saldo 2  
* Saldo 1/Linieær  
* Saldo 2/Lineær  
* Brugerdefineret  

  Angive din egen afskrivningsmetode ved hjælp af Afskrivningstabeller. Du kan finde flere oplysninger om anvendelse af en brugerdefineret afskrivningsmetode i [Konfigurere brugerdefineret afskrivningsmetode](fa-how-setup-user-defined-depreciation-method.md).
* Manuel  

  Brug den manuelle metode til anlægsaktiver, der ikke afskrives, f.eks. jord. Du skal angive afskrivningen i anlægskassekladden. Kørslen **Beregn afskrivninger** medtager ikke de anlægsaktiver, hvor den manuelle afskrivningsmetode bruges.  
* Halvårlig afskrivning  

  Denne metode afskriver et anlægsaktiv med det samme beløb hvert år.  

## Lineær afskrivning

Når du bruger den lineære metode, skal du angive en af følgende indstillinger i anlægsafskrivningsprofilen:  

* Afskrivningsperioden (år eller måneder) eller en afskrivningsslutdato  
* En fast årlig procent  
* Et fast årligt beløb  
* Afskrivningsperiode  

### Afskrivningsperiode

Hvis du angiver afskrivningsperioden (antal afskrivningsår, antal afskrivningsmåneder eller afskrivningsslutdatoen), beregner følgende formel afskrivningsbeløbet:  

*Afskrivningsbeløb = ((Bogført værdi - Skrapværdi) x Antal afskrivningsdage) / Resterende afskrivningsdage*  

De resterende afskrivningsdage beregnes som antallet af afskrivningsdage minus antallet af dage mellem afskrivningens startdato og datoen for den sidste anlægspost.  

Den bogførte værdi kan reduceres med beløb for bogført afskrivning, nedskrivning, bruger 1 og bruger 2, afhængigt af om feltet **Del af afskrivningsberegning** er deaktiveret, og om feltet **Del af bogført værdi** på siden **Anlægsbogf.typeopsætning** er aktiveret. Med denne beregning sikres det, at anlægsaktivet et fuldstændigt afskrevet ved slutdatoen for afskrivningen.  

### Fast årlig procentsats

Hvis du har angivet en fast årlig procent, bruger [!INCLUDE [prod_short](includes/prod_short.md)] følgende formel til at beregne afskrivningsbeløbet:  

*Afskrivningsbeløb = (Lineær pct. x Afskrivningsgrundlag x Antal afskrivningsdage) / (100 x 360)*  

### Fast årligt beløb

Hvis du har angivet et fast årligt beløb, bruger [!INCLUDE [prod_short](includes/prod_short.md)] følgende formel til at beregne afskrivningsbeløbet:  

* *Afskrivningsbeløb = (Fast afskrivningsbeløb x Antal afskrivningsdage) / 360*  

### Eksempel – Lineær afskrivning

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Den anslåede levetid er otte år. Kørslen **Beregn afskrivninger** køres to gange om året.  

I dette eksempel ser anlægsposten sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelse |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 30-06-20 |Afskrivninger |180 |-6.250,00 |93,750.00 |
| 31-12-20 |Afskrivninger |180 |-6.250,00 |87,500.00 |
| 30-06-21 |Afskrivninger |180 |-6.250,00 |81,250.00 |
| 31-12-21 |Afskrivninger |180 |-6.250,00 |75,000.00 |
| 30-06-27 |Afskrivninger |180 |-6.250,00 |6,250.00 |
| 31-12-27 |Afskrivninger |180 |-6.250,00 |0 |

## Saldo 1-afskrivning

Denne afskrivningsmetode allokerer den største del af omkostningerne ved et aktiv til de første år af anlæggets nyttige levetid. Hvis du bruger denne metode, skal du angive en fast årlig procent.  

Følgende formel beregner afskrivningsbeløb:  

* *Afskrivningsbeløb = (Saldoprocent x Antal afskrivningsdage x Afskrivningsgrundlag) / (100 x 360)*  

Afskrivningsgrundlaget beregnes som den bogførte værdi ved årets start. Antal afskrivningsdage er antallet af dage mellem afskrivningsdagen og sidste afskrivningsdag. [!INCLUDE [prod_short](includes/prod_short.md)] beregner afskrivning, hvis der foretages afskrivning i regnskabsåret med denne formel.  

Det bogførte afskrivningsbeløb kan indeholde poster med forskellige bogføringstyper (nedskrivning, bruger1 og bruger2) efter startdatoen på det aktuelle regnskabsår. Disse bogføringstyper er inkluderet i det bogførte afskrivningsbeløb, hvis afkrydsningsfelterne **Afskrivningstype** og **Del af bogført værdi** er markeret på siden **Anlægsbogf.typeopsætning**.  

### Eksempel 1 – Saldo 1 afskrivning

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Feltet **Saldopct.** er angivet til 25. Kørslen **Beregn afskrivninger** køres to gange om året.  

Følgende tabel viser, hvordan de tilhørende anlægsposter ser ud.  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelser |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 30-06-20 |Afskrivninger |180 |-12.500,00 |87,500.00 |
| 31-12-20 |Afskrivninger |180 |-12.500,00 |75,000.00 |
| 30-06-21 |Afskrivninger |180 |-9.375,00 |65,625.00 |
| 31-12-21 |Afskrivninger |180 |-9.375,00 |56,250.00 |
| 30-06-22 |Afskrivninger |180 |-7.031,25 |49,218.75 |
| 31-12-22 |Afskrivninger |180 |-7.031,25 |42,187.50 |
| 30-06-23 |Afskrivninger |180 |-5.273,44 |36,914.06 |
| 31-12-23 |Afskrivninger |180 |-5.273,44 |31,640.62 |
| 30-06-24 |Afskrivninger |180 |-3.955,08 |27,685.54 |
| 31-12-24 |Afskrivninger |180 |-3.955,08 |23,730.46 |

Beregningsmetode:  

* År 1: *25 % af 100.000 = 25.000 = 12.500 + 12.500*

* År 2: *25 % af 75.000 = 18.750 = 9.375 + 9.375*

* År 3: *25 % af 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

Beregningen fortsætter, indtil den bogførte værdi er lig med det endelige afrundingsbeløb eller den skrapværdi, du har angivet.  

### Eksempel 2 – Saldo 1 afskrivning

Et anlægs bogførte værdi er 100.000 den 31.12.2022. Du bogfører en afskrivning på 1.778 den 2.2.2023, som er det forventede (proportionale) beløb for årets afskrivning den 32 dage. Hvis du kører afskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 8.222, fordi der er 148 dage fra 02.02.2023 til 30.06.2023. Den forventede afskrivning for 30.06.2023 beregnes ved hjælp af følgende formel:

* *148/360 x 0,20 x 100.000 = 8.222*

### Eksempel 3 – Saldo 1 afskrivning

Hvis du bogfører et beløb, der ikke stemmer med afskrivningsmetoden saldo 1, f. eks. 5.000, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] resten af det forventede beløb.

Et anlægs bogførte værdi er 100.000 den 31.12.2022. Du bogfører en afskrivning på 5.000 den 02.02.2023, hvilket er mere end det forventede (proportionalt) beløb på 02.02.2023 på 32 dage. Hvis du kører afskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 8.222, fordi der er 148 dage fra 02.02.2023 til 30.06.2023. Den forventede afskrivning for 30.06.2023 beregnes ved hjælp af følgende formel:

* *148/360 x 0,20 x 100.000 = 8.222*

### Eksempel 4 – Saldo 1 afskrivning

Et anlægs bogførte værdi er 100.000 den 31.12.2023. Du bogfører en afskrivning på 95.000 den 02.02.2023, hvilket overstiger det tilladte afskrivningsbeløb for året. Hvis du kører afskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 5.000, fordi der er 148 dage fra 02.02.2023 til 30.06.2023. Den forventede afskrivning for 30.06.2023 beregnes ved hjælp af følgende formel: 

* *148/360 x 0,20 x 100.000 = 8.222*

Den resterende bogførte værdi er dog kun 5.000, så [!INCLUDE [prod_short](includes/prod_short.md)] foreslår 5.000, fordi en bogført værdi ikke kan være negativ.

## Saldo 2-afskrivning

Med Saldo 1- og Saldo 2-metoderne beregnes det samme totale afskrivningsbeløb for hvert år. Men hvis du udfører kørslen **Beregn afskrivning** mere end én gang om året, vil Saldo 1-metoden resultere i lige store afskrivningsbeløb for hver afskrivningsperiode. Med Saldo 2-metoden bliver resultatet derimod afskrivningsbeløb, der bliver mindre og mindre for hver periode.  

### Eksempel – Saldo 2 afskrivning

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. Feltet **Saldopct.** er angivet til 25. Kørslen **Beregn afskrivninger** køres to gange om året. Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelser |(Afskrivningens startdato)|100,000.00 |100,000.00 |
| 30-06-20 |Afskrivninger |180 |-13.397,46 |86,602.54 |
| 31-12-20 |Afskrivninger |180 |-11.602,54 |75,000.00 |
| 30-06-21 |Afskrivninger |180 |-10.048,09 |64,951.91 |
| 31-12-21 |Afskrivninger |180 |-8.701,91 |56,250.00 |

Beregningsmetode:  

* *BV* = Bogført værdi  
* *AD* = Antal afskrivningsdage  
* *DBP* = Saldopct.  
* *P* = *DBP*/100  
* *D* = *ND*/360  

Formlen for beregning af afskrivningsbeløbet er:  

*DA* = *BV* x (1 - (1 - P)<sup>D</sup>)

Afskrivningsværdierne er:  

| Dato | Beregning |
| --- | --- |
| 30-06-20 |DA = 100.000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 13.397,46 |
| 31-12-20 |DA = 86.602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11.602,54 |
| 30-06-21 |DA = 75.000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10.048,09 |
| 31-12-21 |DA = 64.951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8.701,91 |

## DB1/SL-afskrivning

Saldo1/Lin. er et forkortet udtryk for Saldo 1 og Lineær. Beregningen fortsætter, indtil den bogførte værdi er lig med det endelige afrundingsbeløb eller den skrapværdi, du har angivet.  

Ved kørslen **Beregn afskrivning** beregnes et lineært beløb og et saldobeløb, men kun det største af de to overføres til kladden.  

Du kan bruge forskellige procentsatser til saldoberegninger.  

Hvis du bruger denne metode, skal du angive den anslåede levetid og en saldoprocent på siden **Anlægsafskrivningsprofiler**.  

> [!NOTE]
> Hvis du bruger en af saldoafskrivningsmetoderne, og du vil køre afskrivning i flere år, skal du køre hvert års afskrivning separat. Hvis du udfører afskrivning for hele perioden fra anskaffelsesdatoen til slutningen af det sidste regnskabsår eller sidste regnskabsperiode, er det sandsynligt, at resultaterne bliver forkerte. Det kan f.eks. være, at du vil køre det i flere år, hvis du har importeret ældre data, og du bruger de faktiske anskaffelsesdatoer for dine aktiver og vil indhente den akkumulerede afskrivning. For saldoafskrivningsmetoder [!INCLUDE [prod_short](includes/prod_short.md)] beregnes den tilladte afskrivning pr. år startende med den registrerede bogførte værdi for hvert år. Det kan ikke foretage en flerårig afskrivning i ét trin.
>
> I **rapporten Anlæg - forventet værdi** kan der fremskrives afskrivninger for flerårige perioder, hvilket kan være forvirrende sammenlignet med de resultater, du får, hvis du foretager afskrivninger over flere år ved hjælp af en af saldoafskrivningsmetoderne. 

### Eksempel – Afskrivning med Saldo 1

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. På siden **Anlægsafskrivningsprofiler** står der 25 i feltet **Saldopct.** og 8 i feltet **Antal afskrivningsår**. Kørslen **Beregn afskrivninger** køres to gange om året.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelser |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 30-06-20 |Afskrivninger |180 |-12.500,00 |87,500.00 |
| 31-12-20 |Afskrivninger |180 |-12.500,00 |75,000.00 |
| 30-06-21 |Afskrivninger |180 |-9.375,00 |65,625.00 |
| 31-12-21 |Afskrivninger |180 |-9.375,00 |56,250.00 |
| 30-06-22 |Afskrivninger |180 |-7.031,25 |49,218.75 |
| 31-12-22 |Afskrivninger |180 |-7.031,25 |42,187.50 |
| 30-06-23 |Afskrivninger |180 |-5.273,44 |36,914.06 |
| 31-12-23 |Afskrivninger |180 |-5.273,44 |31,640.62 |
| 30-06-24 |Afskrivninger |180 |-3.955,08 |27,685.54 |
| 31-12-24 |Afskrivninger |180 |-3.955,08 |23,730.46 |
| 30-06-25 |Afskrivninger |180 |-3.955,08 |19.775,38 Lin. |
| 31-12-25 |Afskrivninger |180 |-3.955,08 |15.820,30 Lin. |
| 30-06-26 |Afskrivninger |180 |-3.955,08 |11.865,22 Lin. |
| 31-12-26 |Afskrivninger |180 |-3.955,07 |7.910,15 Lin. |
| 30-06-27 |Afskrivninger |180 |-3.955,08 |3.955,07 Lin. |
| 31-12-27 |Afskrivninger |180 |-3.955,07 |0,00 Lin. |

`SL` Hvis der står "Lineær" efter den bogførte værdi, er den lineære metode blevet brugt.  

Beregningsmetode:  

* År 1: (2020):  

    *Saldobeløb: 25% af 100.000 = 25.000=12.500+12.500*  

    *Lineært beløb = 100.000/8=12.500=6.250+6.250*  

    Saldobeløbet anvendes, fordi det er det største beløb af de to.  

* År 5: (2025):  

    *Saldobeløb: 25% af 23,730.46 = 4,943.85=2,471.92+2,471.92*  

    *Lineært beløb = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

    Det lineære beløb anvendes, fordi det er det største af de to.  

## Half-Year Convention-afskrivning

Metoden med det halvårlige afskrivningsprincip bliver kun anvendt, hvis du har markeret afkrydsningsfeltet **Brug Half-Year Convention (US)** på siden **Anlægsafskrivningsprofil**.  

Denne afskrivningsmetode kan bruges sammen med følgende afskrivningsmetoder:  

* Lineær  
* Saldo 2  
* Saldo 1/Linieær  

Når du anvender det halvårlige afskrivningsprincip, afskrives et anlægsaktiv i seks måneder i det første regnskabsår, uanset hvad der står i feltet **Afskrivningsstartdato**.  

> [!NOTE]  
> Den anslåede levetid, der er tilbage for anlægsaktivet efter det første regnskabsår, vil altid indeholde et halvår, hvor det halvårlige afskrivningsprincip anvendes. Når således det halvårlige afskrivningsprincip skal anvendes korrekt, skal feltet **Afskrivningsslutdato** på siden **Anlægsafskrivningsprofil** altid indeholde en dato, der ligger nøjagtigt seks måneder inden den sidste dag i det regnskabsår, hvor anlægsaktivet bliver helt afskrevet.  

### Eksempel – Half-Year Convention-afskrivning

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. I **Afskriv fra den** er datoen 01-03-20 angivet. Den anslåede levetid er fem år, så **Afskriv til den** skal angives til 30-06-25. Kørslen **Beregn afskrivning** udføres en gang om året. Dette eksempel er baseret på et kalenderregnskabsår.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-03-20 |Anskaffelse |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 31-12-20 |Afskrivninger |270 |-10.000,00 |90,000.00 |
| 31-12-21 |Afskrivninger |360 |-20.000,00 |70,000.00 |
| 31-12-22 |Afskrivninger |360 |-20.000,00 |50,000.00 |
| 31-12-23 |Afskrivninger |360 |-20.000,00 |30,000.00 |
| 31-12-24 |Afskrivninger |360 |-20.000,00 |10,000.00 |
| 31-12-25 |Afskrivninger |180 |-10.000,00 |0.00 |

## Eksempel: Saldo1/Lineær afskrivning efter halvårsprincippet

Et anlægsaktiv har en anskaffelsespris på DKK 100.000. I **Afskriv fra den** er datoen 01-11-20 angivet. Den anslåede levetid er fem år, så **Afskriv til den** skal angives til 30-06-25. På siden **Anlægsafskrivningsprofiler** står der 40 i feltet **Saldopct.**. Kørslen **Beregn afskrivning** udføres en gang om året. Dette eksempel er baseret på et kalenderregnskabsår.  

Anlægsposterne ser sådan ud:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-11-20 |Anskaffelse |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 31-12-20 |Afskrivninger |60 |-20.000,00 |80,000.00 |
| 31-12-21 |Afskrivninger |360 |-32.000,00 |48,000.00 |
| 31-12-22 |Afskrivninger |360 |-19.200,00 |28,800.00 |
| 31-12-23 |Afskrivninger |360 |-11.520,00 |17,280.00 |
| 31-12-24 |Afskrivninger |360 |-11.520,00 |5.760,00 Lin. |
| 31-12-25 |Afskrivninger |180 |-5.760,00 |0,00 Lin. |

`SL` Hvis der står "Lineær" efter den bogførte værdi, er den lineære metode blevet brugt.  

Beregningsmetode:  

* År 1:  

    *Saldobeløb = Beløb for hele året = 40 % af 100.000 = 40.000.* For et halvt år således 40.000 / 2 = 20.000  

    *Lineært beløb = Beløb for hele året = 100.000 / 5 = 20.000.* For et halvt år således = 20.000 / 2 =10.000  

    Saldobeløbet anvendes, fordi det er det største beløb af de to.  

* År 5: (2024):  

    *Saldobeløb = 40 % af 17.280,00 = 6.912,00*  

    *Lineært beløb = 28.800 / 1,5 = 11.520,00*  

    Det lineære beløb anvendes, fordi det er det største af de to.  

## Kopiering af poster til flere afskrivningsprofiler

Hvis du har tre afskrivningsprofiler, B1, B2 og B3, og du vil kopiere poster fra B1 til B2 og B3, kan du markere afkrydsningsfeltet **Del af kopiliste** på afskrivningsprofilkortene for B2 og B3. Denne indstilling er f.eks. nyttig i følgende scenarier:

* Afskrivningsmodellen B1 integreres med finansbogholderiet og bruger anlægskassekladden.
* Afskrivningsmodellen B2 og B3 integreres ikke med finansbogholderiet og bruger anlægskassekladden.  

Når du indtaster en post i B1 i anlægskassekladden og markerer afkrydsningsfeltet **Brug kopiliste**, kopierer [!INCLUDE [prod_short](includes/prod_short.md)] posten i profil B2 og B3 i anlægskladden, når posten bogføres.  

> [!NOTE]  
> Du kan ikke kopiere i samme kladde, som du kopierer fra. Hvis du bogfører poster i anlægskassekladden, kan du kopiere dem i anlægskladden eller i anlægskassekladden ved at bruge en anden kladde.  

> [!NOTE]  
> Du kan ikke bruge samme nummerserie i anlægskassekladden og anlægskladden. Når du bogfører poster i anlægskassekladden, skal feltet **Bilagsnr.** være tomt. Hvis du indtaster et tal i feltet, kopieres tallet i anlægskladden. Du skal manuelt ændre bilagsnummeret, før du kan bogføre kladden.  

## Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
