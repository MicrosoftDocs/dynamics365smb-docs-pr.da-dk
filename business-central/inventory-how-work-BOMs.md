---
title: Arbejde med styklister for at styre komponenter | Microsoft Docs
description: Du opretter en montagestykliste eller produktionsstykliste for at angive de komponenter eller ressourcer, der kræves for at sammensætte den vare, som styklisten repræsenterer.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a7cb9dc180ef2b5645ef773f63a2686a4d0ab0b6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240161"
---
# <a name="work-with-bills-of-material"></a>Arbejde med styklister
Du kan bruge styklister til at strukturere overordnede varer, der skal samles eller fremstilles af ressourcer eller produktionsressourcer fra komponenter. En montagestykliste kan også bruges til at sælge en overordnet vare som en pakke bestående af dens komponenter.

## <a name="assembly-boms-or-production-boms"></a>Montagestykliste eller produktionsstyklister
Du kan bruge montageordrer til at oprette slutvarer fra komponenter i en enkel proces, der kan udføres af en eller flere grundlæggende ressourcer, som ikke er produktions- eller arbejdscentre, eller uden nogen ressourcer. En montageproces kunne f.eks. være at plukke to vinflasker og én kaffesæk og pakke dem som en gave.  

En montagestykliste er masterdata, der definerer, hvilke komponentvarer der indgår i en monteret færdigvare, og hvilke ressourcer der bruges til at montere montageelementet. Når du angiver et montageelement og et antal i hovedet på en ny montageordre, udfyldes montageordrelinjerne automatisk i henhold til montagestyklisten med én montageordrelinje pr. komponent eller ressource. Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).

Montagestyklister er beskrevet i dette emne.

Du kan bruge produktionsordrer til at oprette slutvarer fra komponenter i en kompleks proces, der kræver en produktionsrute og arbejdscentre eller produktionsressourcer, som repræsenterer produktionskapacitet. F.eks. kunne en produktionsproces være at klippe stålplader i én handling, svejse dem i den næste operation og male færdigvaren i den sidste operation. Du kan finde flere oplysninger under [Produktion](production-manage-manufacturing.md).  

En produktionsstykliste er masterdata, der definerer en produktionsvare og de komponenter, der går ind i den. Ved montageelementer skal produktionsstyklisten certificeres og tildeles til produktionsvaren, før elementet kan bruges i en produktionsordre. Når du angiver produktionsvaren på en produktionsordrelinje, enten manuelt eller ved at opdatere ordren, bliver produktionsstyklisteindholdet komponenterne i produktionsordren. Du kan finde flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).  

Begrebet ressourcer i produktionen er langt mere avanceret end i montagestyring. Arbejdscentre og produktionsressourcer fungerer som ressourcer, og produktionstrin repræsenteres af operationer, der er tildelt til ressourcer i produktionsruter. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).

Både montageordrer og produktionsordrer kan knyttes direkte til salgsordrer. Du kan dog kun bruge montageordrer til at tilpasse færdigvaren direkte til en debitoranmodning med salgsordren.

## <a name="to-create-an-assembly-bom"></a>Sådan oprettes en montagestykliste
For at definere en overordnet vare, der består af andre elementer og potentielt af ressourcer, der kræves for at sammensætte den overordnede vare, skal du oprette en montagestykliste.  

Montagestyklister indeholder normalt varer, men kan også indeholde en eller flere ressourcer, der er påkrævet for at sammensætte montageelementet.

Montagestyklister kan have flere niveauer, hvilket betyder, at en komponent på montagestyklisten selv kan være et montageelement. I så fald skal feltet **Montagestykliste** på montagestyklistelinjen vise **Ja**.

Der gælder særlige krav for elementerne på montagestyklister for så vidt angår varedisponering. Du kan finde flere oplysninger i [Sådan får du vist tilgængeligheden af en vare via brugen af den i montagestyklister](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Montagestyklister oprettes ad to omgange:
- Oprette en ny vare
- Angive montageelementets styklistestruktur.

1. Opret en ny vare. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

    Fortsæt med at angive komponenter eller ressourcer på montagestyklisten.  
2. På siden **Varekort** for et montageelement skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
3. På siden **Montagestykliste** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Sådan får du vist komponenterne for et montageelement indrykket i overensstemmelse med styklistestrukturen
Fra siden **Montagestykliste** kan du åbne en separat side, der viser komponenterne og evt. ressourcer, der er indrykket i henhold til deres placering på styklisten under montageelementet.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for et montageelement. (Feltet **Montagestykliste** på siden **Varer** indeholder **Ja**).
3. På siden **Varekort** skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
4. På siden **Montagestykliste** skal du vælge handlingen **Vis stykliste**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Sådan erstattes montageelementet med dets komponenter på dokumentlinjer
Du kan bruge en særlig funktion til at erstatte linjen for montageelementet med nye linjer til dets komponenter fra et salgs- og købsdokument, som indeholder et montageelement. Denne funktion er nyttig f.eks., hvis du vil sælge komponenterne som en pakke, der repræsenterer et montageelement.

**Advarsel**: Når du har brugt funktionen **Udfold stykliste**, er det svært at annullere den igen. Du skal slette de salgsordrelinjer, der repræsenterer komponenterne og derefter indsætte en salgsordrelinje for montageelementet igen.

Følgende procedure er baseret på en salgsfaktura. Samme fremgangsmåde gælder for andre salgsdokumenter og alle købsdokumenter.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Salgsfakturaer** og derefter vælge det relaterede link.
2. Åbn en salgsfaktura, som indeholder en linje for et montageelement.
3. Vælg linjen for et montageelement og vælg derefter linjehandlingen **Udfold stykliste**.

Alle felter på salgsfakturalinjen for montageelementet fjernes med undtagelse af felterne **Vare** og **Beskrivelse**. Fuldførte salgsfakturalinjer indsættes for komponenterne og eventuelle ressourcer, der udgør montageelementet.

**Bemærk**: Funktionen Udfold stykliste findes også på siden **Montagestykliste**.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Sådan beregnes standardkostprisen et montageelement
Du kan beregne kostprisen for et montageelement ved at akkumulere kostprisen for hver komponent og ressource i elementets montagestykliste.

Du kan også beregne og opdatere standardkostprisen for en eller flere varer på siden **Standardkostpriskladde**. Du kan finde flere oplysninger i [Opdatere standardkostpriser](finance-how-to-update-standard-costs.md).  

En montagestyklistes kostpris svarer altid til den samlede kostpris for dens komponenter, herunder andre montagestyklister, og eventuelle ressourcer.

1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport**, angive **Varer** og derefter vælge det relaterede link.
2. Åbn kortet for et montageelement. (Feltet **Montagestykliste** på siden **Varer** indeholder **Ja**).
3. På siden **Varekort** skal du vælge handlingen **Montage** og derefter vælge handlingen **Montagestykliste**.
4. På siden **Montagestykliste** skal du vælge handlingen **Beregn kostpris**.
5. Vælg en af følgende muligheder, og klik derefter på knappen **OK**.

|Indstilling |Beskrivelse |
|-------|------------|
|**Øverste niveau**|Beregner montageelementets standardkostpris som kostbeløbet for alle elementer, der er købt eller monteret på montagestyklisten uanset eventuelle underliggende montagestyklister.|
|**Alle niveauer**|Beregner montageelementets standardkostpris som summen af: 1) Den beregnede kostpris for alle underliggende montagestyklister på montagestyklisten. 2) Kostprisen for alle indkøbte varer på montagestyklisten.|



Omkostningerne ved de elementer, der udgør montagestyklisten, kopieres fra komponentvarekortene. Kostprisen på hver vare ganges med antallet, og den samlede kostpris vises i feltet **Kostpris** på varekortet.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Vise varedisponering](inventory-how-availability-overview.md)     
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
