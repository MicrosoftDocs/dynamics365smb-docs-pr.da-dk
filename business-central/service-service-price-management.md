---
title: Serviceprisstyring
description: 'Med serviceprisstyring kan du oprette serviceprisgrupper, serviceprissætning, regulering af serviceprissætning m.m.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Serviceprisstyring
Funktionen til serviceprisstyring gør det muligt at angive den bedste pris på serviceordrer, at oprette personlige serviceprisaftaler for debitorer, at forbedre servicemedarbejdernes effektivitet og at forbedre faktureringsprocessen.  
  
Med serviceprisstyring kan du oprette forskellige serviceprisgrupper, så du kan tage højde for serviceartiklen eller serviceartikelgruppen og for den type fejl, serviceopgaven dækker. Disse grupper kan oprettes for en begrænset periode eller for en bestemt debitor eller valuta. Du kan bruge prisberegningsstrukturer som skabeloner til at tildele en bestemt pris til en bestemt serviceopgave.  
  
Det gør det f.eks. muligt at angive, at bestemte artikler er inkluderet i serviceprisen, og at angive den type arbejde, der er involveret. Dette gør det muligt at bruge forskellige moms- og rabatbeløb for forskellige serviceprisgrupper. For at sikre at den korrekte pris anvendes, kan du bruge faste priser, minimumpriser eller maksimumpriser, afhængigt af de aftaler du indgår med debitorerne.  
  
Inden prisen for en serviceartikel i en serviceordre reguleres, vises en oversigt over, hvad en prisregulering medfører. Du kan godkende resultatet af prisreguleringen, eller du kan foretage flere ændringer, hvis du vil opnå et andet resultat. Reguleringen foretages linje for linje, hvilket medfører, at der ikke oprettes flere linjer.  
  
Ved hjælp af statistikker for serviceprisgrupper og standardrapporter kan du holde styr på rentabiliteten for hver serviceprisgruppe.  
  
## Serviceprisreguleringsgrupper  
Du bruger serviceprisreguleringsgrupper til at oprette forskellige typer prisreguleringer til servicelinjer. Du kan f.eks. oprette en serviceprisreguleringsgruppe, der regulerer priserne på reservedele, en, der regulerer priser for arbejdskraft, en, der regulerer priser på omkostninger, osv. Du kan også angive, om serviceprisregulering kun skal anvendes på én specifik vare eller ressource eller på alle varer eller ressourcer.  
  
Serviceprisreguleringsfunktionen gælder ikke de serviceartikler under følgende betingelser:

* Varen hører til servicekontrakter. Du kan kun regulere servicepriserne på de artikler, der er en del af en serviceordre. 
* Hvis serviceartiklen har en garanti. 
* Hvis servicelinjen er bogført som faktura, enten helt eller delvist.  
  
Når du bruger funktionen til serviceprisregulering, erstattes alle rabatter i ordren med værdierne i serviceprisreguleringen.  
  
## Serviceprisgrupper  
Du kan oprette serviceprisgrupper for at oprette grupper med serviceartikler, der kan opnå samme særlige serviceprissætning. Når du har oprettet serviceprisgrupperne, kan du tildele dem til serviceartikler på serviceartikellinjer. Du kan også tildele serviceprisgrupper til serviceartikelgrupper.  
  
Inden du kan tildele en serviceprisgruppe til en serviceartikel, skal du bestemme, hvilken fejltype, valuta eller serviceprisreguleringsgruppe serviceprisgruppen anvender. Du skal beslutte, hvordan serviceprisen skal reguleres, og om beløbet skal være inklusive moms og rabatter. Du skal også beslutte, om denne regulering gælder et fast beløb, eller om den kun skal anvendes under særlige betingelser.  
  
Når du tildeler en serviceprisgruppe til en serviceartikel, vil alle særlige serviceprissætninger, som du opretter i denne gruppe, blive tildelt til denne serviceartikel.  
  
## Serviceprissætning  
Du definerer de faktiske typer serviceprissætning (prisreguleringstype og pris) for en kombination af serviceprisgrupper og debitorprisgrupper. For hver type serviceprissætning skal du vælge en serviceprisreguleringsgruppe. Du skal også angive prisreguleringstypen, fast, maksimum eller minimum, og den faktiske pris.  
  
Du kan f.eks. definere serviceprissætningstyper for en radioreparationsprisgruppe. For kunder uden prisgruppe kan du bestemme, at du vil have en serviceprisgruppe med maksimumspris på arbejde, arbejdsprisreguleringsgruppen. For kunder i en bestemt prisgruppe kan du bestemme, at du vil have serviceprissætning med fast pris på arbejde, dvs. samme arbejdsprisreguleringsgruppe.  

#### [Aktuel oplevelse](#tab/current-experience)
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceartikler** og vælg derefter det relaterede link.  
2. Vælg serviceartiklen, udvid oversigtspanelet **Priser og salg**, vælg **Ressource**, **Vare** eller **Finanskonto**.
3. Udfyld felterne efter behov i **Projektressourcepriser**, **Projektvarepriser** eller **Projektfinanskontopriser**.

  
## Serviceprisregulering  
Ved hjælp af serviceprisreguleringer kan du regulere prisen på en vare, ressource, finanskonto eller omkostning i en serviceordre.  
  
Når du har angivet en vare på serviceartikellinjerne, skal du angive alle oplysninger om omkostningen for denne artikel på servicelinjerne. Når du kører funktionen Reguler servicepris, kan du få vist prisreguleringerne. Du kan foretage eventuelle ændringer i vinduet. Når du bekræfter ændringerne, beregnes reguleringerne, og de overføres derefter til servicelinjerne. Derefter kan du bogføre serviceordren.  
  
Det samlede reguleringsbeløb beregnes afhængigt af serviceprisreguleringstypen.  
  
Følgende tabel beskriver beregningerne.  
  
|Indstilling | Beskrivelse |  
|----------------------------------|---------------------------------------|  
|**Fast pris**|Dette betyder, at du tager en fast pris for serviceartiklen, ressourcen, finanskontoen eller omkostningen, uanset den reelle omkostning eller gebyrer. Hvis du vælger denne indstilling, vil resultatet af serviceprisreguleringen svare til det beløb, der er angivet i serviceprisgruppen.|  
|**Maksimum**|Dette betyder, at du kan angive en øvre grænse for, hvor meget debitoren skal betale, uanset de reelle omkostninger eller gebyrer. Hvis du vælger denne indstilling, vil serviceprisreguleringen kun blive foretaget, hvis den samlede pris overskrider det beløb, der er angivet i serviceprisgruppen.|  
|**Minimum**|Dette betyder, at du kan angive en nedre grænse for, hvor meget debitoren skal betale, uanset de reelle omkostninger eller gebyrer. Hvis du vælger denne indstilling, vil serviceprisreguleringen kun blive foretaget, hvis den samlede pris er mindre end det beløb, der er angivet i serviceprisgruppen.|  
  
## Se også  
[Konfigurere prissætning og ekstra omkostninger for services](service-how-setup-service-costs-pricing.md)  
[Konfigurere Service](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]