---
title: Oprette et kreditorkort for at registrere en ny leverandør (indeholder video)
description: 'Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør og gemme kreditorkort som en skabelon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: '26, 27, 34, 461, 786, 1379, 1385, 1386, 1628'
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="register-new-vendors" />Registrere nye kreditorer

Kreditorer leverer de produkter, du sælger. Hver kreditor, som du køber fra, skal registreres med et kreditorkort.

Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort. Når alle de obligatoriske stamoplysninger er oprettet, kan du tilføje entydige karakteristika for en kreditor, f.eks. prioritere kreditoren i forbindelse med betaling eller få vist de varer, som kreditoren og andre kreditorer kan levere. En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder. Flere oplysninger i [Opsætning af indkøb](purchasing-setup-purchasing.md).

Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra hver kreditor. Flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).
<br /><br />  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors" />Tilføjelse af nye kreditorer

Du kan tilføje nye kreditorer manuelt ved at udfylde siden **Kreditorkort**, eller du kan bruge skabeloner, der indeholder foruddefinerede oplysninger. Du kan f. eks. oprette skabeloner til forskellige typer kreditorprofiler. Du kan spare tid ved at bruge skabeloner, når du tilføjer nye kreditorer, så oplysningerne bliver korrekte hver gang.

> [!NOTE]  
> Hvis der er kreditorskabeloner til forskellige kreditortyper, når du opretter et nyt kreditorkort, vises en side, hvor du kan vælge en passende skabelon. Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.

Når du har oprettet en skabelon, kan du bruge handlingen **Anvend skabelon** for at anvende den på en eller flere valgte kreditorer. Hvis du vil oprette en skabelon, skal du angive de oplysninger, du vil genbruge, på siden **Kreditorkort** og derefter gemme den som en skabelon. Flere oplysninger i afsnittet [Sådan gemmes kreditorkortsiden som en skabelon](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Det kan være nyttigt at tilpasse siden **Kreditorskabeloner**, når du opretter en skabelon. Du kan f. eks. tilføje et felt, der ikke allerede vises på siden. Flere oplysninger i [Tilpasse dit arbejdsområde](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan også oprette en kreditor ud fra en kontakt. Flere oplysninger i [Oprette en debitor, kreditor, medarbejder eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

Remitter til-adresser bruges, når du udskriver checks til at betale kreditorer, og leverandører kan have flere Remitter til-betalinger. F.eks. kan en kreditor levere en vare fra et datterselskab, men ønsker at modtage betaling hos virksomheden. [!INCLUDE [prod_short](includes/prod_short.md)] bruges til at oprette flere postadresser for hver kreditor, og du kan vælge den korrekte lokation, hvor der skal sendes betalinger til fakturaberegning.

Du angiver Remitter til-adresser på kreditorkort sider og i oversigtspanelet forsendelse & betalinger på købsordrer og fakturaer. Når du opretter Udbetalingskladde linjer ved hjælp af rapporten løn-kreditor eller Opret betaling på listesiden kreditor eller på siden med kreditorkortet eller handlingen Udlign på en betalingskladde, tildeles Remitter til-koden på kreditorposten. Du kan overskrive denne værdi.

### <a name="to-create-a-new-vendor" />Sådan oprettes en ny kreditor

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Nr.** i oversigtspanelet **Generelt**. Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)

Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.

Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon. Flere oplysninger i afsnittet [Sådan gemmes kreditorkortsiden som en skabelon](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information" />Slette og redigere kreditoroplysninger

Du kan til enhver tid oplysninger om kreditorkort. Hvis du har bogført en postering for en kreditor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision. Hvis du vil slette kreditorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.

> [!TIP]
> Du kan ændre IBAN (International Bank Account Number) på en kreditors bankkonto, uden at ændringerne påvirker de historiske kreditoverførselsposter. Overførsel af remburs Journal lagrer *Modtager IBAN* og *Modtagers bankkontonr.*, der blev angivet i felterne **Kreditorbankkonto** og **Modtagernavn** fra siden **Kreditorkort**, da posterne blev oprettet.

> [!TIP]
> Du kan tilføje alternative adresser på kreditorkortet ved at vælge handlingen **Bestillingsadresser**.

## <a name="to-save-the-vendor-card-as-a-template" />Sådan gemmes kreditorkortet som en skabelon

1. På siden **Kreditorkort** skal du vælge handlingen **Gem som skabelon**. Siden **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**. Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.
4. Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.
5. Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.  
   Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.

## <a name="see-related-microsoft-training" />Se relateret [Microsoft-træning](/training/modules/trade-master-data-dynamics-365-business-central/).

## <a name="see-also" />Se også

[Flette dublerede poster](sales-how-merge-duplicate-records.md)  
[Oprette nummerserie](ui-create-number-series.md)  
[Konfigurere kreditorbankkonto](purchasing-how-set-up-vendors-bank-accounts.md)  
[Oprette indkøbere](purchasing-how-setup-purchasers.md)  
[Køb](purchasing-manage-purchasing.md)  
[Registrere køb](purchasing-how-record-purchases.md)  
[Bruge online kort til at finde steder og vejledninger](across-online-maps.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
