---
title: Overføre varer mellem lagerlokationer
description: Beskriver, hvordan du flytter lager fra ét sted eller lagersted til et andet enten med omposteringskladden eller overflytningsordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 166ac80202717ff3418b040ad01bccb1eb97ac66
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059382"
---
# <a name="transfer-inventory-between-locations"></a>Overflytte lagerbeholdning mellem lokationer
Du kan overføre lagervarer mellem lokationer ved at oprette overflytningsordrer. Du kan også bruge vareomposteringskladden.

Med overflytningsordrer leverer du den udgående overflytning fra én placering og modtager den indgående overflytning på en anden. Dette giver dig mulighed for at administrere de involverede lageraktiviteter og giver større sikkerhed for, at lagerantallet opdateres korrekt.

Med omposteringskladden skal du blot udfylde felterne **Lokationskode** og **Ny lokationskode**. Når du bogfører kladden, justeres vareposterne på de pågældende lokationer. Med denne metode administreres lageraktiviteter ikke.

> [!NOTE]  
>   Hvis du har varer, der er registreret i lagerbeholdningen uden en lokationskode, f.eks. fra et tidspunkt, hvor du kun havde ét lagersted, kan du ikke overføre disse varer ved hjælp af overflytningsordrer. I stedet skal du bruge omposteringskladden til at ompostere varerne fra en tom lokationskode til en faktisk lokationskode.  Du kan finde flere oplysninger i trin 3 i [Sådan overflyttes varer i vareomposteringskladden](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Hvis du vil overflytte varer, skal lokationer og overflytningsruter oprettes. Der er flere oplysninger i [Opsætte lokationer](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Såden overflyttes varer med en overflytningsordre
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **overflytningsordrer**, og vælg derefter det relaterede link.
2. På siden **Overflytningsordre** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hvis du har udfyldt felterne **Transitkode**, **Speditørkode** og **Speditørservice** på siden **Overflytningsrutespec.**, udfyldes de tilsvarende felter på overflytningsordren automatisk, når du opretter overflytningsruten.

    Når du udfylder feltet **Speditørservice** beregnes modtagelsesdatoen på den lokation, der overflyttes til, ved at lægge speditørens transporttid til afsendelsesdatoen.

3. Du udfylder linjerne ved enten at angive dem manuelt eller ved at vælge en af følgende indstillinger under handlingen **Funktioner**:
    - Vælg handlingen **Hent placeringsindhold** for at vælge eksisterende varer fra en bestemt placering på lokationen.
    - Vælg **Hent købsleverancelinjer** for at vælge varer, der lige er ankommet på den lokation, der overflyttes fra.   

    Fortsæt med at levere varerne som lagermedarbejder på den lokation, der overflyttes fra.
4. Vælg handlingen **Bogfør**, vælg indstillingen **Lever**, og vælg derefter knappen **OK**.

    Varerne er nu i transit mellem de angivne lokationer i overensstemmelse med den angivne overflytningsrute.

    Fortsæt ved at modtage varerne som lagermedarbejder på den lokation, der overflyttes fra. Overflytningsordrelinjerne er de samme som ved levering og kan ikke redigeres.
5. Vælg handlingen **Bogfør**, vælg indstillingen **Modtag**, og vælg derefter knappen **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Sådan overflyttes varer i vareomposteringskladden
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladder**, og vælg derefter det relaterede link.
2. På siden **Vareomposteringskladder** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **Lokationskode** skal du indtaste den lokation, hvor varerne opbevares i øjeblikket.

    > [!NOTE]  
    >   For at overflytte varer, der ikke har en lokationskode, skal du lade feltet **Lokationskode** stå tomt.
4. I feltet **Ny lokationskode** skal du angive den lokation, som du vil overflytte varerne til.
5. Vælg handlingen **Bogfør**.

## <a name="see-also"></a>Se også
[Administrere lager](inventory-manage-inventory.md)  
[Opsætte lokationer](inventory-how-setup-locations.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]