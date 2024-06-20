---
title: Opsætning af pengestrømsanalyse (indeholder video)
description: 'Opret diagrammerne i rollecenteret Revisor for at analysere pengestrømmen i virksomheden, herunder udgifter og indtægter, likviditet og indbetalinger minus kontantbetalinger.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="setting-up-cash-flow-analysis"></a>Opsætning af pengestrømsanalyse

Hvis du vil have hjælp til at beslutte, hvad du skal gøre med dine likvide midler, kan du få et overblik vha. diagrammerne i rollecenteret Regnskabsmedarbejder:

* **Kassebeholdningsproces**  
* **Indtægter og udgifter**  
* **Pengestrøm**  
* **Pengestrømsprognoser**  

Denne artikel beskriver, hvor data i diagrammerne kommer fra, og om nødvendigt, hvad du skal gøre for at begynde at bruge diagrammerne.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Diagrammerne Kassebeholdningsproces og Indtægter og udgifter

Diagrammere **Kassebeholdningsproces** og **Indtægter og udgifter** er klar til brug, baseret på kontoplanen og finansrapporter. Kontiene er, hvor dataene kommer fra, og finansrapporterne beregner forholdet mellem salg og tilgodehavender. Der findes allerede nogle konti og finansrapporter. Du kan bruge dem, som der er, ændre dem og tilføje nye. Hvis du tilføjer finanskonti i kontoplanen, f.eks. ved at importere dem fra QuickBooks, skal du oprette en tilknytning til kontiene på siden **Finansrapporter** for følgende rapporter:

| Navn på finansiel rapport | Bruges i |
| --- | --- |
| **I_CACYCLE** |Kassebeholdningsproces |
| **I_CASHFLOW** |Pengestrøm |
| **I_INCEXP** |Indtægter og udgifter |
| **I_MINTRIAL** |Som en resultatopgørelse, hvis du ikke bruger kontoplanen |

> [!NOTE]
> Bemærk! Det er en god ide at gemme de beregninger, der bruges i finansrapporter.

Angiv kontiene i feltet **Sammentælling** for **Nettoomsætning i alt**, **Tilgodehavender i alt**, **Gæld i alt** og **Lagerbeholdning i alt**. Hvis du vil knytte til en række konti, skal du angive kontonumrene adskilt af ".." som i **1111..4444**. Alternativt kan du angive kontonumrene ved at angive kontonumre adskilt af en lodret linje som i **2222|3333|5555**.  

> [!TIP] 
> Kontroller tilknytningen ved at vælge handlingen **Oversigt**.  

## <a name="set-up-the-cash-flow-chart"></a>Konfigurere diagrammet Pengestrøm

Diagrammet Pengestrøm er baseret på:  

* En plan over pengestrømskonti.
* En eller flere pengestrømskonfigurationer. Disse opsætninger angiver de konti, der skal bruges til regnskab, køb, salg, tjenester og anlæg.  

For at hjælpe dig i gang findes der i forvejen nogle konti- og pengestrømsopsætninger. Du kan tilføje, ændre eller fjerne dem.  

Du konfigurerer kontiene ved at søge efter **Pengestrømskonti**, vælge linket og derefter udfylde felterne. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Gentag disse trin for **Pengestrømsopsætning**.

## <a name="set-up-cash-flow-forecasts"></a>Konfigurere pengestrømsprognoser

Diagrammet **Pengestrømsprognose** bruger pengestrømskonti, pengestrømsopsætninger og pengestrømsbudgetter. Nogle får du leveret, men du kan oprette dine egne ved hjælp af en assisteret opsætningsvejledning. Vejledningen hjælper dig med f.eks. at angive, hvor ofte prognosen skal opdateres, de konti, den skal baseres på, oplysninger om, hvornår du betaler skatter, og om du skal aktivere [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Pengestrømsopsætning kan bruge Azure AI til at oprette en mere omfattende prognose. Forbindelsen til Azure AI allerede konfigureret for dig. Du skal blot aktivere den. Når du logger på [!INCLUDE[prod_short](includes/prod_short.md)], vises en meddelelse i en blå linje med et link til standardpengestrømsopsætningen. Meddelelsen vises kun én gang. Hvis du lukker den, men beslutter at aktivere Azure AI, kan du bruge den assisterende opsætningsvejledning eller en manuel fremgangsmåde.  

> [!NOTE]
>
> Du kan også vælge at bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til pengestrømsprognoser](#AnchorText).  

Sådan bruges den assisterede opsætningsvejledning:  

1. I rollecenteret Regnskabsmedarbejder under diagrammet **Pengestrømsprognose** skal du klikke på handlingen **Åbn assisteret opsætning**.
2. Udfyld felterne i hvert trin i vejledningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Tilbage i Rollecenteret Regnskabsmedarbejder skal du vælge handlingen **Genberegn prognose** under diagrammet **Pengestrømsprognose**.

Sådan bruges en manuel proces:  

1. I Rollecenteret Regnskabsmedarbejder kan du vælge den ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pengestrømsopsætning**, vælg derefter det relaterede link.
2. Udvid oversigtspanelet **Azure AI**, og marker derefter feltet **Azure AI aktiveret**.
3. Tilbage i Rollecenteret Regnskabsmedarbejder skal du vælge handlingen **Genberegn prognose** under diagrammet **Pengestrømsprognose**.

> [!TIP]  
> Overvej længden på de perioder, som tjenesten skal bruge i beregningerne. Jo flere data du angiver, desto mere nøjagtige forudsigelser får du. Hold også øje med store variationer mellem perioderne. De kan også påvirke forudsigelserne. Hvis Azure AI ikke finder nok data, eller dataene varierer meget, opretter tjenesten ikke en forudsigelse.  

## <a name="design-details"></a>Designoplysninger

Abonnementer på [!INCLUDE[prod_short](includes/prod_short.md)] giver adgang til flere prognosewebtjenester i alle områder, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig. Få mere at vide på Microsoft Dynamics 365 Business Central-licensvejledning. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Disse webtjenester har ingen status, hvilket betyder, at de kun bruger data til at beregne forudsigelser efter behov. De gemmer ikke data.

> [!NOTE]
>
> Du kan bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til pengestrømsprognoser](#AnchorText).

### <a name="data-required-for-forecast"></a>Data, der kræves i forbindelse med prognoser

Webtjenester kræver historiske data fra tilgodehavender, skyldige beløb og skat for at udarbejde prognoser om fremtidige indtægter og udgifter.

#### <a name="receivables"></a>Tilgodehavender

Felterne **Forfaldsdato** og **Beløb (RV)** på siden **Debitorposter**, hvor:

* Dokumenttypen er *Faktura* eller *Kreditnota*.
* Forfaldsdatoen er mellem den dato, der beregnes på grundlag af værdierne i felterne **Historiske perioder** og **Periodetype** på siden **Pengestrømskonfiguration** og arbejdsdatoen.

Før du bruger prognosewebtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Forfaldsdato** baseret på værdien i feltet **Periodetype** på siden **Pengestrømskonfiguration**.

#### <a name="payables"></a>Gæld

Felterne **Forfaldsdato** og **Beløb (RV)** på siden **Kreditorposter**, hvor:

* Dokumenttypen er *Faktura* eller *Kreditnota*.
* Forfaldsdatoen er mellem den dato, der beregnes på grundlag af værdierne i felterne **Historiske perioder** og **Periodetype** på siden **Pengestrømskonfiguration** og arbejdsdatoen.

Før du bruger prognosewebtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Forfaldsdato** baseret på værdien i feltet **Periodetype** på siden **Pengestrømskonfiguration**.

#### <a name="tax"></a>Skat

Felterne **Dokumentdato** og **Beløb** på siden **Momsvareposter (skat)**, hvor:

* Dokumenttypen er *salg*.
* Dokumentdatoen er mellem den dato, der beregnes på grundlag af værdierne i felterne **Historiske perioder** og **Periodetype** på siden **Pengestrømskonfiguration** og arbejdsdatoen.

Før du bruger prognosewebtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Dokumentdato** baseret på værdien i feltet **Periodetype** på siden **Pengestrømskonfiguration**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Oprette og bruge din egen prognosewebtjeneste til pengestrømsprognoser

Du kan også oprette din egen prognosewebtjeneste baseret på en offentlig model med navnet **Prognosemodel til Microsoft Business Central**. Denne prognosemodel er tilgængelig online i Azure AI-galleriet. Sådan bruges modellen:  

1. Åbn en webbrowser, og gå til [Azure AI-galleriet](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Søg efter **Prognosemodel til Microsoft Business Central**, og åbn derefter modellen i Microsoft Azure Machine Learning Studio.  
3. Brug din Microsoft-konto til at tilmelde dig et arbejdsområde og derefter kopiere modellen.  
4. Kør modellen, og udgiv den som en webtjeneste.  
5. Notér URL-adressen for API og API-nøglen. Du skal bruge disse legitimationsoplysninger til en pengestrømsopsætning.  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Pengestrømsopsætning**, og vælg derefter det relaterede link.  
7. Udvid oversigtspanelet **Azure AI**, og Udfyld derefter felterne, herunder API-URL-adressen og API-nøglen fra Azure Machine Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. I Rollecenteret Regnskabsmedarbejder skal du vælge handlingen **Genberegn prognose** under diagrammet **Pengestrømsprognose**.

## <a name="see-also"></a>Se også

[Analysere pengestrømme i din virksomhed](finance-analyze-cash-flow.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
