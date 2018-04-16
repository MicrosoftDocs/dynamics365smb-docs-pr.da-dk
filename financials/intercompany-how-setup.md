---
title: "Konfigurere bogføring af koncernintern transaktion | Microsoft Docs"
description: "Opret koncerninterne kreditorer og debitorer som såkaldte koncerninterne partnere, og konfigurer en koncernintern (IC) kontoplan."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7a23f0ba28ab4c7bc9e028375246ea2e57d32764
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-intercompany"></a>Konfigurere mellemregning
Når du vil sende en transaktion (f.eks. en salgskladde) fra én virksomhed og få den tilsvarende transaktion (f.eks. en købskladdelinje) oprettet automatisk i partnervirksomheden, skal de involverede virksomheder enes om en fælles kontoplan og et sæt dimensioner, som skal anvendes i koncerninterne transaktioner. Intercompany-kontoplanen kan f.eks. være en forenklet udgave af moderselskabets kontoplan. Hver virksomhed knytter deres samlede kontoplan til den delte intercompany-kontoplan, og hver virksomhed knytter deres dimensioner til intercompany-dimensionerne.  

Du skal også oprette en koncernintern partnerkode for hver partnervirksomhed, der er aftalt mellem alle virksomheder, og derefter tildele dem til henholdsvis debitor- og kreditorkort ved at udfylde feltet **Koncernintern partnerkode**.  

Hvis du vil oprette eller modtage koncerninterne linjer med varer, kan du enten bruge egne varenumre, eller du kan angive partnerens varenumre for hver relevant vare. Brug enten feltet **Leverandørs varenr.** eller **Fælles varenr.** på varekortet. Du kan også bruge funktionen **Varereference**: Hvis du vil knytte dine varenumrene til dine koncerninterne partneres varebeskrivelser, skal du åbne kortet for hver vare og derefter vælge handlingen **Varereferencer** for at oprette krydsreferencer mellem dine varebeskrivelser og din koncerninterne partners.  

Hvis du skal foretage IC-salgstransaktioner, der omfatter ressourcer, skal du udfylde feltet **Finanskt.nr. for IC-partnerkøb** på ressourcekortet til hver relevant ressource. Det er nummeret på den IC-finanskonto, som prisen på denne ressource bogføres på i din partners virksomhed. Du kan finde flere oplysninger i .  

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Sådan konfigureres virksomheder til koncerninterne transaktioner
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.  
2. I vinduet **Virksomhedsoplysninger** skal du udfylde felterne **Koncernintern partnerkode**, **Koncernintern indbakketype** og **Koncerninterne indbakkeoplysninger**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Sådan konfigureres koncerninterne partnere
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne partnere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. I vinduet **Koncerninterne partnere** skal du udfylde felterne efter behov.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Sådan konfigureres koncerninterne kreditorer og koncerninterne debitorer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.
2. Du kan også få adgang til kreditoren fra feltet **Kreditornummer** i vinduet **Koncernintern partner**.
3. Åbn kortet for den kreditor, der er en koncernintern partner. Du kan finde flere oplysninger i [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).
4. I feltet **Koncernintern partnerkode** skal du vælge den relevante koncerninterne partnerkode.
5. Gentag trin 1 til 4 for debitorer.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Sådan konfigureres koncerninterne kontoplaner
Virksomhederne i en koncern skal på forhånd aftale, hvilken kontoplan der skal bruges som fælles reference, før de kan foretage IC-transaktioner. Du skal sammen med dine partnere aftale, hvilke kontonumre der skal anvendes, når I opretter IC-transaktioner. Moderselskabet i en koncern kan f.eks. oprette en forenklet version af deres egen kontoplan og udlæse denne IC-kontoplan fra databasen til en XML-fil, hvorefter den kan distribueres til hver virksomhed i koncernen.  

Hvis din virksomhed er moderselskabet og har den definerende koncerninterne kontoplan, som koncernen skal bruge som fælles reference, skal du følge proceduren: "Sådan konfigureres den koncerninterne kontoplan".  

Hvis din virksomhed er et datterselskab, og du modtager en XML-fil med den fælles koncerninterne kontoplan, skal du følge proceduren: ""Sådan indlæses den koncerninterne kontoplan"".  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Sådan konfigureres den definerende koncerninterne kontoplan
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **IC-kontoplan**, og vælg derefter det relaterede link.
2. I vinduet **Kontoplan** skal du angive hver konto på en linje i vinduet.  
3. Hvis den koncerninterne kontoplan skal være identisk med eller ligge tæt opad din almindelige kontoplan, kan du få udfyldt vinduet automatisk ved at vælge handlingen **Kopier fra kontoplan**. Du kan redigere nye linjer efter behov.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Sådan udlæses den koncerninterne kontoplan
Hvis dine koncerninterne partnere skal kunne indlæse den definerende kontoplan, skal du udlæse den til en fil.      
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **IC-kontoplan**, og vælg derefter det relaterede link.
2. I vinduet **IC-kontoplan** skal du vælge handlingen **Udlæs** og derefter vælge knappen **Gem**.
3. Angiv filnavnet og den placering, hvor du vil gemme XML-filen, og vælg derefter knappen **Gem**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Sådan indlæses IC-kontoplanen  
Når der findes en fil til den definerende koncerninterne kontoplan (IC-kontoplan), kan koncerninterne partnere indlæse den for at sikre, at de har de samme konti.  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **IC-kontoplan**, og vælg derefter det relaterede link.  
2. I vinduet **IC-kontoplan** skal du vælge handlingen **Indlæs**.  
3. Vælg XML-filens navn og placering, og vælg derefter knappen **Åbn**.  

Vinduet **IC-kontoplan** udfyldes med nye eller redigerede finanskontolinjer i overensstemmelse med den koncerninterne kontoplan i filen. Alle eksisterende, ikke-relaterede linjer i vinduet forbliver uændrede.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Sådan knyttes IC-kontoplanen til regnskabets kontoplan  
Når du har defineret eller indlæst den koncerninterne kontoplan, som du og dine koncerninterne partnere har aftalt at bruge, skal du knytte hver koncerninterne finanskonto til en af finanskontiene i dit regnskab. I vinduet **IC-kontoplan** angiver du, hvordan IC-finanskonti på indgående transaktioner skal oversættes til finanskonti i dit regnskabs kontoplan.

Hvis kontiene i den koncerninterne kontoplan har samme nummer som de tilsvarende konti i kontoplanen, kan du tildele kontiene automatisk.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **IC-kontoplan**, og vælg derefter det relaterede link.  
2. Marker de linjer, som du vil tilknytte automatisk, og væg derefter handlingen **Knyt til konto med samme nr.**.  
3. For hver IC-finanskonto, der ikke blev tilknyttet automatisk, skal du udfylde feltet **Finanskontonr. for tilknytning**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Sådan oprettes standardfinanskonti for IC-partnere  
Når du opretter en salgs- eller købslinje, der skal sendes som udgående IC-transaktion, angiver du en konto fra den koncerninterne kontoplan, hvor beløbet som standard bogføres på partnerens regnskab. I vinduet **Kontoplan** kan du for de konti, som du ofte bruger på udgående koncerninterne salgslinjer eller købslinjer, angive en standardfinanskonto for en koncernintern partner. Du kan f.eks. angive de tilsvarende samlekonti fra den koncerninterne kontoplan for samlekontiene i dit eget regnskab.  

Når du derefter angiver en finanskonto i feltet **Modkontonr.** på en koncernintern linje, hvor der står **Koncernintern partner** i feltet **Kontotype**, udfyldes feltet **Finanskonto for koncernintern partner** automatisk.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. På linjen for en finanskonto, der bruges til koncerninterne transaktioner, skal du i feltet **Standardfinanskonto for koncernintern partner** angive den IC-finanskonto, som partneren bogfører på, når du bogfører til finanskontoen på linjen.  
3. Gentag trin 3 for hver konto, som du ofte angiver i feltet **Modkontonr.** på en linje i en IC-kladde eller et IC-dokument.

## <a name="to-set-up-intercompany-dimensions"></a>Sådan konfigureres koncerninterne dimensioner
Før du og dine koncerninterne partnere vil kunne udveksle transaktioner med tilknyttede dimensioner, skal I aftale, hvilke dimensioner I alle skal bruge. Moderselskabet i en koncern kan f.eks. oprette en forenklet version af deres eget sæt dimensioner og udlæse disse IC-dimensioner fra databasen til en XML-fil, hvorefter den kan distribueres til hver virksomhed i koncernen. Datterselskaberne i koncernen kan derefter indlæse XML-filen i vinduet **Koncerninterne dimensioner** i deres eget regnskab og knytte de koncerninterne dimensioner her til dimensionerne i vinduet **Dimensioner**.  

Hvis din virksomhed er moderselskabet og har det definerende sæt koncerninterne dimensioner, som skal bruges i koncernen som fælles reference, skal du følge proceduren: "Sådan defineres koncerninterne dimensioner".

Hvis din virksomhed er et datterselskab, og du modtager en XML-fil med koncerninterne dimensioner, som skal bruges som fælles reference i koncernen, skal du følge proceduren: "Sådan indlæses koncerninterne dimensioner".

### <a name="to-define-the-intercompany-dimensions"></a>Sådan defineres koncerninterne dimensioner
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.  
2. Angiv hver dimension på en linje i vinduet **Koncerninterne dimensioner**.

    Hvis dine koncerninterne dimensioner skal være identiske med eller ligge tæt opad de eksisterende dimensioner i dit regnskab, kan du få udfyldt vinduet automatisk ved at klikke på **Kopier fra dimensioner**, hvorefter du kan redigere de indsatte linjer.  
3. Du kan udlæse de koncerninterne dimensioner til en XML-fil, så de kan distribueres til partnerne, ved at vælge handlingen **Udlæs**.  
4. Angiv filnavnet og den placering, hvor du vil gemme XML-filen, og vælg derefter knappen **Gem**.  

### <a name="to-import-the-intercompany-dimensions"></a>Sådan indlæses koncerninterne dimensioner  
Når der findes en fil til de definerende koncerninterne dimensioner, kan koncerninterne partnere indlæse den for at sikre, at de har de samme dimensioner.  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.  
2. I vinduet **Koncerninterne dimensioner** skal du vælge handlingen **Indlæs**.  
3. Angiv XML-filens navn og placering, og vælg derefter knappen **Åbn**.  

Linjerne i vinduerne **Koncerninterne dimensioner** og **Koncerninterne dimensionsværdier** indlæses.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Sådan knyttes IC-dimensioner til dimensioner i regnskabet
Når du har defineret eller importeret de dimensioner, som du og dine koncerninterne partnerne har aftalt at bruge, skal du knytte hver koncerninterne dimension til en af dimensionerne i dit eget regnskab og omvendt. I vinduet **Koncerninterne dimensioner** angiver du, hvordan koncerninterne dimensioner på indgående transaktioner skal oversættes til dimensioner fra din virksomheds liste over dimensioner. I vinduet **Dimensioner** angiver du, hvordan dine dimensioner skal oversættes til koncerninterne dimensioner på udgående transaktioner.

Hvis nogle af de koncerninterne dimensioner har samme kode som de tilsvarende dimensioner i listen over dimensioner i din egen virksomhed, kan du få programmet til automatisk at knytte dimensionerne sammen, og derefter kan du tilknytte kontiene automatisk.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.
2. I vinduet **Koncerninterne dimensioner** skal du markere de linjer, som du vil tilknytte automatisk, og derefter vælge handlingen **Knyt til dim. med samme kode**.
3. Udfyld feltet **Dim.kode for tilknytning** for hver IC-dimension, der ikke tilknyttes automatisk.
4. Vælg handlingen **Koncerninterne dimensionsværdier**.
5. Udfyld feltet **Dim.værdikode for tilknytning** i vinduet **Koncerninterne dimensionsværdier**.

    Fortsæt med at knytte dimensionerne til koncerninterne dimensioner ved at udføre lignende trin.
6. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dimensioner**, og vælg derefter det relaterede link.
7. I vinduet **Koncerninterne dimensioner** skal du markere de linjer, som du vil tilknytte automatisk, og derefter vælge handlingen **Knyt til IC-dim. med samme kode**.
8. Udfyld feltet **IC-dim.værdikode for tilknytn.** for hver koncerninterne dimension, der ikke tilknyttes automatisk.
9. Vælg handlingen **Koncerninterne dimensionsværdier**.
10. Udfyld feltet **IC-dim.værdikode for tilknytn.** i vinduet **Dimensionsværdier**.

## <a name="see-also"></a>Se også
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

