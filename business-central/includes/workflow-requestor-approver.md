---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Når du konfigurerer brugere til godkendelsesworkflow, er det vigtigt, at den samme bruger ikke både er anmoder og godkender i en brugergruppe for workflowet. Når en bruger både er anmoder og godkender, fungerer godkendelse på følgende måde:

* Deres anmodninger godkendes altid automatisk.
* Hvis der er flere godkendere, er det kun godkenderne med et højere sekvensnummer i brugergruppen for workflowet, der kan ændre status for en anmodning til godkendt. Godkendere med et lavere sekvensnummer kan godkende anmodninger, men deres godkendelser påvirker ikke statussen for en anmodning.