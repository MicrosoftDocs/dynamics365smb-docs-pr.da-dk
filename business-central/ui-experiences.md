---
title: "Vælge brugeroplevelsen for at vise eller skjule avancerede funktioner | Microsoft Docs"
description: "Få mere at vide, hvad niveauerne Basis og Essentiel i brugeroplevelserne hver især betyder for brugergrænsefladen, funktionalitetsområderne og dit firma."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: dc7e739bc2b8ac9e8efce3a0f52acb945352416e
ms.openlocfilehash: 0a94d94e58b2aa3f04639a00904b5370c91b1132
ms.contentlocale: da-dk
ms.lasthandoff: 04/19/2018

---
# <a name="changing-which-features-are-displayed"></a>Ændre, hvilke funktioner der vises
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjælpe dig med at køre din virksomhed, uanset hvilken branche du arbejder i. Kernen i [!INCLUDE[d365fin](includes/d365fin_md.md)] er finansiel rapportering og salgs- og købsprocesser. Du føjer oplevelser til i henhold til dine forretningsmæssige behov ved at tilføje udvidelser fra AppSource eller ved at ændre indstillingen for oplevelse for virksomheden. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md), eller i afsnittet "Valg af en brugergrænseflade til at vise eller skjule funktioner" nedenfor.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Valg af en brugergrænseflade til at vise eller skjule funktioner
Brugeroplevelsen bestemmer, hvor mange af de grundlæggende funktioner der er tilgængelige, når du og dine kolleger bruger [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan vælge brugeroplevelsen for din virksomhed i feltet **Oplevelse** i vinduet **Virksomhedsoplysninger**.

> [!NOTE]  
> Denne indstilling gælder for alle brugere i virksomheden. Brugere kan tilpasse deres egne oplevelse yderligere ved at ændre sidelayout og -indhold. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde og sider](ui-personalization-user.md).  

Følgende tabel viser de oplevelser, der i øjeblikket er tilgængelige.

| Oplevelse | Indvirkning på brugergrænseflade |
| --- | --- |
| **Basis** |Viser kun grundlæggende handlinger og felter inden for de mest almindelige forretningsfunktioner, f.eks. salg, køb, lager og finans. |
| **Essentiel** |Viser alle handlinger og felter for alle almindelige forretningsfunktioner.|
| **Premium** |Viser alle handlinger og felter for alle forretningsfunktioner, herunder produktion og service.|

> [!NOTE]  
> De oplevelser, du kan vælge i [!INCLUDE[d365fin](includes/d365fin_md.md)] afhænger af din løsningslicens, der kaldes en plan. Du kan oplysninger om planerne **Essentiel** og **Premium** under [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på Microsoft Dynamics 365-marketingwebstedet.

> [!IMPORTANT]  
> Alle almindelige brugere i en løsning skal have tildelt den samme plan, Essential eller Premium, før oplevelsen kan vælges til virksomheden. Derfor kan én bruger ikke få adgang til Premium-funktioner, hvis en eller flere andre brugere kun har adgang til Essential-funktioner. Dette gælder ikke for mere særlige brugere af typen teammedlem, intern administrator, ekstern bogholder og uddelegeret administrator, der kan hver tildeles en anden plan end andre brugere i løsningen.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funktioner, når du har opgraderet en plan
Brugere tildeles til planer i Office 365 Administration i forbindelse med generelt arbejde for at oprette Business Central-brugere. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Derefter kan du definere, hvilke bestemte funktioner og vinduer i oplevelsen, disse brugere kan få adgang til, ved at tildele tilladelsessæt. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Sådan opdateres planændringer i brugergrupper
Når du har ændret brugerplaner i Office 365 Administration, f.eks. tildelt flere brugere til Premium-planen, skal du afspejle ændringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Log på som administrator.
2. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brugere**, og vælg derefter det relaterede link.
3. Vælg handlingen **Opdater alle brugergrupper** i vinduet **Brugere**.

Alle nye oplysninger om planer for brugere og de tilknyttede brugergrupper opdateres nu i overensstemmelse med ændringerne i planen.

### <a name="to-select-the-premium-experience"></a>Sådan vælges Premium-oplevelsen
Du kan nu fortsætte med at vælge den nye oplevelse.
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Vælg Premium i feltet **Oplevelse** i oversigtspanelet **Brugeroplevelse** i vinduet **Virksomhedsoplysninger**.

## <a name="see-also"></a>Se også
[Oprettelse af nye virksomheder](about-new-company.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

