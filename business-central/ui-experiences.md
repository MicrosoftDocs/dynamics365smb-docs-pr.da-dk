---
title: Vælge brugeroplevelsen for at vise eller skjule avancerede funktioner | Microsoft Docs
description: Få mere at vide, hvad niveauerne Essential og Premium i brugeroplevelserne hver især betyder for brugergrænsefladen, funktionalitetsområderne og dit firma.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 9110ee79e4d1788f41c8f1960f282cb490a3cc8a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "912410"
---
# <a name="changing-which-features-are-displayed"></a>Ændre, hvilke funktioner der vises
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjælpe dig med at køre din virksomhed, uanset hvilken branche du arbejder i. Kernen i [!INCLUDE[d365fin](includes/d365fin_md.md)] er finansiel rapportering og salgs- og købsprocesser. Du føjer oplevelser til i henhold til dine forretningsmæssige behov ved at tilføje udvidelser fra AppSource eller ved at ændre indstillingen for oplevelse for virksomheden. Du kan finde flere oplysninger i [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md) eller i [Valg af en brugergrænseflade til at vise eller skjule funktioner](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features).

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Valg af en brugergrænseflade til at vise eller skjule funktioner
Brugeroplevelsen bestemmer, hvor mange af de grundlæggende funktioner der er tilgængelige, når du og dine kolleger bruger [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan vælge brugeroplevelsen for din virksomhed i feltet **Oplevelse** på siden **Virksomhedsoplysninger**.

> [!NOTE]  
> Denne indstilling gælder for alle brugere i virksomheden. Brugere kan tilpasse deres egne oplevelse yderligere ved at ændre sidelayout og -indhold. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde og sider](ui-personalization-user.md).  

Følgende tabel viser de oplevelser, der i øjeblikket er tilgængelige.

| Oplevelse | Indvirkning på brugergrænseflade |
| --- | --- |
| **Essential** |Viser alle handlinger og felter for alle almindelige forretningsfunktioner.|
| **Premium** |Viser alle handlinger og felter for alle forretningsfunktioner, herunder produktion og service.|

> [!NOTE]  
> De oplevelser, du kan vælge i [!INCLUDE[d365fin](includes/d365fin_md.md)] afhænger af din løsningslicens, der kaldes en plan. Du kan oplysninger om planerne **Essentiel** og **Premium** under [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på Microsoft Dynamics 365-marketingwebstedet. Se også [[!INCLUDE[d365fin](includes/d365fin_md.md)] Licensvejledning](https://go.microsoft.com/fwlink/?linkid=2068931) (kræver adgang til CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alle almindelige brugere i en løsning skal have tildelt den samme plan, Essential eller Premium, før oplevelsen kan vælges til virksomheden. Derfor kan én bruger ikke få adgang til Premium-funktioner, hvis en eller flere andre brugere kun har adgang til Essential-funktioner. Dette gælder ikke for mere særlige brugere af typen teammedlem, intern administrator, ekstern bogholder og uddelegeret administrator, der kan hver tildeles en anden plan end andre brugere i løsningen.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivere Premium-funktioner, når du har opgraderet en plan
Brugere tildeles til planer i Office 365 Administration i forbindelse med generelt arbejde for at oprette Business Central-brugere. Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Derefter kan du definere, hvilke bestemte funktioner og sider i oplevelsen, disse brugere kan få adgang til, ved at tildele tilladelsessæt. Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Sådan opdateres planændringer i brugergrupper
Når du har ændret brugerplaner i Office 365 Administration, f.eks. tildelt flere brugere til Premium-planen, skal du afspejle ændringen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Log på som administrator.
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.
3. Du kan vælge handlingen **Brugergrupper** på siden **Opdater alle brugergrupper**.

Alle nye oplysninger om planer for brugere og de tilknyttede brugergrupper opdateres nu i overensstemmelse med ændringerne i planen.

### <a name="to-select-the-premium-experience"></a>Sådan vælges Premium-oplevelsen
Du kan nu fortsætte med at vælge den nye oplevelse.
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.
2. Vælg Premium i feltet **Oplevelse** i oversigtspanelet **Brugeroplevelse** på siden **Virksomhedsoplysninger**.

## <a name="help-assumes-premium-experience"></a>Hjælpen forudsætter Premium-oplevelse
Alle beskrivelser af funktioner i dokumentationen til [!INCLUDE[d365fin](includes/d365fin_md.md)] antager **Premium**-oplevelsen, hvilket betyder, at beskrivelserne dækker det fulde omfang af elementerne i brugergrænsefladen. En tekstnote indsættes i vigtige emner i Hjælp for funktionsområderne Produktion og Serviceadministration med angivelse af, at de kræver **Premium**-oplevelsen.

## <a name="see-also"></a>Se også
[Oprettelse af nye virksomheder](about-new-company.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-licensvejledning](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
