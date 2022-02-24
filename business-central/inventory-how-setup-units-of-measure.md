---
title: Sådan oprettes vareenheder | Microsoft Docs
description: Du kan konfigurere flere enheder for en vare, så du kan knytte enheder til varen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 07/06/2020
ms.author: SorenGP
ms.openlocfilehash: 7251be2de0cd8b368f0510596b0c695a93acc4b6
ms.sourcegitcommit: 7d05fc049d81cae9b2b711101cdaea037b7ba61f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535943"
---
# <a name="set-up-units-of-measure"></a>Oprette måleenheder

Som en del af opsætningen af [!INCLUDE [prodshort](includes/prodshort.md)] kan du konfigurere generelle måleenheder på siden **Måleenheder**. Når du derefter registrerer nye varer, skal du angive basisenheden på **Varekortet**. Men du kan også tilføje måleenheder senere.  

Du kan konfigurere flere enheder for en vare, så du kan knytte enheder til varen til følgende formål:

- Tildel en basisenhed på varens varekort for at definere, hvordan den opbevares på lageret, og til at fungere som konverteringsbasis for alternative enheder.
- Tildel alternative enheder til købs -, produktions- eller salgsdokumenter for at angive, hvor mange enheder af basisenheden du håndterer ad gangen i disse processer. F.eks. kan du køber varen i paller og kun bruge den enkeltvis i din produktion.

Hvis en vare lagerføres i én enhed, men produceres i en anden, kan der oprettes en produktionsordre, hvor der bruges en produktionskladdeenhed til beregning af det rigtige antal komponenter under kørslen af **Opdater produktionsordre**. Produktionskladdeenheden kan f.eks. bruges til beregning, når den producerede vare lagerføres i enheder, men produceres i ton. Du kan finde flere oplysninger i [Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

## <a name="to-set-up-units-of-measure"></a>Sådan oprettes måleenheder

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Enheder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. En ny tom linje er indsat.  
3. Udfyld felterne. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Hvis du ved, at din organisation sælger varer med denne enhed til kunder i andre lande, kan du tilføje oversættelser.  
    1. Marker den kode, du vil konfigurere oversættelser for, og vælg derefter handlingen **Oversættelser**.
    2. Vælg rullepilen i feltet **Sprogkode** for at se en liste over tilgængelige sprogkoder. Vælg den sprogkode, du vil angive en oversættelse til, og klik derefter på OK for at kopiere koden over i feltet.
    3. Indsæt den relevante tekst i feltet **Beskrivelse**.
5. Gentag de forrige trin for eventuelle yderligere enheder, som du vil tilføje.  

Når du registrerer en ny vare, kan du vælge basisenheden på listen over de måleenheder, som du har oprettet. Du kan også angive flere enheder for en vare.  

## <a name="to-set-up-multiple-item-units-of-measure"></a>Sådan konfigurerer du flere vareenheder

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn varekortet for den vare, du vil angive alternative enheder for.
3. Vælg handlingen **Enheder**. Siden **Vareenheder** åbnes.
4. Hvis feltet **Basisenhed** på varekortet er udfyldt, er denne enhed allerede konfigureret.
5. Vælg handlingen **Ny**. En ny tom linje er indsat.
6. I feltet **Kode** skal du indtaste navnet på enheden. Du kan også vælge feltet for at vælge mellem de enhedskoder, der er i databasen.
7. I feltet **Antal pr. enhed** kan du indtaste, hvor mange enheder, målt i basisenheder, den nye måleenhed indeholder.
8. I felterne **Højde**, **Bredde**, **Længde** og **Vægt** kan du angive nøjagtige oplysninger om størrelsen af én enhed, så [!INCLUDE [prodshort](includes/prodshort.md)] kan beregne, hvor mange af de enkelte vareenheder der kan anbringes på en bestemt placering. Feltet **Rummål** beregnes automatisk ud fra **Højde**, **Bredde** og **Længde**.

    Hvis et af disse felter indeholder en anden værdi end 0, bruges dette mål i alle processer, der omfatter placering af varer: læg-på-lager, bevægelser, modtagelser, leverancer, pluk og reguleringer. [!INCLUDE [prodshort](includes/prodshort.md)] kontrollerer summen af hvert fysiske mål på varer, der lægges på plads, og på varer, der allerede findes på placeringen, op imod den maksimale størrelse eller andet mål, der kan være på placeringen, ifølge den placeringskapacitetsregel, som er valgt på lokationskortet for varen. Det vil sige, at du skal bruge samme måleenhed for hver dimension på alle vareenheder - brug f.eks. kilogram eller pund som vægt, men vær konsekvent.
9. Gentag trin 5 til 7 for at oprette alle de alternative enheder, du ønsker at bruge i forskellige processer til denne vare.

    I feltet **Basisenhed** nederst i vinduet kan du vise eller ændre varens basisenhed. Du kan også ændre basisenheden i feltet **Basisenhed** på varekortet. På siden **Basisenhed** skal basisenheden have værdien **1** i feltet **Antal pr. enhed på**.

Du kan nu bruge alternative enheder på købs-, produktions- og salgsdokumenter som beskrevet i afsnittet [Sådan angives en standardenhedskode for salgs-og købstransaktioner](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## <a name="to-set-up-unit-of-measure-translations"></a>Sådan oprettes enhedsoversættelser

Når du sælger varer til udenlandske kunder, kan det være nødvendigt at angive enheden på kundens sprog. Det kan du gøre, når du har defineret de nødvendige enhedsoversættelser.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Enheder**, og vælg derefter det relaterede link.
2. Marker den kode, du vil konfigurere oversættelser for, og vælg derefter handlingen **Oversættelser**.
3. Vælg rullepilen i feltet **Sprogkode** for at se en liste over tilgængelige sprogkoder. Vælg den sprogkode, du vil angive en oversættelse til, og klik derefter på OK for at kopiere koden over i feltet.
4. Indsæt den relevante tekst i feltet **Beskrivelse**.
5. Gentag trinnene 2 til 4 for alle enhedskoder og sprog, du vil indsætte oversættelser til.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Sådan angives en standardenhedskode for salgs- og købstransaktioner

Hvis du normalt køber eller sælger i andre enheder end basisenheden, kan du angive særskilte enheder, som skal bruges ved køb og salg. Det gør du ved at definere enhederne på siden **Vareenheder**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn det varekort, du vil angive en standardenhedskode for salg eller køb.
3. For salg skal du i oversigtspanelet **Fakturering** i feltet **Salgsenhed** åbne siden **Vareenheder**.
4. For køb skal du i oversigtspanelet **Genbestilling** i feltet **Købsenhed** åbne siden **Vareenheder**.
5. Vælg den kode, du vil angive som standardenhed for henholdsvis salg eller køb, og vælg derefter knappen **OK**.

## <a name="see-also"></a>Se også

[Arbejde med produktionskladdeenheder](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Administrere lager](inventory-manage-inventory.md)  
[Administrere indkøb](purchasing-manage-purchasing.md)  
[Administrere salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
