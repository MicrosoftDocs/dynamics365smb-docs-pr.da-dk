---
title: Oversigt over elektronisk OIOUBL-fakturering | Microsoft Docs
description: "Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL). Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: dd766011c8deb1754a684134971a3c621b98ecdf
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="oioubl-electronic-invoicing-overview"></a>Oversigt over elektronisk OIOUBL-fakturering
Virksomheder skal sende salgsfakturaer, kreditnotaer, rentenotaer og rykkere til den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL). Hvis en virksomhed ikke sender disse dokumenter elektronisk, kan myndighederne nægte at betale.  

Du kan finde flere oplysninger om elektronisk OIOUBL-fakturering i [oioubl.info](https://www.oioubl.info).  

## <a name="implementation-in-included365finincludesd365finmdmd"></a>Implementering i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]  
De aktuelle krav til at sende elektroniske fakturaer er baseret på OIOUBL, som er baseret på UBL (Universal Business Language) version 2.0-standarden. Du kan finde flere oplysninger på [OASIS UBL](https://aka.ms/OasisUblSite)-webstedet. De genererede XML-dokumenter kan derefter sendes til debitoren.  

For at sende dokumenter elektronisk skal du knytte europæiske EAN-lokationsnumre (European Article Numbering) og kontokoder til de relevante debitorer på siden **Debitorkort**. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md). Disse tal medtages, når du opretter dokumenter og bogfører eller udsteder dem. Når dokumenterne er bogførte eller udstedt, kan du oprette elektroniske versioner af dem, som kan sendes til debitoren. Du kan sende følgende typer dokumenter:  

-   Salgsfaktura  
-   Servicefaktura  
-   Salgskreditnota  
-   Servicekreditnota  
-   Rentenota  
-   Rykker  

De elektroniske dokumenter gemmes på de placeringer, som er angivet i Salgsopsætning.  

## <a name="oioubl-profiles"></a>OIOUBL-profiler  
Kunderne kan bruge en profil, der er baseret på de danske OIOUBL-definitioner, eller de kan bruge en profil, der er baseret på OIOUBL-implementering af NES-definitionerne (Northern European Subset). Nogle profiler kræver, at der sendes svar, når et elektronisk dokument modtages. Du kan angive, hvilken profil de fleste af dine kunder bruger. Hvis en kunde bruger en anden profil, kan du ændre dette på debitorkortet. For eksempel kan du angive, at standardprofilen er Procurement-OrdSim-BilSim-1.0, men at kunden 10000 kræver profilen urn: urn:www.nesubl.eu:profiles:profile5:ver2.0. Der er flere oplysninger i [Konfigurere OIOUBL](how-to-set-up-oioubl.md).  

Du kan finde flere oplysninger i emnet om OIOUBL-profiler i afsnittet Ofte stillede spørgsmål på [Digitaliseringsstyrelsen](https://aka.ms/Digitaliseringsstyrelsen).  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
 [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   
 [Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md)  

