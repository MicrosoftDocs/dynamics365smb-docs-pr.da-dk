---
title: Ofte stillede spørgsmål om Fortæl mig | Microsoft Docs
description: Denne artikel indeholder svar på spørgsmål, som vores partnere og kunder ofte stiller om Fortæl mig.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793010"
---
# <a name="tell-me-faq"></a>Ofte stillede spørgsmål om Fortæl mig
Dette emne indeholder svar på spørgsmål, som vores avancerede brugere ofte stiller om den nye Fortæl mig-funktion, som erstatter den tidligere sidesøgefunktion, der også kaldes **Søg efter side eller rapport**.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Kan alle handlinger fra min aktuelle side registreres i Fortæl mig?
Nej. Handlinger i dele, f.eks. en salgslinjedelen eller faktabokse, vises ikke i Fortæl mig.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Filtreres resultaterne i Fortæl mig efter rettigheder?
Hvis brugeren ikke har AccessByPermissions, vises handlinger ikke. Sider og rapporter vises i dog resultaterne, men kræver, at brugeren har rettigheder til at få adgang til dem. Der vises en meddelelse, hvis brugeren ikke har rettigheder til at få vist objektet.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Viser Fortæl mig indhold fra mine tilpasninger eller installerede udvidelser fra tredjepart?
Handlinger, sider og rapporter, der stammer fra udvidelser, hentes af Fortæl mig, men det gælder ikke brugerdefineret dokumentation med hjælp. Du kan finde tekniske oplysninger om, hvordan du kan gøre brugerdefinerede sider og rapporter registrerbare, i [Tilføjelse af sider og rapporter til søgning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hvordan adskiller denne funktion sig fra det, der tidligere blev kaldt sidesøgning?
Sidesøgning er blevet udviklet til Fortæl mig for at hjælpe dig med at få arbejdet gjort hurtigt. Sidesøgning kan kun hjælpe dig med at navigere til sider eller rapporter. På et teknisk plan er Fortæl mig ikke længere baseret på det ældre MenuSuite-princip.

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a>Jeg bruger [!INCLUDE[d365fin](includes/d365fin_md.md)] til det lokale miljø. Omfatter det Fortæl mig?
Du kan bruge Fortæl mig i den lokale webklient til at finde handlinger, sider og rapporter, men ikke dokumentation. Brugere, der opretter forbindelse til [!INCLUDE[d365fin](includes/d365fin_md.md)] fra Dynamics NAV-klienten fortsætter med at bruge sidesøgning.

### <a name="is-tell-me-available-for-all-form-factors"></a>Er Fortæl mig tilgængelig for alle formfaktorer?
Fortæl mig er kun tilgængelig i webklienten eller Windows-skrivebordsappen.

### <a name="are-the-documentation-results-available-in-any-language"></a>Findes dokumentationsresultaterne på alle sprog?
Hjælpeartikler vises på det sprog, du har angivet i **Mine indstillinger**, hvis Hjælp er tilgængelig på det pågældende sprog.

## <a name="see-also"></a>Se også  
[Finde funktioner og oplysninger](ui-search.md)
