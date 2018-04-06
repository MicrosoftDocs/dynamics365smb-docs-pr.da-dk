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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12916e8bb7cf38f84b38ab61587c1f26936ec3f8
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="ean-location-number"></a>EAN-lokationsnummer
Et EAN-lokationsnummer (European Article Numbering) er en elektronisk adresse, som du kan bruge, når du sender en elektronisk faktura. Dette nummer identificerer entydigt køberens faktureringsadresse. EAN-lokationsnumre kan bruges i lande uden for Europa og kaldes også GLN (Global Location Numbers).  

## <a name="ean-location-numbers-in-included365finincludesd365finmdmd"></a>EAN-lokationsnumre i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]  
 Afdelinger, direktorater, organer og andre organisationer i den danske offentlige sektor har EAN-lokationsnumre, som entydigt identificerer debitorens faktureringsadresse. Hvis din virksomhed har en kunde i den offentlige sektor, skal du sende fakturaer og andre dokumenter elektronisk ved hjælp af Offentlig Information Online UBL (OIOUBL). For at gøre det, skal du angive kundens EAN-lokationsnummer. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

 Et EAN-lokationsnummer er en fast længde på 13 cifre. Dette nummer skal behandles i sin helhed. Nedenfor vises et eksempel på et EAN-nummer.  

 **5790987654321**  

 EAN-numre starter med et præfiks på tre cifre, som tildeles af EAN International. I Danmark er de tre første tal **579**. EAN-nummeret slutter med et kontrolciffer, som beregnes på basis af de første 12 cifre.  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)   
 [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)

