---
title: "Administrere anlægsaktiver | Microsoft Docs"
description: "Få mere at vide om funktionerne for anlægsaktiver, og få et overblik over, hvordan du arbejder med anlægsaktiver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 37e71ef201b771b13fc4393f9a6c3ffab91de163
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---
# <a name="fixed-assets"></a>Anlægsaktiver
I Anlæg i [!INCLUDE[d365fin](includes/d365fin_md.md)] får du et overblik over anlægsaktiverne, og her sikres korrekt periodisk afskrivning. Funktionen hjælper dig ligeledes med at holde styr på reparationsomkostningerne, administrere forsikringspolicer, bogføre anlægstransaktioner og generere forskellige rapporter og statistikker.

For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Derefter kan du begynde at anskaffe, vedligeholde og sælge anlægsaktiverne. Du kan også konfigurere budgetterede aktiver. Dermed kan du inkludere eventuelle forventede anskaffelser og salg i rapporterne.

For at holde styr på anlægsaktivers afskrivninger og andre finansielle transaktioner i relation til anlægsaktiver, skal du oprette en eller flere afskrivningsprofiler for hvert anlægsaktiv i din virksomhed. Afskrivning udføres ved at køre en rapport for at beregne den periodiske afskrivning og udfylde en kladde med de resulterende poster, der er klar til at blive bogført. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter forskellige afskrivningsmetoder. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere afskrivningsprofiler pr. anlægsaktiv til forskellige formål, f.eks en til rapportering af moms og en anden til intern rapportering.

For hvert aktiv kan du registrere reparationsomkostningerne og den næste servicedato. Det er vigtigt at holde styr på reparationsomkostningerne af hensyn til budgetteringen og for at kunne træffe beslutningen, om et anlægsaktiv skal udskiftes eller ej.

Hvert anlægsaktiv kan tilknyttes én eller flere forsikringspolicer. Du kan derfor let kontrollere, at forsikringspolicebeløbene er i overensstemmelse med værdien af de aktiver, der er knyttet til policen. Det gør det også nemt at overvåge årlige forsikringspræmier.

> [!NOTE]  
>   Du kan registrere anlægstransaktioner i vinduet **Anlægskassekladde** eller i vinduet **Anlægskladde**, afhængigt af, om transaktionerne, der er til finansiel rapportering eller intern administration. Hjælp for Anlæg beskriver kun, hvordan du bruger vinduet **Anlægskassekladde**. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).

Når du vil begynde at administrere anlægsaktiver, skal du først angive standardværdier, anlægsregnskab, bogføringsgrupper, allokeringsnøgler, kladder og bogføringstyper. Du kan finde flere oplysninger under [Konfigurere anlægsaktiver](fa-setup.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette anlægsaktiver, tilknytte afskrivningsmetoder, bogføre anskaffelser og skrapværdier og udskrive oversigter over anlægsaktiver. |[Anskaffede anlægsaktiver](fa-how-acquire.md) |
| Registrere servicebesøg, bogføre og overvåge reparationsomkostninger. |[Vedligeholde anlægsaktiver](fa-how-maintain.md) |
| Opdatere forsikringsoplysninger, bogføre anskaffelsespriser til forsikringspolicer, ændre forsikringsdækning, få vist forsikringsstatistik og oversigter over forsikringspolicer. |[Forsikring af anlægsaktiver](fa-how-insure.md) |
| Ompostere anlægsaktiver, overføre anlægsaktiver til forskellige lokationer, opdele eller kombinere anlæg. |[Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md) |
| Regulere anlægsaktivernes værdier, bogføre opskrivnings- og nedskrivningstransaktioner. |[Omvurdere anlægsaktiver](fa-how-revalue.md) |
| Beregne afskrivning, bogføre afskrivning og analysere afskrivning i anlægsrapporter. |[Afskrive på eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md) |
| Bogføre salgstransaktioner, have vist salgsposter og bogføre delvist salg. |[Afhænde eller lade anlægsaktiver udgå](fa-how-dispose-retire.md) |
| Administrere anlægsbudgetter, budgettere anskaffelsesomkostninger, salg af anlægsaktiver og afskrivning. |[Administrere budgetter for anlægsaktiver](fa-how-manage-budgets.md) |

## <a name="see-also"></a>Se også
[Opsætning af anlægsaktiver](fa-setup.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Finans](finance.md)  
[Introduktion](product-get-started.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

