---
title: Oversigt over opgaver til konfiguration af salgsprocesser
description: Oversigt over de opgaver, der er nødvendige for at konfigurere regler og værdier, der definerer din salgs politik og-processer, herunder generel opsætning og opsætning af finansrelaterede salg.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.search.form: 170, 172, 300, 301, 428, 459, 1401
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 7ec2741e9ff0a5c8ccd00fb8df31cda0a5bfcec6
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752303"
---
# <a name="setting-up-sales"></a>Konfigurere salg
Før du kan administrere salgsprocesser, skal du konfigurere de regler og værdier, der definerer virksomhedens salgspolitikker.

Du skal definere den generelle opsætning på **Salgsopsætning**, f.eks. hvilke salgsdokumenter der kræves, hvordan deres værdi angives og den type af linjer, der skal oprettes som standard. Denne generelle opsætning udføres typisk én gang i forbindelse med den indledende implementering.

En særskilt sæt opgaver i forbindelse med registrering af nye debitorer er at registrere en særlig pris eller rabataftaler, du indgår med hver debitorer. Du kan finde flere oplysninger i [Registrere specielle salgspriser og rabatter](sales-how-record-sales-price-discount-payment-agreements.md).

Den finansrelaterede salgsopsætning, som betalingsmetoder og valutaer, dækkes i afsnittet Konfigurere Finans. Der er flere oplysninger i [Konfigurere Finans](finance-setup-finance.md).

| Hvis du vil | Se |
| --- | --- |
| Opret et debitorkort for hver debitor, du sælger til. |[Registrere nye debitorer](sales-how-register-new-customers.md) |
| Aktivere debitorer til at betale via PayPal, ved at vælge PayPal-logoet på salgsdokumenter. |[Aktivere debitorbetaling via PayPal](sales-how-enable-payment-service-extensions.md) |
| Angive forskellige rabatter og specialpriser, som du yder kunderne, afhængigt af varen, antal og/eller dato. |[Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md) |
| Konfigurer sælgere, så du kan tildele dem til debitorkontakter eller måle sælgernes præstationer som grundlag for beregning af salgsprovision eller bonus. |[Konfigurere sælgere](sales-how-setup-salespeople.md) |
| Angiv for individuelle debitorer eller for alle kunder, hvordan salgsdokumenterne sendes som standard, når du vælger **Bogfør og send** handlingen. |[Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md) |
| Konfigurer din mail til at indeholde en oversigt over oplysningerne i det salgsdokument, der skal sendes. |[Sende dokumenter som mail](ui-how-send-documents-email.md) |
|Bruge en EU-webtjeneste til at kontrollere en kundes SE/CVR-nummer.|[Kontrollere SE/CVR-numre](finance-setup-vat.md)|
|Definere de forskellige incoterms, du tilbyder kunderne, eller som dine leverandører tilbyder dig.|[Oprette leveringsformer](sales-how-set-up-shipment-methods.md)|
|Angive oplysninger om de forskellige transportleverandører, virksomheden bruger, herunder et link til deres pakkesporingsservice.|[Oprette speditører](sales-how-to-set-up-shipping-agents.md)|
|Angiv standardrapporter, der skal bruges til forskellige dokumenttyper.|[Rapportvalg i Business Central](across-report-selections.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]