---
title: 'Konfigurere projekter, priser og projektbogføringsgrupper'
description: 'Beskriver, hvordan du definerer generelle oplysninger om projekter.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-projects-prices-and-project-posting-groups"></a>Konfigurere projekter, priser og projektbogføringsgrupper

Som projektleder kan du oprette projekter, der definerer hvert af de projekter, som du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. Brug siden **Projektopsætning** til at definere, hvordan du vil bruge projektfunktioner.

For hvert projekt skal du angive forskellige oplysninger:

* Priser for projektvarer
* Projektressourcer
* Finanskonti for projekter
* Projektbogføringsgrupper (påkrævet)

## <a name="to-set-general-information-for-projects"></a>Sådan angives generelle oplysninger for projekter

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Projektopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Feltet **Anvend anvendelseslink som standard** på siden **Projektbogføringsgrupper** angiver, om der som standard knyttes projektposter til projektplanlægningslinjer. Slå til/fra-funktionen til for at anvende denne indstilling på alle nye projekter. Du kan aktivere eller deaktivere sporing af projektforbrug for et bestemt projekt ved at slå værdien i feltet **Anvend anvendelseslink** til/fra på siden **Projektkort**.

### <a name="specify-a-default-location-for-project-items"></a>Angive en standardplacering for projektelementer

Du kan spare tid på dataindtastning ved at angive en standardlokation og -placering for projekter på siden **Projektkort**. Når du opretter projektopgaver, projektplanlægningslinjer og projektkladdelinjer for projektet, tildeles standardlokationen og -placeringen automatisk. Du kan dog ændre lokationskoden og placeringen på opgaver og linjer, hvis det er nødvendigt.

Hvis du definerer en **Til-projektplaceringskode** på lokationen, udfyldes placeringskoden, når du vælger lokationskoden. Hvis lagerstedsprocessen kræver lagerpluk, kan du også definere andre placeringer, som varerne skal forbruges fra.

Disse felter er standardværdier, når du opretter projektopgaver. Eksisterende projektopgaver ændres ikke.

Der er et par ting, du skal vide om brug af standardplaceringer:

* Hvis du for projektopgaver definerer en **Til-projektplaceringskode** på lokationen, tildeles placeringskoden, når du vælger lokationskoden. Hvis lagerstedsprocessen kræver lagerpluk, kan du også definere andre placeringer, som varerne skal forbruges fra.
* For projektplanlægningslinjer er **lokationskoden** baseret på den værdi, der er valgt på projektplanlægningslinjen, når du vælger en vare. Hvis der ikke er defineret en placeringskode for projektopgaven, vælges placeringen fra indholdet på standardplaceringen. Du kan ændre begge værdier manuelt.
* For projektkladdelinjer er **lokationskoden** baseret på den værdi, der er valgt på projektkladdelinjen, når du vælger en vare. Hvis der ikke er defineret en placeringskode for projektopgaven, vælges placeringen fra indholdet på standardplaceringen. Du kan ændre begge værdier manuelt.

### <a name="invoice-multiple-customers-for-project-tasks"></a>Fakturere flere debitorer for projektopgaver

Når projekter involverer flere debitorer, kan det være en udfordring at fakturere de rigtige kunder for de rigtige opgaver. [!INCLUDE [prod_short](includes/prod_short.md)] gør fakturering mindre kompleks ved at give dig mulighed for at angive fakturer til- og sælg til-kunder på hver projektopgavelinje, så du automatisk kan generere fakturaer til de korrekte kunder. Du kan få mere at vide om fakturering af flere kunder ved at gå til [Fakturere en eller flere debitorer for projektopgaver](projects-how-create-jobs.md#invoice-one-or-more-customers-for-project-tasks).

### <a name="to-set-up-project-usage-tracking"></a>Sådan definerer du projektforbrugssporing

Når du ekspederer et aktivt projekt, kan du få flere oplysninger om forbruget i forhold til din plan. Det kan udforske forbruget ved at oprette en tilknytning mellem dine projektplanlægningslinjer og det faktiske forbrug. Du kan bruge hyperlinket til at spore omkostningerne og forstå, hvor meget arbejde der er tilbage. Som standard er projektplanlægningslinjetypen **Budget**, men brug af linjetypen **Både budget og fakturerbar** har samme virkning.

Når du har konfigureret forbrugssporing ved at vælge feltet **Anvend forbrugslink som standard** til/fra, kan du gennemse oplysninger på projektplanlægningslinjen. Du kan f. eks. angive antallet af ressourcen, varen eller finanskontoen. Du kan også angive det antal, du vil overføre til projektkladden. I feltet **Restantal** på projektplanlægningslinjen kan du se, hvad der stadig mangler at blive overført og bogført på projektkladden.

>[!NOTE]
> Hvis afkrydsningsfeltet **Anvend anvendelseslink** som standard på projektkortet er markeret, og feltet **Linjetype** på projektkladdelinjen er tomt, oprettes nye **projektplanlægningslinjer** for linjetypen **Både budget og fakturerbar**, når du bogfører projektkladdelinjerne eller købsdokument.  
>
> Du kan finde flere oplysninger i [Registrere forbrug for projekter](projects-how-record-job-usage.md) og [Administrere projektforsyninger](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Hvis du ikke angiver en specifik værdi i feltet **Linjetype** på projektkladdelinjen eller linjen er tomt, oprettes der ingen projektplanlægningslinjer, når du bogfører projektkladden eller købsdokumentet.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-projects"></a>Konfigurere priser for ressourcer, varer og finanskonti for projekter

> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet nye processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

Konfigurere priser for varer, ressourcer finanskonti i forhold til et projekt. 

#### [Aktuel oplevelse](#tab/current-experience)

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projekt**, og vælg derefter det relaterede link.  
2. Markér det relevante projekt, og vælg **Ressource**, **Vare** eller **Finanskonto**.
3. Udfyld felterne efter behov i **Projektressourcepriser**, **Projektvarepriser** eller **Projektfinanskontopriser**.

Når du vælger en ressource, vare eller finanskonto for et projekt, bruger [!INCLUDE [prod_short](includes/prod_short.md)] oplysninger i de valgfrie felter på projektplanlægningslinjer og projektkladder. I følgende tabel forklares det, hvordan man gør.

|Kolonne1  |Kolonne2  |
|---------|---------|
|**Projektressourcer**|Felterne **Projektopgavenr.**, **Arbejdstype**, **Valutakode**, **Linjerabat i %** og **Kostprisfaktor**. Værdien i feltet **Enhedspris** for ressourcen vil blive anvendt i projektplanlægningslinjerne og projektkladderne, når denne ressource, en ressource, der er tildelt ressourcegruppen, eller en hvilken som helst ressource angives. Denne pris tilsidesætter eventuelle priser på den eksisterende **Ressourcesalgspris/Ressourcegruppe**-side.|
|**Projektvarer**|Felterne **Projektopgavenr.**, **Valutakode** og **Linjerabat i %**. Værdien i feltet **Enhedspris** for varen bruges i projektplanlægningslinjerne og projektkladderne, når varen angives. Prisen tilsidesætter den normale debitorpris (“bedste pris”-mekanismen) for varer. Hvis du vil bruge den normale debitorpris, skal du ikke angive projektvarepriser for projektet.|
|**Finanskonti**|Oplysninger i felterne **Projektopgavenr.**, **Valutakode**, **Linjerabat i %**, **Kostprisfaktor** og **Kostpris** bruges i projektplanlægningslinjerne og projektkladderne, når denne finanskonto angives og tilføjes til projektet. Værdien i feltet **Kostpris** for finanskontoprojektudgiften bruges i projektplanlægningslinjerne og projektkladderne, når denne finanskonto angives.|

#### [Ny oplevelse](#tab/new-experience)

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Markér det relevante projekt, og vælg derefter handlingen **Salgsprislister**.

---

## <a name="to-set-up-project-posting-groups"></a>Sådan oprettes projektbogføringsgrupper

Et aspekt af planlægningsprojekter er at beslutte, hvilke bogføringskonti der skal bruges til projektomkostninger. Hvis du vil bogføre projekter, skal du oprette konti til bogføring for hver projektbogføringsgruppe. En bogføringsgruppe repræsenterer en kæde mellem projektet, og hvordan den bør behandles i Finans. Når du opretter et projekt, kan du angive en bogføringsgruppe, og som standard knyttes hver opgave, du opretter for projektet, til denne bogføringsgruppe. Når du opretter opgaver, kan du tilsidesætte standardindstillingen og vælge en bogføringsgruppe, der passer bedre.  

> [!NOTE]  
> Du skal konfigurere konti i kontoplanen, før du kan oprette bogføringsgrupper. Du kan finde flere oplysninger i [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md).  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektbogføringsgrupper**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne som beskrevet i følgende tabel.  

| Feltet Konto | Beskrivelse | Brugt i WIP-type |
| --- | --- |  --- |
| **Kode** |En identitet for bogføringsgruppen. Du kan indtaste op til 10 tegn inkl. mellemrum. | |
| **Konto til VIA-omkostning** |Kontoen for igangværende arbejde for den beregnede omkostning for projektets igangværende arbejde, som er en anlægsaktivkonto på balancen. | Anvendt omkostning, realiserede omkostninger|
| **Konto til periodiske VIA-omkostninger** |En konto til metoden Kostværdi eller Salgsomkostning for beregning af igangværende arbejde. Kontoen er til skyldige omkostninger på balancen. Der bogføres til denne konto, når reguleringen af igangværende arbejde kræver, at de forbrugsomkostninger, der er bogført til resultatopgørelsen, forhøjes. | Periodiserede omkostninger|
| **Konto til anvendte projektomkostninger** |En modkonto til kontoen til VIA-omkostninger, som er en kontra for en konto med negative udgifter. Bruges, når **Anvendt bogføringsmetode for igangværende arbejde** er angivet til *Projekt*. | Anvendte omkostninger, realiserede omkostninger|
| **Konto til anvendte vareomkostninger** |Samme som **Konto anvendt til projektomkostninger**, men bruges, når **Anvendt bogføringsmetode for igangværende arbejde** er angivet til *Projektposten*.| |
| **Konto til anvendte ressourceomkostninger** |Samme som **Konto anvendt til projektomkostninger**, men bruges, når **Anvendt bogføringsmetode for igangværende arbejde** er angivet til *Projektposten*.| |
| **Konto til anvendte finansomkostninger** |Samme som **Konto anvendt til projektomkostninger**, men bruges, når **Anvendt bogføringsmetode for igangværende arbejde** er angivet til *Projektposten*.| |
| **Konto til regulering af projektomkostninger** |Modkontoen til kontoen til de periodiske VIA-omkostninger, som er en udgiftskonto. | Periodiserede omkostninger|
| **Driftskonto (budget)** |Den salgskonto, der vil blive brugt til finansudgifter i projektopgaver med denne bogføringsgruppe. Hvis den er tom, bruges den finanskonto, som blev angivet på projektplanlægningslinjen. | |
| **Konto til periodisk VIA-salg** |Kontoen for igangværende arbejde for den beregnede salgsværdi af igangværende arbejde, som er en konto for periodiske indtægter på balancen. Der bogføres til denne konto, når reguleringen for igangværende arbejde kræver, at den registrerede omsætning, skal forhøjes. | Periodiseret salg, realiseret salg|
| **Konto til faktureret VIA-salg** |Kontoen for den fakturerede salgsværdi af VIA, som ikke kan registreres. Det er en konto til ikke-indtjent omsætning på balancen. | Realiseret salg, anvendt salg|
| **Konto til anvendt projektsalg** |Modkontoen til kontoen til det fakturerede VIA-salg, som er en kontraindtægtskonto. | Anvendt salg, realiseret salg|
| **Konto til regulering af projektsalg** |Modkontoen til sagssalgskontoen for igangværende arbejde, som er en indtægtskonto. | Periodiseret salg|
| **Konto til realiserede omkostninger** |Den udgiftskonto, som indeholder de registrerede omkostninger for projektet. Det er normalt en debetafrundingskonto. | Realiserede omkostninger|
| **Konto til realiseret salg** |Den indtægtskonto, som indeholder den registrerede indtægt for projektet. Det er normalt en kreditafrundingskonto. | Realiseret salg|

## <a name="see-also"></a>Se også

[Opsætte projektstyring](projects-setup-projects.md)  
[Video: Sådan oprettes et projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
