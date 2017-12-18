---
title: "Søgning efter data og angivelse af filtreringskriterier | Microsoft Docs"
description: "Beskriver, hvordan du arbejder med filtre, f.eks. Quick Filter, for at finjustere resultatet, når du søger efter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Søgning i, filtrering og sortering af data
Der er et par ting, du kan gøre som en hjælp til at finde, identificere og scanne poster på en liste. Disse omfatter sortering, søgning og filtrering.

Når du vil søge efter data, f.eks debitornavne, adresser eller produktgrupper i grupper, skal du angive kriterier. I søgekriterier kan du bruge alle de tal og bogstaver, som du plejer at bruge i det specifikke felt. Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere. Der kan søges på to måder: Ved hjælp af Quick Filter eller med kolonnefiltre.

## <a name="sorting"></a>Sortering
Sortering gør det nemt og hurtigt for dig at overskue dine oplysninger. Hvis du har mange kunder, f.eks. kan du vælge at sortere dem efter **Kundenr.**, **Debitorbogføringsgruppe**, **Valutakode**, **Lande-/områdekode** eller **Momsregistreringsnr.** for at få det nødvendige overblik.

Hvis du vil sortere en liste, kan du enten vælge en kolonneoverskriftstekst, hvor du kan skifte mellem stigende og faldende rækkefølge, eller du kan vælge den lille nedadgående pil i kolonneoverskriften og derefter vælge **Stigende** eller **Faldende**.  

> [!NOTE]  
>   Sortering understøttes ikke af billeder, BLOB-felter, FlowFilters og felter, der ikke tilhører en tabel.  

## <a name="searching-by-using-the-quick-filter"></a>Søge ved hjælp af Quick Filter
Du kan føje filtre til alle sider ved hjælp af Quick Filter. Quick Filter aktiveres ved at klikke på ikonet Forstørrelsesglas i øverste højre hjørne af en side. Denne filtreringstype bruges til en hurtig indtastning af kriterier.

> [!IMPORTANT]  
>   Quick Filter giver en nem adgang til at filtrere data ved at angive almindelig tekst, men giver også mange søgekriterieindstillinger. Afhængigt af, om du indtaster ren tekst eller tekst, der inkluderer symboler, fungerer Quick Filter forskelligt.  

* Hvis du angiver almindelig tekst i søgekriterierne, fortolkes søgekriterierne som en søgning uden skelnen mellem store og små bogstaver, der indeholder bestemt tekst.  
* Hvis du indtaster tekst, herunder symboler i søgekriterierne, fortolkes søgekriterierne nøjagtigt, som du har angivet, og der skelnes mellem store og små bogstaver.

### <a name="quick-filter-criteria"></a>Quick Filter-kriterier
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Søgekriterier</TH>
    <TH>Fortolkes som...</TH>
    <TH>Returnerer...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alle poster, der indeholder teksten <b>man</b>, og som ikke skelner mellem små og store bogstaver.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Alle poster, der indeholder teksten <b>se</b>, og som ikke skelner mellem små og store bogstaver.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Starter med <b>Man</b> og skelner mellem små og store bogstaver.</TD>
    <TD>Alle poster, der starter med teksten <b>Man</b></TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>En nøjagtig tekst, hvor der skelnes mellem store og små bogstaver.</TD>
    <TD>Alle poster, der nøjagtigt svarer til <b>man</b></TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Starter med og uden skelnen mellem små og store bogstaver.</TD>
    <TD>Alle poster, der starter med <b>man</b></TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Slutter med og uden skelnen mellem små og store bogstaver.</TD>
    <TD>Alle poster, der slutter med <b>man</b></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Du kan ikke bruge et jokertegn, når du filtrerer i optællingsfelter, f.eks. feltet **Status** på salgsordrer. Hvis du vil angive et filter for denne type felt, kan du angive den numeriske værdi som en filterparameter. I feltet **Status** på en salgsordre med værdierne **Åben**, **Frigivet**, **Afventer godkendelse** og **Afventer forudbetaling** kan du f.eks. bruge værdierne, **0**, **1**, **2** og **3** til at filtrere efter disse indstillinger. 

## <a name="searching-by-using-column-filters"></a>Søge ved hjælp af kolonnefiltre
Du kan tilføje et filter til en eller flere kolonner på en liste. Filtrering på kolonner er mere fleksibelt og omfattede end Quick Filter. 

### <a name="to-add-a-filter-on-a-column"></a>Sådan tilføjes et filter på en kolonne
1.  Før du tilføjer et filter, skal du vælge ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Pil til venstre Vis som liste") for at skifte til listevisningen.
2. Vælg den nedadgående pil i kolonneoverskriften, og vælg derefter **Filter**.
3. Gør ét af følgende: 
  -  Vælg *...* ud for feltet for at vælge en værdi på en liste.
  -  Angiv filterkriterier i feltet. Se næste afsnit kan få flere oplysninger.
4. Vælg knappen **OK**.

## <a name="filter-criteria-and-symbols"></a>Filterkriterier og -symboler
Når du angiver kriterier, kan du bruge alle de tal og bogstaver, som du plejer at bruger i feltet. Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere. Følgende tabeller viser de tegn, der kan bruges i filtre.  
  
> [!IMPORTANT]  
>  Der kan være tilfælde, hvor feltværdierne indeholder disse symboler, og du vil filtrere efter dem. Hvis du vil gøre dette, skal du medtage det filterudtryk, der indeholder symbolet i anførselstegn ("). Hvis du f.eks. vil filtrere efter poster, der starter med teksten *S&R*, er filterudtrykket **S&R*'**.  
  
### <a name="-interval"></a>(..) Interval  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|1100..2100|Tal fra 1100 til og med 2100.|  
|..2500|Konti til og med 2500|  
|..31-12-00|Datoer til og med 31-12-00.|  
|P8..|Oplysninger for regnskabsperiode 8 og frem|  
|..23|Fra begyndelsesdatoen til 23-aktuel måned-aktuelt år 23.59.59|  
|23..|Fra 23-aktuel måned-aktuelt år 0.00.00 til sluttidspunktet|  
|22..23|Fra den 23-aktuel måned-aktuelt år 0.00.00 til 22-aktuel måned-aktuelt år 22.59.59|  
  
### <a name="124-eitheror"></a>(&#124;) Enten/eller  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|1200&#124;1300|Tal med 1200 eller 1300.|  
  
### <a name="-not-equal-to"></a>(<>) Ikke lig med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<>0|Alle tal undtagen 0<br /><br /> I SQL Server Option kan du kombinere dette symbol med et udtryk med jokertegn. <>A* betyder f.eks. ikke lig med tekst, der starter med A.|  
  
### <a name="-greater-than"></a>(>) Større end  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>1200|Tal større end 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Større end eller lig med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>=1200|Tal lig med eller større end 1200|  
  
### <a name="-less-than"></a>(<) Mindre end  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<1200|Tal mindre end 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Mindre end eller lig med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<=1200|Tal lig med eller mindre end 1200|  
  
### <a name="-and"></a>(&) Og  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>200&<1200|Tal større end 200 og mindre end 1200|  
  
### <a name="-an-exact-character-match"></a>('') Tegn, der stemmer nøjagtigt overens  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|'man'|Tekst, der svarer nøjagtigt til man, og der skelnes mellem store og små bogstaver.|  
  
### <a name="-case-insensitive"></a>(@) Ingen forskel på store og små bogstaver  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|@man*|Tekst, der starter med man, og der skelnes mellem store og små bogstaver.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Mange ukendte tegn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|*A/S*|Tekst, der indeholder "A/S", og der skelnes mellem store og små bogstaver.|  
|*A/S|Tekst, der ender på "A/S", og der skelnes mellem store og små bogstaver.|  
|A/S*|Tekst, der begynder med "A/S", og der skelnes mellem store og små bogstaver.|  
  
### <a name="-one-unknown-character"></a>(?) Ét ukendt tegn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|Hans?n|Tekst som f.eks. Hansen eller Hanson|  
  
### <a name="combined-format-expressions"></a>Kombinerede formatudtryk  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Tallet 5999 og tallene fra og med 8100 til og med 8490.|  
|..1299&#124;1400..|Medtag poster med et tal mindre end eller lig med 1299, eller tal lig med 1400 eller derover (alle tal undtagen 1300 til og med 1399).|  
|>50&<100|Medtag poster med tal større end 50 og mindre end 100 (tal fra 51 til og med 99).|  
 
## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

