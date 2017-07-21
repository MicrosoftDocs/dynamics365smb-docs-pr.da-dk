---
title: "Få mere at vide om Finans og kontoplan | Microsoft Docs"
description: Beskriver finans, kontoplanen og kontokategorier.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06becfd7e54803fea925e8364719576bef0a8bab
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Om Finans og kontoplanen
Finansregnskabet gemmer de finansielle data, og kontoplanen viser de konti, som alle finansposter bogføres til. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansopsætning og bogføringsopsætning
Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data.  

I vinduet **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:  

* Detaljer om fakturaafrunding  
* Adresseformater  
* Økonomirapportering  

Desuden kan du i vinduet **Bogføringsopsætning** angive, hvordan du vil oprette kombinationer af virksomheds- og produktbogføringsgrupper. Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper. Du kan finde flere oplysninger under [Opsætning af bogføringsgrupper](finance-posting-groups.md)  

## <a name="the-chart-of-accounts"></a>Kontoplan
Kontoplanen viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper, som bogføres til kontoen.  

Du kan tilføje, ændre eller slette finanskonti. Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier
Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.  

Vinduet **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem. Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.  

Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje i vinduet **Finanskontokategorier**. Dermed kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo. Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.  

Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter. Kontokategorier hjælper med at definere layoutet af regnskabet.  

F.eks. har standardsaldoopgørelsen en underkategori for Kassebeholdning under Omsætningsaktiver. Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, kan du:  

1. Tilføje to nye underkategorier. Én for kontantbeholdning og én for din checkkonto.  
2. Angive den ekstra rapportdefinition **Saldo for kassekonti** for disse underkategorier.  
3. Indrykke dem under underkategorien **Kassebeholdning**.  

Næste gang du genererer kontoskemaer viser din kontoopgørelse den samlede saldo for kontant og to linjer med saldi for kontantbeholdning og checkkontoen.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)  

