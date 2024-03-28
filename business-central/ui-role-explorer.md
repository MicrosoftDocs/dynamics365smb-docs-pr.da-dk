---
title: Udforske og navigere på sider pr. rolle
description: 'Du kan få vist en oversigt over alle de forretningsfunktioner, der er tilgængelige for din rolle, og for andre roller med Rollestifinder.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="finding-pages-with-the-role-explorer"></a>Søge efter sider med Rollestifinder

Du kan få vist en oversigt over alle de forretningsfunktioner, der er tilgængelige for din rolle, og for andre roller, hvis du går et trin videre. I følgende dokumentation henvises der til denne funktionsoversigt som *Rollestifinder*.

Hvert element i Rollestifinder er en handling, der åbner en side. Derfor kan du også bruge funktionen Rollestifinder til at navigere i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>Åbne rollestifinder

Du kan åbne Rollestifinder fra rollecenteret og alle listesider og fra vinduet **Fortæl mig**.

- I dit rolle Center eller på en listeside vælges ![Menuknappen.](media/ui_menu_button.png "Menuknap") til højre for navigationslinjen, eller vælg på <kbd>Shift</kbd>+<kbd>F12</kbd>.
- I vinduet **Fortæl mig** skal du vælge handlingen **udforskning** nederst.

Når du åbner rollecenteret første gang, vises der links til de fleste funktioner, der er tilgængelige for din rolle.

## <a name="navigate-features"></a>Navigeringsfunktioner

De handlinger, der åbner sider, er organiseret under noder, der er navngivet efter funktionerne eller funktionalitetsområderne. Hver node kan skjules eller udvides individuelt, og du kan skjule/udvide alle noder sammen.

- Hvis du vil udvide/skjule en individuel node, skal du vælge noden. Dette gælder for noder på øverste niveau og underordnede noder.
- Hvis du vil udvide/minimere alle noder på øverste niveau på siden, men lade undernoderne være, skal du vælge **...** øverst og derefter vælge **Udvid** eller **Skjul**.
- Hvis du vil udvide/minimere alle noder på øverste niveau og under-noder, skal du vælge **...** øverst og derefter vælge **Udvid alle** eller **Skjul alle**.

## <a name="search-for-features"></a>Søge efter funktioner

Hvis du hurtigt vil finde funktioner, skal du vælge **Søg** og derefter skrive et ord eller en sætning til den funktion, som du forsøger at finde. Den tilsvarende tekst vil derfor blive fremhævet i rollecenteret. Hvis en funktion er skjult fra Vis i skjult node, er den skjulte node markeret med en prik. 

## <a name="explore-other-roles"></a>Udforsk andre roller

Hvis du vil udforske andre roller end din egen, skal du vælge **Gennemse flere roller**. Rollecenteret viser hver rolle under sin egen overskrift med hyperlinks til de tilhørende funktioner. Du kan derefter navigere og finde funktioner på samme måde, som når du udforsker din rolle.

> [!NOTE]
> Du kan kun se roller, der er indstillet til at blive vist i rolle Stifinder. Så hvis du ikke kan se den rolle, som du forventede at se, er der sandsynligvis ikke oprettet noget. Du kan finde flere oplysninger i [Administrere profiler](admin-users-profiles-roles.md). 

Når du udforsker andre roller, kan du også indsnævre udforskningen ved at bruge **Rapport og analyse** og **Administration**-handlinger øverst i rollecenteret.

- **Rapport og analyse** viser kun de funktioner, der er kategoriseret som rapporter og analysefunktioner.
- **Administration** viser kun de funktioner, der er kategoriseret som administrationsfunktioner.

> [!TIP]
> For udviklere kategoriserer du sider og rapporter ved at angive [egenskaben UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) i objektets AL-kode.
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Udvide/skjule noder i Rollestifinder

De handlinger, der åbner sider, er organiseret under noder, der er navngivet efter funktionerne eller funktionalitetsområderne. Hver node kan skjules eller udvides individuelt, og du kan skjule/udvide alle noder sammen.

- Hvis du vil udvide/skjule en node, skal du vælge noden. Dette gælder for noder på øverste niveau og underordnede noder.
- Hvis du vil udvide/skjule alle noder på øverste niveau på siden, skal du vælge handlingen **Vis** eller **Skjul** i øverste højre hjørne.
- Benyt en af følgende fremgangsmåder for at udvide/minimere alle noder på øverste niveau og alle underordnede noder under den:
  - Vælg <kbd>Ctrl</kbd>+<kbd>Skift</kbd>-tasterne, mens du vælger handlingen **Udvid** eller **Skjul** i øverste højre hjørne.
  - Vælg **...** i øverste højre hjørne, og vælg derefter handlingen **Udvid alle** eller **Skjul alle**.

## <a name="see-also"></a>Se også
[Søge efter sider og oplysninger med Fortæl mig](ui-search.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
