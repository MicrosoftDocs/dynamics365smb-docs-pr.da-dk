---
title: Indhente udestående beløb
description: Få mere at vide om, hvordan du kan huske dine kunder med udestående betalinger. Sende et kundekontoudtog, udstede en rykker eller sende en rentenota.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.search.form: 6, 25, 440, 443, 448, 452
ms.date: 02/09/2022
ms.author: edupont
ms.openlocfilehash: 271b9f032df685b5eac1c3bddca037326ea4c1d6
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520730"
---
# <a name="collect-outstanding-balances"></a>Indhente udestående beløb

Likviditetsstyring omfatter kontrol af, om forfaldne beløb er betalt til tiden. Hvis debitorer har forfaldne betalinger, kan du begynde med at sende rapporten **Kontoudtog** som en påmindelse. Alternativt kan du udstede rykkere.

Du kan bruge rykkere til at minde debitorer om forfaldne beløb. Du kan også bruge rykkere til at beregne renter eller gebyrer og inkludere dem på rykkeren. Du kan bruge rentenotaer, hvis du vil debitere debitorerne for renter eller gebyrer uden at rykke for forfaldne beløb.

## <a name="statements"></a>Kontoudtog

Fra debitorkortet kan du oprette en kontoudtog med den pågældende debitors transaktioner. Derefter sender du kunden den genererede PDF-fil. Du kan også bruge rapporten **Kontoudtog** til at sende dine kunder en oversigt over deres forretning med dig. Kundekontoudtoget kan sendes til Excel til videre behandling.  

### <a name="to-send-the-customer-statement-report"></a>Sådan sendes rapporten Kontoudtog

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 10.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoudtog**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Rapportindstillinger** skal du vælge, hvordan rapporten skal sendes til kunden.

> [!NOTE]
> Hvis du bruger flere valutaer, udskrives rapporten Kontoudtog altid i kundens valuta. Den sidste dato i en kontoudtogsperiode bruges også som kontoudtogsdatoen og aldersfordelingsdatoen, hvis aldersfordelingen er inkluderet.

## <a name="reminders"></a>Rykkere

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

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

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udsted rentenotaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov.  
3. Vælg handlingen **Foreslå rentenotalinjer**.
4. På siden **Foreslå rentenotalinjer** skal du angive et filter på oversigtspanelet **Debitorpost**, hvis du kun vil oprette rentenotaer for specifikke poster.

    > [!NOTE]
    > Selvom de vises, vil valg af filtrene **Betaling** og **Kreditnota** dom **Dokumenttype** ikke have nogen virkning, fordi funktionen **Selvom de vises, vil valg** kun håndterer positive beløb.
5.  Vælg **OK** for at starte kørslen.  

### <a name="to-update-finance-charge-memo-texts"></a>Sådan opdateres tekster til rentenotaer  
I nogle tilfælde kan det være nødvendigt at ændre den start- og sluttekst, der er angivet for rentebetingelser. Hvis du gør det på et tidspunkt, hvor du har oprettet, men ikke udstedt rentenotaer, kan du opdatere notaen med den ændrede tekst.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Rentenota**, og vælg derefter det relaterede link.  
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

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Udsted rentenotaer**, og vælg derefter det relaterede link.
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
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 5.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Poster**.
3. På siden **Debitorposter** skal du vælge linjen med den post, du vil have vist rykkerposter for, og derefter vælge handlingen **Rykker-/rentenotaposter**.

## <a name="multiple-interest-rates"></a>Flere rentesatser

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Du kan finde flere oplysninger i [Angiv flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfiguration af rykkerbetingelser og -niveauer](finance-setup-reminders.md)  
[Konfiguration af Rentebetingelser](finance-setup-finance-charges.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]