---
title: Udvidelsen Betalinger og afstemninger (DK)
description: 'Udvidelsen gør det let at eksportere filer, der forud er formateret til at opfylde bankkravene til elektroniske afsendelser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, bank, formats'
ms.date: 06/24/2021
ms.author: bholtorf
---

# <a name="the-payments-and-reconciliations-dk-extension" />Udvidelsen Betalinger og afstemninger (DK)

Foretag hurtige, fejlfrie betalinger ved at eksportere filer, der er formateret specielt til udveksling med dine kreditorer eller bank. Disse filer giver hurtigere betaling og afstemningsprocesser og fjerner fejl, der kan ske, når du manuelt angivet oplysningerne på en banks websted.  

Udvidelsen understøtter filformater for flere danske banker. Når du eksporterer betalingsoplysninger til en fil, pakker udvidelsen data til det format, der kræves af din bank. Formaterne omfatter f.eks. Bankdata-V3, BEC, SDC og FIK, som mange forskellige banker anvender, og nogle, der er mere specialiserede til visse banker, f.eks. Danske Bank og Nordea. Udvidelsen indeholder også nogle formater til at importere og afstemme bankkontoudtog.  

> [!Note]
> Hvis du vil bruge udvidelsen, skal du kende det format, som din bank eller leverandør kræver. Nogle banker eller leverandører angiver disse oplysninger på deres websted, men du skal muligvis kontakte deres kundeservice for at få oplysningerne.  

## <a name="supported-bank-formats" />Understøttede bankformater
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

## <a name="to-set-up-the-extension" />Sådan konfigureres udvidelsen

Det kræver nogle trin at komme i gang.  

* Tillade eksport af betalingdata. For at beskytte dine data, er dette ikke umiddelbart tilgængeligt.  
* Konfigurer køb og skyldige beløb, så du ikke har brug for eksterne bilagsnumre på fakturaer. Hvis det er nødvendigt, kan du kan bruge referencenummeret til at referere til en bestemt faktura.  
* Angiv betalingsformen for hver kreditor. Betalingsformer definerer, hvordan du betaler fakturaer fra kreditoren. F.eks. Bank, Kontant, Check eller Konto.  
* Angiv den type format, der skal bruges til hver af dine bankkonti. F.eks. NORDEA, DANSKEBANK, SDC osv.  

Desuden skal du tildele kreditorer til en indenlandsk **Virksomhedsbogføringsgruppe** og en **Kreditorbogføringsgruppe**. Indstillingen land/område for kreditoren skal være Danmark (DK). Du kan finde flere oplysninger i [Konfigurere bogføringsgrupper](finance-posting-groups.md).  

### <a name="to-allow--to-export-payment-data" />Sådan tillader du [!INCLUDE[prod_short](includes/prod_short.md)] at eksportere betalingsdata

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladde**, og vælg derefter det relaterede link.  
2. På siden **Rediger udbetalingskladde** skal du vælge kørslen **Bank**.  
3. Vælg afkrydsningsfeltet **Tillad eksport af betaling**.  

### <a name="to-specify-a-payment-method-for-a-vendor" />Sådan angives en betalingsform for en kreditor

Følgende tabel viser de kombinationer af FIK- og GIRO betalingsformer, som [!INCLUDE[prod_short](includes/prod_short.md)] understøtter.

|Kombination|Type 01 | Type 04 | Type 71 | Type 73 |
|----|--------|---------|---------|---------|
|Girokontonr. eller FIK-kreditornummer? | Girokontonr. | Girokontonr. | FIK-kreditornummer | FIK-kreditornummer|
|Tillader meddelelse til modtager? | Ja |Nej |Nej | Ja |
|Indeholder betalingsreferencenummer? | Nej | Ja, 16 cifre. | Ja, 15 cifre. | Nr.|

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.  
2. Åbn kortet, udvid fanen **Betalinger** og vælg betalingsformen i feltet **Betalingsform**.  
3. Afhængigt af dit valg, skal du udfylde andre felter. Se overstående tabel for en beskrivelse af kombinationerne.  

### <a name="to-specify-the-format-to-use-for-a-bank-account" />Sådan angives formatet, der skal bruges til en bankkonto

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.  
2. Åbn kortet for bankkontoen.  
3. I feltet **Format til eksport af betaling** skal du vælge formatet for udlæsningsfilen.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices" />Vælg FIK- eller Giro-betalingsoplysningerne for kreditorfakturaer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Vælg kreditoren. Husk, at det skal være en dansk kreditor med en adresse i Danmark.
3. Opret en faktura. Felterne **Betalingsform** og **Kreditornummer** udfyldes på basis af indstillinger på kreditorkortet. Du kan ændre dem, hvis du ønsker det.
4. I feltet **Betalingsreference** skal du angive tallet på 15 cifre fra kreditorfakturaen.  

    > [!Tip]
    > Du behøver kun at tilføje de sidste 11 cifre i nummeret. [!INCLUDE[prod_short](includes/prod_short.md)] tilføjer fire nuller i begyndelsen af nummeret.  

5. Bogfør fakturaen.

## <a name="to-use-the-extension-to-export-payment-data" />Så bruges udvidelsen til at eksportere betalingsdata

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Lav kreditorbetalingsforslagskladder**.  

    > [!Tip]
    > Hvis du kun vil udlæse specifikke betalinger, kan du bruge indstillingerne til at filtrere dataene.  

3. Hvis det er nødvendigt, kan du tilføje filtre for kun at eksportere specifikke betalinger.  
4. I feltet **Bankbetalingstype** skal du vælge **Elektronisk betaling**.  
5. Vælg handlingen **Eksportér**.  

## <a name="see-also" />Se også

[Tilpasse Business Central til [!INCLUDE[prod_short](includes/prod_short.md)] ved brug af udvidelser](ui-extensions.md)  
[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
