---
title: Bogmærke sammenkæde til side eller rapport i rollecenter
description: 'Ved hjælp af bogmærkeikonet kan du tilføje en handling, der åbner en side eller rapport fra navigationsmenuen i rollecenteret.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: null
ms.date: 07/25/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Oprette et bogmærke til en side eller rapport i rollecenteret

Ved hjælp af bogmærkeikonet kan du tilføje en handling, der åbner en side eller rapport fra navigationsmenuen i rollecenteret. Med bogmærker kan du hurtigt få adgang til dit foretrukne indhold eller dine forretningsopgaver. Du tilføjer bogmærket fra målsiden eller rapporten, hvilket betyder det skærmbillede, som du ønsker, at sammenkæde i rollecenteret skal åbne.

Bogmærkeikonet vises i øverste højre hjørne af en side og også i vinduet **Fortæl mig**, hvor du effektivt kan indsætte bogmærker på flere sider eller rapporter. Hvis der allerede findes et bogmærke for siden, er ikonet mørkt, og der står "Med bogmærke" i værktøjstippet.

## Bogmærke målsiden

1. Åbn en hvilken som helst side, du vil have sammenkæde for, i rollecenteret.
2. Vælg ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er opkaldt efter siden, føjes nu til navigationsmenuen i rollecenteret.

## Bogmærke målrapporten

1. Åbn en rapportanmodningsside, som du vil have en sammenkæde til i rollecenteret.
2. Vælg ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er opkaldt efter rapporten, føjes nu til navigationsmenuen i rollecenteret.

## Oprette et bogmærke til en side eller rapport fra vinduet Fortæl mig det

1. Åbn vinduet **Fortæl mig**, og angiv f.eks. **Salgsordrer**.
2. Peg på søgeresultatet for siden eller rapporten **Salgsordrer**, og vælg derefter ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er opkaldt efter siden eller rapporten, føjes nu til navigationsmenuen i rollecenteret.

## Ofte stillede spørgsmål  

### Kan jeg omorganisere mine bogmærker?

Ja. Du kan tilpasse rollecenteret og flytte handlinger til en mere optimal rækkefølge eller flytte dem til eksisterende grupper eller undergrupper.  
Få at vide, hvordan du kan [Tilpasse dit arbejdsområde](ui-personalization-user.md).

### Hvordan fjerner jeg et bogmærke?

På målsiden eller rapporten skal du vælge bogmærkeikonet igen for at fjerne den involverede handling fra rollecenteret. Du kan også tilpasse rollecenteret og midlertidigt skjule handlinger uden at fjerne dem helt.

### Hvor finder jeg mine bogmærker?

Når du føjer et bogmærke til en side eller rapport, føjes den nye handling til den øverste navigationsmenu på den aktuelle startskærm (rollecenter). Hvis du har mange handlinger, kan det være nødvendigt at aktivere knappen **Flere** for at vise dem alle, fordi den nye handling altid tilføjes i slutningen af disse handlinger.
<!-- Should we add a screenshot here? -->

### Hvorfor har jeg ikke et bogmærke-ikon? Gik noget galt?

Muligheden for at bogmærke en side eller en rapport er en af mange bruger tilpasningsfunktioner i Business Central. Hvis bogmærkeikonet ikke vises, er det sandsynligt, at administratoren har deaktiveret brugertilpasning.

### Hvorfor kan jeg ikke bogmærke bestemte sider eller rapporter?

Ikke alle sider og rapporter kan gives et bogmærke. Når en side eller en rapport køres i en særlig kontekst, der er omfattet af forretningsprogrammet, vises bogmærkeikonet ikke. F.eks. kan sider, der ikke findes i vinduet **Fortæl mig**, men startes fra andre steder, ikke vise et bogmærkeikon. På samme måde vil rapportanmodningssider, der kun bruges til at indsamle filtre uden at køre rapporten, ikke vise et bogmærkeikon.

  Se tekniske oplysninger om [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) og [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

### Når jeg rydder min tilpasning, bliver mine bogmærker så også ryddet?

Ja. Bogmærker findes i navigationsmenuen. Hvis du fjerner ændringer i navigationsmenuen fra en hvilken som helst side eller rydder alle tilpasninger i rollecenteret, fjernes alle dine nye handlinger permanent.

### Hvorfor bliver bogmærkeikonet ved med at angive, at det stadig ikke er bogmærket?

Når du tilføjer et bogmærke, føjes den nye handling til navigationsmenuen i rollecenteret, og efterfølgende besøg på siden eller rapporten viser et mørkt bogmærkeikon. Hvis du tilpasser rollecenteret og omorganiserer handlingerne ved at flytte dem ind i grupper, er bogmærkeikonet ikke længere mørkt, og du kan føje endnu et bogmærke til den samme side eller rapport. På den måde kan du tilføje flere handlinger på den samme side eller rapport og kategorisere dem i forskellige grupper.

### Hvorfor viser min sammenkæde til en rapport en anden rapport?

Nogle rapporter kan erstattes af andre rapporter, når du har anvendt en udvidelse på Business Central. Når erstatningen finder sted, opdateres teksten til den nye handling ikke, og navnet på den oprindelige rapport vises fortsat, men der navigeres til den nye rapport. Hvis du vil rette teksten til den nye handling, kan du fjerne den nye handling og tilføje den igen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

### Er bogmærker tilgængelige for XML-porte?

Nummer På dette tidspunkt er det ikke muligt at føje handlinger til åbne XMLporte fra brugergrænsefladen.

### Vil mine bogmærker blive oversat, når jeg ændrer mit sprog i Business Central?

Når du tilføjer en ny handling, bogmærkes oversat tekst, der var tilgængelig på det tidspunkt, hvor bogmærket blev oprettet. Hvis ny, oversat tekst tilføjes senere, vil den nye handling ikke indeholde de nyere oversættelser.

### Hvorfor kan jeg ikke tilføje tekst på en side direkte efter at have åbnet den med bogmærket?

Når der oprettes et bogmærke til en side, åbnes siden altid i visningstilstand fra bogmærket, selvom den var i redigeringstilstand, da den blev bogmærket. Hvis du vælger indstillingen **Foretag ændringer på side**-ikonet, ![vises blyantsikonet for at redigere siden.](media/edit-pencil.png) giver dig mulighed for at tilføje tekst i de felter, der kan redigeres.

## Se også

[Tilpas arbejdsområdet](ui-personalization-user.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]