---
title: Afstemme bankkonti
description: 'Få mere at vide om, hvordan du afstemmer posteringer i Business Central med transaktioner i kontoudtog fra banken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Afstemme bankkonti

Bankafstemning er med til at sikre, at dine bøger matcher de udtog, du modtager fra banken. Bankkontoafstemning sammenligner og matcher poster på de bankkonti, du har oprettet i [!INCLUDE[prod_short](includes/prod_short.md)], med banktransaktioner i din bank. Derefter kan du bogføre saldiene på bankkontiene i [!INCLUDE[prod_short](includes/prod_short.md)] for at gøre dem tilgængelige for økonomicheferne. Bankafstemning er også en praktisk måde at opdage og løse manglende betalinger og bogføringsfejl på.

I denne artikel beskrives, hvordan du afstemmer bankkonti på siden **Bankkontoafstemning**.

Men du kan også afstemme bankkonti på siden **Betalingsudligningskladde**, når du gennemfører betalinger. Åbne bankposter vedrørende de anvendte debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**. Det afstemmer automatisk bankkontoen for de betalinger, du bogfører, med kladden. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nordamerikanske versioner kan du også udføre dette arbejde på siden **Bankafstemningskladde**, der er mere velegnet til checks og indskud, men ikke tilbyder import af bankkontoudtogsfiler. Hvis du vil bruge denne side i stedet for siden **Bankkontoafstemning**, skal du fjerne markeringen i feltet **Bankafstemning med automatisk match** på siden **Regnskabsopsætning**. Du kan finde flere oplysninger i afsnittet [Afstemme bankkonti](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under Lokal funktionalitet for USA.

Linjerne på siden **Bankkontoafstemning** er opdelt i to ruder. Ruden **Bankkontoudtogslinjer** viser enten importerede banktransaktioner eller poster med udestående betalinger. Ruden **Bankkontoposter** viser finansposterne på en intern bankkonto.

Afstemning af transaktioner i bankkontoudtog med bankposter i [!INCLUDE[prod_short](includes/prod_short.md)] kaldes *matching*. Du kan sammenligne transaktioner med bankposter på to måder:

* Du kan vælge at matche automatisk ved hjælp af handlingen **Match automatisk**.
* Du kan også manuelt markere linjer i begge ruder for at sammenkæde de enkelte bankkontoudtogslinjer med en eller flere relaterede bankposter og derefter bruge handlingen **Match manuelt**.

Afkrydsningsfeltet **Udlignet** er markeret på linjer, hvor posterne stemmer. Du kan finde flere oplysninger i [Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md). Hvis du angiver en Kontoudtogs slutdato på bankafstemningen, efter at du har matchet linjerne med poster, fortryder [!INCLUDE [prod_short](includes/prod_short.md)] de relaterede linjer og poster, der ligger efter denne dato.

> [!NOTE]
> Når du har angivet en dato i feltet Kontoudtogs slutdato, filtrerer bankkonto posterne på siden bankposter, så der kun vises poster op til den dato. Du kan kun bogføre bankafstemninger med bankposter på eller før Kontoudtogs slutdato. Filteret sikrer, at din bankpost stemmer overens med kontoudtoget på slutdatoen, hvor differencen er de udestående betalinger og checks.

Når værdien i feltet **Saldo i alt** i ruden **Bankkontoudtogslinjer** svarer til den samlede værdi i feltet **Saldo til afstemning** plus feltet **Sidste kontoudtog-saldo** i ruden **Bankkontoposter**, kan du vælge handlingen **Bogfør** for at afstemme de udlignede bankkontoposter. Ikke-afstemte bankkontoposter forbliver på siden, hvilket indikerer uoverensstemmelser, som du skal løse for at afstemme bankkontoen.

Alle linjer, der ikke kan afstemmes og er angivet med en værdi i feltet **Difference**, forbliver på siden **Bankkontoafstemning** efter bogføring. De repræsenterer en slags uoverensstemmelse, som du skal løse, før du kan fuldføre afstemningen af bankkontoen. I følgende tabel beskrives nogle få typiske forretningssituationer, der kan være en forskel.

| Difference | Årsag  | Løsning |
|------------|--------|------------|
| En transaktion i din bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke på bankkontoudtoget. | Banktransaktionen blev ikke foretaget, selvom der blev oprettet en bogføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Opret den manglende transaktion (eller bed debitoren om at gøre det). Importer derefter bankkontoudtogsfilen igen, eller angiv transaktionen manuelt. |
| En postering på bankkontoudtoget findes ikke som et dokument eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion blev foretaget uden en tilsvarende bogføring [!INCLUDE[prod_short](includes/prod_short.md)]i, f.eks. bogføring af en kladdelinje for en udgift. | Opret og bogfør den manglende post. Du kan se en hurtig metode under [ Sådan oprettes manglende poster, som banktransaktioner skal afstemmes med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaktion på den interne bankkonto svarer til en banktransaktion, men nogle oplysninger er for forskellige til at give et match. | Oplysninger såsom beløbet eller kundenavnet blev angivet forskelligt i banktransaktionen eller den interne bogføring. | Gennemse oplysningerne, og match derefter de to manuelt. Du bør eventuelt rette uoverensstemmelsen. |

Du skal løse forskellene, f.eks. ved at oprette manglende poster og rette oplysninger, der ikke svarer til hinanden, eller ved at foretage manglende pengeposteringer, indtil afstemningen af bankkontoen kan fuldføres og bogføres.

Du kan udfylde ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning** på følgende måder:

* Automatisk, ved hjælp af funktionen **Importér bankkontoudtog** for at udfylde ruden **Bankkontoudtogslinjer** med banktransaktioner ifølge en importeret fil eller stream, der er leveret af banken.
* Manuelt ved hjælp af funktionen **Foreslå linjer** for at udfylde ruden **Bankkontoudtogslinjer** ifølge fakturaerne i [!INCLUDE[prod_short](includes/prod_short.md)], der har udestående betalinger.

## Sådan tilføjes bankafstemningslinjer ved at importere et bankkontoudtog

Ruden **Bankkontoudtogslinjer** udfyldes med bankposteringer i henhold til en importeret fil eller strøm, der er leveret af banken.

Hvis du vil indlæse bankkontoudtog som bankfeed, skal du konfigurere tjenesten Envestnet Yodlee Bank Feeds. Opsætning inkluderer sammenkædning af dine bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] til de relaterede onlinebankkonti. Du kan finde flere oplysninger i [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan også importere bankkontoudtogsfiler i komma- eller semikolonsepareret format (.CSV). Du kan bruge den assisterende opsætning **Opsæt en bankkontoudtogs filformat** for at definere importformater for bankkontoudtog og knytte formatet til en bankkonto. Du kan bruge disse formater, når du indlæser bankkontoudtog for import på siden **Bankkontoafstemning**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkontoafstemning**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Vælg den relevante bankkonto i feltet **Bankkontonr.**. Bankkontoposterne, der findes på bankkontoen, vises i ruden **Bankkontoposter**.
4. Angiv datoen for kontoudtoget fra banken i feltet **Kontoudtogsdato**.
5. Angiv saldoen fra kontoudtoget i feltet **Kontoudtogs slutsaldo**.
6. Hvis du har en bankkontoudtogsfil, skal du vælge handlingen **Importér bankkontoudtog**.
7. Find filen, og vælg derefter knappen **Åbn** for at importere banktransaktionerne til linjerne ind i ruden **Bankkontoudtogslinjer** på siden **Bankkontoafstemning**.

## Sådan udfyldes bankafstemningslinjer med funktionen Foreslå linjer

Ruden **Bankkontoudtogslinjer** udfyldes i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], der har udestående betalinger.  

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Foreslå linjer**.
2. Angiv den tidligste dato for de poster, der skal afstemmes, i feltet **Startdato**.
3. Angiv den seneste dato for de poster, der skal afstemmes, i feltet **Slutdato**.

    > [!NOTE]
    > Slutdatoen svarer typisk til den dato, der er angivet i feltet **Kontoudtogsdato**. Men hvis du vil afstemme transaktioner for en del af en periode, kan du angive en anden slutdato.

4. Hvis du ikke vil have, at bankkontoposterne skal omfatte ikke-matchede åbne tilbageførte poster, skal du vælge funktionen **Udelad tilbageførte poster**. Som standard vil listen over bankkontoposter medtage tilbageførte poster op til kontoudtogsdatoen.
5. Vælg knappen **OK**.

## Sådan afstemmes kontoudtogslinjer automatisk med bankposter

Siden **Bankkontoafstemning** indeholder automatisk matchningsfunktionalitet, der er baseret på en sammenligning af tekst i en bankkontoudtogslinje (venstre rude) med tekst i en eller flere bankkontoposter (højre rude). Du kan overskrive den foreslåede automatiske afstemning, og du kan vælge slet ikke at bruge automatisk afstemning. Du kan finde flere oplysninger i [Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Du kan undersøge udgangspunktet for matches ved at bruge handlingen **match detaljer**. Detaljerne vil f. eks. omfatte navnene på de felter, der indeholdt identiske værdier.  

1. På siden **Bankkontoafstemning** skal du vælge **Match automatisk**. Siden **Afstem bankposter** åbnes.
2. I feltet **Transaktionsdatotolerance (dage)** skal du angive antallet af dage før og efter bankpostens bogføringsdato, hvorimellem funktionen skal søge efter tilsvarende transaktionsdatoer i kontoudtoget.

    Hvis du indtaster 0 eller lader feltet stå tomt, vil funktionen **Afstem automatisk** kun søge efter afstemte transaktionsdatoer på bankpostens bogføringsdato.
3. Vælg knappen **OK**.

    Linjerne er farvekodet for at gøre det nemmere at forstå, hvad du skal gøre med dem. Bankkontoudtogslinjer og bankposter, der kan afstemmes, der matches i den aktuelle kontoafstemning, skifter til fed grøn skrifttype. Bankkontoposter, der allerede er afstemt på andre bankkontoafstemninger, vises med blå kursiv-skrifttype.
4. For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**.

> [!TIP]
> Du kan bruge en blanding af manuel og automatisk matchning. Hvis du har matchet poster manuelt, overskriver den automatiske matchning ikke dine valg.

## Sådan afstemmes bankkontoudtoglinjer manuelt med bankposter

> [!TIP]
> Når matching af linjer og poster bliver manuelt, kan **Vis alle**, **Vis tilbageførte poster**, **Skjul tilbageførte poster** og **Vis ikke-matchede** gøre det nemmere at få vist en oversigt. Bankkontoposterne indeholder som standard ikke ikke-matchede tilbageførte poster. Hvis du vil medtage disse poster på listen og matche dem manuelt, skal du vælge handlingen **Vis tilbageførte poster**. Hvis du vælger at skjule tilbageførte poster, efter at du har foretaget et eller flere match, vises de matchede poster stadig.

> [!NOTE]
> Du kan ikke bogføre en bankafstemning, hvis du foretager mange-til-én-matching, og de kombinerede beløb indeholder differencer. Dette gælder også, hvis den kombinerede difference er sat til nul.
>
> Her er et eksempel på en mange til én-matching, som har forskelle. Værdien af 200 for bankkontoudtogspost 1 er afstemt med to bankposter, der har en samlet værdi på 180. Forskellen er 20. Værdien af 350 for bankkonto 2 er matchet med to andre bankposter, der har en samlet værdi på 370. Forskellen er -20, som balancerer værdien af 20 for bankkontoudtog 1.  
>
> Hvis du vil bogføre en bankafstemning med differencer på linjerne, skal du bogføre differencerne og derefter afstemme dem mod de bogførte poster.

1. På siden **Bankkontoafstemning** skal du vælge en ikke-udlignet linje i ruden **Bankkontoudtogslinjer**:
2. I ruden **Bankkontoposter** skal du vælge en eller flere bankkontoposter, der kan afstemmes med den valgte bankkontoudtogslinje. Hvis du vil vælge flere linjer, skal du trykke på og holde <kbd>CTRL</kbd>-tasten nede og derefter markere linjerne.

   > [!TIP]
   > Du kan også manuelt sammenholde flere bankkontoudtogslinjer med én bankpost. Dette kan f. eks. være nyttigt, hvis bank indbetalingen indeholder flere betalingsmetoder, f. eks. kreditkort fra forskellige udstedere, og din bank viser dem som separate linjer.
3. Vælg handlingen **Match manuelt**.

    Den valgte bankkontoudtogslinje og de valgte bankposter ændrer farve til grøn skrifttype, og afkrydsningsfeltet **Udlignet** i højre rude markeres.
4. Gentag trin 1 til 3 for alle bankkontoudtogslinjer, der ikke er matchet.

> [!TIP]
> For at fjerne et match skal du markere bankkontoudtogslinjen og derefter vælge handlingen **Fjern match**. Hvis du har knyttet flere bankkontoudtogslinjer til en post og har behov for at fjerne en eller flere af de matchede linjer, fjernes alle de manuelle matches for posten, når du vælger **Fjern match**.

## Sådan valideres bankafstemningen

Hvis du vil dobbelttjekke bankkontoafstemningen, før du bogfører den, skal du bruge handlingen **Test rapport** til at vise en forhåndsversion af afstemningen. Følgende rapport er tilgængelig i følgende kontekster:

* Når du forbereder en bankafstemning på siden **Bankkontoafstemning**.
* Når du afstemmer betalinger på siden **Betalingsudligningskladder**.

Linjer, der ikke kan matches, bliver på siden **Bankkontoafstemning** efter bogføringen. Disse linjer indeholder en værdi i feltet **Difference**. Differencen repræsenterer en uoverensstemmelse, som du skal løse, før du kan fuldføre afstemningen af bankkontoen. I følgende tabel beskrives nogle få typiske forretningssituationer, der kan være en forskel.

| Difference | Årsag  | Løsning |
|------------|--------|------------|
| En transaktion i din bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke på bankkontoudtoget. | Banktransaktionen blev ikke foretaget, selvom der blev oprettet en bogføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Opret den manglende transaktion (eller bed debitoren om at gøre det). Importer derefter bankkontoudtogsfilen igen, eller angiv transaktionen manuelt. |
| En postering på bankkontoudtoget findes ikke som et dokument eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaktion blev foretaget uden en tilsvarende bogføring [!INCLUDE[prod_short](includes/prod_short.md)]i, f.eks. bogføring af en kladdelinje for en udgift. | Opret og bogfør den manglende post. Du kan se en hurtig metode under [ Sådan oprettes manglende poster, som banktransaktioner skal afstemmes med](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaktion på den interne bankkonto svarer til en banktransaktion, men nogle oplysninger er for forskellige til at give et match. | Oplysninger såsom beløbet eller kundenavnet blev angivet forskelligt i banktransaktionen eller den interne bogføring. | Gennemse oplysningerne, og match derefter de to manuelt. Du bør eventuelt rette uoverensstemmelsen. |

Du skal løse forskellene, f.eks. ved at oprette manglende poster og rette oplysninger, der ikke svarer til hinanden, eller ved at foretage manglende pengeposteringer, indtil afstemningen af bankkontoen kan fuldføres og bogføres.

> [!NOTE]
> Siden bank afstemning og kontrolrapporten forudsætter, at du kun skal afstemme inden for perioden indtil slutdatoen for kontoudtoget. Hvis du sammenholder en bankkontoudtogslinje med en bankpost, før du angiver en Kontoudtogs slutdato, og derefter angiver en Kontoudtogs slutdato, der ligger efter slutdatoen for bankposten, vil dataene i kontrolrapporten være forkerte.

I følgende tabel beskrives de felter i kontrolrapporten, der kan bruges til at fuldføre bankkontoafstemningen.

|Felt  |Beskrivelse  |
|---------|---------|
|Kontoudtogsdato| Den dato, der er angivet i feltet **Kontoudtogsdato** på siden **Bankkontoafstemning**.|
|Saldo på sidste kontoudtog|Den balance, der er angivet i feltet **Saldo på sidste kontoudtog** på siden **Bankkontoafstemning**. Dette udfyldes automatisk fra den seneste afstemning for den samme bankkonto. Værdien er nul, hvis det er det første bankkontoafstemning.|
|Slutsaldo for kontoudtog|Den balance, der er angivet i feltet **Kontoudtogs slutsaldo** på siden **Bankkontoafstemning**. |
|Finanskontonummer <*nummer*> saldo på <*dato*> | Saldoen på finanskontoen på kontoudtogets slutdato. Dette er den ufiltrerede saldo fra og med denne dato. Hvis din bank bruger din lokale valuta, skal denne saldo være den samme som saldoen på din bankkonto (vises i højre side af rapporthovedet), når du har matchet alle kontoudtogslinjer. Hvis der angives et tomt **()** i feltet, betyder det, at banken bruger lokal valuta.<br><br>En uoverensstemmelse i dette og de forrige felter kan angive, at du har bogført direkte på finanskontoen, eller at du bruger den samme finanskonto til flere banker, hvilket ikke anbefales. Bankerne knyttes til finanskontoen via den bankkontoens bogføringsgruppe, der er angivet for kontoen.<br><br>Kontrolrapporten viser en advarsel, hvis du har direkte bogføringer, selvom saldoen til bogføringen er nul. Direkte bogføring, der ikke balancerer, vil ofte medføre akkumulerede differencer i forbindelse med fremtidige bankafstemninger. Du skal kontrollere finanskontoen og finansposter, før du bogfører bankafstemningen. Hvis du vil vide mere om direkte bogføring, skal du [undgå at bogføre direkte](#avoid-direct-posting).|
|Finanskontonummer <*nummer*> saldo (<*LV*>) på <*dato*>| Saldoen på finanskontoen på kontoudtogets slutdato i lokal valuta. Saldoen omregnes til bankens valuta vha. den valutakurs, der var gældende på kontoudtogets slutdato. Dette er den ufiltrerede saldo fra og med denne dato. Du kan sammenligne dette med **Finanskontonr. <* nummer *> Saldo til <* dato*>* felt, hvis banken bruger en udenlandsk valuta. Værdien i feltet Finanskontonr. <* nummer *> Saldo til <* dato*>-felt for lokal valuta kan variere en smule, da valutaomregning kan medføre mindre forskelle. Bankens saldo skal være meget tæt på denne saldo.  |
|Buffer for bankkontosaldo på <*dato*>| Saldoen på bankkontoen på kontoudtogets slutdato.|
|Summen af forskelle    | Summen af forskellene for bankafstemningslinjer. Hvis du vil have adgang til detaljerne, skal du slå **Udskriv udestående transaktioner** til, når du angiver kriterier for rapporten. En difference er en bankkontoudtogslinje, der ikke passer helt til en eller flere bankposter. Du kan ikke bogføre en bankkontoafstemning, der har differencer. Du kan bogføre en bankafstemning, der indeholder bankposter, som ikke stemmer overens med kontoudtogslinjer. Værdien vises i feltet **Udestående banktransaktioner** og i en separat sektion, hvis du aktiverer skift til/fra for Udskriv udestående transaktioner.      |
|Kontoudtog - saldo     | Den værdi, der er angivet i feltet **Kontoudtogs slutsaldo** på siden **Bankkontoafstemning**.  |
|Udestående banktransaktioner     | Summen af ikke-afstemte ikke-checkede bankposter med en bogføringsdato på eller før kontoudtogets slutdato. Dette sker, når du registrerer transaktioner, før de registreres i din bank. F.eks. ved slutningen af en periode. Når du opretter den næste bankafstemning, kan du afstemme disse poster.        |
|Udestående checks     | Summen af ikke-afstemte checkede bankposter med en bogføringsdato på eller før kontoudtogets slutdato. Dette sker, når du registrerer transaktioner, før de registreres i din bank. Dette kan f.eks. ske til kontrol, hvis en leverandør ikke indlæser en check i samme periode, som du har registreret den. Når du opretter den næste bankafstemning, kan du afstemme disse poster.        |
|Bankkontosaldo     | Summen af værdierne for kontoudtogets slutsaldo, udestående banktransaktioner og udestående check. Når du har behandlet alle differencer i matchede poster, svarer saldoen til din banksaldo. Du har f.eks. angivet en konto for alle matchede poster og de poster, som du ikke kunne matche for bankkontoudtoget. Du kan nu bogføre afstemningen.        |

> [!TIP]
> Hvis du kører **Test rapport** fra siden **Betalingsafstemningskladde**, beregner [!INCLUDE [prod_short](includes/prod_short.md)] værdien i **kontoudtogets slutsaldo** på følgende måde:
>
> * saldo sidste kontoudtog + summen af alle linjer i kladden til afstemning af betaling
>
> Du kan bruge den værdi, der skal sammenlignes med bankkontoudtoget.

## Sådan oprettes manglende finansposter, som bankkontoudtogslinjer skal matches med

Undertiden indeholder bankafstemninger beløb for renter eller gebyrer. Sådanne bankkontoudtogslinjer kan ikke matches, fordi der ikke findes nogen relaterede finansposter i [!INCLUDE[prod_short](includes/prod_short.md)]. Derefter skal du bogføre en kladdelinje for hver transaktion for at oprette en relateret post, som de kan afstemmes med.

1. På siden **Bankkontoafstemning** skal du vælge handlingen **Overfør til finanskladde**.  
2. På siden **Overfør afstemning til fin.kld** skal du angive, hvilken finanskladde du vil bruge, og derefter klikke på knappen **OK**.

    Siden **Finanskladde** åbnes med nye kladdelinjer for alle bankkontoudtogslinjer, der mangler sagsposter.
3. Udfyld kladdelinjen med de relevante oplysninger som f.eks. modkontoen. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  
4. Hvis du vil have vist resultatet af bogføringen, inden du bogfører, skal du vælge handlingen **Testrapport** og derefter vælge en indstilling for at få adgang til rapporten. Rapporten **Bankkontoudtog** viser de samme felter som hovedet på siden **Bankkontoafstemning**.
5. Vælg handlingen **Bogfør**.

    Når posten er bogført, skal du matche bankkontoudtogslinjen med den.
6. Opdatere eller genåbne siden **Bankkontoafstemning**. Den nye post vises i ruden **Bankkontoposter**.
7. Matche bankkontoudtogslinjen med bankkontoposten, manuelt eller automatisk.

## Finde udestående transaktioner i tidligere perioder

Du kan bruge rapporten bankkontoudtog til at finde frem til de udestående transaktioner i tidligere perioder. Udestående transaktioner blev åbnet før kontoudtogsdatoen og er ikke blevet lukket eller blev lukket, efter at bankafstemningen blev bogført.

Når du kører rapporten bankkontoudtog fra siden Bankkontoudtogsoversigt, kan du aktivere funktionen **Udestående poster**, så rapporten vil indeholde en sektion med en liste over udestående poster.

**Eksempel**: Vi har bankkontofinansposterne A, B og C på vores bankkonto for august måned. Når vi afstemmer vores bankkonto for august, finder vi en bankkontoudtogslinje, der matcher post A, men ingen for B og C. Så vi bogfører afstemningen med post A afstemt og B og C som udestående poster.

I september modtager vi betaling for post B og beslutter at afstemme vores bankkonto. Hvis vi kører rapporten Bankkontoudtog før bogføring af afstemningen, har vi én afstemt transaktion og én udestående.

Hvis vi udskriver rapporten for august, vil vi have udestående transaktioner til vores B- og C-poster, selvom vi har lukket post B i september.

## Fjern en bankkontoafstemning

Hvis du opdager en fejl i en bogført bankafstemning, kan du bruge handlingen **Fortryd** på siden **Bankkontoudtogsliste** til at rette den. Når du fortryder en bogført bankafstemning, flyttes posterne til siden **Bankafstemning** og markeres som **Åbne**, hvilket betyder, at de ikke er afstemt. Du kan derefter rette bankafstemningen og bogføre den igen.

> [!NOTE]
> Hvis du vil bruge Annulleringsfunktionen til bogførte bankafstemninger og bankkontoudtog i den nordamerikanske version, skal du slå **Bankafstemning med automatisk match** til på siden **Regnskabsopsætning**. Fortrydelsesfunktionen er ikke tilgængelig for bankkontoudtog, der er bogført fra bankafstemningskladder.

### Genbrug bankkontonummer

Det bankkontonummer, der bruges til den nye bankafstemning, hentes fra bankkontoen, som er kontoens sidste balance. Du kan ændre værdierne, før du starter på en ny bankafstemning. Men når du opretter en ny bankafstemning, undersøger [!INCLUDE[d365fin](includes/d365fin_md.md)], om kontoudtogsnummeret allerede er knyttet til et bogført bankkontoudtog. Hvis nummeret er i brug, men du ønsker, at det nye bankkontoudtog skal bruge den i stedet, kan du bruge **Skift kontoudtogsnr.** handling på siden **Bankkontoafstemning**.

### Eksempler

Her følger nogle eksempler på, hvordan du kan rette en fejl i en bogført bankafstemning med eller uden brug af det samme kontonummer.

#### Eksempel 1

Du har bankafstemninger for januar, februar og marts. Bankkontonummeret var 100 for marts. Senere opdager du, at marts kun medtager poster indtil den 30., hvilket betyder, at der ikke mangler poster til den 31. Du skal derfor annullere bankkontoafstemningen for marts. I dette tilfælde skal du åbne siden **Bankkontoudtog**, vælge regnskabet for marts og derefter klikke på **Fortryd**. 

Den nye bankafstemning får tildelt kontonummeret 101. Hvis du vil gentildele tallet 100, skal du vælge **Skift Kontoudtogsnr.** og Skriv **100**. 

> [!TIP]
> Husk at angive den korrekte slutdato for kontoudtog (f.eks. 31. marts) og redigere feltet **Sidste kontoudtog-saldo**. 

#### Eksempel 2

Du har bankafstemninger for januar, februar, juni og juli. Du opdager, at februar var forkert. Lad os antage, at det havde kontonummer 100. Som i eksempel 1 skal du bruge felterne Annuller og Skift Kontoudtogsnr. handlinger for at ændre kontoudtogsnummeret som i eksempel #1 ovenfor, og du kan nu gendanne februars bankafstemninger.  

Når du har bogført den korrigerede bankafstemning for februar, skal du på det tilhørende bankkontokort **Sidste kontoudtogsnr.** feltet viser **100**, og feltet **Sidste kontoudtog-saldo** viser slutsaldoen for februar-opgørelsen. 

Hvis den næste bankafstemning er for marts, tildeler [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 som kontokortnummeret og giver den en korrekt **Sidste kontoudtog-saldo**.

Hvis den næste bankafstemning er for august, skal du overveje at ændre værdierne i feltet **sidste kontoudtogsnr.** og felterne **Saldo på sidste kontoudtog** på **Bankkonto**-kortet, før du opretter den næste bankafstemning eller bruger feltet **Skift kontoudtogsnr.** handling, og du kan også ændre værdien i feltet **Saldo på sidste kontoudtog** på siden til bankafstemning.

> [!NOTE]
> Kontoudtogsnummeret er vigtigt, når du foretager bankafstemninger med importerede CAMT-filer, der indeholder Kontoudtogs numre, eller når du afstemmer baseret på udskrevne bankkontoudtog. Hvis du blot henter en række transaktioner fra din online bank, er opgørelses nummeret normalt ikke vigtigt.  
>
> Sidste kontoudtog-saldo gemmes på bankkontoen for at minimere fejl i bankafstemningerne, men den kan også redigeres, så du kan foretage bankafstemninger i den ønskede rækkefølge. Det betyder også, at hvis du fortryder et bankkontoudtog, vil den nye slutsaldo muligvis ikke være saldo sidste kontoudtog på det næste bankkontoudtog. Der er ingen funktion til at flytte en saldo frem til alle efterfølgende bankkontoudtog, så vær opmærksom på dette, når du bruger Fortryd.  

## Undgå direkte bogføring

Undlad at bruge en finanskonto, der tillader direkte bogføring i din bankkontos bogføringsgruppe. Den direkte bogføring vil afbryde forbindelsen mellem bankkontoens finanspost og finanskontoens finanspost. Når du afstemmer din bankkonto, vil poster, der bogføres direkte på finanskontoen, ikke blive medtaget, og det vil være vanskeligt at fuldføre afstemningen.

Fejlen opstår ofte, når der angives en primosaldo for en bankkonto. Det er vigtigt, at du ikke bogfører primosaldoen direkte i finansregnskabet. De poster på finanskontoen, der bogføres direkte på finanskontoen, vil medføre problemer. Disse poster kan f.eks. forhindre dig i at afstemme din bankkonto. I forbindelse med bankkonti i udenlandsk valuta kan posterne skabe øgede differencer, når du bogfører flere bankafstemninger, pga. valutakursreguleringer. Du bogfører ofte primosaldoen direkte på bankkontoen, og beløbet ophører derefter med finanskontoen. Alternativt kan du tilbageføre den senere til en angivet finanskonto, som du har brugt til at afstemme primosaldoen med finansbalancen. I begge tilfælde skal du udligne en direkte bogføring til finanskontoen, før du starter din første bankafstemning, og især hvis bankkontoen er i udenlandsk valuta.

## Se relateret [Microsoft-træning](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## Se også

[Bankkontoafstemning](bank-manage-bank-accounts.md)  
[Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktransaktioner](bank-setup-banking.md)  
[Konfigurere regler for automatisk udligning af betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
