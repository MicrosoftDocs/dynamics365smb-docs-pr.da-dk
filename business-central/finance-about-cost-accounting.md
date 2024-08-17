---
title: Om omkostningsregnskab
description: Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed. Omkostningsregnskabsoplysninger er udviklet til at analysere forskellige situationer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="about-cost-accounting"></a>Om omkostningsregnskab

Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed. Omkostningsregnskabsoplysninger er udviklet til at analysere:  

- Hvilke typer omkostninger din virksomhed pålægger.  
- Hvor omkostningerne opstår.
- Hvem der bærer omkostningerne.

Du kan allokere faktiske og budgetterede udgifter til operationer, afdelinger, produkter og projekter for at analysere dit virksomhed rentabilitet i omkostningsregnskab.  

## <a name="workflow-in-cost-accounting"></a>Arbejdsgang i omkostningsregnskab

Omkostningsregnskab har følgende hovedkomponenter:  

- Omkostningstyper, omkostningssteder og omkostningsobjekter  
- Omkostningsposter og omkostningskladder  
- Omkostningsfordelinger  
- Omkostningsbudgetter
- Rapportering af omkostninger  

Følgende diagram viser arbejdsprocessen i omkostningsregnskab.  

![Oversigt over omkostningsregnskab.](media/costaccountingoverview.png "OversigtOverOmkostningsregnskab")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Omkostningstyper, omkostningssteder og omkostningsobjekter

Du definerer omkostningstyper, omkostningssteder og omkostningsobjekter for at analysere, hvad omkostningerne er, hvor omkostningerne kommer fra, og hvem skal bære omkostningerne.  

Du definerer først et diagram over omkostningstyper med en struktur og funktionalitet, der ligner finanskontoplan. Du kan oprette dit eget diagram over omkostningstyper eller overføre finansresultatopgørelseskonti.  

Omkostningssteder er afdelinger og profitcentre med ansvar for omkostninger og indtægter. Der findes ofte flere omkostningssteder i omkostningsregnskab end i andre dimensioner, der er oprettet i regnskabet. I regnskabet er der typisk kun første niveau af omkostningssteder for direkte omkostninger, og de oprindelige omkostninger anvendes. I omkostningsregnskab oprettes flere omkostningssteder for yderligere allokeringsniveauer.  

Omkostningsobjekter er en virksomheds produkter, produktgrupper eller tjenester. Disse objekter er "færdigvarer", der bærer omkostningerne.  

Du kan sammenkæde omkostningssteder med afdelinger og omkostningsobjekter med projekter i din virksomhed. Vis Finans kan du knytte omkostningssteder og omkostningsobjekter til enhver dimension og supplere dem med subtotaler og titler.  

## <a name="cost-entries-and-cost-journals"></a>Omkostningsposter og omkostningskladder

Driftsomkostningerne kan overføres fra regnskabet. Du kan automatisk overføre omkostningsposterne fra regnskabet til omkostningsposter med hver bogføring. Du kan også bruge et batchjob til at overføre finansposterne til omkostningsposterne på daglig eller månedlig summarisk bogføring.  

I omkostningskladder kan du bogføre omkostninger og aktiviteter, der ikke kommer fra regnskabet, eller der ikke er genereret af allokeringer. For eksempel kan du bogføre rene driftsomkostninger, interne afgifter, allokeringer og korrigerende poster mellem omkostningstyper, omkostningssteder og omkostningsobjekter enkeltvist eller på tilbagevendende basis.  

## <a name="cost-allocations"></a>Omkostningsfordelinger

Allokeringer flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Faste omkostninger bogføres først til omkostningssteder og senere til omkostningsobjekter. Et eksempel kan være en salgsafdeling, der sælger flere produkter på samme tid. Afdelingens faste kostpriser, f.eks. lønninger, forsyninger og rejseudgifter, knyttes i første omgang til salgsomkostningscenteret. Omkostningerne fordeles derefter mellem de forskellige solgte produkter (omkostningsobjekter) sammen med de købte materialer (direkte omkostninger).

Den fordelingsbasis, der bruges, og nøjagtigheden af fordelingsdefinitionen har indflydelse på resultaterne af omkostningsfordelinger. Fordelingsdefinitionen bruges til at allokere omkostninger først fra såkaldte pre-omkostningssteder til primære omkostningssteder og derefter fra omkostningssteder til omkostningsobjekter.  

Hver allokering består af en fordelingskilde og en eller flere fordelingsmål. Du kan allokere faktiske værdier eller budgetterede værdier ved hjælp af den statiske allokeringsmetode baseret på en bestemt værdi. Det kan f.eks. være kvadratmeter eller et etableret fordelingsforhold på 5:2:4. Du kan også tildele faktiske værdier eller budgetterede værdier ved hjælp af den dynamiske fordelingsmetode med ni foruddefinerede allokeringsbaser og 12 dynamiske datointervaller.  

## <a name="cost-budgets"></a>Omkostningsbudgetter

På samme måde som ved budgettering i finansmodulet kan du oprette budgetter for at planlægge omkostninger i en bestemt periode (f.eks. et regnskabsår), der kan anvendes på et omkostningssted (firmaafdeling) eller et omkostningsobjekt (produkt eller service). Du kan oprette lige så mange omkostningsbudgetter, du har brug for. Du kan kopiere omkostningsbudgettet til finansbudget og omvendt. Og du kan overføre budgetterede omkostninger som faktiske omkostninger.

## <a name="cost-reporting"></a>Rapportering af omkostninger

De fleste rapporter og statistikker er baseret på bogførte omkostningsposter. Du kan angive sorteringen af resultaterne og bruge filtre til at definere, hvilke data, der skal vises. Du kan oprette rapporter for omkostningsfordelingsanalyse. Du kan desuden bruge standardfinansrapporter til at definere, hvordan dine rapporter for diagrammet over omkostningstyper vises.  

## <a name="see-also"></a>Se også

[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Finans](finance.md)  
[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
