---
title: Sådan konfigureres afsendelse og modtagelse af elektroniske dokumenter | Microsoft Docs
description: 'Som et alternativ til at sende vedhæftede filer i en mail, kan du sende og modtage forretningsdokumenter elektronisk.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Konfigurere afsendelse og modtagelse af elektroniske dokumenter

> [!NOTE]
> Indholdet i denne artikel gælder kun for versioner af Dynamics 365 Business Central, der blev udgivet før udgivelsesbølge 2 i 2023. I udgivelsesbølge 2 i 2023 er ny funktionalitet til E-dokumenter inkluderet. Du kan få mere at vide under [Konfiguration af e-dokumenter](finance-how-setup-edocuments.md). 


Som et alternativ til at sende vedhæftede filer i en mail, kan du sende og modtage forretningsdokumenter elektronisk. Med et elektronisk dokumentet menes en standard\-kompatibel fil, der repræsenterer et forretningsdokument, f.eks en faktura fra en kreditor, som kan modtages og konverteres til en købsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Udvekslingen af elektroniske forretningsdokumenter mellem to handelspartnere udføres af en ekstern udbyder af dokumentudvekslingstjenester. Den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter afsendelse og modtagelse af elektroniske fakturaer og kreditnotaer i PEPPOL-formatet, som understøttes af de største udbydere af dokumentudvekslingstjenester. En større udbyder af dokumentudvekslingstjenester er forudkonfigureret og klar til at blive konfigureret til din virksomhed.  

Fra PDF-filer eller billedfiler, der repræsenterer indgående bilag, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, som du derefter kan konvertere til bilagsposter i [!INCLUDE[prod_short](includes/prod_short.md)], på samme måde som for elektroniske PEPPOL-dokumenter. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra siden **Indgående bilag**. Efter nogle få sekunder får du filen tilbage som en elektronisk faktura, der kan konverteres til en købsfaktura for kreditoren. Hvis du sender filen til OCR-tjenesten via mail, oprettes en ny indgående bilagspost automatisk, når du får det elektroniske dokument tilbage igen.  

Det elektroniske dokumentformat **PEPPOL** er forudkonfigureret, så du kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-format. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, debitorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i felterne i [!INCLUDE[prod_short](includes/prod_short.md)] til elementer i den udgående dokumentfil. Endelig, skal du vælge formatet på siden **Elektronisk dokumentformat** for hver debitor, som du sender elektroniske PEPPOL-dokumenter til. Du kan finde flere oplysninger i [Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md).  

Dataudvekslingsdefinitionerne **PEPPOL - faktura** og **PEPPOL – kreditnota** er forudkonfigurerede, så du kan modtage elektroniske fakturaer og kreditnotaer i PEPPOL-formatet. Først skal du konfigurere forskellige stamdata, såsom firmaoplysninger, kreditorer, varer og enheder. Disse bruges til at identificere forretningspartnere og varer ved konvertering af data i elementerne i den indgående bilagsfil til felter i [!INCLUDE[prod_short](includes/prod_short.md)]. Endelig, skal du vælge dataudvekslingsdefinitionen på siden **Indgående bilag** for hvert indgående elektroniske dokument, du vil konvertere til et købsbilag i [!INCLUDE[prod_short](includes/prod_short.md)].  

Dataudvekslingsdefinitionen **OCR – faktura** er forudkonfigureret til at kunne modtage elektroniske dokumenter, der genereres af tjenesten OCR-tjenesten. For at kunne modtage f.eks. en faktura som et elektronisk OCR-dokument skal du konfigurere stamdata og derefter behandle dokumentet på samme måde, som når du modtager et elektronisk PEPPOL-dokument. Du kan finde flere oplysninger i [Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

Forudkonfigurerede tjenester til dokumentudveksling og OCR skal være aktiverede, før du sender eller modtager. Du kan finde flere oplysninger i [Konfigurere en dokumentudvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).  

Emnet indeholder følgende procedurer:  

* Sådan defineres regnskabet for afsendelse og modtagelse af elektroniske dokumenter  
* Sådan defineres momsbogføring for afsendelse og modtagelse af elektroniske dokumenter  
* Sådan defineres lande/områder for afsendelse og modtagelse af elektroniske dokumenter  
* Sådan defineres varer for afsendelse og modtagelse af elektroniske dokumenter  
* Sådan defineres måleenheder for afsendelse og modtagelse af elektroniske dokumenter  
* Sådan konfigureres kunder for afsendelse af elektronisk dokumenter  
* Sådan vælges elektronisk **PEPPOL**-dokumentformat for afsendelse af elektronisk dokumenter  
* Sådan konfigureres kreditorer for modtagelse af elektroniske dokumenter  
* Sådan vælges dataudvekslingsformatet **PEPPOL – faktura** for modtagelse af elektroniske dokumenter  
* Sådan konfigureres den finanskonto, der skal bruges på nye købsfakturalinjer, for ikke\-identificerbare varer og ikke\-varer  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Sådan defineres regnskabet for afsendelse og modtagelse af elektroniske dokumenter

1. I feltet **Søg** skal du indtaste **Virksomhedsoplysninger** og derefter vælge det relaterede link.  
2. På oversigtspanelet **Generelt** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Find din virksomhed.<br /><br /> F.eks, når du sender elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt til at udfylde elementet **EndPointID** i gruppen **AccountingSupplierParty**. Nummeret er baseret på GS1 standarden, der overholder ISO 6523.|  
    |**SE/CVR-nr.**|Angiv din virksomheds momsregistreringsnummer.|  
    |**Ansvarscenter**|Hvis din virksomhed er konfigureret med et ansvarscenter, skal du sørge for, at feltet **Lande-/områdekode** er udfyldt.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Sådan defineres momsbogføring for afsendelse og modtagelse af elektroniske dokumenter

1. I feltet **Søg** skal du skrive **Momsbogf.opsætning** og derefter vælge det relaterede link.  
2. For hver momsbogføringslinje, du vil bruge til elektroniske dokumenter, skal du udfylde feltet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Momskategori**|Angiv momskategori.<br /><br /> F.eks, når du sender elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt til at udfylde elementet **TaxApplied** i gruppen **AccountingSupplierParty**. Nummeret er baseret på UNCL5305 standarden.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Sådan defineres lande/områder for afsendelse og modtagelse af elektroniske dokumenter

1. I feltet **Søg** skal du indtaste **Lande/områder** og derefter vælge det relaterede link.  
2. For hvert land/område, du vil udveksle elektroniske dokumenter med, skal du udfylde feltet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Momsskema**|Identificer den nationale myndighed, der udsteder CVR-nummeret for land\/området i forbindelse med afsendelse af elektronisk dokumenter.<br /><br /> F.eks når du sender elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt til at udfylde attributten **SchemeID** for elementet **EndPointID** både under noden **AccountingSupplierParty** og **AccountingCustomerParty** i filen.<br /><br /> Feltet **Momsskema** bruges kun, hvis feltet **GLN** på siden **Virksomhedsoplysninger** ikke er udfyldt. **Bemærk:** Værdien i feltet **Kode** på siden **Lande\/områder** skal overholde ISO 3166\-1:Alpha2.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Sådan defineres varer for afsendelse og modtagelse af elektroniske dokumenter

1. I feltet **Søg** skal du indtaste **Varer** og derefter vælge det relaterede link.  
2. For hver vare, du køber eller sælger i elektroniske dokumenter, skal du udfylde feltet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identificerer varen i forbindelse med afsendelse og modtagelse af elektronisk dokument. For PEPPOL-format bruges feltet på følgende måde:<br /><br /> Hvis **SchemeID**-attributten for **StandardItemIdentification\/ID**-elementet er indstillet til **GTIN**, knyttes elementet til feltet **GTIN** på varekortet.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Sådan defineres måleenheder for afsendelse og modtagelse af elektroniske dokumenter

1. Indtast **Enhed** i feltet **Søg**, og vælg derefter det relaterede link.  
2. For hver måleenhed, du vil bruge til varer i elektroniske dokumenter, skal du udfylde feltet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**International standardkode**|Angiv enhedskoden, udtrykt i overensstemmelse med UNECERec20 standarden i forbindelse med afsendelse af elektroniske dokumenter.<br /><br /> Når du sender elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt f.eks. til at udfylde attributten **unitCode** i elementet **InvoicedQuantity** under noden **InvoiceLine**. **Bemærk:** Hvis feltet **Enhed** på salgslinjen er tomt, indsættes standardværdien UNECERe20 for "Styk" \(H87\) som standard. Du kan finde flere oplysninger og en liste over gyldige enhedskoder i [Anbefaling nr. 20 \- Enheder i international handel](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Sådan konfigureres kunder for afsendelse af elektronisk dokumenter

1. I feltet **Søg** skal du indtaste **Debitorer** og derefter vælge det relaterede link.  
2. For hver debitor, du vil sende elektroniske dokumenter til, skal du udfylde felter som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificer debitoren.<br /><br /> F.eks, når du sender elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt til at udfylde elementet **EndPointID** i noden **AccountingCustomerParty**. Nummeret er baseret på GS1 standarden, der overholder ISO 6523.<br /><br /> Hvis feltet **GLN** er tomt, anvendes værdien i feltet **SE/CVR-nr**.|  
    |**SE/CVR-nr.**|Angiv debitorens momsregistreringsnummer. **Tip:** I understøttede lokaliserede versioner skal du vælge knappen Specificer for at bruge den webtjeneste, der kontrollerer, om nummeret findes i det nationale virksomhedsregister.|  
    |**Ansvarscenter**|Hvis debitoren er konfigureret med et ansvarscenter, skal du sørge for, at feltet **Lande-/områdekode** er udfyldt.|  

    Du kan konfigurere hver debitor med en foretrukken metode til afsendelse af forretningsdokumenter, så du ikke behøver at vælge en afsendelsesindstilling, hver gang du sender et dokument til debitoren. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>Sådan vælges elektronisk PEPPOL-dokumentformat for afsendelse af elektroniske dokumenter
1. I feltet **Søg** skal du indtaste **Profiler for afsendelse af dokumenter** og derefter vælge det relaterede link.  
2. Åbn den eksisterende dokumentafsendelsesprofil, eller opret en ny. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  
3. På siden **Dokumentafsendelsesprofil** skal du vælge **Elektronisk format**, vælge linjen for PEPPOL og derefter vælge **OK**.  
4. I feltet **Elektronisk dokument** skal du vælge **Ja (Via dokumentudvekslingstjeneste)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] registrerer automatisk, om dokumentet er en faktura eller kreditnota, og anvender PEPPOL-formatet i overensstemmelse hermed.  

5. For at gøre dokumentafsendelsesprofilen gældende for alle debitorer, skal du markere afkrydsningsfeltet **Standard** på oversigtspanelet **Generelt**. For at gøre det gældende for bestemte debitorer, skal du udfylde feltet **Dokumentafsendelsesprofil** på de relevante debitorkort. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).  

    Du kan nu sende det elektroniske dokument med de konverterede data. Du kan finde flere oplysninger i [Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Sådan konfigureres kreditorer for modtagelse af elektroniske dokumenter
1. I feltet **Søg** skal du angive **Leverandører** og derefter vælge det relaterede link.  
2. For hver kreditor, du vil modtage elektroniske dokumenter fra, skal du udfylde felter som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificer kreditoren.<br /><br /> F.eks, når du modtager elektroniske fakturaer i PEPPOL-format, bruges værdien i dette felt til at udfylde elementet **EndPointID** i gruppen **AccountingSupplierParty**. Nummeret er baseret på GS1 standarden, der overholder ISO 6523.<br /><br /> Hvis feltet **GLN** er tomt, anvendes værdien i feltet **SE/CVR-nr**.|  
    |**SE/CVR-nr.**|Angiv kreditorens momsregistreringsnummer. **Tip:** I understøttede lokaliserede versioner skal du vælge knappen Specificer for at bruge den webtjeneste, der kontrollerer, om nummeret findes i det nationale virksomhedsregister.|  
    |**Ansvarscenter**|Hvis kreditoren er konfigureret med et ansvarscenter, skal du sørge for, at feltet **Lande-/områdekode** er udfyldt.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>Sådan vælges dataudvekslingsformatet PEPPOL – faktura for modtagelse af elektroniske dokumenter
1. I feltet **Søg** skal du skrive **Indgående bilag** og derefter vælge det relaterede link.  
2. På linjen for det elektronisk dokument, du vil modtage og konvertere, skal du vælge feltet **Dataudvekslingstype** og vælge **PEPPOLINVOICE**.  

     Hvis dokumentet, der skal modtages, er en kreditnota, skal du vælge **PEPPOLCREDITMEMO**.  

    Nu kan du modtage det elektroniske dokument ved at starte datakonverteringsprocessen på siden **Indgående bilag**. Du kan finde flere oplysninger i [Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>Sådan konfigureres den finanskonto, der skal bruges på nye købsfakturalinjer, for varer, der ikke kan identificeres, og ikke-varer
1. I feltet **Søg** skal du indtaste **Købsopsætning** og derefter vælge det relaterede link.  
2. På oversigtspanelet **Standardkonti** skal du udfylde feltet som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Finanskonto til ikke-varelinjer**|Angiver den finanskonto, der indsættes automatisk på indkøbslinjer, der er oprettet fra elektroniske dokumenter, når den indgående bilagslinje ikke indeholder en vare, der kan identificeres. En indgående bilagslinje, der ikke har en GTIN eller kreditors varenummer, konverteres til en købslinje af typen **Finanskonto**, og feltet **Nr.** på købslinjen vil indeholde den konto, som du vælger i feltet **Finanskonto til ikke-varelinjer**.<br /><br /> Hvis du lader feltet **Finanskonto til ikke-varelinjer** stå tomt, og det indgående bilag indeholder linjer uden identificerbare varer, bliver indkøbsdokumentet ikke oprettet. En fejlmeddelelse beder dig om at udfylde feltet **Finanskonto til ikke-varelinjer**, inden du kan udføre opgaven.|  

## <a name="see-also"></a>Se også
[Udveksle data elektronisk](across-data-exchange.md)   
[Fakturere salg](sales-how-invoice-sales.md)   
[Registrere køb](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
