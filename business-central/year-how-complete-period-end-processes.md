---
title: Valgfrie aktiviteter for ultimoperioder
description: Denne artikel beskriver de valgfrie processer og aktiviteter til lukning af regnskabsperioder i Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/02/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# Oversigt over opgaver til afslutning af regnskabsperioder

[!INCLUDE[prod_short](includes/prod_short.md)] Tvinger dig ikke til at lukke perioder, men der er mange periodeafslutningsaktiviteter (månedsafslutning). Denne artikel indeholder en oversigt over valgfrie processer og aktiviteter for ultimoperioder.  

## Finans

* Angiv bogføringsperioder, som enten er brugerspecifikke, eller som gælder på tværs af hele systemet.  

    Dette angiver de datoer, du tillader bogføring mellem. Afhængigt af din virksomhed kan det være en god idé at tillade bogføring i starten af perioden eller mod slutningen. Få mere at vide på [angive bogføringsperioder](finance-how-specify-posting-periods.md).  
* Foretag alle nødvendige Finanspostreguleringer.  
* Opdater og bogfør gentagelseskladder.  
  <!--* Process Consolidations-->
* Kør regnskabsrapporter på følgende måde:  
  * Åbn siden **Finansrapporter**, og vælg derefter handlingen **Udskriv**.  

## Salg og tilgodehavender

* Bogfør alle salgsordrer, fakturaer, kreditnotaer og returvareordrer.  
* Bogfør alle indbetalingskladder.  
* Opdater og bogfør de gentagelseskladder, som vedrører Salg og tilgodehavender.  
* Afstem aldersfordelte tilgodehavender, med finansposterne.  
* Udfør kørslen **Slet fakturerede salgsordrer**.  

## Køb og gæld

* Bogfør alle købsordrer, fakturaer, kreditnotaer og returvareordrer.  
* Bogfør alle udbetalingskladder.  
* Opdater og bogfør de gentagelseskladder, som vedrører Køb og gæld.  
* Udfør rapporten **Aldersfordelt gæld**, og afstem gæld med finansposterne.  
* Udfør kørslen **Slet fakturerede købsordrer**.  

## Anlæg

* Bogfør alle vedligeholdelsesomkostninger via anlægskladderne eller fakturaerne
* Bogfør reguleringer.
* Bogfør opskrivning.
* Bogfør nedskrivning.
* Opdater og bogfør anlægsgentagelseskladden.

## Intercompany-handel

* Behandle koncerninterne transaktioner.

## Beregn og behandl moms

* Udfyld momsangivelser.  

## Se også

[Lukke år og perioder](year-close-years-periods.md)  
[Afslutningregnskab](year-close-books.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
