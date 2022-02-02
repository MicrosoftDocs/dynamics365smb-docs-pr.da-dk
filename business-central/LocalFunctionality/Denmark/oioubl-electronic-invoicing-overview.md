---
title: Oversigt over elektronisk OIOUBL-fakturering | Microsoft Docs
description: Få mere at vide om, hvordan Business Central understøtter behovet for at sende salgsdokumenter til den danske offentlige sektor elektronisk i OIOUBL-format.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 976d3ffdca67e7cbe42adf47df96200d29154ee0
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011961"
---
# <a name="oioubl-electronic-invoicing-overview"></a>Oversigt over elektronisk OIOUBL-fakturering
Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL). Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale.  

Du kan finde flere oplysninger om elektronisk OIOUBL-fakturering i [oioubl.info](http://www.oioubl.info/classes/da/index.html).  

## <a name="implementation-in-prod_short"></a>Implementering i [!INCLUDE[prod_short](../../includes/prod_short.md)]  
De aktuelle krav til at sende elektroniske fakturaer er baseret på OIOUBL, som er baseret på UBL (Universal Business Language) version 2.0-standarden. Du kan finde flere oplysninger på [OASIS UBL](https://aka.ms/OasisUblSite)-webstedet. De genererede XML-dokumenter kan derefter sendes til debitoren.  

For at sende dokumenter elektronisk skal du knytte europæiske EAN-lokationsnumre (European Article Numbering) og kontokoder til de relevante debitorer på siden **Debitorkort**. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md). Disse tal medtages, når du opretter dokumenter og bogfører eller udsteder dem. Når dokumenterne er bogførte eller udstedt, kan du oprette elektroniske versioner af dem, som kan sendes til debitoren. Du kan sende følgende typer dokumenter:  

- Salgsfaktura  
- Servicefaktura  
- Salgskreditnota  
- Servicekreditnota  
- Rentenota  
- Rykker  

De elektroniske dokumenter gemmes på de placeringer, som er angivet i Salgsopsætning.  

## <a name="oioubl-profiles"></a>OIOUBL-profiler

Kunderne kan bruge en profil, der er baseret på de danske OIOUBL-definitioner, eller de kan bruge en profil, der er baseret på OIOUBL-implementering af NES-definitionerne (Northern European Subset). Nogle profiler kræver, at der sendes svar, når et elektronisk dokument modtages. Du kan angive, hvilken profil de fleste af dine kunder bruger. Hvis en kunde bruger en anden profil, kan du ændre dette på debitorkortet. For eksempel kan du angive, at standardprofilen er Procurement-OrdSim-BilSim-1.0, men at kunden 10000 kræver profilen urn: urn:www.nesubl.eu:profiles:profile5:ver2.0. Der er flere oplysninger i [Konfigurere OIOUBL](how-to-set-up-oioubl.md).  

Du kan finde flere oplysninger i emnet om OIOUBL-profiler i afsnittet Ofte stillede spørgsmål på [Digitaliseringsstyrelsen](https://aka.ms/Digitaliseringsstyrelsen).  

## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Konfigurere OIOUBL](how-to-set-up-oioubl.md)  
 [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)  
 [Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]