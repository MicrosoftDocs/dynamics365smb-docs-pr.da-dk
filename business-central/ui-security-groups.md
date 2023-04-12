---
title: Kontrollere adgang ved hjælp af sikkerhedsgrupper
description: 'Denne artikel beskriver, hvordan sikkerhedsgrupper bruges til at definere brugertilladelser.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Kontrollere adgangen til Business central ved brug af sikkerhedsgrupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Sikkerhedsgrupper gør det nemmere for administratorer at administrere brugertilladelser i deres Dynamics 365-programmer, f.eks. SharePoint Online, CRM Online og onlineversionen af [!INCLUDE [prod_short](includes/prod_short.md)]. Administratorer føjer tilladelser til deres sikkerhedsgrupper, og når de føjer brugere til gruppen, gælder tilladelserne for alle medlemmer. En administrator kan f.eks. oprette en sikkerhedsgruppe, der giver sælgere mulighed for at oprette og bogføre salgsordrer. Eller lad indkøbere gøre det samme for købsordrer.

Opret sikkerhedsgrupperne i Microsoft 365 Administration eller Azure Active Directory. I denne artikel beskrives trinene i Microsoft 365 Administration, men trinene er ens i begge.

## Tilføj en sikkerhedsgruppe i Microsoft 365 Administration

1. Gå til siden **Aktive teams og grupper** i Microsoft 365 Administration.
2. Vælg **Tilføj en gruppe**.
3. Vælg gruppetypen **Sikkerhed**, og vælg derefter **Næste**.
4. Angiv basis for din gruppe.
5. Valgfrit: gør medlemmerne i gruppen tilgængelige for rolletildeling. Hvis du vil vide mere om tildelingerne, skal du gå til [Brug Azure AD-grupper for at administrere rolletildelinger](/azure/active-directory/roles/groups-concept).
6. Åbn gruppen, og brug fanen **Tilføj medlemmer** til at medtage personer i gruppen.

## Tilføje en sikkerhedsgruppe i Business Central

I [!INCLUDE [prod_short](includes/prod_short.md)] skal du oprette en sikkerhedsgruppe og derefter knytte den til sikkerhedsgruppen i Microsoft 365 Administration. Den nye gruppe indeholder de medlemmer, du har tilføjet i Microsoft 365 Administration.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sikkerhedsgrupper**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en gruppe.
3. Indtast et navn for gruppen i feltet **Navn**.
4. I feltet **AAD-sikkerhedsgruppenavn** skal du angive navnet på sikkerhedsgruppen, nøjagtigt som den vises i Microsoft 365 Administration. [!INCLUDE [prod_short](includes/prod_short.md)] vil finde den pågældende gruppe og knytte den til denne gruppe.

> [!NOTE]
> De brugere, der vises på kortet **Medlemmer** i faktaboksruden eller på siden **Medlemmer af sikkerhedsgruppe**, hvis de er tilføjet som brugere i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om at tilføje brugere i [Sådan tilføjer du brugere eller opdaterer brugeroplysninger og licenstildelinger i Business Central](ui-how-users-permissions.md#adduser).  

### Tildele rettigheder til gruppen

1. På siden **Sikkerhedsgruppe** skal du vælge gruppen og derefter handlingen **Tilladelser**.
1. Tildel rettigheder på følgende måder:
    * Hvis du vil tildele tilladelsessæt individuelt, skal du vælge de tilladelser, der skal tildeles, i feltet **Tilladelsessæt**.
    * Hvis du vil tildele flere tilladelsessæt, skal du vælge handlingen **Vælg tilladelsessæt** og derefter vælge de sæt, der skal tildeles.

## Gennemse tilladelser i en sikkerhedsgruppe

På siden **Sikkerhedsgrupper** vises faktaboksen med de **Tilladelsessæt**, der er tildelt gruppen. Hver bruger på listen på kortet **Medlemmer** har disse tilladelser. Handlingen **Tilladelsessættet for en sikkerhedsgruppe** giver en mere detaljeret visning. Her kan du også udforske de individuelle tilladelser i de enkelte sikkerhedsgrupper.

Tilladelserne er også tilgængelige på siden **Brugere**. I faktaboksruden vises **Tilladelserne fra sikkerhedsgruppe** og **Sikkerhedsgruppernes medlemskab**-kort for den valgte bruger.

## Sikkerhedsgrupper og brugergrupper

Hvis du har brugergrupper, kan du konvertere grupperne til tilladelsessæt i lejeren ved hjælp af den assisterende opsætningsvejledning til **Migrering af brugergruppe**. Hvis du vil starte programguiden, skal du gå til siden **funktionsstyring**, finde **Funktion: Konverter brugergrupperettigheder** og derefter vælge **Alle brugere** i feltet **Aktiveret for**. Den assisterede opsætningsvejledning giver følgende muligheder med konverteringen.

|Indstilling  |Beskrivlse  |
|---------|---------|
|Tildele til bruger     | Tildel rettigheder i brugergrupper direkte til brugerne, der er tildelt denne gruppe, og fjern deres brugergruppetildelinger.        |
|Konvertér til et rettighedssæt     | Opret en ny tilladelse for tilladelserne i hver brugergruppe. Det nye tilladelsessæt tildeles alle medlemmer af hver brugergruppe.          |

## Se også

[Oprette brugere i henhold til licenser](ui-how-users-permissions.md)  
[Konfigurere Business Central-adgang i Teams med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Få mere at vide om grupper og adgangsrettigheder i Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory-sikkerhedsgrupper](/windows-server/identity/ad-ds/manage/understand-security-groups)  