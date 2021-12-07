---
title: Fejlfinding af udvidelsen til Anlægsposter
description: Det er nemmere at arbejde med hele tal. Du kan bruge denne udvidelse til at afrunde beløb for anlæg i Anlægsposter.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 39bfc61cf928b6556a3c54625c8b6f9221553c93
ms.sourcegitcommit: a6000804ad9a176de5750372d3951547ddb71006
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2021
ms.locfileid: "7865569"
---
# <a name="the-troubleshooting-fa-ledger-entries-extension"></a>Fejlfinding af udvidelsen til Anlægsposter
Brug fejlfinding af udvidelse til Anlægsposter til at afrunde afskrivning og anskaffelsesbeløb i anlægsposterne til hele tal. Hvis du f. eks. vil afrunde et beløb på 30.000,44 til 30.000. Typiske årsager til afrundingsproblemer er dataoverflytning, pludselig start med at bogføre beløb i finans eller de tilpasninger, du har lavet i [!INCLUDE[prod_short](includes/prod_short.md)].

Udvidelsen til fejlfindingen af Anlægsposter er forudinstalleret og klar til brug. Hvis du fjerner filtypenavnet, men vil installere det igen, kan du finde det i AppSource.

## <a name="troubleshooting-fixed-asset-ledger-entries"></a>Foretage fejlfinding af anlægsposter
Når du åbner siden med **anlægs kortet** for første gang, planlægges **Scanning af Anlægsfinansposter**-opgavekøposter til at overvåge beløb hver søndag. Hvis der bliver fundet beløb, som du ønsker at afrunde, vises der en notifikation, næste gang du åbner siden for anlægskortet. Beskeden indeholder en **Vis mere**-indstilling, der åbner vinduet **Anlægsposter med afrundingsproblemer**, som indeholder en oversigt over poster med beløb, som du evt. vil afrunde. Hvis du vil afrunde beløbene, skal du vælge posterne og derefter vælge handlingen **Accepter udvælgelse**. Du kan bruge handlingen **Find poster med problemer** til at opdatere listen med nye problemer, der opstod, efter at opgavekøposten var aktiveret den foregående søndag.

## <a name="see-also"></a>Se også
[Anlægsaktiver](fa-manage.md)  
[Administrere anlægsaktiver](fa-manage.md)  
[Vedligeholde anlægsaktiver](fa-how-maintain.md)  
[Tilpasse Business Central Online ved brug af udvidelser](ui-extensions.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]


