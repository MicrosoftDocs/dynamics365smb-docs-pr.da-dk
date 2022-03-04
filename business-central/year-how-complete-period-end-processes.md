---
title: Valgfrie aktiviteter til afslutning af perioder
description: I dette emne beskriver de valgfrie processer og aktiviteter til afslutning af regnskabsperioder i Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 3b2ab40e0386ced967ad3f389f70817321d9bd92
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142720"
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

## <a name="fixed-assets"></a>Anlægsaktiver

* Bogfør alle vedligeholdelsesomkostninger via anlægskladderne eller fakturaerne
* Bogfør reguleringer.
* Bogfør opskrivning.
* Bogfør nedskrivning.
* Opdater og bogfør anlægsgentagelseskladden.

## <a name="intercompany"></a>Koncernintern

* Behandle koncerninterne transaktioner

## <a name="calculate-and-process-sales-tax"></a>Beregn og behandl moms

* Udfyld momsangivelser.  

## <a name="see-also"></a>Se også

[Afslutning af år og perioder](year-close-years-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]