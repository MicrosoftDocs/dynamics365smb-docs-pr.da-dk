---
title: "Fremgangsmåde: Oprette en farvet køindikator | Microsoft Docs"
description: "Få at vide, hvordan du bruger farvede køindikatorer i dit rollecenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3c5aff53c522729a95763485eb79d13c0f051831
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-a-colored-indicator-on-cues"></a>Fremgangsmåde: Oprette en farvet indikator på køindikatorer
Du kan oprette køindikatorer, der vises på siden **Start**, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne.

Indikatoren vises som en farvet streg langs den øverste kant af feltet Køindikator. Det indeholder et visuelt signal af status for køindikatorens aktivitet, som kan indikere favorable eller ikke-favorable betingelser for at bede brugeren om at handle. Hvis en køindikator f.eks. viser løbende salgsfakturaer, kan du oprette indikatoren som grøn (favorabel), når det samlede antal løbende salgsfakturaer er under 10, og rød (ikke-favorabel), når det samlede antal er større end 20.

Fra vinduet **Opsætning af køindikator** kan du konfigurere indikatorer for alle køindikatorer, der findes i regnskabsdatabasen.

Hvis du vil konfigurere indikatoren, kan du angive op til to tærskelværdier, der definerer tre områder af dataværdier (lav, mellem og høj), hvor du kan anvende en anden farve (eller type).

## <a name="to-set-up-colored-indicators-on-cues"></a>Sådan opretter farveindikatorer på køindikatorer
1. Under **Aktiviteter** på din **Startside** skal du vælge **Konfigurer køindikatorer**.  
   Vinduet **Opsætning af køindikator** vises. Vinduet viser de indikatorer, der aktuelt er konfigureret på køindikatorer.
2. Hvis du vil ændre en indikator skal du redigere felterne og ændre f.eks. værdierne for de forskellige intervalgrænser.  

Følgende tabel viser de farver, der svarer til indstillingerne for felterne **Typen Lavt interval**, **Typen Mellem interval** og **Typen Højt interval**.

| Indstilling | Farve |
| --- | --- |
| **Ingen** |Ingen farve (samme farve som feltet Køindikator |
| **Favorabel** |Grøn |
| **Ikke-favorabel** |Rød |
| **Tvetydig** |Gul |
| **Underordnet** |Grå |

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

