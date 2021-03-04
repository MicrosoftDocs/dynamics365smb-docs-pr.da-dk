---
title: Tilføje ekstra linjer for at definere udvidede beskrivelser
description: Du kan tilføje ekstra linjer for at udvide standardteksten, der beskriver en vare, en finanskonto og andre data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e443a44135bbdaf75f6a064370983592797b10b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756913"
---
# <a name="add-extended-text"></a>Tilføje udvidet tekst

Du kan udvide beskrivelsen af varer, lagerenheder, finanskonti og ressourcer ved at tilføje ekstra linjer som udvidet tekst. Du kan også oprette betingelser for brugen af de ekstra linjer.  

I følgende afsnit beskrives, hvordan du føjer udvidet tekst til en beskrivelse af en vare. Men de samme trin gælder for lagerenheder, finanskonti og ressourcer.  

## <a name="to-define-extended-text-for-an-description"></a>Sådan defineres udvidet tekst for en beskrivelse

1. Åbn kortet for en vare, du vil føje udvidet tekst til, og vælg derefter handlingen **Udvidet tekst**.
2. Udfyld felterne **Kode** og **Beskrivelse**.
3. Vælg **Ny**.
4. Udfyld feltet **Sprogkode**, eller marker afkrydsningsfeltet **Alle sprogkoder**, hvis du bruger sprogkoder.
5. Udfyld felterne **Startdato** og **Slutdato**, hvis du vil begrænse den tid, hvor den udvidede tekst bruges.
6. Skriv den udvidede tekstkode i feltet **Tekst**.
7. Markér de relevante afkrydsningsfelter for de dokumenttyper, hvor den udvidede tekst skal udskrives.
8. Luk siden.

Du kan nu føje denne udvidede tekst til dokumenter. Følgende fremgangsmåde beskriver, hvordan du føjer udvidet tekst til en salgsordre, men samme fremgangsmåde gælder for alle andre dokumenter, du har angivet for den udvidede tekst.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Sådan tilføjes en udvidet varetekst på en salgsordrelinje

1. Åbn en salgsordre med en salgslinje for en vare, der har udvidet tekst defineret. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
2. Vælg den ønskede linje, og vælg derefter handlingen **Indsæt udv. tekster**.

## <a name="see-also"></a>Se også

[Opsætning af lagerbeholdning](inventory-setup-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]