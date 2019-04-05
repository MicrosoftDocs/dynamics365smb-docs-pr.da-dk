---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 743cf7ecbed4157dc9283a97baa956e69ec0c6b5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792984"
---
# <a name="define-check-layouts"></a>Definere checklayout
Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder. Checkbilleder kan udskrives på engelsk, fransk eller spansk.

Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.

## <a name="to-define-check-layouts"></a>Sådan defineres checklayout
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.
2. På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.
3. Vælg et af følgende rapport-id'er.

| Rapport-id | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Check |Dette er standardrapporten. |
| 10401 |Check (følgebrev/følgebrev/check) |Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format. |
| 10411 |Check (følgebrev/check/følgebrev) |Denne rapport er designet til at udskrive check i et check/følgebrev/check-format. |

Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**. Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fuldførelse af periodeafslutningsprocesser](year-how-complete-period-end-processes.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)
