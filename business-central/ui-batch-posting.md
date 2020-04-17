---
title: Sådan bogføres flere dokumenter på én gang | Microsoft Docs
description: I stedet for at bogføre individuelle dokumenter ét ad gangen, kan du vælge flere ikke-bogførte dokumenter i en oversigt til baggrundsbogføring, enten med det samme eller planlagt til f.eks. dagens slutning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 32998248de254facdb225d60a0c8b55066b2707c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192095"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bogføre flere dokumenter på én gang
I stedet for at bogføre individuelle dokumenter ét ad gangen, kan du vælge flere ikke-bogførte dokumenter i en oversigt til bogføring med det samme eller til baggrundsbogføring i henhold til en plan, f.eks. ved dagens slutning. Dette kan være nyttigt, hvis det kun er en supervisor, der kan bogføre dokumenter, der er oprettet af andre brugere, eller for at undgå, at der opstår problemer med systemydeevnen under bogføring i arbejdstiden.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Sådan bogføres flere købsordrer med det samme
Følgende procedure beskriver, hvordan flere købsordrer kan bogføres med det samme. Trinene er de samme for alle købs- og salgsdokumenter.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.
2. Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:
3. I feltet **Nummer** skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.
4. Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.
5. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Bogfør**.
6. Vælg knappen **Ja** i bekræftelsesmeddelelsen.

## <a name="to-batch-post-multiple-purchase-orders"></a>Sådan massebogføres flere købsordrer
Følgende procedure beskriver, hvordan du kan massebogføre flere købsordrer. Fremgangsmåden er den samme for alle købs- og salgsdokumenter, hvor handlingen **Massebogfør** er tilgængelig.

> [!NOTE]
> Massebogføring af dokumenter sker i baggrunden, sådan som det er defineret af en opgavekøpost, som først skal konfigureres. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsordre**, og vælg derefter det relaterede link.  
2. Fortsæt med at vælge alle de ordrer, der skal bogføres, på siden **Købsordrer**:
3. I feltet **Nummer** skal du vælge de tre lodrette prikker for at åbne genvejsmenuen og derefter vælge handlingen **Markér flere**.
4. Marker afkrydsningsfeltet for alle de linjer, der repræsenterer ordrer, som du vil bogføre på samme tid.
5. Vælg handlingen **Bogføring**, og vælg derefter handlingen **Massebogfør**.
6. Udfyld felterne efter behov på siden **Massebogfør købsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Hvis du vil udskrive rapporter under bogføringen, f.eks. rapporten **Ordrebekræftelse** for salgsordrer, skal du markere afkrydsningsfeltet **Udskriv**.<br /><br /> I feltet **Rapportresultattype** på siden **Salgsopsætning** eller siden **Købsopsætning** skal du definere, om rapporten skal udskrives eller oprettes som en PDF-fil.<br /><br /> Bemærk også, at direkte udskrivning til en valgt printer kun er mulig i lokale installationer.

7. Vælg knappen **OK**.
8. Hvis du vil have vist potentielle problemer, der er opstået under massebogføring af dokumenter, skal du åbne siden **Registrer over fejlmeddelelser**.

Købsordrerne føjes nu til en dedikeret opgavekøpost, der definerer, hvornår dokumenterne bliver bogført. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

Hvis du vælger **PDF** i feltet **Rapportresultattype**, er alle købsordrer, der er blevet bogført, tilgængelige i delen **Rapportindbakke** i rollecenteret.

## <a name="see-also"></a>Se også
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  
[Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Redigere bogførte dokumenter](across-edit-posted-document.md)  
[Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
