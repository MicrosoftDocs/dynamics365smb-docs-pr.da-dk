---
title: Om Data Exchange Framework
description: 'I dette emne forklares det, hvordan du kan bruge data Exchange-strukturen til at styre udvekslingen af data i forretningsdokumenter, f. eks. fakturaer med samarbejdspartnere.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 06/10/2021
ms.author: edupont
---
# <a name="about-the-data-exchange-framework" />Om Data Exchange Framework

Du kan bruge dataudvekslingsstrukturen til at håndtere udveksling af forretningsdokumenter, bankfiler, valutakurser og andre datafiler med dine samarbejdspartnere eller myndighederne.

Som administrator eller Microsoft-partner kan du bruge strukturen i nye integrationsfunktioner ved at definere, hvilke data der skal udveksles og hvordan. Filformatet til udveksling af data i bankfiler, elektroniske dokumenter, valutakurser og andet i ERP-systemer afhænger f.eks. af udbyderen af datafilen eller streamen og landet/området. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter forskellige bankfilformater og datatjenestestandarder. For at understøtte andre elektroniske dokumentformater kan du bruge dataudvekslingsstrukturen.

 Følgende diagrammer viser arkitektur af dataudvekslingsstrukturen.  

 ![Dataudvekslingsstruktur &#45; Import.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Dataudvekslingsstruktur &#45; Eksport.](media/across-data-exchange/dataexchangeframework_export.png)  

## <a name="electronic-documents" />Elektroniske dokumenter

Som et alternativ til at sende forretningsdokumenter som vedhæftede, kan du sende og modtage dem elektronisk. Et 'elektronisk dokumentet' menes en standardkompatibel fil, der repræsenterer et forretningsdokument, f.eks en faktura fra en kreditor, som du kan modtage og konvertere til en købsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Handelspartnere udveksler elektroniske dokumenter via eksterne dokumentudvekslingstjenester. Som standard understøtter [!INCLUDE[prod_short](includes/prod_short.md)] afsendelse og modtagelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester. En større udbyder af dokumentudvekslingstjenester, Tradeshift, er forudkonfigureret og klar til at blive konfigureret til din virksomhed. For at understøtte andre elektroniske dokumentformater skal du oprette nye dataudvekslingsdefinitioner.  

Fra PDF-filer eller billedfiler, der repræsenterer indgående bilag, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som du derefter kan konvertere til bilagsposter i [!INCLUDE[prod_short](includes/prod_short.md)], på samme måde som for elektroniske PEPPOL-dokumenter. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Efter nogle få sekunder får du filen tilbage som en elektronisk faktura, der kan konverteres til en købsfaktura for kreditoren. Hvis du sender filen til OCR-tjenesten via mail, oprettes en ny indgående bilagspost automatisk, når du får det elektroniske dokument tilbage igen.  

Når du vil sende f.eks. en salgsfaktura som et elektronisk PEPPOL dokument, skal du vælge indstillingen **Elektronisk dokument** i dialogboksen **Bogfør og send**. Herfra kan du også angive debitorens standardprofil for afsendelse af dokumenter. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer, når du konverterer data i felterne i [!INCLUDE[prod_short](includes/prod_short.md)] til elementer i den udgående dokumentfil. Datakonvertering og afsendelse af PEPPOL-salgsfakturaer udføres af dedikerede codeunits og XML-porte, som repræsenteres af det elektroniske **PEPPOL**-dokumentformat.  

For at modtage f.eks. en faktura fra en kreditor som et elektronisk PEPPOL-dokument, skal du behandle dokumentet på siden **Indgående bilag** for at konvertere det til en faktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan enten konfigurere funktionen opgavekø for at behandle sådanne filer med jævne mellemrum, eller du kan starte processen manuelt. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, kreditorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer, når du konverterer data i elementerne i den indgående bilagsfil til felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Modtagelse og datakonvertering af PEPPOL-fakturaer udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **PEPPOL - Faktura**.  

  For at kunne modtage f.eks. en faktura som et elektronisk OCR-dokument skal du behandle den, som når du modtager et elektronisk PEPPOL-dokument. Modtagelse og konvertering af elektroniske PEPPOL-dokumenter fra OCR udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **OCR - Faktura**.  

## <a name="bank-files" />Bankfiler

Formatet af filer til udveksling af bankdata med virksomhedsadministrationsapplikationer afhænger af leverandøren af filen og landet eller området. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter import og eksport af SEPA-bankfiler (Single Euro Payments Area). Derudover giver AMC Banking 365 Fundamentals-udvidelsen dig mulighed for at oprette forbindelse til en AMC Banking 365 Fundamentals-udvidelse, der leveres af en ekstern udbyder, AMC Consult. Du kan finde flere oplysninger i [Foretage indbetalinger med AMC Banking 365 Fundamentals-udvidelsen eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). For at understøtte andre elektroniske dokumentformater kan du bruge Data Exchange Framework.  

Hvis du vil eksportere SEPA-kreditoverførsler, skal du vælge knappen **Eksportér betalinger til fil** på siden **Udbetalingskladde** og derefter uploade filen for at behandle betalingerne i din bank. Du skal først konfigurere forskellige stamdata, såsom bankkonto, kreditorer og betalingsmetoder. Datakonvertering og eksport af SEPA-bankdata udføres af en dedikeret codeunit og XMLport, som repræsenteres bankeksport-/importkonfigurationen i **SEPA Kreditoverførsel**. Du kan også du kan konfigurere AMC Banking 365 Fundamentals-udvidelsen til at udføre eksporten repræsenteret af **AMC Banking 365 Fundamentals-udvidelsen – Kreditoverførsel**-dataudvekslingsdefinitionen.  

 For at eksportere instruktioner til direkte SEPA-debitering skal du vælge knappen **Udlæs Direct Debit-fil** på siden **Direct Debit-opkrævninger** og derefter sende til din bank for at modtage de relevante debitorbetalinger automatisk. Først skal du konfigurere bankkonti, debitorer, Direct Debit-betalingsaftaler og betalingsmetoder. Datakonvertering og eksport af SEPA-bankdata udføres af en dedikeret codeunit og XMLport, som repræsenteres bankeksport-/importkonfigurationen i **SEPA Direct Debit**.  

 Hvis du vil indlæse SEPA-bankkontoudtog, skal du vælge knappen Importér bankkontoudtog på siderne **Betalingsudligningskladde** og **Bankkontoafstemning**, og derefter fortsætter du og anvender hver bankkontoudtogpost til betalinger eller bankposter, enten manuelt eller automatisk. Du skal først konfigurere bankkonti. Import og konvertering af SEPA-bankdata udføres af Data Exchange Framework, som er repræsenteret ved dataudvekslingsdefinitionen **SEPA CAMT**. Du kan også du kan konfigurere AMC Banking 365 Fundamentals-udvidelsen til at udføre importen repræsenteret af **AMC Banking 365 Fundamentals-udvidelsen – Bankkontoudtog**-dataudvekslingsdefinitionen.  

 Desuden understøtter de lokale versioner af [!INCLUDE[prod_short](includes/prod_short.md)] forskellige andre filformater til import og eksport af bankdata, løntransaktioner og andre data. Se landingssiden [Lokal funktionalitet](about-localization.md) for dit land/område i Hjælp for at få flere oplysninger.  

## <a name="currency-exchange-rates" />Valutakurser

Du kan konfigurere en ekstern tjeneste til at holde dine valutakurser opdaterede. Den tjeneste, der leverer opdaterede valutakurser, aktiveres af en dataudvekslingsdefinition. På samme måde er siden **Opsætning af valutakursopdatering** et komprimeret billede af siden **Dataudvekslingsdefinition** for den pågældende dataudveksling.  

Ved al udveksling af data i XML-filer kan du forberede dataudvekslingsopsætningen ved at indlæse den relaterede XML-skemafil på siden **XML-skemafremviser**. Her kan du vælge de dataelementer, du vil udveksle med [!INCLUDE[prod_short](includes/prod_short.md)], og derefter enten initialisere en dataudvekslingsdefinition eller generere en XMLport.

## <a name="intrastat" />Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] bruger Data Exchange-strukturen til Intrastat-rapportering, hvor du nemt kan oprette tidsstemplede filer i forskellige formater til eksport. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder forberedte formater til lokaliserede lande og til standardversion. Men du kan ændre standardrapporten eller oprette din egen.

## <a name="see-also" />Se også

[Udveksle data elektronisk](across-data-exchange.md)  
[Brug XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
