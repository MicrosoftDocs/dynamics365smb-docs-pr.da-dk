---
title: Brug af udvidelsen Betalinger og afstemninger (DK) | Microsoft Docs
description: "Udvidelsen gør det let at eksportere filer, der forud er formateret til at opfylde bankkravene til elektroniske afsendelser."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2a2fbae74dd5f6c401cfe8fa9b31c27e90a604b
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="the-payments-and-reconciliations-dk-extension"></a>Udvidelsen Betalinger og afstemninger (DK)
Foretag hurtige, fejlfrie betalinger ved at eksportere filer, der er formateret specielt til udveksling med dine kreditorer eller bank. Disse filer giver hurtigere betaling og afstemningsprocesser og fjerner fejl, der kan ske, når du manuelt angivet oplysningerne på en banks websted.  

Udvidelsen understøtter filformater for flere danske banker. Når du eksporterer betalingsoplysninger til en fil, pakker udvidelsen data til det format, der kræves af din bank. Formaterne omfatter f.eks. Bankdata-V3, BEC, SDC og FIK, som mange forskellige banker anvender, og nogle, der er mere specialiserede til visse banker, f.eks. Danske Bank og Nordea. Udvidelsen indeholder også nogle formater til at importere og afstemme bankkontoudtog.  

> [!Note]
> Hvis du vil bruge udvidelsen, skal du kende det format, som din bank eller leverandør kræver. Nogle banker eller leverandører angiver disse oplysninger på deres websted, men du skal muligvis kontakte deres kundeservice for at få oplysningerne.  

## <a name="supported-bank-formats"></a>Understøttede bankformater
Udvidelsen kan anvende følgende filformater for betalingsfiler:  

* BANKDATA V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK CMKV  
* DANSKEBANK CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Sådan konfigureres udvidelsen
Det kræver nogle trin at komme i gang.  

* Tillade eksport af betalingdata. For at beskytte dine data, er dette ikke umiddelbart tilgængeligt.  
* Konfigurer køb og skyldige beløb, så du ikke har brug for eksterne bilagsnumre på fakturaer. Hvis det er nødvendigt, kan du kan bruge referencenummeret til at referere til en bestemt faktura.  
* Angiv betalingsformen for hver kreditor. Betalingsformer definerer, hvordan du betaler fakturaer fra kreditoren. F.eks. Bank, Kontant, Check eller Konto.  
* Angiv den type format, der skal bruges til hver af dine bankkonti. F.eks. NORDEA, DANSKEBANK, SDC osv.  

Desuden skal du tildele kreditorer til en indenlandsk **Virksomhedsbogføringsgruppe** og en **Kreditorbogføringsgruppe**. Indstillingen land/område for kreditoren skal være Danmark (DK). Du kan finde flere oplysninger under [Konfigurere bogføringsgrupper](finance-posting-groups.md).  

### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a>Sådan tillader du [!INCLUDE[d365fin](includes/d365fin_md.md)] at eksportere betalingsdata
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladde**, og vælg derefter det relaterede link.  
2. I vinduet **Rediger udbetalingskladde** skal du vælge kørslen **Bank**.  
3. Vælg afkrydsningsfeltet **Tillad eksport af betaling**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Sådan angives en betalingsform for en kreditor
Følgende tabel viser de kombinationer af FIK- og GIRO betalingsformer, som [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter.

||Type 01 | Type 04 | Type 71 | Type 73 |
|----|---|---|---|---|
|Girokontonr. eller FIK-kreditornummer? | Girokontonr. | Girokontonr. | FIK-kreditornummer | FIK-kreditornummer|
|Tillader meddelelse til modtager? | Ja |Nej |Nej | Ja |
|Indeholder betalingsreferencenummer? | Nej | Ja, 16 cifre. | Ja, 15 cifre. | Nej|

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kreditorer**, og vælg derefter det relaterede link.  
2. Åbn kortet, udvid fanen **Betalinger** og vælg betalingsformen i feltet **Betalingsform**.  
3. Afhængigt af dit valg, skal du udfylde andre felter. Se overstående tabel for en beskrivelse af kombinationerne.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Sådan angives formatet, der skal bruges til en bankkonto
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bankkonti**, og vælg derefter det relaterede link.  
2. Åbn kortet for bankkontoen.  
3. I feltet **Format til eksport af betaling** skal du vælge formatet for udlæsningsfilen.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Vælg FIK- eller Giro-betalingsoplysningerne for kreditorfakturaer
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Vælg kreditoren. Husk, at det skal være en dansk kreditor med en adresse i Danmark.
3. Opret en faktura. Felterne **Betalingsform** og **Kreditornummer** udfyldes på basis af indstillinger på kreditorkortet. Du kan ændre dem, hvis du ønsker det.
4. I feltet **Betalingsreference** skal du angive tallet på 15 cifre fra kreditorfakturaen.  

    > [!Tip]
    > Du behøver kun at tilføje de sidste 11 cifre i nummeret. [!INCLUDE[d365fin](includes/d365fin_md.md)] tilføjer fire nuller i begyndelsen af nummeret.  

5. Bogfør fakturaen.

## <a name="to-use-the-extension-to-export-payment-data"></a>Så bruges udvidelsen til at eksportere betalingsdata
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Lav kreditorbetalingsforslagskladder**.  

    > [!Tip]
    > Hvis du kun vil udlæse specifikke betalinger, kan du bruge indstillingerne til at filtrere dataene.  

3. Hvis det er nødvendigt, kan du tilføje filtre for kun at eksportere specifikke betalinger.  
4. I feltet **Bankbetalingstype** skal du vælge **Elektronisk betaling**.  
5. Vælg handlingen **Eksportér**.  

## <a name="see-also"></a>Se også
[Tilpasse Business Central til [!INCLUDE[d365fin](includes/d365fin_md.md)] ved brug af udvidelser](ui-extensions.md)  
[Oprette poster i SEPA Direct Debit-opkrævning, og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)  
[Bogføre SEPA Direct Debit-betalingskvitteringer](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  

