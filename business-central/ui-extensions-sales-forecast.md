---
title: Bruge udvidelsen Salgs- og lagerprognose til at styre lagerbeholdningen
description: 'Udvidelsen hjælper dig med at forudse salg, få et klart billede af forventede lagermangler og oprette genbestillingsanmodninger til kreditorer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Udvidelsen Salgs- og lagerprognose

Lagerstyring håndterer balancen mellem kundeservice og styring af omkostningerne. På én side kræver et lille lager mindre driftskapital, men på den anden side kan manglende lager medføre tabt salg. Udvidelsen Salgs- og lagerprognose forudsiger muligt salg ved hjælp af historiske data og giver et klart overblik over forbruget af lageret. Baseret på prognosen hjælper udvidelsen med at oprette genbestillingsanmodninger til dine leverandører og sparer tid.  

## Konfigurere prognose

I [!INCLUDE[prod_short](includes/prod_short.md)] er forbindelsen til [Azure AI](https://azure.microsoft.com/overview/ai-platform/) allerede konfigureret for dig. Du kan dog konfigurere en prognose, hvis du vil bruge en anden type periode i rapporten, f.eks hvis du vil skifte fra prognose pr. måned til prognose pr. kvartal. Du kan også vælge, hvor mange perioder prognosen skal beregnes for, afhængigt af hvor detaljeret prognosen skal være. Vi anbefaler prognose pr. måned og en horisont på 12 måneder for prognosen.

> [!TIP]  
> Overvej længden på de perioder, som tjenesten skal bruge i beregningerne. Jo flere data du angiver, desto mere nøjagtige forudsigelser får du. Hold også øje med store variationer mellem perioderne. De kan også påvirke forudsigelserne. Hvis Azure AI ikke finder nok data, eller dataene varierer meget, opretter tjenesten ikke en forudsigelse.

## Brug af prognoser

Udvidelsen bruger Azure AI til at forudse fremtidigt salg ud fra din salgsoversigt, så du bedre kan undgå manglende lager. Når du f.eks. vælger en vare på siden **Varer** , og diagrammet i ruden **Vareprognose** viser det anslåede salg af varen i den kommende periode. På denne måde kan du se, om du sandsynligvis vil løbe tør for lager inden længe.  

Du kan også bruge udvidelsen til at foreslå, hvornår lageret skal øges. Du kan f.eks. oprette en købsordre, så Fabrikam kan købe deres nye skrivebordsstol. Udvidelsen Salgs- og lagerforecast kan foreslå, at du også genopfylder med den LONDON-drejestol, som du normalt køber hos denne leverandør. Udvidelsen kan forudse, at lageret af LONDON-drejestolen snart vil løbe tørt, så du med fordel kan bestille flere stole allerede nu.  

## Designoplysninger

Abonnementer på [!INCLUDE[prod_short](includes/prod_short.md)] giver adgang til flere prognosewebtjenester i alle områder, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig. Du kan få flere oplysninger i Licensvejledning til Microsoft Dynamics 365 Business Central. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Disse webtjenester har ingen status, hvilket betyder, at de kun bruger data til at beregne forudsigelser efter behov. De gemmer ikke data.

> [!NOTE]  
>   Du kan også bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til salgs- og lagerprognoser](#AnchorText). 

### Data, der kræves i forbindelse med prognoser

Webtjenesten kræver kvantitative data om tidligere salg for at kunne udarbejde prognoser i forbindelse med fremtidige salg. Dataene stammer fra felterne **Bogføringsdato**, **Varenr** og **Antal** på siden **Vareposter**, hvor:

- Posttypen er "Salg".
- Bogføringsdatoen er mellem den dato, der beregnes på grundlag af værdierne i felterne **Historiske perioder** og **Periodetype** på siden **Opsætning af salgs- og lagerprognose** og arbejdsdatoen.

Før den bruger webtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Varenr.** og **Bogføringsdato** på grundlag af værdien i feltet **Periodetype** på siden **Opsætning af salgs- og lagerprognose**.

## <a name="AnchorText"> </a>Oprette og bruge din egen prognosewebtjeneste til salgs- og lagerprognose

For [!INCLUDE[prod_short](includes/prod_short.md)] online udgives modellen af Microsoft og er forbundet med Microsoft-abonnementet. Hvis du vil have andre udrulningsmuligheder, skal du oprette Machine Learning-ressourcer i dit eget Azure-abonnement. Du kan finde eksempeltrin i [prøvelager](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Formålet med denne opgave er at hente API-URI'en og API-nøglen.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af salgs- og lagerprognose**, og vælg derefter det relaterede link.  
2. Udvid oversigtspanelet **Generelt**, og udfyld derefter felterne med API URL-adressen og API-nøglen.  

## Se også

[Salg](sales-manage-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Bruge Kunstig intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Forecastoversigt over API](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
