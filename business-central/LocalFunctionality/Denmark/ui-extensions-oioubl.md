---
title: Udvidelsen OIOUBL til elektronisk fakturering
description: Denne udvidelse gør det nemt at sende salgsdokumenter elektronisk til kunder i den danske offentlige sektor i OIOUBL-formatet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 3b9a5ca76b6282907214785b9e2c384d07a544d6
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381795"
---
# <a name="the-oioubl-extension-for-electronic-invoicing-in-denmark"></a>Udvidelsen OIOUBL til elektronisk fakturering i Danmark
Når du sælger varer eller tjenesteydelser til debitorer i den danske offentlige sektor, skal du sende dokumenter til kunden elektronisk i en XML-fil, der er struktureret til at opfylde kravene i en eller flere OIOUBL-profiler (Offentlig oplysninger Online - Universal Business Language).  

Udvidelsen OIOUBL i [!INCLUDE[prod_short](../../includes/prod_short.md)] gør det nemt at oprette disse XML-dokumenter for bogførte salgs- og servicefakturaer, kreditnotaer og udstedte rykkere (som omfatter rentenotaer).  

De aktuelle krav til at sende elektroniske fakturaer er baseret på UBL version 2.0-standarden. Du kan finde flere oplysninger på webstedet [https://aka.ms/OasisUblSite](https://aka.ms/OasisUblSite).

Du kan få yderligere oplysninger om OIOUBL generelt på webstedet med [OIOUBL-onlinedokumentationen](http://www.oioubl.info/classes/da/index.html) og webstedet til [Digitaliseringsstyrelsenl](https://digst.dk/).  

## <a name="getting-started-with-the-oioubl-extension"></a>Kom i gang med udvidelsen OIOUBL  
Som standard er OUOUBL-udvidelsen installeret i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Men, der er et par ting, du skal gøre, før du kan bruge udvidelsen:

* Konfigurere betalingsformer, betalingsbetingelser og varegebyrer.
* Konfigurere kunder til OIOUBL ved at angive en kontokode, OILUBL-profilen, der skal bruges til at udveksle dokumenter, og kundens geografiske placeringsnummer (GLN).

Du kan få flere oplysninger i [Konfigurere udvidelsen OIOUBL](how-to-set-up-oioubl.md).  

## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Konfigurere OIOUBL-udvidelsen](how-to-set-up-oioubl.md)  
[Oprette elektroniske dokumenter i et OIOUBL-format](how-to-create-electronic-documents-by-using-oioubl.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]