---
title: Bruge timesedler
description: 'Få mere at vide om, hvordan du opretter, sender, godkender og bogfører timesedler for ressourcer, projekter og tjenester.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 02/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Bruge timesedler

Denne artikel indeholder en beskrivelse af, hvordan du kan bruge timesedler til at spore fravær og spore tid og ressourcer, der er brugt på et projekt. Med tidssporing kan du nemt identificere problemer tidligt og undgå forsinkelser eller overskridelser af omkostninger. Med timesedler kan en ressource nemt rapportere tidsforbrug for en enkeltperson eller en maskine, og en leder let kan gennemgå forbruget og fordelingen.

Du kan kopiere og bruge dine projektplanlægningslinjer i en timeseddel. På denne måde må du kun indtaste oplysninger på ét sted, og linjeoplysningerne vil altid være korrekte. Du finder flere oplysninger i [Sådan kopieres projektplanlægningslinjer til en timeseddel](#copy-project-planning-lines-to-a-time-sheet).

Når du godkender timeseddelposter for et projekt, kan du bogføre dem i den relevante projektkladde eller ressourcekladde. Du kan få mere at vide ved at gå til [Sådan bogføres timeseddellinjer i en projektkladde](#post-time-sheet-lines-in-a-project-journal) og [Sådan bogføres timeseddellinjer i en ressourcekladde](#post-time-sheet-lines-in-a-resource-journal).

Før du kan bruge timesedler, skal du angive generelle oplysninger og angive en administrator og en eller flere godkendere af timesedler. Du kan få mere at vide om opsætning af timesedler ved at gå til [Opsætning af timesedler](projects-how-setup-time-sheets.md).  

> [!TIP]
> Du kan bruge timesedler på en mobilenhed. For at gøre det skal du muligvis aktivere til/fra-knappen **Brug ny timeseddeloplevelse** på siden [Ressourceopsætning](https://businesscentral.dynamics.com/?page=462).

## <a name="create-time-sheets"></a>Opret timesedler

Du kan bruge siden **Opret timesedler** til at oprette timesedler for et angivet antal tidsperioder eller uger. Derefter kan timesedlens ejer åbne den og registrere tid, der har været brugt på en opgave. Du kan også [planlægge batchprojektet til at køre automatisk](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Du skal have tilladelser til at oprette timesedler. Du kan få mere at vide om tilladelser ved at gå til [Konfigurere timesedler](projects-how-setup-time-sheets.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret timesedler**, og vælg derefter det relaterede link.

    > [!TIP]
    > Du kan også bruge handlingen **Opret timesedler** på listesiden **Ressourcer** og siden **Ressourcekort**.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Før du opretter timesedler for en ressource, skal du sørge for, at felterne **Brug timeseddel** og **Bruger-id** for timeseddelejer er angivet for dem på siden **Ressourcekort**.

    Du kan også vælge at vælge handlingen **Tidsplan** for at angive, hvor ofte opgaven skal udføres automatisk. Hvis du f. eks. vil konfigurere en opgave, så den kører en gang om ugen i fire uger, skal du indstille på siden **Planlæg en rapport - Opret tidsark** feltet **Datoformel for næste kørsel** til **4U**. Hvis du vil vide mere om planlægning, skal du fortsætte med at [Planlægge, at rapporten skal køres](ui-work-report.md#ScheduleReport).  

Du kan se de timesedler, du opretter, på siden **Timesedler**. Hver timeseddel består af en eller flere linjer, der definerer den tid, du vil sende til godkendelse. I følgende tabel beskrives de typer af linjer, du kan føje til en timeseddel.

| **Felt** | **Beskrivelse** |
|---|---|
| | Bruges til at tilføje en note eller en markering i feltet **Beskrivelse** på timeseddellinjen. Du kan f.eks. bruge dette felt til at kategorisere timeseddelposter. Hvis du lader feltet **Type** for en timeseddellinje være tomt, kan du ikke angive tidsværdier i ugedagsfelterne for den pågældende linje. |
| Fravær | Bruges til at registrere den tid, du er fraværende i en arbejdsuge. Hvis du vil udfylde oplysningerne for linjen, skal du angive typen af fravær i feltet **Fraværsårsagskode**. |
| Montageordre | Bruges til at registrere tid for montageordrer. En timeseddellinje af denne type oprettes under bogføringen af montageordrelinjer, hvor ressourcen er konfigureret til at bruge timesedler. Du kan ikke manuelt vælge en linje af denne type. |
| Projekt | Bruges til at registrere tidsforbrug for et projekt. Hvis du vil udfylde oplysningerne for linjen, skal du angive det projektnummer og det projektopgavenummer, du vil registrere tid for. Du kan registrere tid for linjer, du ikke har planlagt.|
| Ressource | Bruges til at registrere tidsforbrug for en ressource. Hvis du vil udfylde oplysningerne for linjen, skal du angive en beskrivelse af arbejdet. |
| Tjeneste | Bruges til at registrere tidsforbrug for en serviceordre eller en servicekreditnota. |

For eksempel vil du indsende en timeseddel for en uge, hvor du udførte rengøringsopgaver og havde en fridag til en lægeaftale. Følgende tabel viser, hvordan du vil tilføje linjer til timesedlen.

| Enhedstype | Beskrivelse | Arbejdstypekode | Fraværstypekode |
|--|--|--|--|
| Ressource | Arbejdstimer | Rengøring |  |
| Fravær | Fri |  | Tilstand |
|  | Jeg var nødt til at tage fri tirsdag grundet en lægeaftale. |  |  |

I dette hypotetiske eksempel kan du registrere de timer på tværs af de relevante dage for hver ugedag.  

> [!TIP]
> I de fleste tilfælde har din virksomhed foruddefinerede arbejdstyper for de forskellige linjetyper. I disse tilfælde skal du bare vælge den relevante arbejdstype på listen, og derefter skal du tilføje din egen beskrivelse.  
>
> Vælg arbejdstypen ved at vælge knappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i feltet **Beskrivelse** ved at vælge handlingen **Aktivitetsdetaljer** og derefter angive den på den side, der åbnes, eller ved at vælge den i feltet **Arbejdstypekode** eller feltet **Fraværstypekode**. Hvis det er tilfældet, kan du ignorere afsnittet [Sådan definerer du arbejdstyper og tilføjer en til en timeseddel](#define-work-types-and-add-one-to-a-time-sheet).  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Sådan genbruges timeseddellinjer i andre timesedler

Hvis dine timeseddeloplysninger forbliver de samme fra tidsperiode til tidsperiode, kan du spare tid ved at kopiere linjerne fra den forrige tidsperiode. Derefter skal du kun angive tidsforbruget for den nye periode.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Åbn timesedlen for en period efter perioden for en eksisterende timeseddel med linjer.  
3. Vælg handlingen **Kopier linjer fra en tidligere timeseddel**.

Linjerne kopieres, herunder oplysninger som type og beskrivelse. Hvis linjen f.eks. er knyttet til et projekt, kopieres **Projektnr.** . Alle kopierede linjer har statussen **Åben**. Du kan nu redigere linjerne efter behov.

## <a name="copy-project-planning-lines-to-a-time-sheet"></a>Kopiere projektplanlægningslinjer til en timeseddel

Følgende procedure beskriver, hvordan du hurtigt føjer projektplanlægningslinjer til en timeseddel.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Vælg en timeseddel for den relevante periode på siden **Timesedler**.  
3. Vælg handlingen **Opret linjer fra projektplanlægning**. Alle projektplanlægningslinjer i timeseddeltidsperioden kopieres til timesedlen for personen eller maskinen i feltet **Ressourcenr.** på timesedlen.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Sådan definerer du arbejdstyper og tilføjer en til en timeseddel

Du kan definere arbejdstypen for alle timeseddellinjer for serviceordrer, projektordrer og ressourcer. På denne måde kan du tilføje oplysninger, du behøver for at fakturere debitoren for forskellige typer arbejde.  

1. På siden **Timesedler** skal du vælge den relevante timeseddel.
2. Vælg feltet **Type** på den første af linjerne i afsnittet **Linjer**, og vælg derefter den relevante type, f.eks. *Ressource*.  
3. Vælg feltet **Beskrivelse**, og udfyld felterne på siden **Res.detaljer for timeseddellinje**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Hvis der ikke findes nogen arbejdstyper, skal du vælge handlingen **Ny**.
    2. På siden **Arbejdstyper** skal du udfylde felterne efter behov og derefter returnere til timesedlen.
4. Udfyld resten af timesedlen. Du kan finde flere oplysninger i afsnittet [Sådan udfyldes en timeseddels linjer og sendes til godkendelse](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Du kan følge lignende trin for at definere fraværskoder.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Sådan udfyldes en timeseddels linjer og sendes til godkendelse

Registrering af timesedler spores i timer, standardbasisenheden for ressourcer. En timeseddel har som standard almindelige arbejdsdage fra mandag til fredag.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.  
2. Vælg en timeseddel for den relevante periode.
3. Udfyld felterne på en linje efter behov. Angiv det antal timer, der bruges af ressourcen på hver ugedag.  

    Hvis du vil spore arbejde, skal du i de fleste tilfælde tilføje en linje af typen *Ressource* og derefter registrere de timer, der er brugt hver dag. Hvis du vil registrere fravær, skal du tilføje en linje af typen *Fravær*.  

    > [!TIP]  
    > Du kan se summen af timeseddeltimer, du har angivet i faktaboksen **Faktisk/budgetteret oversigt**.  
4. Gentag trin 3 for andre arbejdstyper, der udføres af ressourcen.  

    Derefter skal du beslutte, om du vil sende alle eller valgte linjer på timesedlen.  

    * Hvis du vil sende en timeseddel for en eller flere linjer, skal du vælge den relevante linje og derefter vælge handlingen **Send**.

        På afsendelsessiden skal du vælge **Kun valgte linjer**. Linjen skifter tilstand fra **Åben** til **Sendt**.
    * Hvis du vil sende timesedlen for alle åbne linjer, skal du vælge handlingen **Send** øverst på siden **Timeseddel**.  

        Bekræft, at du vil sende alle åbne linjer i den aktuelle timeseddel.  

    > [!NOTE]  
    > Du kan dog kun sende timeseddellinjer, som du har angivet tidspunkter for.  
5. Hvis du vil ændre oplysningerne på en linje, der er indstillet til **Sendt**, skal du markere linjen og derefter vælge handlingen **Åbn igen**.

    > [!NOTE]  
    > En leder kan afvise en timeseddellinje, der er sendt til godkendelse. Hvis en linje har statussen **Afvist**, kan du foretage ændringer i linjen og derefter vælge **Send** igen.  
6. Vælg knappen **OK**.

## <a name="approve-or-reject-a-time-sheet"></a>Godkend eller afvis en timeseddel

En timeseddel skal sendes til godkendelse, før den kan bruges. Du kan godkende og afvise individuelle linjer på en timeseddel eller sende dem tilbage til afsenderen. Du kan godkende en timeseddel på to måder:

* En timeseddeladministrator kan godkende enhver timeseddel.
* Den person, der er angivet i feltet **Bruger-id for timeseddelgodkender** på et ressourcekort, kan godkende timesedler for den pågældende ressource. Du kan få mere at vide om opsætning af godkendelse ved at gå til [Opsætning af timesedler](projects-how-setup-time-sheets.md).

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leders timesedler**, og vælg derefter det relaterede link.
2. Vælg en timeseddel på listen.  
3. På siden **Timeseddel**: 
    1. Vælg **Behandle**-handlingen, og vælg derefter **Godkend**.
    2. Vælg handlingen **Alle sendte linjer** for at godkende alle linjer, eller handlingen **Kun valgte linjer** for at godkende linjer, der er valgt på siden **Timeseddel**.
4. Vælg knappen **OK**.  
5. Du kan også vælge handlingen **Afvis** og følge trin 4 til 5.  

> [!TIP]  
> Brug faktaboksene **Timeseddelstatus** og **Faktisk/budgetteret oversigt** for at få et overblik over timeseddeloplysninger.

Når du godkender eller afviser en timeseddel, kan den ikke redigeres, medmindre den er blevet genåbnet. Følgende fremgangsmåde beskriver, hvordan du genåbner en godkendt eller afvist timeseddel.

## <a name="reopen-a-time-sheet"></a>Sådan genåbnes en timeseddel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leders timesedler** eller **Timesedler**, og vælg derefter det relaterede link.
2. Åbn en timeseddel på listen.  

    > [!NOTE]  
    > Du kan kun genåbne linjer med statussen **Godkendt**. Du kan ikke genåbne linjer med statussen **Afvist**, eller som er bogført.  
3. På siden **Timeseddel** skal du vælge handlingen **Åbn igen** og derefter vælge handlingen **Alle sendte linjer** for at åbne alle linjer igen eller handlingen **Kun valgte linjer** for kun at åbne de linjer, der er valgt på siden **Timeseddel**, igen.
4. Vælg knappen **OK**. Status for timeseddellinjerne er ændringer for **Sendt**.  

## <a name="view-and-approve-time-sheets-by-project"></a>Få vist og godkende en timeseddel efter projekt

Du kan for et projekt angive en person, der er ansvarlig for projektet. Disse oplysninger er knyttet til timeseddellinjer. Linket giver projektledere en liste over de timesedler, der skal godkendes. Teamprojektlederen kan for eksempel være ansvarlig for bestemte projekter i din virksomhed. I så fald bør lederen udpeges som **Ansvarlig person** på projektkortet. Du kan se projektopgaver, der er knyttet til et projekt, og antal timer brugt, i denne visning af timeseddeloplysninger.

> [!NOTE]
> Du skal godkende timesedler på siden **Leders timeseddel efter projekt**, når du har valgt en indstilling for **Timeseddel efter projektgodkendelse** på siden **Ressourceopsætning**. Du kan få mere at vide om opsætning af godkendelse af ressourcer ved at gå til [Konfigurere ressourcer](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-project"></a>Godkende eller afvise en timeseddel efter projekt

1. Indtast **Leders timeseddel efter projekt** i feltet **Søg**, og vælg derefter det relaterede link. [!INCLUDE[prod_short](includes/prod_short.md)] viser en liste over timeseddellinjer, der er knyttet til de projekter, du har ansvaret for.
2. Vælg handlingen **Godkend**, og vælg derefter handlingen **Alle sendte linjer** for at godkende alle linjer eller handlingen **Kun valgte linjer** for kun at godkende de linjer, der er valgt på siden **Timeseddel**.

    > [!NOTE]
    > Du kan kun godkende timesedler med statussen **Sendt**.

3. Hvis du vil angive yderligere oplysninger om godkendelse eller afvisning, skal du vælge den **relaterede** handling, derefter vælge **bemærkninger** og derefter **Linjebemærkninger** og skrive bemærkninger.
4. Vælg knappen **OK**.

> [!NOTE]
> Når du har godkendt eller afvist en timeseddellinje efter projekt, kan den ikke åbnes igen eller ændres i vinduet **Timeseddel**.

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Sådan bogfører du timeseddellinjer i en ressourcekladde

Når du har godkendt timeseddelposter for en ressource, kan du bogføre dem i den relevante ressourcekladde.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcekladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. På siden **Foreslå res.kladdelinjer** skal du udfylde felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Vælg knappen **OK**. Der oprettes poster for forbrug i ressourcekladden, hvor du kan ændre oplysningerne efter behov.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Ressourceposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## <a name="post-time-sheet-lines-in-a-project-journal"></a>Bogføre timeseddellinjer i en projektkladde

Når du har godkendt timeseddelposter for et projekt, kan du bogføre dem i den relevante projektkladde.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Foreslå linjer fra timesedler**.  
3. På siden **Foreslå projektkladdelinjer** skal du udfylde felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Vælg knappen **OK**. Der oprettes poster for forbrug i projektkladden, hvor du kan ændre oplysningerne efter behov.  

    > [!NOTE]  
    > Oplysninger om arbejdstype, og om arbejdet er fakturerbart, kopieres fra timeseddellinjen. Du kan om nødvendigt reducere antallet af timer og foretage en delvis bogføring. Hvis du reducerer antallet, sker der følgende: Næste gang, du vælger handlingen **Foreslå linjer fra timesedler**, vil den linje, der oprettes, indeholde den resterende mængde timer.  
5. Vælg handlingen **Bogfør**.  
6. Vælg handlingen **Poster** for at bekræfte posteringen. Siden **Projektposter** åbnes og viser resultatet for bogføring af ressourcekladden.

## <a name="archive-time-sheets"></a>Arkivér timesedler

Når du har bogført timesedler, kan du arkivere dem til fremtidig reference. Du skal bogføre alle linjer på en timeseddel, før du kan arkivere den.

> [!NOTE]  
> Når du arkiverer en timeseddel, fjernes den fra oversigterne på siden **Timesedler** og på siden **Leders timesedler**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Timesedler**, og vælg derefter det relaterede link.
2. Vælg handlingen **Flyt timesedler til arkiv**.  
3. På siden **Flyt timesedler til arkiv** skal du udfylde felterne efter behov, og derefter vælge knappen **OK**.  
4. Hvis du vil se arkiverede timesedler, skal du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arkiver for timesedler** eller **Arkiver for leders timesedler**, og vælg derefter det relaterede link.

## <a name="see-also"></a>Se også

[Projektstyring](projects-manage-projects.md)  
[Konfigurere projektstyring](projects-setup-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
