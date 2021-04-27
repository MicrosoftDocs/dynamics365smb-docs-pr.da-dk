---
title: Opret fakturaer eller kreditnotaer for serviceydelser | Microsoft Docs
description: Få at vide, hvordan du opretter fakturaer, så du kan få betaling for dine ydelser.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 61890301542ea7225039341eb30fbf4e3dd035d0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778268"
---
# <a name="create-service-invoices-or-credit-memos"></a>Oprette servicefakturaer eller -kreditnotaer
En nøgleegenskab i [!INCLUDE[prod_short](includes/prod_short.md)] er at gøre fakturering af serviceordrerne så let som mulig. Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)], så en feltservicetekniker kan oprette en faktura for en service, der ikke er tilknyttet en kontrakt eller en ordre. Du kan også vælge at konfigurere [!INCLUDE[prod_short](includes/prod_short.md)], så du fakturerer servicekontrakter med jævne mellemrum. Fakturaperioden for den enkelte kontrakt definerer, hvor ofte kontrakten faktureres.

## <a name="to-invoice-several-service-contracts"></a>Sådan fakturerer du flere servicekontrakter

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret servicekontraktfakturaer**, og vælg derefter det relaterede link.  
2. Angiv de filtre, som du vil bruge.  
3. Angiv den dato, du vil bruge som bogføringsdato på de oprettede servicefakturaer, i feltet **Bogføringsdato**.  
4. I feltet **Fakturer til dato** skal du angive den dato, indtil hvilken du vil fakturere kontrakter. Kørslen vil omfatte kontrakter med de næste faktureringsdatoer op til den angivne dato.  
5. Vælg **Opret fakturaer** i feltet **Handling**.  
6. Vælg **OK** for at oprette servicefakturaerne.  
  
Du kan også fakturere en servicekontrakt direkte fra siden **Servicekontrakt**, hvis den næste faktureringsdato på kontrakten ligger tidligere end arbejdsdatoen.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Sådan faktureres en servicekontrakt fra siden Servicekontrakt   
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicekontakter**, og vælg derefter det relaterede link.  
2. Vælg den servicekontrakt, der skal faktureres, og åbn kontraktkortet.  
3. Vælg handlingen **Opret servicefaktura**. 
4. Vælg **Ja** for at oprette servicefakturaerne.  
  
  > [!NOTE]  
  > Du kan ikke oprette servicefakturaer for servicekontrakten, når værdien i feltet **Ændringsstatus** er indstillet til **Åben**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Sådan bogføres fakturaer fra serviceordrer  
I fremgangsmåden nedenfor er det beskrevet, hvordan du kan definere den del af en service, som kunden skal opkræves for.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Serviceordrer**, og vælg derefter det relaterede link.  
2. Vælg den serviceordre, der skal faktureres, og åbn ordrekortet.  
3. Vælg handlingen **Servicelinjer**.  
4. Find de nødvendige poster, og angiv de antal, som du vil opkræve kunden for, i feltet **Fakturer (antal)**.  
  
   > [!NOTE]  
   > Du kan fakturere kunden helt eller delvist for den registrerede service. Hvis du vælger at fakturere kunden fuldt ud, skal værdien i feltet **Lever (antal)** svare til værdien i feltet **Antal**. Du kan bogføre en komplet faktura sammen med en komplet leverance, og du kan bogføre en komplet faktura for en allerede bogført komplet leverance, der hverken er faktureret eller forbrugt tidligere.  
   >  
   > Når du bogfører en delvis faktura, kan du angiv det antal, der skal faktureres, på to måder. Hvis du vil bogføre servicen med indstillingen **Lever og fakturer**, skal værdien i feltet **Fakturer (antal)** svare til værdien i feltet **Lever (antal)**. Hvis du vil fakturere en allerede bogført leverance, må det antal, der skal faktureres, ikke være højere end værdien i feltet **Leveret (antal)**.  
  
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

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Sådan opretter du en faktura, der kombinerer bogførte leverancelinjer fra en eller flere serviceordrer 
Der kan være brug for at oprette en servicefaktura for den service, der allerede er leveret fra en eller flere serviceordrer, men som endnu ikke er faktureret eller forbrugt. Du kan udfylde fakturalinjerne automatisk med de valgte bogførte leverancelinjer for en bestemt kunde.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Opret fakturalinjer for services, der er leveret, men endnu ikke faktureret. Du kan også bruge handlingen **Hent salgsleverancelinjer** til at føje bogførte salgsleverancelinjer til fakturaen.  
4. Bogfør servicefakturaen.  
  
 Den bogførte servicefaktura og de tilsvarende poster oprettes. De leverancedokumenter, der tidligere er bogført, opdateres med de bogførte antal og de relevante antal på servicelinjerne i kildeordrerne.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]