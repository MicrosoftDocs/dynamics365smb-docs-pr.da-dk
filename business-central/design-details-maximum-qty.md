---
title: "Designoplysninger – Maks. antal | Microsoft Docs"
description: "Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a9fd9a2387b209931165cd18bdfb025390778af5
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-maximum-qty"></a>Designoplysninger: Maks. antal
Det maksimale antal er en måde at vedligeholde lageret ved hjælp af et genbestillingspunkt.  
  
 Alt om den faste genbestillingsantalmetode gælder også for denne metode. Den eneste forskel er omfanget af den foreslåede forsyning. Når metoden med maksimalt antal bruges, defineres genbestillingsantallet dynamisk baseret på det planlagte lagerniveau og varierer derfor normalt fra ordre til ordre.  
  
## <a name="calculated-per-time-bucket"></a>Beregnet pr. interval  
 Genbestillingsantallet bestemmes på det tidspunkt (slutningen af et interval), hvor planlægningssystemet registrerer, at genbestillingspunktet er passeret. På dette tidspunkt måler systemet afstanden fra den nuværende forventede lagerbeholdning op til den angivne maksimale lagerbeholdning. Dette består af det antal, der skal genbestilles. Derefter kontrollerer systemet, om leveringen allerede er bestilt andre steder med henblik på at blive modtaget inden for leveringstiden, og i så fald reduceres mængden af den nye forsyningsordre med allerede bestilte antal.  
  
 Systemet sikrer, at den projekterede lagerbeholdning mindst når genbestillingsniveauet – i tilfælde af at brugeren har glemt at angive et maksimalt lagerantal.  
  
## <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
 Afhængigt af opsætningen, kan det være bedst at kombinere metoden Maks. antal med ordremodifikatorer for at sikre et mindste ordreantal eller afrunde til et heltal af købsmåleenheder eller opdele det i flere lotter, som er defineret af det højst tilladte antal.  
  
## <a name="combines-with-calendars"></a>Kombinerer med kalendere  
 Før der bliver foreslået en ny forsyningsordre for at opfylde et genbestillingspunkt, kontrollerer planlægningssystemet, om ordren er planlagt til en ikkearbejdsdag i overensstemmelse med de kalendere, der er defineret i feltet **Basiskalenderkode** i vinduerne **Virksomhedsoplysninger** og **Lokationskort**.  
  
 Hvis den planlagte dato er en ikkearbejdsdag, flytter planlægningssystemet ordren frem til den nærmeste arbejdsdag. Det kan resultere i en ordre, der opfylder et genbestillingspunkt, men ikke opfylder visse specifikke behov. Planlægningssystemet opretter en ekstra levering for sådanne behov.  
  
## <a name="see-also"></a>Se også  
 [Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md)   
 [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md)   
 [Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)
