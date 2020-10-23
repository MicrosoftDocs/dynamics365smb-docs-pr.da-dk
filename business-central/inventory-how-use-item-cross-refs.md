---
title: Bruge varereferencer | Microsoft Docs
description: Konfigurer referencer mellem de beskrivelser, som du og leverandøren bruger til en vare, så du kan indsætte leverandørens varebeskrivelse på købsdokumenter.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 056897c799dd12755432637690446a0797c9f18c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919434"
---
# <a name="use-item-cross-references"></a>Bruge varereferencer
Hvis du har oprettet en reference mellem varebeskrivelsen, du bruger til en vare, og den beskrivelse, som leverandøren af den pågældende vare bruger, indsættes leverandørens varebeskrivelse automatisk i købsdokumenter for leverandøren, når du udfylder feltet **Varereferencenr.** . De samme funktioner gælder for debitorvarenumre i salgsdokumenter.

Følgende procedurer beskriver, hvordan du kan bruge varereferencer på købssiden. Fremgangsmåden er den samme på salgssiden.

> [!NOTE]
> Det bliver mere almindeligt for vare-id'er, f. eks. GTIN eller GUID, der indeholder 30 eller flere tegn, hvilket er mere end den aktuelle funktion for varereferencer, der kan håndtere. Hvis du skal bruge referencer, der indeholder mere end 30 tegn, kan administratoren aktivere funktionen **Skriv længere varereferencer** på siden [Funktionsadministration ](https://businesscentral.dynamics.com/?page=xzy) (linket kræver, at du har en [!INCLUDE[d365fin](includes/d365fin_md.md)]-lejer). Hvordan du bruger referencer, ændres ikke, men navnene på ting som f. eks. sider og knapper ændres. F.eks. bliver siden **Varens krydshenvisningsposter** til **Varereferenceposter**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Sådan oprettes en varereference til en kreditors varebeskrivelse

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for den vare, som du vil oprette en reference for til den varebeskrivelse, som leverandøren bruger til den pågældende vare.
3. Vælg handlingen **Varereferencer**.

     Hvis du ikke kan finde handlingen **Varereferencer**, skal du vælge at få vist flere indstillinger og derefter finde den under **Relateret** > **Vare**.
  
4. På en ny linje på siden **Varereferenceposter** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Sådan angiver du en kreditors varebeskrivelse på en købsordre

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.
2. Opret en købsordre for den leverandør, som du angav en varereference for ovenfor.
3. Opret en købslinje for den vare, som du angav en varereference for ovenfor.
4. I feltet **Varereferencenr.** skal du vælge den varereference, du har oprettet, og derefter vælge knappen **OK**.

Feltet **Beskrivelse** på linjen overskrives med kreditorens varebeskrivelse, som blev oprettet i varereferenceposten.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
