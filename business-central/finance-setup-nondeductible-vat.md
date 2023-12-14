---
title: Oprette ikke-fradragsberettiget moms
description: 'I denne artikel forklares det, hvordan ikke-fradragsberettiget moms konfigureres i Microsoft Dynamics 365 Business Central.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Oprette ikke-fradragsberettiget moms

Moms uden fradragsberettiget moms er den moms, der skal betales af en indkøber, men som ikke er fradragsberettiget for køberens eget momsansvar. Virksomheder kan som regel genoprette moms på køb af varer og tjenester, der vedrører deres forretningsaktiviteter. I nogle situationer er en virksomhed, der er inddraget moms, men som ikke er fradragsberettiget. Disse situationer vedrører typisk de lokale forskrifter og kan variere fra land/område til land/område. Modellen til brug af ikke-fradragsberettiget eller delvist fradragsberettiget moms er den samme. Du kan bruge proportional moms til at beregne moms, når der er fradragsberettiget og ikke-fradragsberettiget moms.

Generelt kan moms ikke fratrækkes for nogle indkøb pga. følgende faktorer:

- **Den type varer eller tjenester, der købes** – momsen er helt eller delvist ikke-fradragsberettiget ved lov om varer, f. eks. biler, mobiltelefoner og fødevarer, der købes på restauranter.
- **Delvist fradragsberettiget moms** – momsen er professionel ifølge forholdet mellem salgs operationerne for den pågældende moms og alle de operationer, der er blevet udført. Moms, der overstiger dette nøgletal, kan ikke fratrækkes.

Da det kan være svært at vide, hvor og hvordan en vare anvendes, skal du kontakte de lokale skattemyndigheder i dit land/område for at finde ud af, om en bestemt procent af momsen fradrages i forhold til historiske data. 

> [!IMPORTANT]
> Denne globale funktion er tilgængelig i alle lande med aktiveret moms, **bortset fra Belgien, Italien og Norge**. Disse lokaliteter har allerede eksisterende lokal funktionalitet og opgraderes fremover. Du skal ikke køre denne funktion i disse lande, da opgraderingsproceduren ikke findes.

## Bruge ikke-fradragsberettiget moms

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af VAT** og vælg derefter det relaterede link.
2. Vælg afkrydsningsfeltet **Aktiver ikke-fradragsberettiget moms**.

    > [!IMPORTANT]
    > Når du har aktiveret ikke-fradragsberettiget moms, kan du ikke deaktivere den, da funktionen kan omfatte ændringer af data og kan starte en opgradering af nogle databasetabeller. Microsoft anbefaler på det kraftigste, at du først aktiverer og tester denne funktion i sandkasse miljøet, før du aktiverer den i produktionsmiljøet.

3. Konfigurer, hvordan systemet skal behandle ikke-fradragsberettigede momsværdier.

    1. I feltet **Brug til varekostpris** skal du angive, om den ikke-fradragsberettigede moms skal føjes til vareomkostningen, når du køber varer. Ellers vil den ikke-fradragsberettigede moms ikke have indflydelse på vareomkostningerne, og hele beløbet registreres kun på finansniveau.
    2. Marker afkrydsningsfeltet **Brug af anlægsaktivomkostninger** for at føje den ikke-fradragsberettigede moms til anlægsaktivets kostbeløb, når du køber nye anlægsaktiver. Ellers vil den ikke-fradragsberettigede moms ikke have indflydelse på anlægsaktivet omkostning, og hele beløbet registreres kun på finansniveau.
    3. Marker afkrydsningsfeltet **Brug af sagsomkostninger** for at angive, at den ikke-fradragsberettigede moms skal lægges til sagsomkostninger, når du køber varer til sagen. Ellers vil den ikke-fradragsberettigede moms ikke have indflydelse på jobomkostningerne, og hele beløbet registreres kun på finansniveau.
    4. Marker afkrydsningsfeltet **Vis ikke-fra. moms i linjer** for at angive, at den ikke-fradragsberettigede moms skal vises på dokumentlinje sider for at gøre det nemmere at manipulere momsbeløb.

## Brug den ikke-fradragsberettigede momsprocent

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.
2. På siden **Momsbogf.opsætning** skal du udfylde felterne som beskrevet i følgende tabel.

    | Felt | Beskrivelse |
    |-------|-------------|
    | Tillad ikke-fradragsberettiget moms | Angiver, om den ikke-fradragsberettigede moms tages i betragtning til denne bestemte kombination af bogføringsgrupper for momsvirksomheder og momsprodukter. |
    | Ikke-fradragsberettiget momsprocent | Angiv den procentdel af transaktionsbeløbet, som momsen ikke er anvendt med. |
    | Ikke-fradragsberettiget købsmomskonto | Angiv den konto, der er knyttet til momsbeløbet, som ikke er fratrukket pga. den købte type varer eller services. |

    > [!NOTE]
    > Hvis du vil have finansposter, som bruger den dedikerede konto, i stedet for salgs- eller købskonti, skal du enten lade feltet **Ikke-fradragsberettiget købsmomskonto** være tomt eller angive **Finanskonto**-feltet.

3. Vælg **OK**.

> [!NOTE]
> Du kan ikke bruge urealiseret moms sammen med ikke-fradragsberettiget moms.
>
> Undlad at bruge den samme **Moms-id**-værdi for både normal moms, hvor feltet **Ikke-fradragsberettiget momsprocent** er indstillet til **0** (nul) og normal moms, hvor feltet **Ikke-fradragsberettiget momsprocent** er indstillet til en anden værdi end nul. Ellers vil det samlede ikke-fradragsberettigede momsbeløb blive beregnet forkert.

## Se også

[Økonomistyring](finance.md)  
[Designoplysninger: Ikke-fradragsberettiget moms](design-details-nondeductible-vat.md)  
[Bruge ikke-fradragsberettiget moms](finance-how-use-non-deductible-vat.md)  
[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
