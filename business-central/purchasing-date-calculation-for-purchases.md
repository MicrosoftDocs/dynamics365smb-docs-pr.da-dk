---
title: Beregning af forfaldsdato for køb
description: 'Denne artikel beskriver, hvordan du kan beregne dato for køb.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# <a name="calculate-dates-for-purchases"></a><a name="calculate-dates-for-purchases"></a>Beregning af forfaldsdato for køb

Hvis du vil have varer fra lageret på eb bestemt dato, kan [!INCLUDE[prod_short](includes/prod_short.md)] automatisk beregne den dato, hvor du skal bestille varen. 

Resultatet er den dato, hvor du kan plukke de bestilte varer.  

Hvis du angiver en ønsket modtagelsesdato på en købsordrelinje, er den beregnede Ordredato den dato, hvor du skal afgive ordren. Derefter beregnes den dato, hvor varerne er disponible til pluk, og datoen indsættes i feltet **Forventet modt.dato**.  

Hvis du ikke angiver en ønsket modtagelsesdato, baseres den dato, du forventer at modtage varerne, på ordredatoen på linjen. 

Modtagelsesdatoen er også den dato, hvor varerne er disponible til pluk.  

> [!TIP]
> Som standard er mange af de datofelter, som denne artikel nævner, skjult på indkøbsordrelinjer. Hvis et felt ikke er tilgængeligt, kan du tilføje det ved at tilpasse siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a><a name="calculating-with-a-requested-receipt-date"></a>Beregning med en ønsket modtagelsesdato

Hvis der står en ønsket modtagelsesdato på købslinjen, bruges denne dato som udgangspunkt for følgende beregninger.  

- Ønsket modtagelsesdato - Leveringstidsberegning = Ordredato  
- Ønsket modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du angiver en ønsket modtagelsesdato på en købsordrelinje, tildeles denne dato til nye linjer, når du opretter dem. Du kan ændre eller fjerne datoen på linjerne efter behov.  

> [!NOTE]
> Hvis processen er baseret på bagudrettet beregning, f.eks. hvis du bruger den ønskede modtagelsesdato til at hente ordredatoen, anbefales det, at du bruger datoformler med faste varigheder, f.eks. "5D" for fem dage eller "1U" for én uge. Datoformler uden faste varigheder, f.eks. "AU" for aktuelle uge eller AM for den aktuelle måned, kan resultere i forkerte datoberegninger. Du kan finde flere oplysninger om datoformler i [Arbejde med kalenderdatoer og-klokkeslæt](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date"></a><a name="calculating-without-a-requested-receipt-date"></a>Beregne uden en ønsket modtagelsesdato

Hvis du angiver en købslinje uden en ønsket modtagelsesdato, udfyldes feltet **Ordredato** automatisk med datoen fra feltet **Ordredato** på købshovedet. Denne dato kan enten være en indtastet dato eller arbejdsdatoen. Med ordredatoen som udgangspunkt beregnes datoer derefter automatisk til købsordrelinjen, som følger:  

- Ordre dato + Leveringstidsberegning = Planlagt modtagelsesdato  
- Planlagt modtagelsesdato + Indgående lagerekspeditionstid + Sikkerhedstid = Forventet modtagelsesdato  

Hvis du ændrer ordredatoen på linjen, genberegner [!INCLUDE[prod_short](includes/prod_short.md)] de andre datoer.  

## <a name="default-values-for-lead-time-calculation"></a><a name="default-values-for-lead-time-calculation"></a>Standardværdier for beregning af leveringstid

[!INCLUDE[prod_short](includes/prod_short.md)] bruger datoformularen i feltet **Leveringstid** på købsordrelinjen til at beregne ordren og de forventede modtagelsesdatoer.  

Du kan angive datoformlen manuelt på linjerne. Ellers bruger [!INCLUDE[prod_short](includes/prod_short.md)] de formler, der er defineret på følgende sider i denne prioriteringsrækkefølge:

1. Vare/leverandører
2. Varekort
3. Lagervarekort
4. Leverandørkort (Kreditor)

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Beregning af forfaldsdato for salg](sales-date-calculation-for-sales.md)  
[Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
