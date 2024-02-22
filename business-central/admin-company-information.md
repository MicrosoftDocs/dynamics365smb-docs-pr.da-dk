---
title: Oversigt over virksomhedsoplysninger
description: 'På siden virksomhedsoplysninger kan du angive grundlæggende oplysninger om en forretningsenhed, f. eks. navn, adresse og leveringsoplysninger.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 09/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="company-information-overview"></a>Oversigt over virksomhedsoplysninger

[!INCLUDE[prod_short](includes/prod_short.md)] organiserer forretningsenheder i *virksomheder*. For hvert regnskab skal du udfylde nogle af de grundlæggende virksomhedsoplysninger og relevante oplysninger på siden **Virksomhedsoplysninger**. Oplysningerne på siden [**Virksomhedsoplysninger**](https://businesscentral.dynamics.com/?page=1) bruges til at udskrive emner såsom fakturaoverskrifter. Du kan oprette mere end ét firma, f.eks. et moderselskab og et datterselskab.  

Hvis virksomhedens lager ligger et andet sted end hovedkontoret, kan du udfylde de forskellige leveringsfelter og feltet **Lokationskode** i oversigtspanelet **Levering**. Så vil oplysningerne i disse felter udskrives på f.eks. købsordrer, så leverandørerne leverer til den rigtige lokation.  

Tabellen **Virksomhedsoplysninger** skal sammen med tabellen **Opsætning af Finans** udfyldes for hver virksomhed, du opretter i programmet. Du skal også oprette hvert område i [!INCLUDE [prod_short](includes/prod_short.md)], f. eks. siden **Salgsopsætning** for hvert firma. Få mere at vide i [Oversigt over opgaver til opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

Siden **virksomhedsoplysninger** indeholder forskellige felter og oversigtspaneler, afhængigt af dit land/område. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] I følgende tabel beskrives de mest almindelige oversigtspaneler.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Når du har udfyldt oplysningerne, kan du lukke siden.  

## <a name="working-with-multiple-companies"></a>Arbejde med flere virksomheder

Hvis [!INCLUDE [prod_short](includes/prod_short.md)] indeholder flere virksomheder, vil brugerne muligvis gerne bruge *virksomhedskort* til hurtigt at identificere og holde styr på, hvilken virksomhed de aktuelt arbejder i. Du kan finde flere oplysninger i [Vise et virksomhedskort](#badge).

Der er nogle få funktioner, som du kan bruge til at skifte mellem virksomheder, f.eks. virksomhedsskifteren (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Få mere at vide i [Skifte til et andet firma eller miljø](ui-organization-switch.md).

## <a name="display-a-company-badge"></a><a name="badge"></a>Vise et virksomhedskort

Hvis der er mere end ét firma eller miljø, kan du se virksomhedsskifteren øverst til højre på applinjen nær søgeikonet. Som standard bruger virksomhedsskifteren et standardfirmaikon, f.eks ![firmaikonet Starter.](media/ui-experience/company-icon.png "Viser ikonet for virksomhedsskifteren, der bruges, når der er et enkelt miljø") og ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Viser ikonet for virksomhedsskifteren, der bruges, når der er flere miljøer").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Viser ikonet for virksomhedsskifteren i overskriften for Business Central-klienten.":::  

Fra og med udgivelsesbølge 2 i 2023, version 23, vises firmabadget på browserfanen, når du bruger webklienten. Det er også inkluderet i sidelinks, som du [kopierer og indsætter](across-share-data-features.md#copying-a-link) i RTF-editorer, som Word, Outlook og Teams.
 
### <a name="set-the-company-badge"></a>Konfigurere virksomhedsbadge

Du kan bruge siden **Virksomhedsoplysninger** til at erstatte standardfirmaikonet med et brugerdefineret kort på hver enkelt virksomhed, hvis virksomhedens kort gør det nemmere for brugerne at identificere den virksomhed, som de arbejder i.

1. I oversigtspanelet **Virksomhedskort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Når du har gjort det, skal du opdatere browseren (vælg <kbd>Ctrl</kbd>+<kbd>F5</kbd>) for at opdatere kortet i klienten.  

> [!NOTE]
> Virksomhedsskifteren blev introduceret i 2022 udgivelsesbølge 2, version 21. I tidligere versioner bruges virksomhedskortet ikke til at skifte virksomhed. Det vises øverst til højre på de fleste sider, selvom der kun er én virksomhed. Hvis du vælger det, vises hele firmanavnet og miljønavnet.

## <a name="change-company-display-name"></a>Ændre virksomheds viste navn

Virksomhedsnavnet vises altid i øverste venstre hjørne og fungerer som en handling, som du kan vælge for at gå tilbage til rollecenteret. Du kan ændre dette navn på siden **Virksomhedsoplysninger**.

1. Vælg ![ikonet Tandhjul for at åbne menuen Indstillinger.](media/ui-experience/settings_icon_small.png) ikon, og vælg derefter **Virksomhedsoplysninger**.
2. I feltet **Navn** skal du angive det nye virksomhedsnavn.
3. Forlad siden. Systemet genstarter og viser den nye virksomhed i øverste venstre hjørne.

## <a name="experience"></a>Oplevelse

Standardbrugeroplevelsen af en [!INCLUDE [prod_short](includes/prod_short.md)]-prøveversion viser ikke alle egenskaber. Du kan skifte til den fulde oplevelse på siden **Virksomhedsoplysninger**.  

Du kan finde flere oplysninger i [Ændre, hvilke funktioner der vises](ui-experiences.md).  

## <a name="see-also"></a>Se også

[Oversigt over opgaver til opsætning af [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Virksomhedsoplysninger til Hurtig start](quick-start-company-information.md)  
[Konfigurere virksomhedsoplysninger i Italien](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Ændre grundlæggende indstillinger](ui-change-basic-settings.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Oprettelse af nye virksomheder](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
