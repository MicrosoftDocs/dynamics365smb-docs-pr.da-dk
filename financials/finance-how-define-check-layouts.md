---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-define-check-layouts"></a>Fremgangsmåde: Definere checklayout
Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder. Checkbilleder kan udskrives på engelsk, fransk eller spansk.

Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.

## <a name="to-define-check-layouts"></a>Sådan defineres checklayout
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.
2. I vinduet **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.
3. Vælg et af følgende rapport-id'er.

| Rapport-id | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Check |Dette er standardrapporten. |
| 10401 |Check (følgebrev/følgebrev/check) |Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format. |
| 10411 |Check (følgebrev/check/følgebrev) |Denne rapport er designet til at udskrive check i et check/følgebrev/check-format. |

Når du har oprettet checklayout, kan du udskrive check i vinduet **Udbetalingskladde**. Du kan finde flere oplysninger i [Fremgangsmåde: Arbejde med checks](payables-how-work-checks.md).

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fuldførelse af periodeafslutningsprocesser](year-how-complete-period-end-processes.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

