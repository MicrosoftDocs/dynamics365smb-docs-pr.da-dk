---
title: Konfigurere omkostningsregnskab | Microsoft Docs
description: Før du begynder at arbejde med omkostningsregnskab, skal du udføre opsætningsopgaver.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 808efe140a0330d9892c01839090b28ef2c0d50c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783743"
---
# <a name="setting-up-cost-accounting"></a>Konfigurere omkostningsregnskab
Før du begynder at arbejde med omkostningsregnskab, skal du udføre opsætningsopgaver.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Saldi mellem omkostningstype, omkostningssted og omkostningsobjekt
Når du konfigurerer omkostningsregnskab, skal du sørge for, at alle poster er tildelt til en pristype samt et omkostningssted eller et omkostningsobjekt. Det betyder, at hver omkostningspost skal have pristype samt en omkostningsstedskode eller et omkostningsobjekt tildelt. Denne regel sikrer, at hver omkostningspost vises i enten omkostningssteder eller omkostningsobjekter, men aldrig begge steder.  

På denne måde kan du oprette følgende regnskabsmæssige ligning:  

*Pristypesaldo* = *Omkostningsstedsaldo* + *Omkostningsobjektsaldo*  

Når du udskriver diagrammet over pristyper, diagrammet over omkostningssteder og diagrammet over omkostningsobjekter, kan du analysere denne relation.

## <a name="setting-up-cost-types"></a>Konfigurere Omkostningstyper
Diagrammet over omkostningstyper ligner kontoplanen i finansregnskabet. Du kan angive diagrammet over omkostningstyper på følgende måder:  

-   Strukturen af diagrammet over omkostningstyper ligner resultatopgørelseskontiene i finanskontoplanen. Herefter kan du overføre finanskontoplanen til diagrammet over omkostningstyper. Du kan foretage de nødvendige justeringer efter overførslen.  
-   Opret et nyt diagram over omkostningstyper, eller tilføj nye omkostningstyper til det eksisterende diagram over omkostningstyper. Du skal oprette hver ny omkostningstype individuelt.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Sådan overføres finanskontoplanen til diagrammet over omkostningstyper  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Diagram over omkostningstyper**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Hent omkostningstyper fra kontoplan**. I dialogboksen skal du trykke på knappen **Ja** for at bekræfte overførslen. Funktionen bruger kontoplanen til at oprette et diagram over omkostningstyper  

    Diagrammet over omkostningstyper indeholder nu alle resultatopgørelseskonti i regnskabet og omfatter overskrifter og subtotaler. Du kan ændre diagrammet over omkostningstyper, hvis det er nødvendigt. For eksempel kan du slette dobbelte omkostningstyper.  

    > [!IMPORTANT]  
    >  Funktionen **Registrer omkostningstyper i kontoplanen** opdaterer forholdet mellem kontoplanen og diagrammet over omkostningstyper. Feltet **Nummer** feltet udfyldes og bekræftes for at sikre, at hver finanskonto kun er relateret til én kostpristype. Funktionen kører automatisk, før den overfører finansposter til omkostningsregnskabet.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>Sådan oprettes nye omkostningstyper på siden Omkostningstyper  
1.  Åbn siden **Omkostningstyper** i redigeringstilstand.  
2.  Udfyld felterne som beskrevet efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan oprette og vedligeholde omkostningstyper enten på siden **Omkostningstypekort** eller på siden **Omkostningstyper**. I denne procedure opretter du omkostningstyper på siden **Omkostningstyper**.

3.  Når du har oprettet alle omkostningstyper, skal du vælge handlingen **Indryk omkostningstyper**. I dialogboksen skal du trykke på knappen **Ja**.  
4.  Sammenkæd den nye pristype til den tilsvarende finanskonto.  

    > [!IMPORTANT]  
    >  Hvis du har angivet definitioner i felterne **Sammentælling** for linjetypen **Til-sum**, før du kører funktionen **Indryk omkostningstyper**, skal du angive definitionerne igen, fordi funktionen overskriver værdierne i alle felter af typen **Til-sum**.  

### <a name="to-update-cost-types"></a>Sådan opdateres omkostningstyper  
1.  På siden **Konfiguration af omkostningsregnskab** skal du vælge, om du ønsker, at omkostningstypeplanen automatisk opdateres, når kontoplanen ændres.  
2.  Du kan vælge mellem følgende indstillinger i feltet **Opdater finanskonto**.  

- **Ingen justering** der er ingen tilsvarende ændring i diagrammet over omkostningstyper, når du ændrer kontoplanen.  
- **Automatisk** - en tilsvarende ændring foretages i diagrammet over omkostningstyper, når du ændrer kontoplanen.  
- **Spørg** - der vises en meddelelse, hvor du bliver spurgt, om du vil foretage en tilsvarende ændring i diagrammet typer omkostninger, når du ændrer kontoplanen.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definition af forholdet mellem omkostningstyper og finanskonti.
Forholdet mellem pristype og finanskontoen oprettes i pristypen og finanskontoen.  

* Feltet **Finanskontointerval** i tabellen **Omkostningstype** fastlægger, hvilke finanskonti der hører til en pristype.  
* Feltet **Omkostningstypenr.** i kontoplanen fastlægger, hvilken pristype en finanskonto tilhører.  

Disse to felter udfyldes automatisk, når du bruger funktionen **Få omkostningstyper fra kontoplanen**.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Forholdet mellem finanskonti og pristyper  
Der er et n:1 forhold mellem finanskonti og pristyper. Flere finanskonti kan tilhøre én pristype, men hver finanskonto tilhører kun én pristype. Følgende tabel beskriver detaljerne om relationen.  

|Relationer|**Finanskontointerval**|**Omkostningstypenr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|En finanskonto for hver pristype|Én finanskonto|En pristype|  
|Flere finanskonti for en pristype|Finanskontointerval, f.eks. 7110..7193, for finanskonto|For hver finanskonto i området er det kun én pristype|  
|Pristyper uden tilsvarende finanskonti|<Empty>||  
|Finanskonti, hvis poster ikke bliver overført||<Empty>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Pristyper uden relation til finanskontoen  
En pristype kan ikke have en relation til finanskonti, hvis en af følgende betingelser er opfyldt:  

* Konti til operationelt regnskab, f.eks, Beregn Renter og afskrivning, henter kun omkostninger fra operationelt regnskab.  
* Hjælpeomkostningstyper, f.eks. 9901, 9902 og 9903 i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen, bruges som kredit- og debetkonti for tildelinger.  
* Hjælpekontoen, 9920 i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen, indeholder faktiske periodiseringer, der viser forskellen mellem omkostningerne og udgifterne fra finansregnskabet.

## <a name="setting-up-cost-centers"></a>Konfigurere Omkostningssteder
Omkostningssteder er afdelinger, der er ansvarlige for omkostninger og indtægter. Diagrammet over omkostningssteder er lig dimensionsoplysningerne for regnskabet. Du kan angive diagrammet over omkostningssteder på følgende måder:  

-   Overfør dimensionsværdier i regnskabet til diagrammet over omkostningssteder. Du kan foretage de nødvendige justeringer efter overførslen.  
-   Opret et nyt diagram over omkostningssteder, der er uafhængigt af regnskabet, eller tilføj et nyt omkostningssted til et eksisterende diagram over omkostningssteder. Du skal oprette hvert omkostningssted individuelt.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>Sådan overføres dimensionsværdier i regnskabet til diagrammet over omkostningssteder.  
1.  Angiv en dimension, der skal være omkostningsstedsdimensionen på siden **Opdater CA-dimensioner**. Kun værdierne fra denne dimension overføres.  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Diagram over omkostningssteder**, og vælg derefter det relaterede link.  
3.  På fanen **Handlinger** i gruppen **Funktioner** skal du vælge **Hent omkostningssteder fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningssteder. Funktionen overfører de dimensionsværdier, som du definerede i trin 1.  

    > [!NOTE]  
    >  Du kan indstille feltet **Opdater omkostningsstedsdimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningssteder. Du kan ikke definere en synkronisering af diagrammet over omkostningssteder fra regnskabet.  

Diagrammet over omkostningssteder indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>Sådan oprettes nye omkostningssteder på siden Diagram over omkostningssteder  
Du kan oprette og vedligeholde omkostningssteder enten på kortet **Omkostningsstedskort** eller på siden **Diagram over omkostningssteder**. I denne procedure opretter du omkostningssteder på siden **Diagram over omkostningssteder**.  

1. Åbn siden **Diagram over omkostningssteder** i redigeringstilstand.  
2. I feltet **Kode** angives omkostningsstedets kode. Alle omkostningssteder skal have en kode.  
3. I feltet **Navn** angives omkostningsstedets navn.  
4. Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsstedet.  

    - For omkostningssteder af typen **I alt** skal du udfylde feltet **Sammentælling**. Brug operatoren **eller**, som er en lodret linje (**&#124;**) til at angive områder for omkostningssteder.  
    - For omkostningssteder af typen **Til-sum** udfyldes dette felt automatisk, når du bruger indrykningsfunktion.  
5.  Udfyld felterne **Sorteringsrækkefølge** og **Omkostningsundertype**.  
6.  Vælg den næste tomme linje for at oprette et nyt omkostningssteder, og gentag derefter trin 2 til 5.  
7.  Når du har oprettet alle omkostningssteder, kan du vælge handlingen **Indryk omkostningssteder**. Vælg knappen **Ja**.  

> [!IMPORTANT]  
>  Hvis du har angivet definitioner i felterne **Sammentælling** for **Til-sum**-omkostningssteder, før du kører indrykningsfunktionen, skal du angive dem igen. Funktionen overskriver værdierne i alle **Til-sum**-felter.

## <a name="setting-up-cost-objects"></a>Konfigurere Omkostningsemner
Omkostningsobjekter er en virksomheds projekter, produkter eller tjenester. Diagrammet over omkostningsobjekter er lig dimensionsoplysningerne for regnskabet. Du kan angive diagrammet over omkostningsobjekter på følgende måder:  

* Overfør dimensionsværdier i regnskabet til diagrammet over omkostningsobjekter. Du kan foretage de nødvendige justeringer efter overførslen.  
* Opret et nyt diagram over omkostningsobjekter, der er uafhængigt af regnskabet, eller tilføje et nyt omkostningsobjekt til et eksisterende diagram over omkostningsobjekter. Du skal oprette hvert omkostningsobjekt individuelt.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>Sådan overføres dimensionsværdier fra regnskabet til diagrammet over omkostningsobjekter.  
1.  Angiv en dimension, der skal være omkostningsobjektdimensionen på siden **Opdater CA-dimensioner**. Kun værdierne fra denne dimension overføres.  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Diagram over omkostningsemner**, og vælg derefter det relaterede link.  
3.  Vælg handlingen **Hent omkostningsemner fra dimensionen** for at overføre dimensionsværdier til diagrammet over omkostningsemner. Funktionen overfører de dimensionsværdier, som du definerede i trin 1.  

    > [!NOTE]  
    >  Du kan indstille feltet **Opdater omkostningsemnedimension** til at definere en envejssynkronisering af dimensionsværdier fra regnskabet til diagrammet over omkostningsemner. Du kan ikke definere en synkronisering af diagrammet over omkostningsobjekter fra regnskabet.  

Diagrammet over omkostningsobjekter indeholder alle de angivne dimensionsværdier fra regnskabet og indeholder titler og subtotaler.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>Sådan oprettes nye omkostningsemner på siden Diagram over omkostningsemner  
Du kan oprette og vedligeholde omkostningsemner enten på **Omkostningsemnekortet** eller på siden **Diagram over omkostningsemner**. I denne procedure opretter du omkostningsobjekter på siden **Diagram over omkostningsemner**.  

1.  Åbn siden **Diagram over omkostningsemner** i redigeringstilstand.  
2.  I feltet **Kode** angives omkostningsemnets kode. Alle omkostningsobjekter skal have en kode.  
3.  I feltet **Navn** angives omkostningsemnets navn.  
4.  Vælg rullepilen i feltet **Linjetype** for at angive formålet med omkostningsemnet.  

    * For omkostningsemner af linjetypen **I alt** skal du udfylde feltet **I alt fra/til**. Brug operatoren **eller**, som er en lodret linje (**&#124;**), til at angive områder for omkostningsemner.  
    * For omkostningsobjekter af typen **Til-sum** udfyldes dette felt automatisk, når du bruger indrykningsfunktion.  
5.  Udfyld feltet **Sorteringsrækkefølge**.  
6.  Vælger den næste tomme linje for at oprette et nyt omkostningsobjekt, og gentag derefter trin 2 til 5.  
7.  Når du har oprettet alle omkostningsemner, kan du vælge handlingen **Indryk omkostningsemner**. Vælg knappen **Ja**.  

> [!IMPORTANT]  
>  Hvis du har angivet definitioner i felterne **I alt fra/til** for **Til-sum**-omkostningsemner, før du kører indrykningsfunktionen, skal du angive dem igen. Funktionen overskriver værdierne i alle **Til-sum**-felter.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definition af omkostningssteder og omkostningsobjekter for kontoplanen
Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører [!INCLUDE[prod_short](includes/prod_short.md)] kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definere standarddimensionsværdier for finanskonti  
For hver enkelt finanskonto kan du definere standarddimensionsværdier i tabellen **Standarddimension**. Følgende eksempel viser, hvordan du definerer, at der altid skal være et omkostningssted DEPARTMENT, men aldrig et omkostningsobjekt PROJECT, når du bogfører til en finanskonto.  

|**Dimensionskode**|**Værdibogføring**|  
|------------------------------------------|-----------------------------------------|  
|Afdeling|Tvungen kode|  
|Projekt|Ingen kode|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definition af dimensionsværdier for faste og direkte omkostninger  
 Du kan overføre faste omkostninger til et omkostningssted og direkte omkostninger til et omkostningsobjekt. Følgende tabel viser den optimale kombination af dimensionsopsætningsværdierne.  

|Kopiér til|Omkostningsstedbogføring|Omkostningsobjektbogføring|  
|-----------------|-------------------------|-------------------------|  
|Omkostningssted|Tvungen kode|Ingen kode|  
|Omkostningsobjekt|Ingen kode|Tvungen kode|  

> [!NOTE]  
>  For at sikre, at det foruddefinerede omkostningssted og omkostningsemne, du har oprettet i regnskabet, automatisk overføres til omkostningsregnskab, skal du markere afkrydsningsfeltet **Kontroller finansbogføringer** på siden Konfiguration af omkostningsregnskab.

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md)   
[Definere og allokere omkostninger](finance-define-and-allocate-costs.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]