---
title: "Sådan konfigureres OIOUBL | Microsoft Docs"
description: "Du skal angive en placering til lagring af OIOUBL-filer (Offentlig Information Online UBL), når du opretter elektroniske dokumenter som f.eks. fakturaer eller kreditnotaer. Du skal også definere betalingsformer, betalingsbetingelser og varegebyrer, og du skal oprette relevante kunder til OIOUBL."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b99524f9393f13716e977399ce24603b0aa4dc4
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-oioubl"></a>Konfigurere OIOUBL
Du skal angive en placering til lagring af OIOUBL-filer (Offentlig Information Online UBL), når du opretter elektroniske dokumenter som f.eks. fakturaer eller kreditnotaer. Du skal også definere betalingsformer, betalingsbetingelser og varegebyrer, og du skal oprette relevante kunder til OIOUBL.  

## <a name="to-set-up-oioubl-file-locations-for-sales-and-receivables"></a>Sådan konfigureres OIOUBL-filplaceringer for salg  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsopsætning**, og vælg derefter det relaterede link.  
2.  I vinduet **Opsætning af Salg** i oversigtspanelet **OIOUBL** i sektionen **Outputstier** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Fakturasti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filer til salgsfakturaer.|  
    |**Kreditnotasti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filerne til salgskreditnotaer.|  
    |**Rykkersti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filerne til rykkere.|  
    |**Rentenotasti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filerne til rentenotaer.|  

3.  I feltet **Standardkoden for OIOUBL-profil** skal du vælge den profil, som de fleste af dine kunder i den offentlige sektor bruger.  

    Når du vælger en profil, opdaterer [!INCLUDE[d365fin](../../includes/d365fin_md.md)] åbne salgs- og servicedokumenter med den angivne profil.  

    1.  Hvis du vil oprette en ny profil, skal du vælge feltet **Standardkoden for OIOUBL-profil** og derefter vælge **Ny**.  
    2.  I vinduet **OIOUBL-profilliste** skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Description|  
        |---------------------------------|---------------------------------------|  
        |**Kode**|Angiver koden for OIOUBL-profilen.|  
        |**Profil-id**|Angiver den profil, som du vil understøtte i de elektroniske dokumenter, som du sender til debitorer i den danske offentlige sektor, f.eks. **Indkøb-BilSim-1.0**.|  

4.  Vælg knappen **OK**.  

> [!IMPORTANT]  
>  Eksterne bilagsnumre kræves til OIOUBL-dokumenter, selvom du ikke har markeret feltet **Eksternt bilagsnr. obl.** i oversigtspanelet **Generelt**. Hvis dokumentet ikke har et eksternt bilagsnummer, får du en fejlmeddelelse.  

### <a name="to-set-up-oioubl-file-locations-for-service-management"></a>Sådan konfigureres OIOUBL-filplaceringer for servicestyring  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopsætning**, og vælg derefter det relaterede link.  
2.  I vinduet **Serviceopsætning** i oversigtspanelet **OIOUBL** i sektionen **Outputstier** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Servicefakturasti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filer til servicefakturaer.|  
    |**Servicekreditnotasti**|Stien til og navnet på den mappe, hvor du vil gemme OIOUBL-filerne til servicekreditnotaer.|  

3.  Vælg knappen **OK**.  

Du skal også tilføje en OIOUBL-betalingskanal til de betalingsformer, du bruger til elektroniske fakturaer. Du skal også angive en kode for de relevante betalingsbetingelser.  

## <a name="to-set-up-payment-methods-and-payments-terms"></a>Sådan konfigureres betalingsformer og betalingsbetingelser  
1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsformer**, og vælg derefter det relaterede link.  
2.  I vinduet **Betalingsformer** skal du for de betalingsformer, du vil bruge til elektroniske fakturaer, vælge en betalingskanal i feltet **Betalingskanal**. Den følgende tabel beskriver indstillingerne.  

    |Indstilling|Description|  
    |-------------------------------------|---------------------------------------|  
    |**Betalingsbon**|Betalingen foretages ved hjælp af en betalingsbon, som f.eks. giro eller et FI-kort (Fællesindbetalingskort). **Vigtigt:** Denne betalingskanal understøttes ikke i standardversionen af [!INCLUDE[d365fin](../../includes/d365fin_md.md)].|  
    |**Kontooverførsel**|Betalingen foretages ved overførsel fra kundens bankkonto.|  
    |**National transaktion**|Betalingen foretages ved overførsel fra kundens bankkonto og behandles af et clearinginstitut.|  
    |**Direkte hævning**|Betalingen foretages ved hjælp af PBS.|  

3.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsbetingelser**, og vælg derefter det relaterede link.  
4.  I vinduet **Betalingsbetingelser** skal du for hver betalingsform, du vil bruge til elektroniske fakturaer, vælge en kode i feltet **OIOXML-kode**. Du kan finde flere oplysninger i OIOXML-kode.  

Du skal derefter kategorisere dine varegebyrer.  

## <a name="to-set-up-item-charges"></a>Sådan konfigureres varegebyrer  
1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varegebyrer**, og vælg derefter det relaterede link.  
2.  I vinduet **Varegebyrer** skal du for hvert varegebyr vælge en kategori i feltet **Gebyrkategori**. Du kan finde flere oplysninger i Gebyrkategori.  

Du skal også sørge for, at feltet OIOUBL lande-områdekode for levering er udfyldt for Danmark i vinduet **Lande/områder**.  

Endelig skal du angive EAN-numre og kontokoder for de relevante debitorer. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)   
[Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   

