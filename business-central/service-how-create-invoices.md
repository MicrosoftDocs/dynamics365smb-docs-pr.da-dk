---
title: Opret fakturaer eller kreditnotaer for serviceydelser | Microsoft Docs
description: Få at vide, hvordan du opretter fakturaer, så du kan få betaling for dine ydelser.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 89b3baa44def2899dc3cbeff95c9e74f32deb63b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877491"
---
# <a name="create-service-invoices-or-credit-memos"></a>Oprette servicefakturaer eller -kreditnotaer
En nøgleegenskab i [!INCLUDE[d365fin](includes/d365fin_md.md)] er at gøre fakturering af serviceordrerne så let som mulig. Du kan sende en faktura til kunderne på et valgfrit tidspunkt eller oprette fakturaer periodisk.  
  
Hvis du vil oprette en faktura direkte, kan du bruge siden **Servicekontrakt**. Du kan også konfigurere systemet, så en feltservicetekniker kan oprette en faktura for service, der ikke er tilknyttet en kontrakt eller en ordre.  

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Sådan faktureres en servicekontrakt fra siden Servicekontrakt   
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret servicekontraktfakturaer**, og vælg derefter det relaterede link.  
2. Angiv de filtre, som du vil bruge.  
3. Angiv den dato, du vil bruge som bogføringsdato på de oprettede servicefakturaer, i feltet **Bogføringsdato**.  
4. I feltet **Fakturer til dato** skal du angive den dato, indtil hvilken du vil fakturere kontrakter. Kørslen vil omfatte kontrakter med de næste faktureringsdatoer op til den angivne dato.  
5. Vælg **Opret fakturaer** i feltet **Handling**.  
6. Vælg **OK** for at oprette servicefakturaerne.  
  
  > [!NOTE]  
  >  Du kan ikke oprette servicefakturaer for servicekontrakten, når værdien i feltet **Ændringsstatus** er indstillet til **Åben**.  
  
## <a name="to-post-an-invoice-from-a-service-order"></a>Sådan bogføres fakturaer fra serviceordrer  
I fremgangsmåden nedenfor er det beskrevet, hvordan du kan definere den del af en service, som kunden skal opkræves for.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Vælg den serviceordre, der skal faktureres, og åbn ordrekortet.  
3. Vælg handlingen **Servicelinjer**.  
4. Find de nødvendige poster, og angiv de antal, som du vil opkræve kunden for, i feltet **Fakturer (antal)**.  
  
   > [!NOTE]  
   >  Du kan fakturere kunden helt eller delvist for den registrerede service. Hvis du vælger at fakturere kunden fuldt ud, skal værdien i feltet **Lever (antal)** svare til værdien i feltet **Antal**. Du kan bogføre en komplet faktura sammen med en komplet leverance, og du kan bogføre en komplet faktura for en allerede bogført komplet leverance, der hverken er faktureret eller forbrugt tidligere.  
   >   
   >  Når du bogfører en delvis faktura, kan du angiv det antal, der skal faktureres, på to måder. Hvis du vil bogføre servicen med indstillingen **Lever og fakturer**, skal værdien i feltet **Fakturer (antal)** svare til værdien i feltet **Lever (antal)**. Hvis du vil fakturere en allerede bogført leverance, må det antal, der skal faktureres, ikke være højere end værdien i feltet **Leveret (antal)**.  
  
5. Vælg **Bogfør**, og derefter enten **Faktura** eller **Lever og fakturer**. Du kan finde flere oplysninger om disse indstillinger i [Bogføring i Service](service-service-posting.md).  
  
 Den servicelinje, du har markeret, er bogført. Du kan bogføre flere servicelinjer på én gang ved at markere dem alle og vælge **Bogfør**. Hvis du gør det, skal du sikre dig, at du har angivet alle nødvendige oplysninger på de linjer, du vil bogføre.  
  
 Når du bogfører ordren vha. indstillingen **Fakturer**, oprettes der en bogført servicefaktura sammen med tilsvarende poster, og de relevante felter på servicelinjerne i ordren opdateres. Derudover opdateres det eller de leverancedokumenter, der tidligere er bogført, med det antal, der er faktureret. Hvis du vælger bogføringsindstillingen **Lever og fakturer**, oprettes der også en bogført leverance i programmet.

## <a name="to-create-a-service-invoice-manually"></a>Sådan oprettes en servicefaktura manuelt  
Når du har bogført en serviceordre vha. indstillingen **Fakturer** eller **Lever og fakturer**, oprettes der automatisk en servicefaktura. Du kan dog alligevel få brug for at skulle udstede en faktura, der ikke er knyttet til hverken en servicekontrakt eller en serviceordre. I denne procedure redegøres for, hvordan du udsteder en faktura på samme tid, som kunden modtager servicen.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Opret en ny servicefaktura.  
3. Udfyld feltet **Nummer**. .  
  
    > [!NOTE]  
    >  Hvis du har defineret en nummerserie for servicefakturaer på siden **Serviceopsætning**, kan du trykke på Enter for at vælge det næste tilgængelige servicefakturanummer.  
  
4. I feltet **Debitornr.** skal du skrive nummeret på en kunde. Markér den relevante debitor på listen.  
  
    De debitorrelevante felter udfyldes automatisk med oplysninger fra **debitorkortet**.  
  
5. Angiv en dato i feltet **Bogføringsdato**. Datoen vises ved de bogførte varer. Dette felt udfyldes med den aktuelle arbejdsdato, men du kan ændre det manuelt.  
6. Udfyld feltet **Bilagsdato**. Den dato, du angiver her, vil blive vist på den udskrevne faktura og anvendes til beregning af forfaldsdatoen.  
7. Udfyld servicelinjerne i fakturaen. Udfyld felterne **Type**, **Nummer** og **Antal** for at registrere varer, ressourcer og omkostninger, der er anvendt til servicen. 

## <a name="to-invoice-posted-shipment-lines"></a>Sådan faktureres bogførte leverancelinjer  
Der kan være brug for at oprette en servicefaktura for den service, der allerede er leveret fra en eller flere serviceordrer, men som endnu ikke er faktureret eller forbrugt. Du kan udfylde fakturalinjerne automatisk med de valgte bogførte leverancelinjer for en bestemt kunde.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Opret fakturalinjer for services, der er leveret, men endnu ikke faktureret. Du kan også bruge handlingen **Hent salgsleverancelinjer** til at føje bogførte salgsleverancelinjer til fakturaen.  
4. Bogfør servicefakturaen.  
  
 Den bogførte servicefaktura og de tilsvarende poster oprettes. De leverancedokumenter, der tidligere er bogført, opdateres med de bogførte antal og de relevante antal på servicelinjerne i kildeordrerne.  

## <a name="to-create-a-combined-invoice"></a>Oprette en kombineret faktura  
Du kan fakturere kunden for service, der er leveret ifølge forskellige serviceordrer. Der oprettes fakturalinjer for varer, ressourcetimer eller omkostninger, der allerede er leveret fra forskellige serviceordrer men endnu ikke faktureret.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Hent salgsleverancelinjer**. På siden **Hent serviceleverancelinjer** vises alle leverede men ikke fakturerede linjer for den angivne kunde.  
4. Vælg linjerne for den service, der faktureres, og vælg derefter **OK** for at føje serviceleverancelinjerne til fakturaen.  

## <a name="to-create-a-service-credit-memo"></a>Sådan oprettes servicekreditnotaer  
Et servicekreditnotadokument bruges normalt, når en kunde returnerer en vare, men det kan også bruges til at yde kunden en vis kompensation eller til at korrigere en fejlbehæftet faktura.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekreditnotaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Felterne **Bogføringsdato** og **Bilagsdato** viser arbejdsdagen. Om nødvendigt kan du ændre den.    
4. På kreditnotalinjerne skal du angive oplysninger om de varer, der er blevet returneret eller fjernet, eller den kompensation, som kunden vil få.  

## <a name="see-also"></a>Se også
[Bogføre servicefakturaer](service-how-to-post-service-orders.md)  
[Konfigurere Service](service-setup-service.md)  
[Bogføring af tjenesten](service-service-posting.md)  
