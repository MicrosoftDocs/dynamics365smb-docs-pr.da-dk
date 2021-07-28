---
title: 'Fremgangsmåde: Konfigurere en dokumentudvekslingstjeneste'
description: Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere ved at bruge "Doc Exch. Service Setup".
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 357c48c6b7ed8e2d44316805bba04ff9236f0e9b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436294"
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentudvekslingstjeneste
Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere. Du kan finde flere oplysninger i [Udveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Sådan konfigureres en dokumentudvekslingstjeneste  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af Doc. Exch. Service**, og vælg derefter det relaterede link.  
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