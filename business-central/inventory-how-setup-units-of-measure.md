---
title: "Sådan oprettes vareenheder | Microsoft Docs"
description: "Du kan konfigurere flere enheder for en vare, så du kan knytte enheder til varen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b920a3edfab41409cd8d7cf3f5e463f66268e953
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-item-units-of-measure"></a>Oprette vareenheder
Du kan konfigurere flere enheder for en vare, så du kan knytte enheder til varen til følgende formål:

- Tildel en basisenhed på varens varekort for at definere, hvordan den opbevares på lageret, og til at fungere som konverteringsbasis for alternative enheder.
- Tildel alternative enheder til købs -, produktions- eller salgsdokumenter for at angive, hvor mange enheder af basisenheden du håndterer ad gangen i disse processer. F.eks. kan du køber varen i paller og kun bruge den enkeltvis i din produktion.

Hvis en vare lagerføres i én enhed, men produceres i en anden, kan der oprettes en produktionsordre, hvor der bruges en produktionskladdeenhed til beregning af det rigtige antal komponenter under kørslen af **Opdater produktionsordre**. Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton. Du kan finde flere oplysninger i [Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Sådan oprettes en enhed
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn varekortet for den vare, du vil angive alternative enheder for.
3. Vælg handlingen **Enheder**. Vinduet **Vareenheder** åbnes.
4. Hvis feltet **Basisenhed** på varekortet er udfyldt, er denne enhed allerede konfigureret.
5. Vælg handlingen **Ny**. En ny tom linje er indsat.
6. I feltet **Kode** skal du indtaste navnet på enheden. Du kan også vælge feltet for at vælge mellem de enhedskoder, der er i databasen.
7. I feltet **Antal pr. enhed** kan du indtaste, hvor mange enheder, målt i basisenheder, den nye måleenhed indeholder.
8. Gentag trin 5 til 7 for at oprette alle de alternative enheder, du ønsker at bruge i forskellige processer til denne vare.

Du kan nu bruge de alternative enheder på købs-, produktions- og salgsdokumenter. Du kan finde flere oplysninger i Angive standardenhedskoder for købs- og salgstransaktioner eller Bruge produktionskladdeenhedskoden.

## <a name="to-set-up-unit-of-measure-translations"></a>Sådan oprettes enhedsoversættelser
Når du sælger varer til udenlandske kunder, kan det være nødvendigt at angive enheden på kundens sprog. Det kan du gøre, når du har defineret de nødvendige enhedsoversættelser.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Enheder**, og vælg derefter det relaterede link.
2. Marker den kode, du vil konfigurere oversættelser for, og vælg derefter handlingen **Oversættelser**.
3. Vælg rullepilen i feltet **Sprogkode** for at se en liste over tilgængelige sprogkoder. Vælg den sprogkode, du vil angive en oversættelse til, og klik derefter på OK for at kopiere koden over i feltet.
4. Indsæt den relevante tekst i feltet **Beskrivelse**.
5. Gentag trinnene 2 til 4 for alle enhedskoder og sprog, du vil indsætte oversættelser til.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Sådan angives en standardenhedskode for salgs- og købstransaktioner
Hvis du normalt køber eller sælger i andre enheder end basisenheden, kan du angive særskilte enheder, som skal bruges ved køb og salg. Det gør du ved at definere enheden i vinduet **Vareenheder**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn det varekort, du vil angive en standardenhedskode for salg eller køb.
3. For salg skal du i oversigtspanelet **Fakturering** i feltet **Salgsenhed** åbne vinduet **Vareenheder**.
4. For køb skal du i oversigtspanelet **Genbestilling** i feltet **Købsenhed** åbne vinduet **Vareenheder**.
5. Vælg den kode, du vil angive som standardenhed for henholdsvis salg eller køb, og vælg derefter knappen **OK**.

## <a name="see-also"></a>Se også
[Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Administrere lager](inventory-manage-inventory.md)  
[Administrere indkøb](purchasing-manage-purchasing.md)  
[Administrere salg](sales-manage-sales.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

