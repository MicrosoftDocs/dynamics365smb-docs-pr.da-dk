---
title: Sådan angives kontantkunder | Microsoft Docs
description: Dette emne beskriver trinnene i opsætning af debitor, som betaler kontant.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a4f73de177129f5bc33808e6acf74bd273ae0d33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915556"
---
# <a name="set-up-cash-customers"></a>Konfigurere kontantkunder
Du kan ikke oprette en faktura uden et debitornummer. Det gælder også, hvis du sælger kontant og ikke har noget at registrere i en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Definere en kontantkunde  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kunde**, og vælg derefter det relaterede link.  
2.  Opret et nyt kort for en **Kunde**. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).
3.  I feltet **Nummer** skal du f.eks. angive **Kontant**.  
4.  Angiv f.eks. **Kontantsalg** i feltet **Navn**.  
5.  I oversigtspanelet **Fakturering** skal du udfylde felterne **Debitorbogføringsgruppe** og feltet **Virksomhedsbogføringsgruppe**.  

 Du har nu angivet en debitor, der indeholder tilstrækkelige oplysninger til fakturering.  

> [!NOTE]  
>  Du kan vælge en bogføringsgruppe, der også anvendes til indenlandsk kreditsalg. Hvis du vil have separate salgstal for kontantsalg, f.eks. på en særlig salgskonto, kan du angive en ekstra bogføringsgruppe til dette formål.  
>   
>  Du skal angive et nummer til salgskonto for bogføringsgruppen, også selvom saldoen altid vil være 0, når du har bogført en faktura.  

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)    
[Finans](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]