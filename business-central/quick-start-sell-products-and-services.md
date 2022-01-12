---
title: Salg, hurtig start (indeholder video)
description: Få mere at vide om, hvordan du udfylder de første kritiske felter om produkter og debitorer i Business central, så du kan begynde at salgsprocessen.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 9641d87dadc3b33683d1bab0bdc70d0b36b4d1ae
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940847"
---
# <a name="sales-quick-start"></a>Salg, Hurtig start

For at kunne købe produkter og tjenester skal du først oprette varer og debitorer. Når det er gjort, kan du begynde at registrere salgsordrer og sende fakturaer.

## <a name="set-up-items-to-sell"></a>Sådan oprettes varer til salg

Denne video viser, hvordan du opretter en vare, der skal sælges i [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Opret en ny vare

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Yderligere oplysninger og andre ting, du kan gøre, når du registrerer varer, finder du i [registrere nye varer](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Sådan oprettes debitorer

I denne video kan du se, hvordan du opretter en ny debitor i [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Opret en ny debitor

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Yderligere oplysninger og andre ting, du kan gøre, når du registrerer debitorer, finder du i [registrere nye debitorer](sales-how-register-new-customers.md)

## <a name="create-a-sales-order"></a>Oprette en salgsordre  

Når du sælger noget til en debitor, har du to muligheder. Den første og den enkleste er blot at oprette en salgsfaktura. Men hvis salgsprocessen er mere kompleks, f. eks. Hvis du har situationer, hvor du kun vil levere dele af ordreantallet, skal du bruge en salgsordre.

### <a name="to-create-a-sales-order"></a>Sådan oprettes en salgsordre  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 10.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en ny post.
3. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

    Andre felter på siden **Salgsordre** er nu udfyldt med standardoplysningerne for den valgte debitor.  

4. Udfylde de resterende felter efter behov på siden **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.

6. I feltet **Nummer** angive nummeret på en vare eller en service.

7. Angiv det antal varer, der skal sælges, i feltet **Antal**.

8. I feltet **Linjerabatpct.** kan du indtaste en procentdel, hvis du vil give debitoren en rabat på produktet.

9. Hvis du vil tilføje en kommentar om den ordrelinje, som debitoren kan se på det udskrevne ordrer, skal du skrive en kommentar i feltet **Beskrivelse** på en tom linje.

10. Gentag trin 5 til 9 for hver vare, du ønsker at sælge til debitoren.

11. Hvis du kun vil sende en del af ordreantallet, skal du angive dette antal i feltet **Lever antal**. Værdien kopieres til feltet **Fakturer antal**.

12. Hvis du kun vil fakturere en del af det leverede antal, skal du angive dette antal i feltet **Fakturer antal**. Antallet skal være mindre end værdien i feltet **Lever antal**.

13. Når salgsordrelinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.

Du kan finde flere oplysninger og yderligere ting, du kan gøre, når du opretter debitorsalgsordrer, i [salgsprodukter med en debitorsalgsordre](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Opret en salgsfaktura

Når du opretter og bogfører en salgsfaktura, opretter du ikke kun det fakturadokument, som du sender til debitoren. du kan også oprette de relaterede antal og værdiposter i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="to-create-and-post-a-sales-invoice"></a>Sådan oprettes og bogføres en salgsfaktura  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 20.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  

2. Vælg **Ny** for at oprette en ny post.

3. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

4. Udfylde de resterende felter efter behov på siden **Salgsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.

6. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

7. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.  

8. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

9. Gentag trin 5 til 8 for hvert produkt eller gebyr, du vil fakturere debitoren for.  

10. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

11. Når salgsfakturalinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.  

Du kan finde flere oplysninger og yderligere ting, du kan gøre, når du opretter debitorsalgsfakturaer, i afsnittet [fakturasalg](sales-how-invoice-sales.md)

## <a name="see-also"></a>Se også

[Hurtig start af Business Central](quick-start-business-central.md)  
[Salgsoversigt](sales-manage-sales.md)  
[Sælge produkter med en debitorsalgsordre](sales-how-sell-products.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
