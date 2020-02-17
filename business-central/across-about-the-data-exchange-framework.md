---
title: Om Data Exchange Framework | Microsoft Docs
description: Filformatet til udveksling af data i bankfiler, elektroniske dokumenter, valutakurser og andet i ERP-systemer afhænger af udbyderen af datafilen eller streamen og landet/området.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/30/2020
ms.author: sgroespe
ms.openlocfilehash: 4ce48121b36ecd3f153d846f346c52b39a0c64bb
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999900"
---
# <a name="about-the-data-exchange-framework"></a>Om Data Exchange Framework
Du kan bruge dataudvekslingsstrukturen til at håndtere udveksling af forretningsdokumenter, bankfiler, valutakurser og andre datafiler med dine samarbejdspartnere.

Som administrator eller Microsoft-partner kan du bruge strukturen i nye integrationsfunktioner ved at definere, hvilke data der skal udveksles og hvordan. Filformatet til udveksling af data i bankfiler, elektroniske dokumenter, valutakurser og andet i ERP-systemer afhænger f.eks. af udbyderen af datafilen eller streamen og landet/området. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter forskellige bankfilformater og datatjenestestandarder. For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.

 Følgende diagrammer viser arkitektur af dataudvekslingsstrukturen.  

 ![Dataudvekslingsstruktur &#45; Import](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Dataudvekslingsstruktur &#45; Eksport](media/across-data-exchange/dataexchangeframework_export.png)  

 ## <a name="electronic-documents"></a>Elektroniske dokumenter
 Som et alternativ til at sende vedhæftede filer i en mail, kan du sende og modtage forretningsdokumenter elektronisk. Med et elektronisk dokumentet menes en standardkompatibel fil, der repræsenterer et forretningsdokument, f.eks en faktura fra en kreditor, som du kan modtage og konvertere til en købsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Udvekslingen af elektroniske forretningsdokumenter mellem to handelspartnere udføres af en ekstern udbyder af dokumentudvekslingstjenester. Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter afsendelse og modtagelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester. En større udbyder af dokumentudvekslingstjenester er forudkonfigureret og klar til at blive konfigureret til din virksomhed. For at understøtte andre elektroniske dokumentformater skal du oprette nye datoudvekslingsdefinitioner ved hjælp af Data Exchange Framework.  

 Fra PDF-filer eller billedfiler, der repræsenterer indgående bilag, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som du derefter kan konvertere til bilagsposter i [!INCLUDE[d365fin](includes/d365fin_md.md)], på samme måde som for elektroniske PEPPOL-dokumenter. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Efter nogle få sekunder får du filen tilbage som en elektronisk faktura, der kan konverteres til en købsfaktura for kreditoren. Hvis du sender filen til OCR-tjenesten via mail, oprettes en ny indgående bilagspost automatisk, når du får det elektroniske dokument tilbage igen.  

 Når du vil sende f.eks. en salgsfaktura som et elektronisk PEPPOL dokument, skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**. Herfra kan du også angive debitorens standardprofil for afsendelse af dokumenter. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer, når du konverterer data i felterne i [!INCLUDE[d365fin](includes/d365fin_md.md)] til elementer i den udgående dokumentfil. Datakonvertering og afsendelse af PEPPOL-salgsfakturaer udføres af dedikerede codeunits og XML-porte, som repræsenteres af det elektroniske **PEPPOL**-dokumentformat.  

 For at modtage f.eks. en faktura fra en kreditor som et elektronisk PEPPOL-dokument, skal du behandle dokumentet på siden **Indgående bilag** for at konvertere det til en faktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan enten konfigurere funktionen opgavekø for at behandle sådanne filer med jævne mellemrum, eller du kan starte processen manuelt. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, kreditorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer, når du konverterer data i elementerne i den indgående bilagsfil til felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Modtagelse og datakonvertering af PEPPOL-fakturaer udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **PEPPOL - Faktura**.  

  For at kunne modtage f.eks. en faktura som et elektronisk OCR-dokument skal du behandle den, som når du modtager et elektronisk PEPPOL-dokument. Modtagelse og konvertering af elektroniske PEPPOL-dokumenter fra OCR udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **OCR - Faktura**.  

 ## <a name="bank-files"></a>Bankfiler  
 Formatet af filer til udveksling af bankdata med ERP-systemer afhænger af leverandøren af filen og landet eller området. Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter import og eksport af SEPA-bankfiler (Single Euro Payments Area), og AMC Banking 365 Fundamentals-udvidelse gør det muligt at oprette forbindelse til en tjeneste til konvertering af bankdata, der leveres af en ekstern udbyder, AMC Consult. For at understøtte andre elektroniske dokumentformater kan du bruge Data Exchange Framework.  

 Hvis du vil eksportere SEPA-kreditoverførsler, skal du vælge knappen **Eksportér betalinger til fil** på siden **Udbetalingskladde** og derefter uploade filen for at behandle betalingerne i din bank. Du skal først konfigurere forskellige stamdata, såsom bankkonto, kreditorer og betalingsmetoder. Datakonvertering og eksport af SEPA-bankdata udføres af en dedikeret codeunit og XMLport, som repræsenteres bankeksport-/importkonfigurationen i **SEPA Kreditoverførsel**. Du kan også du kan konfigurere AMC Banking 365 Fundamentals-udvidelsen til at udføre eksporten repræsenteret af dataudvekslingsdefinitionen **Tjeneste til konvertering af bankdata - Kreditoverførsel**.  

 For at eksportere instruktioner til direkte SEPA-debitering skal du vælge knappen **Udlæs Direct Debit-fil** på siden **Direct Debit-opkrævninger** og derefter sende til din bank for at modtage de relevante debitorbetalinger automatisk. Først skal du konfigurere bankkonti, debitorer, Direct Debit-betalingsaftaler og betalingsmetoder. Datakonvertering og eksport af SEPA-bankdata udføres af en dedikeret codeunit og XMLport, som repræsenteres bankeksport-/importkonfigurationen i **SEPA Direct Debit**.  

 Hvis du vil indlæse SEPA-bankkontoudtog, skal du vælge knappen Importér bankkontoudtog på siderne **Betalingsudligningskladde** og **Bankkontoafstemning**, og derefter fortsætter du og anvender hver bankkontoudtogpost til betalinger eller bankposter, enten manuelt eller automatisk. Du skal først konfigurere bankkonti. Import og konvertering af SEPA-bankdata udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **SEPA CAMT**. Du kan også du kan konfigurere AMC Banking 365 Fundamentals-udvidelsen til at udføre importen repræsenteret af dataudvekslingsdefinitionen **Tjeneste til konvertering af bankdata - Bankkontoudtog**.  

 Desuden understøtter de lokale versioner af [!INCLUDE[d365fin](includes/d365fin_md.md)] forskellige andre filformater til import og eksport af bankdata, løntransaktioner og andre data. Du kan finde flere oplysninger i afsnittet "Lokal funktionalitet" i Hjælp i dine landeversion af [!INCLUDE[d365fin](includes/d365fin_md.md)].

  ## <a name="currency-exchange-rates"></a>Valutakurser  
 Du kan konfigurere en ekstern tjeneste til at holde dine valutakurser opdaterede. Den tjeneste, der leverer opdaterede valutakurser, aktiveres af en dataudvekslingsdefinition. På samme måde er siden **Opsætning af valutakursopdatering** et komprimeret billede af siden **Dataudvekslingsdefinition** for den pågældende dataudveksling.  

 Ved al udveksling af data i XML-filer kan du forberede dataudvekslingsopsætningen ved at indlæse den relaterede XML-skemafil på siden **XML-skemafremviser**. Her kan du vælge de dataelementer, du vil udveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)], og derefter enten initialisere en dataudvekslingsdefinition eller generere en XMLport.

## <a name="see-also"></a>Se også  
[Udveksle data elektronisk](across-data-exchange.md)  
[Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
