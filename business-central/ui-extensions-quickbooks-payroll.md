---
title: "Bruge udvidelsen Import af QuickBooks-lønfil | Microsoft Docs"
description: "Dette emne beskriver, hvordan du kan bruge udvidelsen til at importere gage- og løntransaktioner fra tjenesten QuickBooks."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 01/09/2019
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 79729b42b660399893aebe1116c80ef3b3209042
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.contentlocale: da-dk
ms.lasthandoff: 01/15/2019

---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Udvidelsen Import af QuickBooks-lønfiler
Brug udvidelsen Import af QuickBooks-lønfiler til at importere lønningstransaktioner fra QuickBooks til finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er f.eks. nyttigt, når du går over fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller hvis du outsourcer din løn, men også ønsker at holde styr på den i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Trin til import af løndata
Første trin for dig eller måske din bogholder er at bruge eksportfunktionen i QuickBooks til at eksportere løndata til en .IIF- fil. Det andet trin er at åbne siden **Finanskladder** i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruge handlingen **Importér løntransaktioner** til at importere filen. Under importprocessen knytter du finanskontiene fra QuickBooks til de tilsvarende konti i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det sidste trin er at bogføre lønningstransaktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] i overensstemmelse med kontotilknytningen. 

Du kan finde flere oplysninger under [Importere løntransaktioner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)    
[Finans](finance.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

