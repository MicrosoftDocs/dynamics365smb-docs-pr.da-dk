---
title: Business Central bogholderoplevelse | Microsoft Docs
description: Få mere at vide om revisorportalen til Business Central og rollecenteret Regnskabsmedarbejder, der understøtter interne og eksterne revisorer i kundevirksomheden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2c99b8bef9bff22edd2d27856e703b41c6ec6441
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184024"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Revisoroplevelser i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Enhver virksomhed skal føre regnskab og godkende det. Nogle virksomheder benytter en ekstern revisor, mens andre har kvalificerede regnskabsmedarbejdere. Uanset hvilken model du benytter, kan du bruge rollecenteret **Regnskabsmedarbejder** som din startside i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra kan du få adgang til alle sider, du skal bruge i dit arbejde.  

## <a name="accountant-role-center"></a>Rollecenteret Regnskabsmedarbejder
Rollecenteret er et dashboard med aktivitetsfelter, der viser nøgletal i realtid og giver dig hurtig adgang til data. På båndet øverst på siden har du adgang til flere handlinger, f.eks. åbning af mest almindeligt brugt regnskabsrapporter og kontoudtog i Excel. I navigationsruden øverst kan du hurtigt skifte mellem de lister, du bruger mest. Her vises andre områder, f.eks. **Bogførte dokumenter** med de forskellige typer dokumenter, som firmaet har bogført.  

Hvis du ikke kender [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du åbne en liste over videoer direkte fra dit rollecenter. Du kan også starte en guide, som f.eks. **Introduktion**, der udpeger vigtige områder.  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Inviter din eksterne revisor indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan din administrator invitere ham eller hende indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)], så de kan samarbejde med dig om dine regnskabsdata. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder tre licenser af typen Ekstern revisor. Du kan finde flere oplysninger om licenser i [Licensvejledning til Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Når din revisor har fået adgang til dit [!INCLUDE[d365fin](includes/d365fin_md.md)], kan han eller hun bruge rollecenteret **Regnskabsmedarbejder**, der giver nem adgang til de mest relevante sider for deres arbejde.  

Vi har gjort det nemt for dig at invitere din eksterne revisor. Du skal blot åbne siden **Brugere** og derefter vælge handlingen **Inviter ekstern revisor** på båndet. En mail er gjort klar til dig, så du blot skal tilføje din revisors arbejds-mail og sende invitationen.  

> [!Note]  
> Dette kræver, at du har oprettet SMTP-mail. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Revisorens mailadresse skal være en arbejdsadresse, der er baseret på Azure Active Directory. Hvis revisoren bruger en anden type mail, så kan invitationen ikke sendes. 
> 
> Da denne opgave kræver adgang for at kunne administrere brugere og licenser i Azure Active Directory, skal den bruger, der sender denne invitation, tildeles rollen **Global administrator** eller **Brugeradministrator** i Office 365 Administration. Du kan flere oplysninger i [Om administratorroller](/office365/admin/add-users/about-admin-roles) i Office 365 administratorindholdet.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Tilføjelse af din revisor til Office 365 via Azure-portal

Hvis din administrator eller videresalgspartner ikke vil bruge guiden **Inviter ekstern revisor**, kan vedkommende tilføje en ekstern bruger på Azure-portalen og tildele denne bruger licensen til den eksterne revisor. Du finder flere oplysninger under [Hurtig start: Tilføj gæstebrugere til dit katalog i Azure-portalen](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Sådan tilføjer du din revisor som gæstebruger

1. Åbn [Azure-portalen](https://portal.azure.com/).
2. Gå til venstre rude, og vælg **Azure Active Directory**.
3. Vælg **Brugere** under **Administrer**.
4. Vælg **Ny gæstebruger**.
5. Gå til siden **Ny bruger**, og vælg **Inviter bruger**, og tilføj derefter oplysninger om din eksterne revisor.  

   Du kan også inkludere en personlig velkomstmeddelelse til revisoren for at fortælle vedkommende, at du føjer ham eller hende til [!INCLUDE [prodshort](includes/prodshort.md)].

6. Vælg **Inviter** for automatisk at sende invitationen. Der vises en meddelelse øverst til højre med beskeden **Bruger er blevet inviteret**. 
7. Når du har sendt invitationen, føjes brugerkontoen automatisk til kataloget som gæst.

Derefter skal du tildele den nye gæstebruger en licens til [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Sådan giver du din revisor adgang til [!INCLUDE [prodshort](includes/prodshort.md)]

1. Gå til Azure-portalen, og vælg **Profil**og derefter **Rediger** på den bruger, der netop er tilføjet.
2. Opdater feltet **Brugsplacering** til det relevante land, og vælg derefter **Gem.**
3. Vælg **Licenser**, og åbn derefter **Tildelinger**.
4. Vælg licensen **Dynamics 365 Business Central Ekstern revisor**.  

    Hvis denne licens ikke er tilgængelig, skal du i stedet bruge en tilgængelig **Dynamics 365 Business Central for IWs**-licens.
5. Gem tildelingen.

Hvis det lykkes, tildeles licensen til gæstebrugeren, og gæstekontoen oprettes.

### <a name="importing-the-new-user-into-prodshort"></a>Import af den nye bruger til [!INCLUDE [prodshort](includes/prodshort.md)]

Revisoren modtager en e-mail, der giver vedkommende besked om, at han eller hun har fået adgang til dit Active Directory. Derefter skal du give vedkommende adgang til den rigtige virksomhed i [!INCLUDE [prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Sådan føjes revisoren til den rigtige virksomhed

1. Åbn den [!INCLUDE [prodshort](includes/prodshort.md)]-virksomhed, du vil give revisoren adgang til, på [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugere**, og vælg derefter det relaterede link.  
3. Vælg handlingen **Hent nye brugere fra Office 365**.

Denne importerer den brugerkonto, som du oprettede på Azure-portalen, til virksomheden. Du kan finde flere oplysninger under [Sådan tilføjes en bruger i Business Central](ui-how-users-permissions.md#adduser).  

Hvis du vil give adgang til flere virksomheder, skal du logge ind på hver virksomhed og gentage denne proces. Alternativt kan du opdatere rettighedsgrupperne for revisorens brugerprofil i [!INCLUDE [prodshort](includes/prodshort.md)], f.eks. ved at tildele dem *D365 Bus Premium*-brugergruppen. Du kan finde flere oplysninger i [Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md).  

## <a name="accountant-hub"></a>Accountant Hub

Hvis du er revisor og har mange kunder, kan du bruge [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] for at få et bedre overblik over dine kunder. Her har du adgang til de enkelte kunders lejer i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan bruge rollecenteret Regnskabsmedarbejder som beskrevet ovenfor. Du kan finde flere oplysninger under [Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] er i øjeblikket i offentlig prøveversion på et begrænset antal markeder.

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Finans- og kontoplanen](finance-general-ledger.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Analysere regnskaber i Excel](finance-analyze-excel.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Opsætning af pengestrømsanalyse](finance-setup-cash-flow-analyses.md)  
[Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Accountant Hub på Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
