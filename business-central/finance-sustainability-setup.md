---
title: Opsætning af bæredygtighed
description: 'Få flere oplysninger om, hvordan du konfigurerer bæredygtighedsfunktioner.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Opsætning af bæredygtighedsmodul

For at få bæredygtighedsmodulet til at fungere korrekt skal du først oprette nogle grundlæggende kontroller og instruktioner relateret til hele funktionaliteten.

Følg de næste trin for at oprette et bæredygtighedsmodul:

## <a name="role-center"></a>Rollecenter

For personer, hvis primære ansvarsområder involverer bæredygtighedsprocesser, anbefales det at bruge rollecenteret *Bæredygtighedschef* . Følg trinnene for at konfigurere dette rollecenter:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Mine indstillinger**, og vælg derefter den relaterede sammenkæde.
2. I feltet **Rolle** skal du vælge siden **Tilgængelige roller** .
3. Vælg linjen **Bæredygtighedschef** .
4. Vælg **OK**.

 *Rollecenteret Sustainability Manager* faciliterer effektiv styring af alle nøgleområder relateret til bæredygtighed. Det omfatter centrale bæredygtighedsfunktioner samt finansierings- og indkøbsprocesser. Derudover giver det synlighed i de mest kritiske bæredygtighedsrelaterede KPI'er.

## <a name="sustainability-setup"></a>Opsætning af bæredygtighed

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

3.  **I oversigtspanelet Indkøb** skal du konfigurere de obligatoriske felter, der er relateret til brugen af bæredygtighedsfunktioner i købsprocessen.  

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Brug emissioner i købsdokumenter** | Hvis du aktiverer dette felt, vises bæredygtighedsrelaterede felter og funktioner i købsdokumenterne, f.eks. **. Bæredygtighedskonto** eller forskellige emissioner. |

4. I oversigtspanelet **Beregninger** skal du konfigurere obligatoriske felter relateret til de formler, der bruges til beregning af emissioner.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Decimaltal for brændstof/elektricitet** | Angiv det antal decimaler, der vises for brændstof/elektricitet-beløb. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |
    | **Afstandsdecimaler** | Angiv det antal decimaler, der vises for distancemålinger. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |
    | **Decimaler for brugerdefineret beløb** | Angiv det antal decimaler, der vises for tilpassede beløb. Standardindstillingen *2:5* angiver, at alle beløb vises med mindst to decimaler og højst fem decimaler. Du kan også angive et fastlagt nummer. Hvis du f.eks. indtaster *2*, vises der to decimaler for alle beløbene. |

5. I oversigtspanelet **Rapportering** skal du fuldføre opsætningen ved at konfigurere de felter, der er relateret til rapportering til myndigheder.

    > [!NOTE]
    > I version 24.0 understøtter [!INCLUDE[prod_short](includes/prod_short.md)] ikke rapportering til nogen myndighed. De felter, der er relateret til konfigurationen af denne funktionalitet i oversigtspanelet **Rapportering**, er derfor beregnet til fremtidige rapporteringsfunktioner. Partnere kan dog også bruge disse felter i oversatte versioner.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Enhedskode for udledningsrapportering** | Angiv den enhedskode, der bruges til at rapportere udledninger, da du kan bruge en anden enhed, når du rapporterer til myndigheder. Dette felt er ikke relevant for standardrapporterne. |
    | **Rapportering af UOM-faktor** | Angiv den enhedsfaktor, der bruges til at registrere udledninger, hvis du kan bruge en anden enhed, når du rapporterer til myndigheder. |
    | **Nøjagtighed i afrunding af udledninger** | Angiv størrelsen på det interval, der bruges til afrunding af udledningsbeløb, når du rapporterer til myndigheder. |
    | **Type af udledningsafrunding** | Angiv, hvordan udledningsmængder afrundes, når du rapporterer til myndighederne. Du kan vælge mellem følgende indstillinger: **Nærmeste**, **Op** og **Ned**. |

## <a name="emission-fees"></a>Udledningsafgifter

Hvis du vil spore interne kulstofgebyrer eller beregne dine emissioner ved hjælp af kuldioxidækvivalenter (CO2), skal du konfigurere **siden Emissionsgebyrer** . Følg disse trin for at konfigurere disse oplysninger:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Emissionsgebyrer**, og vælg derefter den relaterede sammenkæde. 
2. Vælg den **drivhusgasudledning, du vil konfigurere, i feltet Emissionstype** : **CO2**, **CH4** eller **N2O**. Denne mulighed er obligatorisk.   
3. Du kan angive Områdetype **yderligere**. Hvis du lader dette felt være tomt, gælder det for alle områder, men du kan konfigurere for hvert område.  
4. Du kan konfigurere **Startdato** og **Slutdato**. Dette særlige betyder, at du kan bruge forskellige konfigurationer i forskellige perioder. 
5. Lande **-/områdekoden** og **ansvarskoden** er valgfrie, og du kan vælge, om du vil bruge dem. Disse felter kan være nyttige, da det er muligt at have forskellige kulstofgebyrer pr. land eller at bruge forskellige konverteringer til CO2e pr. land eller pr. anlæg (ansvarscenter).  
6.  **Feltet Carbon Fee** repræsenterer det interne kulstofgebyr, som en virksomhed opkræver selv for hver enhed CO2-ækvivalent, den udleder. Det kan bruges baseret på nogle lokale eller regionale regler, men også til interne beregninger. **Carbon Fee** beregnes hver gang, når du bogfører emissioner, og disse oplysninger vil være synlige på bæredygtighedsposterne **uden** yderligere bogføring på **finansposter**. Du kan angive CO2-afgift **pr. enhed, som du har i bæredygtighedsopsætningen**  **, og den kan kun udfyldes for den linje, hvor** emissionstypen **er** CO2 **.** 
7.  **Kulstofækvivalentfaktoren** specificerer den koefficient, der omdanner virkningen af forskellige drivhusgasser til den tilsvarende mængde kuldioxid baseret på deres globale opvarmningspotentiale.  **Hvis emissionstypen** er CO2, vil kulstofækvivalentfaktoren **altid** være *1*, og du kan ikke ændre denne værdi, fordi CO2 er den referencegas, der bruges til beregning af det globale opvarmningspotentiale (GWP) for andre drivhusgasser; da CO2 er basislinjen, er dens GWP sat til *1*. For andre drivhusgasser skal brugerne konfigurere værdierne manuelt. For at foretage korrekt beregning kan du bruge følgende eksempel: Hvis vi antager, at 1 kg N2O svarer til 298 kg CO2, skal du beregne 1/298, og det resultat, du skal udfylde, vil være 0.00336.  

> [!NOTE]
> **Feltet CO2-gebyr** i bæredygtighedsposterne **beregnes** ikke ud fra CO2-emissionsværdierne **·** . I stedet, som grundlag for denne formel, [!INCLUDE[prod_short](includes/prod_short.md)]  vil bruge **feltet CO2e-udledning** . **Feltet CO2e-emission** beregnes ud fra alle de emissioner, der er bogført til posten, og den CO2-ækvivalentfaktor **,** der er konfigureret for hver af gasserne **på siden Emissionsgebyrer** .  

Hvis du ikke konfigurerede **emissionsgebyrerne**, før du offentliggjorde dine bæredygtighedsposter, og du vil beregne dine kulstofgebyrer og CO2e med tilbagevirkende kraft, skal du køre handlingen **Beregn emissionsgebyrer** for at opdatere værdierne på **bæredygtighedsposterne**.  

## <a name="see-also"></a>Se også

[Finance](finance.md)    
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)    
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)    
[Registrer bæredygtighedsposter](finance-sustainability-journal.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
