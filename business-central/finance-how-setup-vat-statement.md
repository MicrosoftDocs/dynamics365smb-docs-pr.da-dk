---
title: Opret en momsangivelseslinje
description: 'Dette emne beskriver, hvordan du opretter en Momsangivelsestype og Momsangivelsesnavne for at overholde ændrede skattemyndigheders krav.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '317, 318, 320, 474'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-vat-statement-templates-and-vat-statement-names"></a>Konfigurere momsangivelsestyper og momsangivelsesnavne

Skattemyndighederne kan ændre, og gør det også, kravene til bogføring af moms. Momsangivelsestyper og momsangivelsesnavne kan hjælpe dig med at forberede kommende ændringer og foretage en problemfri overgang til de nye krav. Du kan bruge momsangivelsesskabeloner til at oprette forskellige rapporter, når du vælger at udskrive opgørelsen. Hver momsangivelsestype kan have flere momsangivelsesnavne, der definerer beregninger, og du kan oprette et nyt momsangivelsesnavn, når kravene ændres. F.eks kan ét navn beregne moms for dette år baseret på de aktuelle krav, og et andet kan beregne moms på basis af kravene for næste år. Navne er også en metode til at opbevare en historik over momsangivelsesformater, så du f.eks. kan gå tilbage for at se, hvordan du beregnede moms i tidligere år.

## <a name="to-define-a-vat-statement"></a>Sådan defineres momsangivelse

Momsangivelser giver dig mulighed for at beregne momsangivelsesbeløb for en bestemt periode, f.eks. et kvartal.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsangivelser**, og vælg derefter det relaterede link.  
2. Vælg feltet **Navn**, og vælg derefter **Ny** på siden **Momsangivelsesnavne**.
3. Udfyld de påkrævede felter. Som regel skal du angive en indstilling for hver enkelt kombination af Momsvirksomhedsbogf.gruppe/Momsproduktbogf.gruppe. Når det gælder rækkenumre, giver mening det at bruge ækvivalente numre eller odecs som i din officielle momsangivelse [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Du kan filtrere de oplysninger, som angivelsen omfatter, afhængigt af hvad du vælger i feltet **Type**. **Kontosammentælling** er nyttig, når du vil se momsen fra en bestemt konto.
**Momspostsammentælling** henter moms i de konti, der er knyttet til valgene i felterne **Bogføringstype**, **Momsvirksomhedsbogf.gruppe** og/eller **Momsproduktbogf.gruppe**. **Rækkesammentælling** giver dig mulighed for at angive en værdi eller hurtigt filtrere kriterier i feltet **Rækkesammentælling**. Du kan finde flere oplysninger i [Søgning i, filtrering og sortering af data](ui-enter-criteria-filters.md). **Beskrivelse** bruges ofte til at føje en note til angivelsen. Du kan f.eks. bruge den som en overskrift, når du har brugt Rubriksammentælling.

## <a name="to-preview-the-vat-statement"></a>Sådan får du vist momsangivelsen

Når du har defineret en momsangivelse, kan du få vist et eksempel på den for at sikre, at det passer til dine behov.
> [!Tip]
> Det er bedst at have én sektion i momsangivelsen, der bruger **Type** **Momspostsammentælling**, og en anden sektion herunder, der bruger **Type** **Kontosammentælling** til at afstemme beløbene baseret på tabellen **Momspost** sammenlignet med beløbet på **Finanskonti**. Du kan også bruge rapporten **Finans – Momsafstemning** til dette formål.

1. Vælg **Eksempel**.
2. Opret et datofilter for at begrænse angivelsen til en konkret periode. Du kan finde yderligere oplysninger om, hvordan du tilpasser siden til at vise datofiltret, under [Søgning i, filtrering og sortering af data](ui-enter-criteria-filters.md).
3. Du kan vælge forskellige indstillinger for at angive den type momsposter, der skal medtages i angivelsen.
4. På de linjer, hvor der står **Momspostsammentælling** i feltet **Type**, kan du få vist en oversigt over momsposter ved at vælge beløbet i feltet **Kolonnebeløb**.
5. Du kan bruge tilpasning til at få vist flere felter på linjerne. F.eks. det urealiserede basisbeløb og det urealiserede momsbeløb, hvis du bruger urealiseret moms.

## <a name="see-also"></a>Se også

[Opsætte merværdiafgift (moms)](finance-setup-vat.md)  
[Opsætning af ikke-realiseret moms](finance-setup-unrealized-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Lokal funktionalitet i Business Central](about-localization.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
