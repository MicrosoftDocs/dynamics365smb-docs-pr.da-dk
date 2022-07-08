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
ms.openlocfilehash: b8ff6bebf418a5473e2a53bfc8021d8f47d71abf
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079450"
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

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/close-fiscal-year-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Afslutning af år og perioder](year-close-years-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]