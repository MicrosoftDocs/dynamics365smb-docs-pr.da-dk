---
title: Definere koder for standardservices | Microsoft Docs
description: Få at vide, hvordan du definerer koder for serviceaktiviteter, du udfører ofte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d1d017d74eff9a4bd017cb9417913c0bd37ec500
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388820"
---
# <a name="set-up-standard-service-codes"></a>Konfigurere standardservicekoder

Når der foretages standardservice, skal der ofte oprettes servicedokumenter, der bruger servicelinjer, der indeholder ensartede oplysninger. For at gøre det nemmere at oprette disse linjer kan du oprette standardservicekoder, der har et foruddefineret sæt af servicelinjer. Når du vælger koden i et servicedokument, indsættes linjerne automatisk. Du kan oprette et hvilket som helst antal standardservicekoder, og hver kode kan have et ubegrænset antal servicelinjer af forskellige typer, herunder vare, ressource, pris eller standardtekst, tilknyttet. Du opretter servicelinjer for hver standardservicekode på kortet **Standardservicekode**. Derefter tildeler du standardservicekoder til serviceartikelgrupper på siden **Koder til standardserv.varegrupper**. Senere, når du opretter et servicedokument, du kan bruge handlingen **Hent standardservicekoder** til at tilføje servicelinjer.  
  
> [!Tip]
> Du kan bruge den samme fremgangsmåde til at oprette linjer på salgs- og købsdokumenter. Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).  
  
## <a name="to-set-up-a-standard-service-code"></a>Sådan oprettes standardservicekoder

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardservicekoder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Udfyld de servicelinjer, der er knyttet til denne servicekode.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Tildele en standardservicekode til en serviceartikelgruppe

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Udfyld de servicelinjer, der er knyttet til denne servicekode.  

## <a name="see-also"></a>Se også

[Service Management](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]