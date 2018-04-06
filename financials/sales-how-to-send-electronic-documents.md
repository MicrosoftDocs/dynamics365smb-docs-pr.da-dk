---
title: Sende elektroniske dokumenter | Microsoft Docs
description: "Lær, hvordan du sender fakturaer elektronisk."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fae5e37b8f1fcca84a474b2eac2039f7fc6d8245
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="send-electronic-documents"></a>Sende elektroniske dokumenter
Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter afsendelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester. En udbyder af dokumentudvekslingstjenester sender elektroniske dokumenter mellem handelspartnere. For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.  

 I den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] er en dokumentudvekslingstjeneste forudkonfigureret og klar til at blive konfigureret til din virksomhed. Du kan finde flere oplysninger i [Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).  

 For at sende en salgsfaktura som et elektronisk PEPPOL-dokument skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**, hvor du også kan konfigurere kundens standardprofil til afsendelse af dokumenter. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i felterne i [Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Sådan sendes en elektronisk salgsfaktura  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  

2.  Opret en ny salgsfaktura.  

3.  Når salgsfakturaen er klar til blive faktureret, skal du bruge fanen **Handlinger** i gruppen **Bogføring** og vælge **Bogfør og send**.  

     Hvis kundens standardafsendelsesprofil er **Elektronisk dokument**, bliver den vist i dialogboksen **Bekræftelse af bogfør og send**, og du skal bare klikke på knappen **Ja** for at bogføre og sende fakturaen elektronisk i det valgte format.  

4.  I dialogboksen **Bekræftelse af bogfør og send** skal du vælge knappen AssistEdit til højre for feltet **Send bilag til**.  

5.  I **Send dokument til** dialogboksen og i feltet **Elektronisk dokument** skal du vælge **Via dokumentudvekslingstjeneste**.  

6.  I feltet **Format** skal du vælge **PEPPOL**.  

7.  Vælg knappen **OK**. Dialogboksen **Bekræftelse af bogfør og send** vises. **Elektronisk dokument (PEPPOL)** føjes til feltet **Send dokument til**.  

8.  Vælg knappen **Ja**.  

     Salgsfakturaen bogføres og sendes til kunden som et elektronisk dokument i PEPPOL-format.  

    > [!NOTE]  
    >  Du kan også sende en bogført salgsfaktura som et elektronisk dokument. Fremgangsmåden er den samme som beskrevet i dette emne for ikke-bogførte salgsdokumenter. I vinduet **Bogført salgsfaktura** under fanen **Handlinger** i gruppen **Generelt** skal du vælge **Aktivitetslog** for at få vist status for det elektroniske dokument. Du kan finde flere oplysninger **Aktivitetslog**.  

## <a name="see-also"></a>Se også  
[Fakturere salg](sales-how-invoice-sales.md)  
[Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md)  
[Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)  
[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

