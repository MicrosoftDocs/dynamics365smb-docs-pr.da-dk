---
title: Kontrollere adgang ved hjælp af sikkerhedsgrupper
description: 'Denne artikel beskriver, hvordan sikkerhedsgrupper bruges til at definere brugertilladelser.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 11/29/2023
---

# <a name="control-access-to-business-central-using-security-groups"></a>Kontrollere adgangen til Business central ved brug af sikkerhedsgrupper

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Sikkerhedsgrupper gør det nemmere for administratorer at administrere brugertilladelser. F. eks. til [!INCLUDE [prod_short](includes/prod_short.md)] online kan de genbruges på tværs af Dynamics 365-programmer, f.eks. SharePoint online, CRM Online og [!INCLUDE [prod_short](includes/prod_short.md)]. Administratorer føjer tilladelser til deres [!INCLUDE [prod_short](includes/prod_short.md)]-sikkerhedsgrupper, og når de føjer brugere til gruppen, gælder tilladelserne for alle medlemmer. En administrator kan f.eks. oprette en [!INCLUDE [prod_short](includes/prod_short.md)]-sikkerhedsgruppe, der giver sælgere mulighed for at oprette og bogføre salgsordrer. Eller lad indkøbere gøre det samme for købsordrer.

## <a name="business-central-online-and-on-premises"></a>Konfigurere Business Central online og lokalt

Du kan bruge sikkerhedsgrupper til online-og lokale versioner af [!INCLUDE [prod_short](includes/prod_short.md)]. Afhængigt af produktversionen skal du oprette grupper på en af følgende måder:

* Brug Microsoft Entra-sikkerhedsgrupper til onlineversionen. Hvis du vil vide mere om, hvordan du opretter gruppen, skal du gå til [Opret, rediger eller slet en sikkerhedsgruppe i Microsoft 365 Administration](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Lokalt understøttes sikkerhedsgrupper kun, hvis installationen bruger Windows-godkendelse. Brug Windows Active Directory-grupper til oprettelse af sikkerhedsgrupper til lokal brug. Hvis du vil vide mere, skal du gå til [Opret en gruppekonto i Windows Active Directory](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Bagefter skal du oprette en tilsvarende sikkerhedsgruppe i [!INCLUDE [prod_short](includes/prod_short.md)] og derefter knytte den til den gruppe, du har oprettet. Hvis du vil vide mere, skal du gå til [Tilføje en sikkerhedsgruppe i Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Hvis du har oprettet en særlig type bruger med en Windows-gruppelicenstype i en version af [!INCLUDE [prod_short](includes/prod_short.md)] on-Prem, der er tidligere end 2023-udgivelsesbølge 1, når du opgraderer [!INCLUDE [prod_short](includes/prod_short.md)], konverteres brugeren til en sikkerhedsgruppe. Den nye sikkerhedsgruppe har samme navn som navnet på Windows-gruppen. Sikkerhedsgruppen giver dig et bedre overblik over gruppemedlemmerne og deres gældende tilladelser.

## <a name="add-a-security-group-in-business-central"></a>Tilføje en sikkerhedsgruppe i Business Central

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sikkerhedsgrupper**, og vælg derefter det relaterede link.
1. Vælg **Ny** for at oprette en gruppe.
1. Opret hyperlinket til din gruppe på følgende måde:

    * For [!INCLUDE [prod_short](includes/prod_short.md)] online skal du vælge gruppen i feltet **Microsoft Entra-sikkerhedsgruppenavn**.
    * Til [!INCLUDE [prod_short](includes/prod_short.md)]-lokalt skal du vælge gruppen i feltet **Windows-gruppenavn**.

> [!NOTE]
> De brugere, der vises på kortet **Medlemmer** i faktaboksruden eller på siden **Medlemmer af sikkerhedsgruppe**, hvis de er tilføjet som brugere i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger om at tilføje brugere i [Sådan tilføjer du brugere eller opdaterer brugeroplysninger og licenstildelinger i Business Central](ui-how-users-permissions.md#adduser).  

### <a name="assign-permissions-to-a-security-group"></a>Tildele tilladelser til en sikkerhedsgruppe

1. På siden **Sikkerhedsgruppe** skal du vælge gruppen og derefter handlingen **Tilladelser**.
1. Tildel rettigheder på følgende måder:

    * Hvis du vil tildele tilladelsessæt individuelt, skal du vælge de tilladelser, der skal tildeles, i feltet **Tilladelsessæt**.
    * Hvis du vil tildele flere tilladelsessæt, skal du vælge handlingen **Vælg tilladelsessæt** og derefter vælge de sæt, der skal tildeles.

## <a name="review-the-permissions-in-a-security-group"></a>Gennemse tilladelser i en sikkerhedsgruppe

På siden **Sikkerhedsgrupper** vises faktaboksen med de **Tilladelsessæt**, der er tildelt gruppen. Hver bruger på listen på kortet **Medlemmer** har disse tilladelser. Handlingen **Tilladelsessættet for en sikkerhedsgruppe** giver en mere detaljeret visning. Her kan du også udforske de individuelle tilladelser i de enkelte sikkerhedsgrupper.

Tilladelserne er også tilgængelige på siden **Brugere**. I faktaboksruden vises **Tilladelserne fra sikkerhedsgruppe** og **Sikkerhedsgruppernes medlemskab**-kort for den valgte bruger.

## <a name="security-groups-and-user-groups"></a>Sikkerhedsgrupper og brugergrupper

> [!NOTE]
> Brugergrupper vil ikke længere være tilgængelige i en fremtidig version.

Sikkerhedsgrupper ligner meget de brugergrupper, der er tilgængelige i øjeblikket. Brugergrupper er dog kun relevante for [!INCLUDE [prod_short](includes/prod_short.md)]. Sikkerhedsgrupper er baseret på grupper i Microsoft Entra ID eller i Windows Active Directory, afhængigt af om du bruger henholdsvis [!INCLUDE [prod_short](includes/prod_short.md)] online eller lokalt. Grupper giver administratorer fordel, fordi de kan bruge dem med andre Dynamics 365-apps. Hvis sælgerne f. eks. bruger [!INCLUDE [prod_short](includes/prod_short.md)] og SharePoint, skal administratorer ikke oprette gruppen og dens medlemmer igen.

### <a name="optional-convert-user-groups-to-permission-sets"></a>Eventuelt: Konvertere rettighedssæt til brugergrupper

I 2023-udgivelsesbølge 1 og nyere kan du konvertere brugergrupper til tilladelsessæt i din lejer. Tilladelsessæt giver samme funktionalitet som brugergrupper. Eksempler:

* Du kan bruge faktaboksen **Brugere** til at administrere tilladelser for brugere.
* Du kan foretage detaljeopløftning for navnet på tilladelsessættet for at føje andre tilladelsessæt til det sæt, du arbejder på. Du kan finde flere oplysninger i [Tilføje andre rettighedssæt](ui-define-granular-permissions.md#to-add-other-permission-sets).

Brug den assisterede opsætningsvejledning **Migrering af brugergruppe** til at konvertere dine grupper. Hvis du vil starte programguiden, skal du gå til siden **funktionsstyring**, finde **Funktion: Konverter brugergrupperettigheder** og derefter vælge **Alle brugere** i feltet **Aktiveret for**. Den assisterede opsætningsvejledning giver følgende muligheder med konverteringen.

|Indstilling  |Beskrivlse  |
|---------|---------|
|Tildele til bruger     | Tildel rettigheder i brugergrupper direkte til brugerne, der er tildelt denne gruppe, og fjern deres brugergruppetildelinger.        |
|Konvertér til et rettighedssæt     | Opret en ny tilladelse for tilladelserne i hver brugergruppe. Det nye tilladelsessæt tildeles alle medlemmer af hver brugergruppe.          |

### <a name="license-configurations-still-apply"></a>Licenskonfigurationer gælder stadig

Du kan konfigurere tilladelser i [!INCLUDE [prod_short](includes/prod_short.md)] baseret på licenser. Disse tilladelser tildeles direkte til nye brugere. Disse konfigurationer gælder stadig, selvom du begynder at bruge sikkerhedsgrupper.

Hvis du vil bruge sikkerhedsgrupper eksklusivt, anbefales det, at du fjerner licenskonfigurationerne. Hvis du vil vide mere om licenskonfigurationer, skal du gå til [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).

Du kan fjerne licenskonfigurationer på siden **Licenskonfiguration**. Vælg en licens, og slet alle tildelte tilladelsessæt.

## <a name="see-also"></a>Se også

[Oprette brugere i henhold til licenser](ui-how-users-permissions.md)  
[Konfigurere Business Central-adgang i Teams med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
[Få mere at vide om grupper og adgangsrettigheder i Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra-sikkerhedsgrupper](/windows-server/identity/ad-ds/manage/understand-security-groups)  
