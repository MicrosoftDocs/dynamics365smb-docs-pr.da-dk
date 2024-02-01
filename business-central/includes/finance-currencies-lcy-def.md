---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Da virksomheder handler i flere lande/områder, bliver det mere vigtigt, at de kan gennemgå eller rapportere finansielle oplysninger i mere end én valuta. Den lokale valuta (RV) er defineret på siden **Opsætning af Finans**, som beskrevet i artiklen [Om Finansmodulet og kontoplanen](../finance-general-ledger.md). Når den lokale valuta (RV) er blevet defineret, vises den som en tom valuta, så hvis feltet **Valuta** er tomt, betyder det, at valutaen er RV.  

Derefter skal du oprette valutakoder for hver valuta, du bruger, hvis du køber eller sælger i andre valutaer end den lokale valuta (RV). Du kan også oprette bankkonti ved hjælp af valutaer. Det er muligt at bogføre finanstransaktioner i forskellige valutaer, men finanstransaktionen bogføres altid i lokal valuta (RV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Ved at angive en anden valuta som en såkaldt ekstra rapporteringsvaluta vil [!INCLUDE[prod_short](prod_short.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](../finance-how-setup-additional-currencies.md). Den ekstra rapporteringsvaluta bruges ofte til at lette finansiel rapportering til ejere, som er placeret i lande/områder, som bruger forskellige valutaer end den lokale valuta (RV).  

> [!IMPORTANT]
> Hvis du vil bruge en ekstra rapporteringsvaluta til finansiel rapportering, skal du have kendskab til begrænsningerne. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Når du bogfører på finanskonto ved hjælp af en valutakode, f. eks. Hvis du vil bogføre en udgift i en finanskladde ved hjælp af en valutakode, omregnes transaktionen til RV ved hjælp af valutakursen for bogføringsdatoen. Finansposten vil ikke indeholde oplysninger om den valuta, der er brugt, kun værdien i RV. Hvis du vil holde styr på den oprindelige valuta, f. eks. til en faktura, skal du bruge både salgs-og købsdokumenter og bankkonti, der gemmer valutakode oplysninger for posterne.
