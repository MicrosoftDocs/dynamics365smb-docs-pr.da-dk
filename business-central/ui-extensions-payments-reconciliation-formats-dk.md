---
title: Brug af udvidelsen Betalinger og afstemninger (DK) | Microsoft Docs
description: Udvidelsen gør det let at eksportere filer, der forud er formateret til at opfylde bankkravene til elektroniske afsendelser.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c8dd465213a9882a98c1ac1623d8a093f3eecb9a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757488"
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

### <a name="to-allow-prod_short-to-export-payment-data"></a>Sådan tillader du [!INCLUDE[prod_short](includes/prod_short.md)] at eksportere betalingsdata

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladde**, og vælg derefter det relaterede link.  
2. På siden **Rediger udbetalingskladde** skal du vælge kørslen **Bank**.  
3. Vælg afkrydsningsfeltet **Tillad eksport af betaling**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Sådan angives en betalingsform for en kreditor

Følgende tabel viser de kombinationer af FIK- og GIRO betalingsformer, som [!INCLUDE[prod_short](includes/prod_short.md)] understøtter.

|Kombination|Type 01 | Type 04 | Type 71 | Type 73 |
|----|--------|---------|---------|---------|
|Girokontonr. eller FIK-kreditornummer? | Girokontonr. | Girokontonr. | FIK-kreditornummer | FIK-kreditornummer|
|Tillader meddelelse til modtager? | Ja |Nej |Nej | Ja |
|Indeholder betalingsreferencenummer? | Nej | Ja, 16 cifre. | Ja, 15 cifre. | Nej|

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.  
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
    > Du behøver kun at tilføje de sidste 11 cifre i nummeret. [!INCLUDE[prod_short](includes/prod_short.md)] tilføjer fire nuller i begyndelsen af nummeret.  

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

[Tilpasse Business Central til [!INCLUDE[prod_short](includes/prod_short.md)] ved brug af udvidelser](ui-extensions.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
