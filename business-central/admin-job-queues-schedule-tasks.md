---
title: "Planlægge sager til at køre automatisk | Microsoft Docs"
description: "Planlagte sager styres af opgavekøen. Disse sager kører rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: fae1b2937a3c06fc947dd3dbec529826322d035c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Du kan bruge opgavekøer til at planlægge opgaver
Opgavekøer i [!INCLUDE[d365fin](includes/d365fin_md.md)] giver brugerne mulighed for at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Det kan f.eks. være en god idé at køre rapporten **Sælger - salgsstatistik** ugentlig for at spore salget pr. sælger hver uge, eller at køre kodeenheden **Behandl servicekø for mail** dagligt for at sikre, at afventende mail til debitorer om deres serviceordrer sendes ud tids nok.  

## <a name="add-jobs-to-the-job-queue"></a>Føje sager til opgavekøen
Vinduet **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, du vil planlægge, skal du angive oplysninger om typen af det objekt, du vil køre, f.eks. en rapport eller kodeenhed, og navnet og objekt-id'et for det objekt, du vil køre. Du kan også tilføje parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer. Du skal have tilladelse til at køre den pågældende rapport eller kodeenhed, ellers genereres der en fejl, når opgavekøen køres.  

Du kan også angive et filter i feltet **Opgavekøkategorifilter**. Kategorier for opgavekøen kan bruges til at gruppere sager på listen.

[!INCLUDE[d365fin](includes/d365fin_md.md)] kører automatisk sagerne i overensstemmelse med de angivne planer for hver opgavekøpost. Du kan også starte, stoppe og sætte en opgavekøpost i venteposition manuelt.

### <a name="log-files"></a>Log-filer
Fejl vises i vinduet **Logposter i opgavekø** vindue, som du kan få adgang til fra båndet. Du kan også foretage fejlfinding for opgavekøfejl. De data, der genereres, når der køres en opgavekø, gemmes i databasen.  

### <a name="background-posting-with-job-queues"></a>Baggrundsbogføring med opgavekøer
Jobkøer er et effektivt værktøj til at planlægge kørsel af forretningsprocesser i baggrunden. For eksempel kan der være en forekomst, hvor flere brugere forsøger at bogføre salgsordrer på samme tid, men hvor kun én ordre kan behandles ad gangen. Ved at oprette en baggrundsbogføring kan du placere bogføringerne i en kø til behandling i baggrunden.  

 Alternativt kan du planlægge posteringer i timevis, når det er belejligt for din organisation. F.eks. giver det muligvis mening i din virksomhed at køre visse rutiner, når de fleste af dataindtastningerne for den pågældende dag er afsluttede. Du kan opnå dette ved at indstille opgavekøen til at køre forskellige massebogføringsrapporter, f.eks. rapporterne **Massebogfør salgsordrer**, **Massebogfør salgsfakturaer**, og **Massebogfør salgskreditnotaer**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter baggrundsbogføring for følgende dokumenttyper:  

-   Salg: salgsordre, returvareordre, kreditnota, faktura  

-   Køb: indkøbsordre, returvareordre, kreditnota, faktura  

 Hvis opgavekøen ikke kan bogføre salgsordren, ændres status til **Fejlmeddelelse**, og salgsordren føjes til listen over salgsordrer, som brugeren skal håndtere.  

> [!NOTE]  
>  Når du planlægger et bilag til bogføring, og bogføringen starter, konfigureres bogføringsrutinen automatisk til timeout i to timer, hvis den holder op med at svare af en eller anden årsag.  

Du konfigurerer denne anvendelse af opgavekøen i henholdsvis vinduet **Salgsopsætning** eller vinduet **Købsopsætning**. På oversigtspanelet **Baggrundsbogføring** skal du markere afkrydsningsfeltet **Bogfør dokumenter via opgavekøen** og udfylde de relevante oplysninger. Her kan du også bruge feltet **Opgavekøkategorikode** til at udføre alle Opgavekøposter med denne kode. Du kan f.eks. bruge kategorien **Salgsbogføring**, der filtrerer alle salgsordrer, der svarer til en opgavekø, der har den samme kategorikode.  

> [!IMPORTANT]  
>  Hvis du konfigurerer et opgave, der bogfører og udskriver dokumenter, og printeren viser en dialogboks, f.eks. en anmodning om legitimationsoplysninger eller en advarsel om næsten tom blækpatron, bogføres dit dokument, men det udskrives ikke. Den tilsvarende opgavekøpost får på et tidspunkt timeout og feltet **Status** indstilles til **Fejl**. Derfor anbefaler vi, at du ikke bruger en printeropsæting, der kræver interaktion med visningen af printerdialogbokse i forbindelse med baggrundsbogføring.  

## <a name="use-the-my-job-queue-part"></a>Brug delen Min opgavekø
Delen **Min opgavekø** viser de poster i opgavekøen, som en bruger har startet, men som ikke er færdige endnu. Som standard er delen ikke synlig, så du skal føje den til dit rollecenter. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).  

I denne del kan du se de dokumenter, der behandles, eller som er i kø, hvor dit id er angivet i feltet **Tildelt bruger-id**. Denne del hjælper dig med at holde styr på alle poster i opgavekøen, herunder dem der er relateret til baggrundsbogføring. Denne del kan give dig et overblik over, om der er opstået en fejl i bogføringen af et dokument, eller om der er fejl i en opgavekøpost. Delen giver dig også mulighed for at annullere bogføringen af et dokument, hvis det ikke kører.  

## <a name="security"></a>Sikkerhed  
Opgavekøposter kører på basis af tilladelser. Disse tilladelser skal tillade kørsel af rapporten eller codeunit'en.  

Når en opgavekø aktiveres manuelt, køres den med legitimationsoplysningerne for brugeren. Når en opgavekø aktiveres som en planlagt opgave, køres den med legitimationsoplysningerne for serverforekomsten. Når en opgave kører, køres den med legitimationsoplysningerne for den opgavekø, der aktiverede den. Men den bruger, der oprettede opgavekøposten, skal dog også have tilladelser. Når en opgave er tilstanden "Kør i brugersession" (f.eks. i baggrundsbogføring), køres den med legitimationsoplysningerne for den bruger, der oprettede jobbet.  

> [!IMPORTANT]  
>  Hvis du bruger tilladelsessættet SUPER, der følger med [!INCLUDE[d365fin](includes/d365fin_md.md)], har du og dine brugere tilladelse til at køre alle objekter. I dette tilfælde begrænses adgangen for hver bruger kun af tilladelser til data.  

## <a name="using-job-queues-effectively"></a>Effektiv brug af opgavekøer  
Opgavekøposten har mange felter, hvis formål er at overføre parametre i en codeunit, du har angivet til kørsel sammen med en opgavekø. Det betyder også, at codeunits, der skal køres via opgavekøen, skal angives med opgavekøposten som en parameter i udløseren **OnRun**. Dette giver et ekstra niveau af sikkerhed, da dette forhindrer brugerne i at køre vilkårlige kodeenheder via opgavekøen. Hvis brugeren skal overføre parametre til en rapport, er den eneste måde at gøre dette ved at placere rapportudførelsen i en codeunit, som derefter analyserer inputparametrene og skriver dem i rapporten, før den udføres.  

## <a name="see-also"></a>Se også  
[Opsætning](admin-setup-and-administration.md)  
[Konfigurere Business Central](setup.md)  

