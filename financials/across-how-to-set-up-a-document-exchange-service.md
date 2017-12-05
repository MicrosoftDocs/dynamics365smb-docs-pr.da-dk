---
title: "Sådan konfigureres en dokumentudvekslingstjeneste | Microsoft Docs"
description: Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: c014e3ee7ed580fd893470c0e0b89273eaceb429
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-set-up-a-document-exchange-service"></a>Fremgangsmåde: Konfigurere en dokumentudvekslingstjeneste
Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Sådan konfigureres en dokumentudvekslingstjeneste  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af dok.udv.tjen.**, og vælg derefter det relaterede link.  
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
>  Det anbefales, at du beskytter de logonoplysninger, du angiver i vinduet **Opsætning af VAN-tjeneste**. Du kan kryptere data på serveren ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på den serverforekomst, som opretter forbindelse til databasen. Dette beskrives i følgende fremgangsmåde:  

## <a name="to-encrypt-your-logon-information"></a>Sådan krypterer du logonoplysningerne  
1. I vinduet **Opsætning af VAN-tjeneste** skal du vælge handlingen **Administration af kryptering**.  
2. Aktiver kryptering af dine data i vinduet **Administration af datakryptering**. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)

