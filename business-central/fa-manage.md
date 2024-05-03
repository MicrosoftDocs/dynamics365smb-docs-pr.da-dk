---
title: Administrere anlægsaktiver (indeholder video)
description: 'Få mere at vide om funktionerne for anlægsaktiver, og få et overblik over, hvordan du arbejder med og administrerer anlægsaktiver.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Administration af anlægsaktiver

I Anlæg i [!INCLUDE[prod_short](includes/prod_short.md)] får du et overblik over anlægsaktiverne, og her sikres korrekt periodisk afskrivning. Funktionen hjælper dig ligeledes med at holde styr på reparationsomkostningerne, administrere forsikringspolicer, bogføre anlægstransaktioner og generere forskellige rapporter og statistikker.

## <a name="video-overview"></a>Videooversigt

Følgende video giver en grundlæggende beskrivelse af anlægsaktiver:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="fixed-assets-overview"></a>Oversigt over anlægsaktiver

For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Derefter kan du begynde at anskaffe, vedligeholde og sælge anlægsaktiverne. Du kan også konfigurere budgetterede aktiver. Med budgettering kan du inkludere forventede anskaffelser og salg i rapporterne.

> [!IMPORTANT]
> Før du kan administrere anlægsaktiver, skal du udføre følgende opsætninger:
>
> * Standardværdier
> * Regnskab for anlægsaktiver
> * Bogføringsgrupper
> * Allokeringsnøgler
> * Anlægskladder
>
> Du kan finde flere oplysninger i [Konfigurere anlægsaktiver](fa-setup.md).

For at holde styr på anlægsaktivers afskrivninger og andre finansielle transaktioner i relation til anlægsaktiver, skal du oprette en eller flere afskrivningsprofiler for hver. Afskrivning udføres ved at køre en rapport for at beregne den periodiske afskrivning og udfylde en kladde med de resulterende poster, og derefter bogføre kladden. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter forskellige afskrivningsmetoder. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere afskrivningsprofiler pr. anlægsaktiv til forskellige formål, f.eks en til rapportering af moms og en anden til intern rapportering.

For hvert aktiv kan du registrere reparationsomkostningerne og den næste servicedato. Sporing af omkostninger til sporing af vedligeholdelse er vigtige at holde styr på af hensyn til budgetteringen og for at kunne træffe beslutningen, om et anlægsaktiv skal udskiftes.

Du kan knytte hvert anlægsaktiv til en eller flere forsikringspolicer og kontrollere, at forsikringspræmierne stemmer overens med værdien af aktiverne.

> [!NOTE]  
> Du kan registrere anlægstransaktioner på siden **Anlægskassekladde** eller på siden **Anlægskladde**, afhængigt af om transaktionerne, der er til financial reporting eller intern administration. Hjælp for Anlæg beskriver kun, hvordan du bruger siden **Anlægskassekladde**. Du kan finde flere oplysninger i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).

## <a name="how-to-use-fixed-assets"></a>Forsikre anlægsaktiver

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

| Til  | Se |
| --- | --- |
| Konfigurer forudsætninger for brug af anlægsaktiver (definition af standardværdier, anlægsregnskab, bogføringsgrupper, allokeringsnøgler, kladder og bogføringstyper). | [Opsætning af Anlægsaktiver](fa-setup.md)|
| Oprette anlægsaktiver, tilknytte afskrivningsmetoder, bogføre anskaffelser og skrapværdier og udskrive oversigter over anlægsaktiver. |[Anskaffede anlægsaktiver](fa-how-acquire.md) |
| Registrere servicebesøg, bogføre og overvåge reparationsomkostninger. |[Vedligeholde anlægsaktiver](fa-how-maintain.md) |
| Opdatere forsikringsoplysninger, bogføre anskaffelsespriser til forsikringspolicer, ændre forsikringsdækning, få vist forsikringsstatistik og oversigter over forsikringspolicer. |[Forsikring af anlægsaktiver](fa-how-insure.md) |
| Ompostere anlægsaktiver, overføre anlægsaktiver til forskellige lokationer, opdele eller kombinere anlæg. |[Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md) |
| Regulere anlægsaktivernes værdier, bogføre opskrivnings- og nedskrivningstransaktioner. |[Omvurdere anlægsaktiver](fa-how-revalue.md) |
| Beregne afskrivning, bogføre afskrivning og analysere afskrivning i anlægsrapporter. |[Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md) |
| Få mere at vide om forskellige afskrivningsmetoder for anlægsaktiver. |[Afskrivningsmetoder](fa-depreciation-methods.md) |
| Bogføre salgstransaktioner, have vist salgsposter og bogføre delvist salg. |[Afhænde eller lade anlægsaktiver udgå](fa-how-dispose-retire.md) |
| Administrere anlægsbudgetter, budgettere anskaffelsesomkostninger, salg af anlægsaktiver og afskrivning. |[Administrere budgetter for anlægsaktiver](fa-how-manage-budgets.md) |
| Få mere at vide om indbyggede rapporterings- og analysefunktioner til anlægsaktiver. | [Rapporter og analyser af anlægsaktiver](fa-reports.md) |

## <a name="see-also"></a>Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Oversigt for Finance](finance.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
