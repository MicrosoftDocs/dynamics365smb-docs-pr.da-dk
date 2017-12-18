---
title: Serviceprisstyring | Microsoft Docs
description: "I dette emne beskrives, hvordan du anvender den bedste pris på serviceordrer, at oprette personlige serviceprisaftaler for debitorer, at forbedre servicemedarbejdernes effektivitet og at forbedre faktureringsprocessen."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e9eb165c8ccb196f687c11f4cb4353d88c71de3c
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="service-price-management"></a>Serviceprisstyring
Funktionen til serviceprisstyring gør det muligt at angive den bedste pris på serviceordrer, at oprette personlige serviceprisaftaler for debitorer, at forbedre servicemedarbejdernes effektivitet og at forbedre faktureringsprocessen.  
  
Med serviceprisstyring kan du oprette forskellige serviceprisgrupper, så du kan tage højde for serviceartiklen eller serviceartikelgruppen og for den type fejl, serviceopgaven dækker. Disse grupper kan oprettes for en begrænset periode eller for en bestemt debitor eller valuta. Du kan bruge prisberegningsstrukturer som skabeloner til at tildele en bestemt pris til en bestemt serviceopgave.  
  
Det gør det f.eks. muligt at angive, at bestemte artikler er inkluderet i serviceprisen, og at angive den type arbejde, der er involveret. Dette gør det muligt at bruge forskellige moms- og rabatbeløb for forskellige serviceprisgrupper. For at sikre at den korrekte pris anvendes, kan du bruge faste priser, minimumpriser eller maksimumpriser, afhængigt af de aftaler du indgår med debitorerne.  
  
Inden prisen for en serviceartikel i en serviceordre reguleres, vises en oversigt over, hvad en prisregulering medfører. Du kan godkende resultatet af prisreguleringen, eller du kan foretage flere ændringer, hvis du vil opnå et andet resultat. Reguleringen foretages linje for linje, hvilket medfører, at der ikke oprettes flere linjer.  
  
Ved hjælp af statistikker for serviceprisgrupper og standardrapporter kan du holde styr på rentabiliteten for hver serviceprisgruppe.  
  
## <a name="service-price-adjustment-groups"></a>Serviceprisreguleringsgrupper  
Du bruger serviceprisreguleringsgrupper til at oprette forskellige typer prisreguleringer. Du kan f.eks. oprette en serviceprisreguleringsgruppe, der regulerer priserne på reservedele, en, der regulerer priser for arbejdskraft, en, der regulerer priser på omkostninger, osv. Du kan også angive, om serviceprisregulering kun skal anvendes på én specifik vare eller ressource eller på alle varer eller ressourcer.  
  
Hver serviceprisreguleringsgruppe indeholder oplysninger om reguleringer, som du vil foretage på servicelinjerne.  
  
Serviceprisreguleringsfunktionen gælder ikke de serviceartikler, der hører til servicekontrakter. Du kan kun regulere servicepriserne på de artikler, der er en del af en serviceordre. Du kan ikke regulere prisen på en serviceartikel, hvis den dækkes af en garanti. Du kan ikke justere prisen på en serviceartikel i en serviceordre, hvis den tilknyttede servicelinje er bogført som faktura, enten helt eller delvist.  
  
Når du bruger funktionen til serviceprisregulering, erstattes alle rabatter i ordren med værdierne i serviceprisreguleringen.  
  
## <a name="service-price-groups"></a>Serviceprisgrupper  
Du kan oprette serviceprisgrupper for at oprette grupper med serviceartikler, der kan opnå samme særlige serviceprissætning. Når du har oprettet serviceprisgrupperne, kan du tildele dem til serviceartikler på serviceartikellinjer. Du kan også tildele serviceprisgrupper til serviceartikelgrupper.  
  
Inden du kan tildele en serviceprisgruppe til en serviceartikel, skal du bestemme, hvilken fejltype, valuta eller serviceprisreguleringsgruppe serviceprisgruppen anvender. Du skal beslutte, hvordan serviceprisen skal reguleres, og om beløbet skal være inklusive moms og rabatter. Du skal også beslutte, om denne regulering gælder et fast beløb, eller om den kun skal anvendes under særlige betingelser.  
  
Når du tildeler en serviceprisgruppe til en serviceartikel, vil alle særlige serviceprissætninger, som du opretter i denne gruppe, blive tildelt til denne serviceartikel.  
  
## <a name="service-pricing"></a>Serviceprissætning  
Du definerer de faktiske typer serviceprissætning (prisreguleringstype og pris) for en kombination af serviceprisgrupper og debitorprisgrupper. For hver type serviceprissætning skal du vælge en serviceprisreguleringsgruppe. Du skal også angive prisreguleringstypen, fast, maksimum eller minimum, og den faktiske pris.  
  
Du kan f.eks. definere serviceprissætningstyper for en radioreparationsprisgruppe. For kunder uden prisgruppe kan du bestemme, at du vil have en serviceprisgruppe med maksimumspris på arbejde, arbejdsprisreguleringsgruppen. For kunder i en bestemt prisgruppe kan du bestemme, at du vil have serviceprissætning med fast pris på arbejde, dvs. samme arbejdsprisreguleringsgruppe.  
  
## <a name="service-price-adjustment"></a>Serviceprisregulering  
Ved hjælp af serviceprisreguleringer kan du regulere prisen på en vare, ressource, finanskonto eller omkostning i en serviceordre.  
  
Når du har angivet en vare på serviceartikellinjerne, skal du angive alle oplysninger om omkostningen for denne artikel på servicelinjerne. Når du kører funktionen Reguler servicepris, kan du få vist prisreguleringerne. Du kan foretage eventuelle ændringer i vinduet. Når du bekræfter ændringerne, beregnes reguleringerne, og de overføres derefter til servicelinjerne. Derefter kan du bogføre serviceordren.  
  
Det samlede reguleringsbeløb beregnes afhængigt af serviceprisreguleringstypen.  
  
Følgende tabel beskriver beregningerne.  
  
|Indstilling | Description |  
|----------------------------------|---------------------------------------|  
|**Fast pris**|Dette betyder, at du tager en fast pris for serviceartiklen, ressourcen, finanskontoen eller omkostningen, uanset den reelle omkostning eller gebyrer. Hvis du vælger denne indstilling, vil resultatet af serviceprisreguleringen svare til det beløb, der er angivet i serviceprisgruppen.|  
|**Maksimum**|Dette betyder, at du kan angive en øvre grænse for, hvor meget debitoren skal betale, uanset de reelle omkostninger eller gebyrer. Hvis du vælger denne indstilling, vil serviceprisreguleringen kun blive foretaget, hvis den samlede pris overskrider det beløb, der er angivet i serviceprisgruppen.|  
|**Minimum**|Dette betyder, at du kan angive en nedre grænse for, hvor meget debitoren skal betale, uanset de reelle omkostninger eller gebyrer. Hvis du vælger denne indstilling, vil serviceprisreguleringen kun blive foretaget, hvis den samlede pris er mindre end det beløb, der er angivet i serviceprisgruppen.|  
  
## <a name="see-also"></a>Se også  
[Fremgangsmåde: Konfigurere prissætning og ekstra omkostninger for services](service-how-setup-service-costs-pricing.md)  
[Konfigurere Service](service-setup-service.md)  

