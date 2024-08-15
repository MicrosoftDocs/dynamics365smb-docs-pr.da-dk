---
title: SEPA-direkte debitering i Business Central
description: Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Indsaml betalinger med SEPA Direct Debit

Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.  

Opret først eksportformatet for bankfilen, der instruerer din bank i at udføre en Direct Debit. Derefter konfigureres kundens betalingsform. Til sidst oprettes den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om bankkonti, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Derefter eksporterer du en XML-fil, der er baseret på opkrævningsposten, som du sender til din bank til behandling. Alle betalinger, der ikke kunne behandles, vil blive meddelt dig af din bank, og du skal derefter manuelt afvise de pågældende poster med opkrævning af direkte debitering.  

Du kan angive standarddebitorsalgskoder med oplysninger om Direct Debit-betalingsform og -bemyndigelse. Du kan derefter bruge kørslen **Opret standardkundefakturaer** til at generere flere salgsfakturaer med oplysninger om Direct Debit udfyldt på forhånd. Dette kan udføres manuelt eller automatisk, alt efter betalingens forfaldsdato.  

Når betalingerne er behandlet, som meddelt af din bank, kan du bogføre betalingskvitteringerne enten direkte fra **Direct Debit Collect. Siden Poster** eller ved at flytte betalingslinjerne til den kladde, hvor du bogfører betalingskvitteringer, f.eks. siden **Indbetalingskladder** . Alternativt kan du, afhængigt af hvordan din likviditetsstyring foregår, vente og kun anvende betalingerne som en del af bankafstemningen.  

> [!NOTE]  
> Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

## Sådan konfigurerer du SEPA Direct Debit

Fra siden **Direct Debit-opkrævninger** kan du eksportere instruktioner til din netbank for at udføre en direkte debiteringsopkrævning fra debitorens bankkonto til din bankkonto ifølge SEPA Direct Debit-format.

> [!NOTE]
> Den globale version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter kun SEPA-debetformatet. Versionen for dit land/område kan understøtte andre formater til elektronisk betaling. Se under **Lokal funktionalitet** i indholdsfortegnelsen.  

Hvis du vil aktivere eksport af et bankfilformat, der ikke understøttes som standard [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurere en dataudvekslingsdefinition ved hjælp af dataudvekslingsstrukturen. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle debitorbetalinger elektronisk ved eksport af instruktioner for direkte debitering i SEPA Direct Debit-format, skal du udføre følgende konfigurationstrin:  

* Konfigurer eksportformatet for den bankfil, der instruerer din bank i at udføre en Direct Debit-opkrævning fra kundens bankkonto til din bankkonto.  
* Konfigurer debitorens betalingsform.  
* Konfigurer den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

### Sådan konfigurerer du din bankkonto til SEPA Direct Debit

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.  
2. Åbn den bankkonto, du vil bruge til Direct Debit.  
3. Vælg indstillingen **SEPA Direct Debit i feltet** SEPA Direct Debit Exp. Format **i oversigtspanelet Generelt** .  

### Sådan konfigureres debitorens betalingsmetode for SEPA Direct Debit

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsformer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Definer en betalingsform. Udfyld de Direct Debit\-specifikke felter som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angiv, om betalingsmetoden er til SEPA Direct Debit-opkrævning.|  
    |**Kode for Direct Debit-betalingsbetingelser**|Angiv de betalingsbetingelser, f.eks. BETAL IKKE, der vises på salgsfakturaer, der betales med SEPA Direct Debit, for at indikere over for kunden, at betalingen opkræves automatisk. Alternativt kan du lade feltet være tomt.|  

    > [!NOTE]  
    >  Angiv ikke en værdi i feltet **Kontonr.**.  

4. Vælg knappen **OK** for at lukke siden **Betalingsformer**.  
5. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
6. Åbn kort for den debitor, du vil konfigurere til SEPA Direct Debit-opkrævning.  
7. Vælg feltet **Betalingsformskode**, og vælg derefter den betalingsformskode, du har angivet i trin 3.  
8. Gentag trin 6 og 7 for alle debitorer, som du vil konfigurere til SEPA Direct Debit-opkrævning.  

#### Sådan konfigureres den Direct Debit-betalingsaftale, der repræsenterer kundeaftalen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2. Åbn kort for den debitor, du vil konfigurere til SEPA Direct Debits.  
3. Vælg handlingen **Bankkonti**.  
4.  **På siden Debitorbankkontooversigt** skal du vælge den debitorbankkonto, der skal bruge direkte debiteringer, og derefter vælge handlingen **Direkte debiteringsmandater** fra **Ny**.  
5. På siden **SEPA Direct Debit-betalingsaftaler** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Debitors bankkontokode**|Angiver den bankkonto, hvorfra der opkræves Direct Debit\-betalinger. Dette felt udfyldes automatisk.|  
    |**Gyldig fra**|Angiv den dato, hvor Direct Debit\-betalingsaftalen starter.|  
    |**Gyldig til**|Angiv den dato, hvor Direct Debit\-betalingsaftalen slutter.|  
    |**Underskriftsdato**|Angiv den dato, når kunden har underskrevet Direct Debit\-betalingsaftalen.|  
    |**Betalingstype**|Angiv, om aftalen dækker flere (**Tilbagevendende betaling**) eller en enkelt (**Engangsbetaling**) Direct Debit-opkrævning.|  
    |**Forventet antal debiteringer**|Angiv, hvor mange Direct Debit-opkrævninger du forventer at foretage. Dette felt er kun relevant, hvis du har markeret **Tilbagevendende betaling** i feltet **Betalingstype**.|  
    |**Debettæller**|Angiver, hvor mange Direct Debit\-opkrævninger, der er foretaget ved hjælp af denne Direct Debit\-betalingsaftale. Dette felt opdateres automatisk.|  
    |**Spærret**|Angiv, at opkrævninger via direkte debitering ikke kan foretages ved hjælp af dette mandat til direkte\- debitering.|  

6. Gentag trin 1 til og med 5 for alle debitorer, du vil konfigurere til SEPA Direct Debits.  

 Direct Debit-betalingsaftalen indsættes automatisk i feltet **Id for Direct Debit-betalingsaftale**, når du opretter en salgsfaktura til den debitor, som du valgte i trin 2. Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).

## Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil

For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om kundens bankkonto, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Fra posten i den direkte debiteringsopkrævning, som fås som resultat, kan du derefter eksportere en XML-fil, som du sender eller overfører til din elektroniske bank til behandling. Alle betalinger, der ikke kunne behandles af banken, vil blive meddelt dig af din bank, og du skal derefter manuelt afvise de pågældende poster med direkte debitering.  

 > [!NOTE]  
 > Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

### Sådan oprettes en direkte debiteringsopkrævning  

 1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.  
 2. På siden **Direct Debit-opkrævninger** skal du vælge handlingen **Opret Direct Debit-opkrævning**.  
 3. På siden **Opret Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Fra forfaldsdato**|Angiv den tidligste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Til forfaldsdato**|Angiv den seneste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Partnertype**|Angiver, om der foretages direkte debiteringsopkrævning for debitorer af typen **Virksomhed** eller **Person**.|  
    |**Kun kunder med gyldig bemyndigelse**|Angiv, om der oprettes en Direct Debit-opkrævning for debitorer, der har en gyldig Direct Debit-betalingsaftale. **Bemærk: Der oprettes en opkrævning af direkte debitering,**   selvom feltet Fuldmagts-id **for** direkte debitering ikke er udfyldt på salgsfakturaen.|  
    |**Kun fakturaer med gyldig betalingsaftale**|Angiv, om der kun oprettes en Direct Debit-opkrævning for salgsfakturaer, hvis der er valgt en gyldig Direct Debit-betalingsaftale i feltet **Id for Direct Debit-betalingsaftale** på salgsfakturaen.|  
    |**Bankkontonr.**|Angiv, hvilke af firmaets bankkonti den opkrævede betaling skal overføres til fra debitors bankkonto.|  
    |**Bankkontonavn**|Angiver navnet på den bankkonto, som du vælger i feltet **Bankkontonr.**. Dette felt udfyldes automatisk.|  

 4. Vælg knappen **OK**.  

Der føjes en Direct Debit-opkrævning til siden **Direct Debit-opkrævninger**, og der oprettes en eller flere poster med Direct Debit-opkrævning.  

### Sådan eksporteres en post i en direkte debiteringsopkrævning til en bankfil

 1. På siden **Direct Debit-opkrævninger** skal du vælge handlingen **Poster i Direct Debit-opkrævning**.  
 2. På siden **Poster i Direct Debit-opkrævning** skal du markere den post, du vil eksportere, og derefter vælge handlingen **Opret fil til Direct Debit**.  
 3. Gem eksportfilen på det sted, hvorfra du sender eller overfører den til din elektroniske bank.  

      På siden **Poster i Direct Debit-opkrævning** ændres feltet **Status for Direct Debit-opkrævning** til Fil oprettet. På siden **SEPA Direct Debit-betalingsaftaler** opdateres feltet **Debettæller** med et styk.  

 Hvis den eksporterede fil ikke kan behandles, f.eks. fordi kunden er insolvent, kan du afvise posten med opkrævning via direkte debitering. Hvis den eksporterede fil er blevet behandlet af banken, opkræves forfaldne betalinger for de involverede salgsfakturaer automatisk fra de berørte debitorer. I så fald kan du lukke opkrævningen.  

### Sådan afvises en post i en direkte debiteringsopkrævning  

*  **På direkte debitering indsamle.** Vælg den post, der ikke blev behandlet, og vælg derefter handlingen **Afvis post** .  

    På siden **Poster i Direct Debit-opkrævning** ændres feltet **Status** til **Afvist**.  

### Sådan lukkes en direkte debiteringsopkrævning

* På siden **Poster i Direct Debit-opkrævning** skal du markere den post, der ikke blev behandlet korrekt, og derefter vælge handlingen **Luk opkrævning**.  

    Den relaterede direkte debiteringsopkrævning er lukket.  

 Du kan nu fortsætte med at bogføre kvitteringer for betalinger for de involverede salgsfakturaer. Du kan gøre dette, mens du typisk bogfører betalingskvitteringer, f.eks. på siden **Betalingsregistrering**, eller du kan bogføre de relaterede betalingskvitteringer direkte fra siden **Poster i Direct Debit-opkrævning**. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

## Bogføring af SEPA Direct Debit-betalingskvitteringer

Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer. Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Du kan bogføre betalingskvitteringen direkte fra siden **Direct Debit-opkrævninger** eller siden **Poster i Direct Debit-opkrævning**. Alternativt kan du overføre arbejdet til en anden bruger ved at udarbejde de relaterede kladdelinjer.  

### Sådan bogføres en betalingskvittering i Direct Debit fra siden Direct Debit-opkrævninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.  
2. Vælg en linje for en Direct Debit-opkrævning, der er eksporteret til en bankfil og er blevet behandlet af banken.
3. Vælg handlingen **Bogfør betalingskvitteringer**.  
4. På siden **Bogfør Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit-opkrævningsnr.**|Angiv den Direct Debit-samling, som du vil bogføre betalingskvittering for.|  
    |**Finanskladdetype**|Angiv, hvilken finanskladdeskabelon der skal bruges til bogføring af betalingskvitteringen, f.eks. skabelonen til indbetalinger.|  
    |**Finanskladdenavn**|Angiv, hvilket finanskladdenavn der skal bruges til bogføring af betalingskvitteringen.|  
    |**Opret kun kladde**|Marker dette afkrydsningsfelt, hvis du ikke vil bogføre betalingskvitteringen, når du vælger **knappen OK** . Betalingskvitteringen udarbejdes i den angivne kladde og bogføres først, når nogen bogfører de pågældende kladdelinjer.|  

5. Vælg knappen **OK**.

## Se også

[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Service Management](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
