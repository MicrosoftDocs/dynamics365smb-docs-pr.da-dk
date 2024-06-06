---
title: 'Ændre, hvilke funktioner der vises'
description: 'Få mere at vide, hvad niveauerne Essential og Premium i brugeroplevelserne hver især betyder for brugergrænsefladen, funktionalitetsområderne og dit firma.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: '1,'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Ændre, hvilke funktioner der vises

[!INCLUDE[prod_short](includes/prod_short.md)] er designet til at hjælpe dig med at køre din virksomhed uanset størrelse og kompleksitet. I kernen af produktet finder du væsentlige funktioner som f.eks. finansiel rapportering, salg, køb og lagerstyring. I takt med at kompleksiteten øges, kan du f.eks. aktivere funktionen til produktions- og servicestyring.

Du kan definere niveauet for produktkompleksiteten, og dermed hvilke funktioner virksomhedens brugere får adgang til, ved at ændre indstillingen **Oplevelse** på siden **Virksomhedsoplysninger**. Bemærk, at indstillingen Oplevelse også kan ændres ved at tilføje visse udvidelser fra AppSource. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md).

Følgende tabel viser de oplevelser, der i øjeblikket er tilgængelige.

| Oplevelse | Indvirkning på brugergrænseflade |
| --- | --- |
| **Essential** |Viser alle handlinger og felter for alle almindelige forretningsfunktioner.|
| **Premium** |Viser alle handlinger og felter for alle forretningsfunktioner, herunder produktion og service.|

De oplevelser, der kan vælges i [!INCLUDE[prod_short](includes/prod_short.md)], afspejler de løsningslicenser, der kaldes planer, som er defineret for produktet. Du kan finde oplysninger om planerne Essentiel og Premium under [Business Central](https://go.microsoft.com/fwlink/?linkid=2264940) på Microsoft Dynamics 365 Marketing-webstedet. Se også [[!INCLUDE[prod_short](includes/prod_short.md)]-licensvejledningen](https://go.microsoft.com/fwlink/?linkid=2264939).

> [!IMPORTANT]  
> Brugere af typen teammedlem, intern administrator, ekstern bogholder og uddelegeret administrator kan tildeles en anden plan end andre brugere i løsningen. Kun brugere af type Evaluation eller Premium kan ændre værdien i feltet **Oplevelse** fra Essential til Premium.

> [!NOTE]
> I 2024 udgivelsesbølge 1 kan en bruger med Premium-planen logge på en virksomhed, der bruger Essentials-planen. Premium-brugeren kan dog ikke bruge nogen af de funktioner, som Premium-licensen giver. Det samme er ikke gældende i den modsatte retning. Brugere, der har Essentials-planen kan ikke logge på en virksomhed, der bruger Premium-planen.

Før du angiver en indstilling for en virksomheds oplevelse, skal du angive brugernes adgang til bestemte funktioner og sider ved at tildele tilladelsessæt. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Indstillingen **Oplevelse** gælder for alle brugere i en virksomhed, men de enkelte brugere kan tilpasse deres egne oplevelser yderligere ved at ændre sidelayout og indhold. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## Aktivere Premium-funktioner, når du har opgraderet en plan

Brugere tildeles til planer i Microsoft 365 Administration i forbindelse med generelt arbejde for at oprette Business Central-brugere. Du kan finde flere oplysninger i [Tilføje brugere og tildele licenser på samme tid](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### Sådan opdateres planændringer i brugergrupper

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Når du har ændret brugerplaner i Microsoft 365 Administration, f.eks. tildelt flere brugere til Premium-planen, skal du opdatere [!INCLUDE[prod_short](includes/prod_short.md)] afspejle ændringen.

1. Log på som administrator.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
3. Du kan også vælge handlingen **Opdater brugere fra Microsoft 365** på siden **Brugere**.

### Sådan vælges Premium-oplevelsen

Du kan nu fortsætte med at vælge den nye oplevelse.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, åbn **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Vælg Premium i feltet **Oplevelse** i oversigtspanelet **Brugeroplevelse** på siden **Virksomhedsoplysninger**.

## Hjælpen forudsætter Premium-oplevelse

Alle beskrivelser af funktioner i dokumentationen til [!INCLUDE[prod_short](includes/prod_short.md)] antager **Premium**-oplevelsen, hvilket betyder, at beskrivelserne dækker det fulde omfang af elementerne i brugergrænsefladen.

## Se også

[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)  
[Oprettelse af nye virksomheder](about-new-company.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]