---
title: Sådan oprettes rapporter med XBRL | Microsoft Docs
description: XBRL, som står for eXtensible Business Reporting Language, er et XML-baseret sprog til kodning af finansielle data, der gør det muligt for firmaer at behandle og dele deres data effektivt og præcist.
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
ms.openlocfilehash: 6a327ffa67dcf5f9a388c99b236ce9cbf5755561
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307536"
---
# <a name="create-reports-with-xbrl"></a>Oprette rapporter med XBRL
XBRL, som står for eXtensible Business Reporting Language, er et XML-baseret sprog til kodning af finansielle data, der gør det muligt for firmaer at behandle og dele deres data effektivt og præcist. Talrige ERP-softwarevirksomheder og internationale revisionsfirmaer kan bruge XBRL-initiativerne til global finansiel rapportering. Det globale initiativ er at levere en standard for ensartet rapportering af finansielle oplysninger til banker, investorer og statslige myndigheder. Sådan virksomhedsrapportering kan omfatte:  

 • Regnskabsopgørelser  
 • Finansielle oplysninger  
 • Ikke-finansielle oplysninger  
 • Lovgivningsmæssige arkiveringer, f.eks. årsregnskaber og kvartalsmæssige regnskabsopgørelser  

 Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan virksomhederne implementere data i XBRL, og drage fordel af den fleksibilitet og automatisering, det indebærer, både ved indsamling og deling af data.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage) er et XML-baseret sprog til finansiel rapportering. XBRL indeholder en standard for ensartet rapportering for alle brugere af finansielle oplysninger, f.eks. offentlige og private virksomheder, revisorer, analytikere, investorer, interessenter fra kapitalmarkedet og långivere. Standarden benyttes også af andre involverede nøglepartnere, f.eks. udviklere af software og hardwareleverandører.  

Taksonomier vedligeholdes af www.xbrl.org. Du kan downloade taksonomier og få flere detaljerede oplysninger på XBRL-webstedet.  

En partner, der vil have finansielle oplysninger fra dig, leverer en taksonomi (et XML-dokument), der indeholder et eller flere skemaer, der hver har en eller flere linjer, der skal udfyldes. Linjerne skal indeholde de finansielle oplysninger, som afsenderen kræver. Du indlæser denne taksonomi i programmet og udfylder skemaerne ved at angive den eller de konti, der svarer til hver linje, og hvilken tidshorisont, der skal anvendes, f.eks. bevægelser og saldo til dato. I visse tilfælde kan du i stedet angive en konstant, f.eks. antal medarbejdere. Derefter kan du sende prøvedokumentet (et XML-dokument) til den, der har anmodet om oplysningerne. Arbejdsmåden er tilrettelagt med henblik på, at det er en tilbagevendende begivenhed, så uanset om der er ændret i taksonomien, kan du blot udlæse nye dokumenter for nye perioder på forlangende.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL består af følgende komponenter  
XBRL- **specifikationen** forklarer, hvad XBRL er, hvordan man bygger XBRL-dokumenter og XBRL-taksonomier. XBRL-specifikationen er en teknisk forklaring af XBRL og beregnet til professionelle.  

XBRL- **Skemaet** er den grundlæggende bestanddel i XBRL. Skemaet er den fysiske XSD-fil, der forklarer, hvordan eksempeldokumenter og taksonomier skal bygges.  

XBRL- **linkbaser** er fysiske XML-filer, der indeholder diverse oplysninger om elementer, der er defineret i XBRL-skemaet, f.eks. om etiketter på et eller flere sprog, om deres indbyrdes relation, om hvordan elementerne skal opsummeres osv.  

En XBRL- **taksonomi** er en ordbog, der overholder XBML-specifikationen, der er skrevet af en gruppe med henblik på at kunne udveksle forretningsmæssige oplysninger.  

Et XBRL **dokument** er en forretningsrapport, f.eks. et finansregnskab, der er forberedt til XBML-specifikationen. Betydningen af værdierne i dokumentet forklares i taksonomien. Dokumentet er således værdiløst, medmindre du kender den taksonomi, den er forberedt til.  

## <a name="layered-taxonomies"></a>Niveaudelte taksonomier  
En taksonomi kan bestå af en basistaksonomi, f.eks. us-gaap eller IAS, som der er føjet én eller flere udvidelser til. En taksonomi kan derfor henvise til ét eller flere skemaer, der alle er separate taksonomier. Når de supplerende taksonomier er indlæst i databasen, føjes de nye elementer simpelthen til slutningen af de eksisterende elementer.  

## <a name="linkbases"></a>Linkbaser  
 I specifikation 2 til XBRL beskrives taksonomien i flere XML-filer. Den primære XML-fil er selve taksonomiskemafilen (med filtypen .xsd), der kun indeholder en usorteret liste med elementer eller fakta, der skal rapporteres. Normalt er der desuden tilknyttet nogle linkbasefiler (.xml). Linkbasefilerne indeholder data, der svarer til den rå taksonomi (.xsd-filen). Der er seks forskellige typer linkbasefiler, hvoraf fire er relevante for Produktnavn XBRL. Det er:  

-   Linkbase til etiketter: Denne linkbase indeholder etiketter eller navne på elementer. Filen kan indeholde etiketter på forskellige sprog, der er angivet med en XML-egenskab, der kaldes ’lang’. XML-sprog-id’et består normalt af en forkortelse på to bogstaver, og selvom det er nemt at gætte, hvad forkortelsen betyder, er der ingen forbindelse til Windows-sprogkoden eller til den sprogkode, der er angivet i demonstrationsdata. Når brugeren derfor slår sprogene op for en bestemt taksonomi, vises alle etiketter for det første element i taksonomien, dvs. der er et eksempel på hvert sprog. En taksonomi kan have tilknyttet forskellige linkbaser, så længe disse linkbaser indeholder forskellige sprog.  

-   Linkbase til præsentation: Denne linkbase indeholder oplysninger om strukturen af elementer, eller mere præcist, hvordan leverandøren af taksonomien foreslår, at programmet præsenterer taksonomien for brugeren. Linkbasen indeholder en serie link, der hver har tilsluttet et overordnet og et underordnet element. Ved hjælp af disse link kan elementerne præsenteres hierarkisk. Bemærk, at præsentationslinkbasen kun har ét formål: at præsentere elementerne for brugeren.  

-   Kalkulations-linkbasen: Denne linkbase indeholder oplysninger om, hvilke elementer der akkumuleres i andre. Strukturen ligner præsentations-linkbasen, bortset fra at hvert link eller 'arc', som de hedder, har en vægtegenskab. Vægten kan være enten 1 eller –1, der angiver, om elementet skal lægges til eller trækkes fra dets overordnede. Bemærk, at de aggregerede værdier ikke nødvendigvis er i overensstemmelse med den visuelle præsentation.  

-   Referencelinkbase: Linkbasen er en xml-fil, der indeholder supplerende oplysninger om de data, der kræves af leverandøren af taksonomien.

## <a name="to-set-up-xbrl-lines"></a>Sådan oprettes XBRL-linjer  
Når du har indlæst eller opdateret taksonomien, skal linjerne i skemaet forsynes med alle de oplysninger, der er nødvendige. Oplysningerne omfatter basisoplysninger om virksomheden, finansregnskab, bemærkninger til finansregnskabet, supplerende skemaer og andre oplysninger, der er nødvendige for at tilgodese kravene til finansiel rapportering.  

Du kan oprette XBLR-linjer ved at knytte dataene i taksonomien til dataene i finansposterne.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2.  På siden **XBRL-taksonomier** skal du vælge en taksonomi fra listen.  
3.  Vælg handlingen **Linjer**.  
4.  Vælg en linje, og udfyld felterne.   
5.  Du kan finde flere oplysninger om, hvad der skal udfyldes, ved at vælge handlingen **Oplysninger**.  
6.  Hvis du vil knytte finanskontiene i kontoplanen til XBRL-linjerne, skal du vælge handlingen **Finanskoblingslinjer**.  
7.  Hvis du vil tilføje noter i regnskabet, skal du vælge handlingen **Noter**.  

> [!NOTE]  
>  Du kan kun udlæse data, der svarer til den kildetype, du har valgt i feltet **Kildetype**, der indeholder beskrivelse og noter.  

> [!NOTE]  
>  Linjer, der ikke er relevante, kan markeres som linjetypen **IKKE TILGÆNGELIG**, så linjerne ikke udlæses.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Sådan indlæses en XBRL-taksonomi  
Første trin i arbejdet med XBRL-funktionalitet er at indlæse taksonomien i din database. En taksonomi består af et eller flere skemaer og nogle linkbaser. Når du har indlæst både skemaer og linkbaserne og har knyttet linkbaserne til skemaet, kan du oprette linjer og knytte finanskontiene i kontoplanen til de tilsvarende taksonomilinjer.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2.  På siden **XBRL-taksonomier** skal du oprette en ny linje og indsætte navnet på og beskrivelsen af taksonomien.  
3.  Vælg handlingen **Skemaer**, og indsæt derefter beskrivelsen af skemaet.  
4.  For at importere skemaet skal du på siden **XBRL-skemaer** vælge handlingen **Indlæs** og derefter vælge en mappe og en XSD-fil. Vælg knappen **Åbn**.  
5.  For at importere linkbasen skal du på siden **XBRL-skemaer** vælge handlingen **Linkbaser** og derefter vælge en mappe og en XML-fil. Vælg knappen **Åbn**.  
6.  Du kan nu vælge at knytte linkbasen til skemaet. Gentag fremgangsmåden, indtil du har indlæst alle linkbaser.  
7. Vælg handlingen **Anvend til taksonomi** for at knytte linkbasen til skemaet.  

> [!IMPORTANT]  
>  I stedet for at tilknytte linkbaserne enkeltvist efter indlæsningen, kan du vente, indtil du har indlæst alle linkbaserne og derefter tilknytte dem samtidig. Det gør du ved vælge knappen **Nej**, når du bliver spurgt, om du vil tilknytte den netop indlæste linkbase til skemaet. Marker derefter linjerne med de linkbaser, du vil anvende.  

## <a name="to-update-an-xbrl-taxonomy"></a>Sådan opdateres en XBRL-taksonomi  
Når en taksonomi ændres, skal du opdatere den aktuelle taksonomi i overensstemmelse hermed. Årsagen til opdateringen kan være et ændret skema, en ændret linkbase eller en ny linkbase. Når du har opdateret taksonomien, skal du konvertere linjerne for de ændrede eller nye linjer.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XBRL-taksonomier**, og vælg derefter det relaterede link.  
2.  På siden **XBRL-taksonomier** skal du vælge handlingen **Skemaer**.  
3.  Opdater skemaet ved at vælge det, du vil opdatere, og derefter vælge handlingen **Indlæs**.  
4.  Hvis du vil opdatere eller tilføje en ny linkbase, skal du vælge handlingen **Linkbaser**.  
5.  Vælg den relevante linkbase, eller tryk på Ctrl + N for en ny linje. Vælg linkbasens type, og angiv derefter en beskrivelse.  
6.  Du kan importere linkbasen ved at vælge handlingen **Indlæs**.  
7.  Vælg knappen **Ja** for at anvende linkbasen til skemaet.  

## <a name="see-also"></a>Se også
[Finans](finance.md)    
[Business Intelligence](bi.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
