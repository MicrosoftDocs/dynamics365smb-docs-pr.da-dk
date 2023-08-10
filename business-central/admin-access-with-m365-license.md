---
title: Business Central adgang med Microsoft 365-licenser
description: 'Få mere at vide om, hvordan brugere kan få adgang til Business Central-data, f. eks. i Microsoft Teams-chat og kanaler, med en Microsoft 365-licens, men ingen Business Central-licens.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# <a name="business-central-access-with-microsoft-365-licenses"></a>Business Central-adgang med Microsoft 365-licenser

[!INCLUDE[prod_short](includes/prod_short.md)]-brugere får tildelt en Dynamics 365 Business Central-licens, som giver dem mulighed for at få vist, ændre og behandle forretningsdata fra enhver brugergrænseflade. For alle andre medarbejdere i hele organisationen, der kun har behov for at få vist data af og til, giver Business central adgang via Microsoft 365.  

Når en organisation har både Dynamics 365 Business Central- og Microsoft 365-abonnement, kan administratorer konfigurere miljøer for at aktivere adgang med Microsoft 365-licenser og vælge nøjagtigt, hvilke tabeller og andre objekter denne kategori af brugere skal have adgang til. Når den er konfigureret, kan medarbejdere, der har en Microsoft 365-licens, men ikke en [!INCLUDE [prod_short](includes/prod_short.md)]-licens, få vist [!INCLUDE [prod_short](includes/prod_short.md)]-poster, som deles med dem i Microsoft Teams-chat og kanaler.

## <a name="why-enable-access-with-microsoft-365-licenses"></a>Hvorfor aktivere adgang med Microsoft 365-licenser

- Lås op for stamtræet, som alle medarbejdere i organisationen skal have adgang til.

- Styrk de afdelinger, der ikke kører på [!INCLUDE [prod_short](includes/prod_short.md)] til selvbetjening, med adgang til vigtige data, der er nødvendige for at udføre deres opgaver, hvilket eliminerer behovet for løbende anmodning om data fra andre.

- Øge samarbejdseffekten, så opgaver og projekter, der spænder over flere afdelinger, afsluttes til tiden, ved at fjerne den friktion, der typisk er forbundet med adgang nægtet-fejl pga. licens.

- Øg teamets ydeevne, så brugerne kan foretage datadrevne beslutninger, der inkluderer alle i gruppen, selvom de ikke fungerer i [!INCLUDE [prod_short](includes/prod_short.md)].

- Opfyld til budgetmæssige mål ved at tildele licenser, der gradvist svarer til medarbejderbehov, med Microsoft 365-licenser til skrivebeskyttet adgang, Dynamics 365 Business Central Team-medlemslicenser til begrænset skriveadgang og Dynamics 365 Business Central Essentials eller Premium med fuld skriveadgang.

- Øg datasikkerheden ved at reducere behovet for at indsætte skærmstykker af forretningsdata uden for styring af datagrænser.

## <a name="use-rights"></a>Bruge rettigheder

Når en person får adgang til [!INCLUDE [prod_short](includes/prod_short.md)] med en Microsoft 365-licens, giver denne licens brugeren ret til at læse (men ikke skrive) [!INCLUDE [prod_short](includes/prod_short.md)]-data gennem en forenklet brugergrænseflade i Microsoft Teams. I dette afsnit forklares disse rettigheder og begrænsninger, som du kan bruge til at planlægge, hvordan du konfigurerer og får mest muligt ud af denne funktion. Du kan finde flere oplysninger om denne licenstype i forhold til andre [!INCLUDE [prod_short](includes/prod_short.md)]-licenser i [Dynamics 365-licensvejledning](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### <a name="client-access"></a>Klientadgang

Brugere har ret til at få adgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data i Microsoft Teams. I følgende tabel vises en oversigt over, hvilke metoder du kan bruge til at få adgang til [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten med denne licens.

|Klient, der har adgang til Business Central-tjenesten |Adgang|
|-|-|
|Business central-app til Microsoft Teams|![Ja](media/check.png)|
|Business Central-webklient |![Nej](media/x-icon.png ) |
|Business Central-mobilapps|![Nej](media/x-icon.png )|
|Business Central-API'er|![Nej](media/x-icon.png )|
|Business Central-integration med andre Office-programmer|![Nej](media/x-icon.png )|
|Business Central integreret i alle andre programmer |![Nej](media/x-icon.png )|

### <a name="data-access"></a>Dataadgang

Brugerne har ret til at læse tabeldata, men de kan ikke ændre, oprette eller slette poster. [!INCLUDE [prod_short](includes/prod_short.md)]-platformen forhindrer automatisk skrivning til nogen datatabeller.  

### <a name="use-of-objects"></a>Bruge objekter

Adgang til Microsoft 365-licenser forhindrer ikke, hvilke Business Central-objekter eller objektområder der er adgang til. Brugere har adgang til Microsoft Base Application og alle udvidelser, f. eks. tilpasninger og tilføjelsesprogrammer.

## <a name="simplified-user-interface"></a>Forenklet brugergrænseflade

Brugere har ret til et reduceret sæt funktioner og funktioner, der leveres af [!INCLUDE [prod_short](includes/prod_short.md)] i Microsoft Teams. Tabellerne nedenfor viser de bemærkelsesværdige funktioner. Dette er ikke en udtømmende liste og kan ændres.

Funktioner i [!INCLUDE [prod_short](includes/prod_short.md)]-appen til Teams:

|Funktion  |Tilgængelig|
|-|-|
|Få vist [!INCLUDE [prod_short](includes/prod_short.md)]-kort|![Ja](media/check.png)|
|Vis kortdetaljer |![Ja](media/check.png) |
|Fastgøre kortets detaljer som en fane |![Ja](media/check.png)|
|Vis [!INCLUDE [prod_short](includes/prod_short.md)]-faner|![Ja](media/check.png)|
|Tilføj en [!INCLUDE [prod_short](includes/prod_short.md)]-fane|![Nej_](media/x-icon.png )|
|Søg efter forretningskontakter |![Nr.](media/x-icon.png )|
|Indsætte og dele et link-forhåndsversion som et kort|![Nr.](media/x-icon.png )|

Funktionerne i [!INCLUDE [prod_short](includes/prod_short.md)]-klientens funktioner integreret i Teams:

|Funktion |Tilgængelig|Eksempelfunktioner|
|-|-|-|
|Systemhandlinger for datamanipulation |![Nej](media/x-icon.png )|Redigere, Oprette, Slette|
|Grundlæggende funktioner på lister|![Ja](media/check.png)|Søge, sortere, ændre layout|
|Avancerede funktioner på lister|![Nej](media/x-icon.png )|Filterrude, visninger|
|Detaljeudledning fra liste til kort |![Ja](media/check.png)||
|Adgang til data fra relaterede tabeller|![Nej](media/x-icon.png )|Faktaboks-rude, detaljefelt, smugkig, slå op |
|Handlinger|![Nej](media/x-icon.png )|Handlingslinje, handlingsmenuer, handlinger for sidebeskeder|
|Genveje på tværs af systemet|![Nej](media/x-icon.png )|Mine indstillinger, rollestifinder, Fortæl mig-søgning  |
|Kopiér|![Ja](media/check.png)|Kopiere rækker, kopiere feltværdi, kopiere link til side|
|UI-tilpasning|![Nej](media/x-icon.png )|Tilpas| 
|Indbygget tilpasning|![Ja](media/check.png)|Tilpas kolonne, Udvid/skjul, Vis flere |
|Datadeling |![Nej](media/x-icon.png )|Åbn eller Rediger i Excel, Del med teams|
|Indbygget brugerassistance|![Ja](media/check.png) |Værktøjstip, links til dokumentation|
|Udvidet brugerassistance |![Nej](media/x-icon.png )|Tips om side og felt, hjælp-rude|

## <a name="minimum-requirements"></a>Minimumkrav

I dette afsnit beskrives minimumkravene, der skal opfyldes, for at organisationen kan aktivere adgang med Microsoft 365-licenser, og for at individuelle Microsoft Teams-brugere kan få adgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data uden en [!INCLUDE [prod_short](includes/prod_short.md)]-licens.

### <a name="requirements-to-enable-access"></a>Krav til at aktivere adgang

- [!INCLUDE [prod_short](includes/prod_short.md)] online (SaaS).

- Miljøer skal være af platformversion 21,1 eller nyere.

### <a name="requirements-for-individual-users-to-access-data-in-teams"></a>Krav til individuelle brugere med henblik på at få adgang til data i Teams

- Der skal opnås adgang til til data med [!INCLUDE [prod_short](includes/prod_short.md)]-app til Teams. Brugere skal have installeret [!INCLUDE [prod_short](includes/prod_short.md)]-app til Teams og skal bruge en af de understøttede Teams-klienter. Du kan finde en liste over Teams-klienter, der understøttes af [!INCLUDE [prod_short](includes/prod_short.md)] i [Minimumskrav til brug af Business Central](product-requirements.md#teams).

- Brugere skal være interne i organisationen, hvilket vil sige, at en brugeridentitet kommer fra den samme lejer, hvor [!INCLUDE [prod_short](includes/prod_short.md)] er implementeret, og hvor adgang er aktiveret. Eksterne identiteter understøttes ikke. [!INCLUDE [prod_short](includes/prod_short.md)] forhindrer automatisk adgang for gæster.

- Brugere skal tildeles en Microsoft 365-licens fra en af følgende planer.
  
  |Understøttet plan|Produkt-id |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Azure AD-identitet) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  De fleste tilbud, der er baseret på disse planer, understøttes også. Hvis du f. eks. abonnerer på Microsoft 365 Business Premium (non profit medarbejdere), er det et specifikt tilbud om non-profit-organisationer baseret på Microsoft 365 Business Premium-planen og understøttes derfor.

  > [!NOTE]
  > Kan du ikke finde din plan på listen? Microsoft tjekker hele tiden feedback for at se, hvordan vi kan forbedre tjenesten og udvide vores tilbud, så flere kunder kan udnytte denne funktion. Del din idé for, hvilke planer vi skal understøtte næste gang på [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Brugere skal tildeles en Microsoft 365-licens, hvor appen Microsoft Teams er aktiveret på listen over apps til den pågældende licens.

  |Understøttede apps|Service Plan ID|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- Organisationen skal have mindst én anden bruger, der har fået tildelt en Dynamics 365 Business Central-licens.

## <a name="next-steps"></a>Næste trin

- Få et overblik over brugerens adgangsforløb, så du kan planlægge din metode og konfiguration af Business Central, så den passer til virksomhedens behov. Se [brugerens adgangsflow](admin-access-with-m365-license-flow.md).
- Konfigurere miljøet og brugere til adgang med Microsoft 365-licenser. Se [Konfigurere adgang til Microsoft 365-licenser ](admin-access-with-m365-license-setup.md).

## <a name="see-also"></a>Se også

[Business Central og Microsoft Teams-integration](across-teams-overview.md)  
