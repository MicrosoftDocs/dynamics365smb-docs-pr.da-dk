---
title: Oprette et kreditorkort for at registrere en ny leverandør
description: I dette emne kan du læse, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør og gemme kreditorkort som en skabelon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 662239446426cf64ac20d766e21aee55b92f9809
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587680"
---
# <a name="register-new-vendors"></a>Registrere nye kreditorer

Kreditorer leverer de produkter, du sælger. Hver kreditor, som du køber fra, skal registreres som et kreditorkort.

Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort. Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere. En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder. Du kan finde flere oplysninger i [Opsætning af indkøb](purchasing-setup-purchasing.md).

Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren. Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Tilføjelse af nye kreditorer
Du kan tilføje nye kreditorer manuelt ved at udfylde felterne på siden **Kreditorkort**, eller du kan bruge skabeloner, der indeholder foruddefinerede oplysninger. Du kan f. eks. oprette skabeloner til forskellige typer kreditorprofiler. Du kan spare tid ved at bruge skabeloner, når du tilføjer nye kreditorer, så oplysningerne bliver korrekte hver gang. Hvis du opretter skabeloner til mere end én type kreditor, kan du vælge den skabelon, du vil bruge, når du tilføjer en kreditor. Hvis du kun opretter én skabelon, vil den blive brugt til alle nye kreditorer. Når du har oprettet en skabelon, kan du bruge handlingen **Anvend skabelon** for at anvende den på en eller flere valgte kreditorer. Hvis du vil oprette en skabelon, skal du angive de oplysninger, du vil genbruge, på siden Kreditorkort og derefter gemme den som en skabelon. Du kan finde flere oplysninger i afsnittet [Sådan gemmes kreditorkortet som en skabelon](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Det kan være nyttigt at tilpasse siden **Kreditorskabeloner**, når du opretter en skabelon. Du kan f. eks. tilføje et felt, der ikke allerede vises på siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan også oprette en kreditor ud fra en kontakt. Du kan finde flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Sådan oprettes en ny kreditor

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Kreditornr.**. Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)

Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.

Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon. Du kan finde flere oplysninger i afsnittet [Sådan gemmes kreditorkortet som en skabelon](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Slette og redigere kreditoroplysninger

Du kan til enhver tid oplysninger om kreditorkort. Hvis du har bogført en postering for en kreditor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette kreditorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.

> [!TIP]
> Du kan ændre IBAN på en kreditors bankkonto, uden at ændringerne påvirker de historiske kreditoverførselsposter. Overførsel af remburs Journal lagrer det IBAN-nummer, Recepient Bankkontonr., der blev angivet i felterne kreditorbankkonto og modtagernavn fra siden med kreditorkortet, da posterne blev oprettet.


## <a name="to-save-the-vendor-card-as-a-template"></a>Sådan gemmes kreditorkortet som en skabelon

1. På siden **Kreditorkort** skal du vælge handlingen **Gem som skabelon**. Siden **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.  
   Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.

## <a name="see-also"></a>Se også

[Flette dublerede poster](sales-how-merge-duplicate-records.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Køb](purchasing-manage-purchasing.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]