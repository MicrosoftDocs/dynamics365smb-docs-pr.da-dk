---
title: Om montage til ordre og montage til lager | Microsoft Docs
description: Montageelementer kan leveres, enten ved at montere dem, når de er bestilt, eller ved at montere dem for opbevaring på lageret, indtil der er brug for dem på en salgsordre.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 89a2e2390950bbba0f5d0e93db5ed72359fd637f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747412"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Om montage til ordre og montage til lager
Montageelementer kan leveres med følgende to fremgangsmåder:  

-   Montage efter ordre.  
-   Montage til lager.  

## <a name="assemble-to-order"></a>Montage efter ordre  
Du bruger typisk *montage efter ordre* for varer, som du ikke ønsker på lager, fordi du forventer at tilpasse dem til debitoranmodninger, eller fordi du vil minimere de generelle lageromkostninger. Understøttelsesfunktionerne omfatter:  

-   Muligheden for at tilpasse montageelementer, når du tager imod en salgsordre.  
-   Oversigt over tilgængeligheden af montageelementet og dets komponenter.  
-   Muligheden for at reservere montagekomponenter med det samme for at sikre, at ordren kan opfyldes.  
-   Funktion til at bestemme rentabiliteten af den tilpassede ordre ved at akkumulere pris og pris.  
-   Integration med lageret for at gøre montage og levering lettere.  
-   Muligheden for montage efter ordre, når der skal laves et salgstilbud eller en rammesalgsordre.  
-   Muligheden for at kombinere lagerantal med montage efter ordre-mængder.  

I montage efter ordre-processen samles varen som svar på en salgsordre og med en én til én-sammenkædning mellem montageordren og salgsordren.  

Når du indtaster en montage til ordre-vare på en salgslinje, oprettes der automatisk en montageordre med et hoved, der er baseret på salgslinjen og med linjer, der er baseret på varens montagestykliste ganget med ordrestørrelsen. Du kan bruge siden **Montage efter ordre-linjer** for at se de sammenkædede montageordrelinjer, som kan understøtte din tilpasning af montageelementet og en leveringsdato, der er baseret på oplysninger om komponenttilgængelighed. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Selvom det ikke er en del af standardprocessen, kan du sælge lagermængder med montage efter ordre-mængderne. Du kan finde flere oplysninger i [Sælge lagervarer i montage til ordre-flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 For at aktivere denne proces skal feltet **Assembly politik** på varekortet være **Montage efter ordre**.  

## <a name="assemble-to-stock"></a>Montage til lager  
 Du bruger typisk *montage til lager* for de varer, du vil samle forud for salg, f.eks for at forberede en pakkekampagne og holde på lager, indtil de er bestilt. Disse varer er som regel standardvarer som emballerede pakker, du ikke tilbyder at tilpasse efter kundens behov.  

 Varen samles uden et øjeblikkelig salgsbehov i montage til lager-processen og lagerføres som en lagervare til senere salg eller forbrug som halvfabrikata. Du kan finde flere oplysninger i [Montere varer](assembly-how-to-assemble-items.md). Fra dette punkt plukkes og behandles varen som en enkelt vare og behandles som en færdig produktionsvare.  

 Når du indtaster en montage til lager-vare på en salgslinje, sælges linjen som alle andre varer fra lageret. For eksempel kontrolleres tilgængelighed kun for montageelementet.  

> [!NOTE]  
>  Selvom det ikke er en del af standardprocessen, kan du montere en vare efter ordre, selvom den er indstillet til montage til lager. Du kan finde flere oplysninger i [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 For at aktivere denne proces skal feltet **Assembly politik** på varekortet være **Montage-til-lager**.  

## <a name="combination-scenarios"></a>Kombinationsscenarier  
 Et generelt princip i montagestyring er, når de kombineres på en salgsordrelinje, skal montage efter ordre-mængder leveres før lagerbeholdning.  

 Hvis en montageordre er knyttet til en salgsordrelinje, kopieres værdien i feltet **Mgd. til montage til ordre** på salgsordrelinjen til feltet **Antal til montage** via feltet **Antal** på montageordrehovedet. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Desuden relateres værdien i feltet **Antal til montage** til feltet **Lever antal** på salgsordrelinjen, og denne relation administrerer leverancebogføringen af montage til ordre-mængder, både delvist og fuldstændigt. Dette gælder både, når hele salgslinjeantal er monteret efter ordre og i kombinationssituationer, hvor én del af salgslinjeantallet er monteret efter ordre, og en anden del afsendes fra lageret. I kombinationsscenariet har du dog ekstra fleksibilitet ved delvis levering, hvor du kan ændre feltet **Antal til montage** inden for foruddefinerede regler til at angive, hvor mange enheder der skal leveres delvist fra lageret, og hvor mange der skal leveres delvist ved montage efter ordre.  

 Hvis hele salgslinjemængden skal samles til ordre og leveres, så kopieres værdien i feltet **Lever (antal)** til feltet **Antal til montage** på den tilknyttede montageordre, når du ændrer den mængde, der skal leveres. Dette sikrer, at den mængde, der leveres, leveres fuldstændig af montage til ordre-mængden.  

 Men i kombinationsscenarier kopieres den fulde værdi i **Lever (antal)** ikke til feltet **Antal til montage** på montageordrehovedet. I stedet for indsættes standardværdien i feltet **Antal til montage**, som beregnes fra feltet **Lever antal** i henhold til en foruddefineret regel, der sikrer levering af montage til ordre-mængder først.  

 Hvis du vil afvige fra denne standard, for eksempel fordi du kun vil montere mere eller mindre af mængden i feltet **Lever (antal)**, kan du ændre feltet **Antal til montage**, men kun inden for foruddefinerede regler som illustreret nedenfor.  

 Som eksempel på, hvorfor det er klogt at ændre mængden, der skal monteres, er, at du vil bogføre leverancen af lagerbeholdninger delvist, inden montageoutput kan leveres.  

 Følgende tabel forklarer de regler, der definerer de minimale og maksimale værdier, du kan angive i feltet **Antal til montage**, for at afvige fra standardværdi i et kombinationsscenarie. Tabellen viser et kombinationsscenarie, hvor feltet **Lever (antal)** på den tilknyttede salgsordrelinje er ændret fra 7 til 4, og **Antal til montage** er derfor sat til standardværdien 4.  

|-|Salgsordrelinje|Montageordrehoved|  
|-|----------------------|---------------------------|  
||**Antal**|**Lever (antal)**|**Mgd. til montage til ordre**|**Leveret (antal)**|**Antal**|**Antal til montage**|**Monteret antal**|**Restantal**|  
|Oprettet|10|7|7|0|7|7|0|7|  
|Ændring||4||||4 (indsat som standard)|||  

 Baseret på ovennævnte situation kan du kun ændre feltet **Antal til montage** som følger:  

-   Det mindste antal du kan angive er 1. Dette skyldes, at du mindst skal montere én enhed for at kunne sælge fire enheder, idet de resterende tre antages at være tilgængelig på lageret.  
-   Det maksimale antal du kan angive er 4. Dette er for at sikre, at du ikke samler flere af denne montage til ordre-vare, end der er behov for i salget.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]