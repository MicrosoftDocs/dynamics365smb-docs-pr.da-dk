---
title: Opsætning af bæredygtighed
description: 'Få flere oplysninger om, hvordan du konfigurerer bæredygtighedsfunktioner.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-setup"></a>Opsætning af bæredygtighed

For at få bæredygtighedsmodulet til at fungere korrekt skal du først oprette nogle grundlæggende kontroller og instruktioner relateret til hele funktionaliteten.

Følg de næste trin for at oprette et bæredygtighedsmodul:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af bæredygtighed**, og vælg derefter det relaterede link.
2. I oversigtspanelet **Generelt**, konfigurer de obligatoriske felter, der er relateret til bæredygtighedsmodulet:

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Enhed for udledning** | Angiver den enhedskode, der bruges til at registrere udledninger. |
    | **Udledningsdecimaler** | Angiv det antal decimaler, der vises for udledningsbeløb. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |
    | **Land/område er obligatorisk** | Angiv, om land/område er obligatorisk. Brugere kan angive feltet land/område i kladder, selvom du ikke markerer dette felt. Men hvis du vælger det, skal brugerne angive feltet land/område, før der bogføres. |
    | **Ansvarscenter obligatorisk** | Angiv, om ansvarscenter er obligatorisk. Ansvarscentret kan bruges som et anlæg, så du kan måle anlægsbaserede emissioner. Brugere kan angive Ansvarscenter-feltet i kladder, selvom du ikke markerer dette felt. Men hvis du vælger det, skal brugerne angive Ansvarscenter-feltet, før der bogføres. |
    | **Blokberegning Grundlæggende ændring, hvis der findes finansposter** | Angiv, om ændringer af beregningsgrundlaget (formel) i kontokategoriniveauet er blokeret på tidspunktet for bæredygtighedsposten, når formlen allerede er blevet anvendt. |
    | **Aktiver fejlkontrol i baggrunden** | Angiv, om baggrundsfejlkontrol af bæredygtighedskladdelinjer er aktiveret. |

    > [!NOTE]
    > Når du har aktiveret eller deaktiveret baggrundsfejlkontrol i kladder, skal du logge ind igen, før du starter den nye opsætning.

3. I oversigtspanelet **Beregninger** skal du konfigurere obligatoriske felter relateret til de formler, der bruges til beregning af emissioner.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Decimaltal for brændstof/elektricitet** | Angiv det antal decimaler, der vises for brændstof/elektricitet-beløb. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |
    | **Afstandsdecimaler** | Angiv det antal decimaler, der vises for distancemålinger. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |
    | **Decimaler for brugerdefineret beløb** | Angiv det antal decimaler, der vises for tilpassede beløb. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |

4. I oversigtspanelet **Rapportering** skal du fuldføre opsætningen ved at konfigurere de felter, der er relateret til rapportering til myndigheder.

    > [!NOTE]
    > I version 24.0 understøtter [!INCLUDE[prod_short](includes/prod_short.md)] ikke rapportering til nogen myndighed. De felter, der er relateret til konfigurationen af denne funktionalitet i oversigtspanelet **Rapportering**, er derfor beregnet til fremtidige rapporteringsfunktioner. Partnere kan dog også bruge disse felter i oversatte versioner.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Enhedskode for udledningsrapportering** | Angiv den enhedskode, der bruges til at rapportere udledninger, da du kan bruge en anden enhed, når du rapporterer til myndigheder. Dette felt er ikke relevant for standardrapporterne. |
    | **Rapportering af UOM-faktor** | Angiv den enhedsfaktor, der bruges til at registrere udledninger, hvis du kan bruge en anden enhed, når du rapporterer til myndigheder. |
    | **Nøjagtighed i afrunding af udledninger** | Angiv størrelsen på det interval, der bruges til afrunding af udledningsbeløb, når du rapporterer til myndigheder. |
    | **Type af udledningsafrunding** | Angiv, hvordan udledningsmængder afrundes, når du rapporterer til myndighederne. Du kan vælge mellem følgende indstillinger: **Nærmeste**, **Op** og **Ned**. |

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Oversigt over Ledelse af bæredygtighed](finance-manage-sustainability.md)  
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)  
[Registrer bæredygtighedsposter](finance-sustainability-journal.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
