---
title: Produktionsrapporter og analyser
description: Se, hvilke produktionsrapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216333"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Produktionsrapporter og analyser i Business Central

Produktionsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for produktions-og erhvervs medarbejdere at få indsigt i og statistikker om aktuelle og tidligere produktionsaktiviteter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i produktionsrapportering.

|Report |Objekt-id|Beskrivelse  |
|---------|---------|---------|
|**Styklisteudfold. - antal**|99000753|Viser en indrykket styklisteoversigt med den vare/de varer, du angiver i filtrene. Produktionsstyklisten er fuldstændig udfoldet (alle niveauer).|
|**Vare - Kan blive (tid)**|5871|Viser, hvordan fem forskellige nøgletilgængelighedstal ændres over tid for en styklistevare. Disse tal ændres i overensstemmelse med forventede udbud og efterspørgsel, hændelser og forsyning, der er baseret på tilgængelige komponenter, der kan samles eller produceres.<br>Du kan bruge rapporten til at se, om du kan opfylde en salgsordre for en vare på en bestemt dato ved at kigge på den aktuelle tilgængelighed i kombination med de potentielle mængder, der kan levere dens komponenter, hvis en montageordre blev startet. Rapporten viser, hvornår og hvor mange enheder af en montage og produktionsvare du kan fremstille baseret på komponenttilgængelighed og varens aktuelle tilgængelighed. Dette vises som det samlede antal.<br>Oplysningerne vises i et diagram, hvor hver disponeringsfigur er en linje, der skrider frem langs tidslinjen og flytter op og ned, efterhånden som mængderne ændres. Mængdetallene kommer fra samme system, der leverer oplysninger til vinduet **Varedisponering pr. styklisteniveau**. |
|**Kostprisfordeling for stykliste**|5872|Viser grafisk, hvordan en samlet eller en produceret vares pris er fordelt gennem dens stykliste.<br>Sådanne oplysninger kan være nyttige under beslutningen af, om du for eksempel skal ændre komponentleverandører, erstatte interne kapacitet -forbrug med udliciteret arbejdskraft eller omvendt, eller når du gennemgår og ændrer en vares stykliste.<br>Det første diagram i rapporten viser de samlede kostpris for den overordnede vares komponenter og arbejdskraftressourcer opdelt i op til fem forskellige kostprisfordelinger og repræsenteres grafisk med forskellige farver.<br>Det cirkeldiagram med overskriften *Materiale/arbejdskraft*, viser den proportionale fordeling mellem den overordnede vares materiale- og arbejdskraftsomkostninger samt dets egne produktionsomkostninger. Materialekostprisfordeling omfatter varens materialeomkostninger. Arbejdskraftkostprisfordelingen omfatter kapacitet, kapacitetskostpris og underleverandøromkostninger. Kostpris andelene vises forskelligt, afhængigt af hvad du har valgt i feltet **Vis kun**.<br>Det cirkeldiagram, der hedder *Direkte/indirekte*, viser den proportionale fordeling mellem den overordnedes vares direkte og indirekte omkostninger. Den direkte kostprisfordeling omfatter varens materiale-, kapacitets- og underleverandøromkostninger. Den indirekte kostprisfordeling omfatter kapacitets- og produktionsomkostninger.<br>Tabellen nederst i rapporten, er inkluderet, når du vælger afkrydsningsfeltet **Inkluder detaljer**. Den viser de valgte værdier fra vinduet stykliste på omkostningsfordeling på et enkelt niveau eller akkumuleret, afhængigt af den indstilling, du vælger i feltet **Vis omkostningsfordeling**.|
|**Detaljeret beregning**|99000756|Viser kostprisoversigt pr. vare under hensyntagen til spild.|
|**Indgår-i (højeste niveau)**|99000757|Viser hvor og i hvilke antal varerne anvendes i produktionsstrukturen.<br>Rapporten viser kun varen som Indgår-i, hvis basisvaren anvendes som vare på øverste niveau. Hvis f.eks. varen A anvendes til at producere varen B, og varen B anvendes til at producere varen C, viser rapporten varen B, hvis du kører en rapport for varen A. Hvis du kører rapporten for varen B, vises C som Indgår-i.<br>Du kan også åbne siden **Indgår-i-linje** direkte fra programmet.|
|**Styklistesammenligningsoversigt**|99000758|Denne rapport giver dig mulighed for at sammenligne produkter, som er færdige med hensyn til omkostningerne. Du kan få vist en oversigt med alle komponenter og deres omkostninger samt de nødvendige antal. Beregningsdatoen er normalt angivet til arbejdsdatoen. |
|**Prod.ordrestatistik**|99000791|Angiver de forskellige kostpriser, der er akkumuleret i den valgte produktionsordre.<br>Indholdet af rapporten er meget lig siden **Prod.ordrestatistik**.<br>For en produktionsordre, der bruger *Fremstil til ordre*-produktionsmetoden, viser vinduet kun materiale og kapacitetskostpris for varer på det højeste niveau i styklisten.|
|**Kapacitet - operationsliste**|99000780|Viser de produktionsordrer, der venter på at blive behandlet i arbejdscentre og produktionsressourcer. Der udskrives oversigter vedrørende kapaciteten i arbejdscentret eller produktionsressourcen. Rapporten indeholder bl.a. oplysninger om start-/slutdato og forfaldsdato samt tilgangsantal.|
|**Arbejdscenterbelastning** eller **produktionsressource belastning**|99000783 eller 99000784|Begge rapporter viser en oversigt over belastningen af arbejds-/maskincenter. Belastningen i et arbejds-/maskincenter er summen af det nødvendige antal gange, alle planlagte og aktuelle ordrer køres i arbejdscentret i en angivet periode.|
|**Prod.ordre mankoliste**|99000788|Denne rapport kan bruges til at få vist alle komponenter, der ikke er tilgængelige pga. manglende lagerbeholdning. Derfor kan denne oversigt bruges til at få vist tidslinjen for en planlagt eller frigivet produktionsordre, hvis det planlagte tidspunkt kan bevares.|


## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Vise belastningen på arbejdscentre og produktionsressourcer](production-how-to-view-the-load-on-work-centers.md)  
* [Vise varedisponering](inventory-how-availability-overview.md)

## <a name="see-also"></a>Se også

[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]