---
title: Forudsige forsinket betaling for salgsdokumenter | Microsoft Docs
description: Brug vores forudsigelsesmodel til at forudsige, om en faktura vil blive betalt til tiden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4e47858bf1f7253f8fb8951fe8ea3cb611138852
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="the-late-payment-prediction-extension"></a>Udvidelsen Forudsigelse af forsinket betaling  
Det er vigtigt med effektiv styring af skyldige beløb for virksomhedens samlede finansielle tilstand. Udvidelsen Forudsigelse af forsinket betaling kan hjælpe dig med at reducere udestående tilgodehavender og finjustere din indsamlingsstrategier ved at forudsige, om salgsfakturaer bliver betalt til tiden. Hvis der f.eks. forudsiges en forsinkelse af en betaling, kan du vælge at justere betingelserne for betalingen eller betalingsmetoden for kunden.

## <a name="what-are-predictions-based-on"></a>Hvad er forudsigelser baseret på?  
Udvidelsen Forudsigelse af forsinket betaling bruger en forudsigelsesmodel, som vi har udviklet i Azure Machine Learning Studio, og som vi har oplært ved hjælp af data, der repræsenterer en række små og mellemstore virksomheder. Selvom vi har allerede har oplært og evalueret modellen, lærer den fortsat af dine data. Efterhånden som du bruger modellen, og jo flere data, du indlæser i den, jo mere nøjagtige bliver forudsigelserne. Som standard vurderer udvidelsen modellen og opdaterer forudsigelserne på ugentlig basis. Du kan dog altid opdatere forudsigelserne ved at vælge handlingen **Opdater forudsigelse** på siden **Debitorposter**.  

> [!Note]
> Vi bruger lidt af din beregningstid hver uge, når vi vurderer modellen og opdaterer dine forudsigelser. Ud over manuelt at opdatere dine forudsigelser er der andre handlinger, der forbruger beregningstid, f.eks. når du oplærer modellen (hvilket du kan gøre, hvis du for nylig har tilføjet data), og når du vurderer modellen (som ser på kvaliteten af modellen).

## <a name="getting-started"></a>Introduktion
Udvidelsen er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], og vi leverer et abonnement på Azure Machine Learning. Abonnementet tilbyder 30 minutters beregningstid om måneden. Hvis du har brug for mere end det, kan du oprette din egen forudsigelsesmodel og bruge den i stedet. Du kan finde flere oplysninger i afsnittet _Oprettelse af din egen forudsigelsesmodel_ senere i dette emne.  

Når du åbner et bogført salgsdokument, vises en meddelelse øverst på siden. Når du vil bruge udvidelsen Forudsigelse af forsinket betaling, kan du tilvælge den ved at vælge **Aktiver** i meddelelsen. Du kan også konfigurere udvidelsen manuelt. Hvis du f.eks. fortryder at have afvist meddelelsen.  

Du kan aktivere udvidelsen manuelt ved at gøre følgende:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceforbindelser**, og vælg derefter det relaterede link.  
2. Vælg indstillingen **Opsætning af forudsigelse af forsinket betaling**, og udfyld felterne efter behov.

## <a name="viewing-all-payment-predictions"></a>Få vist alle betalingsforudsigelser
Hvis du aktiverer udvidelsen, er feltet **Betalinger, der forventes at være forsinkede** tilgængeligt i **Business Manager** Rollecenter. Feltet viser antallet af betalinger, der forventes for at være forsinkede, og du kan åbne siden **Debitorposter**, hvor du kan få mere at vide om de bogførte fakturaer. Der er tre kolonner, du skal være opmærksom på:  

* **Forsinket betaling** - Angiver, om betalingen for fakturaen forventes at være forsinket.
* **Forudsigelseskonfidens** - Angiver, hvor pålidelig du kan betragte betalingen som. **Høj** betyder, at forudsigelsen er mindst 90 % sikker, **Mellem** ligger mellem 80 og 90 % og **Lav** er mindre end 80 %.
* **Forudsigelseskonfidens-%** - Viser den faktiske procent bag sikkerhedsvurderingen. Denne kolonne vises ikke som standard, men du kan tilføje den, hvis du vil. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).

> [!Tip]
> Siden Debitorposter viser også en faktaboks til højre. Mens du gennemgår forudsigelserne, kan oplysningerne i sektionen **Debitoroplysninger** være nyttige. Når du vælger fakturaen på listen, viser sektionen oplysninger om kunden. Du kan også umiddelbart fortage handlinger der. Hvis en kunde f.eks. ofte ikke kan betale, kan du åbne debitorkortet fra faktaboksen og spærre for fremtidige salg til kunden.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Få vist en betalingsforudsigelse for et bestemt salgsdokument
Du kan også forudsige forsinkede betalinger på forhånd. På siden **Salgstilbud**, **Salgsordrer** og **Salgsfakturaer** kan du bruge handlingen **Forudsige betaling** til at oprette en forudsigelse for det salgsdokument, du får vist.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Oprettelse af din egen forudsigelsesmodel
Er du interesseret i at udvikle din egen forudsigelsesmodel? Du kan bruge Azure Machine Learning Studio til at oprette din egen forudsigelsesmodel og bruge den i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil bruge din egen model, skal du abonnere Azure Machine Learning. Du kan finde flere oplysninger i [Dokumentationen til Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Vi tilbyder dog en nemmere måde for dig at oprette og bruge dine egen forudsigelsesmodel. Du kan dele data fra dine fakturaer med vores forudsigelsesforsøg i Azure Machine Learning og lade vores forsøg oprette og oplære en forudsigelsesmodel ud fra dine data. Hvis du vil dele dine data, skal du på siden **Opsætning af forudsigelse af forsinket betaling** vælge handlingen **Opret min model**. Herefter baseres forudsigelserne på din model og dine data, ikke på vores.  

> [!Note]
>   Kvaliteten af modellen er vigtig. Når vores forudsigelsesforsøg bruger dine data til at oplære en model, bestemmer det en kvalitetsværdi for modellen som en procentdel. Modelkvaliteten angiver, hvor nøjagtig modellens forudsigelser forventes at være. Flere faktorer kan have indflydelse på kvaliteten af en model. Disse faktorer kan f.eks. være, at der ikke var nok data, eller at dataene ikke var tilstrækkeligt varierede. Du kan få vist kvaliteten af den model, du aktuelt bruger, på siden **Opsætning af forudsigelse af forsinket betaling**. Du kan også angive en mindstegrænse for modelkvaliteten. Modeller med en kvalitetsværdi under grænsen giver ikke forudsigelser.  

### <a name="to-use-your-model-instead-of-ours"></a>Bruge din model i stedet for vores  
Hvis du opretter din egen model i Azure Machine Learning Studio uden at bruge funktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive dine legitimationsoplysninger, så [!INCLUDE[d365fin](includes/d365fin_md.md)] kan få adgang til modellen. Dette kan gøres på flere måder:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af forudsigelse af forsinket betaling**, og vælg derefter det relaterede link.  
2. Marker afkrydsningsfeltet **Brug mit Azure-abonnement**.  
3. I feltet **Valgt model** skal du vælge **Min model**.  
4. I oversigtspanelet **Legitimationsoplysninger for min model** skal angive API URL-adressen og API-nøgle til din model.  

## <a name="see-also"></a>Se også  
[Dokumentation til Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Tilpasse Business Central ved brug af udvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

