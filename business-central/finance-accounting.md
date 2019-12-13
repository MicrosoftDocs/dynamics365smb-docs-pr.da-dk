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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896129"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Revisoroplevelser i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Enhver virksomhed skal føre regnskab og godkende det. Nogle virksomheder benytter en ekstern revisor, mens andre har kvalificerede regnskabsmedarbejdere. Uanset hvilken model du benytter, kan du bruge rollecenteret **Regnskabsmedarbejder** som din startside i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra kan du få adgang til alle sider, du skal bruge i dit arbejde.  

## <a name="accountant-role-center"></a>Rollecenteret Regnskabsmedarbejder
Rollecenteret er et dashboard med aktivitetsfelter, der viser nøgletal i realtid og giver dig hurtig adgang til data. På båndet øverst på siden har du adgang til flere handlinger, f.eks. åbning af mest almindeligt brugt regnskabsrapporter og kontoudtog i Excel. I navigationsruden øverst kan du hurtigt skifte mellem de lister, du bruger mest. Her vises andre områder, f.eks. **Bogførte dokumenter** med de forskellige typer dokumenter, som firmaet har bogført.  

Hvis du ikke kender [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du åbne en liste over videoer direkte fra dit rollecenter. Du kan også starte en guide, som f.eks. **Introduktion**, der udpeger vigtige områder.  

## <a name="inviteaccountant"></a>Inviter din eksterne revisor indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan du invitere ham eller hende indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)], så de kan samarbejde med dig om dine regnskabsdata.

Når din revisor har fået adgang til dit [!INCLUDE[d365fin](includes/d365fin_md.md)], kan han eller hun bruge rollecenteret **Regnskabsmedarbejder**, der giver nem adgang til de mest relevante sider for deres arbejde.  

Vi har gjort det nemt for dig at invitere din eksterne revisor. Du skal blot åbne siden **Brugere** og derefter vælge handlingen **Inviter ekstern revisor** på båndet. En mail er gjort klar til dig, så du blot skal tilføje din revisors arbejds-mail og sende invitationen.  
> [!Note]  
> Dette kræver, at du har oprettet SMTP-mail. Du kan finde flere oplysninger i [Konfigurer mail](admin-how-setup-email.md).   

![Inviter din revisor indenfor](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Revisorens mailadresse skal være en arbejdsadresse, der er baseret på Azure Active Directory. Hvis revisoren bruger en anden type mail, så kan invitationen ikke sendes.  

### <a name="behind-the-scenes"></a>Bag kulisserne
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder tre licenser af typen Ekstern revisor. Hvis din virksomhed bruger en ekstern revisor, kan du give dem adgang til din [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at tildele dem en sådan licens. Du kan finde flere oplysninger om licenser i [Licensvejledning til Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590). 

Hvis dit abonnement stadig har en tilgængelig licens, kan din administrator eller din videresalgspartner tilføje en ekstern bruger via Azure-portalen og tildele denne bruger licensen for den Eksterne revisor. Du kan flere oplysninger i [Tilføj Azure Active Directory B2B-samarbejdsbrugere i Azure-portalen](/azure/active-directory/b2b/add-users-administrator).

Du kan derefter invitere revisoren inde fra [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge den assisterede opsætningsvejledning **Inviter Ekstern revisor**. Men da denne opgave kræver adgang for at kunne administrere brugere og licenser i Azure Active Directory, skal den bruger, der sender denne invitation, tildeles rollen **Global administrator** eller **Brugeradministrator** i Office 365 Administration. Du kan flere oplysninger i [Om administratorroller](/office365/admin/add-users/about-admin-roles) i Office 365 administratorindholdet. 

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
