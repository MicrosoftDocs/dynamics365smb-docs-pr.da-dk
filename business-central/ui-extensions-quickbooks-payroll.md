---
title: Bruge udvidelsen Import af QuickBooks-lønfil | Microsoft Docs
description: 'Dette emne beskriver, hvordan du kan bruge udvidelsen til at importere gage- og løntransaktioner fra tjenesten QuickBooks.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, salary, wage'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Udvidelsen Import af QuickBooks-lønfiler
Brug udvidelsen Import af QuickBooks-lønfiler til at importere lønningstransaktioner fra QuickBooks til finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette er f.eks. nyttigt, når du går over fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)], eller hvis du outsourcer din løn, men også ønsker at holde styr på den i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="steps-to-import-payroll-data"></a>Trin til import af løndata
Første trin for dig eller måske din bogholder er at bruge eksportfunktionen i QuickBooks til at eksportere løndata til en .IIF- fil. Det andet trin er at åbne siden **Finanskladder** i [!INCLUDE[prod_short](includes/prod_short.md)] og bruge handlingen **Importér løntransaktioner** til at importere filen. Under importprocessen knytter du finanskontiene fra QuickBooks til de tilsvarende konti i [!INCLUDE[prod_short](includes/prod_short.md)]. Det sidste trin er at bogføre lønningstransaktionerne i [!INCLUDE[prod_short](includes/prod_short.md)] i overensstemmelse med kontotilknytningen. 

Du kan finde flere oplysninger i [Importere løntransaktioner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)    
[Finans](finance.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
