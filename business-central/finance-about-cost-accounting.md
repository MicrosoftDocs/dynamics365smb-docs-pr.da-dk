---
title: Om omkostningsregnskab
description: Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed. Omkostningsregnskabsoplysninger er udviklet til at analysere forskellige situationer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 08/23/2022
ms.author: bholtorf
---
# Om omkostningsregnskab

Omkostningsregnskab kan hjælpe dig med at forstå omkostningerne til drift af en virksomhed. Omkostningsregnskabsoplysninger er udviklet til at analysere:  

- Hvilke omkostningstyper du pålægger en virksomheds drift  
- Hvor omkostningerne opstår
- Hvem der bærer omkostningerne  

Du kan allokere faktiske og budgetterede udgifter til operationer, afdelinger, produkter og projekter for at analysere dit virksomhed rentabilitet i omkostningsregnskab.  

## Arbejdsgang i omkostningsregnskab

Omkostningsregnskab har følgende hovedkomponenter:  

- Omkostningstyper, omkostningssteder og omkostningsobjekter  
- Omkostningsposter og omkostningskladder  
- Omkostningsfordelinger  
- Omkostningsbudgetter
- Rapportering af omkostninger  

Følgende diagram viser arbejdsprocessen i omkostningsregnskab.  

![Oversigt over omkostningsregnskab.](media/costaccountingoverview.png "OversigtOverOmkostningsregnskab")  

## Omkostningstyper, omkostningssteder og omkostningsobjekter

Du definerer omkostningstyper, omkostningssteder og omkostningsobjekter for at analysere, hvad omkostningerne er, hvor omkostningerne kommer fra, og hvem skal bære omkostningerne.  

Du definerer først et diagram over omkostningstyper med en struktur og funktionalitet, der ligner finanskontoplan. Du kan oprette dit eget diagram over omkostningstyper eller overføre finansresultatopgørelseskonti.  

Omkostningssteder er afdelinger og profitcentre med ansvar for omkostninger og indtægter. Der findes ofte flere omkostningssteder i omkostningsregnskab end i andre dimensioner, der er oprettet i regnskabet. I regnskabet er der normalt kun første niveau af omkostningssteder for direkte omkostninger, og de oprindelige omkostninger anvendes. I omkostningsregnskab oprettes ekstra omkostningssteder for yderligere allokeringsniveauer.  

Omkostningsobjekter er en virksomheds produkter, produktgrupper eller tjenester. Disse er en virksomheds "færdigvarer", der bærer omkostningerne.  

Du kan sammenkæde omkostningssteder med afdelinger og omkostningsobjekter med projekter i din virksomhed. Vis Finans kan du knytte omkostningssteder og omkostningsobjekter til enhver dimension og supplere dem med subtotaler og titler.  

## Omkostningsposter og omkostningskladder

Driftsomkostningerne kan overføres fra regnskabet. Du kan automatisk overføre omkostningsposterne fra regnskabet til omkostningsposter med hver bogføring. Du kan også bruge et batchjob til at overføre finansposterne til omkostningsposterne på daglig eller månedlig summarisk bogføring.  

I omkostningskladder kan du bogføre omkostninger og aktiviteter, der ikke kommer fra regnskabet, eller der ikke er genereret af allokeringer. For eksempel kan du bogføre rene driftsomkostninger, interne afgifter, allokeringer og korrigerende poster mellem omkostningstyper, omkostningssteder og omkostningsobjekter enkeltvist eller på tilbagevendende basis.  

## Omkostningsfordelinger

Allokeringer flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Faste omkostninger bogføres først til omkostningssteder og senere til omkostningsobjekter. Dette kan for eksempel gøres i en salgsafdeling, der sælger flere produkter på samme tid. Afdelingens faste omkostninger, f.eks. løn, forsyninger og rejseudgifter, er først tildelt salgsomkostningsstedet, som derefter fordeles mellem de forskellige produkter (omkostningsobjekter), der sælges, sammen med de indkøbte materialer (direkte omkostninger) til brug i dem.

Den fordelingsbasis, der bruges, og nøjagtigheden af fordelingsdefinitionen har indflydelse på resultaterne af omkostningsfordelinger. Fordelingsdefinitionen bruges til at allokere omkostninger først fra såkaldte pre-omkostningssteder til primære omkostningssteder og derefter fra omkostningssteder til omkostningsobjekter.  

Hver allokering består af en fordelingskilde og en eller flere fordelingsmål. Du kan allokere faktiske værdier eller budgetterede værdier ved hjælp af den statiske fordelingsmetode, der er baseret på en endelig værdi, som f.eks. kvadratmeter eller en etableret fordelingsforhold på 5:2:4. Du kan også tildele faktiske værdier eller budgetterede værdier ved hjælp af den dynamiske fordelingsmetode med ni foruddefinerede allokeringsbaser og 12 dynamiske datointervaller.  

## Omkostningsbudgetter

På samme måde som ved budgettering i finansmodulet kan du oprette budgetter for at planlægge omkostninger i en bestemt periode (f.eks. et regnskabsår), der kan anvendes på et omkostningssted (firmaafdeling) eller et omkostningsobjekt (produkt eller service). Du kan oprette lige så mange omkostningsbudgetter, du har brug for. Du kan kopiere omkostningsbudgettet til finansbudget og omvendt. Og du kan overføre budgetterede omkostninger som faktiske omkostninger.

## Rapportering af omkostninger

De fleste rapporter og statistikker er baseret på bogførte omkostningsposter. Du kan angive sorteringen af resultaterne og bruge filtre til at definere, hvilke data, der skal vises. Du kan oprette rapporter for omkostningsfordelingsanalyse. Du kan desuden bruge standardfinansrapporter til at definere, hvordan dine rapporter for diagrammet over omkostningstyper vises.  

## Se relateret [Microsoft-træning](/training/paths/use-cost-accounting-dynamics-365-business-central/)

## Se også

[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Finans](finance.md)  
[Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
