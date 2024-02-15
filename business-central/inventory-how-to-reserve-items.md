---
title: Sådan reserveres varer
description: 'Flere oplysninger om at reservere varer til salgsordrer, købsordrer og produktionsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="reserve-items"></a>Reservere varer

Du kan reservere varer til salgsordrer, købsordrer, serviceordrer, montageordrer, overførselsordrer og produktionsordrer. Du kan også reservere varer i lagerbeholdning eller indgående varer på åbne dokumentlinjer eller kladdelinjer. Det kan du gøre på siden **Reservation**.

Hver linje på siden **Reservation**, som du åbner for at reservere varer, indeholder oplysninger om én type linje (salg, køb, kladde) eller lagerpost. Linjerne beskriver, hvor mange varer, der er tilgængelige for reservation fra hver linje eller post.

> [!TIP]
> Ud fra de antal, du har reserveret på lageret, viser [!INCLUDE [prod_short](includes/prod_short.md)] en status på dokumenterne, så du hurtigt er klar over det næste trin. Hvis du f.eks. vil angive, at du kan levere en salgsordre eller begynde at arbejde på en sag, en montage eller en produktionsordre. Status er også med til at reducere risikoen for utilsigtede delleverancer eller forsinkelser på grund af manglende lager til produktions- og montageordrer.
>
> Feltet **Reserveret fra lager** kan hjælpe dig med at forstå, om du kan levere eller plukke til en bestemt ordre eller ordrelinje. For linjer er feltet Reserveret fra lager tilgængeligt i faktabokse. Hvis du vil have adgang til oplysninger for hele ordren, findes feltet på siden **Statistik**.

## <a name="reserve-items-for-sales"></a>Reservere varer til salg

Nedenfor kan du se, hvordan du reserverer varer fra en salgsordre. Trinene er de samme for købs-, service-, overførsels- og montageordrer.
  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Vælg salgsordren.
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Reserver**. Siden **Reservation** åbnes.  
4. Vælg den linje, du vil reservere varerne fra.  
5. Vælg en af følgende handlinger.  

    |**Funktion**|**Beskrivelse**|
    |------------------|---------------------|  
    |**Reserver automatisk**|Hvis du automatisk vil reservere varer på siden **Reservation**.|  
    |**Reserver fra aktuel linje**|Hvis du vil reservere varer fra dokumentet på den linje, som du har markeret.|  
    |**Annuller reservation fra aktuel linje**|Hvis du vil annullere reservationen af varerne fra dokumentet på den linje, som du har markeret.|

> [!NOTE]  
> Hvis der findes varesporingslinjer til salgsordren, skal du følge de specielle trin i reservationssystemet. Du kan finde flere oplysninger i [Sådan reserveres et bestemt serienummer eller lotnummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line"></a>Reservere en vare til en produktionsordrelinje

Du kan reservere varer til en produktionsordre. Du skal skelne mellem produktionsordrelinjer, dvs. den overordnede vare, og produktionsordrekomponenter.

I proceduren nedenfor anvendes en fastlagt produktionsordre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagt produktionsordre**, vælg derefter det relaterede link.  
2. Åbn den fastlagte produktionsordre, du vil reservere overordnede varer for.  
3. Marker den relevante produktionsordrelinje.  
4. I oversigtspanelet **Linjer** skal du vælge handlingen **Reserver**.
5. Vælg linjen **Salgslinje, ordre** på siden **Reservation**, vælg derefter handlingen **Reserver fra aktuel linje**.  

Programmet har nu reserveret den mængde, du har angivet på den firmaplanlagte produktionsordrelinje.

## <a name="reserve-items-for-production-order-components"></a>Reservere varer til produktionsordrekomponenter

Du kan reservere varer til en produktionsordre. Du skal skelne mellem produktionsordrelinjer, dvs. den overordnede vare, og produktionsordrekomponenter.

I proceduren nedenfor anvendes en fastlagt produktionsordre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagt produktionsordre**, vælg derefter det relaterede link.  
2. Åbn den fastlagte produktionsordre, du vil reservere komponentvarer for.  
3. Marker den relevante produktionsordrelinje.  
4. I oversigtspanelet **Linjer** skal du vælge **Linje**, derefter vælge **Komponenter**.  
5. Marker den relevante komponentlinje.  
6. I oversigtspanelet **Linjer** skal du vælge handlingen **Reserver**.  
7. Vælg en linje på siden **Reservation**, vælg derefter handlingen **Reserver fra aktuel linje**.  

Programmet har nu reserveret den mængde, du har angivet på den firmaplanlagte produktionskomponentlinje.

## <a name="reserve-items-in-bulk"></a>Reserver varer samlet

Brug siden **Reservationskladde** til at reservere og masseallokere indgående varer. Massereservationer kan f.eks. være med til at sikre, at der er antal til rådighed for salgs- og produktionsordrer. Du kan have flere batches til forskellige formål. Du kan f.eks. allokere produktionsordrer på ugentlig basis, men reservere daglige til salg.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Reservationskladde**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Hent behov**, og angiv derefter den type behov, du vil reservere fra tilgængeligt lager.
3. Du kan vælge en af følgende indstillinger i feltet **Reserveret fra lager**:
    
   |Felt  |Beskrivelse  |
   |---------|---------|
   |Tom     | Det udestående antal reserveres slet ikke, eller det reserveres fra andre kildedokumenter, f.eks. købsordrer.        |
   |Fuld    |  Den udestående mængde er helt reserveret fra tilgængeligt lager.       |
   |Delvis     | Den udestående mængde er delvist reserveret fra tilgængeligt lager.        |

4. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
5. Valgfrit: Hvis du vil allokere varerne med det samme, skal du vælge handlingen **Alloker**.
6. Vælg en politik for hvert trin på siden **Allokeringspolitik**

   |Allokeringspolitik  |Beskrivelse  |
   |---------|---------|
   |Basis     | Allokerer lageret til et behov, hvis der ikke er nogen konflikter, og behovet kan dækkes fuldt ud. Du har f.eks. salgsordre A med et antal på 10 og en sag med et antal på 7. Hvis du har 20 på lager, modtager begge krav fuld mængde. Hvis dit lager er 12, tildeles der ikke noget lager. Du skal allokere mængden manuelt.        |
   |Ligeligt    | Fordeler det disponible lager ligeligt efter behov. Du har f.eks. en salgsordre med et antal på 10 og en sag med et antal på 7. Hvis dit lagerniveau er 20, modtager begge krav fuld mængde. Hvis dit lager er 12, får begge krav 6.        |

7. Hvis du vil reservere alle linjer, hvor **Accepter** er slået til, skal du vælge handlingen Foretag **reservation** .
    
## <a name="change-a-reservation"></a>Ændre en reservation

Du kan ændre en varereservation.

1. Fra den bilagslinje, du har reserveret fra, skal du i oversigtspanelet **Linjer** vælge handlingen **Reserver**.  
2. På siden **Reservation** skal du vælge handlingen **Reservationsposter**.
3. På siden **Reservationsposter** skal du opdatere feltet **Antal** på den linje, du vil ændre.
4. Bekræft den efterfølgende meddelelse ved at vælge knappen **OK**.

## <a name="cancel-a-reservation"></a>Annullere en reservation

Du kan annullere en varereservation.

1. Fra den bilagslinje, du vil annullere en reservation fra, skal du i oversigtspanelet **Linjer** vælge handlingen **Reserver**.  
2. På siden **Reservation** skal du vælge handlingen **Reservationsposter**.  
3. På siden **Reservationsposter** skal du vælge handlingen **Annuller reservation**.  
4. Bekræft den efterfølgende meddelelse ved at vælge knappen **Ja**.  

## <a name="reserve-a-specific-serial-or-lot-number"></a>Reservere et bestemt serienummer eller lotnummer

Fra udgående dokumenter for varer med varesporing, f.eks. salgsordrer eller produktionskomponentlister, kan du reservere bestemte serie- eller lotnumre. Det kan f.eks. være nyttigt at reservere bestemte serie- eller lotnumre i følgende situationer:

* Hvis du har brug for produktionskomponenter fra et bestemt lot for at sikre ensartethed i forhold til tidligere produktionsbatches.
* Fordi en kunde har anmodet om et bestemt serienummer. 

Du kan finde flere oplysninger i [Arbejde med serie- og lotnumre](inventory-how-work-item-tracking.md).

Dette kaldes en bestemt reservation, fordi du reserverer fra antallet af varen X, som tilhører partiet X. Hvis du blot reserverer fra mængder af varen X, er det en normal, ikke-specifik reservation. Flere oplysninger i [Designoplysninger – Varesporing og reservationer](design-details-item-tracking-and-reservations.md).

Følgende procedure er baseret på en salgsordre.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Opret en salgsordrelinje til en vare med varesporing.  
3. Tildel serie- og lotnumre til salgsordrelinjen. Du kan finde flere oplysninger i [Arbejde med serie- og lotnumre](inventory-how-work-item-tracking.md).
4. På salgsordrelinjen skal du vælge handlingen **Reserver**.  
5. Vælg knappen **Ja** for at reservere bestemte serie- eller lotnumre.  
6. På siden **Varesporingsliste** skal du vælge den kombination af serienummer og lotnummer, du lige har tildelt.  
7. Klik på **OK** for at åbne siden **Reservation**, hvor der kun vises forsyning med det angivne varesporingsnummer. Hvis der findes ikke-specifikke reservationer på nogle af de varesporingsnumre, du har angivet for linjen, vises der en meddelelse om det antal, der allerede er reserveret.  
8. Vælg enten handlingen **Reserver automatisk** eller handlingen **Reserver fra aktuel linje** for at oprette reservationen på de specifikke varesporingsnumre.

## <a name="see-also"></a>Se også

[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Reservation, ordresporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designoplysninger: Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
