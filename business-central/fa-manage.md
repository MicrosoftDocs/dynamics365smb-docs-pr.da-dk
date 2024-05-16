---
title: Administrere anlægsaktiver (indeholder video)
description: 'Få mere at vide om funktionerne for anlægsaktiver, og få et overblik over, hvordan du arbejder med og administrerer anlægsaktiver.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Administration af anlægsaktiver

Anlægsaktiver i [!INCLUDE[prod_short](includes/prod_short.md)] giver dig et overblik over anlægsaktiverne, og sikre korrekt periodisk afskrivning. Funktionen hjælper dig ligeledes med at holde styr på reparationsomkostningerne, administrere forsikringspolicer, bogføre anlægstransaktioner og generere forskellige rapporter og statistikker.

## <a name="video-overview"></a>Videooversigt

Følgende video giver en grundlæggende beskrivelse af anlægsaktiver:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Første oprettelse af anlægsaktiver

Før du kan administrere anlægsaktiver, skal du udføre følgende opsætninger:

- Standardværdier
- Regnskab for anlægsaktiver
- Bogføringsgrupper og -typer
- Allokeringsnøgler
- Anlægskladder

Flere oplysninger i [Sådan konfigureres anlægsaktiver](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Analyse af anlægsaktiver

I dette afsnit beskrives de analyseværktøjer, du kan bruge til at få indsigt i data om dine anlægsaktiver.

| Til... | Se |
| --- | --- |
| Få mere at vide om funktioner til analyse af anlægsaktiver. | [Oversigt over analyse af anlægsaktiver](fa-analytics-overview.md) |
| Foretag ad hoc-analyser af data fra anlægsaktiver direkte på listesider og forespørgsler. | [Ad hoc-analyse af data i anlægsaktiver](ad-hoc-analysis-fa.md) |
| Udforsk indbyggede rapporter til anlægsaktiver. | [Indbyggede anlægsrapporter](fa-reports.md) |
| Overvåge reparationsomkostninger. | [Overvåge reparationsomkostninger](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Overvåge forsikringsdækning. | [Overvåge forsikringsdækning](fa-how-insure.md#to-monitor-insurance-coverage) |
| Have vist salgsposter. | [Vise anlægsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vis forventede salgsværdier. | [Vise forventede salgsværdier](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Registrer anlægsaktiver

For hvert anlægsaktiv skal du definere et kort, der indeholder oplysninger om dem. Du kan f.eks. angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste. Du kan gruppere anlæg på forskellige måder, f.eks. efter klasse, afdeling eller lokation. Derefter kan du anskaffe, vedligeholde og sælge anlægsaktiverne. Du kan også konfigurere budgetterede aktiver. Med budgettering kan du inkludere forventede anskaffelser og salg i rapporterne.

| Til  | Se |
| --- | --- |
| Administrere anlægsbudgetter, budgettere anskaffelsesomkostninger, salg af anlægsaktiver og afskrivning. |[Administrere budgetter for anlægsaktiver](fa-how-manage-budgets.md) |
| Oprette anlægsaktiver, tilknytte afskrivningsmetoder, bogføre anskaffelser og skrapværdier og udskrive oversigter over anlægsaktiver. |[Anskaffe anlægsaktiver](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Konfigurer afskrivninger for dine anlægsaktiver

For at holde styr på anlægsaktivers afskrivninger og andre finansielle transaktioner i relation til anlægsaktiver, skal du oprette en eller flere afskrivningsprofiler for hver. Det kræver nogle trin at afskrive aktiver:

1. Lav en rapport for at beregne periodisk afskrivning.
1. Udfyld kladde med resulterede poster.
1. Bogfør journalen.

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter forskellige afskrivningsmetoder. Hvis du vil vide mere, skal du gå til [Afskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere afskrivningsprofiler for hvert anlægsaktiv til forskellige formål, f.eks en til rapportering af moms og en anden til intern rapportering.

| Til  | Se |
| --- | --- |
| Få mere at vide om forskellige afskrivningsmetoder for anlægsaktiver. |[Afskrivningsmetoder](fa-depreciation-methods.md) |
| Beregne afskrivning, bogføre afskrivning og analysere afskrivning i anlægsrapporter. |[Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md) |
| Vis ændrede afskrivningsprofilværdier. | [Vise ændrede afskrivningsprofilværdier](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Manuelt registrer anlægstransaktioner på siden **Anlægskassekladde** eller på siden **Anlægskladde**, afhængigt af om transaktionerne, der er til financiel rapportering eller intern administration. | [Konfigurere afskrivning på anlægsaktiver](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Vedligeholdelse og forsikring af anlægsaktiver

Du kan registrere vedligeholdelsesomkostninger og den næste servicedato for hver aktiv. Sporing af omkostninger til sporing af vedligeholdelse er vigtige at holde styr på af hensyn til budgetteringen og for at kunne træffe beslutningen, om et anlægsaktiv skal udskiftes. Du kan knytte hvert anlægsaktiv til en eller flere forsikringspolicer og kontrollere, at forsikringspræmierne stemmer overens med værdien af aktiverne.

| Til  | Se |
| --- | --- |
| Registrere servicebesøg, bogføre og overvåge reparationsomkostninger. |[Vedligeholde anlægsaktiver](fa-how-maintain.md) |
| Overvåge reparationsomkostninger. | [Overvåge reparationsomkostninger](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Opdatere forsikringsoplysninger, bogføre anskaffelsespriser til forsikringspolicer, ændre forsikringsdækning, få vist forsikringsstatistik og oversigter over forsikringspolicer. |[Forsikre anlægsaktiver](fa-how-insure.md) |
| Overvåge forsikringsdækning. | [Overvåge forsikringsdækning](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Ompostere, overføre, opdele/kombinere, regulere værdi, nedskrive og sælge anlægsaktiver

| Til  | Se |
| --- | --- |
| Ompostere anlægsaktiver, overføre anlægsaktiver til forskellige lokationer, opdele eller kombinere anlæg. |[Overføre, opdele eller kombinere anlægsaktiver](fa-how-trans-split-combine.md) |
| Regulere anlægsaktivernes værdier, bogføre opskrivnings- og nedskrivningstransaktioner. |[Omvurdere anlægsaktiver](fa-how-revalue.md) |
| Bogføre salgstransaktioner, have vist salgsposter og bogføre delvist salg. |[Afhænde eller lade anlægsaktiver udgå](fa-how-dispose-retire.md) |
| Have vist salgsposter. | [Vise anlægsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vis forventede salgsværdier. | [Vise forventede salgsværdier](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="see-also"></a>Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Oversigt over anlægsaktivsanalyser](fa-analytics-overview.md)  
[Oversigt for Finance](finance.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
