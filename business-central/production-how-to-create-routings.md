---
title: Sådan oprettes ruter | Microsoft Docs
description: En rute indeholder stamdata, som beskriver procesbehovene for en bestemt fremstillet vare. Så snart der oprettes en produktionsordre for den overordnede vare, bestemmer dens rute planlægningen af handlinger, som repræsenteret på siden **Prod.ordrerute** under produktionsordren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: aa03051a02309944c66d3fdf89de12627af8c4bf
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314092"
---
# <a name="create-routings"></a>Oprette ruter
Produktionsvirksomheder bruger ruter til at visualisere og styre produktionsprocessen.

Ruten danner også grundlag for procesplanlægning, kapacitetsplaner, planlagt tildeling af materialebehov og produktionsdokumenter.  

Hvad angår produktionsstyklister, tildeles ruterne til slutvaren fra produktionen. En rute indeholder stamdata, som beskriver procesbehovene for en bestemt fremstillet vare. Så snart der oprettes en produktionsordre for den overordnede vare, bestemmer dens rute planlægningen af handlinger, som repræsenteret på siden **Prod.ordrerute** under produktionsordren.  

Før du kan oprette en rute, skal følgende betingelser være opfyldt:  

- Der er oprettet varekort for overordnede varer, der indgår i produktionen. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).
- Produktionsressourcer er oprettet. Du kan finde flere oplysninger i [Konfigurere arbejdscentre og produktionsressourcer](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Sådan oprettes en rute  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Vælg **Seriel** i feltet **Type** for at beregne produktionsruten i henhold til værdien i feltet **Operationsnr.**. .   
    Vælg **parallelle** for at beregne transaktioner i henhold til værdien i det feltet **Næste operationsnr.**. .  
5.  Du kan redigere ruten ved at angive feltet **Status** til **Ny** eller **Under udvikling**. Du kan aktivere den ved at angive feltet **Status** til **Certificeret**.  

    Fortsæt med udfyldning af rutelinjerne.
6.  I feltet **Operationsnr.** skal du skrive nummeret på den første operation, f.eks. **10**.  
7.  I feltet **Type** skal du angive, hvilken ressourcetype er anvendes, f.eks. **Arbejdscenter**.  
8.  I feltet **Nummer** skal du vælge den ressource, der skal bruges, eller skrive den i feltet.  
9.  I feltet **Rutebindingskode** skal du skrive en kode for at knytte komponenten til en bestemt operation. Du kan finde flere oplysninger i [Sådan oprettes rutebindinger](production-how-to-create-routings.md#to-create-routing-links).
10.  Angiv de procestider, der kræves for at fuldføre operationen, i felterne **Operationstid** og **Opstillingstid**.

    > [!NOTE]
    > Opstillingstiden beregnes pr. produktionsordre, hvorimod operationstiden beregnes pr. produceret vare.  

11.  Angiv i feltet **Samtidige kapaciteter**, hvor mange enheder af den valgte ressource, der bruges til at udføre handlingen. F.eks. vil to personer til en pakkehandling vil halvere kørselstiden.  
12.  Fortsæt med at udfylde linjer for alle de operationer, der kræves for at producere den pågældende vare.  
13.  Du kan kopiere linjer fra en eksisterende rute ved at vælge handlingen **Kopier rute** for at vælge eksisterende linjer.  
14. Godkend ruten.  
15. Du kan nu knytte den nye rute til kortet for den pågældende produktionsvare ved at udfylde feltet **Rutenr.**. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Husk også at genberegne varens standardkostpris fra kortet **Vare**: Vælg handlingen **Produktion**, vælg handlingen **Beregn standardkostpris**, og vælg derefter handlingen **Alle niveauer**.  

## <a name="to-create-routing-links"></a>Sådan oprettes rutebindinger
Du kan oprette rutebindinger til at knytte komponenter til bestemte operationer for at bevare deres relationer, selvom produktionsstyklisterne eller ruterne ændres. De letter også yderligere just in time-træk af komponenter på det tidspunkt, hvor den angivne bundne operation starter, og ikke når hele produktionsordren frigives. Du kan finde flere oplysninger i [Udtrække komponenter i henhold til operationsafgang](production-how-to-flush-components-according-to-operation-output.md).  

En anden vigtig fordel er, at bundne komponenter og operationer vises i en logisk processtruktur, når siden **Produktionskladde** bruges til bogføring af afgang og forbrug.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.  
2.  Åbn ruten, der indeholder de handlinger, som du vil tilknytte.  

    Kontroller, at rutens status er **Under udvikling**.  

3.  Vælg en kode på den relevante rutelinje i feltet **Rutebindingskode**.  
4.  Fortsæt efter behov med at tilføje forskellige rutebindingskoder til andre operationer på ruten.  

    > [!NOTE]  
    >  Du bør ikke bruge den samme rutebindingskode i forskellige operationer på en rute, da du kan komme til at binde en komponent til to forskellige operationer og derved forbruge den to gange.  
    >   
    >  Det anbefales at opkalde rutebindingskoden efter operationen for at sikre operationsspecifikke rutebindinger.

5.  Angiv rutestatussen til **Godkendt**.  

    Rutebindingskoder er nu knyttet til operationer. Derefter skal du oprette det faktiske hyperlink ved at knytte de samme koder til bestemte komponenter i den relevante produktionsstykliste.  

6.  Åbn **produktionsstyklisten**, som indeholder de komponenter, som du vil forbinde med ovennævnte handlinger. Du kan finde flere oplysninger i [Oprette produktionsstyklister](production-how-to-create-production-boms.md).
7.  Kontrollér, at styklistestatus er **Under udvikling**.  
8.  Vælg den kode, du lige har tildelt til den relevante operation feltet **Rutebindingskode** på den pågældende produktionsstyklistelinje.  
9. Fortsæt med at føje rutebindingskoder til andre komponenter i overensstemmelse med de entydige operationer, de bruges i forbindelse med.  
10. Angiv produktsstyklistestatus til **Godkendt**.  

    > [!NOTE]  
    >  For at aktivere rutebindingerne på en eksisterende produktionsordre skal du først forny produktionsordren. Du kan finde flere oplysninger i [Oprette produktionsordrer](production-how-to-create-production-orders.md).  

De valgte komponenter knyttes nu til de valgte operationer, når du opretter eller opdaterer en produktionsordre ved hjælp af den pågældende produktionsstykliste og rute. Dette er synligt på siden **Prod.ordrekomponenter** under produktionsordren, og her kan du også når som helst fjerne og definerede rutebindingskoder.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Sådan tildeles personale, værktøj og kvalitetsmål for ruteoperationer.
Hvis du skal bruge personer med særlige kvalifikationer, specialviden eller særlige tilladelser til en operation, kan du knytte dem til operationen her. Du kan også tildele værktøjer og kvalitetskrav til operationen. Denne procedure beskriver, hvordan du tildeler medarbejdere. Trinene er de samme for andre typer operationsoplysninger.

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.  
2.  Åbn den relevante rute.  
3.  På oversigtspanelet **Linjer** skal du markere den linje, du vil behandle, og derefter vælge handlingen **Medarbejdere**.  
4.  Udfyld felterne på siden **Rute - Mandskab**.  
5.  Vælg knappen **OK** for at afslutte siden. De angivne værdier kopieres og knyttes til operationen.    

## <a name="to-create-a-new-versions-of-a-routing"></a>Sådan oprettes en ny version af ruter  
Versionsprincippet gør det muligt for dig at styre flere versioner af en rute. Ruteversionens struktur svarer til rutens struktur, og den består af ruteversionshovedet og -linjerne. Den egentlige forskel består i startdatoen.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Ruter**, og vælg derefter det relaterede link.  
2.  Vælg den rute, der skal kopieres, og vælg derefter handlingen **Versioner**.  
3. På siden **Ruteversioner** skal du vælge handlingen **Ny**.
4. Udfyld felterne efter behov.
5.  I feltet **Versionskode** skal du angive en entydig identifikation af versionen. Alle kombinationer af tal og bogstaver er tilladt.  

    Den nyoprettede version tildeles automatisk status som **Ny**.  
6.  Vælg den første tomme linje for at oprette operationslinjer, og udfyld derefter feltet **Operationsnr.** i overensstemmelse med rækkefølgen af operationer.

    Operationslinjerne sorteres i stigende rækkefølge efter operationsnummer. Gør plads, så du kan tilføje ændringer senere. Feltet **Næste operationsnr.** henviser til den efterfølgende operation. Antallet af operationer kan angives direkte.

7. Når ruteversionen er udført, angiver du feltet **Status** til **Certificeret**.

Gyldigheden i tid for versionen angives i feltet **Startdato**.  

## <a name="see-also"></a>Se også  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
