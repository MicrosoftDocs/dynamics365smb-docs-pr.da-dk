---
title: Administrere arbejde på tværs af flere regnskaber i virksomhedshub
description: Få mere at vide om den virksomhedshub i Dynamics 365 Business Central, som du bruger til at styre dit arbejde på tværs af flere regnskaber.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ed69f86a941a216ef948488d3756c06f298549d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927628"
---
# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Administrere arbejde på tværs af flere regnskaber i virksomhedshub

Nogle personer arbejder i flere firmaer i [!INCLUDE [prodshort](includes/prodshort.md)], og nogle arbejder også i mere end én organisation, f. eks. eksterne bogholdere eller medarbejdere og ledere af virksomheder med flere datterselskaber. For disse brugere og mange andre er virksomhedens hub den samme som en landingsside til styring af arbejde på tværs af de forskellige miljøer, som de arbejder i, på tværs af firmaer, miljøer og områder.  

Du kan få adgang til firma hubben ved at skifte til rollen **Virksomhedshub** i Mine indstillinger eller ved at åbne siden **Virksomhedshub** direkte. Du kan udføre samme arbejde begge steder, men handlinger placeres lidt anderledes i menuer.  

## <a name="company-hub-home-page"></a>Hjemmeside for virksomhedshub

Hvis du bruger **Virksomhedshub**-rollen, viser din startside en liste over virksomheder, du har adgang til, herunder oplysninger om nøglepunkter med interesse data og links til at åbne hvert regnskab. Du kan tilpasse dashboardet for at få vist de datapunkter, som du vil se, ved at tilføje eller fjerne kolonner. Du kan f.eks. få vist skatter, der er forfaldne til betaling, hvor mange åbne salgsdokumenter, virksomheden har, eller antallet af købsfakturaer, der forfalder næste uge. Du kan konfigurere visningen efter behov. Hvis du har tilføjet mange virksomheder, kan du bruge filtre til at sortere visningen.  

Vælg **Virksomhedshub** for at åbne den virksomheds hub, hvor du kan arbejde mere snævert sammen med de enkelte regnskaber.  

> [!TIP]
> Du kan få adgang til et bestemt regnskab i [!INCLUDE [prodshort](includes/prodshort.md)] ved at vælge navnet på virksomheden eller vælge menupunktet **Gå til virksomhed** – du bliver automatisk logget på en ny fane i browseren.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Handlinger for en virksomhed, der er angivet i virksomhedshubben":::

Du kan tilføje nye virksomheder, f. eks. Når du får fat på en ny kunde, eller når virksomheden tilføjer et nyt datterselskab. Du kan finde flere oplysninger i [Tilføj firmaer til virksomhedshub](company-hub-add-company.md).  

> [!TIP]
> Hvis du vil opdatere dataene i virksomhedshub, skal du have adgang til dataene i de virksomheder, som dataene stammer fra.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Tildelte opgaver

I [!INCLUDE [prodshort](includes/prodshort.md)] kan du tildele opgaver til dig selv og andre, og andre kan tildele opgaver til dig. Virksomhedhubben giver dig en oversigt over tildelte opgaver for hver virksomhed, og du kan også få vist en oversigt over alle tildelte opgaver ved at vælge **Mine brugeropgaver** på siden **Start**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Mine brugeropgaver

Listen **Mine brugeropgaver** hjælper dig med at prioritere din dag ved at vise yderligere oplysninger om opgaver, der er tildelt til dig på tværs af alle dine virksomheder.  

Du kan f.eks. sortere efter forfaldsdato eller andre typer data, der hjælper dig med at prioritere din dag. Listen viser som standard alle opgaver, der er tildelt til dig, men du kan oprette filtre, så der f.eks. kun vises opgaver, der er markeret som høj prioritet.  

For at hente en opgave skal du blot vælge den på listen over ventende brugeropgaver. På båndet åbner linket **Gå til opgaveelementet** den side, hvor du kan udføre arbejdet.  

Når du har udført en opgave, skal du blot markeres som fuldført.  

Du kan finde flere oplysninger om virksomheder og miljøer i [Miljølinks](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Få adgang til virksomhedshubben

For at der kan opnås adgang til virksomhedens hub, skal du have adgang via enten *D365-VIRKSOMHEDSHUB* eller via *D365 VIRKSOMHEDSHUB*-tilladelsessættet. Du skal også have adgang til de virksomheder, der er opført i virksomhedens hub, hvilket betyder, at du skal være en bruger af disse virksomheder. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Virksomhedens hub er en liste over hele virksomheden, så enhver bruger, der får adgang til virksomhedens hub, kan se alle regnskaber i deres egen [!INCLUDE [prodshort](includes/prodshort.md)]-lejer og alle KPI'er for de virksomheder, de har adgang til.

Hvis du ikke kan finde virksomhedens hub, og du ved, at du har fået adgang til den, skal du kontakte administratoren, hvis den pågældende virksomheds hub står på siden **Administration af udvidelse**. Du kan finde flere oplysninger under [Tilpasse Business Central ved hjælp af udvidelser](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Konfigurere virksomhedshub

Hvis du vil begynde at bruge virksomhedens hub, skal du tilføje et eller flere regnskaber til dit dashboard. Du kan finde flere oplysninger i [Tilføj firmaer til virksomhedshub](company-hub-add-company.md).  

Men hvis du vil tilføje et regnskab, skal du have fået adgang til en eller flere forekomster af [!INCLUDE [prodshort](includes/prodshort.md)] ud over den virksomhed, som du bruger virksomhedshubben i.  

Hvis du f. eks. er bogholder, kan dine klienter invitere dig til deres [!INCLUDE [prodshort](includes/prodshort.md)]. Du kan finde flere oplysninger i [Inviter din eksterne revisor til at deltage i din Business Central](finance-accounting.md#inviteaccountant).  

Administratorer kan bruge den samme assisterede opsætningsvejledning til at føje dig til dem [!INCLUDE [prodshort](includes/prodshort.md)], eller de kan føje dig til den relevante Azure AD-konto i Microsoft 365 Administration. Du kan finde flere oplysninger i [Administrere brugere og grupper](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Se også

[Tilføj firmaer til virksomhedens hub](company-hub-add-company.md)  
[Revisoroplevelser i Business Central](finance-accounting.md)  
[Virksomhedshub til udvidelsen af Business Central](ui-extensions-company-hub.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
