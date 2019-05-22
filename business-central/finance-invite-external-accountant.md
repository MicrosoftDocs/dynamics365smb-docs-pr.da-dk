---
title: Tilføje din eksterne revisor til Business Central | Microsoft Docs
description: Få at vide, hvordan du inviterer din eksterne revisor indenfor i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 04/01/2019
ms.author: edupont
redirect_url: finance-accounting
ms.openlocfilehash: 4b56e6923d1d554bb27a4c0f82f0226dea51f280
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446895"
---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitere din eksterne revisor indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruger en ekstern revisor til at administrere dine regnskaber og regnskabsaflæggelse, kan du invitere ham eller hende indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)], så de kan samarbejde med dig om dine regnskabsdata.

Når din revisor har fået adgang til dit [!INCLUDE[d365fin](includes/d365fin_md.md)], kan han eller hun bruge rollecenteret **Regnskabsmedarbejder**, der giver nem adgang til de mest relevante sider for deres arbejde.  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Invitere din revisor indenfor i din [!INCLUDE[d365fin](includes/d365fin_md.md)]

Vi har gjort det nemt for dig at invitere din eksterne revisor. Du skal blot åbne siden **Brugere** og derefter vælge handlingen **Inviter ekstern revisor** på båndet. En mail er gjort klar til dig, så du blot skal tilføje din revisors arbejds-mail og sende invitationen.  

![Inviter din revisor indenfor](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Dette kræver, at du har oprettet SMTP-mail. Du kan gøre dette selv eller bede din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner. Desuden du skal være logget på [!INCLUDE[d365fin](includes/d365fin_md.md)] som brugeradministrator, og ikke som virksomhedsejer eller andre brugere. Endelig skal du have forladt prøvevirksomheden, så du har en Azure Active Directory-administrator.  

> [!IMPORTANT]  
> Revisorens mailadresse skal være en arbejdsadresse, der er baseret på Azure Active Directory. Hvis revisoren bruger en anden type mail, så kan invitationen ikke sendes.  

### <a name="separate-license"></a>Separat licens
Revisoren føjes til din Active Directory-lejer i baggrunden. Administratoren kan kontrollere, at revisoren har accepteret invitationen og tildeles den rigtige licens. Fremgangsmåden for at gøre dette afhænger af, hvilken kontotype du brugte, da du tilmeldte dig [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette emne er baseret på brugen af en Office 365-konto, som bruger Microsoft Azure Active Directory.  

Hvis du har aktiveret dit abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] og ikke længere bruger evalueringsregnskabet, du har en Azure Active Directory-lejer. Administratoren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partneren administrerer denne lejer på [Azure-portalen](https://portal.azure.com). Det er her, at nye brugere tilføjes, og licenser anvendes og fjernes. Du kan finde flere oplysninger i [Oversigt over Microsoft Azure-portalen](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

En af licenstyperne for [!INCLUDE[d365fin](includes/d365fin_md.md)] er *Ekstern revisor*-licensen. Denne licenstype er beregnet til brugere som f.eks. eksterne revisorer. Det betyder, at du ikke behøver at købe en ekstra plads i dit aktuelle Active Directory eller bruge en af dine eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugerkonti på en ekstern revisor. F.eks. hvis dit aktuelle Office 365-abonnement omfatter 10 brugere for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du bruger i øjeblikket 10 *Fuld bruger*-licenser, kan administratoren blot føje din eksterne revisor som en gæstebruger på Azure-portalen og tildele denne bruger licensen *Ekstern revisor* uden ekstra omkostninger. Du kan dog kun have én bruger med *Ekstern revisor*-licensen. Hvis du vil tilføje flere brugere, skal du opdatere dit Office 365-abonnement tilsvarende.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere mail manuelt eller ved hjælp af den assisterede opsætning](admin-how-setup-email.md)  
[Revisoroplevelser i Business Central](finance-accounting.md)  
[Business Central for revisorer på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
