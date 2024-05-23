---
title: Oprette fakturaer eller -kreditnotaer for tjenester
description: 'Få at vide, hvordan du opretter fakturaer og kreditnotaer for dine services.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Oprette servicefakturaer eller kreditnotaer

En nøgleegenskab i [!INCLUDE[prod_short](includes/prod_short.md)] er at gøre fakturering af serviceordrerne så let som mulig. Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)], så en feltservicetekniker kan oprette en faktura for en service, der ikke er tilknyttet en kontrakt eller en ordre. Du kan også vælge at konfigurere [!INCLUDE[prod_short](includes/prod_short.md)], så du fakturerer servicekontrakter med jævne mellemrum. Fakturaperioden for den enkelte kontrakt definerer, hvor ofte kontrakten faktureres.

## Sådan fakturerer du flere servicekontrakter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opret servicekontraktfakturaer**, og vælg derefter det relaterede link.  
2. Angiv de filtre, som du vil bruge.  
3. Angiv den dato, du vil bruge som bogføringsdato på de oprettede servicefakturaer, i feltet **Bogføringsdato**.  
4. I feltet **Fakturer til dato** skal du angive den dato, indtil hvilken du vil fakturere kontrakter. Kørslen vil omfatte kontrakter med de næste faktureringsdatoer op til den angivne dato.  
5. Vælg **Opret fakturaer** i feltet **Handling**.  
6. Vælg **OK** for at oprette servicefakturaerne.  
  
Du kan også fakturere en servicekontrakt direkte fra siden **Servicekontrakt**, hvis den næste faktureringsdato på kontrakten ligger tidligere end arbejdsdatoen.

## Sådan faktureres en servicekontrakt fra siden Servicekontrakt   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekontrakter**, og vælg derefter det relaterede link.  
2. Vælg den servicekontrakt, der skal faktureres, og åbn kontraktkortet.  
3. Vælg handlingen **Opret servicefaktura**. 
4. Vælg **Ja** for at oprette servicefakturaerne.  
  
  > [!NOTE]  
  > Du kan ikke oprette servicefakturaer for servicekontrakten, når værdien i feltet **Ændringsstatus** er indstillet til **Åben**.  

## Sådan bogføres fakturaer fra serviceordrer  

I fremgangsmåden nedenfor er det beskrevet, hvordan du kan definere den del af en service, som kunden skal opkræves for.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Vælg den serviceordre, der skal faktureres, og åbn ordrekortet.  
3. Vælg handlingen **Servicelinjer**.  
4. Find de nødvendige poster, og angiv de antal, som du vil opkræve kunden for, i feltet **Fakturer (antal)**.  
  
   > [!NOTE]  
   > Du kan fakturere kunden helt eller delvist for den registrerede service. Hvis du vælger at fakturere kunden fuldt ud, skal værdien i feltet **Lever (antal)** svare til værdien i feltet **Antal**. Du kan bogføre en komplet faktura sammen med en komplet leverance, og du kan bogføre en komplet faktura for en allerede bogført komplet leverance, der ikke er faktureret eller forbrugt.  
   >  
   > Når du bogfører en delvis faktura, kan du angiv det antal, der skal faktureres, på to måder. Hvis du vil bogføre servicen med indstillingen **Lever og fakturer**, skal værdien i feltet **Fakturer (antal)** svare til værdien i feltet **Lever (antal)**. Hvis du vil fakturere en allerede bogført leverance, må det antal, der skal faktureres, ikke være højere end værdien i feltet **Leveret (antal)**.  
  
5. Vælg **Bogfør**, og derefter enten **Faktura** eller **Lever og fakturer**. Flere oplysninger i [Bogføring i Service](service-service-posting.md).  
  
 Den servicelinje, du har markeret, er bogført. Du kan bogføre flere servicelinjer på én gang ved at markere dem og vælge **Bogfør**. Hvis du gør det, skal du sørge for at angive alle nødvendige oplysninger på linjerne.  
  
 Når du bogfører ordren vha. indstillingen **Fakturer**, oprettes der en bogført servicefaktura sammen med tilsvarende poster, og de relevante felter på servicelinjerne i ordren opdateres. Derudover opdateres leverancedokumenter, der tidligere er bogført, med det fakturerede antal. Hvis du vælger bogføringsindstillingen **Lever og fakturer**, oprettes der også en bogført leverance i programmet.

## Sådan oprettes en servicefaktura manuelt  

Når du har bogført en serviceordre vha. indstillingen **Fakturer** eller **Lever og fakturer**, oprettes der automatisk en servicefaktura. Du kan dog alligevel få brug for at skulle udstede en faktura, der ikke er knyttet til en servicekontrakt eller en serviceordre. I denne procedure redegøres for, hvordan du udsteder en faktura på samme tid, som kunden modtager servicen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Opret en ny servicefaktura.  
3. Udfyld feltet **Nummer**. .  
  
    > [!NOTE]  
    >  Hvis du har defineret en nummerserie for servicefakturaer på siden **Serviceopsætning**, kan du trykke på **Enter** for at vælge det næste tilgængelige servicefakturanummer.  
  
4. I feltet **Debitornr.** skal du skrive nummeret på en kunde. Markér den relevante debitor på listen.  
  
    De debitorrelevante felter udfyldes automatisk med oplysninger fra **debitorkortet**.  
  
5. Angiv en dato i feltet **Bogføringsdato**. Datoen vises ved de bogførte varer. Feltet viser den aktuelle arbejdsdato, men du kan ændre datoen.  
6. I feltet **Bilagsdato** skal du angive en dato, der vises på den udskrevne faktura og anvendes til beregning af forfaldsdatoen.  
7. Udfyld servicelinjerne i fakturaen. Udfyld felterne **Type**, **Nummer** og **Antal** for at registrere varer, ressourcer og omkostninger, der er anvendt til servicen.

## Sådan opretter du en faktura, der kombinerer bogførte leverancelinjer fra en eller flere serviceordrer 

Der kan være brug for at oprette en servicefaktura for en service, der allerede er leveret, ud fra en eller flere serviceordrer, men som endnu ikke er faktureret eller forbrugt. Du kan udfylde fakturalinjerne automatisk med de valgte bogførte leverancelinjer for en bestemt kunde.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicefakturaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Opret fakturalinjer for services, der er leveret, men endnu ikke faktureret. Du kan også bruge handlingen **Hent salgsleverancelinjer** til at føje bogførte salgsleverancelinjer til fakturaen.  
4. Bogfør servicefakturaen.  
  
 Den bogførte servicefaktura og de tilsvarende poster oprettes. De leverancedokumenter, der tidligere er bogført, opdateres med de bogførte antal og antallene på servicelinjerne i kildeordrerne.  

## Sådan oprettes servicekreditnotaer  

Du bruger typisk et servicekreditnotadokument, når en kunde returnerer en vare. Du kan dog også bruge det til at refundere en kunde eller til at rette en faktura, der var en fejl.  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Servicekreditnotaer**, og vælg derefter det relaterede link.  
2. Udfyld felterne på linjen efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Felterne **Bogføringsdato** og **Bilagsdato** viser arbejdsdagen. Om nødvendigt kan du ændre den.    
4. På kreditnotalinjerne skal du angive oplysninger om de varer, der er blevet returneret eller fjernet, eller den kompensation, som kunden vil få.  

## Rette fejl i servicefakturaer

Du kan slette servicefakturaer, hvor der er tilknyttet serviceposter. Det betyder, at du kan rette fejl eller foretage ændringer i servicefakturaer uden at sidde fast eller miste data. Hvis du f.eks. glemmer at tildele en produktbogføringsgruppe til en finanskonto, kan du tilføje den senere og oprette servicefakturaen igen.

Brug handlingen :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="ikonet for handlingen Slet"::: til at slette en servicefaktura. 

Når du sletter en servicefaktura, sker der følgende:

* Bogføre en korrigeret servicepost
* Gendanne faktureringsdatoen og -perioden i kontrakten, så du kan oprette fakturaen igen.

> [!NOTE]
> Du kan genindlæse flere fakturaer, men det skal ske i rækkefølge med start fra den sidste faktura.
>
> Du kan ikke slette en servicefaktura, hvis dens oplysninger, f.eks. faktureringsperioden eller til/fra-knappen **Forudbetalt**, er blevet ændret i den relaterede servicekontrakt. Sørg for at slette fakturaer, før du ændrer indstillinger i servicekontrakten.

## Se også

[Bogføre servicefakturaer](service-how-to-post-service-orders.md)  
[Konfigurere Service](service-setup-service.md)  
[Bogføre service](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]