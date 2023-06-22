---
title: Sandkassemiljøer
description: 'Få mere at vide om, hvordan et dedikeret miljø kan gøre det mere sikkert at udforske, lære, afprøve, udvikle, foretage fejlfinding og teste Business Central.'
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sandbox, demo, develop'
ms.date: 12/20/2021
ms.author: solsen
---
# <a name="sandbox-environments-in-includeprodshortincludesprodshortmd" />Sandkassemiljøer i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] online kan du nemt oprette et sikkert miljø, hvor du kan teste, træne eller foretage fejlfinding uden at forstyrre virksomhedens arbejdsprocesser eller forretningsdata. Et sådant ikke-produktionsmiljø kaldes en *sandkasse*. Isoleret fra produktion er et sandkassemiljø stedet, hvor du sikkert kan udforske, lære, demonstrere, udvikle og teste tjenesten uden risiko for at påvirke data og indstillinger i dit produktionsmiljø.  

> [!TIP]
> Har du hentet denne artikel, efter at du har valgt navnet på dit [!INCLUDE [prod_short](includes/prod_short.md)]-miljø i øverste linje? Du kan i øjeblikket ikke ændre navnet eller miljøet på måde. Du skal i stedet bede administratoren om at ændre navnet eller bede vedkommende om at dele linket med et andet miljø.

Administratoren administrerer sandkassemiljøer i [Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Hvis du f.eks. vil oprette en sandkasse til benchmarking, kan administratoren oprette et dedikeret miljø i administrationscenteret. Du kan finde flere oplysninger i [Produktions- og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types) i indholdet til udviklere og og administration.  

Du kan også trygt bruge sandkasser til træning, f.eks. ved at følge en læringssti fra [Microsoft-træning](/training/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), da det er et sikkert miljø at eksperimentere i. Hvis noget går galt, skal du bare slette sandkassen og starte forfra.  

Når du er færdig, kan du fjerne sandkassen via Administrationscenter.  

> [!NOTE]
> Teknisk set er sandkassemiljøer meget forskellige fra produktionsmiljøer. Administratoren kan oprette en sandkasse, der indeholder produktionsdata, men stadig er en sandkasse, og du kan f. eks. ikke anmode om eksport af databaser. Du kan finde flere oplysninger i [Sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) i indholdet til udviklere og og administration.

Sandkassemiljøet er ikke mindst anvendelig, fordi det indeholder et par praktiske funktioner:

* [Udvidet brugeroplevelse](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Designer](#designer)  

## <a name="advanced-user-experience" />Udvidet brugeroplevelse

Du kan aktivere og prøve den fulde funktionalitet af standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasselejer ved at indstille feltet **Oplevelse** på siden **Virksomhedsoplysninger** til *Premium*. Find siden **Virksomhedsoplysninger** i :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Indstillinger-ikon."::: menu.  

Når du har aktiveret *Premium*-brugeroplevelsen, får du adgang til alle standardprofilerne (rollerne) og rollecentre i standardversionen. Alternativt kan du kontakte en videresalgspartner for at demonstrere mulighederne. Du kan finde flere oplysninger i [Hvordan finder jeg en videresalgspartner?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data" />Komplette eksempeldata

I de situationer, hvor du har brug for yderligere eksempeldata, skal du kontakte din forhandlerpartner.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer" />Designer

I et sandkassemiljø er **Designer** aktiveret. Du kan aktivere designer ved at vælge designikon ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) På en side eller ved at vælge menupunktet **Design** i ![Indstillinger](media/ui-experience/settings_icon_small.png) i menuen Indstillinger.  

Du kan finde flere oplysninger i [Brug designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i Developer and admin Content (kun på engelsk).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-related-microsoft-trainingtrainingmodulesadmin-online-dynamics--business-central" />Se relateret [Microsoft-træning](/training/modules/admin-online-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversioner og abonnementer](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions)  
[Sådan styrer du Miljøer i Business Central Administration](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Produktions-og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
