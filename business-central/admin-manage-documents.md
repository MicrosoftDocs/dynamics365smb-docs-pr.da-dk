---
title: Administrere lager ved at slette dokumenter eller komprimere data
description: Få mere at vide om, hvordan du kan bevare dine historiske oplysninger ved at komprimere poster eller slette den.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0d713f57345c312ddbfe6b5462f2623b1088dfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753863"
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

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)], så du sparer plads i databasen, hvilket i [!INCLUDE [prod_short](includes/prod_short.md)] online kan endda spare penge. Komprimeringen er baseret på datoer og fungerer ved at kombinere flere gamle poster til en ny post. Du kan kun komprimere poster fra afsluttede regnskabsår, og der indgår kun kreditorposter, hvor der står **Nej** i feltet *Åben*.  

Kreditorposter fra forrige regnskabsår kan f.eks. komprimeres, så der kun er én kreditpost og én debetpost pr. konto pr. måned. Beløbet i den nye post er summen af alle de komprimerede poster. Den tildelte dato er startdatoen for den komprimerede periode, typisk den første dag i måneden (hvis posterne komprimeres pr. måned). Efter komprimeringen kan du stadig se bevægelserne på hver konto i det forrige regnskabsår.

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der vil altid være mindst én post. Når kørslen er færdig, kan du se resultatet på siden **Datokompr.journaler**.

Du kan komprimere følgende datatyper [!INCLUDE [prod_short](includes/prod_short.md)] ved hjælp af batchjob:

* Bankkontoposter

  Efter komprimering kan du med funktionen **Bevar feltindhold** vælge at bevare indholdet i felterne **Dokumentnr., Vores kontakt**, **Global dimension 1-kode** og **Global dimension 2-kode**.
* Kreditorposter

  Efter komprimeringen bevares indholdet i følgende felter altid: **Bogføringsdato**, **Kreditornr.**, **Dokumenttype**, **Valutakode**, **Bogføringsgruppe**, **Beløb**, **Resterende beløb**, **Oprindeligt beløb (LCY)**, **Resterende beløb (LCY)**, **Beløb (LCY)**, **Køb (LCY)**, **Fakturarabat (LCY)**, **Ydet kont.rabat (LCY)** og **Mulig kontantrabat**.

  Desuden kan du bruge funktionen **Bevar feltindhold** til at bevare oplysningerne i følgende felter: **Dokumentnr.**, **Kreditornr.**, **Indkøberkode**, **Global dimension 1-kode** og **Global dimension 2-kode**.

> [!NOTE]
> Når du har kørt datokomprimering, er alle finanskonti låst. Du kan f. eks. ikke annullere udligning af kreditor-eller bankposter for en konto i den periode, hvor datoerne er komprimeret.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Antallet af poster, der kommer ud af en datokomprimeringskørsel, afhænger af, hvilke filtre du indstiller, hvilke filtre der kombineres og hvilken periodelængde, du vælger. Der vil altid være mindst én post. 

> [!WARNING]
> Ved datokomprimering slettes posterne, så du bør altid lave en sikkerhedskopi af databasen, inden du starter kørslen.

Følgende tabel viser felterne i oversigtspanelet **Indstillinger**, der er tilgængelige på alle batchjob. Afsnittet **Bevar feltindhold** indeholder yderligere felter, der er beskrevet ovenfor.

|Felt  |Description  |
|-------|-------------|
|Startdato     |Indtast den første dato, der skal medtages i datokomprimeringen. Komprimeringen vil omfatte alle momsposter fra denne dato og frem til slutdatoen.|
|Afslutningsdato     |Angiv den sidste dato, der skal medtages i datokomprimeringen. Komprimeringen vil omfatte alle momsposter fra startdatoen og frem til denne dato.|
|Periodelængde |Angiv længden på den periode, hvor der skal komprimeres poster. Klik på feltet for at se indstillingerne. Hvis du markerer periodelængden *Kvartal*, *Måned* eller *Uge*, komprimeres kun poster med samme regnskabsperiode.|
|Bevar feltindhold     |Marker felterne, hvis du vil bevare indholdet af bestemte felter, selvom posterne komprimeres. Jo flere felter du markerer, desto mere detaljerede bliver de komprimerede poster. Hvis du ikke markerer nogen af felterne, oprettes der kun én post pr. dag, uge eller anden periode, alt efter tidsintervallet i feltet **Periodelængde**. |

## <a name="see-also"></a>Se også

[Opsætning](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]