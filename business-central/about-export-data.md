---
title: Eksportere Business Central-data til Excel
description: Du kan eksportere dine regnskabsrapporter og business intelligence-data fra Business Central til Excel eller åbne dine data i Excel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="export-your-business-data-to-excel"></a>Eksportere Business-data til Excel

Excel er et effektivt værktøj til at arbejde med data. Du kan åbne alle lister i Excel fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan endda ændre data i Excel og derefter sende dem tilbage til [!INCLUDE [prod_short](includes/prod_short.md)]. Med denne funktion kan du let tage data med dig, hvis du beslutter dig for at opsige dit abonnement.

## <a name="opening-lists-in-excel"></a>Åbne lister i Excel

Du kan åbne data i Excel fra enhver kladde, liste eller regneark. Du skal bare åbne den ønskede side og derefter vælge **Åbn i Excel**. Du kan f.eks. åbne listen over debitorer (søg efter **Debitorer**) og derefter klikke på **Åbn i Excel**. Din du bliver bedt om at åbne eller gemme den oprettede Excel-projektmappe.  

> [!NOTE]
> Brug denne indstilling, når du ikke vil foretage ændringer og publicere dem tilbage til [!INCLUDE[prod_short](includes/prod_short.md)].  

Hver liste indeholder nogle kolonner. Eksporter til Excel indeholder alle kolonner, som findes i den aktuelle visning. Du kan ændre kolonnerne ved at åbne genvejsmenuen for en vilkårlig kolonne og derefter angive, hvilke kolonner du vil have vist. Listen over kolonner adskiller sig fra de fleste lister. Kolonnerne afspejler strukturen i den database, der indeholder dine data. Hvis du ikke er sikker på, hvilken type data en bestemt kolonne indeholder, kan du tilføje den i visningen. Du kan altid fjerne den igen.  

### <a name="edit-data-in-excel"></a>Redigere data i Excel

Din [!INCLUDE[prod_short](includes/prod_short.md)]-oplevelse omfatter et tilføjelsesprogram til Excel, så du kan redigere data i Excel. Du kan finde flere oplysninger i [Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Eksportere data til andre økonomisystemer

Hvis du beslutter at annullere dit abonnement på [!INCLUDE[prod_short](includes/prod_short.md)], kan du eksportere dine data til Excel og tage dem med dig til dit næste økonomisystem.  

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
> Hvis du har oprettet mere end én virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)], skal du eksportere de relevante data fra hver virksomhed.

> [!NOTE]
> Du skal have mindst én af følgende tilladelser for at kunne åbne eller redigere data i Excel:
>
> * Tilladelsessæt *D365 Excel-eksporthandling*  
> * Systemtilladelse 6110 *Tillad handlingen Eksporter til Excel*.  

Du kan finde flere oplysninger i [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Se også
[Annullere dit abonnement på [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Import af virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere regnskaber i Microsoft Excel](finance-analyze-excel.md)  
[Finans](finance.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
