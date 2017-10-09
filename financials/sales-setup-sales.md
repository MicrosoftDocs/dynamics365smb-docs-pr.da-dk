---
title: Oversigt over opgaver til konfiguration af salgsprocesser | Microsoft Docs
description: "Beskriver opgaver til oprettelse af regler og værdier, som du kan bruge til at definere virksomhedens salgspolitikker og -processer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a16201e48cc823e687c9941082d34044d9612a29
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-sales"></a>Konfigurere salg
Før du kan administrere salgsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens salgspolitikker.

Du skal definere den generelle opsætning, f.eks. hvilke salgsdokumenter der kræves, og hvordan dokumenternes værdier bogføres. Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.

En særskilt sæt opgaver i forbindelse med registrering af nye debitorer er at registrere en særlig pris eller rabataftaler, du indgår med hver debitorer.

Den finansrelaterede salgsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans. Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).

| Hvis du vil | Se |
| --- | --- |
| Opret et debitorkort for hver debitor, du sælger til. |[Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md) |
| Aktivere debitorer til at betale via PayPal, ved at vælge PayPal-logoet på salgsdokumenter. |[Fremgangsmåde: Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md) |
| Angive forskellige rabatter og specialpriser, som du yder kunderne, afhængigt af varen, antal og/eller dato. |[Fremgangsmåde: Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md) |
| Konfigurer sælgere, så du kan tildele dem til debitorkontakter eller måle sælgernes præstationer som grundlag for beregning af salgsprovision eller bonus. |[Fremgangsmåde: Konfigurere sælgere](sales-how-setup-salespeople.md) |
| Angiv for individuelle debitorer eller for alle kunder, hvordan salgsdokumenterne sendes som standard, når du vælger **Bogfør og send** handlingen. |[Fremgangsmåde: Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md) |
| Konfigurer din mail til at indeholde en oversigt over oplysningerne i det salgsdokument, der skal sendes. |[Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md). |
|Bruge en EU-webtjeneste til at kontrollere en kundes SE/CVR-nummer.|[Fremgangsmåde: Kontrollere SE/CVR-numre](sales-how-to-verify-vat-registration-numbers.md)|
|Angive oplysninger om de forskellige transportleverandører, virksomheden bruger, herunder et link til deres pakkesporingsservice.|[Sådan oprettes speditører](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

