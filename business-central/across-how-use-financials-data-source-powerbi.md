---
title: Oprette rapporter i Power BI Desktop for at vise Business Central-data | Microsoft Docs
description: Gøre dine data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: c3ec3a511164d85dd01f827227e2cbcff76ce395
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697718"
---
# <a name="building-power-bi-reports-to-display-prodlong-data"></a>Oprette Power BI-rapporter, der viser [!INCLUDE [prodlong](includes/prodlong.md)]-data

Du kan gøre dine [!INCLUDE[prodlong](includes/prodlong.md)]-data tilgængelige som datakilde i Power BI Desktop og opbygge nyttige rapporter over status for din virksomhed.

Denne artikel beskriver, hvordan du kan komme i gang med at bruge Power BI Desktop til at oprette rapporter, der viser [!INCLUDE[prodlong](includes/prodlong.md)]-data.  Når du har oprettet rapporter, kan du udgive dem til din egen Power BI-tjeneste eller dele dem med andre brugere i din organisation. Når disse rapporter er i Power BI-tjenesten, kan de brugere, der er oprettet til den, se rapporterne i [!INCLUDE[prodlong](includes/prodlong.md)].

## <a name="get-ready"></a>Gør dig klar

- Tilmeld dig Power BI-tjenesten.

    Hvis du ikke allerede har tilmeldt dig, skal du gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du tilmelder dig, skal du bruge din mailadresse og adgangskode.

- Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop er et gratis program, du installerer på din lokale computer. Du kan finde flere oplysninger under [Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Sørg for, at de data, du vil bruge i rapporten, udgivet som en webtjeneste.
    
    Der udgives mange webtjenester som standard. En nem måde at finde webtjenesterne på er at søge efter *webtjenester* i [!INCLUDE[prodshort](includes/prodshort.md)]. Sørg for, at feltet **Udgiv** er markeret på siden **Webtjenester**. Denne opgave er typisk en administrativ opgave.
    
    Du kan finde flere oplysninger om udgivelse af webtjenester under [Udgive en webtjeneste](across-how-publish-web-service.md).

- For [!INCLUDE[prodshort](includes/prodshort.md)] i det lokale miljø skal du have følgende oplysninger:

    - URL-adressen til OData for [!INCLUDE[prodshort](includes/prodshort.md)]. Denne URL-adresse har typisk formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, f.eks. `https://localhost:7048/BC160/ODataV4`. Hvis du har en installation med flere lejere, skal du medtage lejeren i URL-adressen, f.eks. `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Et brugernavn og en adgangskode til webtjenesten for en [!INCLUDE[prodshort](includes/prodshort.md)]-konto.

      For at få data fra [!INCLUDE[prodshort](includes/prodshort.md)] bruger Power BI basisgodkendelse. Derfor skal du bruge et brugernavn og en adgangsnøgle til webtjenesten for at oprette forbindelse. Kontoen kan være din egen brugerkonto, eller din organisation kan have en specifik konto til dette formål.

- Download [!INCLUDE [prodshort](includes/prodshort.md)]-rapporttemaet (valgfrit).

    Du kan finde flere oplysninger under [Bruge [!INCLUDE [prodshort](includes/prodshort.md)]-rapporttemaet](#theme) i denne artikel.

## <a name="add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Tilføje [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop

Den første opgave i oprettelsen af rapporter er at tilføje [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop. Når forbindelsen er oprettet, kan du starte med at generere rapporten.

1. Start Power BI Desktop.
2. Vælg **Hent data**.

    Hvis du ikke kan se **Hent data**, skal du vælge menuen **Filer** og derefter **Hent data**.
2. Vælg **Onlinetjenester** på siden **Hent data**.
3. Benyt en af følgende fremgangsmåder i ruden **Onlinetjenester**:

    1. Hvis du opretter forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] online, skal du vælge **Dynamics 365 Business Central** og derefter **Opret forbindelse**.
    2. Hvis du opretter forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)] i det lokale miljø, skal du vælge **Dynamics 365 Business Central (on-premises)** og derefter **Opret forbindelse**.

4. Power BI viser en guide, der hjælper dig gennem forbindelsesprocessen, deriblandt at logge ind på [!INCLUDE [prodshort](includes/prodshort.md)].

    Vælg **Log på** for online, og vælg derefter den relevante konto. Brug den samme konto, som du bruger til at logge på [!INCLUDE [prodshort](includes/prodshort.md)].
    
    Hvis det er det lokale miljø, skal du angive URL-adressen til OData [!INCLUDE[prodshort](includes/prodshort.md)] og evt. navnet på virksomheden. Angiv derefter brugernavnet og adgangskoden på den konto, der skal bruges til at oprette forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)], når du bliver bedt om det. Angiv webtjenestens adgangsnøgle i feltet **Adgangskode**.

    > [!NOTE]  
    > Når du har oprettet forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)], bliver du ikke bedt om at logge på igen.
    
5. Vælg **Opret forbindelse** for at fortsætte.

    Guiden Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøer, -regnskaber og -datakilder. Disse datakilder repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE [prodshort](includes/prodshort.md)].
6. Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.
7. Gentag fremgangsmåden for at tilføje flere [!INCLUDE [prodshort](includes/prodshort.md)] eller andre data til din Power BI-datamodel.

Når dataene er indlæst, kan du se dem i den højre navigation på siden. Nu har du oprettet forbindelse til dine [!INCLUDE[prodshort](includes/prodshort.md)]-data og er klar til at begynde at oprette din Power BI-rapport.  

> [!TIP]
> Du kan finde flere oplysninger om brugen af Power BI Desktop under [Introduktion til Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Oprette rapporter for at vise data, der er knyttet til en liste

Du kan oprette rapporter, der vises i en faktaboks på en [!INCLUDE [prodshort](includes/prodshort.md)]-listeside. Rapporterne kan indeholde data om den post, der er valgt på listen. Oprettelse af disse rapporter minder om andre rapporter, men der er nogle ting, du skal gøre for at sikre, at rapporterne vises som forventet. Du kan finde flere oplysninger under [Oprette Power BI-rapporter til visning af listedata i [!INCLUDE[prodshort](includes/prodshort.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prodshort-report-theme-optional"></a><a name="theme"></a>Brug af [!INCLUDE [prodshort](includes/prodshort.md)]-rapporttemaet (valgfrit)

Før du opretter rapporten, anbefales det, at du downloader og importerer [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen. Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som [!INCLUDE [prodshort](includes/prodshort.md)]-apps, uden at du skal definere brugerdefinerede farver til hvert visuelle element.

> [!NOTE]
> Denne opgave er valgfri. Du kan altid oprette dine rapporter og derefter downloade og anvende typografiskabelonen senere.

### <a name="download-the-theme"></a>Downloade temaet

Temafilen er tilgængelig som en json-fil i Microsoft Power BI Community-temagalleriet. Benyt følgende fremgangsmåde for at downloade temafilen:

1. Gå til [Microsoft Power BI Community-temagalleriet til Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Vælg den vedhæftede fil **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Indlæse temaet i en rapport

Når du har downloadet [!INCLUDE [prodshort](includes/prodshort.md)]-rapporttemaet, kan du indlæse det i rapporterne. Hvis du vil indlæse temaet, skal du vælge **Vis** > **Temaer** > **Søg efter temaer**. Du kan finde flere oplysninger under [Power BI Desktop - Indlæse brugerdefinerede rapporttemaer](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Udgive rapporter

Når du har oprettet eller redigeret en rapport, kan du udgive rapporten til Power BI-tjenesten og dele den med andre i din organisation. Når den er udgivet, kan du se rapporten i Power BI. Rapporterne kan derefter også vælges i [!INCLUDE[prodshort](includes/prodshort.md)].

Hvis du vil udgive en rapport, skal du vælge **Udgiv** på fanen **Startside** på båndet eller i menuen **Filer**. Hvis du er logget på Power BI-tjenesten, udgives rapporten til denne tjeneste. Ellers bliver du bedt om at logge på. 

## <a name="distribute-or-share-a-report"></a>Distribuere eller dele en rapport

Du kan få rapporter ud til dine kolleger og andre på flere måder:

- Distribuer rapporter som .pbix-filer.

    Rapporter gemmes på din computer som .pbix-filer. Du kan distribuere rapportfilen .pbix til brugere ligesom andre filer. Derefter kan brugerne overføre filen til deres Power BI-tjeneste. Se [Overføre rapporter fra filer](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Hvis du distribuerer rapporter på denne måde, betyder det, at opdatering af data til rapporter udføres individuelt af hver bruger. Denne situation kan have indflydelse på ydeevnen af [!INCLUDE[prodshort](includes/prodshort.md)].

- Dele rapporter fra Power BI-tjenesten

    Hvis du har en Power BI Pro-licens, kan du dele rapporten med andre direkte fra Power BI-servicen. Du kan finde flere oplysninger under [Power BI - Dele et dashboard eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere virksomhedens data til Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Introduktion](product-get-started.md)  
[Importere virksomhedsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
