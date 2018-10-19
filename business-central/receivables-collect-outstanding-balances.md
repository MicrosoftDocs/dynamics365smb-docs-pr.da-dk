---
title: "Rykke debitorer eller give dem en bøde for forfaldne betalinger | Microsoft Docs"
description: "Beskriver, hvordan du sender en påmindelse til kunden om en betaling, der er forfalden, og lægger gebyrer til betalingen på grund af forsinkelsen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4696fa95b82a0deb0ba9642ef796160f25a57afc
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="collect-outstanding-balances"></a>Indhente udestående beløb
Likviditetsstyring omfatter kontrol af, om forfaldne beløb er betalt til tiden. Hvis debitorer har forfaldne betalinger, kan du begynde med at sende rapporten Kontoudtog som en påmindelse. Alternativt kan du udstede rykkere.

Du kan bruge rykkere til at minde debitorer om forfaldne beløb. Du kan også bruge rykkere til at beregne renter eller gebyrer og inkludere dem på rykkeren. Du kan bruge rentenotaer, hvis du vil debitere debitorerne for renter eller gebyrer uden at rykke for forfaldne beløb.

## <a name="reminders"></a>Rykkere
Inden du kan oprette rykkere, skal du oprette betingelser og knytte dem til debitorerne. Hver rykkerbetingelse har foruddefinerede rykkerniveauer. Hvert rykkerniveau indeholder regler om, hvornår rykkeren skal udstedes, f.eks. hvor mange dage efter fakturaens forfaldsdato eller efter datoen for den forrige rykker. Indholdet i vinduet **Rentebetingelser** er bestemmende for, om der beregnes rente på rykkeren.  

Du kan med mellemrum udføre kørslen **Opret rykkere** for at oprette rykkere til alle debitorer med forfaldne beløb, eller du kan oprette en rykker manuelt til en bestemt debitor og få linjerne beregnet og udfyldt automatisk.  

Du kan ændre rykkerne, når først du har oprettet dem. Den tekst, der vises i begyndelsen og slutningen af rykkeren, afhænger af betingelserne for rykkerniveauet og kan ses i kolonnen **Beskrivelse**. Hvis et beregnet beløb er blevet indsat automatisk i start- eller slutteksten, reguleres teksten ikke, hvis du sletter linjerne. Derefter skal du bruge funktionen **Opdater rykkertekst**.  

En debitorpost, hvor feltet **Afvent** er markeret, vil ikke udløse oprettelse af en rykker. Men hvis en rykker oprettes på basis af en anden post, vil en forfalden post, der er markeret som afventende, også blive inkluderet i rykkeren. Der beregnes ikke rente på linjer med disse poster.

Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere, typisk som mail.

## <a name="finance-charges"></a>Finansieringsomkostninger
Når en debitor ikke betaler til forfaldsdatoen, kan du automatisk få en rentenota beregnet og føje den til de forfaldne beløb på debitorens konto. Du kan underrette debitor om de tilføjede gebyrer ved at sende rentenotaen.  

> [!NOTE]  
> Du kan bruge rentenotaer til at beregne renter og til at underrette debitorerne om renterne uden at rykke dem for forfaldne betalinger. Alternativt kan du beregne renter på forfaldne betalinger, når du opretter rykkere.  

Du kan oprette en rentenota manuelt til en individuel debitor og udfylde linjerne automatisk. Alternativt kan du bruge funktionen **Opret rentenotaer** for at oprette rentenotaer til alle eller udvalgte debitorer med forfaldne beløb.  

Du kan ændre rentenotaerne, når du først har oprettet dem. Den tekst, der vises i begyndelsen og slutningen af rentenotaen, afhænger af rentebetingelserne og kan ses i kolonnen **Beskrivelse** i linjerne. Hvis et beregnet beløb er blevet indsat automatisk i start- eller slutteksten, reguleres teksten ikke, hvis du sletter linjerne. Derefter skal du bruge funktionen **Opdater rentenotatekst**.  

Når du har oprettet rentenotaer og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rentenotaer, typisk som mail.

## <a name="multiple-interest-rates"></a>Flere rentesatser
Når du konfigurerer rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder. Hvis flere rentesatser ikke er konfigureret, så bruges den rente og periode, der er defineret i vinduerne **Rentebetingelser** og **Rykkerbetingelser**, for hele beregningsperioden. Du kan finde flere oplysninger i [Angiv flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Sådan sendes rapporten Kontoudtog
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoudtog**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Rapportindstillinger** skal du vælge, hvordan rapporten skal sendes til kunden.

> [!NOTE]  
>   Hvis du bruger flere valutaer, udskrives rapporten Kontoudtog altid i kundens valuta. Den sidste dato i en kontoudtogsperiode bruges også som kontoudtogsdatoen og aldersfordelingsdatoen, hvis aldersfordelingen er inkluderet.

## <a name="to-set-up-reminder-terms"></a>Sådan defineres rykkerbetingelser
Hvis debitorer har forfaldne beløb, skal du afgøre, om der skal sendes en rykker. Desuden vil du evt. debitere deres konti for rente eller gebyrer. Du kan angive et hvilket som helst antal betingelser for rykkere. For hver rykkerbetingelseskode kan du definere et ubegrænset antal rykkerniveauer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.  
3. Hvis du vil bruge mere end én kombination af rykkerbetingelser, kan du angive en kode for hver enkelt.

## <a name="to-set-up-reminder-levels"></a>Sådan angives rykkerniveauer
Første gang en rykker oprettes til en debitor, bruges indstillingen fra niveau 1. Når rykkeren er udstedt, registreres niveaunummeret på de rykkerposter, der er oprettet og sammenkædet med de individuelle debitorposter. Hvis det er nødvendigt at rykke debitoren igen, markeres alle de rykkerposter, der er sammenkædet med åbne debitorposter, så nummeret på det højeste niveau bliver fundet. Derefter vil betingelserne fra det næste niveaunummer blive brugt til den nye rykker.

Hvis du opretter flere rykkere end du har defineret niveauer til, bruges betingelserne for det højeste niveau. Du kan oprette så mange rykkere, som tillades ifølge feltet **Maks. antal rykkere** under rykkerbetingelserne.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkerbetingelser**, og vælg derefter det relaterede link.  
2. Vælg den linje med de betingelser, du vil oprette niveauer for, i vinduet **Rykkerbetingelser**, og vælg derefter handlingen **Niveauer**.  
3. Udfyld felterne efter behov.  

    For hvert rykkerniveau kan du angive individuelle betingelser, som kan omfatte ekstra gebyrer i både lokal og udenlandsk valuta. Du kan definere adskillige opkrævningsgebyrer i udenlandsk valuta for hver kode i vinduet **Rykkerniveauer**.
4. Vælg handlingen **Valutaer**.
5. I vinduet **Valutaer til rykkerniveau** definerer du for hver rykkerniveaukode og tilsvarende rykkerniveaunummer en valutakode og et opkrævningsgebyr.

    > [!NOTE]  
    > Når du opretter rykkere i en udenlandsk valuta, bruges betingelserne for udenlandsk valuta, som du angiver her, til automatisk at oprette rykkere. Hvis der ikke er defineret rykkerbetingelser i udenlandske valutaer, bruges de rykkerbetingelser, der er angivet i vinduet **Rykkerniveauer**, og derefter konverteres de til den relevante valuta.

    For hvert rykkerniveau kan du angive tekst, som bliver udskrevet inden (**Starttekst**) eller efter (**Sluttekst**) på posterne på rykkeren.

6. Vælg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og udfyld vinduet **Rykkertekst**.
7. Hvis du vil indsætte relaterede værdier i den resulterende rykkertekst automatisk, skal du angive følgende pladsholdere i feltet **Tekst**.  

|Pladsholder|Værdi|  
|-----------------|-----------|  
|%1|Indholdet af feltet **Bilagsdato** på rykkerhovedet|  
|%2|Indholdet af feltet **Forfaldsdato** på rykkerhovedet|  
|%3|Indholdet af feltet **Rentesats** på de relaterede rentebetingelser|  
|%4|Indholdet af feltet **Restbeløb** på rykkerhovedet|  
|%5|Indholdet af feltet **Rentebeløb** på rykkerhovedet|  
|%6|Indholdet af feltet **Opkrævningsgebyr** på rykkerhovedet|  
|%7|Rykkerens totalbeløb|  
|%8|Indholdet af feltet **Rykkerniveau** på rykkerhovedet|  
|%9|Indholdet af feltet **Valutakode** på rykkerhovedet|  
|%10|Indholdet af feltet **Bogføringsdato** på rykkerhovedet|  
|%11|Firmanavnet.|  
|%12|Indholdet af feltet **Opkrævningsgebyr pr. linje** på rykkerhovedet|  

Hvis du f.eks. skriver **Du skylder %9 %7, der forfalder den %2.**, vil den resulterende rykker indeholde følgende tekst: **Du skylder USD 1.200,50, der forfalder den 02-02-2014.**.

> [!NOTE]
> Forfaldsdatoen beregnes i overensstemmelse med den datoformel, som du angiver. Du kan finde flere oplysninger i afsnittet "Bruge datoformler" i [Angive datointervaller](ui-enter-date-ranges.md).

Angiv en af koderne på hvert enkelt kundekort, når du har oprettet rykkerbetingelserne med ekstra niveauer og tekst. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Sådan oprettes en rykker automatisk
En rykker svarer til en faktura. Når du opretter en rykker, skal et rykkerhoved og en eller flere rykkerlinjer udfyldes. Du kan bruge en funktion til at oprette rykkere for alle kunder automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opret rykkere** i vinduet **Rykkermeddelelse**.
3. I vinduet **Opret rykkere** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
4. Vælg knappen **OK**.

## <a name="to-create-a-reminder-manually"></a>Sådan oprettes rykkere manuelt
I vinduet **Rykker** skal du udfylde oversigtspanelet **Generelt** manuelt og lade linjerne blive udfyldt automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**.
4. Vælg handlingen **Foreslå rykkerlinjer**.
5. I kørslen **Foreslå rykkerlinjer** skal du udfylde felterne for at angive, hvordan og hvem rykkerne oprettes til.
6. Marker afkrydsningsfeltet **Medtag afventende poster**, hvis rykkere skal indeholde forfaldne åbne poster, som er i venteposition.

    > [!Important]
    > Afventende åbne poster indsættes uanset indstillingen i afkrydsningsfeltet Kun poster med forfaldne beløb.

7. Vælg knappen **OK**.

## <a name="to-replace-reminder-texts"></a>Sådan erstattes rykkertekst  
Du kan angive den tekst, der angives i rykkere, på flere måder. I nogle tilfælde kan du have brug for at erstatte start- og slutteksten, der er angivet for det aktuelle niveau, med tekst fra et andet niveau.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Åbn den relevante rykker, og vælg derefter handlingen **Opdater rykkertekst**.
3. Angiv det ønskede niveau i feltet **Rykkerniveau** i vinduet **Opdater rykkertekst**.
3. Klik på **OK** for at opdatere start- og slutteksten.

## <a name="to-issue-a-reminder"></a>Sådan udstedes en rykker
Når du har oprettet rykkere og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rykkere.

Når du udsteder en rykker, overføres dataene til et separat vindue med udstedte rykkere. Samtidigt bogføres rykkerposter. Hvis der er beregnet rente eller ekstragebyr, bogføres posterne på debitorposten og finansposten.

Når man udsteder en rykker, bogføres posterne automatisk svarende til de betingelser, der er angivet i vinduet **Rykkerbetingelser**. Denne specifikation angiver, om renter og/eller gebyrer skal bogføres på debitorens konto og på finanskonti. Opsætningen i vinduet **Debitorbogføringsgrupper** angiver, hvilke konti der bogføres på.

Der oprettes en post i vinduet **Rykker-/rentenotapost** for hver debitorpost på rentenotaen.

Hvis afkrydsningsfelterne **Bogfør rente** eller **Bogfør opkrævningsgebyr** er markeret i vinduet **Rykkerbetingelser**, oprettes følgende poster også:

- Én post i vinduet **Debitorposter**
- Én betalingspost på den relevante finanskonto
- Én rente- og/eller en gebyrpost i den relevante finanskonto

Desuden kan udstedelse af en rykker medføre momsposteringer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkere**, og vælg derefter det relaterede link.
2. Markér den relevante rykker, og vælg derefter handlingen **Udsted**.
3. I vinduet **Udsted rykkere** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.

Rykkeren udskrives enten eller sendes til en mail, der er angivet som en vedhæftet PDF-fil.

## <a name="to-set-up-finance-charge-terms"></a>Sådan konfigurerer du rentebetingelser
Du skal også definere en kode for hver renteberegningsmetode. Du kan så angive denne kode i feltet **Rentebetingelseskode** på debitor- eller kreditorkortene.

Rentenotaer kan beregnes efter kreditkronedage- eller saldorenteprincippet:

* Saldorenteprincippet:

    Rentegebyret er blot en procentdel af den forfaldne saldo:  
    *Saldorenteprincippet* - *Rente* = *Forfalden saldo* x *(Rentesats/100)*

*   Kreditkronedageprincippet

    Der tages hensyn til det antal dage, betalingsfristen er overskredet med:  
    *Metoden Kreditkronedage* - *Rente* = *Forfalden saldo* x *(Kreditdage/Renteperiode)* x *(Rentesats/100)*

Hver kode i tabellen Rentebetingelser er desuden kædet sammen med en undertabel, nemlig tabellen Rentenotatekst. Til hver rentebetingelse kan du definere en starttekst og/eller en sluttekst, som skal vises på rentenotaen.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentebetingelser**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.  
3. Hvis du vil bruge mere end én kombination af rentebetingelser, kan du angive en kode for hver enkelt.

    For hver rentebetingelse kan du angive individuelle betingelser, som kan omfatte ekstra gebyrer i både lokal og udenlandsk valuta. Du kan definere adskillige opkrævningsgebyrer i udenlandsk valuta for hver kode i vinduet **Rentebetingelser**.
4. Vælg handlingen **Valutaer**.
5. I vinduet **Valutaer til rentebetingelser** skal du for hver periode angive en valutakode og et opkrævningsgebyr.

    > [!NOTE]  
    > Når du beregner renter i en udenlandsk valuta, bruges de betingelser for udenlandsk valuta, som du angiver her, til at oprette rentenotaer. Hvis der ikke er defineret rentebetingelser i udenlandske valutaer, bruges rentebetingelserne i den regnskabsvaluta, der er angivet i vinduet **Rentebetingelser**, og de konverteres derefter til den relevante valuta.

    For hver rentebetingelse kan du angive tekst, der udskrives før (**Starttekst**) eller efter (**Sluttekst**) på posterne i rentenotaen.  
6. Vælg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og udfyld vinduet **Rentenotatekst**.
7. Hvis du vil indsætte relaterede værdier i den resulterende rentenotatekst automatisk, skal du angive følgende pladsholdere i feltet **Tekst**.

|Pladsholder|Værdi|  
|-----------------|-----------|  
|%1|Indholdet af feltet **Bilagsdato** på rentenotahovedet|  
|%2|Indholdet af feltet **Forfaldsdato** på rentenotahovedet|  
|%3|Indholdet af feltet **Rentesats** på de relaterede rentebetingelser|  
|%4|Indholdet af feltet **Restbeløb** i rentenotahovedet|  
|%5|Indholdet af feltet **Rentebeløb** i rentenotahovedet|  
|%6|Indholdet af feltet **Opkrævningsgebyr** i rentenotahovedet|  
|%7|Rykkerens totalbeløb|  
|%8|Indholdet af feltet **Valutadato** på rentenotahovedet|  
|%9|Indholdet af feltet **Bogføringsdato** i rentenotahovedet|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Sådan gør du: Oprette rentenotaer manuelt  
En rentenota svarer til en faktura. Du kan udfylde et hoved manuelt og lade programmet udfylde linjerne, eller du kan oprette rentenotaer for alle kunder automatisk.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentenotaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov.  
3. Vælg handlingen **Foreslå rentenotalinjer**.
4. I vinduet **Foreslå rentenotalinjer** skal du angive et filter på oversigtspanelet **Debitorpost**, hvis du kun vil oprette rentenotaer for specifikke poster.  
5.  Vælg **OK** for at starte kørslen.  

## <a name="to-update-finance-charge-memo-texts"></a>Sådan opdateres tekster til rentenotaer  
I nogle tilfælde kan det være nødvendigt at ændre den start- og sluttekst, der er angivet for rentebetingelser. Hvis du gør det på et tidspunkt, hvor du har oprettet, men ikke udstedt rentenotaer, kan du opdatere notaen med den ændrede tekst.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentenota**, og vælg derefter det relaterede link.  
2. Åbn den rentenota, som du vil ændre tekst for, og vælg derefter handlingen **Opdater rentenotatekst**.
3. I vinduet **Opdater rentenotatekst** kan angive et filter, hvis du vil opdatere flere notaer.
4. Klik på **OK** for at opdatere start- og slutteksten.  

## <a name="to-issue-finance-charge-memos"></a>Sådan udstedes rentenotaer
Når du har oprettet rentenotaer og foretaget eventuelle nødvendige ændringer, kan du enten udskrive testrapporter eller udstede rentenotaer.

Når man udsteder en rykker, bogføres posterne automatisk svarende til de betingelser, der er angivet i vinduet **Rentebetingelser**. Denne specifikation angiver, om renter og/eller gebyrer skal bogføres på debitorens konto og på finanskonti. Opsætningen i vinduet **Debitorbogføringsgrupper** angiver, hvilke konti der bogføres på.

Der oprettes en post i vinduet **Rykker-/rentenotapost** for hver debitorpost på rentenotaen.

Hvis afkrydsningsfelterne **Bogfør rente** eller **Bogfør opkrævningsgebyr** er markeret i vinduet **Rentebetingelser**, oprettes følgende poster også:

- Én post i vinduet **Debitorposter**
- Én betalingspost på den relevante finanskonto
- Én rente- og/eller en gebyrpost i den relevante finanskonto

Desuden kan udstedelse af en rentenota medføre momsposteringer.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentenotaer**, og vælg derefter det relaterede link.
2. Markér den relevante nota, og vælg derefter handlingen **Udsted**.
3. I vinduet **Udsted rentenotaer** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.

Rentenotaen udskrives enten eller sendes til en mail, der er angivet som en vedhæftet PDF-fil.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Sådan får du vist rykker- og rentenotaposter  
Når du udsteder en rykker, oprettes der en rykkerpost i vinduet **Rykker-/rentenotaposter** for hver rykkerlinje, der indeholder en debitorpost. Derefter kan du få vist en oversigt over de oprettede rykkerposter for en bestemt debitor.    
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.  
2. Åbn det relevante debitorkort, og vælg derefter handlingen **Poster**.
3. I vinduet **Debitorposter** skal du vælge linjen med den post, du vil have vist rykkerposter for, og derefter vælge handlingen **Rykker-/rentenotaposter**.

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

