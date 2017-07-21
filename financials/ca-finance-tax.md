---
title: Moms i Canada | Microsoft Docs
description: "Lær om lokal moms og moms på varer og ydelser i Canada."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Rapportering af salgsmoms på varer eller ydelser i Canada
I Canada, når en leverandørs virksomhed ikke er repræsenteret i det område, hvor der foretages køb, opkræver leverandøren kun moms af varer og tjenester eller harmoniseret moms. Hvis området har lokal moms (Provincial Sales Tax – PST), skal køberen dog stadig beregne PST og betale direkte til det lokale områdes myndigheder. Når en lokal skatteområdekode (Provincial Tax Area Code) er markeret, bruger [!INCLUDE[d365fin](includes/d365fin_md.md)] det til at beregne PST og bogføre den, så der er skattetilsvarsforpligtelse på både finanskontoen og skatteposter. Derfor skal den skatteområdekode, der vælges her, være en, hvor kun PST er inkluderet, ikke GST.  

Du kan finde flere oplysninger om moms i [Salgsmoms og skattegrupper i USA og Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Sende GST/HST-filen
Skatteoplysningerne i købsdokumenterne bruges til at oprette en overførsel af den GST/HST-onlinefil, du skal levere til skattemyndighederne. Filen indeholder moms for varer og tjenesteydelser (GST) og harmoniseret moms (HST). Filen oprettes i et .tax-filformat, der kan overføres online.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Salgsmoms og skattegrupper i USA og Canada](us-finance-sales-tax.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

