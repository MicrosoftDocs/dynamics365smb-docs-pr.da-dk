---
title: Administrere arbejde på tværs af flere regnskaber i virksomhedshub
description: 'Få mere at vide om den virksomhedshub i Dynamics 365 Business Central, som du bruger til at styre dit arbejde på tværs af flere regnskaber.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
---

# Administrere arbejde på tværs af flere regnskaber i virksomhedshub

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Nogle personer arbejder i flere firmaer i [!INCLUDE [prod_short](includes/prod_short.md)], og nogle arbejder også i mere end én organisation, f.eks. eksterne bogholdere eller medarbejdere og ledere af virksomheder med flere datterselskaber. For disse brugere og mange andre kan virksomhedshubben bruges som en landingsside, der giver en økonomisk oversigt over virksomheder og miljøer. Den giver brugerne et værktøj til styring af arbejde på tværs af de forskellige miljøer, som de arbejder i, på tværs af firmaer, miljøer og områder.  

Du kan få adgang til firma hubben ved at skifte til rollen **Virksomhedshub** i Mine indstillinger eller ved at åbne siden **Virksomhedshub** direkte. Du kan udføre samme arbejde begge steder, men handlinger placeres lidt anderledes i menuer.  

[![Viser siden med virksomhedshub, der viser alle virksomheder.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> Du kan tilslutte virksomhedens hub til så mange virksomheder, du har brug for. Du kan dog kun tilslutte virksomhedens hub til virksomheder, der er værtsbaseret på [!INCLUDE [prod_short](includes/prod_short.md)]-internettet.

## Hjemmeside for virksomhedshub

Hvis du bruger **Virksomhedshub**-rollen, viser din startside en liste over virksomheder, du har adgang til, herunder oplysninger om nøglepunkter med interesse data og links til at åbne hvert regnskab. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Vælg **Virksomhedshub** for at åbne den virksomheds hub, hvor du kan arbejde mere snævert sammen med de enkelte regnskaber.  

> [!TIP]
> Du kan få adgang til et bestemt regnskab i [!INCLUDE [prod_short](includes/prod_short.md)] ved at vælge navnet på virksomheden eller vælge menupunktet **Gå til virksomhed** – du bliver automatisk logget på en ny fane i browseren.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Handlinger for en virksomhed, der er angivet i virksomhedshubben.":::

Du kan tilføje nye virksomheder, f.eks. Når du får fat på en ny kunde, eller når virksomheden tilføjer et nyt datterselskab. Du kan finde flere oplysninger i [Tilføj firmaer til virksomhedshub](company-hub-add-company.md).  

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

## Tildelte opgaver

I [!INCLUDE [prod_short](includes/prod_short.md)] kan du tildele opgaver til dig selv og andre, og andre kan tildele opgaver til dig. Virksomhedhubben giver dig en oversigt over tildelte opgaver for hver virksomhed, og du kan også få vist en oversigt over alle tildelte opgaver ved at vælge **Mine brugeropgaver** på siden **Start**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### Mine brugeropgaver

Listen **Mine brugeropgaver** hjælper dig med at prioritere din dag ved at vise yderligere oplysninger om opgaver, der er tildelt til dig på tværs af alle dine virksomheder.  

Du kan f.eks. sortere efter forfaldsdato eller andre typer data, der hjælper dig med at prioritere din dag. Listen viser som standard alle opgaver, der er tildelt til dig, men du kan oprette filtre, så der f.eks. kun vises opgaver, der er markeret som høj prioritet.  

For at hente en opgave skal du vælge den på listen over ventende brugeropgaver. På båndet åbner linket **Gå til opgaveelementet** den side, hvor du kan udføre arbejdet.  

Når du har fuldført en opgave, skal du markere den som fuldført.  

Du kan finde flere oplysninger om virksomheder og miljøer i [Miljølinks](company-hub-add-company.md#environment-links).  

## Få adgang til virksomhedshubben

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

For at der kan opnås adgang til virksomhedens hub, skal du have adgang via enten *D365-VIRKSOMHEDSHUB* eller via *D365 VIRKSOMHEDSHUB*-tilladelsessættet. Du skal også have adgang til de virksomheder, der er opført i virksomhedens hub, hvilket betyder, at du skal være en bruger af disse virksomheder. Du kan finde flere oplysninger i [Oprette brugere i henhold til licenser](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Virksomhedens hub er en liste over hele virksomheden, så enhver bruger, der får adgang til virksomhedens hub, kan se alle regnskaber i deres egen [!INCLUDE [prod_short](includes/prod_short.md)]-lejer og alle KPI'er for de virksomheder, de har adgang til.

Hvis du ikke kan finde virksomhedens hub, og du ved, at du har fået adgang til den, skal du kontakte administratoren, hvis den pågældende virksomheds hub står på siden **Administration af udvidelse**. Du kan finde flere oplysninger i [Tilpasse Business Central ved hjælp af udvidelser](ui-extensions.md).  

## Konfigurere virksomhedshub

Hvis du vil begynde at bruge virksomhedens hub, skal du tilføje et eller flere regnskaber til dit dashboard. Du kan finde flere oplysninger i [Tilføj firmaer til virksomhedshub](company-hub-add-company.md).  

Men hvis du vil tilføje et regnskab, skal du have fået adgang til en eller flere forekomster af [!INCLUDE [prod_short](includes/prod_short.md)] ud over den virksomhed, som du bruger virksomhedshubben i.  

Hvis du f.eks. er bogholder, kan dine klienter invitere dig til deres [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Inviter din eksterne revisor til at deltage i din Business Central](finance-accounting.md#inviteaccountant).  

Administratorer kan bruge den samme assisterede opsætningsvejledning til at føje dig til deres [!INCLUDE [prod_short](includes/prod_short.md)], eller de kan føje dig til den relevante Microsoft Entra-konto i Microsoft 365 Administration. Du kan finde flere oplysninger i [Administrere brugere og grupper](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## Se også

[Tilføj firmaer til virksomhedens hub](company-hub-add-company.md)  
[Revisoroplevelser i Business Central](finance-accounting.md)  
[Virksomhedshub til udvidelsen af Business Central](ui-extensions-company-hub.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]