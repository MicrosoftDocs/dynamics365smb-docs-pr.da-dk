---
title: EAN-lokationsnummer | Microsoft Docs
description: "Et EAN-lokationsnummer (European Article Numbering) er en elektronisk adresse, som du kan bruge, når du sender en elektronisk faktura. Dette nummer identificerer entydigt køberens faktureringsadresse. EAN-lokationsnumre kan bruges i lande uden for Europa og kaldes også GLN (Global Location Numbers)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f75e61cb9fdc3649698c68e83f4f861d30e797cd
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="ean-location-number"></a>EAN-lokationsnummer
Et EAN-lokationsnummer (European Article Numbering) er en elektronisk adresse, som du kan bruge, når du sender en elektronisk faktura. Dette nummer identificerer entydigt køberens faktureringsadresse. EAN-lokationsnumre kan bruges i lande uden for Europa og kaldes også GLN (Global Location Numbers).  

## <a name="ean-location-numbers-in-included365finincludesd365finmdmd"></a>EAN-lokationsnumre i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]  
 Afdelinger, direktorater, organer og andre organisationer i den danske offentlige sektor har EAN-lokationsnumre, som entydigt identificerer debitorens faktureringsadresse. Hvis din virksomhed har en kunde i den offentlige sektor, skal du sende fakturaer og andre dokumenter elektronisk ved hjælp af Offentlig Information Online UBL (OIOUBL). For at gøre det, skal du angive kundens EAN-lokationsnummer. Du kan få flere oplysninger i [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

 Et EAN-lokationsnummer er en fast længde på 13 cifre. Dette nummer skal behandles i sin helhed. Nedenfor vises et eksempel på et EAN-nummer.  

 **5790987654321**  

 EAN-numre starter med et præfiks på tre cifre, som tildeles af EAN International. I Danmark er de tre første tal **579**. EAN-nummeret slutter med et kontrolciffer, som beregnes på basis af de første 12 cifre.  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)   
 [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)

