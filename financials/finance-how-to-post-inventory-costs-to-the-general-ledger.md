---
title: "Sådan bogfører du kostpriser i finansregnskabet | Microsoft Docs"
description: "Bruges til at styre de fysiske produkter, som du handler med, f.eks. håndtering af lagerbeholdning på lagerstedet."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 07/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 4cd7eb78c803c8c1e13931f1184daaa3b4c51cdd
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Afstemme lagerværdier med finansregnskabet
Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet.

Automatisk lagerværdibogføring er defineret i feltet **Aut. lagerværdibogføring** i vinduet **Lageropsætning**.

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Du kan finde flere oplysninger i [Regulere varepriser](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Sådan bogføres lagerværdier manuelt
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogfør lagerregulering**, og vælg derefter det relaterede link.
2. Du kan bogføre lagerværdier i finansregnskabet ved at udføre kørslen. Når du udfører denne kørsel, oprettes finansposter ud fra værdiposterne. Du kan bogføre posterne, så de opsummeres pr. bogføringsgruppe.

> [!NOTE]  
> Når du udfører kørslen, kan du finde fejl, der relaterer til manglende opsætning eller inkompatibel opsætning af dimensioner. Hvis kørslen finder fejl i opsætningen af dimensioner, bliver disse fejl tilsidesat, og kørslen bruger dimensionerne for værdiposten. For alle andre typer fejl springer kørslen bogføring af værdiposter over, og anfører dem i slutningen af rapporten under overskriften “Poster, der er sprunget over”. Du skal rette fejlene, inden du kan bogføre posterne.

Hvis du vil se en liste over fejl før kørslen af bogføringen, kan du køre rapporten **Bogfør lageromkostning - kontrol**. Denne kontrolrapport viser alle de fejl, som fanges under en bogføringstest. Du kan derefter rette fejlene og udføre kørslen til bogføring af lagerreguleringer uden at springe nogen poster over.

Hvis du ganske enkelt vil have en oversigt over, hvilke værdier der kan bogføres i finansregnskabet uden at gennemføre bogføringen, kan du udføre kørslen **Bogfør lagerregulering** uden at bogføre værdierne i finansregnskabet. Dette kan du gøre ved at fjerne markeringen i feltet **Bogfør** på anmodningssiden. Når du derefter udfører kørslen, oprettes der kun en rapport, der viser de værdier, der er klar til at blive bogført i finansregnskabet, men de er ikke bogført.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Sådan reviderer du afstemningen mellem lagerposterne og finansposterne
Vinduet **Lagerbeholdning - afstemning** indeholder følgende:

- Vise afstemningsdifferencer ved at sammenligne det, der er registreret i finans, og det, der er registreret i lageropgørelsen (værdiposter).
- Vise ikke-afstemte kostbeløb i værdiposter i lageropgørelsen, som om de var koblet til tilsvarende lagerrelaterede konti i finans og sammenligne disse med de totaler, der faktisk registreres i de samme konti i finans.
- Afspejle dobbeltindtastningsstrukturen i finans ved visuelt at præsentere data som sådan. En vareforbrugsindtastning har f.eks. en tilsvarende lagerpost.
- Lade brugerne specificere og få vist de poster, der udgør kostbeløb.
- Inkludere filtre, der begrænser analysen efter dato, vare og lokation.
- Forklare årsager til afstemningsdifferencer i informative meddelelser.


Kolonnen **Navn** yderst til venstre i gitteret viser de forskellige finanskontotyper, der er tilknyttet lager.

Kolonnerne **Lager**, **Lager (mellemkonto)** og **Igangværende lager** viser de fakturerede og ikke-fakturerede totaler og totaler for igangværende arbejde for hver finanskontotype. Disse beregnes ud fra værdiposter, dvs. de projiceres over på de finanskontotyper, hvor de skal være, når de til sidste bogføres til finans.

Kolonnen **Total** viser summen (med fed tekst) af værdipostbeløbene i de tre lagerkolonner.

Kolonnen **Finanstotal** viser beløbene (med fed skrift) for hver finanskontotype, der findes i finans. Disse beregnes ud fra finansposter, dvs. de repræsenterer lagerreguleringer, der allerede er bogført til finans.

Kolonnen **Difference** repræsenterer forskellen mellem værdien i feltet **Finanstotal** og **Total**.

Øverst i vinduet **Lagerbeholdning - afstemning** kan du angive filtre for at begrænse, hvilke oplysninger der skal vises, f.eks. inden for en bestemt periode.

Hvis du vælger afkrydsningsfeltet **Vis advarsel**, og hvis der er uoverensstemmelser mellem lagertotaler og finanstotaler, vises meddelelser i feltet **Advarsel** for gitteret, som beskriver uoverensstemmelserne. Hvis du klikker på feltet Advarsel, får du yderligere oplysninger om, hvad advarslen betyder.

Vælg handlingen **Vis matrix**, når du har angivet alle relevante filtre. Dataene udregnes og matrix-vinduet vises.

I den venstre kolonne i gitteret vises forskellige finanskontotyper, som er tilknyttet lageret. Gitteret viser derefter totalerne for fakturerede, ufakturerede (foreløbige) og VIA-værdi for hver kontotype. Disse totaler beregnes ud fra værdiposterne.

De næste kolonner viser totalerne for de samme kontotyper beregnet ud fra finansposterne.

Vælg beløbet i en af totalerne for at se de poster i lagerrapporten, der blev brugt til at beregne totalerne. For lagertotalerne er posterne i lagerrapporten summen af værdiposterne for varerne. For finanstotalerne er posterne i lagerrapporten summen fra finansposterne.

## <a name="see-also"></a>Se også  
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

