---
title: "Sådan opsættes omkostningssteder | Microsoft Docs"
description: "Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter. Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7362518cbade8132fb07f49e7b2e9be67c4bce29
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-centers"></a>Oprette omkostningssteder
Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter. Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet. Du kan angive diagrammet over omkostningssteder på følgende måder:  

-   Overfør dimensionsværdier i regnskabet til diagrammet over omkostningssteder. Du kan foretage de nødvendige justeringer efter overførslen.  
-   Opret et nyt diagram over omkostningssteder, der er uafhængigt af regnskabet, eller tilføj et nyt omkostningssted til et eksisterende diagram over omkostningssteder. Du skal oprette hvert omkostningssted individuelt.  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Sådan overføres dimensionsværdier i regnskabet til diagrammet over omkostningssteder.  
1.  Angiv en dimension, der skal være omkostningsstedsdimensionen i vinduet **Opdater CA-dimensioner**. Kun værdierne fra denne dimension overføres.  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningssteder**, og vælg derefter det relaterede link.  
3.  På fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Hent omkostningssteder fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningssteder. Funktionen overfører de dimensionsværdier, som du definerede i trin 1.  

    > [!NOTE]  
    >  Du kan indstille feltet **Opdater omkostningsstedsdimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningssteder. Du kan ikke definere en synkronisering af diagrammet over omkostningssteder fra regnskabet.  

Diagrammet over omkostningssteder indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a>Sådan oprettes nye omkostningssteder i vinduet Diagram over omkostningssteder  
Du kan oprette og vedligeholde omkostningssteder enten på kortet **Omkostningsstedskort** eller i vinduet **Diagram over omkostningssteder**. I denne procedure opretter du omkostningssteder i vinduet **Diagram over omkostningssteder**.  

1. Åbn vinduet **Diagram over omkostningssteder** i redigeringstilstand.  
2. I feltet **Kode** angives omkostningsstedets kode. Alle omkostningssteder skal have en kode.  
3. I feltet **Navn** angives omkostningsstedets navn.  
4. Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsstedet.  

    - For omkostningssteder af typen **I alt** skal du udfylde feltet **Sammentælling**. Brug operatoren **eller**, som er en lodret linje (**&#124;**) til at angive områder for omkostningssteder.  
    - For omkostningssteder af typen **Til-sum**udfyldes dette felt automatisk, når du bruger indrykningsfunktion.  
5.  Udfyld felterne **Sorteringsrækkefølge** og **Omkostningsundertype**.  
6.  Vælg den næste tomme linje for at oprette et nyt omkostningssteder, og gentag derefter trin 2 til 5.  
7.  Når du har oprettet alle omkostningssteder, kan du vælge handlingen **Indryk omkostningssteder**. Vælg knappen **Ja**.  

> [!IMPORTANT]  
>  Hvis du har angivet definitioner i felterne **Sammentælling** for **Til-sum**-omkostningssteder, før du kører indrykningsfunktionen, skal du angive dem igen. Funktionen overskriver værdierne i alle **Til-sum**-felter.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
[Om omkostningsregnskab](finance-about-cost-accounting.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

