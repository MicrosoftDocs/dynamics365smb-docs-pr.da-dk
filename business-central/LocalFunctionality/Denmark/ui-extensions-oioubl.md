---
title: OIOUB-udvidelse til elektronisk fakturering | Microsoft Docs
description: "Udvidelsen gør det let at sende salgs- og servicefakturaer, kreditnotaer, rentenotaer og rykkere til kunder i den danske offentlige sektor elektronisk i OIOUBL-format (Offentlig Information Online UBL)."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/04/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b71f678215bef6d532ca3c60ad2010b6daa5398d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="the-oioubl-extension-for-electronic-invoicing-in-denmark"></a>Udvidelsen OIOUBL til elektronisk fakturering i Danmark
Når du sælger varer eller tjenesteydelser til debitorer i den danske offentlige sektor, skal du sende dokumenter til kunden elektronisk i en XML-fil, der er struktureret til at opfylde kravene i en eller flere OIOUBL-profiler (Offentlig oplysninger Online - Universal Business Language).  

Udvidelsen OIOUBL i [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gør det nemt at oprette disse XML-dokumenter for bogførte salgs- og servicefakturaer, kreditnotaer og udstedte rykkere (som omfatter rentenotaer).  

De aktuelle krav til at sende elektroniske fakturaer er baseret på UBL version 2.0-standarden. Du kan finde flere oplysninger på [OASIS UBL](http://go.microsoft.com/fwlink/?LinkId=212593)-webstedet. 

Yderligere oplysninger om OIOUBL generelt se webstedet for [OIOUBL-onlinedokumentation](http://www.oioubl.info), og siden [Ofte stillede spørgsmål](https://www.digst.dk/It-loesninger/NemHandel/Spoergsmaal-og-svar.aspx) på webstedet Digitaliseringsstyrelsen.  

## <a name="getting-started-with-the-oioubl-extension"></a>Kom i gang med udvidelsen OIOUBL  
Som standard er OUOUBL-udvidelsen installeret i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Men, der er et par ting, du skal gøre, før du kan bruge udvidelsen:

* Konfigurere betalingsformer, betalingsbetingelser og varegebyrer.
* Konfigurere kunder til OIOUBL ved at angive en kontokode, OIOUBL-profilen, der skal bruges til at udveksle dokumenter, og kundens geografiske placering nummer (GLN).

Du kan få flere oplysninger i [Konfigurere udvidelsen OIOUBL](how-to-set-up-oioubl.md).  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Konfigurere OIOUBL-udvidelsen](how-to-set-up-oioubl.md)  
[Oprette elektroniske dokumenter i et OIOUBL-format](how-to-create-electronic-documents-by-using-oioubl.md)  

