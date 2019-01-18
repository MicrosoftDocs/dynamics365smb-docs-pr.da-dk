---
title: "Bruge udvidelsen Import af Quickbooks-lønfil | Microsoft Docs"
description: "Beskriver, hvordan du kan bruge udvidelsen til at indlæse løn og løntransaktioner fra tjenesten Quickbooks-løn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: caf928b653b528c10820a8dfa8feff498c88f4ff
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Udvidelsen Import af Quickbooks-lønfiler
For at tage højde for lønbetalinger og relaterede transaktioner, skal du importere og bogføre finansielle transaktioner, der er foretaget af din lønningssystemudbyder i finansbogholderiet.

For at gøre dette skal du først importere en fil, som du modtager fra lønningsystemudbyderen, på siden **Finanskladde**. Derefter knytter du de eksterne konti i lønningslistefilen til de relevante finanskonti. Til sidst skal du bogføre lønningstransaktionerne i overensstemmelse med kontotilknytningen. Du kan finde flere oplysninger under [Importere løntransaktioner](finance-how-import-payroll-transactions.md).

Udvidelsen for import af Quickbooks-lønfiler giver dig mulighed for at importere løntransaktioner fra Quickbooks-løntjenesten.

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)    
[Finans](finance.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

