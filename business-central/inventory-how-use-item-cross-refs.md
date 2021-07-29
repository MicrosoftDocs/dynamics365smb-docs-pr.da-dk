---
title: Bruge varereferencer
description: Konfigurer referencer mellem de beskrivelser, som du og leverandøren bruger til en vare, så du kan indsætte leverandørens varebeskrivelse på købsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 853c574f5b262f7b826bc92dd8e35484e902c1f4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444941"
---
# <a name="use-item-cross-references"></a>Bruge varereferencer
Hvis du har oprettet en reference mellem varebeskrivelsen, du bruger til en vare, og den beskrivelse, som leverandøren af den pågældende vare bruger, indsættes leverandørens varebeskrivelse automatisk i købsdokumenter for leverandøren, når du udfylder feltet **Varereferencenr.** . De samme funktioner gælder for debitorvarenumre i salgsdokumenter.

Følgende procedurer beskriver, hvordan du kan bruge varereferencer på købssiden. Fremgangsmåden er den samme på salgssiden.

> [!NOTE]
> Det bliver mere almindeligt for vare-id'er, f.eks. GTIN eller GUID, der indeholder 30 eller flere tegn, hvilket er mere end den aktuelle funktion for varereferencer, der kan håndtere. Hvis du skal bruge referencer, der indeholder mere end 30 tegn, kan administratoren aktivere funktionen **Skriv længere varereferencer** på siden [Funktionsstyring](https://businesscentral.dynamics.com/?page=2610) (linket kræver, at du har en [!INCLUDE[prod_short](includes/prod_short.md)]-lejer). Hvordan du bruger referencer, ændres ikke, men navnene på ting som f.eks. sider og knapper ændres. F.eks. bliver siden **Varens krydshenvisningsposter** til **Varereferenceposter**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Sådan oprettes en varereference til en kreditors varebeskrivelse

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, som du vil oprette en reference for til den varebeskrivelse, som leverandøren bruger til den pågældende vare.
3. Vælg handlingen **Varereferencer**.

     Hvis du ikke kan finde handlingen **Varereferencer**, skal du vælge at få vist flere indstillinger og derefter finde den under **Relateret** > **Vare**.
  
4. På en ny linje på siden **Varereferenceposter** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Sådan angiver du en kreditors varebeskrivelse på en købsordre

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **købsordrer**, og vælg derefter det relaterede link.
2. Opret en købsordre for den leverandør, som du angav en varereference for ovenfor.
3. Opret en købslinje for den vare, som du angav en varereference for ovenfor.
4. I feltet **Varereferencenr.** skal du vælge den varereference, du har oprettet, og derefter vælge knappen **OK**.

Feltet **Beskrivelse** på linjen overskrives med kreditorens varebeskrivelse, som blev oprettet i varereferenceposten.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]