---
title: Om omkostningsregnskab | Microsoft Docs
description: Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d8628953230b27ae84ee363d41c43873c81cb11c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919526"
---
# <a name="about-cost-accounting"></a>Om omkostningsregnskab
Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed. Omkostningsregnskabsoplysninger er udviklet til at analysere:  

-   Hvilke typer omkostninger, der påløber, når du driver en virksomhed?  
-   Hvor opstår omkostningerne?  
-   Hvem bærer omkostningerne?  

Du kan allokere faktiske og budgetterede udgifter til operationer, afdelinger, produkter og projekter for at analysere dit virksomhed rentabilitet i omkostningsregnskab.  

## <a name="workflow-in-cost-accounting"></a>Arbejdsgang i omkostningsregnskab  
Omkostningsregnskab har følgende hovedkomponenter:  

-   Omkostningstyper, omkostningssteder og omkostningsobjekter  
-   Omkostningsposter og omkostningskladder  
-   Omkostningsfordelinger  
-   Omkostningsbudgetter
-   Rapportering af omkostninger  

Følgende diagram viser arbejdsprocessen i omkostningsregnskab.  

![Oversigt over omkostningsregnskab](media/costaccountingoverview.png "OversigtOverOmkostningsregnskab")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Omkostningstyper, omkostningssteder og omkostningsobjekter  
Du definerer omkostningstyper, omkostningssteder og omkostningsobjekter for at analysere, hvad omkostningerne er, hvor omkostningerne kommer fra, og hvem skal bære omkostningerne.  

Du definerer et diagram over omkostningstyper med en struktur og funktionalitet, der ligner finanskontoplan. Du kan overføre finansresultatopgørelseskonti eller oprette dit eget diagram over omkostningstyper.  

Omkostningssteder er afdelinger og profitcentre, der er ansvarlige for omkostninger og indtægter. Der findes ofte flere omkostningssteder i omkostningsregnskab end i andre dimensioner, der er oprettet i regnskabet. I regnskabet er der normalt kun første niveau af omkostningssteder for direkte omkostninger, og de oprindelige omkostninger anvendes. I omkostningsregnskab oprettes ekstra omkostningssteder for yderligere allokeringsniveauer.  

Omkostningsobjekter er en virksomheds produkter, produktgrupper eller tjenester. Disse er en virksomheds færdige varer, der bærer omkostningerne.  

Du kan sammenkæde omkostningssteder med afdelinger og omkostningsobjekter med projekter i din virksomhed. Du kan dog knytte omkostningssteder og omkostningsobjekter til alle dimensioner i regnskabet og supplere dem med subtotaler og titler.  

## <a name="cost-entries-and-cost-journals"></a>Omkostningsposter og omkostningskladder  
Driftsomkostningerne kan overføres fra regnskabet. Du kan automatisk overføre omkostningsposterne fra regnskabet til omkostningsposter med hver bogføring. Du kan også bruge et batchjob til at overføre finansposterne til omkostningsposterne på daglig eller månedlig summarisk bogføring.  

I omkostningskladder kan du bogføre omkostninger og aktiviteter, der ikke kommer fra regnskabet, eller der ikke er genereret af allokeringer. For eksempel kan du bogføre rene driftsomkostninger, interne afgifter, allokeringer og korrigerende poster mellem omkostningstyper, omkostningssteder og omkostningsobjekter enkeltvist eller på tilbagevendende basis.  

## <a name="cost-allocations"></a>Omkostningsfordelinger  
Allokeringer flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Faste omkostninger bogføres først til omkostningssteder og senere til omkostningsobjekter. Dette kan for eksempel gøres i en salgsafdeling, der sælger flere produkter på samme tid. Direkte omkostninger kan direkte allokeres til et omkostningsobjekt, f.eks. materiale, der køber til et bestemt produkt.  

Den fordelingsbasis, der bruges, og nøjagtigheden af fordelingsdefinitionen har indflydelse på resultaterne af omkostningsfordelinger. Fordelingsdefinitionen bruges til at allokere omkostninger først fra såkaldte pre-omkostningssteder til primære omkostningssteder og derefter fra omkostningssteder til omkostningsobjekter.  

Hver allokering, der består af en fordelingskilde og mål for en eller flere fordelinger. Du kan allokere faktiske værdier eller budgetterede værdier ved hjælp af den statiske fordelingsmetode, der er baseret på en endelig værdi, som f.eks. kvadratmeter eller en etableret fordelingsforhold på 5: 2: 4. Du kan også tildele faktiske værdier eller budgetterede værdier ved hjælp af den dynamiske fordelingsmetode med ni foruddefinerede allokeringsbaser og 12 dynamiske datointervaller.  

## <a name="cost-budgets"></a>Omkostningsbudgetter  
Du kan oprette lige så mange omkostningsbudgetter, du vil. Du kan kopiere omkostningsbudgettet til finansbudget og omvendt. Du kan overføre budgetterede omkostninger som faktiske omkostninger.  

## <a name="cost-reporting"></a>Rapportering af omkostninger  
De fleste rapporter og statistikker er baseret på bogførte omkostningsposter. Du kan angive sorteringen af resultaterne og bruge filtre til at definere, hvilke data, der skal vises. Du kan oprette rapporter for omkostningsfordelingsanalyse. Du kan desuden bruge standardkontoskemaerne til at definere, hvordan dine rapporter for diagrammet over omkostningstyper vises.  

## <a name="see-also"></a>Se også  
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)  
 [Finans](finance.md)   
 [Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
