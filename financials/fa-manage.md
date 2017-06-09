---
title: "Anlægsaktiver | Microsoft Docs"
description: "Beskriver, hvordan du administrerer anlægsaktiver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d57603202d9e2e5304c899eaf764dde8cfa6369d
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="fixed-assets"></a>Anlægsaktiver
I Anlæg i [!INCLUDE[d365fin](includes/d365fin_md.md)] får du et overblik over anlægsaktiverne, og her sikres korrekt periodisk afskrivning. Funktionen hjælper dig ligeledes med at holde styr på reparationsomkostningerne, administrere forsikringspolicer, bogføre anlægstransaktioner og generere forskellige rapporter og statistikker.

For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Derefter kan du begynde at anskaffe, vedligeholde og sælge anlægsaktiverne. Du kan også konfigurere budgetterede aktiver. Dermed kan du inkludere eventuelle forventede anskaffelser og salg i rapporterne.

For at holde styr på anlægsaktivers afskrivninger og andre finansielle transaktioner i relation til anlægsaktiver, skal du oprette en eller flere afskrivningsprofiler for hvert anlægsaktiv i din virksomhed. Afskrivning udføres ved at køre en rapport for at beregne den periodiske afskrivning og udfylde en kladde med de resulterende poster, der er klar til at blive bogført. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter forskellige afskrivningsmetoder. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere afskrivningsprofiler pr. anlægsaktiv til forskellige formål, f.eks en til rapportering af moms og en anden til intern rapportering.

For hvert aktiv kan du registrere reparationsomkostningerne og den næste servicedato. Det er vigtigt at holde styr på reparationsomkostningerne af hensyn til budgetteringen og for at kunne træffe beslutningen, om et anlægsaktiv skal udskiftes eller ej.

Hvert anlægsaktiv kan tilknyttes én eller flere forsikringspolicer. Du kan derfor let kontrollere, at forsikringspolicebeløbene er i overensstemmelse med værdien af de aktiver, der er knyttet til policen. Det gør det også nemt at overvåge årlige forsikringspræmier.

**Bemærk**: Du kan registrere anlægstransaktioner i vinduet **Anlægskassekladde** eller i vinduet **Anlægskladde**, afhængigt af, om transaktionerne, der er til finansiel rapportering eller intern administration. Hjælp for Anlæg beskriver kun, hvordan du bruger vinduet **Anlægskassekladde**. Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).

**Bemærk**: Denne funktion kræver, at oplevelsen er indstillet til **Pakke**. Du kan finde flere oplysninger i [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

Når du vil begynde at administrere anlægsaktiver, skal du først angive standardværdier, anlægsregnskab, bogføringsgrupper, allokeringsnøgler, kladder og bogføringstyper. Du kan finde flere oplysninger under [Konfigurere anlægsaktiver](fa-setup.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette anlægsaktiver, tilknytte afskrivningsmetoder, bogføre anskaffelser og skrapværdier og udskrive oversigter over anlægsaktiver. |[Fremgangsmåde: Anskaffe anlægsaktiver](fa-how-acquire.md) |
| Registrere servicebesøg, bogføre og overvåge reparationsomkostninger. |[Fremgangsmåde: Vedligeholde anlægsaktiver](fa-how-maintain.md) |
| Opdatere forsikringsoplysninger, bogføre anskaffelsespriser til forsikringspolicer, ændre forsikringsdækning, få vist forsikringsstatistik og oversigter over forsikringspolicer. |[Fremgangsmåde: Forsikre anlægsaktiver](fa-how-insure.md) |
| Ompostere anlægsaktiver, overføre anlægsaktiver til forskellige lokationer, opdele eller kombinere anlæg. |[Fremgangsmåde: Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md) |
| Regulere anlægsaktivernes værdier, bogføre opskrivnings- og nedskrivningstransaktioner. |[Fremgangsmåde: Regulere anlægsaktiver](fa-how-revalue.md) |
| Beregne afskrivning, bogføre afskrivning og analysere afskrivning i anlægsrapporter. |[Fremgangsmåde: Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md) |
| Bogføre salgstransaktioner, have vist salgsposter og bogføre delvist salg. |[Fremgangsmåde: Afhænde eller afvikle anlægsaktiver](fa-how-dispose-retire.md) |
| Administrere anlægsbudgetter, budgettere anskaffelsesomkostninger, salg af anlægsaktiver og afskrivning. |[Fremgangsmåde: Administrere budgetter for anlægsaktiver](fa-how-manage-budgets.md) |

## <a name="see-also"></a>Se også
[Opsætning af anlægsaktiver](fa-setup.md)  
[Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
