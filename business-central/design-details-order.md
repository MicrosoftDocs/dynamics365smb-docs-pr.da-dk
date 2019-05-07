---
title: Designoplysninger – Ordre | Microsoft Docs
description: Dette emne indeholder oplysninger om ordre-til-ordre-links i et miljø med fremstil-til-ordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3a0014a80bd4f1f6c786638ddec23a1852c9a635
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "913844"
---
# <a name="design-details-order"></a>Designoplysninger: Ordre
I et Fremstil-til-ordre-miljø bliver en vare købt eller produceret udelukkende til at dække et bestemt behov. Normalt relateres det til A-varer, og motivationen for at vælge denne ordregenbestillingsmetode kan være, at behovet er sjældent, leveringstiden er ubetydelig, eller de påkrævede attributter varierer.  

Programmet opretter et ordre-til-ordre-link, der fungerer som en indledende forbindelse mellem forsyningen, en forsyningsordre eller lager og det behov, som den eller det skal opfylde.  

Bortset fra brug af prdrepolitikken, kan ordre-til-ordre-linket anvendes under planlægningen på følgende måder:  

* Når produktionsmetoden Fremstil-til-ordre bruges til at oprette produktionsordrer med flere niveauer eller produktionsordrer af projekttype (fremstilling af nødvendige komponenter på den samme produktionsordre).  
* Når funktionen Salgsordreplanlægning bruges til at oprette en produktionsordre fra en salgsordre.  

Selvom en produktionsvirksomhed anser sig selv som værende et Fremstil-til-ordre-miljø, kan det være bedst at bruge en genbestillingsmetode med lot-for-lot, hvis varerne er ren standard uden variation i attributter. Som resultat vil systemet bruge ikke-planlagt lagerbeholdning og akkumulerer kun salgsordrer med samme afsendelsesdato eller inden for et defineret interval.  

## <a name="order-to-order-links-and-past-due-dates"></a>Ordre-til-ordre-links og overskredne datoer  
I modsætning til de fleste forsyning-behov-sæt, planlægges tilknyttede ordrer med forfaldsdatoer, før planlægningsstartdatoen er fuldt planlagt af systemet. Forretningsårsagen til denne undtagelse er, at bestemte behov-forsyningssæt skal synkroniseres til kørsel. Du kan finde flere oplysninger om den fastlåste zone, der gælder for de fleste behovsforsyningstyper i [Designoplysninger: Håndtering af ordrer før planlægningsstartdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="see-also"></a>Se også  
[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
