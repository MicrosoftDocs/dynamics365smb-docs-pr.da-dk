---
title: Oprette arbejdsprocesser for at forbinde opgaver
description: Du kan oprette arbejdsgange, der forbinder forretningsproces opgaver, der udføres af forskellige brugere, og medtager system opgaver, f. eks. automatisk bogføring, som trin i arbejdsgangen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: b4f6894c0d9c5a23445f70b2a50fcd677b17be66
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438403"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Oprette arbejdsprocesser for at forbinde virksomhedsbehandlingsopgaver

Du kan oprette arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

På siden **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en workflowhændelse, begrænset af hændelsesbetingelser, og et workflowrespons med responsmuligheder. Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.  

Når du opretter workflows, kan du kopiere trinene fra eksisterende workflows eller workflowskabeloner. Workflowskabeloner repræsenterer workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[prod_short](includes/prod_short.md)]. Koden for arbejdsgangsskabeloner, som er tilføjet af Microsoft, har "MS-" foran som f.eks. i "MS PIW". Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  

Hvis et virksomhedsscenarie kræver workflowhændelser eller et respons, der ikke understøttes, skal en Microsoft-partner implementere dem ved at oprette en udvidelse, der implementerer den relevante arbejdsflowhændelse.  

> [!NOTE]  
> Alle notifikationer om arbejdsgangstrin sendes via en opgavekø. Sørg for, at opgavekøen afspejler virksomhedens behov. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Illustration af et eksempel på en arbejdsproces.":::

Arbejdsflowet er inddelt i tre sektioner:

1) **Hvis hændelse** er dette det sted, hvor udløseren er valgt.
    Eksempler på Trigger kan være:
    - En masterdatapost er ændret
    - Der er oprettet en finanskladdelinje.
    - Et indgående dokument er oprettet eller frigivet
    - Der er anmodet om godkendelse af et salgsdokument

2) **På betingelse af** de **betingelser** er relateret til hændelsen og åbner ved oprettelse af filtre for, hvornår hændelsen udløses
3) **Svar** de **svar** er på svarene på det næste trin i arbejdet.

Hændelserne er systemdefinerede for begge typer hændelser. Nye hændelser skal tilføjes ved hjælp af udviklingen af et filtypenavn.

## <a name="to-create-a-workflow"></a>Sådan oprettes en arbejdsgang

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsflow**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Workflow** åbnes.  
3. I feltet **Kode** skal du angive op til 20 tegn for at identificere workflowet.  
4. Når du vil oprette workflowet fra en workflowskabelon på siden **Workflows**, skal du vælge handlingen **Opret workflow fra skabelon**. Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).  
5. I feltet **Beskrivelse** skal du beskrive workflowet.  
6. I feltet **Kategori** kan du angive, hvilken kategori workflowet hører under.  
7. I feltet **Når hændelse** skal du angive den hændelse, der skal udføres for at starte trinnet i workflowet.  

    Når du vælger feltet, åbnes siden **Workflowhændelser**, hvor du kan vælge mellem alle workflowhændelser, der findes.  
8. I feltet **Betingelse** skal du angive en eller flere betingelser, der skal opfyldes, før hændelsen i feltet **Når hændelse** kan udføres.  

    Når du vælger feltet, åbnes siden **Hændelsesbetingelser**, hvor du kan vælge på en liste over filterfelter, der er relevante som betingelser for den pågældende hændelse. Du kan tilføje nye filterfelter, du vil bruge som hændelsesbetingelser. Du kan angive hændelsesbetingelsesfiltre, ligesom du angiver filtre for rapportanmodningssider.  

    Hvis workflowhændelsen er ændringen af et bestemt felt i en post, åbnes siden **Hændelsesbetingelser**, hvor du kan vælge feltet og ændringstypen.  

    1. Hvis du vil angive feltændringen for hændelsen, skal du i feltet **Felt** på siden **Hændelsesbetingelser** markere det felt, der ændres.  
    2. I feltet **Operator** skal du vælge enten **Reduceret**, **Forøget** eller **Ændret**.  
9. Angiv den respons, der skal følge, når workflowhændelsen forekommer, i feltet **Så svar**.  

     Når du vælger feltet, åbnes siden **Workflowrespons**, hvor du kan vælge mellem alle workflowresponser, der findes, og angive indstillinger for respons for den valgte respons.  
10. I oversigtspanelet **Indstillinger for den valgte workflowrespons** skal du angive indstillinger for workflowet ved at vælge værdier i de forskellige felter, der vises, på følgende måde:  

    1. Hvis du vil angive indstillinger for et workflowrespons, der involverer afsendelse af en notifikation, skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Beskrivelse|  
        |-----|-----------|  
        |**Giv afsender besked**|Angiv, om godkendelsesanmoderen er blevet underrettet i stedet for modtageren af godkendelsesanmodningen. Hvis du markerer afkrydsningsfeltet, bliver feltet **Modtagers bruger-ID** deaktiveret, da anmoderen til godkendelsen, afsenderen, får besked i stedet. Navnet på workflowresponset ændres tilsvarende til **Opret notifikation til &lt;afsender&gt;**. Hvis afkrydsningsfeltet ikke er markeret, angives navnet på workflowresponset til **Opret notifikation til &lt;bruger&gt;**.
        |**Modtagers bruger-id**|Angiv den bruger, som notifikationen skal sendes til. **Bemærk**: Denne indstilling er kun tilgængelig for workflowrespons med en pladsholder for en bestemt bruger. Notifikationsmodtageren defineres typisk af godkendelsesbrugeropsætningen, når det drejer sig om arbejdsgangssvar uden pladsholdere for brugere.|  
        |**Notifikationsposttype**|Angiver, om notifikationen fra en arbejdsgang udløses af en postændring, en godkendelsesanmodning eller data vedrørende forfaldsdato.|
        |**Side, der linkes til**|Angiv en anden side, som linket i notifikationen åbner i stedet for standardsiden. Bemærk, at siden skal have samme kildetabel som den record, det drejer sig om.|
        |**Brugerdefineret link**|Angiv URL-adressen på et link, der føjes til notifikationen ud over standardlinket til en side.|  

    2. Hvis du vil angive indstillinger for et workflowrespons, der involverer oprettelse af en godkendelsesanmodning, skal du udfylde felterne som beskrevet i følgende tabel.  

        |Felt|Beskrivelse|  
        |-----|-----------|  
        |**Formular for forfaldsdato**|Angiv, inden hvor mange dage godkendelsesanmodningen skal løses fra den dato, hvor den blev sendt.|
        |**Uddeleger efter**|Angiv, om og hvornår en godkendelsesanmodning uddelegeres automatisk til den relevante stedfortræder. Du kan vælge, at der automatisk skal uddelegeres én, to eller fem dage efter den dato, hvor der blev anmodet om godkendelse.|
        |**Godkendertype**|Angiv, hvem godkenderen er, i overensstemmelse med opsætningen af godkendelses- og arbejdsgangsbrugere. Når feltet er angivet til **Sælger/indkøber**, angiver indstillingen, at den bruger, der er angivet i feltet **Sælger/indkøbskode** på siden **Brugeropsætning af godkendelser**, bestemmer godkenderen. Derefter oprettes der godkendelsesanmodningsposter ud fra værdien i feltet **Godkenders grænsetype**. Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-workflow-users.md)|
        |**Vis bekræftelsesmeddelelse**|Angiv, om en bekræftelsesmeddelelse vises for brugere, når de anmoder om en godkendelse.|
        |**Godkenders grænsetype**|Angiv, hvordan godkenderes godkendelsesgrænser påvirker, hvornår godkendelsesanmodningsposter oprettes for dem. En kvalificeret godkender er en person, hvis godkendelsesgrænse er større end værdien i anmodningen, der sendes. Der er følgende muligheder: <ol><li>**Godkenderkæde** angiver, at godkendelsesanmodningsposter oprettes for alle anmoderens godkendere til og med den første kvalificerede godkender.</li><li>**Direkte godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens umiddelbare godkender, uanset godkenderens godkendelsesgrænse.</li><li>**Første kvalificerede godkender** angiver, at en godkendelsesanmodningspost kun oprettes for anmoderens første kvalificerede godkender.</li></ol>|
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
13. Markér afkrydsningsfeltet **Aktiveret** for at angive, at workflowet starter, så snart hændelsen på det første trin af typen **Startpunkt** nås. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).  

> [!NOTE]  
> Undlad at aktivere en arbejdsgang, før du er sikker på, at arbejdsgangen er fuldført, og at arbejdsgangstrin involveret kan begynde.  

> [!TIP]  
> Hvis du vil se relationer mellem de tabeller, der bruges i arbejdsgange, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og derefter angive **arbejdsproces – tabelrelationer**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Eksempel på oprettelse af en ny arbejdsproces vha. eksisterende hændelser

I følgende eksempel oprettes der en ny arbejdsgang for at godkende ændringer af navnet på en eksisterende kreditor:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsflow**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**. Siden **Workflow** åbnes.
3. I oversigtspanelet Indstillinger skal du udfylde felterne som beskrevet i følgende tabel.

    |Felt  |Værdi  |
    |---------|---------|
    |**Kode**|**VENDAPN-01**|
    |**Beskrivelse**|**Godkendelse af kreditornavn ændring** |
    |**Kategori**|**KØB**|

4. Følg disse trin for at oprette det første arbejdsgangstrin.

    1. I feltet **Når-hændelse** skal du angive, at *En kreditorpost er ændret*.  
    2. I feltet **På betingelse** skal du vælge ordet **Altid** og derefter vælge **Tilføj en betingelse for, hvornår en feltværdi skifter kæde**, på siden **Hændelsesbetingelser**, og vælg derefter feltet *Navn*.  

      Resultatet af dette trin er, at betingelsen læses som *Navnet er ændret*.  
    3. I feltet **Svar** skal du vælge **Vælg svar**-link, og derefter skal du i feltet **Vælg svar** på siden **Arbejdsgangssvar** vælge at *tilbageføre værdien af <Field>-feltet i posten og gemme ændringssvaret*, og derefter skal du angive feltet **Navn** i *indstillingerne for den valgte svar sektion*.  
    4. Vælg linket **Tilføj flere svar**, og tilføj derefter en post for at *oprette en godkendelsesanmodning for posten vha. godkender type <%1> og <%2>.* svar.  
    5. Under **Indstillinger for den valgte svar**-sektion til det nye svar skal du ændre feltet **Godkendertype** til *brugergruppen arbejdsgang* og derefter angive den relevante brugergruppe i feltet **arbejdsgang-brugergruppe**.  

    Du kan finde flere oplysninger i [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
    6. Tilføj et tredje svar, *Send godkendelsesanmodning for posten, og opret en notifikation.*  
    7. Tilføj et fjerde svar, *Vis meddelelse "%1"*, og angiv derefter **indstillinger for det valgte svar** i feltet Meddelelser **en anmodning om godkendelse er sendt**.  
    8. Vælg knappen OK for at gå tilbage til workflowtrinnet.  

5. På næste linje skal du tilføje et nyt arbejdsprocestrin for *en godkendelsesanmodning er godkendt.* begivenhed.  

    1. I feltet **når hændelse** skal du angive, at *en godkendelsesanmodning er godkendt*.  
    2. Vælg linje menuen, og vælg derefter **Øg indrykning**.  
    3. I feltet **på betingelse** skal du vælge ordet **altid** og derefter angive **0** i feltet *ventende godkendelser*.  

      Resultatet af dette trin læses som *ventende godkendelser:0* for at angive, at dette er den sidste godkender.  
    4. I feltet **Svar** skal du vælge **Vælg svar**-link, og derefter skal du vælge **Workflowsvar** i feltet **Vælg svar** - vælg *Send godkendelsesanmodningen for posten og opret et meddelelsessvar*.  
    5. Vælg knappen OK.  
6. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er godkendt*.  

    1. I feltet **når hændelse** skal du angive, at *en godkendelsesanmodning er godkendt*.
    2. I feltet **på betingelse** skal du vælge ordet **altid** og derefter angive **>0** i feltet *ventende godkendelser*.  

      Resultatet af dette trin læses som *ventende godkendelser:>0* for at angive, at dette er *ikke* den sidste godkender.  
    3. I feltet **Svar** skal du vælge **Vælg svar**-link, og derefter skal du vælge **Workflowsvar** i feltet **Vælg svar** - vælg *Send godkendelsesanmodningen for posten og opret et meddelelsessvar*.  
    4. Vælg knappen OK.  
7. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er afvist*.  

    1. I feltet **når hændelse** du angive, at *en godkendelsesanmodning er afvist*.  
    2. I feltet **på betingelse** skal du lade værdien være som *altid*.  
    3. I feltet **Svar** skal du vælge **Vælg svar**-link, og derefter skal du vælge **Workflowsvar** i feltet **Vælg svar** - vælg svaret *Afvis nye værdier*.  
    4. Vælg linket **Tilføj flere svar**, og tilføj derefter en post for at *afvise en godkendelsesanmodning for posten og oprette en notifikation*.
    5. Vælg knappen OK.  
8. På næste linje skal du tilføje et nyt arbejdsprocestrin for hændelsen *en godkendelsesanmodning er afvist*.  

    1. I feltet **når hændelse** du angive, at *en godkendelsesanmodning er afvist*.  
    2. I feltet **på betingelse** skal du lade værdien være som *altid*.  
    3. I feltet **Svar** skal du vælge **Vælg svar**-link, og derefter skal du vælge **Workflowsvar** i feltet **Vælg svar** - vælg *Send godkendelsesanmodningen for posten og opret et meddelelsessvar*.  
    4. Vælg knappen OK.  
9. Hvis du vil aktivere arbejdsflowet, skal du vælge feltet **aktiveret**.  

Følgende illustrationer giver en oversigt over resultatet af denne procedure.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Illustration af arbejdsgangen til godkendelse af kreditornavn.":::

Derefter skal du afprøve arbejdsgangen ved at åbne en eksisterende kreditor og ændre navnet. Kontrollere, at der er oprettet en godkendelsesanmodning om ændring af kreditorens navn.

## <a name="see-also"></a>Se også

[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)  
[Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)  
[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)  
[Slette arbejdsgange](across-how-to-delete-workflows.md)  
[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Opsætte workflows](across-set-up-workflows.md)  
[Anvende workflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
