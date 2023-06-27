---
title: Ofte stillede spørgsmål om Fortæl mig
description: 'Denne artikel indeholder svar på spørgsmål, som vores partnere og kunder ofte stiller om Fortæl mig-funktionen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="tell-me-faq"></a>Ofte stillede spørgsmål om Fortæl mig
I denne artikel besvares spørgsmål, som erfarne brugere ofte stiller om funktionen Fortæl mig.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Kan alle handlinger fra min aktuelle side registreres i Fortæl mig?

Nej. Handlinger i dele, f.eks. en salgslinjedelen eller faktabokse, vises ikke i Fortæl mig.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Filtreres resultaterne i Fortæl mig efter rettigheder?

Hvis brugeren ikke har AccessByPermissions, vises handlinger ikke. Sider og rapporter vises i dog resultaterne, men kræver, at brugeren har rettigheder til at få adgang til dem. Der vises en meddelelse, hvis brugeren ikke har rettigheder til at få vist objektet.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Viser Fortæl mig indhold fra mine tilpasninger eller installerede udvidelser fra tredjepart?

Handlinger, sider og rapporter, der stammer fra udvidelser, hentes af Fortæl mig. Du kan finde tekniske oplysninger om, hvordan du kan gøre brugerdefinerede sider og rapporter registrerbare, i [Tilføjelse af sider og rapporter til søgning](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Hvordan adskiller denne funktion sig fra det, der tidligere blev kaldt sidesøgning?

Sidesøgning er blevet udviklet til Fortæl mig for at hjælpe dig med at få arbejdet gjort hurtigt. Sidesøgning kan kun hjælpe dig med at navigere til sider eller rapporter. På et teknisk plan er Fortæl mig ikke længere baseret på det ældre MenuSuite-princip.

### <a name="i-use-on-premises--does-that-include-tell-me"></a>Jeg bruger [!INCLUDE[prod_short](includes/prod_short.md)] til det lokale miljø. Omfatter det Fortæl mig?

Du kan bruge Fortæl mig i den lokale webklient til at finde handlinger, sider og rapporter, men ikke apps og konsulenttjenester i AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Er Fortæl mig tilgængelig for alle formfaktorer?

Fortæl mig er kun tilgængelig i webklienten eller Windows-skrivebordsappen.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language"></a>Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things"></a>Vil jeg give mig hjælp til at bruge sider, rapporter og andre ting?

Nej, men du kan nemt få disse oplysninger fra Hjælp-ruden. Du skal blot vælge menupunktet **Hjælp** (spørgsmålstegnet i øverste højre hjørne) eller trykke på <kbd>Ctrl</kbd>+<kbd>F1</kbd> på tastaturet. Du kan finde flere oplysninger på [Ruden hjælp](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>Hvorfor vises der ikke et bogmærkeikon for mine søgeresultater?

Bogmærkeikonet vises ikke i vinduet Fortæl mig, når tilpasning er deaktiveret for en brugerrolle.


## <a name="see-also"></a>Se også
[Gemme og tilpasse listevisninger](ui-views.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Søge efter sider med Rollestifinder](ui-role-explorer.md)  
[Bogmærke en side eller en rapport i rollecenteret](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
