---
title: OIOUB-udvidelse til elektronisk fakturering | Microsoft Docs
description: Udvidelsen gør det let at sende salgs- og servicefakturaer, kreditnotaer, rentenotaer og rykkere til kunder i den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL).
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6c5c6d0add22a91be6c84e38ea434fbf8d54adfb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180818"
---
# <a name="the-oioubl-extension-for-electronic-invoicing-in-denmark"></a>Udvidelsen OIOUBL til elektronisk fakturering i Danmark
Når du sælger varer eller tjenesteydelser til debitorer i den danske offentlige sektor, skal du sende dokumenter til kunden elektronisk i en XML-fil, der er struktureret til at opfylde kravene i en eller flere OIOUBL-profiler (Offentlig oplysninger Online - Universal Business Language).  

Udvidelsen OIOUBL i [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gør det nemt at oprette disse XML-dokumenter for bogførte salgs- og servicefakturaer, kreditnotaer og udstedte rykkere (som omfatter rentenotaer).  

De aktuelle krav til at sende elektroniske fakturaer er baseret på UBL version 2.0-standarden. Du kan finde flere oplysninger på webstedet [https://aka.ms/OasisUblSite](https://aka.ms/OasisUblSite).

Du kan få yderligere oplysninger om OIOUBL generelt på webstedet med [OIOUBL-onlinedokumentationen](http://www.oioubl.info/classes/da/index.html) og webstedet til [Digitaliseringsstyrelsenl](https://digst.dk/).  

## <a name="getting-started-with-the-oioubl-extension"></a>Kom i gang med udvidelsen OIOUBL  
Som standard er OUOUBL-udvidelsen installeret i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Men, der er et par ting, du skal gøre, før du kan bruge udvidelsen:

* Konfigurere betalingsformer, betalingsbetingelser og varegebyrer.
* Konfigurere kunder til OIOUBL ved at angive en kontokode, OILUBL-profilen, der skal bruges til at udveksle dokumenter, og kundens geografiske placeringsnummer (GLN).

Du kan få flere oplysninger i [Konfigurere udvidelsen OIOUBL](how-to-set-up-oioubl.md).  

## <a name="see-also"></a>Se også

[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Konfigurere OIOUBL-udvidelsen](how-to-set-up-oioubl.md)  
[Oprette elektroniske dokumenter i et OIOUBL-format](how-to-create-electronic-documents-by-using-oioubl.md)  
