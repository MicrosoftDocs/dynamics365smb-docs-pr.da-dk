---
title: Oprette elektroniske dokumenter i et OIOUBL-format | Microsoft Docs
description: Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor i Danmark, skal du sende dokumenter elektronisk. I dette emne kan du læse, hvordan du gør dette.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/14/2020
ms.author: bholtorf
ms.openlocfilehash: 733c5c9ece0374bafda86f1d6dde03a9699cf8bf
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076399"
---
# <a name="create-electronic-documents-by-using-oioubl"></a>Oprette elektroniske dokumenter ved hjælp af OIOUBL
Når du sælger varer eller tjenesteydelser til en kunde i den offentlige sektor, skal du sende dokumenter elektronisk. I [!INCLUDE[d365fin](../../includes/d365fin_md.md)], kan du oprette elektroniske dokumenter til fakturaer, kreditnotaer, rykkere og rentenotaer. Før du kan oprette elektroniske dokumenter, skal du have angivet filplaceringer og oplysninger om kunderne. Du kan få flere oplysninger i [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md).  

Du kan oprette et elektronisk dokument, når du har bogført et salgs- eller servicedokument. I følgende afsnit beskrives, hvordan du bogfører en salgsfaktura med de nødvendige oplysninger og derefter opretter en elektronisk salgsfaktura, men samme fremgangsmåde gælder for salgs-og servicekreditnotaer og rykkere.  

## <a name="to-post-a-sales-invoice"></a>Sådan bogføres en salgsfaktura  
1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den salgsfaktura, som du vil bogføre.  
3.  Kontrollér, at feltet **Eksternt bilagsnr.** indeholder nummeret på det dokument, kunden har leveret. Elektroniske OIOUBL-dokumenter kræver dette nummer.

    > [!Note]  
    > For servicedokumenter skal du udfylde feltet **Din reference**.  

4.  I oversigtspanelet **Fakturering** skal du udfylde felterne **GLN** og **OIOUB-kontokode**.  

    Til rykkere og rentenotaer findes felterne i oversigtspanelet **Bogføring**.  

5.  Bogfør fakturaen.  

## <a name="to-create-an-electronic-sales-invoice"></a>Sådan oprettes en elektronisk salgsfaktura  
Når du har bogført et dokument, kan du oprette en elektronisk faktura i OIOUBL-format. Nedenfor beskrives processen for bogførte salgsfakturaer, men proceduren er den samme for andre dokumenter.

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn den relevante bogførte salgsfaktura.  
3.  Vælg handlingen **Opret elektronisk <*dokumenttype*>**.  
4.  På siden **Opret elektronisk <*dokumenttype*>** kan du angive yderligere filtre og derefter vælge knappen **OK**.  

Derved oprettes en XML-fil, der gemmes på standardplaceringen for hentning på din enhed.


## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
 [Konfigurere kunder til OIOUBL](how-to-set-up-customers-for-oioubl.md)   
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)
