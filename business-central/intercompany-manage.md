---
title: Transaktioner mellem virksomheder i den samme organisation | Microsoft Docs
description: Du kan forenkle forretningsgange og transaktioner mellem virksomheder i den samme organisation med Intercompany-funktionaliteten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c68e4bd69c854ecd99cfb833c941066d9a805da
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-intercompany-transactions"></a>Administrere Intercompany-transaktioner (IC)
Organisationen består muligvis af flere virksomheder, men har måske ikke det tilsvarende antal regnskabs- og administrationsgrupper. Med Intercompany-funktionen kan du handle med datterselskaber og interne partnerorganisationer på samme måde som med dine eksterne leverandører og kunder. Du angiver kun oplysninger om intercompany-transaktioner én gang i de relevante bilag. Du kan bruge de funktioner, du allerede kender, f.eks. likviditetsstyring. Tilknytningsfunktioner i kontoplanerne og dimensioner er med til at sikre, at oplysningerne vises de rigtige steder.  

Der er fire overordnede formål med Intercompany-funktioner:  

- Øget produktivitet på grund af sparet tid og forenklede transaktioner  
- Mindsket risiko for fejl, fordi oplysninger kun skal angives én enkelt gang og automatiserede opdateringer på tværs af hele systemet  
- Komplet revisionssporing og fuld synlighed af forretningsaktiviteter og transaktionsoversigter  
- Effektive og besparende transaktioner med søster- og datterselskaber  

Du har den fulde kontrol over alle transaktionsbilag. Du kan f.eks. afvise et bilag, der er sendt til dig, og på denne måde tilbageføre forkerte bogføringer. Eller når du foretager et køb fra en partner eller et datterselskab, kan du opdatere købsordren, så længe den sælgende virksomhed ikke har afsendt nogen varer.  

Når du angiver en transaktion, skal du ikke angive kontiene for et individuelt sæt af profiler, men blot oplyse partnervirksomhedens id. Intercompany-funktionen opretter finanslinjer, som resulterer i afstemning af profilerne i de to virksomheder, der er involveret i en transaktion. I tilgodehavender og skyldige beløb tildeler du en koncernintern partnerkode til alle kunder og leverandører. Fra det øjeblik af vil alle de ordrer og fakturaer, der oprettes på baggrund af transaktioner med disse virksomheder, resultere i tilsvarende bilag i partnervirksomheden, som igen resulterer i korrekt afstemning af kontiene.  

 Når du har oprettet forretningspartnere som debitorer og kreditorer i systemet og tildelt dem Intercompany-partnerkoder, er det muligt at udveksle IC-købs- og salgsbilag, herunder varer og varegebyrer. Intercompany-funktionen muliggør intercompany-transaktioner mellem flere databaser, f.eks. i forskellige lande såvel som flere valutaer, forskellige kontoplaner, forskellige dimensioner og forskellige varenumre.  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

 |Hvis du vil |Se|
 |---|---|
 |Opret koncerninterne kreditorer og debitorer som såkaldte koncerninterne partnere, og konfigurer en koncernintern (IC) kontoplan.|[Konfigurere mellemregning](intercompany-how-setup.md)|
 |Bruge IC-dokumenter eller -kladder til at bogføre transaktioner med koncerninterne partnere.|[Arbejde med koncerninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)|
 |Organisere og behandle indgående og udgående transaktioner, som du udveksler med dine koncerninterne partnere.|[Administrere IC-indbakken og -udbakken](intercompany-how-manage-intercompany-inbox.md)|

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

