---
title: Designoplysninger – Lagerværdi | Microsoft Docs
description: Lagerværdi XE "Lagerværdi" er bestemmelse af de omkostninger, der er tildelt en lagervare, som udtrykt ved følgende ligning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1321c9cfdb3814802db295eb7f5dcc90b325c19e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "936712"
---
# <a name="design-details-inventory-valuation"></a>Designoplysninger: Lagerværdi
Lagerværdi XE "Lagerværdi" er bestemmelse af de omkostninger, der er tildelt en lagervare, som udtrykt ved følgende ligning.  

Afslutningslager = begyndelseslager + nettokøb – produktionspris  

Beregningen af lagerværdien bruger feltet **Kostbeløb (faktisk)** i værdiposterne for varen. Posterne er klassificeret i henhold til den posttype XE "Posttype", der svarer til omkostningskomponenter, direkte omkostninger, indirekte omkostninger, afvigelse, værdiregulering og afrunding. Du kan finde flere oplysninger i [Designoplysninger: Omkostningskomponenter](design-details-cost-components.md).  

Poster udlignes med hinanden, enten ved fast udligning XE "Udligning, fast" eller i henhold til det forventede generelle kostprisforløb, der er defineret af omkostningsmetoden XE "Metode; omkostning" XE "Omkostningsmetode". En post på lagerreducering kan anvendes til mere end én tilgangspost med forskellige bogføringsdatoer og eventuelle andre anskaffelsesomkostninger XE "Anskaffelse". Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md). Beregning af lagerværdien XE "Lagerværdi" for en given dato er derfor baseret på en opsummering af positive og negative værdiposter.  

## <a name="inventory-valuation-report"></a>Lagerværdirapport  
For at beregne lagerværdien i rapporten **Lagerværdi** begynder rapporten at beregne varens lagerværdi på en angivet startdato. Derefter tilføjes værdien af lagerforøgelser, og værdien af lagerreduceringer fratrækkes op til en bestemt slutdato. Slutresultatet er lagerværdien på slutdatoen. Rapporten beregner disse værdier ved at addere værdierne i feltet **Kostbeløb (faktisk)** i værdiposterne med bogføringsdatoerne som filtre.  

Den udskrevne rapport viser altid faktiske beløb, det vil sige købsprisen for poster, der er bogført som fakturerede. Rapporten udskriver også den forventede købspris på poster, der er bogført som modtaget eller leveret, hvis du markerer feltet Medtag forventet kostpris på oversigtspanelet Indstillinger.  

> [!IMPORTANT]  
>  Værdier i rapporten **Lagerværdi** er afstemt med lagerkontoen i Finans, hvilket betyder, at de pågældende værdiposter, er bogført i Finans.  

> [!IMPORTANT]  
>  Beløb i kolonnen **Værdi** i rapporten er baseret på bogføringsdatoen af transaktioner for en vare.  

## <a name="inventory-valuation---wip-report"></a>Lagerværdi – igangværende arbejde, rapport  
En produktionsvirksomhed skal bestemme værdien af tre typer af lagerbeholdning:  

* Lager af råmaterialer  
* VIA-lagerbeholdning  
* Færdigvarelager  

Værdien af VIA-lagerbeholdningen bestemmes af følgende ligning:  

* Afslutning af igangværende arbejde på lager = Begyndelse på igangværende arbejde på lager + produktionsomkostninger – omkostninger ved producerede varer  

Hvad angår købt lager, danner værdiposterne grundlag for lagerværdien. Beregningen foretages ved hjælp af værdierne i feltet **Kostbeløb (faktisk)** for de vare- og kapacitetsværdiposter, der er knyttet til en produktionsordre.  

Formålet med VIA-lagerværdi er at bestemme værdien af de varer, hvis produktion endnu ikke er fuldført på en given dato. Derfor er VIA-lagerbeholdningen baseret på de værdiposter, der er relateret til forbrugs- og kapacitetsposter. Forbrugsposter skal være fuldt faktureret ved værdiansættelsesdatoen. Derfor viser rapporten **Lagerværdi - igangværende arb.** omkostningerne, der repræsenterer det igangværende arbejdes værdi i to kategorier: forbrug og kapacitet.  

## <a name="see-also"></a>Se også  
[Designoplysninger: Afstemning med Finans](design-details-reconciliation-with-the-general-ledger.md)   
[Designoplysninger: Regulering](design-details-revaluation.md)   
[Designoplysninger: Bogføring af produktionsordrer](design-details-production-order-posting.md)
[Administrere lageromkostninger](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
