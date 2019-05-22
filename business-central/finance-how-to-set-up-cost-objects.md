---
title: Sådan opsættes omkostningsemner | Microsoft Docs
description: Få at vide, hvordan du opsætter omkostningsemner, der svarer til dimensioner i finansregnskabet.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 725ad9ed12dd32dc1cc3257c266efa274ea964a0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239621"
---
# <a name="set-up-cost-objects"></a>Oprette omkostningsemner
Omkostningsobjekter er en virksomheds projekter, produkter eller tjenester. Diagrammet over omkostningsobjekter er lig dimensionsoplysningerne for regnskabet. Du kan angive diagrammet over omkostningsobjekter på følgende måder:  

* Overfør dimensionsværdier i regnskabet til diagrammet over omkostningsobjekter. Du kan foretage de nødvendige justeringer efter overførslen.  
* Opret et nyt diagram over omkostningsobjekter, der er uafhængigt af regnskabet, eller tilføje et nyt omkostningsobjekt til et eksisterende diagram over omkostningsobjekter. Du skal oprette hvert omkostningsobjekt individuelt.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Sådan overføres dimensionsværdier fra regnskabet til diagrammet over omkostningsobjekter.  
1.  Angiv en dimension, der skal være omkostningsobjektdimensionen på siden **Opdater CA-dimensioner**. Kun værdierne fra denne dimension overføres.  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsemner**, og vælg derefter det relaterede link.  
3.  Vælg handlingen **Hent omkostningsemner fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningsemner. Funktionen overfører de dimensionsværdier, som du definerede i trin 1.  

    > [!NOTE]  
    >  Du kan indstille feltet **Opdater omkostningsemnedimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningsemner. Du kan ikke definere en synkronisering af diagrammet over omkostningsobjekter fra regnskabet.  

Diagrammet over omkostningsobjekter indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Sådan oprettes nye omkostningsemner på siden Diagram over omkostningsemner  
Du kan oprette og vedligeholde omkostningsemner enten på **Omkostningsemnekortet** eller på siden **Diagram over omkostningsemner**. I denne procedure opretter du omkostningsobjekter på siden **Diagram over omkostningsemner**.  

1.  Åbn siden **Diagram over omkostningsemner** i redigeringstilstand.  
2.  I feltet **Kode** angives omkostningsemnets kode. Alle omkostningsobjekter skal have en kode.  
3.  I feltet **Navn** angives omkostningsemnets navn.  
4.  Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsemnet.  

    * For omkostningsemner af linjetypen **I alt** skal du udfylde feltet **I alt fra/til**. Brug operatoren **eller**, som er en lodret linje (**&#124;**), til at angive områder for omkostningsemner.  
    * For omkostningsobjekter af typen **Til-sum** udfyldes dette felt automatisk, når du bruger indrykningsfunktion.  
5.  Udfyld feltet **Sorteringsrækkefølge**.  
6.  Vælger den næste tomme linje for at oprette et nyt omkostningsobjekt, og gentag derefter trin 2 til 5.  
7.  Når du har oprettet alle omkostningsemner, kan du vælge handlingen **Indryk omkostningsemner**. Vælg knappen **Ja**.  

> [!IMPORTANT]  
>  Hvis du har angivet definitioner i felterne **I alt fra/til** for **Til-sum**-omkostningsemner, før du kører indrykningsfunktionen, skal du angive dem igen. Funktionen overskriver værdierne i alle **Til-sum**-felter.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Definition af omkostningssteder og omkostningsobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Saldi mellem omkostningstype, omkostningssted og omkostningsobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
[Om omkostningsregnskab](finance-about-cost-accounting.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
