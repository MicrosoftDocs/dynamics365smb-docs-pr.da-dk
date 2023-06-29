---
title: Bruge udvidelsen Salgs- og lagerprognose til at styre lagerbeholdningen | Microsoft Docs
description: 'Udvidelsen hjælper dig med at forudse salg, få et klart billede af forventede lagermangler og oprette genbestillingsanmodninger til kreditorer.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 12/20/2021
ms.author: edupont
---

# <a name="the-sales-and-inventory-forecast-extension"></a><a name="the-sales-and-inventory-forecast-extension"></a>Udvidelsen Salgs- og lagerprognose

Lagerstyring håndterer balancen mellem kundeservice og styring af omkostningerne. På én side kræver et lille lager mindre driftskapital, men på den anden side kan manglende lager medføre tabt salg. Udvidelsen Salgs- og lagerprognose forudsiger muligt salg ved hjælp af historiske data og giver et klart overblik over forbruget af lageret. Baseret på prognosen hjælper udvidelsen med at oprette genbestillingsanmodninger til dine leverandører og sparer tid.  

## <a name="setting-up-forecasting"></a><a name="setting-up-forecasting"></a>Konfigurere prognose

I [!INCLUDE[prod_short](includes/prod_short.md)] er forbindelsen til [Azure AI](https://azure.microsoft.com/overview/ai-platform/) allerede konfigureret for dig. Du kan dog konfigurere en prognose, hvis du vil bruge en anden type periode i rapporten, f.eks hvis du vil skifte fra prognose pr. måned til prognose pr. kvartal. Du kan også vælge, hvor mange perioder prognosen skal beregnes for, afhængigt af hvor detaljeret prognosen skal være. Vi anbefaler prognose pr. måned og en horisont på 12 måneder for prognosen.

> [!TIP]  
> Overvej længden på de perioder, som tjenesten skal bruge i beregningerne. Jo flere data du angiver, desto mere nøjagtige forudsigelser får du. Hold også øje med store variationer mellem perioderne. De kan også påvirke forudsigelserne. Hvis Azure AI ikke finder nok data, eller dataene varierer meget, opretter tjenesten ikke en forudsigelse.

## <a name="use-the-forecasts"></a><a name="use-the-forecasts"></a>Brug af prognoser

Udvidelsen bruger Azure AI til at forudse fremtidigt salg ud fra din salgsoversigt, så du bedre kan undgå manglende lager. Når du f.eks. vælger en vare på siden **Varer** , og diagrammet i ruden **Vareprognose** viser det anslåede salg af varen i den kommende periode. På denne måde kan du se, om du sandsynligvis vil løbe tør for lager inden længe.  

Du kan også bruge udvidelsen til at foreslå, hvornår lageret skal øges. Hvis du f.eks. opretter en købsordre for Fabrikam, fordi du vil købe deres nye skrivebordsstol, vil udvidelsen Salgs- og lagerprognose foreslå, at du også øger lageret af LONDON-drejestolen, som du normalt køber hos denne leverandør. Det skyldes, at udvidelsen forudser, at lageret af LONDON-drejestolen vil løbe tørt i de kommende to måneder, så du med fordel kan bestille flere stole allerede nu.  

## <a name="design-details"></a><a name="design-details"></a>Designoplysninger

Abonnementer på [!INCLUDE[prod_short](includes/prod_short.md)] giver adgang til flere prognosewebtjenester i alle områder, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig. Du kan få flere oplysninger i Licensvejledning til Microsoft Dynamics 365 Business Central. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Disse webtjenester har ingen status, hvilket betyder, at de kun bruger data til at beregne forudsigelser efter behov. De gemmer ikke data.

> [!NOTE]  
>   Du kan også bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til salgs- og lagerprognoser](#AnchorText). 

### <a name="data-required-for-forecast"></a><a name="data-required-for-forecast"></a>Data, der kræves i forbindelse med prognoser

Webtjenesten kræver kvantitative data om tidligere salg for at kunne udarbejde prognoser i forbindelse med fremtidige salg. Dataene stammer fra felterne **Bogføringsdato**, **Varenr** og **Antal** på siden **Vareposter**, hvor:

- Posttypen er "Salg".
- Bogføringsdatoen er mellem den dato, der beregnes på grundlag af værdierne i felterne **Historiske perioder** og **Periodetype** på siden **Opsætning af salgs- og lagerprognose** og arbejdsdatoen.

Før du bruger webtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Varenr.** og **Bogføringsdato** på grundlag af værdien i feltet **Periodetype** på siden **Opsætning af salgs- og lagerprognose**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Oprette og bruge din egen prognosewebtjeneste til salgs- og lagerprognose

Du kan også oprette din egen prognosewebtjeneste baseret på en offentlig model med navnet **Prognosemodel til Microsoft Business Central**. Denne prognosemodel er tilgængelig online i Azure AI-galleriet. Sådan bruges modellen:  

1. Åbn en webbrowser, og gå til [Azure AI-galleriet](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Søg efter **Prognosemodel til Microsoft Business Central**, og åbn derefter modellen i Azure Machine Learning Studio.  
3. Brug din Microsoft-konto til at tilmelde dig et arbejdsområde og derefter kopiere modellen.  
4. Kør modellen, og udgiv den som en webtjeneste.  
5. Notér URL-adressen for API og API-nøglen. Du skal bruge disse legitimationsoplysninger til en pengestrømsopsætning.  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af salgs- og lagerprognose**, og vælg derefter det relaterede link.  
7. Udvid oversigtspanelet **Generelt**, og udfyld derefter felterne med API URL-adressen og API-nøglen.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/use-sales-inventory-forecast-extension/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Bruge Kunstig intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
