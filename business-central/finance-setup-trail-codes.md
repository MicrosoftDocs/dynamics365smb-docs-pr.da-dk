---
title: Konfigurere koder for revisionsspor
description: 'Få mere at vide om de opgaver, der bruges til at oprette kilde- og årsagskoder, som du kan bruge til at spore revisionsspor.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails" />Oprette kilde- og årsagskoder til revisionsspor

Alle bogførte poster får automatisk tildelt en kildekode, så transaktioner kan spores til deres oprindelse. Hvis du vil knytte en supplerende kildekode til poster, kan du benytte årsagskoder. Årsagskoder kan bruges til at angive, hvorfor en post er oprettet. Når du har angivet årsagskoder, kan du tildele dem til hele anlægskladdetyper og kladder, og derefter kan du tildele dem til individuelle kladdelinjer og dokumenter.  

Brug koder, der er lette at huske, og som er beskrivende, til både kilde- og årsagskoder. Koden skal være entydig, og du kan oprette et ubegrænset antal koder.

## <a name="define-source-codes" />Definere kildekoder

Det kan være nyttigt at se, hvordan en bestemt post blev oprettet, f.eks. om posten blev oprettet ved bogføring af en finanskladde eller af en købsfaktura. En kildekode angiver, hvor en post er oprettet. Der oprettes poster, når kladder og fakturaer bogføres, og når visse kørsler udføres. Hver bogføringstype har en bestemt kildekode, der tilknyttes, når der oprettes individuelle poster.  

Når kladder, ordrer, fakturaer eller kreditnotaer bogføres, og når forskellige kørsler udføres, oprettes der poster i regnskabet. Siden **Kildekodedefinition** indeholder adskillige oversigtspaneler med en for hvert modul. Hvert oversigtspanel indeholder kildekoder, der kan anvendes til det pågældende område.

Når du bogfører eller udfører en kørsel, knyttes den korrekte kildekode automatisk til posten. Det vil sige, at når du f.eks. bogfører fra kassekladden, får posten koden *KASSEKLD*. Herefter kan du filtrere siden **Finansposter** for at se, hvilke poster der er bogført fra finanskladden eller fra salgsdokumenter, f.eks.

### <a name="to-define-source-codes" />Sådan defineres kildekoder

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, angiv **Kildekodedefinition** og derefter vælge det relaterede link.  

2. Angiv den relevante kildekode for hver bogføringstype og kørsel i vinduet **Kildekodedefinition**.  

Du kan ændre indholdet i et felt senere. Herefter vil ændringerne påvirke fremtidige bogføringer.

## <a name="change-source-codes" />Ændre kildekoder

Det kan være en fordel at ændre en kildekode. Lad os sige, at du vil ændre kildekoden *KASSEKLD* til *GNJ*.

### <a name="to-change-source-codes" />Sådan ændres kildekoder

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Varespor**, og vælg derefter det relaterede link.

2. Vælg den kode, der skal ændres, på den pågældende linje i feltet **Kode**.

3. Indtast den nye kode, og tryk derefter på knappen **Ja**. Du kan også ændre indholdet i feltet **Beskrivelse**.

Alle nye poster, der er bogført fra finanskladden, skal have en ny kildekode.

## <a name="define-reason-codes" />Definere årsagskoder

Årsagskoder supplerer kildekoder og bruges til at angive, hvorfor en post er oprettet. Du kan tildele årsagskoder i individuelle poster, og du kan tildele permanente koder i bestemte anlægskladder og kladder. Når en årsagskode er knyttet til en kladdelinje eller til købs- og salgshoveder, bliver alle posterne markeret med årsagskoder, når de bogføres.  

### <a name="to-set-up-reason-codes" />Sådan oprettes årsagskoder

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport")  ikon, skriv **revisionsspor**, og vælg derefter det relaterede link.

2. I vinduet **Årsagskoder** skal du indtaste den første kode i feltet **Kode**. Angiv en beskrivende tekst i feltet **Beskrivelse**.

Gentag denne fremgangsmåde for hver enkelt af de koder, du vil bruge. Du kan oprette et ubegrænset antal koder.

Følgende fremgangsmåde beskriver, hvordan du føjer en årsagskode til en kladdetype, men lignende trin gælder for tilføjelse af en årsagskode til en kladdelinje eller et kladdenavn.  

### <a name="to-assign-reason-codes-to-journal-templates" />Sådan knytter du årsagskoder til kladdetyper

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport")  ikon, skriv **Finanskladdetyper**, og vælg derefter det relaterede link.

2. Angiv den relevante kode i feltet **Årsagskode** på linjen med den valgte kladdetype.

3. Luk kladdetypen.

Den valgte årsagskode kopieres til nye kladdenavne, der er oprettet under denne kladdetype. Du kan knytte årsagskoder til kladdetyper i andre områder på samme måde.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents" />Sådan bruges årsagskoder i salgs- og købsdokumenter

1. Åbn det relevante salgs- eller købsdokument.

2. Angiv koden i feltet **Årsagskode** i salgs- eller købshovedet.

Når fakturaen er bogført, kopieres årsagskoden til hver finans-, debitor- og kreditorpost. Du kan ikke tilknytte forskellige årsagskoder til individuelle købs- og salgslinjer, fordi alle linjer er bogført som en post.

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Finans](finance.md)  
[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
