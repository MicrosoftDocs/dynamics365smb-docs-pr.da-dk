---
title: 'Konfigurere varesporing med serie-, lot- og pakkenumre'
description: 'Konfigurere varesporing med serie-, lot- og pakkenumre'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Konfigurere varesporing med serie-, lot- og pakkenumre

Hold styr på lagervarer, selv i komplekse lagerkonfigurationer, med numre, der er specifikke for hver enkelt vare, som et individuelt objekt, et lot eller en pakke. Med varesporing kan du spore varer på tværs af interne lagerflytninger og udgående og indgående dokumenter.

Varer med serie- og lotnumre kan spores både frem og tilbage i forsyningskæden. Dette er nyttigt ved generel kvalitetssikring og tilbagekaldelser af produkter. Du kan finde flere oplysninger i [Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> I 2021 udgivelsesbølge 1 og senere skal du aktivere funktionen *Brug sporing efter pakkenummer i reservations- og sporingssystemet*, hvis du vil arbejde med pakkenumre samt serie-og lotnumre. Du kan finde flere oplysninger i [Aktivering af kommende funktioner på forhånd](admin-feature-management.md). Når funktionen er slået til, kan du tildele pakkenumre til udgående og indgående dokumenter, som svarer til, hvordan du kan arbejde med lotnumre.  

## Numre og varesporing

Som del af processerne på lagerstedet kan du samle lagerbeholdningen i pakker, kasser, beholdere osv. For at kunne holde styr på varerne skal du til imidlertid tildele dem entydige numre som identifikation. Hvis du f.eks. fremstiller og sælger en stol, kan den have varenummeret *1900-S*. Hver enkelt stol har et serienummer, *1001*, men du kan også samle fire stole i en lot som *LOT0001*, og du kan forsende stolene i en beholder med pakkenummeret *CONTAINER010*, som også omfatter andre varer, f.eks. *LOT0100* for sideborde og *LOT200* for lamper.  

Afhængigt af konfigurationen bruger du disse forskellige numre til at holde styr på lageret i [!INCLUDE [prod_short](includes/prod_short.md)] på de forskellige stadier i købs-, salgs-, lageroperationerne osv.

## Sådan oprettes varesporingskoder

En varesporingskode afspejler de forskellige overvejelser, som en virksomhed skal gøre sig i forbindelse med brugen af serie- og lotnumre på varer, der bevæger sig igennem lageret.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varesporingskoder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. På oversigtspanelerne **Serienr.**, **Lotnr.** og **Pakkenr.** skal du definere politikker for varesporingen henholdsvis efter serie-, lot- og pakkenumre.  

> [!NOTE]  
> Hvis du vil spore bestemte varer eller bestemte partier i hele deres levetid, skal du vælge henholdsvis feltet **Serienr.specifik sporing** og feltet **Lotspecifik sporing**. Det betyder, at når du håndterer en udgående enhed for en vare med denne varesporingskode, skal du altid angive, hvilket eksisterende serienummer eller hvilket eksisterende lotnummer der skal håndteres. Det betyder, at når du sælger en vareenhed, skal den holdes op mod et specifikt serienummer eller et specifikt lotnummer på lageret. Med andre ord følger et serie- eller lotnummer, der knyttes til varen, når den indføres på lageret, også den pågældende varetype ud af lageret.

Da dette specielle opsætningsfelt dækker alle mulige transaktioner med varen, markeres de individuelle indgående og udgående felter også. De individuelle ind- og udgående felter har imidlertid intet at gøre med udligning på lageret – de angiver blot din virksomheds arbejdsgang for, hvornår der skal tilknyttes varesporingsnumre.  

> [!NOTE]  
> Når du vil tildele varesporingsnumre i lageraktiviteter, skal du markere afkrydsningsfelterne **Serienr. - lagersporing** og **Lotlagersporing** være markeret på varens varesporingskodekort.  

## Sådan oprettes udløbsregler for serienumre eller lotnumre

Det kan være praktisk at angive særlige udløbsdatoer og regler i varesporingskoden. Dette gør det muligt at holde styr på, hvornår bestemte serie- og lotnumre udløber.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varesporingskoder**, og vælg derefter det relaterede link.
2. Vælg en eksisterende varesporingskode, og vælg derefter handlingen **Rediger**.  
3. Markér følgende afkrydsningsfelter i oversigtspanelet **Diverse**:  

    |Felt|Beskrivlse|  
    |---------------------------------|---------------------------------------|  
    |**Nøje bogføring af udløbsdato**|Angiver, at den udløbsdato, der blev knyttet til varesporingsnummeret ved modtagelse på lageret, skal overholdes, når varen forlader lageret.|  
    |**Kræver angivelse af udløbsdato**|Angiver, at du skal angive en udløbsdato manuelt på varesporingslinjen.|  
    |**Brug udløbsdatoer**|Angiver, at du ikke vil beregne udløbsdatoer. |  

## Sådan oprettes garantier for serie- eller lotnumre

Det kan være praktisk at angive særlige garantier for bestemte varer i varesporingskoden. Det betyder, at du kan holde styr på, hvornår garantierne for bestemte serie- eller lotnumre udløber for varerne på dit lager.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varesporingskoder**, og vælg derefter det relaterede link.  
2. Vælg en eksisterende varesporingskode, og vælg derefter handlingen **Rediger**.  
3. Udfyld feltet **Garantiophørsformel** i oversigtspanelet **Diverse**, og marker derefter afkrydsningsfelterne på følgende måde:  

    |Felt|Beskrivlse|  
    |---------------------------------|---------------------------------------|  
    |**Garantiophørsformel**|Angiver den sidste dag for garantien på varen.|  
    |**Kræv post for garantidato**|Angiver, at du manuelt skal angive en garantidato på varesporingslinjen.|  


## Sådan defineres varer til sporing med de korrekte varesporingskoder

Hvis du vil aktivere varesporing, skal du først tildele varesporingskoderne til en vare. Du kan tilføje varesporingskoder på to måder ved at vælge koden på en foruddefineret liste eller ved at tildele en ny entydig kode. Placer markøren over felterne for at se en kort beskrivelse.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare**, og vælg derefter det relaterede link.
2. Vælg en eksisterende vare på listen, og Åbn siden **Varekort**.  
3. I oversigtspanelet **varesporing** skal du tildele de relevante varesporingskoder og vælge **Varesporingskode**, **serienumre** og **lotnumre**.
    1. Du kan også vælge at oprette en ny varesporingskode ved at vælge den **nye** handling.

## Sådan angives startsaldoer for de varer, du sporer

Du kan oprette primosaldi for de varer, som du sporer. Da du kan vælge forskellige lageropsætninger, er der to muligheder:

* Aktivere bestemte batchnumre på siden **Varekladder** for at lade personer angive serie-, lot- og pakkedata direkte på kladdelinjer.
* For lokationer, hvor funktionen **Styret læg-på-lager og pluk** er aktiveret, skal du bruge siden **Lagerplaceringsopgørelse** til at gøre alle varesporingsfelter tilgængelige. De felter, der er tilgængelige, omfatter felterne **Garantidato** og **Udløbsdato**.

### Varekladder 

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varekladder**, og vælg derefter det relaterede link.
2. Vælg feltet **Navn** for at åbne en liste over varekladdenavne.
3. Vælg **Ny** for at oprette et nyt batch, og aktiver derefter **Varesporing på linjer**.
4. Klik på **OK** for at vælge den oprettede batch.
5. Udfyld felterne efter behov på varekladdelinjen. Bemærk, at felterne **Lotnr.**, **Serienr.**, **Udløbsdato**, **Garantidato** og **Pakkesporingsnr.** felterne er tilgængelige (hvis funktionen er aktiveret).
6. Vælg handlingen **Bogfør** for at justere lagerbeholdning.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] understøtter nogle få mindre valideringer, når du indtaster eller importerer data. Der foretages en mere omfattende kontrol, når du bogfører eller overfører data fra kladdelinjer til vinduet **Varesporing**. Sidstnævnte sker automatisk, når du åbner siden **Varesporing** fra varekladdelinjen, eller hvis du har valgt handlingen **Opdater varesporingslinjer**.

### Lagerplaceringsopgørelseskladde til lokationer, hvor styret pluk og læg-på-lager er aktiveret  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageropgørelsesordrer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov på varekladdelinjen. Bemærk, at felterne **Lotnr.**, **Serienr.**, **Udløbsdato**, **Garantidato** og **Pakkesporingsnr.** felterne er tilgængelige (hvis funktionen er aktiveret).
3. Vælg handlingen **Registrer** for at regulere lagerbeholdningen. Husk, at du skal synkronisere de regulerede lagerposter med de relaterede vareposter. Hvis du vil vide mere, skal du gå til [synkronisering af de justerede lagerposter](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

I forbindelse med masseimport skal du bruge konfigurationspakker til at importere data til kladderne.

> [!NOTE]
> Du kan ikke bruge **Rediger i Excel** til at oprette kladdelinjer med sporingsoplysninger.

## Se også

[Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)  
[Spore varer - sporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)  
[Designoplysninger - Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
