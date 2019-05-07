---
title: Planlægge sager til at køre automatisk | Microsoft Docs
description: Planlagte sager styres af opgavekøen. Disse sager kører rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "935371"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Du kan bruge opgavekøer til at planlægge opgaver
Opgavekøer i [!INCLUDE[d365fin](includes/d365fin_md.md)] giver brugerne mulighed for at planlægge og køre specifikke rapporter og kodeenheder. Du kan angive opgaver, der skal køres én gang eller gentagne gange. Det kan f.eks. være en god idé at køre rapporten **Sælger - salgsstatistik** ugentlig for at spore salget pr. sælger hver uge, eller at køre kodeenheden **Behandl servicekø for mail** dagligt for at sikre, at afventende mail til debitorer om deres serviceordrer sendes ud tids nok.

Siden **Opgavekøposter** viser alle eksisterende sager. Hvis du tilføjer en ny opgavekøpost, du vil planlægge, skal du angive oplysninger om typen af det objekt, du vil køre, f.eks. en rapport eller kodeenhed, og navnet og objekt-id'et for det objekt, du vil køre. Du kan også tilføje parametre for at angive funktionsmåden for opgavekøposten. Du kan f.eks. tilføje en parameter til kun at sende bogførte salgsordrer. Du skal have tilladelse til at køre den pågældende rapport eller kodeenhed, ellers genereres der en fejl, når opgavekøen køres.  

En opgavekø kan have mange poster, som er de opgaver, der administreres og køres i køen. Oplysninger i posten angiver, hvilken codeunit eller rapport der køres, når og hvor ofte posten køres, i hvilken kategori opgaven kører, og hvordan den køres.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Sådan konfigureres baggrundsbogføring med opgavekøer
Opgavekøer er et effektivt værktøj til planlægning af kørsel af forretningsprocesser i baggrunden, f.eks. når mange brugere prøver at bogføre salgsordrer, men kun én ordre kan behandles ad gangen. Alternativt kan du planlægge posteringer i timevis, når det er belejligt for din organisation. F.eks. giver det muligvis mening i din virksomhed at køre visse rutiner, når de fleste af dataindtastningerne for den pågældende dag er afsluttede.

Du kan opnå dette ved at indstille opgavekøen til at køre forskellige massebogføringsrapporter, f.eks. rapporterne **Massebogfør salgsordrer**, **Massebogfør salgsfakturaer**, **Massebogfør salgsreturvareordrer** og **Massebogfør salgskreditnotaer**. Du kan finde flere oplysninger i [Sådan oprettes en opgavekøpost for baggrundsbogføring af salgsordrer](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter baggrundsbogføring for alle salg, køb og servicedokumenter.

Nedenstående fremgangsmåde beskriver, hvordan du konfigurerer baggrundsbogføring af salgsordrer. Trinene er de samme for køb og service.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af salg og tilgodehavender**, og vælg derefter det relaterede link.
2. På siden **Salgsopsætning** skal du markere afkrydsningsfeltet **Bogfør med opgavekøen**.
3. Hvis du vil filtrere opgavekøposter for salgsordrebogføring, skal du vælge feltet **Opgavekøkategorikode** og derefter vælge kategorien **Salgsbogføring**.

    Et opgavekøobjekt, codeunit 88 **Salgsbogføring via opgavekø**, oprettes. Fortsæt med at aktivere det på siden **Opgavekøposter**.
4. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.
5. På siden **Opgavekøposter** skal du vælge handlingen **Ny**.
6. I feltet **Objekttype, der skal aktiveres** skal du vælge **Codeunit**.  
7. I feltet **Objekt-id, der skal køres** skal du vælge 88, **Salgsbogføring via opgavekø**.

    Ingen andre felter er relevante for dette scenarie.
8. Vælg handlingen **Angiv status til Klar**.
9. Du kan kontrollere, at opgavekøen fungerer som forventet ved at bogføre en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).
10. Gennemse på siden **Logposter i opgavekø**, hvis salgsordren blev bogført korrekt. Du kan finde flere oplysninger i [Sådan får du vist status eller fejl i opgavekøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Hvis også salgsdokumenter skal udskrives, når de er bogført, skal du markere afkrydsningsfeltet **Bogfør og udskriv med opgavekøen** på siden **Salgsopsætning**.  

> [!IMPORTANT]  
> Hvis du konfigurerer et opgave, der bogfører og udskriver dokumenter, og printeren viser en dialogboks, f.eks. en anmodning om legitimationsoplysninger eller en advarsel om næsten tom blækpatron, bogføres dit dokument, men det udskrives ikke. Den tilsvarende opgavekøpost får på et tidspunkt timeout og feltet **Status** indstilles til **Fejl**. Derfor anbefaler vi, at du ikke bruger en printeropsæting, der kræver interaktion med visningen af printerdialogbokse i forbindelse med baggrundsbogføring.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Sådan oprettes en opgavekøpost for baggrundsbogføring af salgsordrer
Følgende procedure viser, hvordan du kan indstille rapporten **Massebogfør salgsordrer** til automatisk bogføring af frigivne salgsordrer kl. 16 på ugedage.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. I feltet **Objekttype, der skal aktiveres** skal du vælge **Rapport**.  
4. I feltet **Objekt-id, der skal køres** skal du vælge 296, **Massebogfør salgsordrer**.
5. Marker **Siden Rapportanmodning** afkrydsningsfeltet.
6. På siden **Massebogfør salgsordrer** skal du definere, hvad der skal medtages under den automatiske bogføring af salgsordrer, og derefter vælge **OK** knappen.
7. Marker alle afkrydsningsfelter fra **Aktiver hver mandag** til og med **Aktiver hver fredag**.
8. I feltet **Starttidspunkt** skal du angive kl. 16.
9. Vælg handlingen **Angiv status til Klar**.

Salgsordrer, der er klar til bogføring nu, bogføres hver ugedag kl. 16.

> [!NOTE]
> Hvis opgavekøen ikke kan bogføre salgsordren, ændres status til **Fejlmeddelelse**, og salgsordren føjes til listen over salgsordrer, som brugeren skal håndtere manuelt. Du kan finde flere oplysninger i [Sådan får du vist status eller fejl i opgavekøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Når opgavekøer er konfigureret og kører, kan status ændres på følgende måde i hver gentagede periode:

* **Afvent**  
* **Klar**  
* **Igangsat**  
* **Fejl**  
* **Færdig**  

Når en opgave er afsluttet korrekt, fjernes den fra listen over opgavekøposter, medmindre det er en tilbagevendende opgave. Hvis det er en tilbagevendende opgave, justeres feltet **Tidligste starttidspunkt** og viser, næste gang opgaven forventes at køre.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Sådan får du vist status eller fejl i opgavekøen
Data, der genereres, når der køres en opgavekø, gemmes i databasen, så du kan foretage fejlfinding i opgavekøen.

### <a name="to-view-status-for-any-job"></a>Sådan får du vist status for en opgave
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opgavekøposter**, og vælg derefter det relaterede link.
2. På siden **Opgavekøposter** skal du vælge en opgavekøpost og derefter vælge **Logposter**-handlingen.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Sådan vises status fra et salgs- eller købsdokument
1. I det dokument, du har forsøgt at bogføre med opgavekøen, skal du vælge feltet **Opgavekøstatus**, der indeholder **Fejl**.
2. Gennemgå fejlmeddelelsen, og løs problemet.

## <a name="the-my-job-queue-part"></a>Delen Min opgavekø
Delen **Min opgavekø** i dit rollecenter viser de poster i opgavekøen, som du har startet, men som ikke er færdige endnu. Som standard er delen ikke synlig, så du skal føje den til dit rollecenter. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).  

I denne del kan du se, hvilke dokumenter med dit id i feltet **Tildelt bruger-id**, der behandles, eller som er i kø, herunder dem, der er relateret til baggrundsbogføring. Denne del kan give dig et overblik over, om der er opstået en fejl i bogføringen af et dokument, eller om der er fejl i en opgavekøpost. Delen giver dig også mulighed for at annullere bogføringen af et dokument, hvis det ikke kører.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Se en fejl fra Min opgavekø
1. I en post med status **Fejl** skal du vælge **Vis fejl**-handlingen.
2. Gennemgå fejlmeddelelsen, og løs problemet.

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
[Ændring af grundlæggende indstillinger](ui-change-basic-settings.md)  
