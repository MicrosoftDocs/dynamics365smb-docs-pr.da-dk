---
title: Bogføringsdato på værdiposter
description: Få mere at vide, hvordan kørslen Juster kostpris - vareposter identificerer og tildeler en posteringsdato til de værdiposter, der er ved at blive oprettet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215099"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designoplysninger: Bogføringsdato på post med reguleringsværdi
Denne artikel indeholder en vejledning til brugere af funktionen Lagerkostmetode i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne specifikke artikel giver en vejledning i, hvordan kørslen **Juster kostpris - vareposter** identificerer og tildeler en bogføringsdato til de værdiposter, der er ved at blive oprettet.  

Først gennemgås konceptet i processen, hvordan kørslen identificerer og tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet. Derefter beskrives nogle scenarier, som vi i supportteamet støder på fra tid til anden, og endelig vises der en oversigt over de begreber, der er brugt.  

## <a name="the-concept"></a>Konceptet  
Kørslen **Reguler kostværdi – vareposter** tildeler en bogføringsdato til den værdipost, der er ved at blive oprettet i følgende trin:  

1.  Først har bogføringsdatoen for posten, der skal oprettes, den samme dato som den post, den regulerer.  

2.  Bogføringsdatoen valideres op mod lagerperioder og/eller Opsætning af Finans.  

3.  Tildeling af bogføringsdato. Hvis den oprindelige bogføringsdato ikke er inden for det tilladte datointerval for posteringen, tildeler kørslen en tilladt bogføringsdato fra Opsætning af Finans eller lagerperiode. Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der tildeles til posten med reguleringsværdien.  

 Lad os gennemgå processen mere i praksis. Antag, at vi har en varepost for varesalg. Varen blev leveret på den 5. september 2013, og den blev faktureret dagen efter.  

![Status for varepostnumre i scenariet](media/helene/TechArticleAdjustcost1.png "Status for varepostnumre i scenariet")  

Nedenfor repræsenterer den første værdipost (379) forsendelsen og har den samme bogføringsdato som den overordnede varepost.  

Den anden værdipost (381) repræsenterer fakturaen.  

 Den tredje værdipost (391) er en justering af faktureringsværdiposten (381)  

 ![Status for værdiposter i scenariet](media/helene/TechArticleAdjustcost2.png "Status for værdiposter i scenariet")  

 Trin 1: Reguleringsværdiposten, der skal oprettes, er knyttet til samme bogføringsdato, som den post, den justerer, illustreret ovenfor af værdipost 391.  

 Trin 2: Validering af oprindelig tildelt bogføringsdato.  

Kørslen **Juster kostpris - vareposter** bestemmer, om den første bogføringsdato for reguleringsværdiposten er inden for det tilladte bogføringsdatointerval, der er baseret på lagerperioder og/eller Opsætning af Finans.  

 Lad os gennemgå ovennævnte salg ved at tilføje opsætningen af tilladte bogføringsdatointervaller.  

 Lagerperioder:  

![Lagerperioder i scenariet](media/helene/TechArticleAdjustcost3.png "Lagerperioder i scenariet")

 Den først tilladte bogføringsdato er den første dag i den første åbne periode. 1. september 2013.  

 Opsætning af Finans:  

![Regnskabsopsætning i scenariet](media/helene/TechArticleAdjustcost4.png "Regnskabsopsætning i scenariet")

 Første tilladte bogføringsdato er den dato, der er angivet i feltet Tillad bogføring fra: 10. september 2013.  

 Hvis både lagerperioder og tilladte bogføringsdatoer i Opsætning af Finans er defineret, så er det den seneste dato af de to, der definerer det tilladte bogføringsdatointerval.  

 Trin 3: Tildeling af en tilladt bogføringsdato.  

 Den oprindeligt tildelt bogføringsdato er 6. september, som vist i trin 1. Men i 2. trin identificerer kørslen Juster kostpris - vareposter, at den tidligst tilladte bogføringsdato er 10. september, og dermed tildeles 10. september til 10 reguleringsværdiposten nedenfor.  

 ![Status for værdiposter i scenariet 2](media/helene/TechArticleAdjustcost5.png "Status for værdiposter i scenariet 2")

 Vi har nu gennemgået konceptet for tildeling af bogføringsdatoer til værdiposter, der er oprettet af kørslen Juster kostpris - vareposter.  

 Lad os fortsætte med at gennemse nogle scenarier, som vi i supportteamet støder på fra tid til anden i forbindelse med tilknyttede bogføringsdatoer i kørslen Juster kostpris – vareposter og de relaterede opsætninger.  

## <a name="scenarios"></a>Eksempler  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenarie I: "Bogføringsdatoen er ikke inden for intervallet af tilladte bogføringsdatoer..."  
 Dette er en scenarie, hvor en bruger får vist den nævnte fejlmeddelelse, under kørsel af Juster kostpris - vareposter.  

 I det foregående afsnit, der beskriver konceptet med tildeling af bogføringsdatoer, var formålet med kørslen Juster kostpris - vareposter at oprette en værdipost med bogføringsdatoen 10. september.  

![Fejlmeddelelse om bogføringsdato.](media/helene/TechArticleAdjustcost6.png "Fejlmeddelelse om bogføringsdato")

 Vi følger op på brugeropsætningen:  

![Opsætning af brugerens tilladte bogføringsdatoer](media/helene/TechArticleAdjustcost7.png "Opsætning af brugerens tilladte bogføringsdatoer")

 Brugeren har i dette tilfælde et tilladt bogføringsdatointerval fra 11. september til 30. september og må derfor ikke bogføre reguleringsværdiposten med bogføringsdatoen 10. september.  

![Oversigt over opsætning af den involverede bogføringsdato](media/helene/TechArticleAdjustcost8.png "Oversigt over opsætning af den involverede bogføringsdato")

 Vidensbaseartikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver yderligere scenarier, der er relateret til nævnte fejlmeddelelse.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenarie II: Bogføringsdato på reguleringsværdipost og bogføringsdatoen på post, der forårsager reguleringen, f.eks. værdiregulering eller varegebyr.  

### <a name="revaluation-scenario"></a>Værdireguleringsscenarie:  
 Forudsætninger:  

 Opsætning af lager:  

-   Aut. lagerværdibogføring = Ja  

-   Automatisk kostregulering = Altid  

-   Beregn.type for gnsn. kostpris = Vare  

-   Gennemsnitlig omkostningsperiode = Dag  

 Opsætning af Finans:  

-   Bogf. tilladt fra = 1. januar 2014  

-   Bogf. tilladt til = tom  

 Brugeropsætning:  

-   Bogf. tilladt fra = 1. december 2013  

-   Bogf. tilladt til = tom  

##### <a name="to-test-the-scenario"></a>Sådan testes scenariet  

1.  Opret varen TEST:  

     Basisenhed = STK  

     Kostmetode = Gennemsnit  

     Vælg valgfrie bogføringsgrupper.  

2.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Bogføringsdato = 15. december 2013  

     Vare = TEST  

     Posttype = Køb  

     Antal = 100  

     Pris = 10  

3.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Dato = 20. december 2013  

     Vare = TEST  

     Posttype = Nedregulering  

     Antal = 2  

4.  Åbn varekladden, opret og bogfør en linje på følgende måde:  

     Dato = 15. januar, 2014.  

     Vare = TEST  

     Posttype = Nedregulering  

     Antal = 3  

5.  Åbn værdireguleringskladden, opret og bogfør en linje på følgende måde:  

     Vare = TEST  

     Udligningspost = Vælg købspost, der er bogført i trin 2. Bogføringsdatoen for værdireguleringen er den samme som for den post, den regulerer.  

     Kostpris (reguleret) = 40  

 Følgende vare- og værdiposter er bogført:  

![Oversigt over resulterende vare- og værdiposter 1](media/helene/TechArticleAdjustcost9.png "Oversigt over resulterende vare- og værdiposter 1")

 ![Oversigt over resulterende vare- og værdiposter 2](media/helene/TechArticleAdjustcost10.png "Oversigt over resulterende vare- og værdiposter 2")

 Kørslen Juster kostpris - vareposter har registreret en ændring i kostprisen og har justeret de negative reguleringer.  

 **Gennemgang af bogføringsdatoer på oprettede poster med reguleringsværdier:** Den tidligst tilladte bogføringsdato, som kørslen Juster kostpris - vareposter skal forholde sig til, er 1. januar 2014 som angivet i Opsætning af Finans.  

 **Negativ regulering i trin 3:** den tildelte bogføringsdato er 1. januar fra Opsætning af Finans. Bogføringsdatoen for værdiposten i området til regulering er 20. december 2013. I henhold til Opsætning af Finans er datoen ikke inden for det tilladte bogføringsdatointerval. Derfor tildeles den bogføringsdato, der er angivet i feltet Bogf. tilladt fra i Opsætning af Finans, til værdireguleringsposten.  

 **Negativ regulering i trin 4:** den tildelte bogføringsdato er 15. januar. Værdiposten i reguleringen har bogføringsdatoen 15. januar, som er inden for det tilladte bogføringsdatointerval i henhold til Opsætning af Finans.  

 Reguleringen, der er foretaget for nedreguleringen i trin 3 giver problemer. Den favorable bogføringsdato for værdireguleringsposten ville have været 20. december eller i det mindste i december, da værdireguleringen som medfører ændringen i vareforbruget blev bogført i december.  

 For at opnå regulering i december af nedreguleringen i trin 3, skal Opsætning af Finans i feltet Bogf. tilladt fra angive en dato i december.  

 **Konklusion:**  

 Med oplevelserne fra dette scenarie, hvor vi overvejer den mest velegnede opsætning af tilladt bogføringsdatointerval for en virksomhed, kan følgende være nyttigt: Så længe ændringer i lagerværdien må bogføres i en periode, december i det tilfælde, skal den opsætning, virksomheden bruger til tilladte bogføringsdatointervaller, justeres i forhold til beslutningen. Bogf. tilladt fra i Opsætning af Finans angiver 1. december, og det tillader at, værdireguleringen foretaget i december kan sendes til berørte udgående poster i samme periode.  

 Brugergrupper, der ikke må bogføre i december, men i januar, hvilket sandsynligvis var beregnet til at være begrænset af Opsætning af Finans i dette scenarie, skal i stedet behandles via Brugeropsætning.  

### <a name="item-charge-scenario"></a>Scenarie med varegebyr:  
 Forudsætninger:  

 Opsætning af lager:  

-   Aut. lagerværdibogføring = Ja  

-   Automatisk kostregulering = Altid  

-   Beregn.type for gnsn. kostpris = Vare  

-   Gennemsnitlig omkostningsperiode = Dag  

 Opsætning af Finans:  

-   Bogf. tilladt fra = 1. december 2013  

-   Bogf. tilladt til = tom  

 Brugeropsætning:  

-   Bogf. tilladt fra = 1. december 2013  

-   Bogf. tilladt til = tom  

##### <a name="to-test-the-scenario"></a>Sådan testes scenariet  

1.  Opret varegebyr:  

     Basisenhed = STK  

     Kostmetode = Gennemsnit  

     Vælg valgfrie bogføringsgrupper.  

2.  Opret en ny købsordre  

     Leverandørnr.: 10000  

     Bogføringsdato = 15. december 2013  

     Kreditors fakturanr.: 1234  

     På købsordrelinje:  

     Vare = GEBYR  

     Antal = 1  

     Købspris = 100  

     Bogfør modtagelse og faktura.  

3.  Opret en ny salgsordre:  

     Kundenr.: 10000  

     Bogføringsdato = 16. december 2013  

     På salgsordrelinjen:  

     Vare = GEBYR  

     Antal = 1  

     Salgspris = 135  

     Bogfør levering og faktura.  

4.  Opsætning af Finans:  

     Bogf. tilladt fra = 1. januar 2014  

     Bogf. tilladt til = tom  

5.  Opret en ny købsordre:  

     Leverandørnr.: 10000  

     Bogføringsdato = 2. januar 2014  

     Kreditors fakturanr.: 2345  

     På købsordrelinje:  

     Varegebyr = JB-FRAGT  

     Antal = 1  

     Købspris = 3  

     Tildele varegebyrer til købsleverance fra trin 2.  

     Bogfør modtagelse og faktura.  

     ![Oversigt over resulterende vare- og værdiposter 3](media/helene/TechArticleAdjustcost11.png "Oversigt over resulterende vare- og værdiposter 3")

6.  På arbejdsdatoen 3. januar ankommer en købsfaktura, der indeholder et ekstra varegebyr for købet, der er oprettet i trin 2. Fakturaen er dateret 30. december og bogføres derfor med bogføringsdato 30. december 2013.  

     Opret en ny købsordre:  

     Leverandørnr.: 10000  

     Bogføringsdato = 30. december 2013  

     Kreditors fakturanr.: 3456  

     På købsordrelinje:  

     Varegebyr = JB-FRAGT  

     Antal = 1  

     Købspris = 2  

     Tildele varegebyrer til købsleverance fra trin 2  

     Bogfør modtagelse og faktura.  

   ![Oversigt over resulterende vare- og værdiposter 4](media/helene/TechArticleAdjustcost12.png "Oversigt over resulterende vare- og værdiposter 4")

 Lageropgørelsesrapporten udskrives pr. dato 31. december 2013  

![Indholdet i lagerværdirapport](media/helene/TechArticleAdjustcost13.png "Indholdet i lagerværdirapport")

 **Oversigt over scenarie:**  

 Det beskrevne scenarie afsluttes med rapporten Lagerværdi, der viser Antal = 0, mens værdien = 2. Varegebyret, der er bogført i trin 11, er en del af lagerforøgelsesværdien i december, mens lagerfaldet i samme periode ikke påvirkes.  

 Det var godt for det første varegebyr, at Opsætning af Finans angav Bogf. tilladt fra 1. januar. Omkostningerne til lagerforøgelse og -fald blev registreret i samme periode. For anden varegebyret medfører Opsætning af Finans dog, at ændringen i vareforbrug registreres i perioden efter.  

 **Konklusion:**  

 Det er en udfordring, at rapporten Lagerværdi viser antal = 0, mens værdien er <> 0. I dette tilfælde er det også sværere at angive de optimale indstillinger, da købsfakturaer ankommer den samme dag, men drejer sig om forskellige perioder eller endda regnskabsår. Overgangen til et nyt regnskabsår kræver som regel nogen planlægning, og som en del af denne indsigt, skal processen Juster kostpris - vareposter, der genkender vareforbrug, tages i betragtning.  

 I dette scenarie kunne det være en mulighed at lade feltet Bogf. tilladt fra i Opsætning af Finans angive en dato i december i et par dage til, og lade bogføringen af det første varegebyr vente for at tillade, at alle omkostninger fra den forrige periode/det forrige regnskabsår blev genkendt i den periode, hvor de hører til, og køre kørslen Juster kostpris - vareposter og derefter flytte den tilladte bogføringsdato til den nye periode\/det nye regnskabsår. Den første varegebyr med bogføringsdatoen 2. januar kan derefter bogføres.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Oversigt over kørslen Juster kostpris - vareposter  
 Nedenfor vises en oversigt over konceptet for tildeling af bogføringsdatoer til reguleringsværdier i kørslen Juster kostpris - vareposterkørsel.  

### <a name="about-the-request-form-posting-date"></a>Om bogføringsdatoen for anmodningsformularen:  
 Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Juster kostpris - vareposter. Kørslen kører gennem alle nødvendige rettelser og oprettet værdiposter med den bogføringsdato, der er angivet i den værdipost, som justeres. Hvis bogføringsdatoen ikke er inden for det tilladte bogføringsdatointerval, bruges bogføringsdatoen i feltet Bogf. tilladt fra i Opsætning af Finans, ELLER hvis der anvendes lagerperioder, bruges den seneste dato af disse to. Se det beskrevne koncept ovenfor.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Oversigt over kørslen Bogfør lagerregulering  
 Kørslen Bogfør lagerregulering er tæt forbundet med kørslen Juster kostpris - vareposter, hvorfor oversigten over denne kørsel opsummeres og deles også her.  
 
![Faktisk omkostning ift. forventet omkostning](media/helene/TechArticleAdjustcost14.png "Faktisk omkostning ift. forventet omkostning")

### <a name="about-the-posting-date"></a>Om bogføringsdato
 Der skal ikke længere angives en bogføringsdato i anmodningsformularen til kørslen Bogfør lagerregulering. Finansposten oprettes med samme bogføringsdato som den tilknyttede værdipost. Med henblik på at udføre kørslen skal det tilladte bogføringsdatointerval tillade bogføringsdatoen for den tilknyttede finanspost. Hvis ikke, skal det tilladte bogføringsdatointerval midlertidigt åbnes igen ved at ændre eller fjerne datoerne i felterne Bogf. tilladt fra og Bogf. tilladt til i Opsætning af Finans. Det er nødvendigt for at undgå problemer med afstemningen, at bogføringsdato på finansposten svarer til bogføringsdatoen for værdiposten.  

 Kørslen søger i tabel 5811 - Bogfør værdi for at identificere værdiposterne i området til bogføring i Finans. Tabellen tømmes efter korrekt gennemført kørsel.

## <a name="see-also"></a>Se også  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Vareudligning](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
