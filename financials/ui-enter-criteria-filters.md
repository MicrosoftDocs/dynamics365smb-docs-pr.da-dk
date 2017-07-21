---
title: "Definere søgekriterier i filtre | Microsoft Docs"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Indtaste kriterier i filtre
Når du vil søge efter data, f.eks debitornavne, adresser eller produktgrupper i grupper, skal du angive kriterier. I søgekriterier kan du bruge alle de tal og bogstaver, som du plejer at bruge i det specifikke felt. Derudover kan du bruge nogle specialtegn til at filtrere resultaterne yderligere.

## <a name="searching-using-the-quick-filter"></a>Søge ved hjælp af Quick Filter
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

## <a name="see-also"></a>Se også
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

