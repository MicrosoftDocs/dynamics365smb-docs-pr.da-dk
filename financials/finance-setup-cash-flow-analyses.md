---
title: "Opsætning af pengestrømsanalyse | Microsoft Docs"
description: "Opret diagrammerne i rollecenteret Konti for at analysere pengestrømmen i virksomheden, herunder udgifter og indtægter, likviditet og indbetalinger minus kontantbetalinger."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1f6b31663aad5c777d16b82742bf11c7dce05264
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-cash-flow-analysis"></a>Opsætning af pengestrømsanalyse
Hvis du vil have hjælp til at beslutte, hvad du skal gøre med dine likvide midler, kan du få et overblik vha. diagrammerne i rollecenteret Regnskabsmedarbejder:  

* **Kassebeholdningsproces**  
* **Indtægter og udgifter**  
* **Pengestrøm**  
* **Pengestrømsprognoser**  

Dette emne beskriver, hvor data i diagrammerne kommer fra, og om nødvendigt, hvad du skal gøre for at begynde at bruge diagrammerne.  

## <a name="the-cash-cycle-and-income--expense-charts"></a>Diagrammerne Kassebeholdningsproces og Indtægter og udgifter
Diagrammere **Kassebeholdningsproces** og **Indtægter og udgifter** er klar til brug, baseret på kontoplanen og kontoskemaer. Kontiene er, hvor dataene kommer fra, og kontoskemaer beregner forholdet mellem salg og tilgodehavender. Der findes allerede nogle konti og kontoskemaer. Du kan bruge dem, som der er, ændre dem og tilføje nye. Hvis du tilføjer finanskonti i kontoplanen, f.eks. ved at importere dem fra QuickBooks, skal du oprette en tilknytning til kontiene på siden **Kontoskemaer** for følgende kontoskemanavne:  

| Kontoskemanavn | Bruges i |
| --- | --- |
| **I_CACYCLE** |Kassebeholdningsproces |
| **I_CASHFLOW** |Pengestrøm |
| **I_INCEXP** |Indtægter og udgifter |
| **I_MINTRIAL** |Som en resultatopgørelse, hvis du ikke bruger kontoplanen |

**Bemærk!** Det er en god ide at gemme de beregninger, der bruges i kontoskemaet.  

Angiv kontiene i feltet **Sammentælling** for **Nettoomsætning i alt**, **Tilgodehavender i alt**, **Gæld i alt** og **Lagerbeholdning i alt**. Du kan oprette tilknytning til en række konti eller mere end én bestemt konto ved at angive kontonumrene adskilt af henholdsvis ".." eller en lodret linje. F.eks. **1111..4444** eller **2222|3333|5555**.  

**Tip!** Kontroller tilknytningen ved at vælge handlingen **Oversigt**.  

## <a name="set-up-the-cash-flow-chart"></a>Konfigurere diagrammet Pengestrøm
Diagrammet Pengestrøm er baseret på følgende:  

* En plan over pengestrømskonti.
* En eller flere pengestrømskonfigurationer. Disse angiver de konti, der skal bruges til regnskab, køb, salg, tjenester og anlæg.  

For at hjælpe dig i gang findes der i forvejen nogle konti- og pengestrømsopsætninger. Du kan tilføje, ændre eller fjerne dem.  

Du konfigurerer dem ved at søge efter **pengestrømskonti**, vælge linket og derefter udfylde felterne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Gentag disse trin for **pengestrømskonti**.  

## <a name="set-up-cash-flow-forecasts"></a>Konfigurere pengestrømsprognoser
Diagrammet **Pengestrømsprognose** bruger pengestrømskonti, pengestrømsopsætninger og pengestrømsbudgetter. Nogle får du leveret, men du kan oprette dine egne ved hjælp af en assisteret opsætningsvejledning. Vejledningen hjælper dig med f.eks. at angive, hvor ofte prognosen skal opdateres, de konti, den skal baseres på, oplysninger om, hvornår du betaler skatter, og om du skal aktivere [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite).  

Pengestrømsprognoser kan bruge Cortana Intelligence til at medtage dokumenter med forfaldsdato i fremtiden. Resultatet er en mere omfattende forudsigelse. Forbindelsen til Cortana Intelligence er allerede konfigureret for dig. Du skal blot aktivere den. Når du logger på [!INCLUDE[d365fin](includes/d365fin_md.md)], vises en meddelelse i en blå linje med et link til standardpengestrømsopsætningen. Meddelelsen vises kun én gang. Hvis du lukker den, men beslutter at aktivere Cortana Intelligence, kan du bruge den assisterende opsætningsvejledning eller en manuel fremgangsmåde.  

> [!NOTE]  
>   Du kan også vælge at bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til pengestrømsprognoser](#AnchorText).  

Sådan bruges den assisterede opsætningsvejledning:  

1. I rollecenteret Regnskabsmedarbejder under diagrammet **Pengestrømsprognose** skal du klikke på handlingen **Åbn assisteret opsætning**.  
2. Udfyld felterne i hvert trin i vejledningen.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pengestrømsprognose**, og vælg derefter det relaterede link.
4. I vinduet **Pengestrømsprognose** skal du vælge handlingen **Genberegn prognose**.  

Sådan bruges en manuel proces:  

1. I rollecenteret Regnskabsmedarbejder skal du søge efter **Pengestrømskonfiguration** og derefter vælge det relaterede link.  
2. Udvid oversigtspanelet **Cortana Intelligence**, og marker derefter afkrydsningsfeltet **Cortana Intelligence aktiveret**.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pengestrømsprognose**, og vælg derefter det relaterede link.
4. I vinduet **Pengestrømsprognose** skal du vælge handlingen **Genberegn prognose**.  

> [!TIP]  
>   Overvej længden på de perioder, som tjenesten skal bruge i beregningerne. Jo flere data du angiver, desto mere nøjagtige forudsigelser får du. Hold også øje med store variationer mellem perioderne. De kan også påvirke forudsigelserne. Hvis Cortana Intelligence ikke finder nok data, eller dataene varierer meget, opretter tjenesten ikke en forudsigelse.  

## <a name="AnchorText"> </a>Oprette og bruge din egen prognosewebtjeneste til pengestrømsprognoser.
Du kan også oprette din egen prognosewebtjeneste baseret på en offentlig model med navnet **Prognosemodel for Microsoft Finance and Operations, Business edition**. Denne prognosemodel er tilgængelig online i Cortana Intelligence-galleriet. Sådan bruges modellen:  

1. Åbn en webbrowser, og gå til [Cortana Intelligence-galleriet](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Søg efter **Prognosemodel for Microsoft Finance and Operations, Business edition**, og åbn derefter modellen i Azure Machine Learning Studio.  
3. Brug din Microsoft-konto til at tilmelde dig et arbejdsområde og derefter kopiere modellen.  
4. Kør modellen, og udgiv den som en webtjeneste.  
5. Notér URL-adressen for API og API-nøglen. Du skal bruge disse legitimationsoplysninger til en pengestrømsopsætning.  
6. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Pengestrømskonfiguration**, og vælg derefter det relaterede link.  
7. Udvid oversigtspanelet **Cortana Intelligence**, og udfyld derefter felterne.  

## <a name="see-also"></a>Se også
[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

