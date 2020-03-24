---
title: Overføre debitordata | Microsoft Docs
description: Du kan overflytte eksisterende debitordata fra et eksisterende ERP-system til Business Central ved hjælp af RapidStart Services. Du kan bruge Excel .xlsx-filer som datamedie. Du kan også manuelt flytte data ved at indtaste dem direkte i virksomheden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/19/2019
ms.author: sgroespe
ms.openlocfilehash: 2da58a4f5a3655fc2153647d80c5d69e1356b503
ms.sourcegitcommit: 35552b250b37c97772129d1cb9fd9e2537c83824
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2020
ms.locfileid: "3097692"
---
# <a name="migrate-customer-data"></a>Overflytte debitordata
Du kan overflytte eksisterende debitordata fra et eksisterende ERP-system til [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af dataoverflytningsværktøjerne i RapidStart Services. Du kan bruge Excel-filer som datamedie. Du kan også manuelt flytte data ved at indtaste dem direkte i virksomheden.

> [!NOTE]
> Felter af typen Blob kan ikke eksporteres/importeres ved hjælp af Excel.

Siderne **Overflytningsoversigt** og **Konfig.kladde** giver adgang til funktioner og visninger til at udføre alle de opgaver, der er relateret med dataoverflytning. Vi anbefaler, at du overflytter én tabel ad gangen for at håndtere afhængigheder i dine data. Ved overflytning berører du også masterdatatabeller, der indeholder oplysninger om debitorer, kreditorer, varer, kontaktpersoner og regnskab.  

## <a name="to-import-configuration-packages"></a>Sådan importeres konfigurationspakker
Når du opretter et nyt virksomhed, kan du importere virksomhedsindstillinger for det nye virksomhed. Du indlæser indstillingerne fra en .rapidstart-fil, som leverer pakkens indhold i komprimeret format. Der importeres et tilsvarende sæt tabeller for standarddataoverflytning. Datasæt indeholder masterdatatabeller og opsætningsdatatabeller. Din første opgave i dataoverflytningen er at vurdere, om standardopsætning for overflytningen opfylder behovene i det nye virksomhed.

> [!NOTE]  
>  Du kan ikke omdøbe en fil, der ikke allerede er en RapidStart Services-konfigurationspakke, til en .rapidstart-konfigurationspakkefil og derefter forsøge at importere den. Hvis du prøver at gøre det, modtager du en fejlmeddelelse.  

Før du starter, skal du sikre dig, at du har tilladelse til at køre RapidStart Services-objekterne. Du kan f.eks. have rettighedssætterne SUPER eller D365 RAPIDSTART. Vi anbefaler også, at du er i et rollecenter med links til RapidStart Services, f.eks. rollecentret Administration. Du kan finde flere oplysninger under [Sådan ændres rollen](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> Ved eksport og import af konfigurationspakker mellem to virksomhedsdatabaser, skal databaserne har samme skema for at sikre, at alle data er blevet overført. Dette betyder, at databaserne skal have den samme tabel- og feltstruktur, hvor tabellerne har samme primære nøgler, og felter har samme id'er og datatyper.  
>
>  Du kan indlæse konfigurationspakker, der er eksporteret fra en database med et andet skema end måldatabasen. Men tabeller eller felter i konfigurationspakken, der mangler i måldatabasen, importeres ikke.
>
> Tabeller, der har forskellige primære nøgler, og felter, der har forskellige datatyper, vil heller ikke blive importeret korrekt. Hvis konfigurationspakken indeholder tabellen **50000 Customer**, hvor primærnøgle **Code20**, og databasen, som du importerer pakken til, indeholder tabellen **50000 debitorbankkonto**, der har primærnøglen **Code20 + kode 20**, importeres data ikke.  

1. Åbn den nye virksomhed.  
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Indlæs pakke**. Gå til den .rapidstart-pakkefil, du vil indlæse, og vælg derefter handlingen **Åbn**. Under indlæsning dekomprimeres pakkeindholdet, og pakkeposten oprettes.  

    Når indlæsningen er fuldført, kan du se antallet af konfigurationstabeller, der er indlæst, i feltet **Antal tabeller**.  
4. For at få vist listen over konfigurationstabeller skal du vælge handlingen **Vis**.  
5. Hvis du vil anvende pakken, skal du vælge handlingen **Anvend pakke**.  

    > [!NOTE]  
    >  Oplysningerne om dataoverflytning er baseret på konfigurationsskabeloner, hvis du angiver en. Du skal opdatere skabelonen, inden du kan ændre listen over felter.  

6.  For at gennemse valget af felter skal du markere en tabel og derefter under fanen **Linjer** vælge handlingen **Felter**. Du kan sammenligne og gennemgå antallet af felter, der er tilgængelige, med antallet af felter, hvis data er blevet anvendt.  

Hvis tabellerne ikke opfylder dine behov, kan du oprette en eller flere nye dataoverflytningsfiler. Hvis filerne opfylder dine behov, kan du fortsætte med dataoverflytningen ved hjælp af Excel- eller XML-filer.

## <a name="to-create-a-data-migration-file"></a>Sådan oprettes en dataoverflytningsfil

Du kan oprette nye dataoverflytningsfiler og tilpasse dem til din virksomheds behov.  

> [!TIP]
> En fil kan kun bruges til at overflytte et felt, hvis dens egenskab **FieldClass** er indstillet til **Normal**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakke**, og vælg derefter det relaterede link.  
2. Vælg og åbn den pakke, du vil bruge til at overføre data, og vælg derefter handlingen **Hent tabeller**. Siden **Hent pakketabel** åbnes.  
3. I feltet **TableID** skal du indtaste et tal i tabellen eller vælge en tabel på listen, f.eks. tabel 18 **Debitor**. Feltet **Tabelnavn** udfyldes automatisk.  
4. Vælg den nye overflytningstabel, og vælg derefter under fanen **Tabeller** handlingen **Felter**. Siden **Overflytningsfelter** åbnes.  
5. Ryd afkrydsningsfeltet **Inkluder felt** ud for de felter, som du ikke vil indlæse, og vælg derefter handlingen **Angiv inkluderede** eller **Ryd inkluderede**.  

> [!IMPORTANT]  
>  Hvis afkrydsningsfeltet **Medtag felt** som standard er markeret, er feltet en del af den primære nøgle. Markeringen bør ikke fjernes. Elles vil der opstå fejl, og posten kan ikke indlæses.  
>
>  Hvis du medtager et felt, der har en relation til en anden tabel, markeres afkrydsningsfeltet **Valider felt** automatisk. Validering kan resultere i opdateringen af andre felter i denne og andre tabeller og afvikles i feltnumrenes rækkefølge.  

Der oprettes en ny overflytningstabel .  

## <a name="to-export-data-migration-files"></a>Sådan udlæses overflytningsfiler
Når du har fastlagt de tabeller, du vil overføre debitordata til, skal du eksportere filerne.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
2. Markér og åbn den pakke, som du vil bruge til eksport.
3. Vælg den eller de tabeller, du vil eksportere, og vælg derefter handlingen **Udlæs til Excel**.
4. Gem den eksporterede Excel-fil.  
5. Gentag denne procedure for alle relevante dataoverflytningstabeller. Hvis du markerer flere tabeller samtidig, udlæses deres data til et fælles regneark.  

Hvis tallen er tom, indeholder den resulterende dataoverflytningsfil tomme celler for de felter, du markerede, da du valgte eller oprettede overflytningstabeller for din nye virksomhed. Hvis den markerede dataoverflytningstabel indeholder data, udlæses de.  

## <a name="to-map-values-to-be-used-during-import"></a>Sådan tilknytter du værdier, der skal bruges under import
Når du anvender data, som du har importeret fra Excel eller fra en RapidStart-pakke, behandler og håndterer [!INCLUDE[d365fin](includes/d365fin_md.md)] tilknytningen på basis af tabelrelationer:  

- Hvis du defineret en kobling direkte for et felt i en tabel, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] bruge den.  

- Hvis feltet har en relation til en anden tabel, søger [!INCLUDE[d365fin](includes/d365fin_md.md)] efter den kobling, der er defineret for det primære nøglefelt i den relaterede tabel. Den relaterede tabel skal dog være en del af konfigurationspakken.  

- Hvis koblingsoplysninger er defineret begge steder, for feltet direkte og for den primære nøgle i den relaterede tabel, så vil [!INCLUDE[d365fin](includes/d365fin_md.md)] søge efter koblingen begge steder.  

- Hvis de samme koblinger er defineret direkte for et felt og i den relaterede tabel, men de har forskellige nye værdier, tilsidesætter den kobling, der er defineret direkte for feltet, den kobling, der er defineret for den tabel, som feltet refererer til.  

I nedenstående fremgangsmåder bør du gennemgå på forhånd, hvilke værdier du vil bevare under overflytningen. Hvis du vil udføre følgende procedurer, skal du bruge dataoverflytningsfiler (.xlsx), du har eksporteret fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Sådan udlæses overflytningstabeller](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.
2. Åbn pakken for den pågældende virksomhed.  
3. Vælg tabellen, hvor du vil tilknytte værdier, og vælg derefter under fanen **Tabeller** handlingen **Felter**.  
4. For hvert felt du vil tilknytte, skal du vælge handlingen **Kobling**.  
5. Brug feltet **Gammel værdi** til at angive den værdi, som skal ændres. Brug feltet **Ny værdi** til at angive den værdi, som den gamle værdi skal ændres til. Vælg knappen **OK**.  
6. Importér debitordataene. Du kan finde flere oplysninger i [Sådan importeres debitordata](admin-migrate-customer-data.md#to-import-customer-data).
7. Brug feltet **Antal pakkefejl** til at se, om der er rapporteret fejl. Hvis der er, skal du dykke ned for at få vist fejlene. Siden **Konfigurationspakkeposter** åbnes.
8. Vælg handlingen **Vis fejl**. Du får vist følgende fejl: **XX er ikke en gyldig indstilling. Gyldige indstillinger er: XX**. Vælg knappen **OK**.  
9. Du kan anvende den tilknytning, som du har oprettet, ved at vælge handlingen **Anvend Data**.  

### <a name="mapping-example"></a>Eksempel på tilknytning  
Følgende eksempel illustrerer, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] implementerer koblingsdefinitionerne.  

1. Oprette en konfigurationstabel med tabellen **Sælger/indkøber**. Definere en tilknytning for feltet **Kode**.  
2. Tilføj flere tabeller til pakken, f.eks. **Debitor** og **Kreditor**. Disse tabeller refererer begge til tabellen **Sælger/indkøber** via henholdsvis **sælgerkoden** og **indkøberkoden**.  
3. Når du anvender data, tages den tilknytning, du har angivet i feltet **Kode** i tabellen **Sælger/indkøber**, også i betragtning ved behandlingen af felterne **Sælgerkode** og **Indkøberkode**.

## <a name="to-add-additional-values-to-d365fin"></a>Sådan føjer du flere værdier til [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Konfigurationspakker**, og vælg derefter det relaterede link.  
2. Vælg tabellen, hvor du vil tilføje yderligere værdier, og vælg derefter under fanen **Tabeller** handlingen **Felter**.  
3. For de felter, hvor [!INCLUDE[d365fin](includes/d365fin_md.md)] skal tillade flere værdier under overflytningen, skal du markere afkrydsningsfeltet **Opret manglende koder**.  
4. Importér debitordataene. Du kan finde flere oplysninger i [Sådan importeres debitordata](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Rydde op og behandle data, før du anvender data
I nogle tilfælde kan du rydde op i kundedata og behandle dem, før du udligner dem til databasen. For at gøre dette, kan du bruge kørslen **Konfigurationspakke - proces** til at løse problemer, f.eks.:  

- Konverter datoer og decimaler til det format, som kræves af de internationale indstillinger på en brugers computer.  
- Fjern foranstillede/efterstillede mellemrum eller specialtegn.  

Når du har kørt kørslen, kan du benytte følgende fremgangsmåde til at behandle data.  

1. Åbn konfigurationspakken for virksomheden.  
2. Vælg handlingen **Behandl data**.  
3. Du kan anvende den tilknytning, som du har oprettet, ved at vælge handlingen **Anvend Data**.

## <a name="to-migrate-customer-data"></a>Sådan overføres debitordata
Når du har eksporteret en overflytningstabel, er dit næste skridt at angive debitorens ældre data. For at forenkle dine opgaver, kan du drage fordel af de XML-manipulationsværktøjer, der er indbygget i Excel. Du kan også bruge indbyggede funktioner i Excel til at hjælpe med dataformatering og til at indsætte data i den korrekte celle.

For at få hjælp til XML kan du aktivere fanen **Udvikler** på Excel-båndet, og derefter vælge handlingen **Kilde** for at få vist XML-skemaet for overførselstabellen, som den er repræsenteret i Excel.

Følgende fremgangsmåde er baseret på et Excel-regneark, du har oprettet til overflytning. Du kan finde flere oplysninger i [Sådan udlæses overflytningstabeller](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> Undlad at ændre kolonnerne i Excel-regnearkene. Hvis de flyttes, ændres eller slettes, kan regnearket ikke importeres i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. I Excel skal du åbne den eksporterede datafil. Der er et regneark med navnet på tabellen.
2. Omdøb Ark1 for at angive, at regnearket skal bruges til at omdanne dataene. Kopier overskriftsrækken uden tekstformatering fra den eksporterede tabel til det nye regneark.
3. På et tredje regneark skal du kopiere alle dine debitordata. Omdøb arket, så det hedder f.eks. Ældre data.
4. Skriv en Excel-formel til at afbilde dataene i overflytningsregnearket mellem felterne i det eksporterede regneark og debitorens ældre data.
5. Når du har tilknyttet alle data, skal du kopiere dataområdet ind i regnearket med tabellen.
6. Gem filen, og sørg for ikke at ændre filtypen.

Du er nu klar til at importere dataoverflytningsfilerne, der indeholder debitorens ældre data, i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Sådan importeres debitordata
Når debitordata er indsat i dataoverflytningsfilerne i Excel, kan du indlæse filerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Åbn siden **Konfig.pakkekort**.
2. Vælg tabellen, hvor du vil importere data, og vælg derefter under fanen **Tabeller** handlingen **Indlæs fra Excel**.
3. Find og åbn den fil, du vil importere data fra.
4. På siden **Eksempel på import af konfig.pakke** kan du gennemse det indhold, der skal importeres.

    Siden **Eksempel på import af konfig.pakke** indeholder en oversigt over indholdet af Excel-filen, der skal importeres. Den angiver også, om der oprettes en ny konfigurationspakke, eller den eksisterende opdateres, og om nye konfigurationspakkelinjer (tabeller) er oprettet, eller eksisterende er opdateret.    
5. Vælg handlingen **Importér**.

Data fra filen importeres til konfigurationspakketabellerne. Du kan se antallet af databaseposter, der er blevet importeret, i feltet **Antal pakkerecords**. Desuden kan du se antallet af overflytningsfejl.

## <a name="to-validate-customer-data"></a>Sådan valideres debitordata
Kundedata skal valideres, før du anvender poster til [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

> [!NOTE]  
>  I de fleste tilfælde oprettes ugyldige data ikke i databasen. Programmet kan dog lejlighedsvis blokeres, hvis en importeret overflytningstabel indeholder fejl.  

1. På siden **Overflytningsoversigt** skal du gennemse feltet **Antal overflytningsfejl** for at se, om der opstod fejl under import.  
2. Hvis der er fejl, skal du vælge overflytningstabellen, og derefter under fanen **Tabeller** vælge handlingen **Fejl**. Afkrydsningsfeltet **Ugyldig** er markeret for hver post, der har en fejl.  
3. Hvis du vil gennemse fejl, skal du markere en linje og derefter vælge handlingen **Vis fejl**.  

    Feltet **Fejltekst** viser årsagen til fejlen. Feltet **Felttitel** indeholder titelteksten for feltet, der indeholder fejlen.  
4.  Hvis du vil rette en fejl eller på anden måde foretage en opdatering, skal du på siden **Overflytningsoversigt** vælge handlingen **Overflytningspost** og derefter i rette posten med fejl på siden **Overflytningspost**.  

Når du har foretages en rettelse, fjernes posten fra listen over poster på siden **Dataoverførselsfejl**.  

Du er nu klar til at anvende debitorens data i databasen.  

## <a name="to-apply-customer-data"></a>Sådan overføres debitordata
Når du har importeret alle de dataoverflytningsposter, der er gyldige, og som ikke indeholder fejl, kan du overføre posterne til [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Åbn siden **Konfigurationspakker**.  
2. Vælg tabellen for den dataoverflytningsfil, du vil anvende, og vælg derefter handlingen **Anvend data**.

Du kan se antallet af databaseposter, der er blevet oprettet, i feltet **Antal databaserecords**. Du kan kontrollere, at det korrekte antal poster er blevet oprettet, ved at vælge linket i feltet **Antal databaserecords**.  

Virksomhedens kundedatabase er nu indstillet, og grundlæggende data er nu importeret. Dine næste trin i implementeringsprocessen er at oplære brugere, definere processer, oprette yderligere data, tilpasse rapporter osv.

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
