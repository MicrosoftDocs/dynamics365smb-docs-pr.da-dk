---
title: Administrere lager ved at slette dokumenter eller komprimere data
description: Få mere at vide om, hvordan du kan håndtere historiske dokumenter (og reducere mængden af data, der er gemt i en database) ved at slette eller komprimere dem.
author: edupont04
ms.topic: conceptual
ms.search.form: 107, 9035, 9040
ms.date: 09/14/2022
ms.author: edupont
ms.openlocfilehash: d6a98decb0b518629e29673d21147acc079b1b9e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607359"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Administrere lager ved at slette dokumenter eller komprimere data

En central rolle, f.eks. som programadministrator, skal regelmæssigt håndtere store mængder akkumulerede oversigtsdokumenter, der skal slettes eller komprimeres.  

> [!TIP]
> Du kan finde flere oplysninger om, hvordan du reducerer mængden af data, der er gemt i en database, ved at læse [Reduktion af data, der er gemt i Business central-databaser](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i vores Developer and IT Pro-dokumentation.

## <a name="delete-documents"></a>Slette dokumenter.

Du kan i visse situationer have behov for at slette fakturerede indkøbsordrer. Du kan dog ikke slette dem, medmindre du har fuldt faktureret for og modtaget varerne i indkøbsordrerne. [!INCLUDE[prod_short](includes/prod_short.md)] hjælper dig med at kontrollere det.

Returordrer slettes normalt, når de er faktureret. Når en faktura bogføres, overføres den til siden **Bogført købskreditnota**. Hvis afkrydsningsfeltet **Returvarekvit. på kreditnota** er markeret på siden **Købsopsætning**, overføres den til siden **Bogført returvareleverance**. Du kan slette dokumenter ved hjælp af kørslen **Slet fakt. købsreturvareordrer**. Før du sletter, kontrollerer kørslen, om købsreturvareordreordrer er fuldt leveret og faktureret.  

Rammekøbsordrer slettes ikke automatisk, når du har behandlet og faktureret alle relaterede købsordrer. Du kan slette dem med batchjobbet **Slet fakturerede rammekøbsordrer**.  

Fakturerede serviceordrer slettes som regel automatisk, når de er faktureret fuldt ud. Når en faktura bogføres, oprettes der en tilsvarende post, som kan ses på siden **Bogførte servicefakturaer**.  

Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra siden **Servicefaktura**. Det kan være nødvendigt at slette fakturerede ordrer manuelt ved at udføre batchjobbet **Slet fakturerede serviceordrer**.  

## <a name="compress-data-with-date-compression"></a>Komprimere data med datokomprimering

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)], så du sparer plads i databasen, hvilket i [!INCLUDE [prod_short](includes/prod_short.md)] online kan spare penge. Komprimeringen er baseret på datoer og funktioner og kombinerer flere gamle poster til en ny post.

Du kan komprimere poster, der opfylder alle af følgende betingelser:

* De er fra afsluttede regnskabsår.
* Feltet **Åbn** er angivet til **Nej**.
* De er mindst fem år gamle. Hvis du vil komprimere data, der er mindre end fem år gamle, skal du kontakte din Microsoft-partner.

Kreditorposter fra forrige regnskabsår kan f.eks. komprimeres, så der kun er én kreditpost og én debetpost pr. konto pr. måned. Beløbet i den nye post er summen af alle komprimerede poster. Den angivne dato er startdatoen i den periode, der skal komprimeres, f.eks. første dag i måneden, hvis der komprimeres pr. måned. Efter komprimeringen kan du stadig se bevægelserne på hver konto i det forrige regnskabsår.

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der er altid mindst én post. Når kørslen er færdig, kan du se resultatet på siden **Datokompr.journaler**.

Du kan komprimere følgende datatyper ved hjælp af batchjob.

* Finansposter – finansposter, momsposter, bankkontoposter, finansbudgetposter, debitorfinansposter og kreditorfinansposter.
* Lagerposter
* Ressourceposter
* Varebudgetposter
* Anlægsaktivfinansposter, anlægsreparationsposter og anlægsforsikringsposter.

Når du angiver kriterier for komprimeringen, kan du bevare indholdet af visse felter med indstillingerne under **Bevar feltindhold**. De felter, der er tilgængelige, afhænger af de data, du komprimerer.

> [!NOTE]
> Før du kan udføre datokomprimering, skal dine analysevisninger være aktuelle. Du kan finde flere oplysninger i [Opdatere en analysevisning](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Efter komprimeringen bevares indholdet i følgende felter altid: **Bogføringsdato**, **Kreditornr.**, **Dokumenttype**, **Valutakode**, **Bogføringsgruppe**, **Beløb**, **Resterende beløb**, **Oprindeligt beløb (LCY)**, **Resterende beløb (LCY)**, **Beløb (LCY)**, **Køb (LCY)**, **Fakturarabat (LCY)**, **Ydet kont.rabat (LCY)** og **Mulig kontantrabat**.

## <a name="posting-compressed-entries"></a>Bogføre komprimerede poster

Komprimerede poster skal bogføres en smule anderledes end standard bogføring. Det er at reducere antallet af nye finansposter, der er oprettet ved datokomprimering, og det er specielt vigtigt, når du gemmer oplysninger som f.eks. dimensioner og dokumentnumre. Datokomprimering opretter nye poster på følgende måde:

* På siden **Finansposter** oprettes nye poster for de komprimerede poster. Feltet **Beskrivelse** indeholder **Datokomprimeret**, så de komprimerede poster nemt kan identificeres. 
* På finanssider, f.eks. siden **Debitorposter**, oprettes der en eller flere ny poster. 

Bogføringsprocessen skaber huller i nummerserien til poster på siden **Finansposter**. Disse numre tildeles kun poster på finans sider. Det nummerinterval, der er knyttet til posterne, er tilgængeligt på siden **Finansjournal** i felterne **Fra løbenr.** og **Til løbenr.** 

> [!NOTE]
> Når du har kørt datokomprimering, er alle finanskonti låst. Du kan f.eks. ikke tilbageføre kreditor- eller bankposter for en konto, der er påvirket af komprimeringen.

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der vil altid være mindst én post.

> [!WARNING]
> Datokomprimering sletter posterne, så du bør altid lave en sikkerhedskopi af databasen, inden du starter kørslen.

### <a name="to-run-a-date-compression"></a>Kør datokomprimering

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dataadministration**, og vælg derefter det relaterede link.
2. Gør ét af følgende:
    * Hvis du vil bruge en assisteret vejledning til at oprette datokomprimering for en eller flere typer data, skal du vælge **Dataadministrationsguide**.
    * Hvis du vil angive komprimering for en enkelt datatype, skal du vælge **Datakomprimering**, **Komprimer poster** og derefter vælge de data, der skal komprimeres.

   > [!NOTE]
   > Du kan kun komprimere data, der er mere end fem år gamle. Hvis du vil komprimere data, der er mindre end fem år gamle, skal du kontakte din Microsoft-partner.

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
