---
title: Sådan oprettes servicetilbud | Microsoft Docs
description: Du kan bruge siden **Servicetilbud** til at oprette dokumenter, hvor du indtaster oplysninger om en serviceydelse, f.eks. reparation og vedligeholdelse, for serviceartikler efter kundeforespørgsel. Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1486be71b0b848aa48996f4161f8987322a09e32
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "791994"
---
# <a name="create-service-quotes"></a>Oprette servicetilbud
Du kan betragte servicetilbud som grundlaget for serviceordrer. De er faktisk næsten identiske. Begge indeholder oplysninger, f.eks. hvem debitoren er, ordretypen, den vare, der har behov for service, fakturerings- og leveringsoplysninger og oplysninger om det aktuelle servicearbejde.
 
Du kan bruge et servicetilbud som foreløbig kladde til en serviceordre og derefter konvertere tilbuddet til en serviceordre.  
  
## <a name="to-create-a-service-quote"></a>Sådan oprettes servicetilbud  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicetilbud**, og vælg derefter det relaterede link.  
2. Opret et nyt servicetilbud.  
3. I feltet **Nummer** skal du indtaste et nummer på servicetilbuddet. Hvis du har defineret en nummerserie for servicetilbud på siden **Serviceopsætning**, kan du trykke på Enter for at vælge det næste tilgængelige servicetilbudsnummer.  
4. I feltet **Debitornr.**  skal du markere den relevante debitor på listen.  

  > [!Note]  
  >  De debitorrelevante felter udfyldes automatisk med oplysninger fra **debitorkortet**. Hvis der ikke findes et **debitorkort** for debitoren, og du har oprettet en debitorskabelon, kan du oprette debitoren fra servicetilbuddet. Udfyld de relevante felter, og vælg derefter handlingen **Opret debitor**.  
  
5. Afhængig af indstillingerne i oversigtspanelet **Obligatoriske felter** på siden **Serviceopsætning** kan det være nødvendigt at udfylde feltet **Serviceordretype** og feltet **Sælgerkode**.  
6. Udfyld serviceartikellinjerne.  
7. Registrer de anslåede kostpriser på servicelinjerne.  
  
## <a name="see-also"></a>Se også  
[Oprette serviceordrer](service-how-to-create-service-orders.md)  
[Arbejde med serviceopgaver](service-how-to-work-on-service-tasks.md)  

 