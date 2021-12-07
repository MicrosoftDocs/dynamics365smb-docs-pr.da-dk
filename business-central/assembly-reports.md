---
title: Samle rapporter og analyser i Business Central
description: Se, hvilke samling rapporter og analyser der er tilgængelige i standardversionen af Business Central, så du kan holde styr på virksomheden.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 91234cd02736d425116be40137efd9d068b5bd97
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216335"
---
# <a name="assembly-reports-and-analytics-in-business-central"></a>Samle rapporter og analyser i Business Central

Samlingsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gør det muligt for produktions-og erhvervs medarbejdere at få indsigt i og statistikker om aktuelle og tidligere montageaktiviteter.  

## <a name="reports"></a>Rapporter

I følgende tabel beskrives nogle af nøglerapporterne i samlingsrapporter.

|Report |Objekt-id|Beskrivelse  |
|---------|---------|---------|
|**Montagestyklister**|801|Viser en oversigt over styklister: navn, styklistenummer, styklistekomponenter og andre styklister, der indgår i styklisten. Styklistekomponenterne defineres i tabellen Styklistekomponent. Her kan du også se enhedskoden og den mængde, der er behov for for hver komponent pr. basisenhed. |
|**Vare - Kan blive (tid)**|5871|Viser, hvordan fem forskellige nøgletilgængelighedstal ændres over tid for en styklistevare. Disse tal ændres i overensstemmelse med forventede udbud og efterspørgsel, hændelser og forsyning, der er baseret på tilgængelige komponenter, der kan samles eller produceres.<br>Du kan bruge rapporten til at se, om du kan opfylde en salgsordre for en vare på en bestemt dato ved at kigge på den aktuelle tilgængelighed i kombination med de potentielle mængder, der kan levere dens komponenter, hvis en montageordre blev startet. Rapporten viser, hvornår og hvor mange enheder af en montage og produktionsvare du kan fremstille baseret på komponenttilgængelighed og varens aktuelle tilgængelighed. Dette vises som det samlede antal.<br>Oplysningerne vises i et diagram, hvor hver disponeringsfigur er en linje, der skrider frem langs tidslinjen og flytter op og ned, efterhånden som mængderne ændres. Mængdetallene kommer fra samme system, der leverer oplysninger til vinduet **Varedisponering pr. styklisteniveau**. |
|**Kostprisfordeling for stykliste**|5872|Viser grafisk, hvordan en samlet eller en produceret vares pris er fordelt gennem dens stykliste.<br>Sådanne oplysninger kan være nyttige under beslutningen af, om du skal ændre komponentleverandører, erstatte interne kapacitet -forbrug med udliciteret arbejdskraft eller omvendt, eller når du gennemgår og ændrer en vares stykliste for eksempel.<br>Det første diagram i rapporten viser de samlede kostpris for den overordnede vares komponenter og arbejdskraftressourcer opdelt i op til fem forskellige kostprisfordelinger og repræsenteres grafisk med forskellige farver.<br>Det cirkeldiagram med overskriften *Materiale/arbejdskraft*, viser den proportionale fordeling mellem den overordnede vares materiale- og arbejdskraftsomkostninger samt dets egne produktionsomkostninger. Materialekostprisfordeling omfatter varens materialeomkostninger. Arbejdskraftkostprisfordelingen omfatter kapacitet, kapacitetskostpris og underleverandøromkostninger. Kostpris andelene vises forskelligt, afhængigt af hvad du har valgt i feltet **Vis kun**.<br>Det cirkeldiagram, der hedder *Direkte/indirekte*, viser den proportionale fordeling mellem den overordnedes vares direkte og indirekte omkostninger. Den direkte kostprisfordeling omfatter varens materiale-, kapacitets- og underleverandøromkostninger. Den indirekte kostprisfordeling omfatter kapacitets- og produktionsomkostninger.<br>Tabellen nederst i rapporten, er inkluderet, når du vælger afkrydsningsfeltet Inkluder detaljer. Den viser de valgte værdier fra vinduet stykliste på omkostningsfordeling på et enkelt niveau eller akkumuleret, afhængigt af den indstilling, du vælger i feltet Vis omkostningsfordeling.|
|**Indgår-i-liste**|809|Viser en liste over, hvilke styklister de valgte varer indgår i. En nyttig oversigt, hvis du skal ændre en komponent i en STYKLISTE, der er indsat i et montageelement. Hvis leverandøren f. eks. ikke længere kan levere en bestemt vare, som du har brugt til montage/produktion. I sådanne scenarier giver denne rapport dig et hurtigt overblik over, hvilke styklister komponenten er inkluderet i. Du kan angive et filter for komponentens nummer.|
|**Stykliste - råvarer**|810|Denne rapport kan give dig et overblik over de nødvendige komponenter, både til montage og til produktion. Du kan se lagerbeholdningen, basisenheden, den hovedleverandør, hvis feltet Leverandørnr. skrives på selve varekortet og i leveringstiden.|
|**Stykliste - halvfabrikata**|811|Hvis du opretter og/eller samler halvfabrikata, kan du bruge denne rapport til at få vist en oversigt over denne type komponent. Denne rapport viser basisenheden, lageret, kostpris og alternativt varenummer. |
|**Montagestykliste - slutvarer**|812|Viser en oversigt over varer eller styklister, der ikke indgår i andre styklister. **Bemærk**: Denne rapport er ikke begrænset til kun at omfatte styklister, Husk at angive filter i feltet **Montagestykliste** eller på **Genbestillingssystem**.|
|**Montage til ordre - salg**|915|Viser vigtige salgstal for montagekomponentvarer, der kan sælges som en del af en montage i montage efter ordre-salg som en separat vare direkte fra lager.<br>Du kan bruge denne rapport til at analysere tallene for antal, pris, salg og fortjeneste for montagekomponenter til støtte for beslutninger, f.eks om en pakke skal have en anden pris, eller en bestemt vare ikke længere skal bruges i montager.<br>Rækken **Montage** viser salgstallene for det samlede antal, der sælges som en del af et montageelement. Det specifikke montageelementsalg, der udgør denne sum, vises, hvis du vælger feltet **Vis Montageelement - detaljer**.<br>Fokus er på montagekomponenter, men tallene beregnes fra avancemargenen for den overordnede vare, montageelementet. Salgsbeløbet for hver komponent beregnes derfor ud fra sine egne pris og avancemargenen for den overordnede i følgende formel.<br>Rapporten viser oplysninger om varer, der opfylder et eller begge af følgende kriterier:<br>- Findes i montagestykliste for en vare, der bruger Montage efter ordre-montagepolitik.<br>- Er blevet solgt som en del af et montage efter ordre-salg.|

## <a name="tasks"></a>Opgaver

I følgende artikler beskrives nogle af de vigtigste opgaver i forbindelse med analyse af virksomhedens tilstand:

* [Vise varedisponering](inventory-how-availability-overview.md)

## <a name="see-also"></a>Se også

[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-boms.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]