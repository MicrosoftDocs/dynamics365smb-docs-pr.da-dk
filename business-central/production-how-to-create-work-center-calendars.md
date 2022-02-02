---
title: Konfigurere produktionskalendere
description: Oprettelse og aktivering af en arbejdscenterkalender omfatter flere opgaver, herunder opsætning af produktionskalendere og oprettelse af arbejdsskift.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: ab690e038c3e7c681cea9677e48b35876c567eac
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972771"
---
# <a name="set-up-shop-calendars"></a>Konfigurere produktionskalendere

En arbejdscenter- eller produktionsressourcekalender angiver de arbejdsdage og -timer, arbejdsskift, fridage og det fravær, der bestemmer arbejdscentrets tilgængelige bruttokapacitet, målt i tid, i henhold til centrets definerede værdier for effektivitet og kapacitet.

Som grundlag for at beregne en bestemt arbejdscenter- eller produktionsressourcekalender skal du først opstille en eller flere generelle produktionskalendere. En produktionskalender definerer en standardarbejdsuge i form af start- og sluttidspunkter for hver arbejdsdag og de tilhørende arbejdsskift. Produktionskalenderen definerer desuden de faste fridage i året.  

Nedenstående beskrives, hvordan du opretter arbejdscenterkalendere. Trinene er de samme som ved oprettelse af produktionsressourcekalendere.  

## <a name="to-create-work-shifts"></a>Sådan oprettes arbejdsskift  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsskift**, og vælg derefter det relaterede link.  
2.  Angiv på en tom linje et tal i feltet **Kode** for at identificere arbejdsskiftet, f.eks. **1**.  
3.  Beskriv arbejdsskiftet i feltet **Beskrivelse**, f.eks. **Første skift**.  
4.  Udfyld eventuelt linjer for et andet eller tredje arbejdsskift.  

Selvom arbejdscentrene ikke arbejder i forskellige arbejdsskift, skal du angive mindst én arbejdsskiftkode.  

## <a name="to-set-up-a-shop-calendar"></a>Sådan oprettes en produktionskalender  
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **produktionskalendere**, og vælg derefter det relaterede link.  
2.  Angiv på en tom linje et tal i feltet **Kode** for at identificere produktionskalenderen.  
3.  Beskriv produktionskalenderen i feltet **Beskrivelse**.  
4.  Vælg handlingen **Arbejdsdage**.
5.  På siden **Arb.dage (produktionskalender)** skal du definere en fuldstændig arbejdsuge med start- og sluttidspunkter for hver dag.  

    I feltet **Arbejdsskiftkode** skal du vælge en af de arbejdsskift, du tidligere har defineret. Tilføj en linje for hver arbejdsdag og hvert skift. Eksempler:  

    Mandag 07:00 15:00 1   
    Tirsdag 07:00 15:00 1  

    Hvis du vil oprette en produktionskalender med to arbejdsskift, skal du udfylde den på følgende måde:  

    Mandag 07:00 15:00 1   
    Mandag 15:00 23:00 2  
    Tirsdag 07:00 15:00 1  
    Tirsdag 15:00 23:00 2  

    Alle ugedage, som du ikke definerer i produktionskalenderen, f.eks. lørdag og søndag, anses automatisk for fridage, og de har ingen tilgængelig kapacitet i arbejdscenterkalenderen.  

    Når alle arbejdsdagene i ugen er defineret, kan du lukke siden **Arb.dage (produktionskalender)** og fortsætte med at angive fridage.  

6.  På siden **Produktionskalendere** skal du vælge produktionskalenderen, og derefter vælge handlingen **Helligdage**.
7. På siden **Prod.kalender - fridage** skal du angive årets fridage ved at indtaste startdatoen/-klokkeslættet, sluttidspunktet samt beskrivelsen af hver fridag på enkelte linjer. Eksempler:  

    04-07-14 0:00:00 23:59:00 Sommerferie  
    05-07-14 0:00:00 23:59:00 Sommerferie  
    06-07-14 0:00:00 23:59:00 Sommerferie  

De definerede fridage har ingen tilgængelig kapacitet i en arbejdscenterkalender.  

Produktionskalenderen kan nu knyttes til et arbejdscenter for at beregne den arbejdscenterkalender, der skal styre alle operationsplaner i løbet af tiden på arbejdscentret.  

## <a name="to-calculate-a-work-center-calendar"></a>Sådan beregnes en arbejdscenterkalender  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **arbejdscentre**, og vælg derefter det relaterede link.
2. Åbn det arbejdscenter, du vil opdatere.  
3. Vælg hvilken produktionskalender, der skal bruges som grundlag for en arbejdscenterkalender i feltet **Produktionskalenderkode**.  
4. Vælg handlingen **Kalender**.  
5. På siden **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.  

    I venstre side af matrixsiden vises de konfigurerede arbejdscentre. I højre side vises en tidskalender med værdierne for tilgængelig kapacitet pr. arbejdsdag i den definerede enhed, f.eks. **480** (minutter). Hver linje repræsenterer kalenderen for et arbejdscenter.  

    > [!NOTE]  
    >  Du kan også vælge at få vist kapacitetsværdien for hver uge eller måned ved at ændre indstillingen i feltet **Vis efter** på siden **Arbejdscenterkalender**.  

    For at afspejle den nye produktionskalender som en linje i det markerede arbejdscenter, skal den først beregnes.  

6.  Vælg handlingen **Beregn**.  
7.  Du kan angive et filter i oversigtspanelet **Arbejdscenter**, hvis du kun vil udføre beregningen for ét arbejdscenter. Hvis du ikke filtrerer, beregnes alle eksisterende arbejdscenterkalendere.  
8.  Definer start- og slutdatoerne for den kalenderperiode, der skal beregnes, f.eks. et år fra 01/01/14 til 31/12/14.
9. Vælg knappen **OK** for at beregne kapaciteten.  

Der er nu oprettet (eller opdateret) kalenderindgange, som viser den tilgængelige kapacitet for hver periode i overensstemmelse med følgende 3 sæt stamdata:  

- De arbejdsdage og arbejdsskift, der er defineret i den tilknyttede produktionskalender.  
- Værdien i feltet **Kapacitet** på arbejdscenterkortet.  
- Værdien i feltet **Effektivitet** på arbejdscenterkortet.  

Den beregnede arbejdscenterkalender definerer nu, hvor meget kapacitet der er tilgængelig på dette arbejdscenter. Dette styrer den detaljerede planlægning af operationer, der udføres på arbejdscenter.  

## <a name="to-record-work-center-absence"></a>Sådan registreres fraværet på arbejdscentret  
1.  På siden **Arbejdscenterkalender** skal du vælge handlingen **Vis matrix**.
2. Vælg det arbejdscenter og den kalenderdag, fraværstiden skal registreres for, på siden **Matrix for arbejdscenterkalender**, og klik derefter på handlingen **Fravær**.  
3.  Definer starttidspunktet, sluttidspunktet og beskrivelsen for dagens fravær på siden **Fravær**. Eksempler:  

    25-01-01 08:00 10:00 Reparation  

4.  Vælg handlingen **Opdatering**, og luk derefter siden **Fravær**.  

Kapaciteten på den markerede dag er nu reduceret med den registrerede fraværstid.  

## <a name="see-also"></a>Se også  
[Konfigurere basiskalendere](across-how-to-assign-base-calendars.md)  
[Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]