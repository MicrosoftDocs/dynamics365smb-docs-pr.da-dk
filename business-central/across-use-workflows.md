---
title: Anvende workflows
description: Du kan oprette og bruge arbejdsprocesser, der knytter forretningsproces opgaver som f. eks. automatisk bogføring eller anmodning om godkendelse af nye poster.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 767b2873e0c7307a9642aa3b38d049b4869f7a1b
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531184"
---
# <a name="use-workflows"></a>Bruge arbejdsprocesser

En arbejdsproces er en række opgaver, der udløses af en handling, en betingelse eller en regel. Arbejdsprocesser implementeres som regel med henblik på at integrere forretningslogikken i en virksomhed, f. eks. adskillelse af opgaver, samling af opgaver eller større tillid og ansvar.  

Arbejdsprocesserne er beregnet til at oprette anmodninger om godkendelse af en ny værdi, samtidig med at den gamle værdi bevares, ikke godkendes. Den nye værdi implementeres først, når den sidste anmodning er godkendt.  

Forretningslogikken kan være godkendelse af:

- Nye stamdata som f. eks. finanskonti, debitorer, kreditorer eller varer
- Ændringer af felter i eksisterende poster, der indeholder Sensible-oplysninger, f . eks. **kreditors bankkonto nr.** eller **debitorkreditmaksimum**
- Ændringer af felter i eksisterende poster, der indeholder vigtige virksomhedsoplysninger, f. eks. **varesalgspriser**
- Nye brugere eller ændringer i brugertilladelser
- Købsdokumenter
- Salgsdokumenter
- Indgående dokumenter
- Finanskladder inden bogføring

Følgende illustration viser et eksempel på en arbejdsgang med fortløbende godkendelse fra en bruger. Ved at udløse en arbejdsgang oprettes der en godkendelsesanmodning for den første godkender.  

![Illustration af en arbejdsproces med fortløbende godkendelse.](media/Workflows/approval-flow.png)

I dette eksempel skal anmodningen godkendes af den første godkender, før anmodningen sendes til den næste godkender. Hvis anmodningen ikke er godkendt af den første godkender, går anmodningen aldrig videre til den næste godkender.  

Den rute, der hentes fra den første udløsning af arbejdsgangen, kan variere afhængigt af arten af godkendelsen.  

Følgende illustration viser en parallel godkendelse, som udløses af brugeren. Ved at udløse en arbejdsgang sendes der en anmodning om godkendelse til alle godkendere samtidig.  

![Illustration af en arbejdsproces med sideløbende godkendelse.](media/Workflows/approval-flow-2.png)

Arbejdsprocessen er dog ikke godkendt, før alle anmodninger er godkendt af godkenderne, som vist i følgende illustration:  

![Illustration af en afvist arbejdsproces med sideløbende godkendelse.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Det er ikke muligt at oprette en arbejdsproces med flere godkendere og forventer, at hele arbejdsprocessen godkendes, efter at den første anmodning er godkendt. Alle anmodninger skal være godkendt, før arbejdsprocessen kan godkendes.

Du kan oprette og bruge arbejdsgange, der forbinder forretningsprocesopgaver, der udføres af forskellige brugere. Du kan også oprette den samme arbejdsgang mere end én gang. Hver arbejdsproces kan udløses af en hændelse med forskellige filtre. Dette er nyttigt, hvis en godkendelsesanmodning i én afdeling skal godkendes af en godkender, mens en anden godkender anmoder om godkendelsesanmodninger i andre afdelinger. Systemopgaver, f.eks automatisk bogføring, kan medtages som trin i arbejdsgange, med forudgående eller efterfølgende brugeropgaver. Anmodning om og tildeling af tilladelse til at oprette nye poster er typiske arbejdsgangstrin.  

Inden du kan bruge arbejdsprocesser, skal du oprette arbejdsgangbrugere, oprette arbejdsgangene, som kan være med tilpasning af kode, og angive, hvordan brugere får vist meddelelser. Du kan finde flere oplysninger i [Opsætte workflows](across-set-up-workflows.md).  

> [!NOTE]  
> Typiske arbejdsgangstrin er om brugere, der anmoder om godkendelse af opgaver, og godkendere, der accepterer eller afviser godkendelsesanmodninger. Derfor henviser mange emner om brug af workflows til godkendelser.  

 Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Angiv, at en arbejdsgang skal startes, når den første startpunkthændelse finder sted.|[Aktivere arbejdsgange](across-how-to-enable-workflows.md)|  
|Anmode om godkendelse af en opgave, som godkender, godkende, afvise eller uddelegere godkendelser og sende eller få vist godkendelsesnotifikationer.|[Bruge godkendelsesworkflows](across-how-use-approval-workflows.md)|  
|Opret arbejdsgangstrin, der sikrer, at en bestemt posttype ikke bruges, før en bestemt hændelse opstår, for eksempel at posten godkendes.|[Begrænse og tillade brugen af en record](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Vis forekomsten af workflowtrin med statussen **Afsluttet**.|[Vise arkiverede forekomster af workflowtrin](across-how-to-view-archived-workflow-step-instances.md)|  
|Slet et workflow, som du er sikker på ikke længere bruges.|[Slette arbejdsgange](across-how-to-delete-workflows.md)|  

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Opsætte workflows](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
