---
title: Eksportere Business Central-data til Excel | Microsoft Docs
description: Du kan eksportere dine regnskabsrapporter og business intelligence-data fra Business Central til Excel eller åbne dine data i Excel.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 382bee236225c1038430bb2243c6c54b56ef772e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240998"
---
# <a name="exporting-your-business-data-to-excel"></a>Eksportere forretningsdata til Excel
Hvis du vil arbejde med dine data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Excel, kan du åbne alle lister i Excel og arbejde med dem der. På samme måde, hvis du vil annullere dit abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du eksportere dataene til Excel, så du kan tage dem med dig.

## <a name="opening-lists-in-excel"></a>Åbne lister i Excel
Du kan åbne data i Excel fra enhver kladde, liste eller regneark. Du skal bare åbne den ønskede side og derefter vælge **Åbn i Excel**. Du kan f.eks. åbne listen over debitorer (søg efter **Debitorer**) og derefter klikke på **Åbn i Excel**. Din du bliver bedt om at åbne eller gemme den oprettede Excel-projektmappe.  

> [!NOTE]
> Brug denne indstilling, når du ikke vil foretage ændringer og publicere dem tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Hver liste indeholder et antal kolonner, og eksporten til Excel medtager alle de kolonner, der er i den aktuelle visning. Hvis du vil tilføje eller fjerne kolonner, før du åbner listen i Excel, kan du åbne genvejsmenuen for en kolonne og derefter angive, hvilke kolonner der skal vises. Listen over kolonner er forskellig for de fleste lister, og den afspejler strukturen i den database, hvor dine data er gemt. Hvis du ikke er sikker på, hvilken type data en bestemt kolonne indeholder, kan du føje den til visningen og derefter beslutte, om du vil fjerne den igen.  

### <a name="edit-data-in-excel"></a>Redigere data i Excel
Din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse omfatter et tilføjelsesprogram til Excel, så du kan redigere data i Excel. Du kan finde flere oplysninger i [Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Eksportere data til andre økonomisystemer
Hvis du beslutter at annullere dit abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du eksportere dine data til Excel og tage dem med dig til dit næste økonomisystem.  

Du kan eksportere alle sider, men det kan være mere, end du reelt har brug for. Derfor bør du overveje at eksportere følgende vigtige sider og huske at tilføje alle kolonner som tidligere beskrevet:  

* Kontoplan  
* Kunder (Debitorer)  
* Leverandører (Kreditorer)  
* Banker  
* Varer  

Hvis du også vil medtage alle dine finansielle transaktioner, er det en stor mængde data, så eksporten tager ofte mere end blot et par minutter. Finansielle transaktioner vises på siden **Finansposter**.  

Det anbefales, at du også overvejer at eksportere data fra følgende sider:  

* Debitorposter  
* Kreditorposter  
* Bankkontoposter  
* Vareposter  
* Bogføringsopsætning  
* Debitorbogføringsgrupper  
* Kreditorbogføringsgrupper  
* Varebogføringsgrupper  
* Bankbogføringsgruppe  
* Finansbudgetter  
* Finansbudgetposter  
* Salgstilbud  
* Salgsfakturaer  
* Købsfakturaer  
* Kontakter  
* Sælgere  

> [!NOTE]  
>   Hvis du har oprettet mere end én virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du eksportere de relevante data fra hver virksomhed.

## <a name="see-also"></a>Se også
[Annullere dit abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-cancel.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Finans](finance.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
