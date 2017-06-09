---
title: Rapportering af 1099-transaktioner i USA | Microsoft Docs
description: "På købsdokumenterne kan du angive, at dokumentet er 1099-pligtigt, og du kan angive 1099-koden for kreditoren."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a0a31c28b6c96dc80593ac3862b97b36c3ec81c7
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="reporting-1099-transactions-in-the-us"></a>Rapportering af 1099 transaktioner i USA
De interne skattemyndigheder (IRS) kræver en eller flere versioner af skatteformularen 1099 for betalinger til kreditorer. Kopier af disse formularer skal sendes til kreditorer årligt på eller inden den sidste dag i januar. På købsdokumenterne kan du angive, at dokumentet er 1099-pligtigt, og du kan angive 1099-koden for kreditoren.  

## <a name="1099-codes"></a>1099 koder
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er de mest almindelige 1099-koder allerede konfigureret for dig, så du er klar til at oprette de nødvendige rapporter. Koderne er defineret i vinduet **IRS 1099-formular for**, hvor du også kan tilføje nye 1099-koder. For hver skattepligtig kreditor kan du derefter angive den relevante 1099-kode på oversigtspanelet **Betalinger** på kreditorkortet.  

Med rapporten **1099-oplysninger for kreditor** kan du gennemse 1099-transaktioner, der er betalt i en bestemt periode. Ved afslutningen på året kan du udskrive 1099-transaktioner på fortrykte formularer.  

## <a name="printing-1099-tax-forms"></a>Udskrivning af 1099-skatteformularer
Fra vinduet **IRS 1099-formularfeltet** kan du få adgang til de følgende skatteformularer:  

* Kreditor 1099-div  

  Udskriver den føderale formular 1099-DIV for udbytte og distribution. Du kan udskrive alle eller specifikke 1099-DIV formularer. Rapporten anvender de koder, der gælder for DIV-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.  
* Kreditor 1099 Int  

  Udskriver den føderale formular 1099-INT for renteindtægter. Du kan udskrive alle eller specifikke 1099-INT formularer. Rapporten anvender de koder, der gælder for INT-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.  
* Diverse 1099 for kreditor - diverse indtægter  

  Udskriver den føderale formular 1099-MISC for diverse indtægter. Du kan udskrive alle eller specifikke 1099-MISC formularer. Rapporten anvender de koder, der gælder for MISC-formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**.  

Lovmæssige ændringer, der berører denne rapport og tabeldataene, håndteres normalt i opdateringer i slutningen af året.
Det kan være nyttigt at køre rapporten **1099-oplysninger for kreditor** for at gennemgå dataene, inden formularerne udskrives.

## <a name="submitting-1099-tax-forms-electronically"></a>Indsendelse af 1099-skatteformularer elektronisk
Hvis du vil sende 1099-skatteformularer elektronisk, kan du bruge rapporten **Kreditor 1099 magnetiske medier**. Angiver de 1099-formularer, som kan eksporteres. De formularoplysninger, der eksporteres i denne rapport, er de samme, som de rapporter, der udskriver 1099-formularer, som er beskrevet i det foregående afsnit.  

Rapporten anvender de koder, der gælder for formularens beløbsfelter, fra vinduet **IRS 1099-formularfelt**. Koderne er knyttet til formularfelterne i de forskellige fillayout i denne rapport, og tabeldataene og rapportversionen for et bestemt momsår skal derfor stemme overens. Hvis der tilføjes brugerdefinerede koder til tabellen, skal disse knyttes til formularfelterne i dette objekt.  

Lovmæssige ændringer, der berører denne rapport og tabeldataene, håndteres normalt i opdateringer i slutningen af året.
Det kan være nyttigt at køre rapporten **Kreditor 1099-oplysninger** for at gennemgå dataene, inden den elektroniske fil genereres.  

## <a name="see-also"></a>Se også
[Fremgangsmåde: Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

