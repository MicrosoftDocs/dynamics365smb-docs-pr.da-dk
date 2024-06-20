---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Hvis din virksomhed opererer i mere end ét land eller område, er det sandsynligvis vigtigt, at du kan gøre forretninger i mere end én valuta. Du definerer din lokale valuta (RV) på siden **Opsætning af Finans**. Derefter vil din lokale valuta blive repræsenteret som en tom valuta på dokumenter og transaktioner. Når feltet **Valuta** er tomt, er valutaen RV.

Følgende video forklarer, hvordan du konfigurerer din lokale valuta.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Derefter skal du oprette valutakoder for hver valuta, du bruger, hvis du køber eller sælger i andre valutaer end den lokale valuta (RV). Du kan også oprette bankkonti ved hjælp af valutaer. Det er muligt at bogføre finanstransaktioner i forskellige valutaer, men finanstransaktionen bogføres altid i lokal valuta (RV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Ved at angive en anden valuta som en ekstra rapporteringsvaluta registrerer [!INCLUDE[prod_short](prod_short.md)] automatisk beløb i både RV og i den ekstra ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](../finance-how-setup-additional-currencies.md). Den ekstra rapporteringsvaluta bruges ofte til at lette finansiel rapportering til ejere, som er placeret i lande/områder, som bruger forskellige valutaer end den lokale valuta (RV).  

> [!IMPORTANT]
> Hvis du vil bruge en ekstra rapporteringsvaluta til finansiel rapportering, skal du have kendskab til begrænsningerne. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Når du bogfører i finansbogholderiet med brug af en udenlandsk valuta, konverterer [!INCLUDE [prod_short](prod_short.md)] transaktionen til RV vha. valutakursen på bogføringsdatoen. Finansposten vil ikke indeholde oplysninger om den valuta, der er brugt, kun værdien i RV. Hvis du vil holde styr på den oprindelige valuta, skal du bruge både salgs-og købsdokumenter og bankkonti, der gemmer valutakode oplysninger for posterne.
