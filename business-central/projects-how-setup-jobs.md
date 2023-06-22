---
title: 'Oprette sager, priser og sagsbogføringsgrupper'
description: 'Bruges til at oprette oplysninger om almindelige opgaver og oprette priser for sagsvarer, ressourcer og finanskonti og sagsbogføringsgrupper.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-jobs-prices-and-job-posting-groups" />Oprette sager, priser og sagsbogføringsgrupper

Som projektleder kan du oprette sager, der definerer hvert af de projekter, som du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Sagsopsætning** skal du angive, hvordan du vil bruge bestemte sagsfunktioner.

For hver sag kan du derefter specificere de individuelle jobkort med oplysninger om priser for sagsvarer, sagsressourcer og sagsfinanskonti, og du skal oprette sagsbogføringsgrupper.

## <a name="to-set-general-information-for-jobs" />Sådan angives generelle oplysninger for sager

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagsopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Feltet **Anvend anvendelseslink som standard** angiver, om der som standard knyttes sagsposter til sagsplanlægningslinjer. Marker feltet, hvis du vil anvende indstillingen på alle nye sager, du opretter. Du kan aktivere eller deaktivere sporing af sagsforbrug for et bestemt job ved at ændre værdien i feltet **Anvend anvendelses link** på det enkelte jobkort. Konsekvenser beskrives i følgende afsnit.

### <a name="to-set-up-job-usage-tracking" />Sådan definerer du sagsforbrugssporing

Når du ekspederer en aktiv sag, kan du få flere oplysninger om forbruget i forhold til din plan. Det kan du nemt gøre ved at oprette en tilknytning mellem dine sagsplanlægningslinjer og det faktiske forbrug. På denne måde kan du holde styr på dine omkostninger og nemt se, hvor meget arbejde, der mangler at blive udført. Som standard er sagsplanlægningslinjetypen *Budget*, men brug af linjetypen **Både budget og fakturerbar** har samme virkning.

Når du har konfigureret forbrugssporing ved at vælge feltet **Anvend forbrugslink**, kan du gennemse oplysninger på sagsplanlægningslinjen. Du kan angive antallet af ressourcen, varen eller finanskontoen, og derefter angive, hvilket antal du vil overføre til sagskladde. I feltet **Restantal** på sagsplanlægningslinjen kan du se, hvad der stadig mangler at blive overført og bogført på sagskladden.

>[!NOTE]
> Hvis afkrydsningsfeltet **Anvend anvendelseslink** som standard på sagskortet er markeret, og feltet **Linjetype** på sagskladdelinjen er tomt, oprettes nye *sagsplanlægningslinjer* for linjetypen *Budget*, når du bogfører sagskladdelinjerne eller købsdokument.  
> Du kan finde flere oplysninger i [Registrere forbrug for sager](projects-how-record-job-usage.md) og [Administrere stillingsforsyninger](projects-how-manage-project-supplies.md).

> [!IMPORTANT]
> Hvis feltet **Linjetype** på sagskladdelinjen eller linjen er tomt, oprettes der ingen sagsplanlægningslinjer, når du bogfører sagskladden eller købsdokumentet.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs" />Konfigurere priser for ressourcer, varer og finanskonti for jobs.

> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet nye processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

Konfigurere priser for varer, ressourcer finanskonti i forhold til jobs. 

#### [Aktuel oplevelse](#tab/current-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg **Ressource**, **Vare** eller **Finanskonto**.
3. Udfyld felterne efter behov i **Salgsressourcepriser**, **Salgsvarepriser** eller **Sagsfinanskontopriser**.

I følgende tabel vises, hvordan oplysningerne i de valgfrie felter bruges på Sagsplanlægningslinjer og kladder, når ressourcen, varen eller finanskontoen vælges for sagen.

|Kolonne1  |Kolonne2  |
|---------|---------|
|**Sagsressourcer**|Felterne **Sagsopgavenr.**, **Arbejdstype**, **Valutakode**, **Linjerabat i %** og **Kostprisfaktor**. Værdien i feltet **Enhedspris** for ressourcen vil blive anvendt i sagsplanlægningslinjerne og sagskladderne, når denne ressource, en ressource, der er tildelt ressourcegruppen, eller en hvilken som helst ressource angives. Bemærk, at denne pris altid vil tilsidesætte eventuelle priser på den eksisterende **Ressourcesalgspris/Ressourcegruppe**-side.|
|**Sagsvarepriser**|Felterne **Sagsopgavenr.**, **Valutakode** og **Linjerabat i %**. Værdien i feltet **Enhedspris** for varen bruges i sagsplanlægningslinjerne og sagskladderne, når varen angives. Bemærk, at denne pris altid vil tilsidesætte den normale debitorpris (“bedste pris”-mekanisme) for varer. Hvis du vil bruge den normale debitorpris, skal du ikke oprette sagsvarepriser.|
|**Finanskonti**|Oplysninger i felterne **Sagsopgavenr.**, **Valutakode**, **Linjerabat i %**, **Kostprisfaktor** og **Kostpris** bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives og tilføjes til sagen. Værdien i feltet **Kostpris** for finanskontosagsudgiften bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives.|

#### [Ny oplevelse](#tab/new-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Sagsplanlægningslinjer**.

---

## <a name="to-set-up-job-posting-groups" />Sådan oprettes sagsbogføringsgrupper

Et aspekt af planlægningssager er at beslutte, hvilke bogføringkonti, der skal bruges til sagsomkostninger. Hvis du vil bogføre sager, skal du oprette konti til bogføring for hver sagsbogføringsgruppe. En bogføringsgruppe repræsenterer en kæde mellem sagen, og hvordan den bør behandles i Finans. Når du opretter en sag, kan du angive en bogføringsgruppe, og som standard knyttes hver opgave, du opretter for sagen, til denne bogføringsgruppe. Når du opretter opgaver, kan du tilsidesætte standardindstillingen og vælge en bogføringsgruppe, der passer bedre.  

> [!NOTE]  
>   De nødvendige konti, der skal bogføres til i tabellen over konti skal oprettes, før du kan oprette bogføringsgrupper. Du kan finde flere oplysninger i [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter kontofelterne som beskrevet i følgende tabel.  

| Feltet Konto | Beskrivelse |
| --- | --- |
| **Kode** |En kode for bogføringsgruppen. Du kan indtaste op til 10 tegn inkl. mellemrum. |
| **Konto til VIA-omkostning** |VIA-kontoen for den beregnede omkostning for sagens VIA, som er en anlægsaktivkonto på balancen. |
| **Konto til periodisk VIA-omkostning** |En konto til metoden Kostværdi eller Salgsomkostning til beregning af VIA, som er en kreditorkonto for skyldige omkostninger på balancen. Der bogføres til denne konto, når VIA-reguleringen kræver, at de forbrugsomkostninger, der er bogført til resultatopgørelsen, forhøjes. |
| **Konto til anvendt sagsomkostning** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. |
| **Konto til anvendte vareomkostninger** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. |
| **Konto til anvendte ressourceomkostninger** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. |
| **Konto til anvendte omkostninger** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. |
| **Konto til regulering af sagsomkostning** |Modkontoen til kontoen til de periodiske VIA-omkostninger, som er en udgiftskonto. |
| **Driftskonto (budget)** |Den salgskonto, der vil blive brugt til finansudgifter i sagsopgaver med denne bogføringsgruppe. Hvis den er tom, bruges den finanskonto, som blev angivet på sagsplanlægningslinjen. |
| **Konto til periodisk VIA-salg** |VIA-kontoen for den beregnede salgsværdi af VIA, som er en konto for periodiske indtægter på balancen. Der bogføres til denne konto, når VIA-reguleringen kræver, at den registrerede omsætning, skal forhøjes. |
| **Konto til faktureret VIA-salg** |Kontoen for den fakturerede salgsværdi af VIA, som ikke kan registreres. Det er en konto til ikke-indtjent omsætning på balancen. |
| **Konto til anvendt sagssalg** |Modkontoen til kontoen til det fakturerede VIA-salg, som er en kontraindtægtskonto. |
| **Konto til justering af sagssalg** |Modkontoen til sagssalgskontoen for VIA, som er en indtægtskonto. |
| **Konto til realiserede omkostninger** |Den udgiftskonto, som indeholder de registrerede omkostninger for sagen. Det er normalt en debetafrundingskonto. |
| **Konto til realiseret salg** |Den indtægtskonto, som indeholder den registrerede indtægt for sagen. Det er normalt en kreditafrundingskonto. |

## <a name="see-related-microsoft-trainingtrainingpathsset-up-jobs-resources" />Se relateret [Microsoft-træning](/training/paths/set-up-jobs-resources/)

## <a name="see-also" />Se også

[Oprette projektstyring](projects-setup-projects.md)  
[Video: Sådan oprettes en sag i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
