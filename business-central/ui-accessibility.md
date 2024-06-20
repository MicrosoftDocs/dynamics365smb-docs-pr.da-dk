---
title: Hjælpefunktioner
description: Denne artikel indeholder oplysninger om tastaturgenveje og andre hjælpefunktioner i Business central for personer med handicap.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Tilgængelighedsfunktioner og tastaturgenveje

Dette emne indeholder oplysninger om de funktioner, der gør [!INCLUDE[prod_short](includes/prod_short.md)] direkte tilgængelig for personer med handicap. [!INCLUDE[prod_short](includes/prod_short.md)] understøtter følgende funktioner i Hjælp til handicappede:  

- Tastaturgenveje. Se [Tastaturgenveje](keyboard-shortcuts.md).
- Håndbevægelser til touch og pen til tablet og telefoner. Se [Håndbevægelser til touch og pen](touch-gestures.md).
- Navigation  
- Overskrifter  
- Alternativ tekst til billeder og hyperlinks  
- Understøttelse af almindelige hjælpeteknologier 
- Zoome ind og ud på en side
- Værktøjstip om elementer i brugergrænsefladen

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="Navigation"></a> Navigation
  
Du kan bruge forskellige kombinationer af tab, Skift og piletaster på tastaturet til at flytte mellem elementerne på en side. Elementer omfatter handlinger, felter og kolonner, dele og andre kontrolelementer. Vælg generelt <kbd>Tab</kbd> eller <kbd>Skift</kbd>+<kbd>Tab</kbd> for at flytte til næste eller forrige element.

Når du fokuserer på et område, der indeholder handlinger, f. eks. navigationspanelet øverst i Rollecenter eller handlingslinje på andre sider, skal du bruge piletasterne til at flytte gennem de forskellige handlinger og grupper. Vælg <kbd>Enter</kbd> på en gruppe for at åbne dens underliggende handling, og fortsæt derefter med at bruge piletasterne. Vælg <kbd>Tab</kbd> eller <kbd>Skift</kbd>+<kbd>Tab</kbd> for at gå ud af handlingsområdet.

Ved hjælp af fanerækkefølgen kan du også skifte mellem hovedbrowsersiden og dialogbokse, der anmoder om bekræftelse, for eksempel logonsiden.  

## <a name="Headings"></a> Overskrifter i indhold

HTML-kilden til [!INCLUDE[prod_short](includes/prod_short.md)]-indhold bruger koder til at hjælpe brugerne af hjælpeteknologien med at forstå strukturen og indholdet af siden. På oversigtssider defineres kolonnerne f.eks. i TH-koder, og kolonneoverskrifterne oprettes med TITEL-attributten i koden. Tekster til elementer som oversigtspaneler, faktabokse og felter er inkluderet i overskriftskoder (H1 H2, H3 og H4).  

## <a name="Images"></a> Billede og links

En beskrivende tekst til billeder er angivet med attributten ALT i koden IMG. En beskrivende tekst til hyperlinkser angivet med attributten titel i koden A.  

## <a name="AssistiveTech"></a> Hjælpeteknologier

[!INCLUDE[prod_short](includes/prod_short.md)] understøtter forskellige hjælpeteknologier, f.eks. stor kontrast, skærmlæsere og talegenkendelsessoftware. Nogle hjælpeteknologier fungerer ikke sammen med bestemte elementer på [!INCLUDE[prod_short](includes/prod_short.md)]-sider.  

## <a name="zoom"></a> Zoom

De fleste browsere bruger standardtastaturgenveje til at zoome ind og ud på den aktuelle side. Disse tastaturgenveje er ikke specifikke for [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerer, når du bruger [!INCLUDE [prod_short](includes/prod_short.md)] i en browser. Du kan få vist en liste over understøttede tastaturgenveje under [Tastaturgenveje til zoom ind og ud](keyboard-shortcuts.md#zoomshortcuts).

## Værktøjstips

Værktøjstip er tilgængelige på de fleste elementer i brugergrænsefladen, f. eks. sidefelter og kolonner, handlinger, køindikatorer og diagrammer. Et værktøjstip giver ekstra tekst, der forklarer et element, så du bedre kan forstå formålet. 

Der kan opnås adgang til værktøjstip på forskellige måder, afhængigt af klienten (internettet eller mobil) og den enhed, som du arbejder med. Brug følgende tabel som reference. Nogle værktøjstip kan læses af skærmlæsere. Hvis det er tilfældet, kan du få adgang til værktøjstips som beskrevet i tabellen og derefter bruge skærmlæseren til at navigere til værktøjstippet på samme måde, som du kan med alle andre elementer.

#### Få adgang til værktøjstips

|Element|Musehandling for webklient|Genvejstast for webklient|Berøringsbevægelse på tablet/telefon for mobilapp|Skærmlæser-understøttelse|
|-------|-----------------|------------|--------------------------|---------------------|
|Sidefelter og kolonneoverskrifter|Holde markøren over eller klikke på felttitlen eller kolonneoverskriften|Flyt fokus til felt- eller kolonneoverskriften, og vælg <kbd>Alt</kbd>+<kbd>Pil op</kbd>-tasterne|Tryk på felttitlen |ja|
|Diagramelementer, f. eks. en søjle, streg, cirkeludsnit|Placer markøren over elementet|Flytte fokus til et element, f. eks. ved hjælp af piletasterne|Tryk og hold elementet nede|ja|
|Handlinger|Placer markøren over elementet|ingen|ingen |nummer|
|Stikordsfliser|Placer markøren over flisen |ingen|ingen|nummer|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## Flere oplysninger om tilgængelighedsfunktioner

Du kan finde flere oplysninger om tilgængelighedsfunktioner i Microsoft-produkter og hjælpeteknologier på webstedet [Microsoft Hjælp til handicappede](https://go.microsoft.com/fwlink/?LinkId=262160).

## Se også

[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ofte stillede spørgsmål](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
