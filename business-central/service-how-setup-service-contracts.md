---
title: Konfigurere servicekontrakter | Microsoft Docs
description: Få at vide, hvordan du definerer servicekontrakter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 785a1f813956fa769d55b9bd71544613ca463b5b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316136"
---
# <a name="set-up-service-contracts"></a>Opsætte servicekontrakter
Før du kan arbejde med kontrakter, skal du angive følgende: 

* **Servicekontraktgrupper**, som samler servicekontrakter, der på en eller anden måde er indbyrdes relateret.
* **Servicekontraktkontogrupper**, der bruges til at gruppere servicekontraktkonti for servicefakturaer, der er oprettet til servicekontrakter. Du tildeler disse grupper til servicekontrakter.  
* **Kontraktskabeloner**, som definerer kontraktlayout for kontrakter, der indeholder de mest almindeligt anvendte detaljer i servicekontrakter. Når du opretter servicekontrakttilbud, kan du gøre det ved at bruge skabeloner. Når du opretter et kontrakttilbud, indeholder felterne automatisk indholdet af skabelonfelterne.
* **Debitorskabeloner**, så du kan oprette tilbud til kontakter eller potentielle kunder, der ikke er registreret som debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Sådan defineres servicekontraktgrupper  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontraktgrupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Marker afkrydsningsfeltet **Kun rabat på kontraktordrer**, hvis kontrakt- eller servicerabatter kun skal være gyldige for kontraktserviceordrer, f.eks. vedligeholdelse.  

## <a name="to-set-up-a-service-contract-account-group"></a>Sådan oprettes servicekontraktkontogrupper  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontraktkontogrupper**, og vælg derefter det relaterede link.  
2. Opret en ny servicekontraktkontogruppe.   
3. Udfyld felterne **Kode** og **Beskrivelse**. Disse felter beskriver servicekontogruppen.  
4. Udfyld feltet **Ikkeforudbet. kontraktkonto**, og vælg finanskontonummeret for den ikke forudbetalte konto.  
5. I feltet **Forudbet. kontraktkonto** skal du vælge finanskontonummeret for den forudbetalte konto.  

## <a name="to-set-up-a-contract-template"></a>Sådan oprettes kontraktskabeloner  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Skabelon til servicekontrakt**, og vælg derefter det relaterede link.  
2. Opret en ny servicekontraktskabelon.  
3. I feltet **Nummer** skal du skrive et nummer til kontraktskabelonen.  
  
     Hvis du har defineret en nummerserie for kontraktskabeloner på siden **Serviceopsætning**, kan du trykke på Enter og få indsat det næste ledige kontraktskabelonnummer automatisk. Udfyld de andre felter efter behov.  
  
4. I oversigtspanelet **Faktura** skal du udfylde feltet **Servicekontraktkto.grp.kode**, **Faktureringsperiode** osv. Udfyld de andre felter efter behov.  
5. Vælg handlingen **Servicerabatter** for at tilføje kontraktrabatter.  

## <a name="to-set-up-a-customer-template"></a>Sådan oprettes debitorskabeloner  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorskabeloner**, og vælg derefter det relaterede link.  
2. Opret et nyt debitorskabelonkort.  
3. I oversigtspanelet **Generelt** skal du skrive en kode og en beskrivelse til debitorskabelonen i henholdsvis feltet **Kode** og **Beskrivelse**. 
4. Du kan definere søgekriterier ved at udfylde de øvrige felter, f.eks. **Lande-/områdekode**, **Distriktskode** og **Sprogkode**.  
5. Udfyld felterne **Virksomhedsbogføringsgruppe** og **Debitorbogføringsgruppe**.  

## <a name="see-also"></a>Se også
[Konfigurere Service](service-setup-service.md)