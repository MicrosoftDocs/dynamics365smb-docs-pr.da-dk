---
title: 'Fremgangsmåde: Oprette serviceartikler'
description: 'Læse om de forskellige måder, du kan oprette serviceartikler på i Business central, f. eks. i en serviceordre eller ved levering af varer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Opret serviceartikler

I [!INCLUDE[prod_short](includes/prod_short.md)] refererer termen "serviceartikel" til udstyr eller varer, der kræver service. Når du opretter en serviceordre, kan du angive de varer, der har brug for service. I ordren kan du knytte en serviceartikel til en vare på lageret eller en serviceartikelgruppe.

Når du modtager en vare, der kræver service, kan du registrere den som en serviceartikel. Dette kan gøres på flere måder. Du kan f.eks. oprette en serviceartikel på siden **Serviceartikler** eller som en del af en anden proces, f.eks. når du arbejder med en serviceordre.

## Oprette en serviceartikel

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceartikler** og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Sådan oprettes serviceartikler fra serviceordrer

Når du modtager artikler, som du vil registrere som serviceartikler, kan du oprette dem som serviceartikler på siderne **Serviceordre** eller **Servicetilbud**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Vælg handlingen **Opret serviceartikel**.  

    Der tildeles et nummer til serviceartiklen, og der oprettes et serviceartikelkort. Feltet **Serviceartikelnr.** udfyldes med nummeret på den nye serviceartikel.

## Oprette en serviceartikel ved levering af varer

Når du leverer varer enten ved at bogføre salgsordrer eller salgsfakturaer, registreres de leverede varer automatisk som serviceartikler, hvis følgende betingelser er opfyldt. Varerne skal høre til en serviceartikelgruppe, hvor afkrydsningsfeltet **Opret serviceartikel** er markeret. Hvis varerne har serienumre registreret på siden Varesporingslinje, kopieres disse oplysninger automatisk til feltet **Serienr.** på serviceartikelkortet ved oprettelse af serviceartikler.  

Nedenstående fremgangsmåde viser, hvordan du kan oprette serviceartikler, når du leverer varer i salgsordrer.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Åbn den relevante Salgsordre.  
3. Vælg handlingen **Bogfør** eller **Bogfør og udskriv**.  
4. Vælg handlingen **Lever** eller **Lever og fakturer**.  
5. Der oprettes automatisk serviceartikler for varerne i ordren, forudsat at disse hører til en serviceartikelgruppe, som du har defineret for at oprette serviceartikler. Hvis der er registreret specifikke serienumre på siden **Varesporingslinjer**, tildeles de til disse serviceartikler.  

> [!NOTE]  
> Hvis en vare er en stykliste, og du har udfoldet styklisten, bliver styklistevarerne behandlet på samme måde som almindelige varer. Der oprettes serviceartikler baseret på samme betingelser for serviceartikelgruppe og eventuelt betingelser for serienummer. Hvis der oprettes en serviceartikel for en udfoldet styklistevare, som består af andre styklistekomponenter, oprettes disse varer desuden som serviceartikelkomponenter for den udfoldede styklisteartikel.  
>
> Hvis varen er en stykliste, og du ikke har udfoldet styklisten, oprettes der en serviceartikel til den på de samme betingelser for serviceartikelgruppen og eventuelt betingelsen for serienumre.  

## Sådan indsættes startgebyrer for serviceartikler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopgaver** og vælg derefter det relaterede link.
2. Vælg handlingen **Varekladde**.
3. Vælg servicelinjen, og vælg derefter **Handlinger**, vælg **Funktioner**, og vælg derefter handlingen **Indsæt startgebyr**.  

    Der indsættes en servicelinje af typen **Omkostning** med startgebyr. Startgebyret gælder den valgte serviceartikel.

## Spærre varer, varevarianter eller bestemte serviceartikler

Du kan forhindre, at varer, varevarianter eller serviceartikler bruges i servicestyringstransaktioner, f.eks. servicekontrakter, serviceordrer og servicefakturaer. Dette kan være nyttigt, hvis du vil begrænse tilgængeligheden af visse varer eller serviceartikler til serviceformål, f.eks. på grund af ophørt support, begrænset lagerbeholdning eller kontraktlige aftaler.

Hvis du vil spærre en vare eller en varevariant, så den ikke kan bruges i servicestyringstransaktioner, skal du slå til/fra-knappen **Servicen er spærret** til på siden **Varekort**, **Varevarianter** og **Kort med varevariant**. Du kan også angive dette felt på siden **Vareskabelon**, hvorefter det kopieres til de varer, der oprettes ud fra skabelonen.

Når der er spærret for service for en vare eller varevariant, kan den ikke vælges på følgende sider:

- Servicelinje (undtagen servicekreditnotaer, hvor du får vist en meddelelse om, at varen eller varianten er spærret, men tilladt i denne type dokument)
- Servicevare
- Servicekontraktlinje
- Standardservicelinje

Hvis du manuelt angiver et varenummer eller en variant, der er spærret, får du vist fejlmeddelelsen "Feltet indeholder en værdi, der ikke blev fundet i den relaterede tabel".

Hvis du derudover har servicekontrakter, servicekontrakttilbud eller serviceordrer, der omfatter spærrede serviceartikler eller varevarianter, kan du ikke bruge følgende handlinger:

- **Lås** eller **Opret kontrakt** på siden **Servicekontrakttilbud**.
- **Lås kontrakt**, **Underskriv kontrakt**, **Opret kontraktserviceordrer** eller **Opret kontraktfakturaer** på siden **Servicekontrakt**.
- **Lav ordre** på siden **Servicetilbud**.
- **Frigiv til levering** eller **Bogfør** på siden **Serviceordre**.
- **Bogfør** på siden **Servicefaktura**.

### Spærre en serviceartikel

Hvis du vil spærre en serviceartikel, så den ikke kan bruges i servicestyringstransaktioner, skal du vælge en af følgende indstillinger i feltet **Spærret** på siden **Serviceartikelkort**:

- **Servicekontrakt**: Spær serviceartiklen, så den ikke kan bruges i servicekontrakter og servicekontrakttilbud, men kan bruges i serviceordrer eller andre servicedokumenter.
- **Alle**: Spær serviceartiklen, så den ikke kan bruges i servicestyringstransaktioner, herunder servicekontrakter, serviceordrer og andre servicedokumenter.

Når en serviceartikel er spærret, kan du ikke vælge den på følgende sider:

- Servicekontraktlinje (hvis spærret for servicekontrakt eller alle)
- Serviceartikellinje (undtagen servicekreditnotaer, hvis spærret for alle)

Hvis du manuelt angiver et serviceartikelnummer for en spærret serviceartikel, får du vist fejlmeddelelsen "Feltet indeholder en værdi, der ikke blev fundet i den relaterede tabel".

Hvis du derudover har servicekontrakter, servicekontrakttilbud eller serviceordrer, der omfatter spærrede serviceartikler, kan du ikke bruge følgende handlinger:

- **Lås** og **Lav kontrakt** på siden **Servicekontrakttilbud** (hvis spærret for servicekontrakt eller alle).
- **Lås kontrakt** og **Underskriv kontrakt** eller **Skift debitor** på siden **Servicekontrakt** (hvis spærret for servicekontrakt eller alle).
- **Lav ordre** på **Servicetilbud** (hvis spærret for alle).
- **Frigiv til levering**, **Bogfør** på siden **Serviceordre** (hvis spærret for alle). Hvis serviceordredokumenter indeholder flere serviceartikler, og nogle er spærret og andre ikke er, kan du frigive og bogføre linjer, der ikke er spærret. Overvej, om du vil slå til/fra-knappen **Én serviceart.linje pr. ordre** til på siden **Serviceopsætning**.
- **Bogfør** på siden **Servicefaktura** (hvis spærret for alle).

Du kan også få vist de spærrede serviceartikler ved at anvende et filter på følgende rapporter:

- Serviceartikler (rapport 5935)
- Serviceart. - garanti udløbet (rapport 5937)
- Serviceavance (serviceart.) (rapport 5938)

### Dataopgradering

Denne funktion kræver ikke yderligere konfiguration. Men hvis du opgraderer [!INCLUDE [prod_short](includes/prod_short.md)], skal du være opmærksom på følgende:

- Hvis du har varer, varevarianter eller vareskabeloner, hvor til/fra-knappen **Salg er spærret** er slået til, slås feltet **Servicen er spærret** også til for disse poster under opgraderingen. Dette sikrer, at den eksisterende logik for spærring af salg også gælder for servicestyringstransaktioner.
- Data opgraderes kun, hvis du har mindst én serviceartikel i virksomheden, hvilket betyder, at du bruger servicestyringsfunktionen og har brug for dataopgraderingen. Hvis du ikke har serviceartikler, springes dataopgraderingen over, og til/fra-knappen **Servicen er spærret** er som standard slået fra for alle varer, varevarianter og vareskabeloner.

## Se også

[Konfigurere serviceartikler og serviceartikelkomponenter](service-how-setup-service-items.md)  
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
