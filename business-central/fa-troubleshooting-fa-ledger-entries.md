---
title: Fejlfinding af udvidelsen til Anlægsposter
description: Det er nemmere at arbejde med hele tal. Du kan bruge denne udvidelse til at afrunde beløb for anlæg i Anlægsposter.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'machinery, buildings'
ms.date: 10/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Fejlfinding af udvidelsen til Anlægsposter
Brug fejlfinding af udvidelse til Anlægsposter til at afrunde afskrivning og anskaffelsesbeløb i anlægsposterne til hele tal. Hvis du f. eks. vil afrunde et beløb på 30.000,44 til 30.000. Typiske årsager til afrundingsproblemer er dataoverflytning, pludselig start med at bogføre beløb i finans eller de tilpasninger, du har lavet i [!INCLUDE[prod_short](includes/prod_short.md)].

Udvidelsen til fejlfindingen af Anlægsposter er forudinstalleret og klar til brug. Hvis du fjerner filtypenavnet, men vil installere det igen, kan du finde det i AppSource.

## Foretage fejlfinding af anlægsposter
Når du åbner siden med **anlægs kortet** for første gang, planlægges **Scanning af Anlægsfinansposter**-opgavekøposter til at overvåge beløb hver søndag. Hvis der bliver fundet beløb, som du ønsker at afrunde, vises der en notifikation, næste gang du åbner siden for anlægskortet. Beskeden indeholder en **Vis mere**-indstilling, der åbner vinduet **Anlægsposter med afrundingsproblemer**, som indeholder en oversigt over poster med beløb, som du evt. vil afrunde. Hvis du vil afrunde beløbene, skal du vælge posterne og derefter vælge handlingen **Accepter udvælgelse**. Du kan bruge handlingen **Find poster med problemer** til at opdatere listen med nye problemer, der opstod, efter at opgavekøposten var aktiveret den foregående søndag.

## Se også
[Anlægsaktiver](fa-manage.md)  
[Administrere anlægsaktiver](fa-manage.md)  
[Vedligeholde anlægsaktiver](fa-how-maintain.md)  
[Tilpasse Business Central Online ved brug af udvidelser](ui-extensions.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



