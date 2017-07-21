---
title: "Konfigurere skattegrupper, områder og skatteregioner i USA og Canada | Microsoft Docs"
description: "Få mere at vide om, hvordan moms konfigureres, og hvordan skattegrupper, skatteområder (stater, lande, byer og lokaliteter), skatteregioner og skattedetaljer fungerer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 763bb1b954b30734b0f81f121a6534c83442321a
ms.contentlocale: da-dk
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-in-the-us-and-canada"></a>Rapportering af moms i USA og Canada
Når du begynder at bruge [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du køre en assisteret opsætningsvejledning for hurtigt og nemt angive oplysninger for din virksomhed, debitorer og kreditorer. I løbet af minutter kan du oprette salgs- og købsdokumenter med korrekt beregnet moms. Det er beskrevet [i vores blogindlæg](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Hvis du flytter til den tomme Min virksomhed, anbefales det, at du starter med hver assisteret opsætningsvejledning, herunder én til moms. Hvis du vil oprette moms selv, kan du i denne artikel læse, hvad der skal tages højde for.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Skattegrupper, skatteområder og skatteregioner
I [!INCLUDE[d365fin](includes/d365fin_md.md)] udgør en skattegruppe en gruppe lagervarer eller ressourcer, der er omfattet af de samme beskatningsregler. F.eks. kan du oprette én skattegruppe for momspligtige varer og en anden for ikke-momspligtige varer. Du skal knytte skattegruppekoder til lagervarer og finanskonti. På samme måde skal du knytte skatteområdekoder til kunder, placeringer og til dine egne virksomhedsindstillinger. Den assisterede opsætningsvejledning hjælper dig med at gøre dette.  

Hvert skatteområde er en gruppe af momsregioner baseret på en bestemt geografiske placering. F.eks. omfatter Miami, Florida-skatteområdet tre momsregioner: by (Miami), region (Dade) og stat (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder et begrænset sæt af skatteområder med en standardkonfiguration, men du kan ændre dem og tilføje nye skatteområder.  

Hvis du opretter nye skatteområder og skatteregioner, skal du sikre, at du udfylder felterne korrekt. I USA kan stater, regioner, byer og lokalområder afkræve moms. I Canada kan forbundsregeringen og provinser opkræve moms. Virksomheder indsamler og sender moms til disse myndigheder for produkter, der sælges til slutbrugere. Der kan også blive opkrævet moms af eksisterende moms. F.eks. kan der beregnes moms af beløb på en salgsfaktura, der allerede indeholder moms fra andre skatteregioner.  

I Canada skal du angive momsbeløb i dokumenter for hver skatteregion. Op til fire skatteregioner kan vises i et dokument, og skatteregioner, der har samme udskrivningsrækkefølge, kombineres, når de udskrives.  

## <a name="tax-details"></a>Skattedetaljer
Vinduet **Skattedetaljer** viser forskellige kombinationer af momsregioner og momsgrupper til fastlæggelse af momssatser. Det anbefales, at du for hver region opretter én skattegruppe for normal moms, en anden skattegruppe for varer eller tjenester, der ikke beskattes, og en ekstra skattegruppe for hver type vare eller service, der behandles med en anden momssats i den pågældende region.  

I USA, når du sælger til en kunde på en lokation, hvor du ikke har en *rei* – eller en juridisk lokation – opkræver du ikke moms. For lokationer, hvor du ikke har en rei, skal du sikre, at både feltet **Skat under Minimum** og feltet **Skat over Maks** er 0,00.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Salgsmoms og moms på varer og ydelser i Canada](ca-finance-tax.md)  
[Nem opsætning af moms](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

