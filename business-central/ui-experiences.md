---
title: Vælge brugeroplevelsen for at vise eller skjule avancerede funktioner | Microsoft Docs
description: Få mere at vide, hvad niveauerne Essential og Premium i brugeroplevelserne hver især betyder for brugergrænsefladen, funktionalitetsområderne og dit firma.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e53ef4e33d489de7ff92e537b01b8563e62ba77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379629"
---
# <a name="change-which-features-are-displayed"></a>Ændre, hvilke funktioner der vises
[!INCLUDE[prod_short](includes/prod_short.md)] er designet til at hjælpe dig med at køre din virksomhed uanset størrelse og kompleksitet. I kernen af produktet finder du væsentlige funktioner som f.eks. finansiel rapportering, salg, køb og lagerstyring. I takt med at kompleksiteten øges, kan du f.eks. aktivere funktionen til produktions- og servicestyring.

Du kan definere niveauet for produktkompleksiteten, og dermed hvilke funktioner virksomhedens brugere får adgang til, ved at ændre indstillingen **Oplevelse** på siden **Virksomhedsoplysninger**. Bemærk, at indstillingen Oplevelse også kan ændres ved at tilføje visse udvidelser fra AppSource. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md).

Følgende tabel viser de oplevelser, der i øjeblikket er tilgængelige.

| Oplevelse | Indvirkning på brugergrænseflade |
| --- | --- |
| **Essential** |Viser alle handlinger og felter for alle almindelige forretningsfunktioner.|
| **Premium** |Viser alle handlinger og felter for alle forretningsfunktioner, herunder produktion og service.|

De oplevelser, der kan vælges i [!INCLUDE[prod_short](includes/prod_short.md)], afspejler de løsningslicenser, der kaldes planer, som er defineret for produktet. Du kan finde oplysninger om planerne Essentiel og Premium under [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på Microsoft Dynamics 365 Marketing-webstedet. Se også [[!INCLUDE[prod_short](includes/prod_short.md)] Licensvejledning](https://go.microsoft.com/fwlink/?linkid=2068931) (kræver adgang til CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alle almindelige brugere i en løsning skal have tildelt den samme plan, Essential eller Premium, før oplevelsen kan vælges til virksomheden. Derfor kan én bruger ikke få adgang til Premium-funktioner, hvis en eller flere andre brugere kun har adgang til Essential-funktioner. Dette gælder ikke for mere særlige brugere af typen teammedlem, intern administrator, ekstern bogholder og uddelegeret administrator, der kan hver tildeles en anden plan end andre brugere i løsningen.<br /><br /> Kun brugere af type Evaluation eller Premium kan ændre værdien i feltet **Oplevelse** fra Essential til Premium.

Før du angiver en indstilling for en virksomheds oplevelse, skal du angive brugernes adgang til bestemte funktioner og sider ved at tildele tilladelsessæt. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).

Indstillingen **Oplevelse** gælder for alle brugere i en virksomhed, men de enkelte brugere kan tilpasse deres egne oplevelser yderligere ved at ændre sidelayout og indhold. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funktioner, når du har opgraderet en plan
Brugere tildeles planer i Microsoft 365 Administration i forbindelse med generelt arbejde for at oprette Business Central-brugere. Du kan finde flere oplysninger under [Tilføje brugere og tildele licenser på samme tid](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Sådan opdateres planændringer i brugergrupper
Når du har ændret brugerplaner i Microsoft 365 Administration, f.eks. tildelt flere brugere til Premium-planen, skal du afspejle ændringen i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Log på som administrator.
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
3. Vælg handlingen **Opdater alle brugergrupper** på siden **Brugergrupper**.

Alle nye oplysninger om planer for brugere og de tilknyttede brugergrupper opdateres nu i overensstemmelse med ændringerne i planen.

### <a name="to-select-the-premium-experience"></a>Sådan vælges Premium-oplevelsen
Du kan nu fortsætte med at vælge den nye oplevelse.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Vælg Premium i feltet **Oplevelse** i oversigtspanelet **Brugeroplevelse** på siden **Virksomhedsoplysninger**.

## <a name="help-assumes-premium-experience"></a>Hjælpen forudsætter Premium-oplevelse
Alle beskrivelser af funktioner i dokumentationen til [!INCLUDE[prod_short](includes/prod_short.md)] antager **Premium**-oplevelsen, hvilket betyder, at beskrivelserne dækker det fulde omfang af elementerne i brugergrænsefladen.

## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Tildele rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Oprettelse af nye virksomheder](about-new-company.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-licensvejledning](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]