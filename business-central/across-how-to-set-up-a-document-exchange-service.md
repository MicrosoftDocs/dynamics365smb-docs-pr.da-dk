---
title: Sådan konfigureres en dokumentudvekslingstjeneste | Microsoft Docs
description: Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 92a1b6118f0617dfd219ab38be5ff8d029a68275
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754713"
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentudvekslingstjeneste
Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Sådan konfigureres en dokumentudvekslingstjeneste  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af dok.udv.tjen.**, og vælg derefter det relaterede link.  
2. Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brugeragent**|Skriv en tekst, der kan bruges til at identificere din virksomhed i dokumentudvekslingsprocesser.|  
    |**Lejer-id for dok.udv.**|Angiv lejeren i dokumentudvekslingstjenesten, der repræsenterer din virksomhed. Den leveres af udbyderen af dokumentudvekslingstjenesten.|  
    |**Aktiveret**|Angiv, om tjenesten er aktiveret. **Bemærk:** Når du har aktiveret tjenesten, oprettes der mindst to opgavekøposter til behandling af den elektroniske dokumenttrafik ind og ud af [!INCLUDE[prod_short](includes/prod_short.md)]. Når du deaktiverer tjenesten, slettes posterne i opgavekøen.|  
    |**URL-adresse til tilmelding**|Angiv den webside, hvor du tilmelder dig dokumentudvekslingstjenesten.|  
    |**URL-adresse for tjeneste**|Angiv adressen på den dokumentudvekslingstjeneste, som bliver kaldt, når du sender og modtager elektroniske dokumenter.|  
    |**URL-adresse til logon**|Angiv logonsiden for dokumentudvekslingstjenesten, hvor du angiver virksomhedens brugernavn og adgangskode for at logge på tjenesten.|  
    |**Forbrugernøgle**|Angiv trebenede OAuth-nøgle til forbrugernøglen. Den leveres af udbyderen af dokumentudvekslingstjenesten.|  
    |**Forbrugerhemmelighed**|Angiv den hemmelighed, der beskytter forbrugernøglen. Den leveres af udbyderen af dokumentudvekslingstjenesten.|  
    |**Token**|Angiv den trebenede OAuth-nøgle for tokenet. Den leveres af udbyderen af dokumentudvekslingstjenesten.|  
    |**Tokenhemmelighed**|Angiv den hemmelighed, der beskytter tokenet. Den leveres af udbyderen af dokumentudvekslingstjenesten.|  

    > [!NOTE]  
    > Dine logondata krypteres automatisk.

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]