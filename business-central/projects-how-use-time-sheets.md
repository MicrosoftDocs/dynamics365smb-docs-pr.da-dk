---
title: Bruge timesedler
description: 'Beskriver, hvordan du opretter en timeseddel, definerer arbejdstyper, udfylde timesedlen og sender den til godkendelse.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 03/01/2022
ms.author: bholtorf
---
# Bruge timesedler

Du kan bruge timesedler i [!INCLUDE [prod_short](includes/prod_short.md)] til at spore fravær og spore tid og ressourcer, der er brugt på et projekt. Med tidsstyring kan du nemt identificere problemer tidligt og undgå forsinkelser eller overskridelser af omkostninger. Med timesedler kan en ressource nemt rapportere tidsforbrug for en enkeltperson eller en maskine, og en leder let kan gennemgå forbruget og fordelingen. Denne artikel beskriver, hvordan du opretter en timeseddel, definerer arbejdstyper, udfylde timesedlen og sender den til godkendelse.  

Du kan kopiere og bruge dine sagsplanlægningslinjer i en timeseddel. På denne måde må du kun indtaste oplysninger på ét sted, og linjeoplysningerne vil altid være korrekte.

Når du har godkendt timeseddelposter for en sag, kan du bogføre dem i den relevante sagskladde eller ressourcekladde.

Før du kan bruge timesedler, skal du angive generelle oplysninger og angive en administrator og en eller flere godkendere af timesedler. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).  

> [!TIP]
> Fra 2021 udgivelsesbølge 2 kan du administrere tildelte timesedler på en mobil enhed. Din administrator skal evt. aktivere **Funktionsopdatering: ny funktion til visning af timesedler** på siden [Funktionsstyring](https://businesscentral.dynamics.com/?page=2610) for at bruge denne funktion. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

## Sådan opretter du timesedler

Du kan bruge kørslen **Opret timesedler** til at oprette timesedler for et angivet antal tidsperioder eller uger. Derefter kan timesedlens ejer åbne den og registrere tid, der har været brugt på en opgave. Du kan også [planlægge batchjobbet til at køre automatisk](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Du skal have tilladelser for at kunne oprette timesedler. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.
2. På siden **Timesedler** skal du vælge handlingen **Opret timesedler**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Felterne **Brug timeseddel** og **Bruger-id for timeseddelejer** skal udfyldes på kortet for ressourcen for timesedlen.

    Du kan også vælge at vælge handlingen **Tidsplan** for at angive, hvor ofte opgaven skal udføres automatisk. Hvis du f. eks. vil konfigurere en opgave, så den kører en gang om ugen i fire uger, skal du indstille på siden **Planlæg en rapport - Opret tidsark** feltet **Datoformel for næste kørsel** til *4U*. Du kan få flere oplysninger [Planlægge en rapport til kørsel](ui-work-report.md#ScheduleReport).  
4. Vælg knappen **OK**.  

Du kan se de timesedler, du har oprettet, på siden **Timesedler**. Hver timeseddel består af en eller flere linjer, der definerer den tid, du vil sende til godkendelse. I følgende tabel beskrives de typer af linjer, du kan føje til en timeseddel.

| **Felt** | **Beskrivelse** |
|---|---|
| | Bruges til at tilføje en note eller en markering i feltet **Beskrivelse** på timeseddellinjen. Du kan f.eks. bruge dette felt til at kategorisere timeseddelposter. Hvis du lader feltet **Type** for en timeseddellinje være tomt, kan du ikke angive tidsværdier i ugedagsfelterne for den pågældende linje. |
| Fravær | Bruges til at registrere den tid, du er fraværende i en arbejdsuge. Hvis du vil udfylde oplysningerne for linjen, skal du angive typen af fravær i feltet **Fraværsårsagskode**. |
| Montageordre | Bruges til at registrere tid for montageordrer. En timeseddellinje af denne type oprettes under bogføringen af montageordrelinjer, hvor ressourcen er konfigureret til at bruge timesedler. Du kan ikke manuelt vælge en linje af denne type. |
| Sag | Bruges til at registrere tidsforbrug for et projekt. Hvis du vil udfylde oplysningerne for linjen, skal du angive det sagsnummer og det sagsopgavenummer, du vil registrere tid for. Du kan registrere tid for linjer, du ikke har planlagt.|
| Ressource | Bruges til at registrere tidsforbrug for en ressource. Hvis du vil udfylde oplysningerne for linjen, skal du angive en beskrivelse af arbejdet. |
| Tjeneste | Bruges til at registrere tidsforbrug for en serviceordre eller en servicekreditnota. |

Hvis du f. eks. vil indsende en timeseddel for en arbejdsuge, hvor du har arbejdet på oprydningsopgaver de fleste dage, men har haft en fridag på grund af lægeaftaler, skal du tilføje linjer som vist i følgende tabel.

| Type | Beskrivlse | Arbejdstypekode | Fraværstypekode |
|--|--|--|--|
| Ressource | Arbejdstimer | Rengøring |  |
| Fravær | Fri |  | Sundhed |
|  | Jeg var nødt til at tage fri tirsdag grundet en lægeaftale. |  |  |

I dette hypotetiske eksempel skal du registrere de relevante timer på tværs af de relevante dage i felterne for hver ugedag.  

> [!TIP]
> I de fleste tilfælde har din virksomhed foruddefinerede arbejdstyper for de forskellige linjetyper. I disse tilfælde skal du bare vælge den relevante arbejdstype på listen, og derefter skal du tilføje din egen beskrivelse.  
>
> Vælg arbejdstypen ved at vælge knappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i feltet **Beskrivelse** ved at vælge handlingen **Aktivitetsdetaljer** og derefter angive den på den side, der åbnes, eller ved at vælge den i feltet **Arbejdstypekode** eller feltet **Fraværstypekode**. Hvis det er tilfældet, kan du ignorere afsnittet [Sådan definerer du arbejdstyper og tilføjer en til en timeseddel](#to-define-work-types-and-add-one-to-a-time-sheet).  

## Sådan genbruges timeseddellinjer i andre timesedler

Hvis dine timeseddeloplysninger forbliver de samme fra tidsperiode til tidsperiode, kan du spare tid ved at kopiere linjerne fra den forrige tidsperiode. Derefter skal du kun angive tidsforbruget for den nye periode.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Åbn timesedlen for en period efter perioden for en eksisterende timeseddel med linjer.  
3. Vælg handlingen **Kopier linjer fra en tidligere timeseddel**.

Linjerne kopieres, herunder oplysninger som type og beskrivelse. Hvis linjen f.eks. er knyttet til en sag, kopieres **Sagsnr.**. Alle kopierede linjer har statussen **Åben**. Du kan nu redigere linjerne efter behov.

## Sådan kopieres sagsplanlægningslinjer til en timeseddel
Følgende procedure beskriver, hvordan du hurtigt føjer sagsplanlægningslinjer til en timeseddel.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Vælg en timeseddel for den relevante periode på siden **Timesedler**.  
3. Vælg handlingen **Opret linjer fra sagsplanlægning**. Alle sagsplanlægningslinjer i timeseddeltidsperioden kopieres til timesedlen for personen eller maskinen i feltet **Ressourcenr.** på timesedlen.

## Sådan definerer du arbejdstyper og tilføjer en til en timeseddel

Du kan definere arbejdstypen for alle timeseddellinjer for serviceordrer, sagsordrer og ressourcer. På denne måde kan du tilføje oplysninger, du behøver for at fakturere debitoren for forskellige typer arbejde.  

1. På siden **Timesedler** skal du vælge den relevante timeseddel.
2. Vælg feltet **Type** på den første af linjerne i afsnittet **Linjer**, og vælg derefter den relevante type, f.eks. *Ressource*.  
3. Vælg feltet **Beskrivelse**, og udfyld felterne på siden **Res.detaljer for timeseddellinje**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Hvis der ikke findes nogen arbejdstyper, skal du vælge handlingen **Ny**.
    2. På siden **Arbejdstyper** skal du udfylde felterne efter behov og derefter returnere til timesedlen.
4. Udfyld resten af timesedlen. Du kan finde flere oplysninger i afsnittet [Sådan udfyldes en timeseddels linjer og sendes til godkendelse](#to-fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Lignende trin gælder for definition af fraværskoder.

## Sådan udfyldes en timeseddels linjer og sendes til godkendelse

Registrering af timesedler spores i timer, standardbasisenheden for ressourcer. En timeseddel har som standard almindelige arbejdsdage fra mandag til fredag.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Vælg en timeseddel for den relevante periode.
3. Udfyld felterne på en linje efter behov. Angiv det antal timer, der bruges af ressourcen på hver ugedag.  

    Hvis du vil spore arbejde, skal du i de fleste tilfælde tilføje en linje af typen *Ressource* og derefter registrere de timer, der er brugt hver dag. Hvis du vil registrere fravær, skal du tilføje en linje af typen *Fravær*.  

    > [!TIP]  
    > Du kan se summen af timeseddeltimer, du har angivet i faktaboksen **Faktisk/budgetteret oversigt**.  
4. Gentag trin 3 for andre arbejdstyper, der udføres af ressourcen.  

    Derefter skal du beslutte, om du vil sende alle linjer på timesedlen, eller om du vil sende enkelte linjer.  

    * Hvis du vil sende en timeseddel for en eller flere linjer, skal du vælge den relevante linje og derefter vælge handlingen **Send**.

        På afsendelsessiden skal du vælge **Kun valgte linjer**. Linjen skifter tilstand fra *Åben* til *Sendt*.
    * Hvis du vil sende timesedlen for alle åbne linjer, skal du vælge handlingen **Send** øverst på siden **Timeseddel**.  

        Du bliver bedt om at bekræfte, at du vil sende alle åbne linjer i den aktuelle timeseddel.  

    > [!NOTE]  
    > Du kan dog kun sende timeseddellinjer, som du har angivet tidspunkter for.  
5. Hvis du vil ændre oplysningerne på en linje, der er indstillet til **Sendt**, skal du markere linjen og derefter vælge handlingen **Åbn igen**.

    > [!NOTE]  
    >   En leder kan afvise en timeseddellinje, der er sendt til godkendelse. Hvis en linje har statussen **Afvist**, kan du foretage ændringer i linjen og derefter vælge **Send** igen.  
6. Vælg knappen **OK**.

## Sådan godkendes eller afvises en timeseddel
En timeseddel skal sendes til godkendelse, før den kan bruges. Du kan godkende og afvise individuelle linjer på en timeseddel eller sende dem tilbage til afsenderen til yderligere behandling. En timeseddel kan godkendes på to måder:

* En timeseddeladministrator kan godkende enhver timeseddel.
* Den person, der er angivet i feltet **Bruger-id for timeseddelgodkender** på et ressourcekort, kan godkende timesedler for den pågældende ressource. Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leders timesedler**, og vælg derefter det relaterede link.
2. Vælg en timeseddel på listen.  
3. På siden **Timeseddel** 
    1. Vælg **Behandle**-handlingen, og vælg derefter **Godkend**.
    2. Vælg handlingen **Alle sendte linjer** for at godkende alle linjer, eller handlingen **Kun valgte linjer** for at godkende linjer, der er valgt på siden **Timeseddel**.
4. Vælg knappen **OK**.  
5. Du kan også vælge handlingen **Afvis** og følge trin 4 til 5.  

> [!TIP]  
>   Brug faktaboksene **Timeseddelstatus** og **Faktisk/budgetteret oversigt** for at få et overblik over timeseddeloplysninger.

Når du har godkendt eller afvist en timeseddel, kan den ikke redigeres, medmindre den er blevet genåbnet. Følgende fremgangsmåde beskriver, hvordan du genåbner en godkendt eller afvist timeseddel.

## Sådan genåbnes en timeseddel
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leders timesedler** eller **Timesedler**, og vælg derefter det relaterede link.
2. Åbn en timeseddel på listen.  

    > [!NOTE]  
    >   Du kan kun åbne linjer med statussen **Godkendt**. Du kan ikke genåbne linjer med statussen **Afvist**. Du kan ikke genåbne en timeseddel, hvis den er blevet bogført.  
3. På siden **Timeseddel** skal du vælge handlingen **Åbn igen** og derefter vælge handlingen **Alle sendte linjer** for at åbne alle linjer igen eller handlingen **Kun valgte linjer** for kun at åbne de linjer, der er valgt på siden **Timeseddel**, igen.
4. Vælg knappen **OK**. Status for timeseddellinjerne er ændringer for **Sendt**.  

## Sådan kan du se og godkende en timeseddel efter sag

Du kan for en sag angive en person, der er ansvarlig for sagen. Disse oplysninger er knyttet til timeseddellinjer og kan bruges til at angive en liste over timesedler, som en projektleder skal gennemse og godkende. Teamprojektlederen kan for eksempel være ansvarlig for bestemte sager i din virksomhed. I så fald bør lederen udpeges som **Ansvarlig person** på sagskortet. Du kan se sagsopgaver, der er knyttet til en sag, og antal timer brugt, i denne visning af timeseddeloplysninger.

> [!NOTE]
> Du skal godkende timesedler i vinduet **Leders timeseddel efter sag**, når du har valgt en indstilling for **Timeseddel efter sagsgodkendelse** på siden **Ressourceopsætning**. Der er flere oplysninger i [Konfigurere ressourcer](projects-how-setup-resources.md).

### Sådan godkendes eller afvises en timeseddel efter sag

1. Indtast **Leders timeseddel efter sag** i feltet **Søg**, og vælg derefter det relaterede link. [!INCLUDE[prod_short](includes/prod_short.md)] viser en liste over timeseddellinjer, der er knyttet til de job, du har ansvaret for.
2. Vælg handlingen **Godkend**, og vælg derefter handlingen **Alle sendte linjer** for at godkende alle linjer eller handlingen **Kun valgte linjer** for kun at godkende de linjer, der er valgt på siden **Timeseddel**.

    > [!NOTE]
    > Du kan kun godkende timesedler med status **Sendt**.

3. Hvis du vil angive yderligere oplysninger om godkendelse eller afvisning, skal du vælge den **relaterede** handling, derefter vælge **bemærkninger** og derefter **Linjebemærkninger** og skrive bemærkninger.
4. Vælg knappen **OK**.

> [!NOTE]
> Når du har godkendt eller afvist en timeseddellinje efter sag, kan den ikke åbnes igen eller ændres i vinduet **Timeseddel**.

## Sådan bogfører du timeseddellinjer i en ressourcekladde
Når du har godkendt timeseddelposter for en ressource, kan du bogføre dem i den relevante ressourcekladde.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcekladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. På siden **Foreslå res.kladdelinjer** skal du udfylde felterne efter behov.  
4. Vælg knappen **OK**. Der oprettes poster for forbrug i ressourcekladden, hvor du kan ændre oplysningerne efter behov.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Ressourceposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## Sådan bogfører du timeseddellinjer i en sagskladde
Når du har godkendt timeseddelposter for en sag, kan du bogføre dem i den relevante sagskladde.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. På siden **Foreslå Job kladdelinjer** skal du udfylde felterne efter behov.  
4. Vælg knappen **OK**. Der oprettes poster for forbrug i sagskladden, hvor du kan ændre oplysningerne efter behov.  

    > [!NOTE]  
    >   Oplysninger om arbejdstype, og om arbejdet er fakturerbart, kopieres fra timeseddellinjen. Du kan om nødvendigt reducere antallet af timer og foretage en delvis bogføring. Hvis du reducerer antallet, sker der følgende: Næste gang, du vælger handlingen **Foreslå linjer fra timesedler**, vil den linje, der oprettes, indeholde den resterende mængde timer.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Sagsposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## Sådan arkiveres timesedler
Når du har bogført timesedler, kan du arkivere dem til fremtidig reference. Alle linjer på timesedler skal bogføres, før en timeseddel kan arkiveres.

> [!NOTE]  
>   Når du arkiverer en timeseddel, fjernes den fra oversigterne på siden **Timesedler** og på siden **Leders timesedler**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.
2. Vælg handlingen **Flyt timesedler til arkiv**.  
3. På siden **Flyt timesedler til arkiv** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.  
4. Hvis du vil se arkiverede timesedler, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arkiver for timesedler** eller **Arkiver for leders timesedler**, og vælg derefter det relaterede link.

## Se også
[Projektstyring](projects-manage-projects.md)  
[Konfigurere projektstyring](projects-setup-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]