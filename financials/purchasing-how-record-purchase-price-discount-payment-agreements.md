---
title: Oprette specialpriser og alternative priser og rabatter for kreditorer | Microsoft Docs
description: "Du kan angive forskellige eller alternative priser og rabataftaler og anvende dem på købsdokumenter for kreditorer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c5212bd9e89994ec71cbc4f3613b63571762c31
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrere særlige købspriser og rabatter
De forskellige pris- og betalingsaftaler, der gælder, når du køber fra forskellige leverandører, skal defineres, så de aftalte regler og værdier anvendes i de købsdokumenter, der oprettes for leverandørerne.

Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer. Du kan finde flere oplysninger i afsnittet "Beregning af bedste pris".

Med hensyn til priser kan du få en særlig købspris indsat på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes.

Med hensyn til rabatter kan du oprette og bruge to typer købsrabat:

| Rabattype | Beskrivelse |
| --- | --- |
| **Købslinjerabat** |En beløbsrabat, der indsættes på købslinjerne, hvis en bestemt kombination af leverandør, vare, minimumsantal, enhed eller start-/ slutdato findes. Dette fungerer på samme måde som for købspriser. |
| **Fakturarabat** |En procentvis rabat, der fratrækkes fra dokumenttotalen, hvis værdibeløbet for alle linjer i et købsdokument overstiger et bestemt minimum. |

Da købslinjerabatter og købspriser er baseret på en kombination af vare og leverandør, kan du også angive denne konfiguration fra det varekort, hvor reglerne og værdierne er defineret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Sådan oprettes en særlig købspris for en kreditor
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Priser**.

    Feltet **Indkøbstype** er på forhånd udfyldt med **Kreditor**, og feltet **Indkøbskode** er på forhånd udfyldt med kreditornummer.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Sådan oprettes en linjerabat for en kreditor
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn det relevante kreditorkort, og vælg derefter handlingen **Linjerabatter**.

    Feltet **Indkøbstype** er på forhånd udfyldt med **Kreditor**, og feltet **Indkøbskode** er på forhånd udfyldt med kreditornummer.
3. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Udfyld en linje for hver kombination, som kreditoren yder dig en købslinjerabat for.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Sådan oprettes en fakturarabat for en kreditor
Når dine kreditorer har oplyst, hvilke fakturarabatter de yder, skal du angive fakturarabatkoden på kreditorkortene og definere betingelserne for hver kode.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Åbn kreditorkortet for en kreditor, der kan ydes mængderabat til.
3. Vælg en kode i feltet **Fakturarabatkode** for de fakturarabatbetingelser, som skal bruges til automatisk beregning af fakturarabat til kreditoren.

    > [!NOTE]  
>   Fakturarabatkoder repræsenteres af eksisterende kreditorkort. Det gør det muligt hurtigt at tildele betingelserne for fakturarabatten til kreditorer ved at vælge navnet på en anden leverandører, der skal have samme betingelser.

    Fortsæt med at angive nye fakturarabatbetingelser for køb.
4. I vinduet **Kreditorkort** skal du vælge handlingen **Fakturarabatter**. Vinduet **Kred./fakt.-rabatter** åbnes.
5. Angiv koden for den valuta, som fakturarabatbetingelserne på linjen gælder for, i feltet **Valutakode**. Lad feltet stå tomt for at angive fakturarabatbetingelser for RV.
6. Angiv det minimumsbeløb, der berettiger til rabatten, i feltet **Min. beløb**.
7. I feltet **Rabatpct.** skal du angive fakturarabatten som en procentdel af fakturabeløbet.
8. Gentag trin 5-7 for hver valuta, som kreditoren får en personlig fakturarabat for.

Fakturarabatten er nu oprettet og knyttet til den pågældende kreditor. Når du vælger kreditorkoden i feltet **Fakturarabatkode** på andre kreditorkort, knyttes samme fakturarabat til den pågældende kreditor.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Sådan vælges en metode til bogføring af rabatter  
Når du bogfører en købsfaktura, som der ydes en eller to rabatter på, kan du vælge mellem to metoder til at bogføre mængderabatter. Du kan bogføre rabatter separat, eller du kan fratrække rabatter som fakturarabatter.  

Før du kan gøre dette, skal du allerede have oprettet de nødvendige konti til bogføring af rabatbeløb i kontoplanen. Du skal også kontrollere, at du har angivet de korrekte kontonumre i bogføringsopsætning i felterne **Købslinjerabatkonto** og **Købsfakturarabatkonto**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.
2. Vælg et af følgende bogføringsmetoder i feltet **Bogføring med rabat**.

|**Metode til bogføring af rabat**|**Fakturarabat**|**Linjerabat**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle rabatter**|Bogført separat|Bogført separat|  
|**Fakturarabat**|Bogført separat|Fratrukket|  
|**Linjerabat**|Fratrukket|Bogført separat|  
|**Ingen rabat**|Fratrukket|Fratrukket|  

# <a name="purchase-invoice-discounts-and-service-charges"></a>Købsfakturarabatter og servicegebyrer
Du kan angive de faste betingelser for fakturarabat, som bruges af dine kreditorer. Rabatten beregnes automatisk, når du udfylder en købsfaktura.  

 Før du kan bruge fakturarabatter ved køb, skal du angive de kreditorer, som yder rabat.  

 Du kan sammenkæde rabatprocenter til bestemte fakturabeløb i vinduet **Kred./fakt.-rabatter**. Du kan angive et vilkårligt antal procenter i hvert vindue. Hver debitor kan have sit eget vindue, eller du kan sammenkæde flere debitorer i det samme vindue.  

 Du kan også knytte et servicegebyr til et bestemt fakturabeløb i tillæg til rabatprocenten.  

 Du kan definere, at betingelserne for fakturarabatten er DKK for danske kreditorer og udenlandsk valuta for udenlandske kreditorer.  

 Du kan få [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at beregne fakturarabatter i rekvisitioner, rammeordrer, ordrer, fakturaer og kreditnotaer.  

> [!TIP]  
>  Det anbefales, at du forbereder en skitse over den rabatstruktur, der skal anvendes, før du begynder at indtaste disse oplysninger. Det gør det nemmere at se, hvilke kreditorer der kan knyttes til samme fakturarabatvindue. Jo færre vinduer, du har sat op, jo hurtigere kan du indtaste stamoplysningerne.

## <a name="best-price-calculation"></a>Beregning af bedste pris
Når du har registreret særpriser og linjerabatter for salg og køb, sørger [!INCLUDE[d365fin](includes/d365fin_md.md)] for, at dine avance på varehandel altid er optimal ved automatisk at beregne den bedste pris på salgs- og købsdokumenter og på sags- og varekladdelinjer.

Den bedste pris er den lavest tilladte pris med den størst tilladte linjerabat på en givet dato. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk dette, når enhedsprisen og linjerabatprocenten for varer indsættes på nye dokument- og kladdelinjer.

> [!NOTE]  
>   I det følgende beskrives, hvordan den bedste pris beregnes for salg. Beregningen er den samme for køb.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer kombinationen af faktureringsdebitoren og varen automatisk og beregner derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Har denne kunde en pris-/rabataftale, eller tilhører kunden en gruppe, der har en sådan aftale?
    - Er varen eller varerabatgruppen på linjen medtaget i nogen af disse pris/rabataftaler?
    - Ligger ordredatoen (bogføringsdatoen for faktura- eller kreditnotaen) inden for start- og slutdatoen for pris-/rabataftalen?
    - Er enhedskoden angivet? Hvis den gør det, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)], om der er priser/rabatter med samme enhedskode, og om der er priser/rabatter, uden at der er tilknyttet en enhedskode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om der ligger pris-/ rabataftaler i oplysningerne om dokument- eller kladdelinjen og indsætter derefter den relevante enhedspris og linjerabatprocent ud fra følgende kriterier:

    - Er der et krav om et mindste antal i pris-/ rabataftalen, som er opfyldt?
    - Er der et krav om valuta i pris-/ rabataftalen, som er opfyldt? Hvis der er det, indsættes den laveste pris og den højeste linjerabat for valutaen, selvom RV giver en bedre pris. Hvis der ikke er nogen pris-/rabataftale for den angivne valutakode, indsætter [!INCLUDE[d365fin](includes/d365fin_md.md)] den laveste pris og den højeste linjerabat i RV.

Hvis der ikke kan beregnes en særpris for varen på linjen, indsættes seneste indirekte omkostning eller enhedsprisen fra varekortet.

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

