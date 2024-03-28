---
title: 'Oprette sager, priser og sagsbogføringsgrupper'
description: 'Beskriver, hvordan du definerer generelle oplysninger om sager.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# Oprette sager, priser og sagsbogføringsgrupper

Som projektleder kan du oprette sager, der definerer hvert af de projekter, som du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. Brug siden **Jobopsætning** til at definere, hvordan du vil bruge jobfunktioner.

For hvert job skal du angive forskellige oplysninger:

* Priser for jobvarer
* Jobressourcer
* Finanskonti for sag
* Sagbogføringsgrupper (påkrævet)

## Sådan angives generelle oplysninger for sager

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagsopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Feltet **Anvend anvendelseslink som standard** på siden **Sagbogføringsgrupper** angiver, om der som standard knyttes sagsposter til sagsplanlægningslinjer. Slå til/fra-funktionen til for at anvende denne indstilling på alle nye job. Du kan aktivere eller deaktivere sporing af sagsforbrug for et bestemt job ved at slå værdien i feltet **Anvend anvendelseslink** til/fra på siden **sagskort**.

### Sådan definerer du sagsforbrugssporing

Når du ekspederer en aktiv sag, kan du få flere oplysninger om forbruget i forhold til din plan. Det kan udforske forbruget ved at oprette en tilknytning mellem dine sagsplanlægningslinjer og det faktiske forbrug. Du kan bruge hyperlinket til at spore omkostningerne og forstå, hvor meget arbejde der er tilbage. Som standard er sagsplanlægningslinjetypen **Budget**, men brug af linjetypen **Både budget og fakturerbar** har samme virkning.

Når du har konfigureret forbrugssporing ved at vælge feltet **Anvend forbrugslink som standard** til/fra, kan du gennemse oplysninger på sagsplanlægningslinjen. Du kan f. eks. angive antallet af ressourcen, varen eller finanskontoen. Du kan også angive det antal, du vil overføre til sagskladden. I feltet **Restantal** på sagsplanlægningslinjen kan du se, hvad der stadig mangler at blive overført og bogført på sagskladden.

>[!NOTE]
> Hvis afkrydsningsfeltet **Anvend anvendelseslink** som standard på sagskortet er markeret, og feltet **Linjetype** på sagskladdelinjen er tomt, oprettes nye **sagsplanlægningslinjer** for linjetypen **Både budget og fakturerbar**, når du bogfører sagskladdelinjerne eller købsdokument.  
>
> Du kan finde flere oplysninger i [Registrere forbrug for sager](projects-how-record-job-usage.md) og [Administrere stillingsforsyninger](projects-how-manage-project-supplies.md).

> [!IMPORTANT]
> Hvis du ikke angiver en specifik værdi i feltet **Linjetype** på sagskladdelinjen eller linjen er tomt, oprettes der ingen sagsplanlægningslinjer, når du bogfører sagskladden eller købsdokumentet.

## Konfigurere priser for ressourcer, varer og finanskonti for jobs.

> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet nye processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

Konfigurere priser for varer, ressourcer finanskonti i forhold til jobs. 

#### [Aktuel oplevelse](#tab/current-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg **Ressource**, **Vare** eller **Finanskonto**.
3. Udfyld felterne efter behov i **Salgsressourcepriser**, **Salgsvarepriser** eller **Sagsfinanskontopriser**.

Når du vælger en ressource, vare eller finanskonto for en sag, bruger [!INCLUDE [prod_short](includes/prod_short.md)] oplysninger i de valgfrie felter på Sagsplanlægningslinjer og sagskladder. I følgende tabel forklares det, hvordan man gør.

|Kolonne1  |Kolonne2  |
|---------|---------|
|**Sagsressourcer**|Felterne **Sagsopgavenr.**, **Arbejdstype**, **Valutakode**, **Linjerabat i %** og **Kostprisfaktor**. Værdien i feltet **Enhedspris** for ressourcen vil blive anvendt i sagsplanlægningslinjerne og sagskladderne, når denne ressource, en ressource, der er tildelt ressourcegruppen, eller en hvilken som helst ressource angives. Denne pris tilsidesætter eventuelle priser på den eksisterende **Ressourcesalgspris/Ressourcegruppe**-side.|
|**Sagsvarepriser**|Felterne **Sagsopgavenr.**, **Valutakode** og **Linjerabat i %**. Værdien i feltet **Enhedspris** for varen bruges i sagsplanlægningslinjerne og sagskladderne, når varen angives. Prisen tilsidesætter den normale debitorpris (“bedste pris”-mekanismen) for varer. Hvis du vil bruge den normale debitorpris, skal du ikke angive Sagsvarepriser.|
|**Finanskonti**|Oplysninger i felterne **Sagsopgavenr.**, **Valutakode**, **Linjerabat i %**, **Kostprisfaktor** og **Kostpris** bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives og tilføjes til sagen. Værdien i feltet **Kostpris** for finanskontosagsudgiften bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives.|

#### [Ny oplevelse](#tab/new-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Sagsplanlægningslinjer**.

---

## Sådan oprettes sagsbogføringsgrupper

Et aspekt af planlægningssager er at beslutte, hvilke bogføringkonti, der skal bruges til sagsomkostninger. Hvis du vil bogføre sager, skal du oprette konti til bogføring for hver sagsbogføringsgruppe. En bogføringsgruppe repræsenterer en kæde mellem sagen, og hvordan den bør behandles i Finans. Når du opretter en sag, kan du angive en bogføringsgruppe, og som standard knyttes hver opgave, du opretter for sagen, til denne bogføringsgruppe. Når du opretter opgaver, kan du tilsidesætte standardindstillingen og vælge en bogføringsgruppe, der passer bedre.  

> [!NOTE]  
> Du skal konfigurere konti i kontoplanen, før du kan oprette bogføringsgrupper. Du kan finde flere oplysninger i [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

| Feltet Konto | Beskrivelse | Brugt i WIP-type |
| --- | --- |  --- |
| **Kode** |En identitet for bogføringsgruppen. Du kan indtaste op til 10 tegn inkl. mellemrum. | |
| **Konto til VIA-omkostning** |VIA-kontoen for den beregnede omkostning for sagens VIA, som er en anlægsaktivkonto på balancen. | Anvendt omkostning, realiserede omkostninger|
| **Konto til periodiske VIA-omkostninger** |En konto til metoden Kostværdi eller Salgsomkostning for beregning af igangværende arbejde. Kontoen er til skyldige omkostninger på balancen. Der bogføres til denne konto, når reguleringen af igangværende arbejde kræver, at de forbrugsomkostninger, der er bogført til resultatopgørelsen, forhøjes. | Periodiserede omkostninger|
| **Konto til anvendte sagsomkostninger** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. Bruges, når **WIP-bogføringsmetode anvendt** er angivet til *Sag*. | Anvendte omkostninger, realiserede omkostninger|
| **Konto til anvendte vareomkostninger** |Samme som **Sagsomkostninger anvendt konto**, men brugt, når **WIP-bogføringsmetode anvendt** er angivet til *Sagsposten*.| |
| **Konto til anvendte ressourceomkostninger** |Samme som **Sagsomkostninger anvendt konto**, men brugt, når **WIP-bogføringsmetode anvendt** er angivet til *Sagsposten*.| |
| **Konto til anvendte finansomkostninger** |Samme som **Sagsomkostninger anvendt konto**, men brugt, når **WIP-bogføringsmetode anvendt** er angivet til *Sagsposten*.| |
| **Konto til justering af sagsomkostninger** |Modkontoen til kontoen til de periodiske VIA-omkostninger, som er en udgiftskonto. | Periodiserede omkostninger|
| **Driftskonto (budget)** |Den salgskonto, der vil blive brugt til finansudgifter i sagsopgaver med denne bogføringsgruppe. Hvis den er tom, bruges den finanskonto, som blev angivet på sagsplanlægningslinjen. | |
| **Konto til periodisk VIA-salg** |Kontoen for igangværende arbejde for den beregnede salgsværdi af igangværende arbejde, som er en konto for periodiske indtægter på balancen. Der bogføres til denne konto, når reguleringen for igangværende arbejde kræver, at den registrerede omsætning, skal forhøjes. | Periodiseret salg, realiseret salg|
| **Konto til faktureret VIA-salg** |Kontoen for den fakturerede salgsværdi af VIA, som ikke kan registreres. Det er en konto til ikke-indtjent omsætning på balancen. | Realiseret salg, anvendt salg|
| **Konto til anvendt sagssalg** |Modkontoen til kontoen til det fakturerede VIA-salg, som er en kontraindtægtskonto. | Anvendt salg, realiseret salg|
| **Konto til justering af sagssalg** |Modkontoen til sagssalgskontoen for VIA, som er en indtægtskonto. | Periodiseret salg|
| **Konto til realiserede omkostninger** |Den udgiftskonto, som indeholder de registrerede omkostninger for sagen. Det er normalt en debetafrundingskonto. | Realiserede omkostninger|
| **Konto til realiseret salg** |Den indtægtskonto, som indeholder den registrerede indtægt for sagen. Det er normalt en kreditafrundingskonto. | Realiseret salg|

## Se også

[Opsætte projektstyring](projects-setup-projects.md)  
[Video: Sådan oprettes en sag i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
