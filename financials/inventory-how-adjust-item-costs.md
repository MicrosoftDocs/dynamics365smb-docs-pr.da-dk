---
title: Regulere varepriser manuelt | Microsoft Docs
description: "Du kan regulere lagerværdien for en vare ved hjælp af FIFO eller gennemsnitlige kostmetoder, f.eks., når varepriser ændres af andre årsager end transaktioner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Fremgangsmåde: Regulere varepriser manuelt
Kostprisen for en vare (lagerværdi), du køber og senere sælger, kan ændres i varens levetid, fordi f.eks. en fragtomkostning føjes til købsprisen, når du har solgt varen. Omkostningsregulering er især relevant i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Hvis du altid vil kende den korrekte lagerværdi, skal varepriser regelmæssigt reguleres. Dette sikrer, at salgs- og indtjeningsstatistikkerne er opdateret, og at finansielle nøgletal er korrekte.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] reguleres varepriser automatisk, hver gang der forekommer en lagertransaktion, f.eks. når du bogfører en købsfaktura for en vare.

Du kan også bruge en funktion til at regulere omkostningerne for en eller flere varer manuelt. Dette er nyttigt, når du f.eks. ved, at varepriser er ændret af andre årsager end varetransaktioner.

Varepriser reguleres efter FIFO eller gennemsnitlig kostmetode, afhængigt af dit valg i den assisterede opsætning **Konfigurer min virksomhed**. Du kan finde flere oplysninger under [Blive klar til at handle](ui-get-ready-business.md).  

Hvis du bruger kostmetoden FIFO, er en vares kostpris er den faktiske værdi af alle modtagelser af varen. Lager vurderes ud fra den forudsætning, at de første varer, der lægges på lager, bliver solgt først.

Hvis du bruger kostmetoden Gennemsnit, beregnes en vares kostpris som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb. Lager værdiansættes ud fra den forudsætning, at alle lagerbeholdninger sælges samtidig.

Funktionen til regulering af kostpriser behandler kun de værdiposter, der endnu ikke er reguleret. Hvis der opstår en situation, hvor funktionen skal overføre ændrede indgående omkostninger til tilknyttede udgående poster, oprettes nye justeringsværdiposter, som er baseret på oplysningerne i de oprindelige værdiposter, men som indeholder justeringsbeløbet. Omkostningsreguleringsfunktionen bruger bogføringsdatoen for den oprindelige værdipost i justeringsposten, medmindre den dato er inden for en lukket lagerperiode. Hvis det er tilfældet, bruges startdatoen for den næste åbne lagerperiode. Hvis der ikke anvendes lagerperioder, er det datoen i feltet **Bogf. tilladt fra** i vinduet **Regnskabsopsætning**, der definerer, hvornår reguleringsposten bogføres.

Ændringer i lagerværdien fra handel afstemmes automatisk med dine finansielle regnskaber ved bogføring af varetransaktioner. Du kan finde flere oplysninger i afsnittet "Lagerafstemning" i [Lagerbeholdning](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Sådan reguleres varekostpriser manuelt
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Juster kostpris - vareposter**, og vælg derefter det relaterede link.
2. I vinduet **Reguler kostværdi - vareposter** skal du angive de varer, hvis omkostninger skal reguleres.
3. Vælg knappen **OK**.

## <a name="see-also"></a>Se også
[Lagerbeholdning](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

