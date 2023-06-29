---
title: 'Ændre, hvilke funktioner der vises'
description: 'Få mere at vide, hvad niveauerne Essential og Premium i brugeroplevelserne hver især betyder for brugergrænsefladen, funktionalitetsområderne og dit firma.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: 1
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="change-which-features-are-displayed"></a><a name="change-which-features-are-displayed"></a>Ændre, hvilke funktioner der vises
[!INCLUDE[prod_short](includes/prod_short.md)] er designet til at hjælpe dig med at køre din virksomhed uanset størrelse og kompleksitet. I kernen af produktet finder du væsentlige funktioner som f.eks. finansiel rapportering, salg, køb og lagerstyring. I takt med at kompleksiteten øges, kan du f.eks. aktivere funktionen til produktions- og servicestyring.

Du kan definere niveauet for produktkompleksiteten, og dermed hvilke funktioner virksomhedens brugere får adgang til, ved at ændre indstillingen **Oplevelse** på siden **Virksomhedsoplysninger**. Bemærk, at indstillingen Oplevelse også kan ændres ved at tilføje visse udvidelser fra AppSource. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md).

Følgende tabel viser de oplevelser, der i øjeblikket er tilgængelige.

| Oplevelse | Indvirkning på brugergrænseflade |
| --- | --- |
| **Essential** |Viser alle handlinger og felter for alle almindelige forretningsfunktioner.|
| **Premium** |Viser alle handlinger og felter for alle forretningsfunktioner, herunder produktion og service.|

De oplevelser, der kan vælges i [!INCLUDE[prod_short](includes/prod_short.md)], afspejler de løsningslicenser, der kaldes planer, som er defineret for produktet. Du kan finde oplysninger om planerne Essentiel og Premium under [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på Microsoft Dynamics 365 Marketing-webstedet. Se også [[!INCLUDE[prod_short](includes/prod_short.md)]-licensvejledningen](https://go.microsoft.com/fwlink/?linkid=2068931).

> [!IMPORTANT]  
> Alle almindelige brugere i en løsning skal have tildelt den samme plan, Essential eller Premium, før oplevelsen kan vælges til virksomheden. Derfor kan én bruger ikke få adgang til Premium-funktioner, hvis en eller flere andre brugere kun har adgang til Essential-funktioner. Dette gælder ikke for mere særlige brugere af typen teammedlem, intern administrator, ekstern bogholder og uddelegeret administrator, der kan hver tildeles en anden plan end andre brugere i løsningen.<br /><br /> Kun brugere af type Evaluation eller Premium kan ændre værdien i feltet **Oplevelse** fra Essential til Premium.

Før du angiver en indstilling for en virksomheds oplevelse, skal du angive brugernes adgang til bestemte funktioner og sider ved at tildele tilladelsessæt. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Indstillingen **Oplevelse** gælder for alle brugere i en virksomhed, men de enkelte brugere kan tilpasse deres egne oplevelser yderligere ved at ændre sidelayout og indhold. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a><a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funktioner, når du har opgraderet en plan
Brugere tildeles til planer i Microsoft 365 Administration i forbindelse med generelt arbejde for at oprette Business Central-brugere. Du kan finde flere oplysninger i [Tilføje brugere og tildele licenser på samme tid](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a><a name="to-update-plan-changes-in-users-groups"></a>Sådan opdateres planændringer i brugergrupper

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Når du har ændret brugerplaner i Microsoft 365 Administration, f.eks. tildelt flere brugere til Premium-planen, skal du opdatere [!INCLUDE[prod_short](includes/prod_short.md)] afspejle ændringen.

1. Log på som administrator.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.
3. Du kan også vælge handlingen **Opdater brugere fra Microsoft 365** på siden **Brugere**.

### <a name="to-select-the-premium-experience"></a><a name="to-select-the-premium-experience"></a>Sådan vælges Premium-oplevelsen
Du kan nu fortsætte med at vælge den nye oplevelse.
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, åbn **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Vælg Premium i feltet **Oplevelse** i oversigtspanelet **Brugeroplevelse** på siden **Virksomhedsoplysninger**.

## <a name="help-assumes-premium-experience"></a><a name="help-assumes-premium-experience"></a>Hjælpen forudsætter Premium-oplevelse
Alle beskrivelser af funktioner i dokumentationen til [!INCLUDE[prod_short](includes/prod_short.md)] antager **Premium**-oplevelsen, hvilket betyder, at beskrivelserne dækker det fulde omfang af elementerne i brugergrænsefladen.

## <a name="see-also"></a><a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Oprettelse af nye virksomheder](about-new-company.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-licensvejledning](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
