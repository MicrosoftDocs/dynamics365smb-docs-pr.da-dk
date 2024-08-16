---
title: Tilpasse sider til roller
description: 'Få mere at vide om, hvordan du tilpasser brugergrænsefladen for en profil (rolle), så alle brugere, der har fået tildelt denne rolle, kan se et tilpasset arbejdsområde.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 06/13/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="customize-pages-for-profiles"></a>Tilpasse sider til profiler

Business Central indeholder både [tilpasning](ui-personalization-user.md) for brugere og tilpasning for administratorer. Tilpasning giver brugerne mulighed for at skræddersy deres arbejdsområde ved at justere sidelayout, så de passer til deres egne præferencer. Administratorer kan tilpasse sidelayouts til en specifik profil i henhold til forretningsroller eller afdelinger, så alle de tildelte brugere kan se den tilpassede side. Mens tilpasning giver brugerne mulighed for at vise, skjule og flytte felter og handlinger på en side, giver tilpasning ekstra muligheder. Tilpasning giver dig f.eks. mulighed for at vise felter, der findes i sidens kildetabel eller udvidelsestabeller, men som ikke er defineret i sideobjektet – hvilket ikke er muligt at tilpasse dem.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Den typiske forretningsbrug af en profil er en rolle. En profil har derfor navnet *Profil (rolle)* i brugergrænsefladen.

Sidetilpasningen begynder på siden **Profiler (roller)**, som er administratorens udgangspunkt for styring af brugerprofiler for individuelle profilkort. Ud over at tilpasse sidelayoutet kan du styre forskellige andre indstillinger for profiler på siden **Profil (rolle)** for hver profil. Du kan finde flere oplysninger i [Administrere profiler](admin-users-profiles-roles.md).

## <a name="prerequisites"></a>Forudsætninger

- Din Business Central-konto skal have angivet tilladelsen **D365-profilopsætningen** eller tilsvarende tilladelser. 

   Tilladelsessættet **D365-profilen Mgt.** omfatter kørselstilladelsen til systemobjektet **9026 Føj felt til tabel**. Hvis du ikke har denne tilladelse, har du ikke tilladelse til at tilføje felter på siden, medmindre de er defineret på sideobjektet. 

## <a name="customize-pages-for-a-profile"></a>Tilpasse sider for en profil

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Profiler (roller)**, og vælg derefter det relaterede link.
2. Marker linjen for den profil, du vil tilpasse sider for, og vælg derefter handlingen **Rediger**.
3. Vælg handlingen **Tilpas sider**.

    [!INCLUDE[prod_short](includes/prod_short.md)] åbner en ny webbrowserfane for den valgte profil, hvor banneret **Tilpasning** er aktiveret. Banneret **Tilpasning** har samme funktionalitet som banneret **Tilpas**, der er tilgængeligt for brugerne.

4. Tilpas sider efter den pågældende rolles eller afdelings behov på samme måde som en bruger gør. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

    > [!NOTE]
    > Hvis du vil navigere under tilpasningen, skal du bruge <kbd>Ctrl</kbd>+<kbd>Klik</kbd> på en handling, hvis den er fremhævet af pilespidsen.

5. Når du er færdig med at ændre layoutet for en eller flere sider, skal du vælge knappen **Udført** på banneret **Tilpasning**.
6. Luk fanen i webbrowseren.

Tilpasningen af sider er nu registreret for profilen.

## <a name="view-all-customized-pages-for-a-profile"></a>Vise alle tilpassede sider for en profil

Du kan få vist en oversigt over, hvilke sider der er tilpasset for en profil, f.eks. hvis du vil planlægge, hvilke sider, der skal tilpasses yderligere eller slettes.

- Vælg handlingen **Administrer tilpassede sider** på siden **Profil (rolle)**.

Du kan slette tilpasninger på siden **Brugerdefinerede sider**, og du kan foretage fejlfinding ved at søge efter mulige problemer.  

## <a name="delete-all-customizations-for-a-profile"></a>Slette alle tilpasninger for en profil

Du kan annullere alle tilpasninger, du har foretaget for en profil. Tilpasninger, som er introduceret med en udvidelse, og tilpasninger, der er udført af en bruger, slettes ikke. Du kan slette alle tilpasninger med en anden handling. Du kan finde flere oplysninger under [Sådan slettes alle tilpasninger, der er foretaget af en bruger](admin-users-profiles-roles.md#delete-all-personalizations-made-by-a-specific-user).

- På siden **Profil (rolle)** for en tilpasset profil skal du vælge handlingen **Fjern brugerdefinerede sider**.

Layoutet på siderne i profilen nulstilles til standardlayoutet.  

## <a name="delete-customization-for-specific-pages-for-a-profile"></a>Slette tilpasning af bestemte sider for en profil

Du kan slette enkelte sidetilpasninger, du har foretaget for en profil. Tilpasninger, som er introduceret med en udvidelse, og tilpasninger, der er udført af en bruger, slettes ikke. Du kan slette bestemte sidetilpasninger med en anden handling. Du kan finde flere oplysninger under [Sådan slettes tilpasninger for bestemte sider](admin-users-profiles-roles.md#delete-personalizations-for-specific-pages).

1. Vælg handlingen **Administrer tilpassede sider** på siden **Profil (rolle)**.
2. På siden **Brugerdefinerede sider** skal du vælge en eller flere linjer for sidetilpasninger, som du vil slette, og derefter vælge handlingen **Slet**.

Layoutet på de valgte sider justeres til de ændringer, du har foretaget.

## <a name="add-a-field"></a>Tilføje et felt

Du føjer felter til siden fra ruden **Føj felt til side**, som du kan åbne ved at vælge handlingen **+ Felt**, når du er i tilpasningstilstand. Det er vigtigt at forstå, at ruden **Føj felt til side** bruges til at vise felter, der allerede findes enten på siden og dens kildetabeller, men som i øjeblikket er skjult. Du kan ikke oprette nye felter.

Ruden **Føj felt til side** viser alle de felter, der kan vises på siden. Felter er opdelt i følgende kategorier afhængigt af selve sidens underliggende design, kildetabel og udvidelser:

|Kategori|Beskrivelse|
|-|-|
|Tabelfelter, der ikke er på sideobjektet|Indeholder felter, der er defineret i basistabellen eller udvidelsestabellerne, men som ikke er defineret på siden. Værktøjstippet til disse felter indeholder etiketten **Defineret af tabellen**.<br><br>|
|Sidefelter, der er bundet til en tabel|Indeholder felter, der er defineret i basistabellen eller tabeludvidelserne, og som også er defineret på siden som enten viste eller skjulte. Værktøjstippet til disse felter indeholder etiketten **Defineret af siden**.|
|Sidefelter er ikke bundet til en tabel| Felter, der er defineret på siden og ikke i basistabellen eller udvidelsestabeller. Disse felter bruges typisk til variabel eller beregning. Værktøjstippet til disse felter indeholder etiketten **Defineret af siden**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Brug filterknappen over listen til at ændre, hvilken kategori af felter der vises i ruden **Føj felt til side**.  

:::image type="content" source="media/customization-filter.svg" alt-text="Viser filterknappen i ruden Tilføj et felt i tilpasningstilstand.":::
 
### <a name="add-table-field-thats-not-on-the-page-object"></a>Tilføj tabelfelt, der ikke er på sideobjektet

Hvis du vil gøre et tabelfelt tilgængeligt på en side for brugerne, skal du først føje det til siden. Når du har tilføjet feltet, kan brugerne vælge at vise eller skjule feltet ved hjælp af tilpasning. Du kan tilføje et felt på flere måder.

- En måde er at trække det fra ruden **Tilføj felt til side** til den ønskede placering.
- Du kan også markere feltet i ruden for at få vist den anbefalede placering på siden. Gå derefter til feltplaceringen på siderne, vælg pilespidsen, og vælg derefter **Tilføj**. 

Når feltet er tilføjet, skifter værktøjstippet til feltet i ruden **Føj felt til side** til **Defineret af siden**.

> [!NOTE]
> Det tilføjede felt er låst fra redigering og kan ikke låses op.

## <a name="remove-a-field"></a>Fjerne et felt

Hvis du har tilføjet et tabelfelt, der oprindeligt ikke var på sideobjektet, kan du fjerne det igen. At fjerne et felt er anderledes end at skjule det. Når du skjuler et felt, kan brugerne stadig vise det på deres arbejdsområde via tilpasning. Men hvis du fjerner et felt, kan brugerne ikke længere vise eller skjule feltet. Hvis feltet aktuelt vises i en brugers arbejdsområde, forsvinder det fra brugerens arbejdsområde, når du fjerner det. 

Hvis du vil fjerne et felt, skal du markere pilespidsen på feltet på siden og derefter **Fjern**. Hvis du ikke kan finde feltet, skal du markere det i ruden **Føj felt til side** for at angive dets skjulte placering. 

> [!IMPORTANT]
> Når du fjerner et felt, slettes data, der er gemt i feltet, eller dets kildetabeller ikke. Det fjerner bare feltet fra visningen. 

## <a name="lock-and-unlock-editing"></a>Lås og lås op for redigering

Tilpasning giver dig mulighed for at låse (tillade redigering) eller låse op for redigering (forhindre redigering) af de fleste felter på en side. Hvis du vil låse eller låse redigering op, skal du markere feltet på siden, vælge pilespidsen og derefter vælge **Lås redigering** eller **Lås redigering op**. Det er vigtigt at huske på nogle få regler om låsning og oplåsning af felter:

- Felter, der oprindeligt ikke fandtes i sideobjektet, men som blev føjet til siden ved tilpasning, er altid låst og kan ikke låses op ved hjælp af tilpasning.
- Feltets design kan også forhindre, at det redigeres. Hvis AL-udvikleren angiver feltets [redigerbare egenskab](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) til `false`, er det altid låst og kan ikke låses op.
- Det er vigtigt at bemærke, at låseredigeringsfunktionen er beregnet til at hjælpe med nøjagtigheden, konsistensen og pålideligheden af data. Det er ikke beregnet til at sikre dataintegritet.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## <a name="important-information-and-tips"></a>Vigtig information og tips

- Det er ikke sikkert, at alle tabelfelter kan tilpasses fra ruden **Føj felt til side**. Udvikleren af en tabel kan vælge at forhindre, at et felt vises i tilpasning, ved at angive feltets [AllowInCustomization-egenskab](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) til `Never`.
- Du kan ikke tilpasse en side, der er i [analysetilstand](analysis-mode.md). Kontakten **Analysér** er deaktiveret. Hvis du skifter til tilpasningstilstand, mens siden er i analysetilstand, deaktiveres analysetilstand automatisk. 
- Nogle sider har flere sidefelter, der er knyttet til den samme kildetabel. Ruden **Føj felt til side** viser alle disse sidefelter uafhængigt af hinanden. Du kan vise, skjule eller flytte disse felter uafhængigt af hinanden, uden at det påvirker de andre.
- Hvis en del eller gruppe er skjult, kan du stadig identificere skjulte felter i delen eller gruppen, men du kan ikke tilføje, flytte eller vise felter i delen eller gruppen, før de er gjort synlige. 
## <a name="see-also"></a>Se også

[Tilpasse arbejdsområdet](ui-personalization-user.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
