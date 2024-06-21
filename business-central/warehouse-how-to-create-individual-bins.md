---
title: Oprette placeringer
description: 'Opret grupper af lignende placeringer i placeringsoprettelseskladden, Opret placeringer individuelt på lokationskortet eller automatisk i placeringsoprettelseskladden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '7368, 7369, 7370, 7371, 7372, 7373'
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Oprette placeringer

Den mest effektive metode til at oprette lagerplaceringer er at generere grupper af tilsvarende placeringer i oprettelseskladden, men du kan også oprette placeringer enkeltvist fra lokationskortet. Du kan også bruge en funktion på siden **Placeringsopr.kladde** til at oprette placeringer automatisk.  

## Sådan oprettes en placering ud fra lokationskortet

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  Marker den lokation, du vil oprette en placering fra, og vælg derefter handlingen **Placeringer**.  
3. Vælg handlingen **Ny**.
4. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Feltet Dedikeret

Feltet **Dedikeret** på siden **Placeringer** angiver, at antallet på placeringen er beskyttet mod pluk til andre behov. Men mængderne i dedikerede placeringer kan stadig reserveres. På samme måde medtages mængderne i dedikerede placeringer i feltet **Beholdning i alt** på siden **Reservation**.

Hvis du gør en placering dedikeret, resulterer det i den samme funktionalitet i grundlæggende lagerfunktioner som brugen af placeringstyper, der kun er tilgængeligt i avanceret logistik. Der er flere oplysninger i [Konfigurere placeringer](warehouse-how-to-set-up-bin-types.md).

### Eksempel

Et arbejdscenter med en placeringskode i feltet **Til-produktionsplaceringskode**. Produktionsordrekomponentlinjerne med den placeringskode kræver, at der anbringes komponenter, der trækkes forlæns, der. Indtil der forbruges komponenter fra placeringen, kan andre komponentbehov plukke eller forbruge fra placeringen, da de stadig betragtes som tilgængelige placeringsindhold. For at sikre, at placeringsindholdet kun er tilgængeligt for komponentbehov, der bruger produktionsplacering, skal du vælge feltet **Dedikeret** på linjen for placeringskoden.

> [!Caution]
> Varer på dedikerede placeringer er ikke beskyttet, når de plukkes og forbruges som produktions- eller montagekomponenter på siden **Pluk (lager)**. Du kan finde flere oplysninger i [Plukke til produktion eller montage i grundlæggende lageropsætninger](warehouse-how-to-pick-for-production.md)

## Sådan oprettes individuelle placeringer i placeringsoprettelseskladden

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Placeringsopr.kladde**, og vælg derefter det relaterede link.  
2.  Udfyld de felter på hver linje, der er nødvendige for at navngive og karakterisere de placeringer, som du opretter.  
3.  Vælg handlingen **Opret placeringer**.  

## Sådan oprettes placeringer automatisk i oprettelseskladden

Du skal på forhånd have taget stilling til, hvilken slags placeringer der er brug for på lagerstedet, og den mest praktiske varestrøm gennem lagerstedets fysiske struktur, før du begynder at oprette placeringer automatisk.  

> [!NOTE]  
> Når du først har brugt en placering, kan du ikke slette den, medmindre den er tom. Hvis du på et tidspunkt vil indføre et andet navngivningssystem til placeringerne, kan du dog bruge omposteringskladden til faktisk at flytte varer til et nyt placeringssystem. Det er derfor bedst, hvis du får sat placeringerne op korrekt allerede fra begyndelsen.  

Hvis du vil arbejde med siden **Placeringsopr.kladde**, skal du være oprettet som lagermedarbejder på det sted, hvor placeringerne findes. Du kan finde flere oplysninger i [Definere lagermedarbejdere](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Placeringsopr.kladde**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Beregn placeringer**.
3. På siden **Beregn placeringer** i feltet **Placeringsskabelonkode**, og vælg den placeringsskabelon, der skal bruges som model for de placeringer, som du opretter.
4.  Indtast en beskrivelse af placeringerne.  
5.  For at oprette placeringskoderne, skal du udfylde felterne **Fra nr.** og **Til nr.** i de tre kategorier, der vises på siden: **Hylde**, **Afsnit** og **Niveau.** Placeringskoden kan være på op til 20 tegn.  

    > [!NOTE]  
    >  Det antal tegn, som du har indtastet i de tre kategorier for et felt, f.eks. de tegn, som du har indtastet i de tre felter **Fra nr.**, plus eventuelle feltafgrænsere, skal være på 20 eller færre tegn.  

     Du kan bruge bogstaver i koden, men de anvendte bogstaver skal være de samme i felterne **Fra nr.** og **Til nr.** . Du kan f.eks. definere kodens hyldedel som **Fra nr. A01** og **Til nr. A10**. Programmet er ikke designet til at generere koder med bogstavserier, f.eks. fra A01 til F05.  

6.  Hvis du vil bruge et tegn, f.eks. bindestreg, til at adskille de kategorifelter, som du har defineret som en del af placeringskoden, skal du angive tegnet i feltet **Feltafgrænser**.  
7.  Marker feltet **Kontroller eksist. plac.**, hvis du ikke ønsker, at programmet skal oprette en linje for en placering, hvis denne allerede findes.  
8. Vælg knappen **OK**, når du er færdig med at udfylde felterne.

    Der oprettes en linje for hver placering i kladden. Du kan slette nogle af placeringerne, f.eks. hvis adgangen til en hylde er spærret.  

9. Vælg handlingen **Opret placeringer**, når du har slettet alle de unødvendige placeringer. Der oprettes nu placeringer for hver linje i kladden.  

Gentag processen, hvis det er nødvendigt med endnu et sæt placeringer, indtil du har oprettet alle placeringerne på lagerstedet.  

## Se også

[Oversigt over Warehouse Management](design-details-warehouse-management.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)    
[Montagestyring](assembly-assemble-items.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
