---
title: Designoplysninger – Vareudligning | Microsoft Docs
description: Dette emne beskriver, hvor lagerantal og værdi registreres, når du bogfører en lagertransaktion.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, items, ledger entries, posting, inventory
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9da76eb0058d2215e6437b52cf68720e663dd4c7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "929547"
---
# <a name="design-details-item-application"></a>Designoplysninger: Vareudligning
Når du bogfører en lagertransaktion, registreres antalsbogføringen i vareposterne og værdibogføringen i værdiposterne. Du kan finde flere oplysninger i [Designoplysninger: Varekladde](design-details-inventory-posting.md).  

Desuden foretages en vareudligning for at sammenkæde modtageren af omkostningerne til kilden for omkostninger for at videresende omkostninger i overensstemmelse med kostmetoden. Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] foretager to typer af vareudligning.  

|Udligningstype|Beskrivelse|  
|----------------------|---------------------------------------|  
|Mængdeudligning|Oprettet for alle lagertransaktioner.|  
|Kostprisudligning|Oprettet for indgående poster sammen med et antalsudligning som følge af brugerinteraktion i særlige processer.|  

Vareudligninger kan gøres på følgende måder.  

|Metode|Beskrivelse|Udligningstype|  
|------------|---------------------------------------|----------------------|  
|Automatisk|Optræder som videresendelse af generelle omkostninger i overensstemmelse med kostmetoden|Mængdeudligning|  
|Fast|Oprettet af brugeren, når:<br /><br /> -   Behandling af returvarer<br />-   Bogføring af rettelser<br />-   Annullere antalsbogføringer<br />-   Oprettelse af direkte leveringer **Bemærk:** Fast udligning kan foretages manuelt ved at indtaste et løbenummer i feltet **Udlign fra varepost** eller ved hjælp af en funktion, f.eks. **Hent bogførte bilagslinjer, der skal tilbageføres**.|Mængdeudligning<br /><br /> Kostprisudligning **Bemærk:** Kostprisudligning sker kun i indgående transaktioner, hvor feltet **Udlign fra varepost** udfyldes for at oprette en fast udligning. Se den næste tabel.|  

Om der oprettes antals- eller kostprisudligninger, afhænger af retningen af lagertransaktionen, og om vareudligningen foretages automatisk eller fast i forbindelse med særlige processer.  

I følgende tabel vises, baseret på de centrale felter på lagerposteringslinjer, hvordan omkostninger strømmer afhængigt af retningen for posteringen. Den angiver også, hvornår og hvorfor vareudligningen er af typen antal eller omkostning.  

||Feltet Udl.varepostløbenr.|Feltet Udlign fra-varepost|  
|-|--------------------------------|----------------------------------|  
|Udligning for udgående post|Den udgående post trækker omkostningen fra den åbne indgående post.<br /><br /> **Mængdeudligning**|Ikke understøttet|  
|Udligning for indgående post|Den indgående post trækker omkostningen til den åbne udgående post.<br /><br /> Den indgående post er kilden til omkostninger.<br /><br /> **Mængdeudligning**|Den indgående post trækker omkostningen fra den udgående post. **Bemærk:** Når du foretager denne faste udligning, behandles den indgående transaktion som en salgsreturvare. Derfor forbliver den anvendte udgående post åben. <br /><br /> Den indgående post er IKKE kilden til omkostninger.<br /><br /> **Kostprisudligning**|  

> [!IMPORTANT]  
>  En salgsreturvare anses IKKE for en omkostningskilde, når den anvendes fast.  
>   
>  Salgsposteringen forbliver åben, indtil den rigtige kilde er bogført.  

Følgende oplysninger registreres i en vareudligningspost.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Varepostløbenr.**|Nummeret på den varepost for transaktionen, som udligningsposten oprettes for.|  
|**Indgående varepostløbenr.**|Varepostnummeret på den lagerforøgelse, som transaktionen skal knyttes til, hvis det er relevant.|  
|**Udgående varepostløbenr.**|Varepostnummeret på den lagerreduktion, som transaktionen skal knyttes til, hvis det er relevant.|  
|**Antal**|Det antal, der udlignes.|  
|**Bogføringsdato**|Transaktionens bogføringsdato.|  

## <a name="inventory-increase"></a>Lagerforøgelse  
Når du bogfører en lagerforøgelse, registreres der en simpel vareudligningspost uden en udligning med en udgående post.  

### <a name="example"></a>Eksempel  
Følgende tabel viser den vareudligningspost, der oprettes, når du bogfører en købsleverance på 10 enheder.  

|Bogføringsdato|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|Varepostløbenr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease"></a>Lagerreducering  
Når du bogfører en lagerreduktion, oprettes der en vareudligningspost, der knytter lagerreduktionen til en lagerforøgelse. Dette link oprettes ved at bruge varens kostmetode som retningslinje. For varer, der bruger kostmetoden FIFO, Standard og Gennemsnit, er tilknytningen baseret på princippet først ind-først ud. Der lagerreduktionen anvendes til lagerforøgelsen, der har den tidligste bogføringsdato. For varer, der bruger kostmetoden LIFO, er tilknytningen baseret på princippet sidst ind-først ud. Lagerreduktionen anvendes til lagerforøgelsen, der har den nyeste bogføringsdato.  

I tabellen **Varepost** viser feltet **Restantal** det antal, som endnu ikke er blevet udlignet. Hvis restantallet er større end 0, vil afkrydsningsfeltet **Åben** være markeret.  

### <a name="example"></a>Eksempel  
Det følgende eksempel viser den vareudligningspost, der oprettes, når du bogfører en salgsleverance på 5 enheder af de varer, der blev modtaget i det forrige eksempel. Den første vareudligningspost er købsleverancen. Den anden udligningspost er salgsleverancen.  

Følgende tabel viser de to vareudligningsposter, der skyldes henholdsvis lagerforøgelsen og lagerreduceringen.  

|Bogføringsdato|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|Varepostløbenr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  

## <a name="fixed-application"></a>Fast udligning  
Du foretager faste udligninger, når du angiver, at kostprisen for en lagerforøgelse skal udlignes med en bestemt lagerreduktion eller vice versa. Den faste udligning har indflydelse på det resterende antal i posterne, men den faste udligning tilbagefører også den præcise kostpris for den oprindelige post, du udligner til eller fra.  

Hvis du vil foretage en fast udligning, skal du bruge felterne **Udl.varepostløbenr.** eller **Udlign fra varepost** på de bilagslinjer, der angiver den varepost, som transaktionslinjen skal udlignes til eller fra. Du kan f.eks. foretage en fast udligning, hvis du vil oprette en kostprisudligning, der angiver, at en salgsreturvareordre skal udlignes med en bestemt salgsleverance for at kostprisen for salgsleverancen kan tilbageføres. I dette tilfælde tilsidesætter [!INCLUDE[d365fin](includes/d365fin_md.md)] kostmetoden og anvender lagerreduktionen eller forøgelsen for en salgsreturvare på den varepost, du angiver. Fordelen ved en fast udligning er, at kostprisen for den oprindelige transaktion overføres til den nye transaktion.  

### <a name="example--fixed-application-in-purchase-return"></a>Eksempel – Fast udligning i købsreturvare  
Følgende eksempel, som illustrerer virkningen af fast udligning af en købsreturvare, der bruger kostmetoden FIFO, er baseret på følgende scenario:  

1. I post 1 bogfører brugeren et køb til en kostpris på RV 10,00.  
2. I post 2 bogfører brugeren et køb til en kostpris på RV 20,00.  
3. I post 3 bogfører brugeren en købsreturvare. Brugeren foretager en fast udligning med det andet køb ved at angive varepostnummeret i feltet **Udl.varepostløbenr.** på ordrelinjen for købsreturvaren.  

Følgende tabel viser de vareposter, der er resultatet af scenariet.  

|**Bogføringsdato**|**Vareposttype**|**Antal**|**Kostbeløb (faktisk)**|**Varepostløbenr.**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Køb|10|10.00|1|  
|01-05-20|Køb|10|20.00|2|  
|01-06-20|Køb (returvare)|-10|-20,00|3|  

Da en fast udligning sker fra købsreturvaren til den anden købspost, returneres varerne til den rigtige pris. Hvis brugeren ikke har udført fast udligning, vil den returnerede vare være forkert værdiansat til RV 10,00, da returnering ville have været gældende for den første købspost efter FIFO-princippet.  

Følgende tabel viser den vareudligningspost, der skyldes fast udligning.  

|Bogføringsdato|Indgående varepostløbenr.|Udgående varepostløbenr.|Antal|Varepostløbenr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|2|3|10|3|  

Kostprisen for det andet køb, RV 20,00, vil derefter blive overført korrekt til købsreturvareordren.  

### <a name="example--fixed-application-with-average-cost"></a>Eksempel – Fast udligning med gennemsnitlig kostpris  
Følgende eksempel, som illustrerer virkningen af fast udligning, er baseret på følgende scenario for en vare, der bruger kostmetoden Gennemsnit:  

1. Brugeren bogfører to købsfakturaer i postnummer 1 og 2. Den anden faktura har en forkert købspris på RV 1000,00.  
2. Brugeren bogfører en købskreditnota, med en fast udligning, der er anvendt på købsposten med den forkerte købspris i post nummer 3. Summen af feltet **Kostbeløb (faktisk)** for de to fast udlignede værdiposter bliver 0,00  
3. I løbenummer 4 bogfører brugeren en anden købsfaktura med den korrekte købspris på RV 100,00  
4. I post nummer 5 bogfører brugeren en salgsfaktura.  
5. Lagerantallet er 0, og lagerværdien er også 0,00  

Følgende tabel viser effekten af scenariet på værdiposterne for varen.  

|Bogføringsdato|Vareposttype|Værdiansat antal|Kostbeløb (faktisk)|Udl.varepostløbenr.|Værdisat efter gnsn. kostpris|Varepostløbenr.|Løbenummer|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Køb|1|200.00||Nej|1|1|  
|01-01-20|Køb|1|1000.00||Nej|2|2|  
|01-01-20|Køb|-1|-1000|2|Nej|3|3|  
|01-01-20|Køb|1|100.00||Nej|4|4|  
|01-01-20|Salg|-2|-300,00||Ja|5|5|  

Hvis brugeren ikke havde foretaget fast udligning mellem købskreditnotaen og købet med forkert købspris (trin 2 i det forrige scenario), ville omkostningerne være blevet justeret anderledes.  

I følgende tabel vises resultatet i værdiposterne for varen, hvis trin 2 er udført i det forrige scenario uden en fast udligning.  

|Bogføringsdato|Vareposttype|Værdiansat antal|Kostbeløb (faktisk)|Udl.varepostløbenr.|Værdisat efter gnsn. kostpris|Varepostløbenr.|Løbenummer|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Køb|1|200.00||Nej|1|1|  
|01-01-20|Køb|1|1000.00||Nej|2|2|  
|01-01-20|Køb|-1|433.33||Ja|3|3|  
|01-01-20|Køb|1|100.00||Nej|4|4|  
|01-01-20|Salg|-2|866,67||Ja|5|5|  

I post nummer 3 er værdien i feltet **Kostbeløb (faktisk)** værdisat efter gennemsnit og indeholder derfor forkert bogføring af 1000,00. Derfor bliver det -433,33, som er en oppustet kostpris. Udregningen er 1300 / 3 = .-433,33.  

I post nummer 5 er værdien af feltet **Kostbeløb (faktisk)** for denne post også unøjagtig af samme grund.  

> [!NOTE]  
>  Hvis du opretter en fast udligning for en lagerreduktion for en vare, der bruger kostmetoden Gennemsnit, vil reduktionen ikke som sædvanlig modtage den gennemsnitlige kostpris for varen, men den vil i stedet modtage kostprisen for den lagerforøgelse, du har angivet. Den lagerreduktion er derefter ikke en del af beregningen af den gennemsnitlige kostpris.  

### <a name="example--fixed-application-in-sales-return"></a>Eksempel – Fast udligning i salgsreturvare  
Faste udligninger er også en meget god måde til at tilbageføre omkostninger nøjagtigt, som f.eks. ved salgsreturvarer.  

Følgende eksempel, som illustrerer, hvordan fast udligning sikrer præcis kostprisudligning, er baseret på følgende scenario:  

1.  Brugeren bogfører en købsfaktura.  
2.  Brugeren bogfører en salgsfaktura.  
3.  Brugeren bogfører en salgskreditnota for den returnerede vare, som udlignes med salgsposten, for at tilbageføre omkostninger korrekt.  
4.  Fragtomkostninger, der er relateret til den købsordre, der blev bogført tidligere, ankommer. Brugeren bogfører det som et varegebyr.  

Tabellen nedenfor viser resultatet af scenarietrin 1 til 3 på varens værdiposter.  

|Bogføringsdato|Vareposttype|Værdiansat antal|Kostbeløb (faktisk)|Udlign fra-varepost|Varepostløbenr.|Løbenummer|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Køb|1|1000.00||1|1|  
|02-01-20|Salg|-1|1000.00||2|2|  
|03-01-20|Salg (kreditnota)|1|1000|2|3|3|  

Følgende tabel viser den værdipost, der følger af scenarietrin 4, der bogfører varegebyret.  

|Bogføringsdato|Vareposttype|Værdiansat antal|Kostbeløb (faktisk)|Udlign fra-varepost|Varepostløbenr.|Løbenummer|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Varegebyr)|1|100.00||1|4|  

Følgende tabel viser effekten af præcis kostprisudligning i værdiposterne for varen.  

|Bogføringsdato|Vareposttype|Værdiansat antal|Kostbeløb (faktisk)|Udlign fra-varepost|Varepostløbenr.|Løbenummer|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Køb|1|1000.00||1|1|  
|02-01-20|Salg|-1|1100.00||2|2|  
|03-01-20|Salg (kreditnota)|1|1100.00|2|3|3|  
|04-01-20|(Varegebyr)|1|100.00||1|4|  

Når du udfører kørslen **Juster kostpris - vareposter**, videreføres de forøgede omkostninger på købsposten på grund af varegebyret til salgsposten (løbenummer 2). Salgsposten overfører derefter denne forøgede omkostning til salgskreditposten (løbenummer 3). Det endelige resultat er, at omkostningerne er tilbageført korrekt.  

> [!NOTE]  
>  Hvis du arbejder med returvareordrer eller kreditnotaer, og du har indstillet feltet **Obl. beløbstilbageførsel** på enten siden **Købsopsætning** eller siden **Salgsopsætning**, som det nu er relevant for dig, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk disse felter, når du bruger funktionen **Kopiér dokument**. Hvis du bruger funktionen **Hent bogførte bilagslinjer**, udfyldes felterne altid automatisk.  

> [!NOTE]  
>  Hvis du bogfører en transaktion med en fast udligning, og den varepost, du udligner, er lukket, dvs. restantallet er nul, annulleres den gamle udligning automatisk, og derefter udlignes vareposten igen med den faste udligning, du har angivet.  

## <a name="transfer-application"></a>Overfør udligning  
Når en vare overflyttes fra én placering til en anden inden for virksomhedens lager, oprettes der en udligning mellem de to overflytningsposter. Værdiansættelse af en overflytningspost afhænger af kostmetoden. For varer, der bruger kostmetoden Gennemsnit, foretages værdiansættelsen ved hjælp af den gennemsnitlige kostpris i den gennemsnitlige omkostningsperiode, hvori værdiansættelsesdatoen for overførslen sker. For varer, der benytter andre kostmetoder, foretages værdiansættelse ved sporing tilbage til kostprisen for den oprindelige lagerforøgelse.  

### <a name="example--average-costing-method"></a>Eksempel – Gennemsnitlig kostmetode  
Følgende eksempel, som illustrerer, hvordan overførselsposter anvendes, er baseret på følgende scenario for en vare, der bruger kostmetoden Gennemsnit og en gennemsnitlig omkostningsperiode på en dag.  

1. Brugeren køber varen til en pris på RV 10,00.  
2. Brugeren køber varen igen til en pris på RV 20,00.  
3. Brugeren overflytter varer fra lokationen BLÅ til RØD.  

Følgende tabel viser effekten af overførslen på værdiposterne for varen.  

|Bogføringsdato|Vareposttype|Lokationskode|Værdiansat antal|Kostbeløb (faktisk)|Løbenummer|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Køb|BLÅ|1|10.00|1|  
|01-01-20|Køb|BLÅ|1|20.00|2|  
|02-01-20|Overførsel|BLÅ|-1|15.00|3|  
|02-01-20|Overførsel|RØD|1|15.00|4|  

### <a name="example--standard-costing-method"></a>Eksempel – standardkostmetode  
Følgende eksempel, som illustrerer, hvordan overførselsposter anvendes, er baseret på følgende scenario for en vare, der bruger kostmetoden Standard og en gennemsnitlig omkostningsperiode på en dag.  

1. Brugeren køber varen til en standardpris på RV 10,00.  
2. Brugeren overfører varen fra lokationen BLÅ til RØD med en standardkostpris på RV 12,00.  

Følgende tabel viser effekten af overførslen på værdiposterne for varen.  

|Bogføringsdato|Vareposttype|Lokationskode|Værdiansat antal|Kostbeløb (faktisk)|Løbenummer|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Køb|BLÅ|1|10.00|1|  
|02-01-20|Overførsel|BLÅ|-1|10,00|2|  
|02-01-20|Overførsel|RØD|1|10,00|3|  

Da værdien af den oprindelige lagerforøgelse er RV 10,00, er overførslen værdisat til denne kostpris, ikke RV 12,00.  

## <a name="reapplication"></a>Genudligning  
På grund af den måde, som kostprisen på en vare beregnes, kan en forkert vareudligning føre til en forkert gennemsnitlig kostpris og en forkert kostpris. Følgende situationer kan medføre forkerte vareudligninger, som kræver, at du fortryder vareudligninger og genanvender vareposter:  

* Du har glemt at foretage en fast udligning.  
* Du har oprettet en forkert fast udligning.  
* Du ønsker at tilsidesætte den udligning, der oprettes automatisk, når du bogfører, i henhold til varens kostmetode.  
* Du skal returnere en vare, hvor salget allerede er udlignet manuelt, uden at bruge funktionen **Hent bogførte bilagslinjer, der skal tilbageføres**, og du skal derfor fortryde udligningen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en funktion, der analyserer og korrigerer vareudligninger. Dette arbejde udføres på siden **Udligningskladde**.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Kendt problem med vareudligning](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)  
[Designoplysninger: Kostmetoder](design-details-costing-methods.md)  
[Designoplysninger: Gennemsnitlig kostpris](design-details-average-cost.md)   
[Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
