---
title: Indhente udestående beløb
description: Få mere at vide om, hvordan du sender en påmindelse til kunden om en betaling, der er forfalden, og lægger gebyrer til betalingen på grund af forsinkelsen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 81f43ef3f021ef0d348eb14abdffdfda2b3d85fc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758388"
---
# <a name="collect-outstanding-balances"></a>Indhente udestående beløb

Likviditetsstyring omfatter kontrol af, om forfaldne beløb er betalt til tiden. Hvis debitorer har forfaldne betalinger, kan du begynde med at sende rapporten **Kontoudtog** som en påmindelse. Alternativt kan du udstede rykkere.

Du kan bruge rykkere til at minde debitorer om forfaldne beløb. Du kan også bruge rykkere til at beregne renter eller gebyrer og inkludere dem på rykkeren. Du kan bruge rentenotaer, hvis du vil debitere debitorerne for renter eller gebyrer uden at rykke for forfaldne beløb.

## <a name="statements"></a>Kontoudtog

Fra debitorkortet kan du oprette en kontoudtog med den pågældende debitors transaktioner. Derefter sender du kunden den genererede PDF-fil. Du kan også bruge rapporten **Kontoudtog** til at sende dine kunder en oversigt over deres forretning med dig. Kundekontoudtoget kan sendes til Excel til videre behandling.  

### <a name="to-send-the-customer-statement-report"></a>Sådan sendes rapporten Kontoudtog

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoudtog**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Rapportindstillinger** skal du vælge, hvordan rapporten skal sendes til kunden.

> [!NOTE]
> Hvis du bruger flere valutaer, udskrives rapporten Kontoudtog altid i kundens valuta. Den sidste dato i en kontoudtogsperiode bruges også som kontoudtogsdatoen og aldersfordelingsdatoen, hvis aldersfordelingen er inkluderet.

## <a name="reminders"></a>Rykkere

Inden du kan oprette rykkere, skal du oprette betingelser og knytte dem til debitorerne. Du kan finde flere oplysninger i [Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] Indholdet af siden **Rentebetingelser** er bestemmende for, om der beregnes rente på rykkeren.  

Du kan med mellemrum udføre kørslen **Opret rykkere** for at oprette rykkere til alle debitorer med forfaldne beløb, eller du kan oprette en rykker manuelt til en bestemt debitor og få linjerne beregnet og udfyldt automatisk.  

Du kan ændre rykkerne, når først du har oprettet dem. Den tekst, der vises i begyndelsen og slutningen af rykkeren, afhænger af betingelserne for rykkerniveauet og kan ses i kolonnen **Beskrivelse**. Hvis et beregnet beløb er blevet indsat automatisk i start- eller slutteksten, reguleres teksten ikke, hvis du sletter linjerne. Derefter skal du bruge funktionen **Opdater rykkertekst**.  

En debitorpost, hvor feltet **Afvent** er markeret, vil ikke udløse oprettelse af en rykker. Men hvis en rykker oprettes på basis af en anden post, vil en forfalden post, der er markeret som afventende, også blive inkluderet i rykkeren. Der beregnes ikke rente på linjer med disse poster.

Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere, typisk som mail.

### <a name="to-create-a-reminder-automatically"></a>Sådan oprettes en rykker automatisk

En rykker svarer til en faktura. Når du opretter en rykker, skal et rykkerhoved og en eller flere rykkerlinjer udfyldes. Du kan bruge en funktion til at oprette rykkere for alle kunder automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opret rykkere** på siden **Rykkermeddelelse**.
3. På siden **Opret rykkere** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
4. Vælg knappen **OK**.

### <a name="to-create-a-reminder-manually"></a>Sådan oprettes rykkere manuelt

På siden **Rykker** skal du udfylde oversigtspanelet **Generelt** manuelt og lade linjerne blive udfyldt automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. Vælg handlingen **Foreslå rykkerlinjer**.
5. I kørslen **Foreslå rykkerlinjer** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
6. Marker afkrydsningsfeltet **Medtag afventende poster**, hvis rykkere skal indeholde forfaldne åbne poster, som er i venteposition.
7. Marker afkrydsningsfeltet **Kun poster med forfaldne beløb**, hvis rykkere kun skal indeholde forfaldne åbne poster. Kun fakturaer og betalinger vises, da de er poster, hvor kundernes betalinger kan være forfaldne.

    > [!Important]
    > Afventende åbne poster indsættes, uanset hvilken indstilling der er markeret i afkrydsningsfeltet **Kun poster med forfaldne beløb**.

8. Vælg knappen **OK**.

### <a name="to-replace-reminder-texts"></a>Sådan erstattes rykkertekst

Du kan angive den tekst, der angives i rykkere, på flere måder. I nogle tilfælde kan du have brug for at erstatte start- og slutteksten, der er angivet for det aktuelle niveau, med tekst fra et andet niveau.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Åbn den relevante rykker, og vælg derefter handlingen **Opdater rykkertekst**.
3. Angiv det ønskede niveau i feltet **Rykkerniveau** på siden **Opdater rykkertekst**.
4. Klik på **OK** for at opdatere start- og slutteksten.

### <a name="to-issue-a-reminder"></a>Sådan udstedes en rykker

Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere.

Når du udsteder en rykker, overføres dataene til en separat side med udstedte rykkere. Samtidigt bogføres rykkerposter. Hvis der er beregnet rente eller ekstragebyr, bogføres posterne på debitorposten og finansposten.

Når man udsteder en rykker, bogføres posterne automatisk svarende til de betingelser, der er angivet på siden **Rykkerbetingelser**. Denne specifikation angiver, om renter og/eller gebyrer skal bogføres på debitorens konto og på finanskonti. Opsætningen på siden **Debitorbogføringsgrupper** angiver, hvilke konti der bogføres på.

Der er oprettet en post på siden **Rykker-/rentenotaposter** for hver debitorpost på rentenotaen.

Hvis afkrydsningsfelterne **Bogfør rente** eller **Bogfør opkrævningsgebyr** er markeret på siden **Rykkerbetingelser**, oprettes følgende poster også:

- Én post på siden **Debitorposter**
- Én betalingspost på den relevante finanskonto
- Én rente- og/eller en gebyrpost i den relevante finanskonto

Desuden kan udstedelse af en rykker medføre momsposteringer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Markér den relevante rykker, og vælg derefter handlingen **Udsted**.
3. På siden **Udsted rykkere** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.

Rykkeren udskrives enten eller sendes til en mail, der er angivet som en vedhæftet PDF-fil.

### <a name="to-cancel-an-issued-reminder"></a>Sådan annulleres en udstedt rykker

Hvis rykkere er blevet udstedt ved en fejl, kan du annullere dem, før de sendes. Det kan du gøre enten en for en eller som en kørsel.

1. På siden **Udstedte rykkere** skal du vælge en eller flere linjer for udstedte rykkere, som du vil annullere, og derefter vælge handlingen **Annuller**.
2. På siden **Annuller udstedte rykkere** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.

## <a name="finance-charges"></a>Finansieringsomkostninger

Når en debitor ikke betaler til forfaldsdatoen, kan du automatisk få en rentenota beregnet og føje den til de forfaldne beløb på debitorens konto. Du kan underrette debitor om de tilføjede gebyrer ved at sende rentenotaen.  

> [!NOTE]  
> Du kan bruge rentenotaer til at beregne renter og til at underrette debitorerne om renterne uden at rykke dem for forfaldne betalinger. Alternativt kan du beregne renter på forfaldne betalinger, når du opretter rykkere.  

Du kan først konfigurere betingelser, når du har oprettet rentenotaer. Du kan finde flere oplysninger i [Konfiguration af Rentebetingelser](finance-setup-finance-charges.md).  

Du kan oprette en rentenota manuelt til en individuel debitor og udfylde linjerne automatisk. Alternativt kan du bruge funktionen **Opret rentenotaer** for at oprette rentenotaer til alle eller udvalgte debitorer med forfaldne beløb.  

Du kan ændre rentenotaerne, når du først har oprettet dem. Den tekst, der vises i begyndelsen og slutningen af rentenotaen, afhænger af rentebetingelserne og kan ses i kolonnen **Beskrivelse** i linjerne. Hvis et beregnet beløb er blevet indsat automatisk i start- eller slutteksten, reguleres teksten ikke, hvis du sletter linjerne. Derefter skal du bruge funktionen **Opdater rentenotatekst**.  

Når du har oprettet rentenotaer og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rentenotaer, typisk som mail.

### <a name="to-create-a-finance-charge-memo-manually"></a>Sådan gør du: Oprette rentenotaer manuelt

En rentenota svarer til en faktura. Du kan udfylde et hoved manuelt og lade programmet udfylde linjerne, eller du kan oprette rentenotaer for alle kunder automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udsted rentenotaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov.  
3. Vælg handlingen **Foreslå rentenotalinjer**.
4. På siden **Foreslå rentenotalinjer** skal du angive et filter på oversigtspanelet **Debitorpost**, hvis du kun vil oprette rentenotaer for specifikke poster.

    > [!NOTE]
    > Selvom de vises, vil valg af filtrene **Betaling** og **Kreditnota** dom **Dokumenttype** ikke have nogen virkning, fordi funktionen **Selvom de vises, vil valg** kun håndterer positive beløb.
5.  Vælg **OK** for at starte kørslen.  

### <a name="to-update-finance-charge-memo-texts"></a>Sådan opdateres tekster til rentenotaer  
I nogle tilfælde kan det være nødvendigt at ændre den start- og sluttekst, der er angivet for rentebetingelser. Hvis du gør det på et tidspunkt, hvor du har oprettet, men ikke udstedt rentenotaer, kan du opdatere notaen med den ændrede tekst.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udsted rentenota**, og vælg derefter det relaterede link.  
2. Åbn den rentenota, som du vil ændre tekst for, og vælg derefter handlingen **Opdater rentenotatekst**.
3. På siden **Opdater rentenotatekst** kan angive et filter, hvis du vil opdatere flere notaer.
4. Klik på **OK** for at opdatere start- og slutteksten.  

### <a name="to-issue-finance-charge-memos"></a>Sådan udstedes rentenotaer
Når du har oprettet rentenotaer og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rentenotaer.

Når man udsteder en rykker, bogføres posterne automatisk svarende til de betingelser, der er angivet på siden **Rentebetingelser**. Denne specifikation angiver, om renter og/eller gebyrer skal bogføres på debitorens konto og på finanskonti. Opsætningen på siden **Debitorbogføringsgrupper** angiver, hvilke konti der bogføres på.

Der er oprettet en post på siden **Rykker-/rentenotaposter** for hver debitorpost på rentenotaen.

Hvis afkrydsningsfelterne **Bogfør rente** eller **Bogfør opkrævningsgebyr** er markeret på siden **Rentebetingelser**, oprettes følgende poster også:

- Én post på siden **Debitorposter**
- Én betalingspost på den relevante finanskonto
- Én rente- og/eller en gebyrpost i den relevante finanskonto

Desuden kan udstedelse af en rentenota medføre momsposteringer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udsted rentenotaer**, og vælg derefter det relaterede link.
2. Markér den relevante nota, og vælg derefter handlingen **Udsted**.
3. På siden **Udsted rentenotaer** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.

Rentenotaen udskrives enten eller sendes til en mail, der er angivet som en vedhæftet PDF-fil.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Sådan annulleres den udstedte rentenota
Hvis rentenotaer er blevet udstedt ved en fejl, kan du annullere dem, før de sendes. Det kan du gøre enten en for en eller som en kørsel.
1. På siden **Udstedte rentenotaer** skal du vælge en eller flere linjer for udstedte rentenotaer, som du vil annullere, og derefter vælge handlingen **Annuller**.
2. På siden **Annuller udstedte rentenotaer** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Sådan får du vist rykker- og rentenotaposter  
Når du udsteder en rykker, oprettes der en rykkerpost på siden **Rykker-/rentenotaposter** for hver rykkerlinje, der indeholder en debitorpost. Derefter kan du få vist en oversigt over de oprettede rykkerposter for en bestemt debitor.    
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.  
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Poster**.
3. På siden **Debitorposter** skal du vælge linjen med den post, du vil have vist rykkerposter for, og derefter vælge handlingen **Rykker-/rentenotaposter**.

## <a name="multiple-interest-rates"></a>Flere rentesatser

Når du konfigurerer rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder. Hvis flere rentesatser ikke er konfigureret, så bruges den rente og periode, der er defineret på siderne **Rentebetingelser** og **Rykkerbetingelser**, for hele beregningsperioden. Du kan finde flere oplysninger i [Angiv flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md)  
[Konfiguration af Rentebetingelser](finance-setup-finance-charges.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
