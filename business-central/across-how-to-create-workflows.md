---
title: Oprette godkendelsesworkflows for at forbinde opgaver
description: 'Lær, hvordan du kan oprette arbejdsgange, der udføres af personer i forretningsprocesser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/11/2022
ms.author: bholtorf
---
# Oprette arbejdsgange for at forbinde opgaver i virksomhedsprocesser

Du kan oprette arbejdsgange, der forbinder handlinger i forretningsprocesser, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

På siden **Workflow** oprettes et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en workflowhændelse, begrænset af hændelsesbetingelser, og et workflowrespons med responsmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer med faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden.  

[!INCLUDE[workflow](includes/workflow.md)]

Når du opretter workflows, kan du kopiere trinene fra eksisterende workflows eller workflowskabeloner. Workflowskabeloner repræsenterer workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)]. Koden for arbejdsgangsskabeloner tilføjet af Microsoft, har "MS-" foran som f.eks. i "MS PIW". Flere oplysninger [Oprette workflows fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Alle notifikationer om arbejdsgangstrin sendes via en opgavekø. Sørg for, at opgavekøen afspejler virksomhedens behov. Flere oplysninger under [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration af et eksempel på en arbejdsproces.":::

Arbejdsflowet er inddelt i tre sektioner:

1. **Hvis hændelse**  
   Hver vælges udløseren.  
   Eksempler på en udløser:
   * En masterdatapost er ændret
   * Der er oprettet en finanskladdelinje.
   * Der oprettes et indgående eller udgivet dokument
   * Der er anmodet om godkendelse af et salgsdokument
2. **På betingelse**  
   **Betingelserne** er relateret til hændelsen og gør det muligt at oprette filtre for at bestemme, hvordan arbejdsprocessen fortsætter.
3. **Så svar**  
   **Svarene** angiver de næste trin i workflowet.

Indstillingerne er systemdefinerede for både hændelser og svar. Nye hændelser skal tilføjes ved hjælp af udviklingen af et filtypenavn.

## Sådan oprettes en arbejdsgang

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. Når du vil oprette workflowet fra en workflowskabelon på siden **Workflows**, skal du vælge handlingen **Nyt workflow fra skabelon**. Flere oplysninger [Oprette workflows fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  
5. I feltet **Beskrivelse** skal du beskrive workflowet.  
6. I feltet **Kategori** kan du angive, hvilken kategori workflowet hører under.  
7. I feltet **Når hændelse** skal du angive den hændelse, der skal udføres for at starte trinnet i workflowet.  

   Når du vælger feltet, åbnes siden **Workflowhændelser**, hvor du kan vælge mellem alle tilgængelige workflowhændelser.  
8. I feltet **På betingelse** skal du angive en eller flere betingelser, der skal opfyldes, før hændelsen i feltet **Når hændelse** kan udføres.  

   Når du vælger feltet, åbnes siden **Hændelsesbetingelser**, så du kan vælge på en liste over filterfelter, der er relevante som betingelser for den pågældende hændelse. Du kan tilføje nye filterfelter, du vil bruge som hændelsesbetingelser. Du kan angive hændelsesbetingelsesfiltre, ligesom du angiver filtre for rapportanmodningssider.  

   Hvis workflowhændelsen er ændringen af et bestemt felt i en post, åbnes siden **Hændelsesbetingelser**, hvor du kan vælge feltet og ændringstypen.  

   1. Hvis du vil angive feltændringen for hændelsen, skal du i feltet **Felt** på siden **Hændelsesbetingelser** markere det felt, der ændres.  
   2. I feltet **Operator** skal du vælge enten **Reduceret**, **Forøget** eller **Ændret**.  
9. Angiv den respons, der skal følge, når workflowhændelsen forekommer, i feltet **Så svar**.  

   Når du vælger feltet, åbnes siden **Workflowrespons**, så du kan vælge mellem alle tilgængelige workflowresponser, og angive indstillinger for respons for den valgte respons.  
10. På oversigtspanelet **Indstillinger for den valgte svar** skal du angive indstillinger for workflowsvar ved at vælge værdier i forskellige felter, der vises, som følger:  

    1. Hvis du vil angive indstillinger for et workflowrespons, der involverer afsendelse af en notifikation, skal du udfylde felterne som beskrevet i følgende tabel.  

    > [!NOTE]
    > Disse felter kan variere, afhængigt af hvilket svar du har valgt.

       |Felt|Beskrivelse|
       |-----|-----------|
       |**Giv afsender besked**|Angiv, om godkendelsesanmoderen er blevet underrettet i stedet for modtageren af godkendelsesanmodningen. Hvis du markerer afkrydsningsfeltet, bliver feltet **Modtagers bruger-ID** deaktiveret, da anmoderen til godkendelsen, afsenderen, får besked i stedet. Navnet på workflowresponset ændres tilsvarende til **Opret notifikation til &lt;afsender&gt;**. Hvis afkrydsningsfeltet ikke er markeret, angives navnet på workflowresponset til **Opret notifikation til &lt;bruger&gt;**.|
       |**Modtagers bruger-id**|Angiv den bruger, som notifikationen skal sendes til. **Bemærk**: Denne indstilling er kun tilgængelig for workflowrespons med en pladsholder for en bestemt bruger. Notifikationsmodtageren defineres typisk af **godkendelsesbrugeropsætningen**, når det drejer sig om workflowsvar uden pladsholdere for brugere.|
       |**Notifikationsposttype**|Angiv, om workflow-notifikationen udløses af en postændring, en godkendelsesanmodning eller data vedrørende forfaldsdato.|
       |**Side, der linkes til**|Angiv en anden side, som linket i notifikationen åbner i stedet for standardsiden. Siden skal have samme kildetabel som den post, det drejer sig om.|
       |**Brugerdefineret link**|Angiv URL-adressen på et link, der føjes til notifikationen ud over standardlinket til siden.|

    2. Hvis du vil angive indstillinger for et workflowrespons, der involverer oprettelse af en godkendelsesanmodning, skal du udfylde felterne som beskrevet i følgende tabel.  

       |Felt|Beskrivelse|  
       |-----|-----------|  
       |**Formular for forfaldsdato**|Angiv, inden hvor mange dage godkendelsesanmodningen skal løses fra den dato, hvor den blev sendt.|
       |**Uddeleger efter**|Angiv, om og hvornår en godkendelsesanmodning uddelegeres automatisk til den relevante stedfortræder. Du kan vælge, at der automatisk skal uddelegeres én, to eller fem dage efter den dato, hvor der blev anmodet om godkendelse.|
       |**Godkendertype**|Angiv, hvem godkenderen er, i overensstemmelse med opsætningen af godkendelses- og arbejdsgangsbrugere. Når feltet er angivet til **Sælger/indkøber**, angiver den bruger, der er angivet i feltet **Sælger/indkøbskode** på siden **Brugeropsætning af godkendelser**, godkenderen. Derefter oprettes der godkendelsesanmodningsposter ud fra værdien i feltet **Godkenders grænsetype**. Flere oplysninger i [Konfigurere godkendte brugere](across-how-to-set-up-workflow-users.md).|
       |**Vis bekræftelsesmeddelelse**|Angiv, om en bekræftelsesmeddelelse vises for brugere, når de anmoder om en godkendelse.|
       |**Godkenders grænsetype**|Angiv, hvordan godkenderes godkendelsesgrænser påvirker, hvornår godkendelsesanmodningsposter oprettes for dem. En kvalificeret godkender er en person, hvis godkendelsesgrænse er større end værdien i anmodningen, der sendes. Der findes følgende indstillinger: <ol><li>**Godkenderkæde** angiver, at godkendelsesanmodningsposter oprettes for alle anmoderens godkendere til og med den første kvalificerede godkender.</li><li>**Direkte godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens umiddelbare godkender, uanset godkenderens godkendelsesgrænse.</li><li>**Første kvalificerede godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens første kvalificerede godkender.</li><li>**Specifik godkender** angiver, at du får besked om, at brugeren har valgt feltet **Godkender-id**.</li></ol>|
    3. Hvis du vil angive indstillinger for et arbejdsgangssvar, der involverer oprettelse af kladdelinjer, skal du udfylde felterne som beskrevet i følgende tabel.  

       |Felt|Beskrivelse|  
       |-----|-----------|  
       |**Finanskladdetypes navn**|Angiv navnet på den finanskladdetype, som de angivne kladdelinjer oprettes i.|  
       |**Finanskladdenavn**|Angiv det finanskladdenavn, som de angivne kladdelinjer oprettes i.|  

11. Vælg knapperne **Forøg indrykning** og **Reducer indrykning** for at indrykke hændelsesnavnet i feltet **Når** for at definere trinnets placering i workflowet.  

    1. Angiv, at trinnet er næste i arbejdsgangrækkefølgen ved at indrykke hændelsesnavnet under hændelsesnavnet på det foregående trin.  
    2. Angiv, at trinnet er et af flere alternative trin, der kan starte, afhængigt af dets tilstand, ved at placere hændelsesnavnet på den samme indrykning som de andre alternative trin. Ranger sådanne valgfrie trin i overensstemmelse med prioritet ved at placere det vigtigste først.  

    > [!NOTE]  
    >  Du kan kun ændre indrykningen af et trin, der ikke har et efterfølgende trin.  

12. Gentag trin 7 til 11 for at tilføje flere arbejdsgang trin, før eller efter det trin, du lige har oprettet.  
13. Aktiver afkrydsningsfeltet **Aktiveret** for at angive, at workflowet starter, så snart hændelsen på det første trin af typen **Startpunkt** nås. Flere oplysninger i [Bruge workflows](across-use-workflows.md).  

> [!NOTE]  
> Undlad at aktivere en arbejdsgang, før du er sikker på, at arbejdsgangen er fuldført, og at arbejdsgangstrin involveret kan begynde.  

> [!TIP]  
> Hvis du vil se relationer mellem de tabeller, der bruges i arbejdsgange, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og derefter angive **Workflow – tabelrelationer**.  

## Eksempel på oprettelse af en ny arbejdsproces vha. eksisterende hændelser

I følgende eksempel oprettes der en ny arbejdsgang for at godkende ændringer af navnet på en eksisterende kreditor:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Workflow** åbnes.
3. I oversigtspanelet Indstillinger skal du udfylde felterne som beskrevet i følgende tabel.

    |Felt  |Værdi  |
    |---------|---------|
    |**Kode**|**VENDAPN-01**|
    |**Beskrivelse**|**Godkendelse af kreditornavn ændring** |
    |**Kategori**|**KØB**|

4. Gør følgende for at oprette det første workflow-trin.

    1. I feltet **Når-hændelse** skal du angive, at *En kreditorpost er ændret*.  
    2. I feltet **på betingelse** skal du vælge **Altid**. Vælg derefter linket **Tilføj en betingelse for, hvornår en feltværdi skifter** på siden **Hændelsesbetingelser** og derefter feltet *Navn*. Resultatet af dette trin er, at betingelsen læses som *Navnet er ændret*.  
    3. I feltet **Så svar** skal du vælge linket **Vælg svar**. Vælg nu i feltet **Vælg svar** på siden **Workflow-svar** svaret *Tilbagefør værdien for feltet \<Field\> i posten, og gem ændringen*. Angiv feltet **Navn** i sektionen *Indstillingerne for den valgte svar*.  
    4. Vælg linket **Tilføj flere svar**, og tilføj derefter svaret *Opret en godkendelsesanmodning for posten ved hjælp af godkendertype <%1> og <%2>* svaret.  
    5. Under **Indstillinger for den valgte svar**-sektion til det nye svar skal du ændre feltet **Godkendertype** til *brugergruppen arbejdsgang* og derefter angive den relevante brugergruppe i feltet **arbejdsgang-brugergruppe**. Flere oplysninger i [Konfigurere godkendte brugere](across-how-to-set-up-approval-users.md).  
    6. Tilføj et tredje svar, *Send godkendelsesanmodning for posten, og opret en notifikation.*  
    7. Tilføj et fjerde svar *Vis meddelelse "%1"*, og angiv derefter **Indstillinger for det valgte svar** i feltet **Meddelelse**, og angiv derefter **En godkendelsesanmodning er sendt**.  
    8. Vælg **OK** for at gå tilbage til workflowtrinnet.  

5. På næste linje skal du tilføje et nyt arbejdsprocestrin for *en godkendelsesanmodning er godkendt.* begivenhed.

    1. I feltet **når hændelse** skal du angive, at *en godkendelsesanmodning er godkendt*.  
    2. Vælg linje menuen, vælg derefter **Øg indrykning**.  
    3. I feltet **På betingelse** skal du vælge ordet **Altid** og derefter angive **0** i feltet *ventende godkendelser*. Resultatet af dette trin læses som *ventende godkendelser:0* for at angive, at dette er den sidste godkender.  
    4. I feltet **Så svar** skal du vælge linket **Vælg svar**. Derefter på siden **Workflow-svar** i feltet **Vælg svar** vælges *Send godkendelsesanmodning til post, og opret en notifikation*.  
    5. Vælg **OK**.  
6. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er godkendt*.  

    1. I feltet **når hændelse** skal du angive, at *en godkendelsesanmodning er godkendt*.
    2. I feltet **På betingelse** skal du vælge ordet **Altid** og derefter angive i feltet **Ventende godkendelser** *>0*. Resultatet af dette trin læses som *ventende godkendelser:>0* for at angive, at dette er *ikke* den sidste godkender.  
    3. I feltet **Så svar** skal du vælge linket **Vælg svar**. Derefter på siden **Workflow-svar** i feltet **Vælg svar** vælges *Send godkendelsesanmodning til post, og opret en notifikation*.  
    4. Vælg **OK**.  
7. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er delegeret*.  

    1. I feltet **når hændelse** skal du angive, at *en godkendelsesanmodning er delegeret*.  
    2. I feltet **på betingelse** skal du lade værdien være som *altid*.  
    3. I feltet **Så svar** skal du vælge linket **Vælg svar**. Derefter på siden **Workflow-svar** i feltet **Vælg svar** vælges *Send godkendelsesanmodning til post, og opret en notifikation*.  
    4. Vælg **OK**.  
8. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er afvist*.  

    1. I feltet **når hændelse** du angive, at *en godkendelsesanmodning er afvist*.  
    2. I feltet **på betingelse** skal du lade værdien være som *altid*.  
    3. I feltet **Så svar** skal du vælge linket **Vælg svar**. Vælg derefter indstillingen **Fjern de nye værdier** i feltet **Vælg svar** på siden *Workflow-svar*.  
    4. Vælge linket **Tilføj flere svar**, tilføj derefter en post for *Afvis en godkendelsesanmodning for posten og opret en notifikation*-svaret
    5. Vælg **OK**.  
9. Aktiver workflowet ved at slå **Aktiveret** til.  

Følgende illustration giver en oversigt over resultatet af denne procedure.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration af arbejdsgangen til godkendelse af kreditornavn.":::

Derefter skal du afprøve arbejdsgangen ved at åbne en eksisterende kreditorkort og ændre navnet. Kontrollere, at der er sendt en godkendelsesanmodning om ændring af kreditorens navn.

## Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## Se også

[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Konfiguration af workflow-godkendelsesnotifikationer](across-setting-up-workflow-notifications.md)  
[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette godkendelsesworkflows](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
