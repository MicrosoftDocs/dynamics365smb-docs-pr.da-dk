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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9bba4d097ca24de094f153c91d7888811cdfd4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241188"
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
    |**Aktiveret**|Angiv, om tjenesten er aktiveret. **Bemærk:** Når du har aktiveret tjenesten, oprettes der mindst to opgavekøposter til behandling af den elektroniske dokumenttrafik ind og ud af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du deaktiverer tjenesten, slettes posterne i opgavekøen.|  
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
