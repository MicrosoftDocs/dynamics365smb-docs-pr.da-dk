---
title: Administrere lager ved at slette dokumenter eller komprimere data
description: Få mere at vide om, hvordan du kan håndtere historiske dokumenter (og reducere mængden af data, der er gemt i en database) ved at slette eller komprimere dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: e29e3c0c4ce7b6cfc5ce3f38cd67781c377991ad
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543041"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Administrere lager ved at slette dokumenter eller komprimere data

En central rolle, f.eks. som programadministrator, skal regelmæssigt håndtere store mængder akkumulerede oversigtsdokumenter, der skal slettes eller komprimeres.  

> [!TIP]
> Du kan finde flere oplysninger om, hvordan du reducerer mængden af data, der er gemt i en database, i afsnittet om [Reduktion af data, der er gemt i Business central-databaser](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i Developer and IT Pro Help.

## <a name="delete-documents"></a>Slet dokumenter

Du kan i visse situationer have behov for at slette fakturaer. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om de slettede købsordrer er fuldt faktureret. Du kan kun slette ordrer, hvis de er blevet fuldt faktureret og modtaget.  

Returvareordrer slettes normalt, når de er faktureret. Når en faktura bogføres, overføres den til siden **Bogført købskreditnota**. Hvis afkrydsningsfeltet **Returvarekvit. på kreditnota** er markeret på siden **Købsopsætning**, overføres den også til siden **Bogført returvareleverance**. Du kan slette dokumenter ved hjælp af kørslen **Slet fakt. købsreturvareordrer**. Før du sletter, kontrollerer kørslen, om købsreturvareordreordrer er fuldt leveret og faktureret.  

Rammekøbsordrer slettes ikke, når du har behandlet og faktureret alle relaterede købsordrer. Du kan slette rammeordrer med kørslen **Slet fak. rammekøbsordrer**.  

Fakturerede serviceordrer slettes som regel automatisk, når de er faktureret fuldt ud. Når en faktura bogføres, oprettes der en tilsvarende post på siden **Bogførte servicefakturaer**. Det bogførte dokument kan ses i på siden **Bogført servicefaktura**.  

Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra siden **Servicefaktura**. Det kan i så fald være nødvendigt at slette fakturerede ordrer, der ikke er slettet. Det kan du gøre ved at aktivere kørslen **Slet fakturerede serviceordrer**.  

## <a name="compress-data-with-date-compression"></a>Komprimer data med datokomprimering

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)], så du sparer plads i databasen, hvilket i [!INCLUDE [prod_short](includes/prod_short.md)] online kan endda spare penge. Komprimeringen er baseret på datoer og fungerer ved at kombinere flere gamle poster til en ny post. Du kan kun komprimere poster fra afsluttede regnskabsår, og der indgår kun kreditorposter, hvor der står **Nej** i feltet **Åben**.  

Kreditorposter fra forrige regnskabsår kan f.eks. komprimeres, så der kun er én kreditpost og én debetpost pr. konto pr. måned. Beløbet i den nye post er summen af alle de komprimerede poster. Den tildelte dato er startdatoen for den komprimerede periode, typisk den første dag i måneden (hvis posterne komprimeres pr. måned). Efter komprimeringen kan du stadig se bevægelserne på hver konto i det forrige regnskabsår.

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der vil altid være mindst én post. Når kørslen er færdig, kan du se resultatet på siden **Datokompr.journaler**.

Du kan komprimere følgende datatyper ved hjælp af batchjob. Der er en kørsel for hver type data.

* Finansposter – finansposter, momsposter, bankkontoposter, finansbudgetposter, debitorposter, kreditorposter.
* Lagerposter 
* Ressourceposter
* Varebudgetposter
* Anlægsaktiver - anlægsposter, anlægsreparationsposter, anlægsforsikringsposter.

Når du angiver kriterier for komprimeringen, kan du bruge indstillingerne under feltet **Bevar feltindhold** til at bevare oplysningerne i bestemte felter. De felter, der er tilgængelige, afhænger af de data, du komprimerer.

> [!NOTE]
> Før du kan udføre datokomprimering, skal dine analyser være opdaterede. Du kan finde flere oplysninger i [Opdatere en analysevisning](/dynamics365/business-central/bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Efter komprimeringen bevares indholdet i følgende felter altid: **Bogføringsdato**, **Kreditornr.**, **Dokumenttype**, **Valutakode**, **Bogføringsgruppe**, **Beløb**, **Resterende beløb**, **Oprindeligt beløb (LCY)**, **Resterende beløb (LCY)**, **Beløb (LCY)**, **Køb (LCY)**, **Fakturarabat (LCY)**, **Ydet kont.rabat (LCY)** og **Mulig kontantrabat**.

> [!NOTE]
> Komprimerede poster skal bogføres en smule anderledes end standard bogføring. Det er at reducere antallet af nye finansposter, der er oprettet ved datokomprimering, og det er specielt vigtigt, når du gemmer oplysninger som f.eks. dimensioner og dokumentnumre. Datokomprimering opretter nye poster på følgende måde:
>* På siden **Finansposter** oprettes nye poster med nye løbenumre for de komprimerede poster. Feltet **Beskrivelse** indeholder **Datokomprimeret**, så de komprimerede poster nemt kan identificeres. 
>* På Finanssider, f.eks. siden **Debitorposter** oprettes der en eller flere poster med nye løbenumre. 
> Bogføringsprocessen skaber huller i nummerserien til poster på siden **Finansposter**. Disse numre tildeles kun poster på finans sider. Det nummerinterval, der er knyttet til posterne, er tilgængeligt på siden **Finansjournal** i felterne **Fra løbenr.** og **Til løbenr.** 

> [!NOTE]
> Når du har kørt datokomprimering, er alle finanskonti låst. Du kan f.eks. ikke annullere udligning af kreditor-eller bankposter for en konto i den periode, hvor datoerne er komprimeret.

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der vil altid være mindst én post. 

> [!WARNING]
> Ved datokomprimering slettes posterne, så du bør altid lave en sikkerhedskopi af databasen, inden du starter kørslen.

### <a name="to-run-a-date-compression"></a>Kør datokomprimering
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dataadministration**, og vælg derefter det relaterede link.
2. Gør ét af følgende:
    1. Hvis du vil bruge en assisteret installationsvejledning til at oprette datokomprimering for en eller flere typer data, skal du vælge **guiden dataadministration**.
    1. Hvis du vil angive komprimering for en enkelt datatype, skal du vælge **datokomprimering**, **Komprimer poster** og derefter vælge de data, der skal komprimeres.

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]