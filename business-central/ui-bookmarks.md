---
title: Bogmærke til en side eller en rapport i rollecenteret
description: 'Med bogmærkeikonet kan du tilføje en handling, der åbner en side eller en rapport fra navigationsmenuen i dit rollecenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Bogmærke en side eller en rapport i rollecenteret
Med bogmærkeikonet kan du tilføje en handling, der åbner en side eller en rapport fra navigationsmenuen i dit rollecenter. Med bogmærker kan du hurtigt få adgang til dit foretrukne indhold eller dine forretningsopgaver. Du kan tilføje bogmærket fra målsiden eller rapporten, dvs. det skærmbillede, du vil have linket i rollecenteret til at åbne.

Bogmærkeikonet vises i øverste højre hjørne af en side og også i vinduet **Fortæl mig**, hvor du effektivt kan indsætte bogmærker på flere sider eller rapporter. Hvis der allerede findes et bogmærke for siden, er ikonet mørkt, og der står "Med bogmærke" i værktøjstippet.

## <a name="to-bookmark-the-target-page"></a>Sådan føjes et bogmærke til målsiden
1. Åbn en side, som du vil oprette et link til, i dit rollecenter.
2. Vælg ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er navngivet efter siden, føjes nu til navigationsmenuen i dit rollecenter.

## <a name="to-bookmark-the-target-report"></a>Sådan føjes et bogmærke til målrapporten
1. Åbn en rapportanmodningsside, som du vil oprette et link til, i dit rollecenter.
2. Vælg ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er navngivet efter rapporten, føjes nu til navigationsmenuen i dit rollecenter.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Sådan oprettes et bogmærke til en side eller en rapport fra vinduet Fortæl mig
1. Åbn vinduet **Fortæl mig**, og angiv f.eks. **Salgsordrer**.
2. Peg på søgeresultatet for siden eller rapporten **Salgsordrer**, og vælg derefter ikonet ![Bogmærke.](media/ui_bookmark_icon.png "Bogmærke") ikon.

En handling, der er navngivet efter siden eller rapporten, føjes nu til navigationsmenuen i dit rollecenter.


## <a name="frequently-asked-questions"></a>Ofte stillede spørgsmål

- **Kan jeg omarrangere mine bogmærker?**  
Ja. Du kan tilpasse rollecenteret og placere handlinger i en mere optimal rækkefølge eller flytte dem til eksisterende grupper eller undergrupper.  
Få at vide, hvordan du kan [Tilpasse dit arbejdsområde](ui-personalization-user.md).

- **Hvordan fjerner jeg et bogmærke?**  
På målsiden eller -rapporten skal du vælge bogmærkeikonet igen for at fjerne den pågældende handling fra dit rollecenter. Du kan også tilpasse rollecenteret og midlertidigt skjule handlinger uden at fjerne dem fuldstændigt.

- **Hvor finder jeg mine bogmærker?**  
Når du føjer et bogmærke til en side eller en rapport, føjes den nye handling til den øverste navigationsmenu på den aktuelle startskærm (rollecenter). Hvis du har mange handlinger, kan det være nødvendigt at aktivere knappen **Flere** for at vise dem alle, fordi den nye handling altid tilføjes i slutningen af disse handlinger.
<!-- Should we add a screenshot here? -->

- **Jeg har ikke noget bogmærkeikon. Er der noget galt?**  
Muligheden for at bogmærke en side eller en rapport er en af mange bruger tilpasningsfunktioner i Business Central. Hvis bogmærkeikonet ikke vises, er det sandsynligt, at administratoren har deaktiveret brugertilpasning.

- **Hvorfor kan jeg ikke bogmærke bestemte sider eller rapporter?**  
Ikke alle sider og rapporter kan gives et bogmærke. Når en side eller en rapport køres i en særlig kontekst, der er omfattet af forretningsprogrammet, vises bogmærkeikonet ikke. F.eks. kan sider, der ikke findes i vinduet **Fortæl mig**, men startes fra andre steder, ikke vise et bogmærkeikon. På samme måde vil rapportanmodningssider, der kun bruges til at indsamle filtre uden at køre rapporten, ikke vise et bogmærkeikon.

  Se tekniske oplysninger om [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) og [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Når mine personlige indstillinger fjernes, slettes mine bogmærker så også?**  
Ja. Bogmærker findes i navigationsmenuen. Hvis du rydder ændringer i navigationsmenuen fra en side eller rydder alle tilpasninger i rollecenteret, fjernes alle dine nye handlinger permanent.

- **Hvorfor viser bogmærkeikonet fortsat, at der ikke er oprettet et bogmærke?**  
Når du tilføjer et bogmærke, føjes den nye handling til navigationsmenuen i rollecenteret og efterfølgende besøg på siden eller rapporten viser et mørkt bogmærkeikon. Hvis du tilpasser rollecenteret og reorganiserer dine handlinger ved at flytte dem ind i grupper, vil bogmærke ikonet ikke længere være mørkt, og du kan tilføje endnu et bogmærke til den samme side eller rapport. På den måde kan du tilføje flere handlinger på den samme side eller rapport og kategorisere dem i forskellige grupper.

- **Hvorfor viser linket til en rapport en anden rapport?**  
Nogle rapporter kan erstattes af andre rapporter, når du har anvendt en udvidelse på Business Central. Når erstatningen finder sted, opdateres teksten til den nye handling ikke, og navnet på den oprindelige rapport vises fortsat, men der navigeres til den nye rapport. Hvis du vil rette teksten til den nye handling, kan du fjerne den nye handling og tilføje den igen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Er der muligt at føje bogmærker til XMLporte?**  
Nummer På dette tidspunkt er det ikke muligt at føje handlinger til åbne XMLporte fra brugergrænsefladen.

- **Bliver bogmærkerne oversat, når jeg ændrer sproget i Business Central?**  
Når du tilføjer en ny handling, bogmærkes oversat tekst, der var tilgængelig på det tidspunkt, hvor bogmærket blev oprettet. Hvis ny, oversat tekst tilføjes senere, vil den nye handling ikke indeholde de nyere oversættelser.

- **Hvorfor kan jeg ikke tilføje tekst på en side direkte, når den er åbnet med bogmærket?**<br> Når der oprettes et bogmærke til en side, åbnes siden altid i visningstilstand fra bogmærket, selvom den var i redigeringstilstand, da den blev bogmærket. Hvis du vælger indstillingen **Foretag ændringer på side**-ikonet, ![vises blyantsikonet for at redigere siden.](media/edit-pencil.png) giver dig mulighed for at tilføje tekst i de felter, der kan redigeres.


## <a name="see-also"></a>Se også
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
