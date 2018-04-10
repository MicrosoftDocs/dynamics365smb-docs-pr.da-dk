---
title: "Sådan konfigureres nye virksomheder ved brug af en cmdlet | Microsoft Docs"
description: "I en række scenarier kan du indlæse og importere en konfigurationspakke uden at involvere brugerne eller ved hjælp af RapidStart Services-brugergrænsefladen. Du kan gøre det ved hjælp af en Windows PowerShell-cmdlet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Konfigurere nye virksomheder ved brug af en cmdlet
I en række scenarier kan du indlæse og importere en konfigurationspakke uden at involvere brugerne eller ved hjælp af RapidStart Services-brugergrænsefladen. Du kan gøre det ved hjælp af en Windows PowerShell-cmdlet. Scenarier, hvor dette kan være nyttigt, omfatter:  

- Udføre import af data på tværs af flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installationer.
- Konfiguration af yderligere moduler til flere kunder.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Sådan implementeres en konfigurationspakke ved brug af cmdlet  

1. Forberede en RapidStart Services-pakke. Du kan for eksempel oprette en pakke for at importere bestemte værdier og navnene på tabellen og felterne, som disse værdier skal indsættes i.  
2. Placer pakken på en computer, hvor du kører cmdlet.  
3. Åbn [!INCLUDE[d365fin](includes/d365fin_md.md)] Administration Shell.  
4. Angiv **Invoke-NAVCodeUnit**, og angiv oplysninger, der svarer til følgende eksempel.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Denne cmdlet importerer pakken til hvert firma. Brugere kan begynde at bruge de nye funktioner med det samme.  

## <a name="see-also"></a>Se også  
[Konfigurere nye virksomheder](admin-how-to-configure-new-companies.md)  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell-cmdletter](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

