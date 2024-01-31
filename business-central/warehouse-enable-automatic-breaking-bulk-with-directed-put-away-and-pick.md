---
title: Nedbrydning med styret læg-på-lager og pluk
description: 'Få mere at vide om, hvordan du aktiverer automatisk nedbrydning med styret læg-på-lager og pluk samt nedbrydning i pluk, putaways, bevægelser m.m.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Aktivere automatisk nedbrydning med styret læg-på-lager og pluk

På lokationer, hvor der bruges styret læg-på-lager og pluk, kan [!INCLUDE[prod_short](includes/prod_short.md)] nedbryde større enheder til mindre enheder, når der oprettes lagerinstruktioner, som opfylder behovet for kildedokumenter, produktionsordrer eller interne pluk og læg-på-lager. Nedbrydning kan også betyde, at varer i mindre enheder bliver større, så de svarer til antallet af en større enhed i et kildedokument eller en produktionsordre.

## Nedbryde i pluk  

Hvis du vil lagre varer i flere forskellige enheder på en placering og lade dem blive automatisk kombineret efter behov i plukprocessen, skal du aktivere feltet **Tillad nedbrydning** på siden med lokationskortet. Når programmet skal fuldføre en opgave, leder [!INCLUDE [prod_short](includes/prod_short.md)] efter en vare fra samme enhed. Hvis der ikke findes en, foreslår [!INCLUDE [prod_short](includes/prod_short.md)], at du afbryder en større enhed i den måleenhed, der er nødvendig.  

Hvis systemet kun kan finde mindre enheder, foreslår [!INCLUDE [prod_short](includes/prod_short.md)], at du samler varerne for at opfylde antallet på leverance- eller produktionsordren. I praksis nedbryder det større enheder på kildedokumentet til mindre enheder, der kan plukkes.  

## Nedbryde i læg-på-lager  

I læg-på-lager-aktiviteter kommer [!INCLUDE [prod_short](includes/prod_short.md)] med forslag til placeringslinjer i læg-på-lager-enheden. F.eks. kan det foreslå dele, selvom varerne ankommer til en anden enhed.  

## Nedbryde i bevægelse  

[!INCLUDE [prod_short](includes/prod_short.md)] kan også nedbryde i genopfyldningsbevægelser, hvis indstillingen **Tillad nedbrydning** på siden **Beregn genopfyldning** er aktiveret.  

Du kan få vist resultaterne af konverteringsprocessen fra en enhed til en anden som midlertidige nedbrydningslinjer i læg-på-lager-, pluk- eller bevægelsesinstruktionerne.  

> [!NOTE]  
> Hvis du markerer feltet **Angiv nedbrydningsfilter** i lagerinstruktionshovedet, skjuler programmet nedbrydningslinjer, hver gang en større enhed vil blive brugt fuldstændig. Hvis en palle f.eks. består af 12 stykker, og du skal bruge alle 12, anmoder plukket dig om at tage 1 palle og placere 12 stykker der. Men hvis du kun skal plukke 9 styk, skjules nedbrydningslinjerne ikke, selvom du har valgt **nedbrydnings filter**-feltet. Linjerne er ikke skjulte, fordi du skal anbringe de resterende tre stykker et sted på lagerstedet.  

> [!NOTE]  
> Hvis enhederne skal fungere optimalt på lagerstedet – også i forbindelse med nedbrydningsfunktionen – bør du altid tilstræbe at:  
>
> - indstille basisenheden for en vare til at være den mindste enhed, som du forventer at skulle håndtere under lagerprocessen.  
> - Indstil alternative enheder for varen som flere forekomster af basisenheden.  

## Se også  

[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Konfigurere Warehouse Management](warehouse-setup-warehouse.md) 
[Montagestyring](assembly-assemble-items.md)
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]