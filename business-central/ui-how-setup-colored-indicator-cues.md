---
title: Tilpasse visuelle signaler om en køindikators aktivitet | Microsoft Docs
description: Du kan oprette et farvet symbol i et Køindikator-felt for at levere et tilpasset visuelt signal om køindikatorens aktivitet.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "923434"
---
# <a name="set-up-a-colored-indicator-on-cues"></a>Oprette en farvet indikator på køindikatorer
Du kan oprette køindikatorer, der vises i rollecenteret, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne.

Indikatoren vises som en farvet streg langs den øverste kant af feltet Køindikator. Det indeholder et visuelt signal af status for køindikatorens aktivitet, som kan indikere favorable eller ikke-favorable betingelser for at bede brugeren om at handle. Hvis en køindikator f.eks. viser løbende salgsfakturaer, kan du oprette indikatoren som grøn (favorabel), når det samlede antal løbende salgsfakturaer er under 10, og rød (ikke-favorabel), når det samlede antal er større end 20.

Fra siden **Opsætning af køindikator** kan du konfigurere indikatorer for alle køindikatorer, der findes i regnskabsdatabasen.

Hvis du vil konfigurere indikatoren, kan du angive op til to tærskelværdier, der definerer tre områder af dataværdier (lav, mellem og høj), hvor du kan anvende en anden farve (eller type).

## <a name="to-set-up-colored-indicators-on-cues"></a>Sådan opretter farveindikatorer på køindikatorer
1. Under **Aktiviteter** i dit Rollecenter skal du vælge **Konfigurer køindikatorer**.  
   Siden **Opsætning af køindikator** vises. Siden viser de indikatorer, der aktuelt er konfigureret på køindikatorer.
2. Hvis du vil ændre en indikator skal du redigere felterne og ændre f.eks. værdierne for de forskellige intervalgrænser.  

Følgende tabel viser de farver, der svarer til indstillingerne for felterne **Typen Lavt interval**, **Typen Mellem interval** og **Typen Højt interval**.

| Indstilling | Farve |
| --- | --- |
| **Ingen** |Ingen farve (samme farve som feltet Køindikator)|
| **Favorabel** |Grøn |
| **Ikke-favorabel** |Rød |
| **Tvetydig** |Gul |
| **Underordnet** |Grå |

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
