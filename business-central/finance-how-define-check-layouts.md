---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/24/2019
ms.author: edupont
ms.openlocfilehash: 6ba5b6f0f91e207ec8ffedf5b45003a5787b9e0f
ms.sourcegitcommit: 0854c074b500c3031eaf86fde9d452f93f238081
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701125"
---
# <a name="select-a-check-layout"></a>Vælge et checklayout
Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder. Checkbilleder kan udskrives på engelsk, fransk eller spansk.

Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.

## <a name="to-select-a-check-layout"></a>Sådan vælges et checklayout
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.
2. På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.
3. Vælg et af følgende rapport-id'er.

| Rapport-id | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Check |Dette er standardrapporten. |
| 10411 |Check (følgebrev/følgebrev/check) |Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format. |
| 10412 |Check (følgebrev/check/følgebrev) |Denne rapport er designet til at udskrive check i et følgebrev/check/følgebrev-format. |
| 10413 |Tre checks pr. side |Denne rapport er udviklet til at udskrive tre checks på hver side. |

Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**. Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).

Hvis du vil ændre et af disse standardchecklayout, skal du bruge enten Word eller RDLC-integration til at gøre det. Du kan finde flere oplysninger under [Oprette og ændre et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Oprette og ændre et brugerdefineret rapport- eller dokumentlayout](ui-how-create-custom-report-layout.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fuldførelse af periodeafslutningsprocesser](year-how-complete-period-end-processes.md)  
[Arbejde med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)
