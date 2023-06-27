---
title: Bruge godkendelsesworkflows
description: Du kan oprette og bruge workflows til at knytte forretningsprocesopgaver som f. eks. automatisk bogføring eller anmodning om godkendelse af nye poster.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="use-approval-workflows"></a>Bruge godkendelsesworkflows

Et workflow er en række opgaver, der udløses af en handling, en betingelse eller en regel. Workflows implementeres som regel med henblik på at integrere forretningslogikken i en virksomhed, f. eks. adskillelse af opgaver, samling af opgaver eller anvendelse af bedste praksis.

Workflows kan designes til at oprette anmodninger om godkendelse af en postfeltændring, samtidig med at de gamle data, der bevares, ikke godkendes. Den nye værdi implementeres først, når den sidste anmodning er godkendt.

Forretningslogikken kan være godkendelsen af:

- Nye stamdata som f. eks. finanskonti, debitorer, kreditorer eller varer.
- Ændringer af felter i eksisterende poster, der indeholder Sensible-oplysninger, f . eks. **kreditors bankkonto nr.** eller **debitorkreditmaksimum**.
- Ændringer af felter i eksisterende poster, der indeholder vigtige virksomhedsoplysninger, f. eks. **varesalgspriser**.
- Nye brugere eller ændringer i brugertilladelser.
- Købsdokumenter.
- Salgsdokumenter.
- Indgående dokumenter.
- Finanskladder inden bogføring.

Følgende illustration er et eksempel på en arbejdsgang med fortløbende godkendelse fra en bruger. Ved at udløse en arbejdsgang oprettes der en godkendelsesanmodning for den første godkender.  

![Illustration af en arbejdsproces med fortløbende godkendelse.](media/Workflows/approval-flow.png)

I eksemplet herover kan du se, hvordan anmodningen skal godkendes af den første godkender, før den sendes til den næste. Hvis anmodningen ikke er godkendt af den første godkender, går anmodningen aldrig videre til den næste.

Den rute, der hentes fra den første udløsning af arbejdsgangen, kan variere afhængigt af arten af godkendelsen.  

Følgende illustration viser en parallel godkendelse, som udløses af brugeren. En parallel godkendelse betyder en anmodning om godkendelse til alle godkendere samtidig.  

![Illustration af en arbejdsproces med sideløbende godkendelse.](media/Workflows/approval-flow-2.png)

Arbejdsprocessen er dog ikke godkendt, før alle anmodninger er godkendt af godkenderne, som vist i følgende illustration:  

![Illustration af en afvist arbejdsproces med sideløbende godkendelse.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Til et workflow med flere godkendere skal alle godkendere godkende hvert trin, før arbejdsprocessen kan gå videre til næste hændelse. Godkendelse fra kun én godkender, flytter ikke arbejdsgangen videre.

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Du kan også oprette den samme arbejdsgang mere end én gang. Hver arbejdsproces kan udløses af en hændelse med forskellige filtre. Dette er nyttigt, hvis en godkendelsesanmodning i én afdeling skal godkendes af en godkender, hvor en anden godkender anmoder om godkendelsesanmodninger af en anden godkender. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

Inden du kan bruge workflows, skal du oprette arbejdsgangbrugere, oprette workflows, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser. Flere oplysninger i [Konfigurere workflows](across-set-up-workflows.md).

> [!NOTE]  
> Typiske workflowtrin involverer brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger. Derfor henviser mange emner om brug af workflows til godkendelser.  

 Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.  

| **Hvis du vil** | **Se** |
|--|--|
| Angiv, at et godkendelsesworkflow skal startes, når den første startpunkthændelse finder sted. | [Aktivere godkendelsesworkflows](across-how-to-enable-workflows.md) |
| Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer. | [Sådan bruger du godkendelsesworkflows](across-how-use-approval-workflows.md) |
| Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes. | [Begrænse og tillade brugen af en record](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Vis forekomsten af workflowtrin med statussen **Afsluttet**. | [Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md) |
| Slet et godkendelsesworkflow, som du er sikker på ikke længere bruges. | [Slette godkendelsesworkflows](across-how-to-delete-workflows.md) |

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurere godkendelsesworkflows](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
