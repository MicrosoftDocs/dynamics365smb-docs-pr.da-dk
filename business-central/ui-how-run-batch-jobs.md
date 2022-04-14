---
title: Udføre kørsler og XMLporte
description: Du kører kørsler for at behandle data og opdatere oplysninger, f.eks. for at foretage periodiske regnskabsaktiviteter eller udføre beregninger.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.search.form: 672, 676, 682, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: cd61ebd816fe5b701d493f03816f78d90b59e4f6
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512780"
---
# <a name="run-batch-jobs-and-xmlports"></a>Udføre kørsler og XMLporte

En kørsel er en rutine, hvor data behandles i bundter, f.eks. kørslen **Kursreguler valutabeholdninger**. Der findes kørsler, som udfører periodiske regnskabsaktiviteter, som f.eks. opgørelse af resultatopgørelsen ved afslutning af regnskabsåret. Mange kørsler udfører beregninger, som f.eks. beregningen af rentenotaer, kursjusteringer og beregning af salgspriser.

En kørsel minder om en rapport med den undtagelse, at kørslen bruger resultatet af sit arbejde til at opdatere oplysningerne direkte i stedet for at udskrive resultaterne.

Du kan planlægge, hvornår en kørsel skal udføres. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Sådan foretages en kørsel
1. Hvis du vil åbne anmodningssiden for den relevante kørsel, skal du vælge ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv navnet på batchjobbet, og vælg derefter det relaterede link.
2. Hvis der er et oversigtspanel med **Indstillinger** for kørslen, skal du udfylde felterne for at angive, hvad kørslen skal gøre.
3. Siden kan indeholde mere end et oversigtspanel med filtre, som du kan bruge til at begrænse de data, der inkluderes i kørslen. Du kan angive kriterier i de foreslåede filtre eller tilføje flere filtre.
4. Vælg **OK** for at starte kørslen.

## <a name="see-also"></a>Se også
[Sortering af, søgning i og filtrering af lister](ui-enter-criteria-filters.md)  
[Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]