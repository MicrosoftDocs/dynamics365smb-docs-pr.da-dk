---
title: Indsende lovgivningsmæssige påmindelser
description: 'Hvis du kender til ny lovgivning, som du mener kræver understøttelse af funktioner i Business Central, kan du følge denne vejledning for at sende en lovgivningsmæssig påmindelse til produktgruppen.'
author: sorenfriisalexandersen
ms.topic: conceptual
ms.reviewer: bholtorf
ms.search.keywords: null
ms.date: 12/07/2023
ms.author: soalex
ms.service: dynamics-365-business-central
---

# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>Sende påmindelser om lande-/områdespecifikke lovgivningsmæssige funktioner

Du inviteres til at bruge Microsoft Dynamics Lifecycle Services (LCS) til at sende lovgivningsmæssige påmindelser via Dynamics-tjenesten til afsendelse af lovgivningsmæssige påmindelser.  

## <a name="to-submit-a-regulatory-alert-in-lcs"></a>Sådan sendes en lovgivningsmæssig påmindelse i LCS

1. Gå til [Lifecycle Services](https://lcs.dynamics.com) og log ind.  

    Du får vist de projekter, du har adgang til.

2. Vælg projektet **Lovgivningsmæssige påmindelser - globalt**.

    Projektet åbnes, og der vises en række forskellige ting, der er relateret til dette projekt.

3. Vælg **påmindelsestjenesten** i højre side af sektionen **Flere værktøjer**.

    Du får vist en liste over påmindelser med overskriften **Afsendelse af lovgivningsmæssige påmindelser i Dynamics**.

4. Du kan tilføje en ny påmindelse ved at klikke på plustegnet **(+)** øverst på listen.

    Du får vist vejledning med 4 trin til at oprette påmindelsen. Der er følgende trin i vejledningen:
    - Søg efter eksisterende elementer.

        Søg efter alle oplysninger, du mener er relevante for den påmindelse, du vil oprette. Hvis du ikke kan finde nogen relevante søgeresultater, kan du vælge knappen **Send lovgivningsmæssig påmindelse** nederst på siden for at fortsætte med at sende påmindelser.
    - Tilknyt forretningsprocesser.

        Denne del er ikke relevant for Dynamics 365 Business Central. Vælg **Spring over** for at gå videre til næste trin.
    - Beskriv påmindelsen.

        Angiv oplysninger om påmindelsen i de relevante felter. Obligatoriske felter er angivet med en rød stjerne (\*) i vejledningen.

        |Felt        |Beskrivelse                               |
        |-------------|------------------------------------------|
        |Titel  | Angiv en beskrivende titel for at identificere det påvirkede område. Skriv f.eks. *Ændringer i fakturadokumenter pr. 1. juli 2019*. |
        |Beskrivelse  | Angiv en kort oversigt over lovgivningen. Beskrivelsen skal fokusere på problemer, der er relevante for ERP (enterprise resource planning), så brugere kan forstå kravene på højt niveau uden at skulle læse lovgivning først.|
        |Land/område  | Angiv det land eller område, som lovgivningen vedrører.|
        |Branche| Angiv branchen, hvis kravet gælder kun for bestemte brancher. F.eks. vælg **Offentlig sektor**, **Detail** eller **Produktion**.|
        |Funktionsreference  | Dette er ikke relevant for Business Central, men du kan angive en reference til funktionen, hvis du kender til den. Listen over funktioner for bestemte lande/områder findes på [Lokaliseringsportal](/dynamics/s-e/) på CustomerSource-webstedet. |
        |Dato for retshåndhævelse  | Angiv den dato, hvor de berørte kunder skal begynde at overholde lovgivningen.|
        |Myndighedernes offentliggørelsesdato  | Angiv den dato, hvor myndighederne offentliggjorde ændringen.|
        |Seneste arkiveringsdato  | Vælg datoen for den første indsendelse af den nye eller ændrede rapport.|
        |Link til lovgivning  | Angiv et eller flere links til den publicerede lovgivning, retningslinjer for fortolkning, implementeringsvejledning eller anden nyttig dokumentation, så brugerne kan forstå eller kan implementere kravet.|
        |Navn på virksomhed  | Angiv virksomhedsnavnet for den person, der sender beskeden.|
        |Kontaktnavn  | Angiv navnet på den person, der sender beskeden. |
        |Kontaktens mailadresse  | Mailadressen på den person, der sender beskeden.|
        |Forretningsproces  | De forretningsprocesser, du har valgt via guiden **Afsendelse af påmindelse**|
        |Bemærkninger  | Angiv yderligere oplysninger, der kan hjælpe brugerne med at forstå eller implementere kravet. Vælg **Send** for at gemme dine kommentarer. Flere kommentarer kan tilføjes og skal sendes separat. Kommentarer gemmes i den rækkefølge, de tilføjes. |
        |Vedhæftede filer  | Vælg knappen **Overfør**, og gennemse derefter filerne, og vælg en, der skal bruges som vedhæftet fil. Når du vælger filen, overføres den og vises som en sammenkædet fil. Du kan tilføje op til tre filer, der hver kan have en størrelse på 5 MB. Hvis du vil slette filer, der er vedhæftet, skal du vælge **Fjern** under overskriften på filen. Vedhæftede filer skal være offentligt tilgængelige materialer. De må ikke være private eller partnerspecifikke/kundespecifikke.|

        Vælg **Send** for at gemme og sende beskeden.

        Hvis du ikke har alle nødvendige oplysninger, eller hvis du ikke er endnu er klar til at sende påmindelsen, kan du gemme en delvist fuldført påmindelse.

    - Afsendelsesbekræftelse.

      Når du har sendt påmindelsen, får du en bekræftelse af, at beskeden blev sendt til Microsoft.

## <a name="see-also"></a>Se også

[Lokal funktionalitet i [!INCLUDE[prod_long](includes/prod_long.md)]](about-localization.md)  
[Ændre sprog og landestandard](about-locale-language.md)  
[Blive køreklar til at foretage handler](ui-get-ready-business.md)  
[Velkommen til Business Central](welcome.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
