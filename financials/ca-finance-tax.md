---
title: "Salgsmoms og moms på varer og ydelser i Canada | Microsoft Docs"
description: "Få mere at vide om moms på varer og ydelser (GST) og harmoniseret moms (HST)."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Salgsmoms og moms på varer og ydelser i Canada
I Canada, når en leverandørs virksomhed ikke er repræsenteret i det område, hvor der foretages køb, opkræver leverandøren kun moms af varer og tjenester eller harmoniseret moms. Hvis området har lokal moms (Provincial Sales Tax – PST), skal køberen dog stadig beregne PST og betale direkte til det lokale områdes myndigheder. Når en lokal skatteområdekode (Provincial Tax Area Code) er markeret, bruger [!INCLUDE[d365fin](includes/d365fin_md.md)] det til at beregne PST og bogføre den, så der er skattetilsvarsforpligtelse på både finanskontoen og skatteposter. Derfor skal den skatteområdekode, der vælges her, være en, hvor kun PST er inkluderet, ikke GST.  

Du kan finde flere oplysninger om moms i [Salgsmoms og skattegrupper i USA og Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Sende GST/HST-filen
Skatteoplysningerne i købsdokumenterne bruges til at oprette en overførsel af den GST/HST-onlinefil, du skal levere til skattemyndighederne. Filen indeholder moms for varer og tjenesteydelser (GST) og harmoniseret moms (HST). Filen oprettes i et .tax-filformat, der kan overføres online.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Salgsmoms og skattegrupper i USA og Canada](us-finance-sales-tax.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

