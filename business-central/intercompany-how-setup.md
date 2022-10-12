---
title: Konfigurere bogføring af koncernintern transaktion
description: Opret koncerninterne kreditorer og debitorer som såkaldte koncerninterne partnere, og konfigurer en koncernintern (IC) kontoplan.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.search.form: 605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 32a0005f2ebbc6bfc87c21fed8469c86535e15de
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607279"
---
# <a name="set-up-intercompany-transaction-posting"></a>Konfigurere bogføring af koncernintern transaktion

Koncerninterne bogføringer gør det lettere for to eller flere virksomheder at foretage en nemmere opgave for en centraliseret finansafdeling og koncerninterne partnervirksomheder. Når du vil sende en transaktion (f.eks. en salgskladde) fra én virksomhed og få den tilsvarende transaktion (f.eks. en købskladdelinje) oprettet automatisk i partnervirksomheden, skal de involverede virksomheder enes om en fælles kontoplan og et sæt dimensioner, som skal anvendes i koncerninterne transaktioner. Intercompany-kontoplanen kan f.eks. være en forenklet udgave af moderselskabets kontoplan. Hver virksomhed knytter deres samlede kontoplan til den delte intercompany-kontoplan, og hver virksomhed knytter deres dimensioner til intercompany-dimensionerne.  

Du skal også oprette en koncernintern partnerkode for hver [!INCLUDE [prod_short](includes/prod_short.md)] virksomhed, der er aftalt mellem alle virksomheder, og derefter tildele dem til henholdsvis debitor- og kreditorkort.  

Hvis du vil oprette eller modtage koncerninterne linjer med varer, kan du enten bruge egne varenumre, eller du kan angive partnerens varenumre for hver relevant vare. Brug enten feltet **Leverandørs varenr.** eller **Fælles varenr.** på varekortet. Du kan også bruge funktionen **Varereference** til at knytte dine varenumrene til dine koncerninterne partneres varebeskrivelser, skal du åbne kortet for hver vare og derefter vælge handlingen **Varereferencer** for at oprette krydsreferencer mellem dine varebeskrivelser og din koncerninterne partners. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md).

Hvis du skal foretage IC-salgstransaktioner, der omfatter ressourcer, skal du udfylde feltet **Finanskt.nr. for IC-partnerkøb** på ressourcekortet til hver relevant ressource. Det er nummeret på den IC-finanskonto, som prisen på denne ressource bogføres på i din partners virksomhed. Der er flere oplysninger i [Konfigurere ressourcer](projects-how-setup-resources.md).

> [!NOTE]
> Koncerninterne købstransaktioner, der omfatter ressourcer, anlægsaktiver og varegebyrer, understøttes ikke fuldstændigt. I den koncerninterne partnervirksomhed er feltet **Linhjetype** tomt på købsdokumentlinjer, som indeholder disse enheder. Du skal opdatere feltet manuelt.

## <a name="auto-accept-transactions-from-intercompany-partners"></a>Acceptér automatisk transaktioner fra IC-partnere

2022 udgivelsesbølge 1 har introduceret en ny side til **intern opsætning**, som gør det hurtigere at behandle transaktioner fra partnere. På siden kan du angive, om der automatisk oprettes kladdelinjer på baggrund af IC-partnernes indlæg fra **IC-finanskladde**-siden. Kladdelinjerne er oprettet til dig, men de er ikke bogført. Du kan bruge følgende felter på siden ny IC-opsætning til at angive, hvor de modtagne IC-kladdeposteringer skal oprettes:

* **Standardskabelon for koncerninterne finanskladder**
* **Koncernintern standardfinanskladde**

> [!NOTE]
> Hvis din organisation har brugt intercompany-funktioner i [!INCLUDE [prod_short](includes/prod_short.md)] før 2022 udgivelsesbølge 1, skal du aktivere funktionen **Acceptér automatisk IC-finanskladdetransaktioner** for automatisk at acceptere på siden **Funktionsstyring**.

## <a name="to-set-up-a-company-for-intercompany-transactions"></a>Sådan konfigureres en virksomhed til koncerninterne transaktioner

Disse felter, der skal udfyldes, afhængigt af, om din administrator har slået funktionsopdateringen **Ny vareprissætningsopdatering** til.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern konfiguration**, og vælg derefter det relaterede link.  
2. På siden **Koncernintern konfiguration** skal du udfylde følgende felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-intercompany-partners"></a>Opsæt koncerninterne partnere

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne partnere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Koncerninterne partnere** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gentag trin 2 og 3 for alle andre virksomheder, der er en del af denne koncerninterne opsætning.

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)] online kan du ikke bruge filplaceringer til at overføre transaktioner til partnerne, fordi [!INCLUDE[prod_short](includes/prod_short.md)] ikke har adgang til dit lokale netværk. Hvis du vælger **Filplacering** i feltet **Overførselstype**, er feltet **Mappesti** ikke tilgængeligt. I stedet bliver filen downloadet til mappen Overførsler på din computer. Derefter kan du sende filen til en person i partnervirksomheden, f.eks. via mail. Hvis du vil have en mere direkte proces, anbefales du at vælge **Mail** i stedet.

> [!NOTE]
> Når du har aktiveret funktionen til **automatisk accept af transaktioner** på siden **Intercompany-bogføring**, vises der en [!INCLUDE[prod_short](includes/prod_short.md)]-meddelelse om købsfakturaer, der duplikerer den oprindelige købsordre. Det er derfor vigtigt at have en forretningsproces til håndtering af dubletter. F.eks. ved at slette disse købsordrer, når købsfakturaen modtages fra IC-partneren.


## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Sådan konfigureres koncerninterne kreditorer og koncerninterne debitorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link.
2. Du kan også få adgang til kreditoren fra feltet **Kreditornummer** på siden **Koncernintern partner**.
3. Åbn kortet for den kreditor, der er en koncernintern partner. Du kan finde flere oplysninger i [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).
4. I feltet **Koncernintern partnerkode** skal du vælge den relevante koncerninterne partnerkode.
5. Gentag trin 1 til 4 for debitorer.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Sådan konfigureres koncerninterne kontoplaner

Virksomhederne i en koncern skal på forhånd aftale, hvilken kontoplan der skal bruges som fælles reference, før de kan foretage IC-transaktioner. Du skal sammen med dine partnere aftale, hvilke kontonumre der skal anvendes, når I opretter koncerninterne transaktioner. Moderselskabet i en koncern kan f.eks. oprette en forenklet version af deres egne kontoplaner, der derefter eksporteres til en XML-fil, der kan distribueres til hver virksomhed i koncernen.  

Hvis kontoplanen for din virksomhed definerer den koncerninterne kontoplan for partnervirksomheder, skal du følge proceduren, der er beskrevet i [Sådan konfigureres definition af den koncerninterne kontoplan](intercompany-how-setup.md#to-set-up-the-intercompany-chart-of-accounts).  

Hvis din virksomhed er et datterselskab, og du modtager en XML-fil med den fælles koncerninterne kontoplan, skal du følge proceduren: [Sådan importeres den koncerninterne kontoplan](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-intercompany-chart-of-accounts"></a>Konfigurere IC-kontoplanen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern kontoplan**, og vælg derefter det relaterede link.
2. På siden **Koncernintern kontoplan** skal du angive hver konto på en linje på siden.  
3. Hvis den koncerninterne kontoplan skal være identisk med eller ligge tæt opad din almindelige kontoplan, kan du få udfyldt siden automatisk ved at vælge handlingen **Kopier fra kontoplan**. Du kan redigere nye linjer efter behov.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Sådan udlæses den koncerninterne kontoplan

Hvis dine koncerninterne partnere skal kunne indlæse den definerende kontoplan, skal du udlæse den til en fil.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern kontoplan**, og vælg derefter det relaterede link.
2. På siden **Koncernintern kontoplan** skal du vælge handlingen **Udlæs** og derefter vælge knappen **Gem**.
3. Angiv filnavnet og den placering, hvor du vil gemme XML-filen, og vælg derefter knappen **Gem**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Sådan indlæses IC-kontoplanen  

Når der findes en fil til den definerende koncerninterne kontoplan (IC-kontoplan), kan koncerninterne partnere indlæse den for at sikre, at de har de samme konti.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern kontoplan**, og vælg derefter det relaterede link.  
2. På siden **Koncernintern kontoplan** skal du vælge handlingen **Indlæs**.  
3. Vælg XML-filens navn og placering, og vælg derefter knappen **Åbn**.  

Siden **IC-kontoplan** udfyldes med nye eller redigerede finanskontolinjer i overensstemmelse med den koncerninterne kontoplan i filen. Alle eksisterende, ikke-relaterede linjer på siden forbliver uændrede.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Sådan knyttes IC-kontoplanen til regnskabets kontoplan  

Når du har defineret eller indlæst den koncerninterne kontoplan, som du og dine koncerninterne partnere har aftalt at bruge, skal du knytte hver koncerninterne finanskonto til en af finanskontiene i dit regnskab. På siden **IC-kontoplan** angiver du, hvordan IC-finanskonti på indgående transaktioner skal oversættes til finanskonti i dit regnskabs kontoplan.

Hvis kontiene i den koncerninterne kontoplan har samme nummer som de tilsvarende konti i kontoplanen, kan du tildele kontiene automatisk.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncernintern kontoplan**, og vælg derefter det relaterede link.  
2. Marker de linjer, som du vil tilknytte automatisk, og væg derefter handlingen **Knyt til konto med samme nr.**.  
3. For hver IC-finanskonto, der ikke blev tilknyttet automatisk, skal du udfylde feltet **Finanskontonr. for tilknytning**.  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Sådan oprettes standardfinanskonti for IC-partnere  

Når du opretter en salgs- eller købslinje, der skal sendes som udgående IC-transaktion, angiver du en konto fra den koncerninterne kontoplan, hvor beløbet som standard bogføres på partnerens regnskab. På siden **Kontoplan** kan du for de konti, som du normalt bruger på udgående koncerninterne salgslinjer eller købslinjer, angive en standardfinanskonto for en koncernintern partner. Du kan f.eks. angive de tilsvarende samlekonti fra den koncerninterne kontoplan for samlekontiene i dit eget regnskab.  

Når du derefter angiver en finanskonto i feltet **Modkontonr.** på en koncernintern linje, hvor der står **Koncernintern partner** i feltet **Kontotype**, udfyldes feltet **Finanskonto for koncernintern partner** automatisk.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. På linjen for en finanskonto, der bruges til koncerninterne transaktioner, skal du i feltet **Standardfinanskonto for koncernintern partner** angive den IC-finanskonto, som partneren bogfører på, når du bogfører til finanskontoen på linjen.  
3. Gentag trin 2 for hver konto, som du ofte angiver i feltet **Modkontonr.** på en linje i en IC-kladde eller et IC-dokument.

## <a name="to-set-up-intercompany-dimensions"></a>Sådan konfigureres koncerninterne dimensioner

Før du og dine koncerninterne partnere vil kunne udveksle transaktioner med tilknyttede dimensioner, skal I aftale, hvilke dimensioner I alle skal bruge. Moderselskabet i en koncern kan f.eks. oprette en forenklet version af deres egne dimensionssæt, eksportere dem til en XML-fil, der kan distribueres til hver virksomhed i gruppen. Datterselskaberne i koncernen kan derefter indlæse XML-filen på siden **Koncerninterne dimensioner** i deres eget regnskab og knytte de koncerninterne dimensioner her til dimensionerne på siden **Dimensioner**.  

> [!NOTE]
> Hvert regnskab i [!INCLUDE [prod_short](includes/prod_short.md)] skal knytte dimensioner til IC-dimensioner for udgående dokumenter og knytte IC-dimensioner til deres egne dimensioner for indgående dokumenter. Denne tilknytning er med til at sikre konsistens i alle virksomheder. Du kan finde flere oplysninger i afsnittet [Oversigt over tilknytning af intercompany-dimensioner til regnskabets dimensioner](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Hvis din virksomhed er moderselskabet og har det definerende sæt koncerninterne dimensioner, som skal bruges i koncernen som fælles reference, skal du følge proceduren: [Sådan defineres koncerninterne dimensioner](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Hvis din virksomhed er et datterselskab, og du modtager en XML-fil med koncerninterne dimensioner, som skal bruges som fælles reference i koncernen, skal du følge proceduren: [Sådan indlæses koncerninterne dimensioner](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Sådan defineres koncerninterne dimensioner

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.  
2. Angiv hver dimension på en linje på siden **Koncerninterne dimensioner**.

    Hvis dine koncerninterne dimensioner skal være identiske med eller ligge tæt opad de eksisterende dimensioner i dit regnskab, kan du få udfyldt siden automatisk ved at klikke på **Kopier fra dimensioner**, hvorefter du kan redigere de indsatte linjer.  
3. Du kan udlæse de koncerninterne dimensioner til en XML-fil, så de kan distribueres til partnerne, ved at vælge handlingen **Udlæs**.  
4. Angiv filnavnet og den placering, hvor du vil gemme XML-filen, og vælg derefter knappen **Gem**.  

### <a name="to-import-the-intercompany-dimensions"></a>Sådan indlæses koncerninterne dimensioner  

Når der findes en fil til de definerende koncerninterne dimensioner, kan koncerninterne partnere indlæse den for at sikre, at de har de samme dimensioner.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.  
2. På siden **Koncerninterne dimensioner** skal du vælge handlingen **Indlæs**.  
3. Angiv XML-filens navn og placering, og vælg derefter knappen **Åbn**.  

Linjerne på siderne **Koncerninterne dimensioner** og **Koncerninterne dimensionsværdier** indlæses.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Sådan knyttes IC-dimensioner til dimensioner i regnskabet

Når du har defineret eller importeret de dimensioner, som du og dine koncerninterne partnerne har aftalt at bruge, skal du knytte hver koncerninterne dimension til en af dimensionerne i dit eget regnskab og omvendt. På siden **Koncerninterne dimensioner** angiver du, hvordan koncerninterne dimensioner på *indgående transaktioner* skal oversættes til dimensioner fra din virksomheds liste over dimensioner. På siden **Dimensioner** angiver du, hvordan dine dimensioner skal oversættes til IC-dimensioner på *udgående transaktioner*.

Hvis nogle af de koncerninterne dimensioner har samme kode som de tilsvarende dimensioner i listen over dimensioner i din egen virksomhed, kan du få programmet til automatisk at knytte dimensionerne sammen, og derefter kan du tilknytte kontiene automatisk.  

I følgende trin skal du først knytte IC-dimensionerne til dimensioner for indgående dokumenter på siden **IC-dimensioner**. Derefter knytter du dimensioner til IC-dimensioner for udgående dokumenter på siden **Dimensioner**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Koncerninterne dimensioner**, og vælg derefter det relaterede link.
2. På siden **Koncerninterne dimensioner** skal du markere de linjer, som du vil tilknytte automatisk, og derefter vælge handlingen **Knyt til dim. med samme kode**.
3. Udfyld feltet **Dim.kode for tilknytning** for hver IC-dimension, der ikke tilknyttes automatisk.

    Du skal muligvis føje feltet til visningen. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).
4. Vælg handlingen **Koncerninterne dimensionsværdier**.
5. Udfyld feltet **Dim.værdikode for tilknytning** på siden **Koncerninterne dimensionsværdier**.

    Fortsæt med at knytte dimensionerne til koncerninterne dimensioner ved at udføre lignende trin.
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Dimensioner**, og vælg derefter det relaterede link.
7. På siden **Koncerninterne dimensioner** skal du markere de linjer, som du vil tilknytte automatisk, og derefter vælge handlingen **Knyt til IC-dim. med samme kode**.
8. Udfyld feltet **IC-dim.værdikode for tilknytn.** for hver koncerninterne dimension, der ikke tilknyttes automatisk.
9. Vælg handlingen **Koncerninterne dimensionsværdier**.
10. Udfyld feltet **Knyt til IC-dim. med samme kode** på siden **Dimensionsværdier**.

## <a name="see-also"></a>Se også

[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]