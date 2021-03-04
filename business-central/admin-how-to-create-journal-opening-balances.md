---
title: Sådan oprettes kladden Primosaldi | Microsoft Docs
description: Business Central indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data med posteringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8ffb5b8b90d0fdd4f3e1bd90271db8568c05d41e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753963"
---
# <a name="create-journal-opening-balances"></a>Oprette kladden Primosaldi

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data til debitorkladden, kreditorkladden, varekladden og finanskladden.

Det første trin er at oprette en konfigurationspakke, der omfatter konfigurationstabellerne for disse kladder. I følgende procedure antages det, at dette trin er udført. Du kan finde flere oplysninger i [Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md). Proceduren beskriver de efterfølgende trin, som omfatter anvendelse af den pakke, der leveres af en partner.  

Før du starter, skal du kontrollere, at du du bruger rollecentersiden Administration, fordi den indeholder den korrekte kontekst til dit konfigurationsarbejde. Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Udligne posterne i en kladde til en ny virksomhed

1. Konfigurer en ny virksomhed, og anvend en konfigurationspakke på den. Du kan finde flere oplysninger i [Konfigurere en virksomhed med guiden RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Den nye virksomhed indeholder ikke oplysninger om kladdeprimosaldi.  

2. Åbn konfigurationsregnearket, og importér eksisterende data om debitorer, varer, kreditorer og regnskabet. Du kan finde flere oplysninger i [Overflytte debitordata](admin-migrate-customer-data.md).  

    Nu er stamdataene på plads. Derefter skal du tilføje primosaldi. Følgende fremgangsmåde beskriver, hvordan du opretter kladdelinjer til finanskonti, men gælder også for oprettelse af kladdelinjer til debitorer, kreditorer og varer.  
3. Vælg handlingen **Opret kladdelinjer for finanskonto**.  
4. Udfyld oversigtspanelet **Indstillinger**, og angiv filtre efter behov. Skriv f.eks. et navn i feltet **Kladdetype**.  
5. Vælg knappen **OK**. Posterne er nu i kladden, men beløbene er tomme.  
6. Eksportér kladdetabellen til Excel, og angiv manuelt bogførings- og modkontooplysninger fra ældre data.
7. Importér og anvend tabeloplysningerne i den nye virksomhed. Kladdelinjerne er klar til bogføring.  
8. I konfigurationsregnearket skal du vælge kladdelinjetabellen og derefter vælge handlingen **Databasedata**.  
9. Gennemgå oplysningerne, og vælg derefter handlingen **Bogfør**.  
10. Gentag trinene for at importere og bogføre eventuelle andre primosaldi.  

> [!TIP]
> Du kan bruge de samme kørsler til at tilføje primosaldi, hver gang du registrerer en ny debitor eller kreditor, som du har handlet med, men som ikke er registreret i [!INCLUDE [prod_short](includes/prod_short.md)]. Du skal blot søge efter den relevante opgave og derefter vælge det relevante link.

## <a name="see-also"></a>Se også

[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]