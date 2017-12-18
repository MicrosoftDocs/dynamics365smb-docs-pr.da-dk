---
title: "Sådan oprettes elektroniske dokumenter ved hjælp af OIOUBL | Microsoft Docs"
description: "Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 6a524d65f3994ae882f9addd58c9c144defa7913
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-electronic-documents-by-using-oioubl"></a>Fremgangsmåde: Oprette elektroniske dokumenter ved hjælp af OIOUBL
Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk. I [!INCLUDE[d365fin](../../includes/d365fin_md.md)], kan du oprette elektroniske dokumenter til fakturaer, kreditnotaer, rykkere og rentenotaer. Før du kan oprette elektroniske dokumenter, skal du have angivet filplaceringer og oplysninger om kunderne. Du kan få flere oplysninger i [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

## <a name="creating-electronic-documents"></a>Oprettelse af elektroniske dokumenter  
Elektroniske dokumenter kan kun oprettes, når et dokument er bogført eller udstedt. I følgende afsnit beskrives, hvordan du bogfører en salgsfaktura med de nødvendige oplysninger og derefter opretter en elektronisk salgsfaktura, men samme fremgangsmåde gælder for salgskreditnotaer, rykkere, rentenotaer, servicefakturaer og servicekreditnotaer.  

### <a name="to-post-a-sales-invoice"></a>Sådan bogføres en salgsfaktura  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den salgsfaktura, som du vil bogføre.  
3.  I oversigtspanelet **Generelt** skal du kontrollere, at feltet **Eksternt bilagsnr.** indeholder nummeret på det dokument, kunden har leveret.  

    > [!IMPORTANT]  
    >  Dette er nødvendigt, hvis du vil oprette en elektronisk faktura.  

    For servicedokumenter skal du udfylde feltet **Din reference** i oversigtspanelet **Generelt**.  

4.  I oversigtspanelet **Fakturering** skal du sørge for, at følgende felter indeholder værdier:  

    -   **EAN-nr.**  
    -   **Kontokode**  
    -   **Betalingskanal**  

    Til rykkere og rentenotaer findes felterne i oversigtspanelet **Bogføring**.  

5.  Bogfør fakturaen.  

### <a name="to-create-an-electronic-sales-invoice"></a>Sådan oprettes en elektronisk salgsfaktura  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den relevante bogførte salgsfaktura.  
3.  Vælg handlingen **Opret elektronisk faktura**.  
4.  I vinduet **Opret elektroniske fakturaer** skal du angive yderligere filtre og derefter vælge knappen **OK**.  

En XML-fil oprettes og gemmes på den lokation, som er defineret i vinduet **Salgsopsætning**. Du kan nu sende dokumentet til kunden.  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Fremgangsmåde: Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
 [Fremgangsmåde: Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)

