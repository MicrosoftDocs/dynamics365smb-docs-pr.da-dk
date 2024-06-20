---
title: Bruge udvidelsen C5-dataoverførsel | Microsoft Docs
description: 'Du kan bruge denne udvidelse til at overføre debitorer, kreditorer, varer og omkostninger på finanskonti fra Microsoft Dynamics C5 2012 til Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'extension, migrate, data, C5, import'
ms.search.form: '1860, 1861, 1862, 1863, 1864, 1867, 1868, 1869, 1874, 1882, 1883, 1884, 1885, 1886, 1888, 1890, 1891, 1892, 1893, 1894, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906'
ms.date: 12/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-c5-data-migration-extension"></a>Udvidelsen C5-dataoverførsel

Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan også overføre gamle poster for finanskonti.

> [!NOTE]
> Virksomheden i [!INCLUDE[prod_short](includes/prod_short.md)] må ikke indeholde data. Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.

## <a name="what-data-is-migrated"></a>Hvilke data overføres?

Følgende data overføres for hver enhed:

### <a name="customers"></a>Kunder

* Kontakter  
* Sted
* Land/område
* Kundedimensioner (afdeling, arbejdscenter og formål)
* Leveringsform
* Sælger
* Betalingsbetingelser
* Betalingsform
* Debitorprisgruppe
* Debitorfakturarabat

Hvis du overfører konti, overføres følgende data også:

* Opsætning for debitorbogføring
* Finanskladdenavn
* Åbne transaktioner (debitorposter)

### <a name="vendors"></a>Leverandører (Kreditorer)

* Kontakter
* Sted
* Land/område
* Kreditordimensioner (afdeling, arbejdscenter og formål)
* Fakturarabat
* Leveringsform
* Indkøber
* Betalingsbetingelser
* Betalingsform
* Kreditorfakturarabat

Hvis du overfører konti, overføres følgende data også:

* Opsætning af kreditorbogføring
* Finanskladdenavn
* Åbne transaktioner (kreditorposter)

### <a name="items"></a>Varer

* Sted
* Land
* Varedimensioner (afdeling, arbejdscenter og formål)
* Salgslinjerabatter
* Debitorrabatgrupper
* Varerabatgrupper
* Salgspris
* Tarifnummer
* Enheder
* Varesporingskode
* Debitorprisgruppe
* Montagestyklister

Hvis du overfører konti, overføres følgende data også:

* Opsætning af lagerbogføring
* Bogføringsopsætning
* Varekladdenavn
* Åbne transaktioner (vareposter)

> [!NOTE]
> Hvis der er åbne transaktioner, der bruger udenlandske valutaer, overføres valutakursen også for disse valutaer. Andre valutakurser overflyttes ikke.

### <a name="chart-of-accounts"></a>Kontoplan

* Standarddimensioner: afdeling, omkostningssted og formål  
* Historiske finanstransaktioner  

> [!NOTE]
> Historisk finanstransaktioner behandles lidt anderledes. Når du overfører data, angiver du en **Nuværende periode**-parameter. Denne parameter angiver, hvordan du skal behandle finanstransaktioner. Transaktioner efter denne dato overføres enkeltvis. Transaktioner inden denne dato lægges sammen pr. konto og overføres som et enkelt beløb. Lad os antage, at der er transaktioner i 2015, 2016, 2017, 2018, og du angiver den 1. januar 2017 i feltet Nuværende periode. For hver konto samles beløb for alle transaktioner på eller før den 31. december 2106 på en enkelt finanskladdelinje for hver finanskonto. Alle transaktioner efter denne dato overføres enkeltvist.

## <a name="file-size-requirements"></a>Krav til størrelsen af filer

Den største filstørrelse, du kan overføre til [!INCLUDE[prod_short](includes/prod_short.md)], er 150 MB. Hvis filen, du eksporterer fra C5, er større end det, kan du overveje at overføre data i flere filer. Eksporter f.eks. en eller to typer objekter fra C5, f.eks. kunder og leverandører, til en fil, og eksporter derefter elementer til en anden fil osv. Du kan importere filer individuelt i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-migrate-data"></a>Sådan overføres data

Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene. Send derefter eksportmappen til en komprimeret (zippet) mappe.  
2. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du vælge ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Dataoverførsel**, og vælg derefter **Dataoverførsel**.  
3. Udfør trinnene i guiden til assisteret opsætning. Sørg for at vælge **Indlæs fra Microsoft Dynamics C5 2012** som datakilde.  

## <a name="viewing-the-status-of-the-migration"></a>Få vist status for overførslen

Brug siden **Dataoverførselsoversigt** til at overvåge status for overførslen. Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket. Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne. Du kan finde flere oplysninger i næste afsnit i denne artikel.  

> [!NOTE]
> Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.

## <a name="how-to-avoid-double-posting"></a>Sådan undgås dobbeltbogføring

For at undgå dobbeltbogføring i finansregnskabet bruges følgende modkonti til åbne posteringer:  

* For kreditorer bruger vi kreditorkontoen fra kreditorbogføringsgruppen.  
* For debitorer bruger vi debitorkontoen fra debitorbogføringsgruppen.  
* For varer opretter vi en bogføringsopsætning, hvor reguleringskontoen er den konto, der er angivet som lagerkontoen i varebogføringsopsætningen.  

## <a name="correcting-errors"></a>Rette fejl

Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange. For at få vist en liste over fejlene, kan du åbne siden **Dataoverførselsfejl** side ved at vælge:  

* Nummeret i feltet **Antal fejl** for enheden.  
* Enheden og derefter handlingen **Vis fejl**.  

På siden **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse og derefter vælge **Rediger post** for at få vist de overførte data for objektet. Hvis du har flere fejl, der skal løses, kan du vælge **Fejl flere fejl ad gangen** for at redigere objekter på en liste. Du skal stadig åbne de individuelle poster, dog kun hvis fejlen blev forårsaget af en relateret post. F.eks. overføres en leverandør ikke, hvis en e-mailadresse for en af leverandørens kontakter har et ugyldigt format.

Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.  

> [!TIP]
> Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres. Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.

> [!NOTE]
> Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den. Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.  

## <a name="verifying-data-after-migrating"></a>Kontrol af data efter overførsel

En måde til at kontrollere, at dine data overføres korrekt, er ved at se på følgende sider i C5 og [!INCLUDE[prod_short](includes/prod_short.md)].

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Den kørsel, der skal bruges |
|---------------------------|------------------------------|------------------|
|Debitorposter| Finanskladder| CUSTMIGR |
|Kreditorposter| Finanskladder| VENDMIGR|
|Vareposter| Varekladder| ITEMMIGR |
|Finansposter| Finanskladder| GLACMIGR |

## <a name="stopping-data-migration"></a>Stoppe dataoverførslen

Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**. Hvis du gør det, stoppes alle ventende overførsler også.

## <a name="see-also"></a>Se også

[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Blive køreklar](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
