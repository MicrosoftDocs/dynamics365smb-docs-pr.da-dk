---
title: Revisoroplevelser i Business Central (indeholder video)
description: 'Få mere at vide om rollecentret Revisor og virksomhedshubben, der understøtter interne og eksterne revisorer i kundevirksomheden.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="accountant-experiences-in-includeprodlongincludesprodlongmd" />Revisoroplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]

Enhver virksomhed skal føre regnskab og godkende det. Nogle virksomheder benytter en ekstern revisor, mens andre har kvalificerede regnskabsmedarbejdere. Uanset hvilken model du benytter, kan du bruge rollecenteret **Regnskabsmedarbejder** som din startside i [!INCLUDE[prod_short](includes/prod_short.md)]. Herfra kan du få adgang til alle sider, du skal bruge i dit arbejde.  

## <a name="accountant-role-center" />Rollecenteret Regnskabsmedarbejder

Rollecenteret er et dashboard med aktivitetsfelter, der viser nøgletal i realtid og giver dig hurtig adgang til data. På båndet øverst på siden har du adgang til flere handlinger, f.eks. åbning af mest almindeligt brugt regnskabsrapporter og kontoudtog i Excel. I navigationsruden øverst kan du hurtigt skifte mellem de lister, du bruger mest. Her vises andre områder, f.eks. **Bogførte dokumenter** med de forskellige typer dokumenter, som firmaet har bogført.  

Hvis du ikke kender [!INCLUDE[prod_short](includes/prod_short.md)], kan du åbne en liste over videoer direkte fra dit rollecenter. Du kan også starte en guide, som f.eks. **Introduktion**, der udpeger vigtige områder.  

## <a name="company-hub" />Virksomhedshub

Hvis du arbejder i flere [!INCLUDE [prod_short](includes/prod_short.md)]-firmaer, kan det være nyttigt at bruge siden **Virksomhedshub** til at holde styr på arbejdet.  Du kan finde flere oplysninger i [Administrer arbejde på tværs af flere firmaer i virksomhedens hub](company-hub.md).  

## <a name="a-nameinviteaccountantainviting-your-external-accountant-to-your-includeprodshortincludesprodshortmd" /><a name="inviteaccountant"></a>Inviter din eksterne revisor indenfor i din [!INCLUDE[prod_short](includes/prod_short.md)]

Hvis du bruger en ekstern revisor til at administrere dine regnskaber og financial reporting, kan din administrator invitere ham eller hende indenfor i din [!INCLUDE[prod_short](includes/prod_short.md)], så de kan samarbejde med dig om dine regnskabsdata. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder tre licenser af typen Ekstern revisor. Du kan finde flere oplysninger om licenser i [Licensvejledning til Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Når din revisor har fået adgang til dit [!INCLUDE[prod_short](includes/prod_short.md)], kan han eller hun bruge rollecenteret **Regnskabsmedarbejder**, der giver nem adgang til de mest relevante sider for deres arbejde. De kan også bruge virksomheds hubben [!INCLUDE [prod_short](includes/prod_short.md)] til at styre deres arbejde. Du kan finde flere oplysninger i [Administrer arbejde på tværs af flere firmaer i virksomhedens hub](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Vi har gjort det nemt for dig at invitere din eksterne revisor. Du skal blot åbne siden **Brugere** og derefter vælge handlingen **Inviter ekstern revisor** på båndet. En mail er gjort klar til dig, så du blot skal tilføje din revisors arbejds-mail og sende invitationen.  

> [!Note]  
> Dette kræver, at du har oprettet SMTP-mail. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Revisorens mailadresse skal være en arbejdsadresse, der er baseret på Azure Active Directory. Hvis revisoren bruger en anden type mail, så kan invitationen ikke sendes.
>
> Denne opgave kræver adgang til at administrere brugere og licenser i Azure Active Directory. Den bruger, der sender denne invitation, skal tildeles rollen **Globale administrator** eller **Brugeradministrator** i Microsoft 365 Administration. Du kan flere oplysninger i [Om administratorroller](/microsoft-365/admin/add-users/about-admin-roles) i Microsoft 365 Administrator-indholdet.  

### <a name="adding-your-accountant-to-your-microsoft--in-the-azure-portal" />Tilføjelse af din revisor til Microsoft 365 i Azure-portalen

Hvis din administrator eller videresalgspartner ikke vil bruge guiden **Inviter ekstern revisor**, kan vedkommende tilføje en ekstern bruger på Azure-portalen og tildele denne bruger licensen til den *Eksterne revisor*. Du finder flere oplysninger under [Hurtig start: Tilføj gæstebrugere til dit katalog i Azure-portalen](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user" />Sådan tilføjer du din revisor som gæstebruger

1. Åbn [Azure-portalen](https://portal.azure.com/).
2. Gå til venstre rude, og vælg **Azure Active Directory**.
3. Vælg **Brugere** under **Administrer**.
4. Vælg **Ny gæstebruger**.
5. Gå til siden **Ny bruger**, og vælg **Inviter bruger**, og tilføj derefter oplysninger om din eksterne revisor.  

   Du kan også inkludere en personlig velkomstmeddelelse til revisoren for at fortælle vedkommende, at du føjer ham eller hende til [!INCLUDE[prod_short](includes/prod_short.md)].

6. Vælg **Inviter** for automatisk at sende invitationen. Der vises en meddelelse øverst til højre med beskeden **Bruger er blevet inviteret**. 
7. Når du har sendt invitationen, føjes brugerkontoen automatisk til kataloget som gæst.

Derefter skal du tildele den nye gæstebruger en licens til [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-give-your-accountant-access-to-your-includeprodshortincludesprodshortmd" />Sådan giver du din revisor adgang til [!INCLUDE[prod_short](includes/prod_short.md)]

1. Gå til Azure-portalen, og vælg **Profil**og derefter **Rediger** på den bruger, der netop er tilføjet.
2. Opdater feltet **Brugsplacering** til det relevante land, og vælg derefter **Gem.**
3. Vælg **Licenser**, og åbn derefter **Tildelinger**.
4. Vælg licensen **Dynamics 365 Business Central Ekstern revisor**.  
    
    Hvis licensen ikke er tilgængelig, skal du kontakte din forhandlingspartner for at føje licensen til dit abonnement.

    Med henblik på evalueringsformål kan du i stedet bruge en tilgængelig **Dynamics 365 Business Central til IWs**-licens. Men du kan ikke bruge denne type licens, hvis du allerede har købt [!INCLUDE[prod_short](includes/prod_short.md)]. 
5. Gem tildelingen.

Hvis det lykkes, tildeles licensen til gæstebrugeren, og gæstekontoen oprettes.

### <a name="importing-the-new-user-into-includeprodshortincludesprodshortmd" />Import af den nye bruger til [!INCLUDE[prod_short](includes/prod_short.md)]

Revisoren modtager en e-mail, der giver vedkommende besked om, at han eller hun har fået adgang til dit Active Directory. Derefter skal du give vedkommende adgang til den rigtige virksomhed i [!INCLUDE[prod_short](includes/prod_short.md)].

#### <a name="to-add-the-accountant-to-the-right-company" />Sådan føjes revisoren til den rigtige virksomhed

1. Åbn den [!INCLUDE[prod_short](includes/prod_short.md)]-virksomhed, du vil give revisoren adgang til, på [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugere**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Hent nye brugere fra Microsoft 365**.

Denne importerer den brugerkonto, som du oprettede på Azure-portalen, til virksomheden. Du kan finde flere oplysninger i [Sådan tilføjes en bruger i Business Central](ui-how-users-permissions.md#adduser).  

Hvis du vil give adgang til flere virksomheder, skal du logge ind på hver virksomhed og gentage denne proces. Alternativt kan du opdatere rettighedsgrupperne for revisorens brugerprofil i [!INCLUDE[prod_short](includes/prod_short.md)], f.eks. ved at tildele dem *D365 Bus Premium*-brugergruppen. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

## <a name="see-also" />Se også

[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Analysere regnskabsopgørelser i Excel](finance-analyze-excel.md)  
[Administrere arbejde på tværs af flere regnskaber i virksomhedshub](company-hub.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Opsætning af pengestrømsanalyse](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
