---
title: Opsætning af bæredygtighed
description: 'Få flere oplysninger om, hvordan du konfigurerer bæredygtighedsfunktioner.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Opsætning af bæredygtighed  

For at få bæredygtighedsmodulet til at fungere korrekt skal du først oprette nogle grundlæggende kontroller og instruktioner relateret til hele funktionaliteten.  

Følg de næste trin for at oprette et bæredygtighedsmodul:  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opsætning af bæredygtighed**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Generelt**, konfigurer de obligatoriske felter, der er relateret til dette modul:   

|  Felt  |  Beskrivelse  |  
|--------|--------------| 
| **Enhed for udledning** | Angiver den enhedskode, der bruges til at registrere udledning. |
| **Udledningsdecimaler** | Angiver det antal decimaler, der vises for udledningsbeløb. Standardindstillingen 2:5 angiver, at alle beløb vises med mindst 2 decimaler og højst 5 decimaler. Du kan også angive et fast tal, f.eks. 2, hvilket også betyder, at beløb vises med to decimaler. |
| **Land/område er obligatorisk** | Angiver, om land/område er obligatorisk. Du kan bruge dette felt i kladder uden at konfigurere dette, men du kan markere det, hvis du vil tvinge brugerne til at udfylde feltet, før de bogfører. |
| **Ansvarscenter obligatorisk** | Angiver, om ansvarscenter er obligatorisk, da ansvarscentret kan bruges som en facilitet til måling af facilty-baserede emissioner. Du kan bruge dette felt i kladder uden at konfigurere dette, men du kan markere det, hvis du vil tvinge brugerne til at udfylde feltet, før de bogfører. |
| **Blokberegning Grundlæggende ændring, hvis der findes finansposter** | Angiver, om ændringen af beregningsgrundlaget i kontokategorien er blokeret på tidspunktet for bæredygtighedsposten, hvilket betyder, at denne formel allerede er blevet anvendt. |
| **Aktiver fejlkontrol i baggrunden** | Angiver, om baggrundsfejlkontrol af bæredygtighedskladdelinjer er aktiveret. |

3.  I oversigtspanelet **Beregninger** skal du konfigurere obligatoriske felter relateret til de formler, der bruges til beregning af emissioner:  

|  Felt  |  Beskrivelse  |  
|--------|--------------| 
| **Decimaltal for brændstof/elektricitet** | Angiver det antal decimaler, der vises for brændstof/elektricitet-beløb. Standardindstillingen 2:5 angiver, at alle beløb vises med mindst 2 decimaler og højst 5 decimaler. Du kan også angive et fast tal, f.eks. 2, hvilket også betyder, at beløb vises med to decimaler. |
| **Afstandsdecimaler** | Angiver det antal decimaler, der vises for distancemålinger. Standardindstillingen 2:5 angiver, at alle beløb vises med mindst 2 decimaler og højst 5 decimaler. Du kan også angive et fast tal, f.eks. 2, hvilket også betyder, at beløb vises med to decimaler. |
| **Decimaler for brugerdefineret beløb** | Angiver det antal decimaler, der vises for tilpassede beløb. Standardindstillingen 2:5 angiver, at alle beløb vises med mindst 2 decimaler og højst 5 decimaler. Du kan også angive et fast tal, f.eks. 2, hvilket også betyder, at beløb vises med to decimaler. |

4.  Afslut opsætningen af oversigtspanelet **Rapportering**, der vedrører rapportering til myndigheder:   

|  Felt  |  Beskrivelse  |  
|--------|--------------| 
| **Enhedskode for udledningsrapportering** | Angiver den enhedskode, der bruges til at rapportere emission, da du kan bruge en anden enhed, mens du rapporterer til myndigheder. Dette felt er ikke relevant for standardrapporterne. |
| **Rapportering af UOM-faktor** | Angiver den enhedsfaktor, der bruges til at registrere udledning, hvis du kan bruge en anden enhed, mens du rapporterer til myndigheder. |
| **Nøjagtighed i afrunding af udledninger** | Angiver størrelsen på det interval, der skal bruges til afrunding af udledningsbeløb, mens du rapporterer til myndigheder. |
| **Type af udledningsafrunding** | Angiver, hvordan programmet afrunder en emissionsmængde under rapportering til myndigheder ved hjælp af indstillingerne: Nærmeste, Op eller Ned. |

>[!NOTE]
> I version 24.0 understøtter [!INCLUDE[prod_short](includes/prod_short.md)] ikke rapportering til nogen myndighed. Så det felt, der er relateret til konfigurationen i oversigtspanelet **Rapportering** , vil blive brugt til fremtidige rapporteringsfunktioner, men det kan også bruges af partnere i oversatte versioner.

## Se også  
[Finance](finance.md)    
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)
[Sådan kan du registrere udledninger](finance-sustainability-journal.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
