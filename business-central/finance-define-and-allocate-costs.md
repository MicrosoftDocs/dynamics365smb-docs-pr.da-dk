---
title: Definere og allokere omkostninger | Microsoft Docs
description: Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Du kan angive så mange tildelinger, som du har brug for.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9d4167751289b26926bdde3148d6f2241df787cf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388595"
---
# <a name="defining-and-allocating-costs"></a>Definere og allokere omkostninger
Allokering af omkostninger flytter omkostninger og indtægter mellem omkostningstyper, omkostningssteder og omkostningsobjekter. Du kan angive så mange tildelinger, som du har brug for. Hver allokering består af:  

-   En fordelingskilde.  
-   Et eller flere allokeringsmål.  

Fordelingskilden fastlægger, hvilke omkostninger der skal fordeles, og allokeringsmål bestemmer, hvor omkostningerne skal fordeles til. F.eks. kan en fordelingskilde være omkostningerne for omkostningstypen Elektricitet og varme. Du allokerer alle el- og varmeomkostninger til tre omkostningssteder: Workshop, produktion og salg. Disse omkostningssteder er dine fordelingsmål.  

For hver fordelingskilde skal du definere et fordelingsniveau, en gyldighedsperiode og en variant som gruppe-id. Du kan bruge et batchjob til at angive filtre til valg af allokeringsdefinitioner og derefter køre allokering af omkostninger automatisk.  

Du kan definere en fordelingsbasis for hvert fordelingsmål. Fordelingsbasis kan være enten statisk eller dynamisk.  

-   Statisk allokeringsbasis er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5:2:4.  
-   Dynamisk fordelingsbasis afhænger af værdier, der kan ændres, f.eks antallet af medarbejdere på et omkostningssted eller salgsindtægter fra et omkostningsobjekt i en bestemt tidsperiode.  

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

## <a name="setting-up-allocation-source-and-targets"></a>Konfigurere fordelingskilde og mål
Hver allokering består af en fordelingskilde og en eller flere fordelingsmål. Fordelingskilden definerer, hvilke omkostninger, der vil blive tildelt. Fordelingsmålet bestemmer, hvortil omkostningerne fordeles.  

### <a name="to-set-up-cost-allocations"></a>Opsætning af omkostningsfordelinger  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.  
2.  På siden **Omkostningsfordeling** skal du vælge handlingen **Rediger**.  
3.  Angiv et id for fordelingskilden i feltet **Id**.  
4.  Definer et niveau som et tal mellem 1 og 99 i feltet **Niveau**. Fordelingsbogføringen følger niveauernes rækkefølge.  
5.  Angiv en pristype for at definere, hvilken pris der skal fordeles, i feltet **Omkostningstypeinterval**. Hvis alle omkostninger for en pristype fordeles, defineres der intet område.  
6.  Angiv et omkostningssted sammen med de omkostninger, der skal allokeres, i feltet **Omkostningsstedskode**.  
7.  Angiv et omkostningsemne sammen med de omkostninger, der skal allokeres, i feltet **Omkostningsstedskode**. Feltet forbliver oftest tomt, da der sjældent allokeres omkostningsobjekter til andre omkostningsobjekter.  
8.  Angiv en omkostningstype i feltet **Kredit til omkostningstype**. Omkostningerne, der fordeles, krediteres til kildeomkostningstypen. Kreditnotaen bogføres til den omkostningstype, der er angivet her.  
9. Definer fordelingsmålene på oversigtspanelet **Linjer**. Angiv en omkostningstype på første linje i feltet **Målomkostningstype**. Den definerer, hvilken pristype fordelingen fordeles til.  
10. På den første linje, skal du angive første fordelingsmål i feltet **Målomkostningssted** eller feltet **Målomkostningsemne**. Disse to felter definere, hvilket omkostningssted eller omkostningsobjekt fordeling debiteres til. Du kan kun udfylde et disse felter, ikke begge.  
11. Gentag de samme trin på den anden linje for at angive yderligere fordelingsmål.  
12. Når du har angivet fordelingsmål og -kilder, skal du vælge handlingen **Beregn fordelingsnøgle** for at beregne de samlede fordelingsværdier.  

> [!NOTE]  
>  Vælg afkrydsningsfeltet **Spærret** for at deaktivere fordelingsopsætningen.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Indstilling af filtre for dynamiske allokeringsbaser
Metoden til dynamisk fordeling er baseret på værdier, der kan ændres. For eksempel antal medarbejdere et omkostningssted eller antal solgte varer for et omkostningsobjekt i en bestemt tidsperiode. Der findes ni foruddefinerede fordelingsbaser og tolv dynamiske datointervaller. Du kan angive forskellige filtre, der er baseret på allokeringsbasen.  

### <a name="setting-filters-for-dynamic-allocation-bases"></a>Indstilling af filtre for dynamiske allokeringsbaser  
 Følgende tabel viser, hvilke filtre der er mulige for forskellige tildelingsbaser, og hvilke værdier der er gyldige i felterne **Nummerfilter** og **Gruppefilter**. Tryk på F1 i feltet **Datofilterkode** for at læse detaljerede beskrivelser.  

|**Basis**|**Nummerfilter**|**Datofilterkode**|**Omkostningsstedsfilter**|**Omkostningsemnefilter**|**Gruppefilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Finansposter|Finanskonto|Ja|Ja|Ja|I/R|  
|Finansbudgetposter|Finanskonto|Ja|Ja|Ja|Finansbudgetnavn|  
|Pristypeposter|Pristype|Ja|Ja|Ja|I/R|  
|Omkostningsbudgetposter|Pristype|Ja|Ja|Ja|Budgetnavn|  
|Antal ansatte|I/R|Ja|Ja|Ja|I/R|  
|Varer solgt (antal)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer købt (antal)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer solgt (beløb)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|  
|Varer købt (beløb)|Varenr.|Ja|Ja|Ja|Varebogføringsgruppe|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Scenarieeksempel 1: Definition af statisk allokeringer baseret på fordelingsforholdet
Metoden statisk allokering er baseret på en endelig værdi, for eksempel anvendt antal kvadratmeter eller et etableret fordelingsforhold såsom 5: 2: 4.  

Dette emne beskriver, hvordan du definerer tre nye fordelingsmålsomkostningsobjekter til fordelingskilden PROD-omkostningssted ved hjælp af det etablerede fordelingsforhold 5:2:4. De tre målomkostningsobjekter er ACCESSO, PAINT og FITTINGS.  

> [!NOTE]  
>  I eksemplet bruges demonstrationsdataene i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Sådan defineres fordelingskilden PROD-omkostningssted på oversigtspanelet Generelt  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordeling**, og vælg derefter det relaterede link.  
2.  På siden **Omkostningsfordeling** skal du vælge handlingen **Ny**.  
3.  I feltet **Id** skal du trykke på Enter eller indtaste et id.  
4.  Angiv **1** i feltet **Niveau**.  
5.  I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.  
6.  I feltet **Omkostningsstedskode** skal du angive **PROD**.  
7.  Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Sådan angives fordelingsmålsomkostningsobjekter på oversigtspanelet Linjer  

1.  Angiv **9903** i feltet **Målomkostningstype** på den første linje.  
2.  Vælg **TILBEHØR** i feltet **Målomkostningstype** på den første linje.  
3.  På den første linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
4.  På den første linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
5.  På den første linje i feltet **Fordeling** skal du angive fordelingsforholdet **5**.  
6.  Angiv **9903** i feltet **Målomkostningstype** på den anden linje.  
7.  Vælg **MALING** i feltet **Målomkostningsemne** på den anden linje.  
8.  På den anden linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
9. På den anden linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
10. På den anden linje i feltet **Fordeling** skal du angive fordelingsforholdet **2**.  
11. Angiv **9903** i feltet **Målomkostningstype** på den tredje linje.  
12. Vælg **BESLAG** i feltet **Målomkostningsemne** på den første linje.  
13. På den tredje linje i feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle påløbne omkostninger allokeres.  
14. På den tredje linje i feltet **Basis** skal du vælge **Statisk** for at bruge den statiske allokeringsmetode.  
15. På den tredje linje i feltet **Fordeling** skal du angive fordelingsforholdet **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk feltet **Procent** ved hjælp af en procentsats , der er afhængig af alle tre fordelingsforhold, der er angivet i feltet **Fordeling** for alle tre linjer.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Scenarie 2: Definition af dynamiske fordelinger baseret på solgte varer
I dette emne vises et eksempel på, hvordan du definerer allokeringer ved hjælp af metoden til dynamisk fordeling. I dette eksempel skal du ændre dynamisk fordeling af omkostningerne for omkostningsstedet SALES til understøttelse af det nye omkostningsobjekt IT-UDSTYR. IT_UDSTYR-pakker har varenumre i området fra 8904-W til 8924-W. Du bruger salgstal for det foregående år til at beregne det andelen. Allokeringen bogføres til hjælpeomkostningstypen 9903.  

> [!NOTE]  
>  I eksemplet bruges demonstrationsdataene i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Sådan defineres dynamiske fordelinger baseret på varer, der er solgt i det foregående år  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Omkostningsfordelinger**, og vælg derefter det relaterede link.  
2.  På siden **Omkostningsfordeling** skal du vælge handlingen **Ny**.  
3.  I feltet **Id** skal du trykke på Enter eller indtaste et id.  
4.  Angiv **1** i feltet **Niveau**.  
5.  I felterne **Gyldig fra** og **Gyldig til** skal du angive relevante datoer.  
6.  I feltet **Omkostningsstedskode** skal du angive **SALG**.  
7.  Angiv omkostningstypen **9903** i feltet **Kredit til omkostningstype**.  
8.  Angiv omkostningstypen **9903** i feltet **Målomkostningstype**.  
9. I feltet **Målomkostningstype** skal du vælge **Ny** for at oprette et nyt omkostningsobjekt IT-UDSTYR og udfylde felter efter behov. Vælg **IT-UDSTYR**. Lad feltet **Målomkostningssted** stå tomt.  
10. I feltet **Fordelingsmåltype** skal du vælge **Alle omkostninger** for at definere, hvordan alle akkumulerede omkostninger allokeres.  
11. I feltet **Basis** skal du vælge fordelingsbasen **Varer solgt (beløb)**.  
12. I feltet **Nummerfilter** skal du angive **8904-W..8924-W**.  
13. I feltet **Datofilterkode** skal du angive **Sidste år**.  
14. Vælg handlingen **Beregn fordelingsnøgle** for at beregne det andelen.  

> [!IMPORTANT]  
>  [!INCLUDE[prod_short](includes/prod_short.md)] bruger salgstal fra de foregående år til at beregne andelen af 1596,50 RV med 100 procent for IT-UDSTYR-pakkerne. Det betyder, at alle varer, der er solgt sidste år, tildeles omkostningsobjektet IT-UDSTYR.

## <a name="see-also"></a>Se også  
 [Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)   
 [Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)   
 [Terminologi i omkostningsregnskab](finance-terminology-in-cost-accounting.md)   
 [Om omkostningsregnskab](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]