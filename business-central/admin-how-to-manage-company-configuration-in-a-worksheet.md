---
title: "Sådan administreres virksomhedskonfigurationen i et regneark | Microsoft Docs"
description: "Konfigurationsregnearket er en central placering, hvor du kan planlægge, spore og udføre konfigurationsarbejdet. Du kan oprette et regneark for hver virksomhed, du arbejder med, eller oprette et standardkonfigurationsregneark, der kan bruges til at konfigurere flere identiske virksomheder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d52c54b18ccb7794f7556919e20b23df65c95acd
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="manage-company-configuration-in-a-worksheet"></a>Administrere virksomhedskonfigurationen i et regneark
Konfigurationsregnearket er en central placering, hvor du kan planlægge, spore og udføre konfigurationsarbejdet. Du kan oprette et regneark for hver virksomhed, du arbejder med, eller oprette et standardkonfigurationsregneark, der kan bruges til at konfigurere flere identiske virksomheder.  

Det første trin i at udarbejde en konfigurationspakke er at vælge en virksomhed, du allerede har oprettet og ændret, så den passer til de fleste af dine løsningsbehov. Denne virksomhed tjener som udgangspunkt for konfiguration af arbejde på nye selskaber. I regnearket skal du angive de tabeller, du ønsker, at din konfiguration skal styre og håndtere. Da de fleste tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] har relationer og afhængigheder af andre tabeller, skal du også medtage disse relaterede tabeller efter behov. Sammen fungerer disse tabeller som den struktur, du opbygger en ny virksomhed omkring. Efterfølgende trin kan hjælpe dig med at pakke og derefter installere din konfiguration.  

Som en hjælp til at registrere og gennemse dit arbejde skal du bruge faktaboksen **Konfig.pakketabel** til at se oplysninger om poster. Brug faktaboksen **Konfig. relateret tabel** til at overvåge tabelrelationer.  

Følgende procedurer viser, hvordan du tilføjer og tilpasser tabeloplysninger for din konfiguration.  

## <a name="to-open-the-configuration-worksheet"></a>Åbne konfigurationsregnearket  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du åbne den virksomhed, der er udgangspunkt for konfigurationen og derefter åbne dens rollecenter for RapidStart Services-implementering.  
2.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationskladde**, og vælg derefter det relaterede link.  

## <a name="to-add-a-table-to-the-worksheet"></a>Føje en tabel til regnearket  
1.  I vinduet **Konfig.kladde** skal du vælge handlingen **Rediger liste**.  
2.  På den første linje i feltet **Linjetype** skal du vælge **Tabel**.  
4.  Vælg den tabel, du vil føje til din konfiguration, i feltet **Tabel-id**.  
5.  Angiv id'et for den side, der er knyttet til tabellen, i feltet **Side-id**. For standardtabeller angives værdien automatisk. For brugerdefinerede tabeller skal du angive id'et.
6.  I feltet **Reference** skal du angive en URL-adresse på en dokumentationsside, f.eks. i Hjælp, der indeholder oplysninger om bedste praksis eller instruktioner i, hvordan du skal konfigurere tabellen.  
7.  Hvis du vil tilføje relaterede tabeller, skal du vælge handlingen **Hent relaterede tabeller**.  

    > [!NOTE]  
    > Relaterede tabeller bliver ikke tilføjet med handlingen **Hent relaterede tabeller**, hvis en af følgende er sandt:
    > - Relationen er betinget.  
    > Eksempel: Hvis du henter relaterede tabeller for tabellen **Debitor**, så vil tabellen **Lokation** ikke blive tilføjet, da den kun er betinget relateret til tabellen **Debitor**, nemlig hvis feltet **Lokationskode** i tabellen **Debitor** er udfyldt.  
    > - Den relaterede tabel er filtreret.  
    > Eksempel: Et felt i den relaterede tabel indeholder en WHERE-sætning. Årsagen til dette er, at de involverede relaterede oplysninger er gemt i systemtabellen **Felt**, der ikke er fuldt tilgængelig for anvendelsen.  
    > Du skal tilføje sådanne typer af tabeller manuelt ved at følge trin 4 i denne procedure.  

8.  Hvis du vil redigere den resulterende liste over tabeller, skal du markere en tabel, du vil fjerne, og derefter vælge handlingen **Slet**.  
9. Gentag trinnene for hver tabel, som du ønsker at føje til konfigurationen.  
10. Du kan fjerne dublerede tabeloplysninger, som kan være resultatet af handlingen **Hent relaterede tabeller** ved at vælge handlingen **Slet dubletlinjer**. Dette vil fjerne dublerede tabeller, der har den samme kode til pakken.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Tilføje flere tabeller til konfigurationsregnearket  
1. Vælg handlingen **Hent tabeller**. Kørselsvinduet **Hent konfig.tabeller** åbnes.  
2. I oversigtspanelet **Indstillinger** skal du angive typerne af tabeller, som du vil føje til konfigurationen, som beskrevet i følgende tabel.

    |Indstilling|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Medtag kun med data**|Markér afkrydsningsfeltet for kun at medtage de tabeller, der indeholder data. F.eks. vil du måske medtage en tabel, der definerer de typiske betalingsbetingelser, som din løsning understøtter.|  
    |**Medtag relaterede tabeller**|Markér afkrydsningsfeltet for at medtage alle relaterede tabeller. Se trin 3 i denne procedure for at tilføje et undersæt af relaterede tabeller.|  
    |**Medtag dimensionstabeller**|Markér afkrydsningsfeltet for at medtage dimensionstabeller.|  
    |**Medtag kun licenserede tabeller**|Markér afkrydsningsfeltet for kun at medtage de tabeller, som den licens, som du opretter regnearket under, giver dig adgang til.|

3. I oversigtspanelet **Objekt** kan du efter behov angive filtre for at angive de tabeltyper, du vil medtage eller udelade.  
4. Vælg knappen **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller føjes til kladden. Hver post på listen har en linje af typen **Tabel**.  
5. Du kan fjerne dublerede tabeloplysninger, som kan være resultatet af handlingen **Hent tabeller** ved at vælge handlingen **Slet dubletlinjer**. Dette vil fjerne dublerede tabeller, der har den samme kode til pakken.  
6. Du kan føje tabeller til det regneark, der er relateret til en tabel, du har valgt. Gennemgå oplysningerne i faktaboksen **Relaterede tabeller** for at se, om der mangler tabeller. Hvis du vil føje relaterede tabeller til en bestemt tabel, skal du markere tabellen på listen og derefter vælge handlingen **Hent relaterede tabeller**.  

    > [!NOTE]  
    > Relaterede tabeller bliver ikke tilføjet med handlingen **Hent relaterede tabeller**, hvis en af følgende er sandt:
    > - Relationen er betinget.  
    > Eksempel: Hvis du henter relaterede tabeller for tabellen **Debitor**, så vil tabellen **Lokation** ikke blive tilføjet, da den kun er betinget relateret til tabellen **Debitor**, nemlig hvis feltet **Lokationskode** i tabellen **Debitor** er udfyldt.  
    > - Den relaterede tabel er filtreret.  
    > Eksempel: Et felt i den relaterede tabel indeholder en WHERE-sætning. Årsagen til dette er, at de involverede relationsoplysninger er gemt i den virtuelle **Felt**-tabel og ikke er tilgængelig i vinduer som konfigurationsregnearket af hensyn til ydeevnen.  
    > Du skal tilføje relaterede tabeller med sådanne komplekse relationer manuelt ved at følge trin 4 i afsnittet "Føje en tabel til regnearket".

7. Hvis du vil slette tabeller i den resulterende liste over tabeller, skal du markere en tabel, du vil fjerne, og derefter vælge handlingen **Slet**.  

Brug den næste procedure til at angive, hvilke tabelfelter der skal medtages. Når du har foretaget denne specifikation, kan du eksportere tabellen til Excel og bruge tabelstrukturen som en skabelon for indsamling af debitordata. Du kan finde flere oplysninger i [Forberede overflytning af debitordata](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Angive et sæt felter og poster for en konfigurationstabel  
1. Vælg en tabel på listen over konfigurationstabeller, og vælg derefter handlingen **Rediger liste**.  
2. Vælg en tabel, som du vil angive feltoplysninger for, og vælg derefter handlingen **Felter**.  
3. For kun at vælge de felter du vil medtage, skal du vælge handlingen **Ryd inkluderede**. Hvis du vil tilføje alle felter, skal du vælge handlingen **Angiv inkluderede**.  
4. Hvis du vil angive, at feltdata ikke skal valideres, skal du fjerne markeringen af afkrydsningsfeltet **Valider felt** for feltet.  
5. Vælg knappen **OK**.  
6. For at filtrere efter et bestemt sæt poster, der skal medtages i konfigurationsarket, skal du vælge handlingen **Filtre** og derefter angive de ønskede filterværdier.

Du kan oprette funktionalitetsområder og tabelgrupper i regnearket for at sammensætte tilsvarende funktionalitet. F.eks. kan du i konfiguration af kontoplanen for din konfiguration beslutte at oprette en tabelgruppe af bogføringstabeller. Områder bruges typisk til at gruppere et sæt tabeller, der svarer til et funktionsområde. Hvert område kan indeholde grupper. En gruppe kan bruges til at arrangere tabeller, der sammen har en fælles betydning.  

Følgende procedure beskriver, hvordan du tilføjer område- og gruppebetegnelser, når du har oprettet den første liste over tabeller. Når du har tilføjet disse kategorier, kan du fortsætte med at tilføje og redigere din liste over tabeller.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Kategorisere og gruppere funktionalitet i regnearket  
1. I begyndelsen af et område skal du indsættes en ny linje i regnearket.  
2. I feltet **Linjetype** skal du vælge **Område**. Indtast et navn til området i feltet **Navn**.  
3. I begyndelsen af en tabelgruppering skal du indsætte en ny linje i regnearket.  
4. I feltet **Linjetype** skal du vælge **Gruppe**. Indtast et navn til området i feltet **Navn**. Gruppenavnet indrykkes automatisk.  
5. Hvis du vil flytte tabeller til den relevante kategori, skal du vælge handlingen **Flyt op** eller **Flyt ned**. Du kan også slette en kladdelinje og indsætte tabellen igen på den krævede placering.  

Nogle [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller, der er standard, og dataene i dem vil sandsynligvis ikke blive ændret fra implementering til implementering. Som en følge deraf kan du for at hjælpe din kunde fjerne disse tabeller fra regnearket, efter du har inkluderet dem i konfigurationspakken. Så snart tabellerne er tilføjet, forbliver de en del af konfigurationspakken.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Fjerne en standardtabel i regnearket  
Når du har føjet alle de nødvendige tabeller til en konfigurationspakke, kan du bestemme, hvilke tabeller der ikke kræver kundens opmærksomhed.  
1.  Vælg tabellerne, og slet dem derefter ved at vælge handlingen **Slet**.  

    > [!NOTE]  
    >  Tabellerne forbliver i pakken, selvom de slettes fra regnearket.  

## <a name="see-also"></a>Se også  
[Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

