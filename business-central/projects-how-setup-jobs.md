---
title: Oprette sagspriser og sagsbogføringsgrupper | Microsoft Docs
description: Bruges til at oprette oplysninger om almindelige opgaver og oprette priser for sagsvarer, ressourcer og finanskonti og sagsbogføringsgrupper.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6fe583e93261b58d13802eadef5f3d807045fa20
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758638"
---
# <a name="set-up-jobs"></a>Opsætte sager

Som projektleder kan du oprette sager, der definerer hvert af de projekter, som du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Sagsopsætning** skal du angive, hvordan du vil bruge bestemte sagsfunktioner.

For hver sag kan du derefter specificere de individuelle jobkort med oplysninger om priser for sagsvarer, sagsressourcer og sagsfinanskonti, og du skal oprette sagsbogføringsgrupper.

## <a name="to-set-general-information-for-jobs"></a>Sådan angives generelle oplysninger for sager
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagsopsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Virkningen af feltet **Anvend anvendelseslink som standard** er temmelig komplekst og forklares derfor i følgende afsnit.

### <a name="to-set-up-job-usage-tracking"></a>Sådan definerer du sagsforbrugssporing

Når du ekspederer en sag, kan du få flere oplysninger om forbruget i forhold til din plan. Det kan du nemt gøre ved at oprette en tilknytning mellem dine sagsplanlægningslinjer og det faktiske forbrug. På denne måde kan du holde styr på dine omkostninger og nemt se, hvor meget arbejde, der mangler at blive udført. Som standard er sagsplanlægningslinjetypen **Budget**, men brug af linjetypen **Både budget og fakturerbar** har samme virkning.

Hvis du markerer feltet **Anvend anvendelseslink som standard**, kan du gennemse oplysninger på sagsplanlægningslinjen. Du kan angive antallet af ressourcen, varen eller finanskontoen, og derefter angive, hvilket antal du vil overføre til sagskladde. I feltet **Restantal** på sagsplanlægningslinjen kan du se, hvad der stadig mangler at blive overført og bogført på sagskladden.

> [!TIP]  
> Du kan aktivere eller deaktivere sagsforbrugssporing for en bestemt sag. Værdien i feltet **Anvend anvendelseslink som standard** på det enkelte sagskort tilsidesætter indstillingen på siden **Sagsopsætning**.  

Når afkrydsningsfelt **Anvend anvendelseslink som standard** er markeret, og sagsplanlægningslinjetypen er **Fakturerbar**, oprettes en sagsplanlægningslinje af typen **Budget**, når du har bogført en sagskladdelinje.

> [!IMPORTANT]
> Hvis sagsforbrugssporing er aktiveret på siden **Sagsopsætning** eller i den individuelle sag, og feltet **Linjetype** på sagskladdelinjen er tomt, oprettes nye sagsplanlægningslinjer for linjetypen **Budget**, når du bogfører sagskladdelinjer.  
>  
> Hvis sagsforbrugssporing *ikke* er aktiveret på siden **Sagsopsætning** eller i den individuelle sag, og feltet **Linjetype** på sagskladdelinjen er tomt, oprettes ingen sagsplanlægningslinjer, når du bogfører sagskladdelinjer. Du kan finde flere oplysninger under [Registrere forbrug for sager](projects-how-record-job-usage.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sagsopsætning**, og vælg derefter det relaterede link.
2. Markér afkrydsningsfeltet **Anvend anvendelseslink som standard**.

## <a name="to-set-up-prices-for-job-resources"></a>Sådan oprettes priser for sagsressourcer
Du kan oprette specifikke priser for ressourcer for en sag. Det gør du på siden **Ressourcepriser for sag**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Ressourcer**.
3. På siden **Sagsressourcepriser** skal du udfylde felterne efter behov.

De valgfrie oplysninger i felterne **Sagsopgavenr.**, **Arbejdstype**, **Valutakode**, **Linjerabatpct.** og **Kostprisfaktor** bruges i sagsplanlægningslinjerne og forbrugskladderne, når ressourcen angives og tilføjes til sagen.  

Værdien i feltet **Enhedspris** for ressourcen vil blive anvendt i sagsplanlægningslinjerne og sagskladderne, når denne ressource, en ressource, der er tildelt ressourcegruppen, eller en hvilken som helst ressource angives.  

> [!NOTE]  
>   Denne pris vil altid tilsidesætte eventuelle priser på den eksisterende **Ressourcesalgspris/Ressourcegruppe**-side.

## <a name="to-set-up-prices-for-job-items"></a>Sådan oprettes priser for sagsvarer
Du kan oprette specifikke priser for varer for en sag. Det gør du på siden **Sagsvarepriser**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Vare**.
3. På siden **Sagsvarepriser** skal du udfylde felterne efter behov.

De valgfrie oplysninger i felterne **Sagsopgavenr.**, **Valutakode** og **Linjerabat %** bruges i sagsplanlægningslinjerne og forbrugskladderne, når ressourcen angives og tilføjes til sagen.  

Værdien i feltet **Enhedspris** for varen bruges i sagsplanlægningslinjerne og sagskladderne, når varen angives.  

> [!NOTE]  
>   Prisen vil altid tilsidesætte den normale debitorpris (“bedste pris”-mekanismen) for varer. Hvis du vil bruge den normale debitorpris, skal du ikke oprette sagsvarepriser.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Sådan oprettes priser for finanskonti for sag
Du kan oprette specifikke priser for regnskabsmæssige udgifter for en sag. Det gør du på siden **Sagsfinanskontopriser**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Markér den relevante sag, og vælg derefter handlingen **Finanskonto**.  
3. På siden **Sagsfinanskontopriser** skal du udfylde felterne efter behov.

De valgfrie oplysninger i felterne **Sagsopgavenr.**, **Valutakode**, **Linjerabatpct.**, **Kostprisfaktor** og **Kostpris** bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives og tilføjes til sagen.  

Værdien i feltet **Kostpris** for finanskontosagsudgiften bruges i sagsplanlægningslinjerne og sagskladderne, når denne finanskonto angives.

## <a name="to-set-up-job-posting-groups"></a>Sådan oprettes sagsbogføringsgrupper
Et aspekt af planlægningssager er at beslutte, hvilke bogføringkonti, der skal bruges til sagsomkostninger. Hvis du vil bogføre sager, skal du oprette konti til bogføring for hver sagsbogføringsgruppe. En bogføringsgruppe repræsenterer en kæde mellem sagen, og hvordan den bør behandles i Finans. Når du opretter en sag, kan du angive en bogføringsgruppe, og som standard knyttes hver opgave, du opretter for sagen, til denne bogføringsgruppe. Når du opretter opgaver, kan du tilsidesætte standardindstillingen og vælge en bogføringsgruppe, der passer bedre.  

> [!NOTE]  
>   De nødvendige konti, der skal bogføres til i tabellen over konti skal oprettes, før du kan oprette bogføringsgrupper. Du kan finde flere oplysninger i [Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md).  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagsbogføringsgrupper**, og vælg derefter det relaterede link.  
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

## <a name="see-also"></a>Se også

[Oprette projektstyring](projects-setup-projects.md)  
[Video: Sådan oprettes en sag i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere projekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]