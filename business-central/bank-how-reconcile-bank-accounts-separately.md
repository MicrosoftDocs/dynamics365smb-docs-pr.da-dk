---
title: Afstemme bankkonti
description: Dette emne beskriver, hvordan du kan afstemme transaktionerne på de interne bankkonti med transaktionerne i kontoudtog fra banken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.search.form: 379, 388, 389, 1290, 10124
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 1ebc2680aea583410a0f1bab8f4ff1d35989eb36
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381084"
---
# <a name="reconcile-bank-accounts"></a>Afstemme bankkonti

Du udfører bankafstemning for at sikre, at dine forskellige forretningstransaktioner og udgifter afspejles korrekt i firmaets regnskabsbøger. Det gør du ved at sammenligne og afstemme poster på dine interne bankkonti med banktransaktioner i din bank og derefter bogføre saldi på dine interne bankkonti for at gøre totaler tilgængelige for økonomichefer. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.

I det følgende beskrives, hvordan du udfører bankafstemning med siden **Bankkontoafstemning**.

> [!TIP]
> Du kan også afstemme bankkonti på siden **Betalingsudligningskladde**, når du gennemfører betalinger. Eventuelle åbne bankposter vedrørende de udlignede debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**. Det afstemmer automatisk bankkontoen for de betalinger, du bogfører, med kladden. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre dette arbejde på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke tilbyder import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet [Afstemme bankkonti](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Lokal funktionalitet for USA.

Linjerne på siden **Bankkontoafstemning** er opdelt i to ruder. Ruden **Bankkontoudtogslinjer** viser enten importerede banktransaktioner eller poster med udestående betalinger. Ruden **Bankkontoposter** viser finansposterne på en intern bankkonto.

Afstemning af banktransaktioner med interne bankposter kaldes *afstemning.* Du kan vælge at udføre tilsvarende afstemning automatisk ved hjælp af funktionen **Afstem automatisk**. Du kan alternativt manuelt markere linjer i begge ruder for at sammenkæde de enkelte bankkontoudtogslinjer med en eller flere relaterede bankposter og derefter bruge funktionen **Afstem manuelt**. Afkrydsningsfeltet **Udlignet** er markeret på linjer, hvor posterne stemmer. Du kan finde flere oplysninger i [Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Hvis bankkontoudtogslinjerne vedrører checkposter, kan du ikke bruge afstemningsfunktionerne. I stedet skal du vælge handlingen **Udlign poster** og derefter vælge den relevante checkpost, som bankkontoudtogslinjen skal afstemmes med.

Når værdien i feltet **Saldo i alt** i ruden **Bankkontoudtogslinjer** svarer til den samlede værdi i feltet **Saldo til afstemning** plus feltet **Sidste kontoudtog-saldo** i ruden **Bankkontoposter**, kan du vælge handlingen **Bogfør** for at afstemme de udlignede bankkontoposter. Ikke-afstemte bankkontoposter forbliver på siden, hvilket indikerer uoverensstemmelser, som du skal løse for at afstemme bankkontoen.

Alle linjer, der ikke kan afstemmes og er angivet med en værdi i feltet **Difference**, forbliver på siden **Bankkontoafstemning** efter bogføring. De repræsenterer en slags uoverensstemmelse, som du skal løse, før du kan fuldføre afstemningen af bankkontoen. Typiske forretningssituationer, der kan forårsage forskelle:

| Difference | Årsag | Løsning |
|------------|--------|------------|
| En transaktion i den interne bankkonto er ikke på bankkontoudtoget. | Banktransaktionen blev ikke foretaget, selvom der blev bogført en bogføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Foretag den manglende pengetransaktion (eller bed en debitor om at foretage den), og importer derefter bankkontoudtogsfilen igen, eller angiv transaktionen manuelt. |
| En postering på bankkontoudtoget findes ikke som et dokument eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion blev foretaget uden en tilsvarende bogføring [!INCLUDE[prod_short](includes/prod_short.md)]i, f.eks. bogføring af en kladdelinje for en udgift. | Opret og bogfør den manglende post. Du finder oplysninger om, hvordan du hurtigt starter dette, under [ Sådan oprettes manglende poster, som banktransaktioner skal afstemmes med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with). |
| En transaktion på den interne bankkonto svarer til en banktransaktion, men nogle oplysninger er for forskellige til at give et match. | Oplysninger såsom beløbet eller kundenavnet blev angivet forskelligt i forbindelse med banktransaktionen eller den interne bogføring. | Gennemse oplysningerne, og match derefter de to manuelt. Du bør eventuelt rette uoverensstemmelsen mellem oplysningerne. |

Du skal løse forskellene, f.eks. ved at oprette manglende poster og rette oplysninger, der ikke svarer til hinanden, eller ved at foretage manglende pengeposteringer, indtil afstemningen af bankkontoen er fuldført og bogført.

Du kan udfylde ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning** på følgende måder:

* Automatisk, ved hjælp af funktionen **Importér bankkontoudtog** for at udfylde ruden **Bankkontoudtogslinjer** med banktransaktioner ifølge en importeret fil eller stream, der er leveret af banken.
* Manuelt ved hjælp af funktionen **Foreslå linjer** for at udfylde ruden **Bankkontoudtogslinjer** ifølge fakturaerne i [!INCLUDE[prod_short](includes/prod_short.md)], der har udestående betalinger.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Sådan udfyldes bankafstemningslinjer ved at importere et bankkontoudtog

Ruden **Bankkontoudtogslinjer** udfyldes med bankposteringer i henhold til en importeret fil eller strøm, der er leveret af banken.

For at gøre det muligt at importere bankkontoudtog som bankfeeds skal du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og derefter knytte dine bankkonti til de relaterede onlinebankkonti. Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan også importere bankkontoudtogsfiler i komma- eller semikolonsepareret format (.CSV). Du kan bruge den assisterende opsætning **Opsæt en bankkontoudtogs filformat** for at definere importformater for bankkontoudtog og knytte formatet til en bankkonto. Du kan bruge disse formater, når du indlæser bankkontoudtog for import på siden **Bankkontoafstemning**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemning**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Vælg den relevante bankkonto i feltet **Bankkontonr.**. Bankkontoposterne, der findes på bankkontoen, vises i ruden **Bankkontoposter**.
4. Angiv datoen for kontoudtoget fra banken i feltet **Kontoudtogsdato**.
5. Angiv saldoen fra kontoudtoget i feltet **Kontoudtogs slutsaldo**.
6. Hvis du har en bankkontoudtogsfil, skal du vælge handlingen **Importér bankkontoudtog**.
7. Find filen, og vælg derefter knappen **Åbn** for at importere banktransaktionerne til linjerne ind i ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Sådan udfyldes bankafstemningslinjer med funktionen Foreslå linjer

Ruden **Bankkontoudtogslinjer** udfyldes i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], der har udestående betalinger.  

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Foreslå linjer**.
2. Angiv den tidligste dato for de poster, der skal afstemmes, i feltet **Startdato**.
3. Angiv den seneste dato for de poster, der skal afstemmes, i feltet **Slutdato**.

> [!NOTE]
> Slutdatoen svarer typisk til den dato, der er angivet i feltet **Kontoudtogsdato**. Men hvis du vil afstemme transaktioner for en del af en periode, kan du angive en anden slutdato. 

1. Marker afkrydsningsfeltet **Medtag check**, hvis du vil foreslå checkposter i stedet for de tilsvarende bankkontoposter.
1. Vælg knappen **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Sådan afstemmes kontoudtogslinjer automatisk med bankposter

Siden **Bankkontoafstemning** indeholder automatisk matchningsfunktionalitet, der er baseret på en sammenligning af tekst i en bankkontoudtogslinje (venstre rude) med tekst i en eller flere bankkontoposter (højre rude). Bemærk, at du kan overskrive den foreslåede automatiske afstemning, og du kan vælge slet ikke at bruge automatisk afstemning. Du kan finde flere oplysninger i [Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Du kan undersøge udgangspunktet for matches ved at bruge handlingen **match detaljer**. Detaljerne vil f. eks. omfatte navnene på de felter, der indeholdt identiske værdier.  

1. På siden **Bankkontoafstemning** skal du vælge **Match automatisk**. Siden **Afstem bankposter** åbnes.
2. I feltet **Transaktionsdatotolerance (dage)** skal du angive antallet af dage før og efter bankpostens bogføringsdato, hvorimellem funktionen skal søge efter tilsvarende transaktionsdatoer i kontoudtoget.

    Hvis du indtaster 0 eller lader feltet stå tomt, vil funktionen **Afstem automatisk** kun søge efter afstemte transaktionsdatoer på bankpostens bogføringsdato.
3. Vælg knappen **OK**.

    Alle bankkontoudtogslinjer og bankposter, der kan afstemmes, ændrer farve til grøn skrifttype, og afkrydsningsfeltet **Udlignet** markeres.
4. For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**.

> [!TIP]
> Du kan bruge en blanding af manuel og automatisk matchning. Hvis du har matchet poster manuelt, overskriver den automatiske matchning ikke dine valg. 

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter
1. På siden **Bankkontoafstemning** skal du vælge en ikke-udlignet linje i ruden **Bankkontoudtogslinjer**:
2. I ruden **Bankkontoposter** skal du vælge en eller flere bankkontoposter, der kan afstemmes med den valgte bankkontoudtogslinje. Hvis du vil vælge flere linjer, skal du trykke på og holde Ctrl-tasten nede.

   > [!TIP]
   > Du kan også manuelt sammenholde flere bankkontoudtogslinjer med én bankpost. Dette kan f. eks. være nyttigt, hvis bank indbetalingen indeholder flere betalingsmetoder, f. eks. kreditkort fra forskellige udstedere, og din bank viser dem som separate linjer. 
3. Vælg handlingen **Match manuelt**.

    Den valgte bankkontoudtogslinje og de valgte bankposter ændrer farve til grøn skrifttype, og afkrydsningsfeltet **Udlignet** i højre rude markeres.
4. Gentag trin 1 til 3 for alle kontoudtogslinjer, der ikke er afstemt.

> [!TIP]
> For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**. Hvis du har knyttet flere bankkontoudtogslinjer til en post og har behov for at fjerne en eller flere af de matchede linjer, fjernes alle de manuelle matches for posten, når du vælger **Fjern match**. 

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Sådan oprettes manglende poster, som bankkontoudtogslinjer skal afstemmes med

Undertiden indeholder bankafstemninger beløb med renter eller gebyrer. Sådanne bankkontoudtogslinjer kan ikke afstemmes, fordi der ikke findes nogen relaterede finansposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Derefter skal du bogføre en kladdelinje for hver transaktion for at oprette en relateret post, som de kan afstemmes med.

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Overfør til finanskladde**.  
2. På siden **Overfør afstemning til fin.kld** skal du angive, hvilken finanskladde du vil bruge, og derefter klikke på knappen **OK**.

    Siden **Finanskladde** åbnes. Det indeholder nye kladdelinjer for alle bankkontoudtogslinje med manglende poster.
3. Udfyld kladdelinjen med de relevante oplysninger som f.eks. modkonto. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  
4. For at få vist resultatet af bogføringen, inden du bogfører, skal du vælge handlingen **Kontrollér rapport**. Rapporten **Bankkontoudtog** åbnes og viser de samme felter som hovedet på siden **Bankkontoafstemning**.
5. Vælg handlingen **Bogfør**.

    Når posten er bogført, skal du afstemme bankkontoudtogslinjen med den.
6. Opdatere eller genåbne siden **Bankkontoafstemning**. Den nye post vises i ruden **Bankkontoposter**.
7. Matche bankkontoudtogslinjen med bankkontoposten, manuelt eller automatisk.

## <a name="undo-a-bank-account-reconciliation"></a>Fjern en bankkontoafstemning
Hvis du opdager en fejl i en bogført bankafstemning, kan du bruge handlingen **Fortryd** på siden **Bankkontoudtog** til at rette fejlen. Når du fortryder en bogført bankafstemning, flyttes posterne til siden **Bankafstemning** og markeres som **Åbne**, hvilket betyder, at de ikke er afstemt. Du kan derefter rette bankafstemningen og bogføre den igen.

> [!NOTE]
> Hvis du vil bruge Annulleringsfunktionen til bogførte bankafstemninger og bankkontoudtog i den nordamerikanske version, skal du slå **Bankafstemning med automatisk match** til på siden **Regnskabsopsætning**. Fortrydelsesfunktionen er ikke tilgængelig for bankkontoudtog, der er bogført fra bankafstemningskladder.

### <a name="reusing-the-bank-statement-number"></a>Genbrug bankkontonummer
Det bankkontonummer, der bruges til den nye bankafstemning, hentes fra bankkontoen, som er kontoens sidste balance. Du kan ændre værdierne, før du starter på en ny bankafstemning. Men når du opretter en ny bankafstemning, undersøger [!INCLUDE[d365fin](includes/d365fin_md.md)], om kontoudtogsnummeret allerede er knyttet til et bogført bankkontoudtog. Hvis nummeret er i brug, men du ønsker, at det nye bankkontoudtog skal bruge den i stedet, kan du bruge **Skift kontoudtogsnr.** handling på siden **Bankkontoafstemning**.

### <a name="examples"></a>Eksempler
Her følger nogle få eksempler på, hvordan du kan rette en fejl i en bogført bankafstemning med eller uden brug af det samme kontonummer.

#### <a name="example-1"></a>Eksempel 1
Du har bankafstemninger for januar, februar og marts. Bankkontonummeret var 100 for marts. Senere opdager du, at marts kun medtager poster indtil den 30., hvilket betyder, at der ikke mangler poster til den 31. Du skal derfor annullere bankkontoafstemningen for marts. I dette tilfælde skal du åbne siden **Bankkontoudtog**, vælge regnskabet for marts og derefter klikke på **Fortryd**. 

Den nye bankafstemning får tildelt kontonummeret 101. Hvis du vil gentildele tallet 100, skal du vælge **Skift Kontoudtogsnr.** og Skriv **100**. 

> [!TIP]
> Husk at angive den korrekte slutdato for kontoudtog (f.eks. 31. marts) og redigere feltet **Sidste kontoudtog-saldo**. 

#### <a name="example-2"></a>Eksempel 2
Du har bankafstemninger for januar, februar, juni og juli. Du opdager, at februar var forkert. Lad os antage, at det havde kontonummer 100. Som i eksempel 1 skal du bruge felterne Annuller og Skift Kontoudtogsnr. handlinger for at ændre kontoudtogsnummeret som i eksempel #1 ovenfor, og du kan nu gendanne februars bankafstemninger.  

Når du har bogført den korrigerede bankafstemning for februar, skal du på det tilhørende bankkontokort **Sidste kontoudtogsnr.** feltet viser **100**, og feltet **Sidste kontoudtog-saldo** viser slutsaldoen for februar-opgørelsen. 

Hvis den næste bankafstemning er for marts, tildeler [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 som kontokortnummeret og giver den en korrekt **Sidste kontoudtog-saldo**.

Hvis den næste bankafstemning er for august, skal du overveje at ændre værdierne i feltet **sidste kontoudtogsnr.** og felterne **Sidste kontoudtogssaldo** på **Bankkonto**-kortet, før du opretter den næste bank afstemning, eller bruger feltet Skift kontoudtogsnr. handling, og du kan også ændre værdien i feltet "Sidste kontoudtog-saldo" på siden bankafstemning.

> [!NOTE]
> Kontoudtogsnummeret er vigtigt, når du foretager bankafstemninger med importerede CAMT-filer, der indeholder Kontoudtogs numre, eller når du afstemmer baseret på udskrevne bankkontoudtog. Hvis du blot henter en række transaktioner fra din online bank, er opgørelses nummeret normalt ikke vigtigt. 
>
>Sidste kontoudtog-saldo gemmes på bankkontoen for at minimere fejl i bankafstemningerne, men den kan også redigeres, så du kan foretage bankafstemninger i den ønskede rækkefølge. Det betyder også, at hvis du fortryder et bankkontoudtog, vil den nye slutsaldo muligvis ikke være saldo sidste kontoudtog på det næste bankkontoudtog. Der er ingen funktion til at flytte en saldo frem til alle efterfølgende bankkontoudtog, så vær opmærksom på dette, når du bruger Fortryd. 

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret træning på [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]