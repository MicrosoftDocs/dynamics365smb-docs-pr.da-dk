---
title: "Tælle, justere og ompostere inventar | Microsoft Docs"
description: "Beskriver, hvordan du foretager fysisk optælling, foretag negative eller positive reguleringer, hvordan du kan redigere oplysninger, f.eks. placering eller lotnummer, på vareposter eller lagerstedsposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Fremgangsmåde: Tælle, justere og ompostere inventar
Mindst én gang hvert regnskabsår skal der foretages lageropgørelse, dvs. alle varer i lagerbeholdningen optælles for at se, om det antal, der er registreret i databasen, svarer til det faktiske fysiske antal på lagerstederne. Når det faktiske fysiske antal kendes, skal det bogføres til Finans som en del af lagervurderingen ved periodeafslutning.

Selvom alle varer på lageret optælles mindst en gang om året, har du måske besluttet, at nogle varer skal optælles oftere. Det kan være fordi, der er tale om særligt dyre vare, eller fordi de har en stor omsætningshastighed og udgør hovedparten af salget. Du kan tildele særlige optællingsperioder til de pågældende varer til dette formål. Du kan finde flere oplysninger i afsnittet "Sådan udføres periodisk optælling".

Hivs der er brug for en regulering af de registrerede lagerantal i forbindelse med optælling eller af andre årsager, kan du bruge en varekladde til at ændre lageropgørelsesposterne direkte, uden at bogføre forretningstransaktioner. Du kan også justere for en enkelt vare på varekortet.

Hvis det er nødvendigt at ændre attributter for varekladdeposter udover antallene, kan du bruge vareomposteringskladden. Blandt det attributter, der kan omposteres, er typisk serie-/lotnumre, udløbsdatoer og dimensioner.

## <a name="to-perform-a-physical-inventory"></a>Sådan foretages en lageropgørelse
Du skal foretage en lageropgørelse ved udgangen af hvert regnskabsår eller oftere, dvs. tælle antallet af fysiske varer, for at kontrollere, om det antal, der er registreret, er det samme som det fysiske antal varer, der er på lager. Hvis der er forskelle, skal du bogføre dem på de relevante varekonti, før du foretager en værdiansættelse af lageret.

Ud over den fysiske optællingsopgave omfatter hele processen følgende tre opgaver:

- Beregning af den forventede lagerbeholdning.
- Udskrivning af rapporten, der skal bruges til optælling.
- Indtastning og bogføring af den faktiske optalte lagerbeholdning.

### <a name="to-calculate-the-expected-inventory"></a>Sådan beregnes den forventede lagerbeholdning
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lageropgørelseskladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn beholdning**.
3. I vinduet **Beregn beholdning** skal du angive betingelserne, der skal bruges til at oprette kladdelinjerne, f.eks. om der skal medtages varer med ingen registreret lagerbeholdning.
4. Angiv filtre, hvis du kun vil beregne lagerbeholdningen for visse varer, placeringer, lokationer eller dimensioner.
5. Vælg knappen **OK**.

> [!NOTE]  
>   Vareposterne behandles i overensstemmelse med de oplysninger, du har angivet, og der oprettes linjer i lageropgørelseskladden. Bemærk, at feltet **Antal (optalt)** udfyldes automatisk med det samme antal som feltet **Antal (beregnet)**. Med denne funktion er det ikke nødvendigt at indtaste den optalte lagerbeholdning for varer, der er de samme som det beregnede antal. Men hvis det optalte antal afviger fra det, der er indtastet i feltet **Antal (beregnet)**, skal du overskrive det med det antal, der faktisk er optalt.

### <a name="to-print-the-report-used-when-counting"></a>Sådan udskrives rapporten, der bruges ved optælling
1. I vinduet **Lageropgørelseskladde**, der indeholder den beregnede forventede lagerbeholdning, skal du vælge **Udskriv**.
2. I vinduet **Lageropgørelsesoversigt** skal du angive, om rapporten skal vise det beregnede antal, og om rapporten skal indeholde lagervarer med serie- og lotnumre.
3. Angiv filtre, hvis du kun vil udskrive rapporten for visse varer, placeringer, lokationer eller dimensioner.
4. Vælg knappen **Udskriv**.

Medarbejderne kan nu fortsætte med at optælle lagerbeholdningen og registrere eventuelle afvigelser på den udskrevne rapport.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Sådan indtastes og bogføres den faktiske optalte lagerbeholdning
1. På hver linje i vinduet **Lageropgørelseskladde**, hvor den faktiske lagerbeholdning, der er optalt manuelt, afviger fra det beregnede antal, skal du indtaste den faktiske lagerbeholdning i feltet **Antal (optalt)**.

    Relaterede felter opdateres tilsvarende.

    > [!NOTE]  
>   Hvis den fysiske optælling afslører forskelle, som skyldes, at varer er blevet bogført med forkerte lokationskoder, skal du ikke angive forskellene i lageropgørelseskladden. Brug i stedet omposteringskladden eller en overflytningsordre til at omdirigere varerne til de rigtige steder. Du kan finde flere oplysninger under Vareomposteringskladde eller Sådan oprettes overflytningsordrer.

2. Hvis du vil regulere det beregnede antal til det faktiske optalte antal, skal du vælge handlingen **Bogfør**.

    Både vareposter og lageropgørelsesposter oprettes. Åbn varekortet for at få vist de oprettede lageropgørelsesposter.

3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
4. For at kontrollere lageropgørelsen skal du åbne det relevante varekort og vælge handlingen **Lageropgørelsesposter**.

# <a name="to-perform-cycle-counting"></a>Sådan udføres periodisk optælling
Selvom alle varer på lageret optælles mindst en gang om året, har du måske besluttet, at nogle varer skal optælles oftere. Det kan være fordi, der er tale om særligt dyre vare, eller fordi de har en stor omsætningshastighed og udgør hovedparten af salget. Du kan tildele særlige optællingsperioder til de pågældende varer til dette formål.

> [!NOTE]  
>   Hvis lokationen er konfigureret til styret læg-på-lager og pluk, skal du først bruge vinduet **Lagersted - fysisk lagerkladde** og derefter skal du bruge funktionen **Beregn regulering (logistik)** i vinduet **Varekladde**.

## <a name="to-set-up-counting-periods"></a>Sådan defineres optællingsperioder
Lageropgørelser foretages typisk med et fast interval, f.eks. hver måned, hvert kvartal eller årligt. Der er ingen begrænsninger med hensyn til lageroptællingsperioder.

Du konfigurerer hver lageroptællingsperiode, du vil bruge, og knytter en til hver vare. Når du foretager en lageropgørelse og bruger **Beregn optællingsperiode** i lageropgørelseskladden, bogføres linjer for varerne, der oprettes, automatisk.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lageropgørelse - optællingsperioder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Sådan tildeles en optællingsperiode til en vare  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2. Vælg den vare, som der skal knyttes en optællingsperiode til.  
3. I feltet **Lageropg.-optællingsperiodekode** skal du vælge den relevante optællingsperiode.  
4. Vælg knappen **Ja** for at ændre koden og beregne den første optællingsperiode for varen. Næste gang du vælger at beregne en optællingsperiode i opgørelseskladden, vises elementet som en linje i vinduet **Lageropgørelse – varevalg**. Du kan derefter begynde at optælle varen på regelmæssig basis.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Sådan foretages en optælling baseret på optællingsperioder
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lageropgørelseskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Beregn optællingsperiode**.

    Vinduet **Lageropgørelse - varevalg**, der viser de varer, der er tildelt optællingsperioder til, og som skal optælles, åbnes.
3. Foretag lageropgørelsen. Du kan finde flere oplysninger i afsnittet "Sådan foretages en lageropgørelse".

## <a name="to-adjust-the-inventory-of-one-item"></a>Sådan regulerer du lagerbeholdningen for én vare
Når du har foretaget en fysisk optælling af varen i dit lagerområde, kan du bruge funktionen **Reguler lager** til at registrere den faktiske lagerbeholdning.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg den vare, som du vil regulere lagerbeholdningen for, og vælg derefter handlingen **Reguler lager**.
3. Angiv det maksimale lagerantal, du vil registrere for varen, i feltet **Ny lagerbeholdning**.
4. Vælg knappen **OK**.

Varens lager er nu reguleret. Det nye antal vises i feltet **Aktuel lagerbeholdning** i vinduet **Reguler lager** og i feltet **Lager** i vinduet **Varekort**.

Du kan også bruge funktionen **Reguler lager** som en enkel måde at placere købte varer på lager, hvis du ikke bruger købsfakturaer eller -ordrer til at registrere dine køb. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Når du har reguleret lageret, skal du opdatere det med den aktuelle, beregnede værdi. Du kan finde flere oplysninger under [Fremgangsmåde: Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Sådan justeres lagerantallet for en eller flere varer
I vinduet **Varekladde** kan du bogføre varetransaktionen direkte for at regulere lagerbeholdningen i forbindelse med køb, salg og op- og nedregulering af lageret uden brug af dokumenter.

Hvis du ofte bruger varekladden til at bogføre de samme eller lignende kladdelinjer, f.eks. i forbindelse med materialeforbrug, kan du bruge vinduet **Standardvarekladde** til at lette denne gentagne opgave. Du kan finde flere oplysninger i afsnittet "Standardkladder" i [Arbejde med finanskladder](ui-work-general-journals.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vælg handlingen **Bogfør** for at regulere lagerbeholdningen.

> [!NOTE]  
>   Når du har reguleret lageret, skal du opdatere det med den aktuelle, beregnede værdi. Du kan finde flere oplysninger under [Fremgangsmåde: Regulere lagerbeholdningen](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Sådan omposteres en vares lotnummer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. I vinduet **Vareomposteringskladder** skal du udfylde felterne efter behov.
3. I feltet **Lotnr.** skal du angive det aktuelle lotnummer på varerne.
4. I feltet **Nyt lotnr.** skal du angive varens nye lotnummer.
5. Vælg handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

