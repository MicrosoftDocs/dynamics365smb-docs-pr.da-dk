---
title: Konfigurere britiske GetAddress.io-postnummerudvidelser | Microsoft Docs
description: Beskriver, hvordan du installerer og konfigurerer postnummertjenesten for at importere adresser i Storbritannien
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/16/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 29b3b551e3ea8e8dfd52a3846332eec47f9346ce
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="set-up-the-getaddressio-uk-postcodes-extension"></a>Konfigurere britiske GetAddress.io-postnummerudvidelser
Denne udvidelse gør det nemt at angive adresser i Storbritannien for enheder som kunder, kontaktpersoner, medarbejdere, leverandører, bankkonti og osv. 

Dem britiske GetAddress.io-postnumerudvidelse bruger getAddress API'en til at finde adresser i postnumre i Storbritannien. Hvis du vil bruge udvidelsen, skal du hente en plan og en API-nøgle til getAddress-API'en. Det er nemt, og vi hjælpe dig med at gøre det, når du opretter den britiske GetAddress.io-postnummerudvidelse. Planer er baseret på brug, eller hvad der til tider omtales som kald. I dette tilfælde er et kald, når [!INCLUDE[d365fin](includes/d365fin_md.md)] viser en liste over adresser i et postnummer. Afhængigt af hvor ofte du tilføjer adresser skal du vælge den plan, der passer bedst til dig. Hvis du vælger **Hent API nøgle** på siden, skal du bruge planen **Fri**, hvor du kan tilføje 20 adresser pr. dag, og som gælder for 30 dage. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Sådan konfigurerer du britiske GetAddress.io-postnummerudvidelser 
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Serviceforbindelser** og derefter vælge det relaterede link.  
2. I vinduet **Serviceforbindelser** skal du vælge **Britisk postnummertjeneste**.
3. På siden **Konfiguration af postnummerudbyder** skal du vælge **Deaktiveret**.
4. I vinduet **Valg af postnummertjeneste** skal vælge **GetAddress.io**.
5. I vinduet **GetAddress.io konfiguration** skal du vælge **Hent API nøgle** for at åbne siden **Planer** på webstedet for getAddress-API'en.  

    **Bemærk!** Du skal muligvis tillade pop op-vinduer i din webbrowser.
6. Køb en plan, eller vælg **Hent API nøgle**, og angiv derefter din mailadresse.
7. Åbn mailen fra getAddress.io, og kopier API-nøglen. Nøglen findes under overskriften **Din API-nøgle**.
8. I vinduet **GetAddress.io konfiguration** skal du indsætte API-nøglen i feltet **API-nøgle** og derefter vælge **OK**.
9. På siden **Serviceforbindelser** skal du kontrollere, at feltet **Adresseudbyder** viser **GetAddress.io**. Hvis det gør det, er tjenesten aktiveret.

## <a name="see-also"></a>Se også
[Britiske GetAddress.io-postnumre](ui-extensions-getaddressio.md) [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
