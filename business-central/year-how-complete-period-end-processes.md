---
title: Valgfrie aktiviteter til afslutning af perioder | Microsoft Docs
description: I dette emne beskriver de valgfrie processer og aktiviteter til afslutning af regnskabsperioder i Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6066d0ddcfc32520f56d053c9624e8c1d8e7505d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391020"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Oversigt over opgaver til afslutning af regnskabsperioder
[!INCLUDE[prod_short](includes/prod_short.md)] tvinger dig ikke at lukke perioder, men der er mange periodeafslutnings- (månedsafslutning) aktiviteter, du kan udføre. Dette emne indeholder en oversigt over valgfrie processer og aktiviteter til afslutning af perioder.  

## <a name="general-ledger"></a>Finansposter
* Angiv bogføringsperioder, som enten er brugerspecifikke, eller som gælder på tværs af hele systemet.  

    Dette angiver de datoer, du tillader bogføring mellem. Afhængigt af dine forretningsmæssige behov kan det være en god idé at tillade bogføring i begyndelsen af perioden eller mod afslutningen af den. Du kan finde flere oplysninger i [Angive bogføringsperioder](finance-how-specify-posting-periods.md).  
* Foretag alle nødvendige Finanspostreguleringer.  
* Opdater og bogfør gentagelseskladder.  
  <!--* Process Consolidations-->
* Kør kontoskemaer på følgende måde:  
  * Åbn siden **Kontoskema**, og vælg derefter handlingen **Udskriv**.  

## <a name="sales-and-receivables"></a>Salg
* Bogfør alle salgsordrer, fakturaer, kreditnotaer og returvareordrer.  
* Bogfør alle indbetalingskladder.  
* Opdater og bogfør de gentagelseskladder, som vedrører salg.  
* Afstem aldersfordelte tilgodehavender, med finansposterne.  
* Udfør kørslen **Slet fakturerede salgsordrer**.  

## <a name="purchases-and-payables"></a>Køb og gæld
* Bogfør alle købsordrer, fakturaer, kreditnotaer og returvareordrer.  
* Bogfør alle udbetalingskladder.  
* Opdater og bogfør de gentagelseskladder, som vedrører Køb.  
* Udfør rapporten **Aldersfordelt gæld**, og afstem gæld med finansposterne.  
* Udfør kørslen **Slet fakturerede købsordrer**.  

Anlægsaktiver
* Bogfør alle vedligeholdelsesomkostninger via anlægskladderne eller fakturaerne
* Bogfør reguleringer.
* Bogfør opskrivning.
* Bogfør nedskrivning.
* Opdater og bogfør anlægsgentagelseskladden.

Koncernintern
* Behandle koncerninterne transaktioner

## <a name="calculate-and-process-sales-tax"></a>Beregn og behandl moms
* Udfyld momsangivelser.  

## <a name="see-also"></a>Se også
[Afslutning af år og perioder](year-close-years-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]