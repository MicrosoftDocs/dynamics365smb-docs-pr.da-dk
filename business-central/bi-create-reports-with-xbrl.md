---
title: 'Fremgangsmåde: Oprette rapporter med XBRL'
description: 'XBRL er et XML-baseret sprog til kodning af finansielle data, der gør det muligt for firmaer at behandle og dele deres data effektivt og præcist.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: bholtorf
---
# <a name="create-reports-with-xbrl"></a>Oprette rapporter med XBRL

> [!NOTE]
> Du er i gang med at fjerne funktionerne til XBRL-rapportering fra [!INCLUDE[prod_short](includes/prod_short.md)]. Få mere at vide om [Ændringer i 2022 udgivelsesbølge 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL, som står for (e**X**tensible **B**usiness **R**eporting **L**anguage), er et XML-baseret sprog til kodning af finansielle data, der gør det muligt for firmaer at behandle og dele deres data effektivt og præcist. Talrige ERP-softwarevirksomheder og internationale revisionsfirmaer kan bruge XBRL-initiativerne til global finansiel rapportering. Det globale initiativ er at levere en standard for ensartet rapportering af finansielle oplysninger til banker, investorer og statslige myndigheder. Sådan virksomhedsrapportering kan omfatte:  

* Regnskabsopgørelser  
* Finansielle oplysninger  
* Ikke-finansielle oplysninger  
* Lovgivningsmæssige arkiveringer, f.eks. årsregnskaber og kvartalsmæssige regnskabsopgørelser  

> [!NOTE]
> Du kan indlæse finansrelaterede skemaer og oprette XBRL-instansdokumenter ved at knytte finansdata fra kontoplanen til de elementer i taksonomier, der er designet til finansrapporter, f.eks. balance, resultatopgørelse osv.
>
> XBRL-funktionerne i Business Central understøtter taksonomier til specifikation 2.1. Taksonomier kan imidlertid indeholde ikke-understøttede elementer, f.eks. formellinkbaser eller iXBRL (indbygget XBRL), eller som har andre strukturelle forskelle. Det anbefales, at du validerer XBRL-egenskaben, før du bruger den til rapportering.
>
> Den fulde understøttelse af taksonomier kan kræve XBRL-mærkning og -værktøjer fra tredjepart. XBRL International Organization indeholder en liste over værktøjer og tjenester, men afhængigt af XBRL-rapporteringskravene for en given taksonomi, kan det være en god idé at undersøge disse ressourcer. Du kan finde flere oplysninger i [Introduktion for virksomheder](https://go.microsoft.com/fwlink/?linkid=2153466) og [Værktøjer og tjenester](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language

XBRL-taksonomier vedligeholdes af www.xbrl.org. Du kan downloade taksonomier og læse flere detaljerede oplysninger på XBRL-webstedet.  

Lad os antage, at nogen vil have finansielle oplysninger fra dig. De leverer en taksonomi (et XML-dokument), der indeholder et eller flere skemaer, der hver har en eller flere linjer, der skal udfyldes. Linjerne skal indeholde de finansielle oplysninger, som afsenderen kræver. Du indlæser denne taksonomi og udfylder skemaerne ved at angive den eller de konti, der svarer til hver linje, og hvilken beregning, der skal anvendes, f.eks. nettobevægelser og saldo til dato. I visse tilfælde kan du i stedet angive en konstant, f.eks. antal medarbejdere. Derefter kan du sende prøvedokumentet (et XML-dokument) til den, der har anmodet om oplysningerne. Arbejdsmåden er tilrettelagt med henblik på, at det er en tilbagevendende begivenhed, så uanset om der er ændret i taksonomien, kan du blot udlæse nye dokumenter for nye perioder på forlangende.

## <a name="xbrl-comprises-the-following-components"></a>XBRL består af følgende komponenter

XBRL **Specifikation** forklarer, hvad XBRL er, og hvordan man bygger XBRL-dokumenter og XBRL-taksonomier. XBRL-specifikationen er en teknisk forklaring af XBRL og beregnet til professionelle.  

XBRL- **Skemaet** er den grundlæggende bestanddel i XBRL. Skemaet er den fysiske XSD-fil (også kaldet en XML-skemadefinition), der forklarer, hvordan XBRL-forekomstdokumenter og -taksonomier skal bygges.

XBRL-**Linkbaser** er fysiske XML-filer, der indeholder oplysninger om elementer, der er defineret i XBRL-skemaet, f.eks. om etiketter på et eller flere sprog, om deres indbyrdes relation, om hvordan elementerne skal opsummeres osv.  

En XBRL-**taksonomi** er en "ordliste" eller "ordbog" oprettet af en gruppe, der overholder XBML-specifikationen, som muliggør udveksling af forretningsmæssige oplysninger.  

Et XBRL **dokument** er en forretningsrapport, f.eks. et finansregnskab, der er forberedt til XBML-specifikationen. Betydningen af værdierne i dokumentet forklares i taksonomien. Et forekomstdokument er reelt ret værdiløst, medmindre du kender den taksonomi, den er forberedt til.  

## <a name="layered-taxonomies"></a>Niveaudelte taksonomier

En taksonomi kan bestå af en basistaksonomi, f.eks. US GAAP (i USA almindeligt godkendte regnskabsprincipper) eller IAS (internationale regnskabsstandarder), og har derefter en eller flere udvidelser. En taksonomi kan derfor henvise til ét eller flere skemaer, der alle er separate taksonomier i sig selv. Når de supplerende taksonomier er indlæst i databasen, føjes de nye elementer simpelthen til slutningen af de eksisterende elementer.  

## <a name="linkbases"></a>Linkbaser

I specifikation 2 til XBRL beskrives taksonomien i flere XML-filer. Den primære XML-fil er selve taksonomiskemafilen (med filtypen .xsd), der kun indeholder en usorteret liste med elementer eller fakta, der skal rapporteres. Normalt er der desuden tilknyttet nogle linkbasefiler (.xml). Linkbasefilerne indeholder data, der supplerer den rå taksonomi (.xsd-filen). Der er seks forskellige typer linkbasefiler, hvoraf fire er relevante for [!INCLUDE[prod_short](includes/prod_short.md)]. Det er:

* Linkbase til etiketter: Denne linkbase indeholder etiketter eller navne på elementer. Filen kan indeholde etiketter på forskellige sprog, der er angivet med en XML-egenskab, der kaldes ’lang’. XML-sprog-id’et består normalt af en forkortelse på to bogstaver, og selvom det er nemt at gætte, hvad forkortelsen betyder, er der ingen forbindelse til Microsoft Windows-sprogkoden eller til den sprogkode, der er angivet i demonstrationsdata. Når du derfor slår sprogene op for en bestemt taksonomi, vises alle etiketter for det første element i taksonomien, dvs. der er et eksempel på hvert sprog. En taksonomi kan have tilknyttet forskellige linkbaser, så længe disse linkbaser indeholder forskellige sprog.  
* Linkbase til præsentation: Denne linkbase indeholder oplysninger om strukturen af elementer eller, mere præcist, hvordan leverandøren af taksonomien foreslår, at programmet præsenterer taksonomien for brugeren. Linkbasen indeholder en serie link, der hver har tilsluttet to elementer i en overordnet-underordnet-relation. Ved hjælp af disse link kan elementerne præsenteres hierarkisk. Bemærk, at præsentationslinkbasen kun har ét formål: at præsentere elementerne for dig.
* Kalkulations-linkbase: Denne linkbase indeholder oplysninger om, hvordan elementer akkumuleres. Strukturen ligner præsentations-linkbasen, bortset fra at hvert link eller 'arc', som de hedder, har en vægtegenskab. Vægten kan være enten 1 eller –1, der angiver, om elementet skal lægges til eller trækkes fra dets overordnede. Bemærk, at de aggregerede værdier ikke nødvendigvis er i overensstemmelse med den visuelle præsentation.  
* Referencelinkbase: Linkbasen er en xml-fil, der indeholder supplerende oplysninger om de data, der kræves af leverandøren af taksonomien.

## <a name="set-up-xbrl-lines"></a>Konfigurere XBRL-linjer

Når du har indlæst eller opdateret taksonomien, skal linjerne i skemaet udfyldes med alle de oplysninger, der er nødvendige for at opfylde de konkrete krav til finansiel rapportering. De omfatter grundlæggende virksomhedsoplysninger, de faktiske regnskaber, revisors påtegninger, noter til regnskaberne, supplerende planer samt andre oplysninger, som afspejler de krævede regnskabsoplysninger.  

Du kan oprette XBLR-linjer ved at knytte dataene i taksonomien til dataene i finansposterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2. På siden **XBRL-taksonomier** skal du vælge en taksonomi fra listen.  
3. Vælg handlingen **Linjer**.  
4. Vælg en linje, og udfyld felterne.  
5. Du kan finde flere oplysninger om, hvad der skal udfyldes, ved at vælge handlingen **Oplysninger**.  
6. Hvis du vil knytte finanskontiene i kontoplanen til XBRL-linjerne, skal du vælge handlingen **Finanskoblingslinjer**.  
7. Hvis du vil tilføje noter i regnskabet, skal du vælge handlingen **Noter**.  

   > [!TIP]
   > Hvis du vil udelukke linjer fra eksporten, skal du vælge **IKKE TILGÆNGELIG** som kildetype.

   > [!NOTE]  
   > Du kan kun udlæse data, der svarer til det, du har valgt i feltet **Kildetype**. Det omfatter beskrivelser og noter.  

   > [!NOTE]  
   > Taksonomier kan indeholde elementer, som [!INCLUDE[prod_short](includes/prod_short.md)] ikke understøtter. Hvis et element ikke understøttes, kan feltet **Kildetype** vises feltet **Ikke tilgængelig**, og feltet **Beskrivelse** viser en fejlmeddelelse, f. eks **Uventet type: "den specifikke type blev ikke genkendt"**. Hvis du vil eksportere elementet, skal du vælge en tilsvarende kildetype. Dette er typisk en konstant eller en beskrivelse. På den måde kan du indtaste og eksportere data, men der kan også være valideringsregler, der ikke kan kontrolleres inden eksporten.

## <a name="import-an-xbrl-taxonomy"></a>Indlæse en XBRL-taksonomi

Første trin i arbejdet med XBRL-funktionalitet er at indlæse en taksonomi i din database. En taksonomi består af et eller flere skemaer og nogle linkbaser. Når du har indlæst både skemaer og linkbaserne og har knyttet linkbaserne til skemaet, kan du oprette linjer og knytte finanskontiene i kontoplanen til de tilsvarende taksonomilinjer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2. På siden **XBRL-taksonomier** skal du oprette en ny linje og indsætte navnet på og beskrivelsen af taksonomien.  
3. Vælg handlingen **Skemaer**, og indsæt derefter beskrivelsen af skemaet.  
4. Hvis du vil indlæse skemaet, skal du på siden **XBRL-skemaer** vælge **Import**-handlingen og derefter udføre et af følgende trin for at overføre filen:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Hvis du vil importere linkbasen, skal du på siden **XBRL-skemaer** vælge **Linkbaser**-handlingen og derefter udføre et af følgende trin for at overføre filen:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Du kan nu vælge at knytte linkbasen til skemaet. Gentag fremgangsmåden, indtil du har indlæst alle linkbaser.  
7. Vælg handlingen **Anvend til taksonomi** for at knytte linkbasen til skemaet.  

> [!IMPORTANT]  
> I stedet for at tilknytte linkbaserne enkeltvist efter indlæsningen, kan du vente, indtil du har indlæst alle linkbaserne og derefter tilknytte dem samtidig. Det gør du ved vælge knappen **NEJ**, når du bliver spurgt, om du vil tilknytte den netop indlæste linkbase til skemaet. Marker derefter linjerne med de linkbaser, du vil anvende.  

## <a name="update-an-xbrl-taxonomy"></a>Opdatere en XBRL-taksonomi

Når en taksonomi ændres, skal du opdatere den aktuelle taksonomi i overensstemmelse hermed. Årsagen til opdateringen kan være et ændret skema, en ændret linkbase eller en ny linkbase. Når du har opdateret taksonomien, skal du konvertere linjerne for de ændrede eller nye linjer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2. På siden **XBRL-taksonomier** skal du vælge handlingen **Skemaer**.  
3. Opdater skemaet ved at vælge det, du vil opdatere, og derefter vælge handlingen **Indlæs**.  
4. Hvis du vil opdatere eller tilføje en ny linkbase, skal du vælge handlingen **Linkbaser**.  
5. Vælg den relevante linkbase, eller tryk på <kbd>Ctrl</kbd>+<kbd>N</kbd> for en ny linje, vælg linkbasens type, og angiv derefter en beskrivelse.  
6. Du kan importere linkbasen ved at vælge handlingen **Indlæs**.  
7. Vælg knappen **Ja** for at anvende linkbasen til skemaet.  

## <a name="see-also"></a>Se også

[Økonomisk Business Intelligence](bi.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
