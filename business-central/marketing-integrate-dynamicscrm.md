---
title: Administrere kunder ved hjælp af Dynamics 365 Sales (indeholder video) | Microsoft Docs
description: Du kan bruge Dynamics 365 Sales fra Business Central til at tilknytte data og få gnidningsløs integration og synkronisering i lead-til-kontant-processen.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 67d9915e4f60b20d0e871810dfc3d66450103a5a
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940447"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Bruge Dynamics 365 Sales fra Business Central
Hvis du bruger Dynamics 365 Sales for Customer Engagement, kan du nyde godt af problemfri lead-til-kontant-processen ved hjælp af [!INCLUDE[prod_short](includes/prod_short.md)] for back end-aktiviteter som f.eks. behandling af ordrer, administration af lageret og håndtering af økonomien.

Før du kan bruge integrationsfunktionerne, skal din systemadministrator oprette forbindelsen og definere brugere i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Følgende fremgangsmåde beskriver processen med at integrere onlineversioner af [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde oplysninger om konfiguration af det lokale miljø under [Forberede Dynamics 365 Sales til integration i det lokale miljø](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Ved integration af programmerne kan du få adgang til data i Salg fra [!INCLUDE[prod_short](includes/prod_short.md)] og omvendt i nogle tilfælde. Du kan arbejde med og synkronisere datatyper, der er fælles for begge tjenester, f.eks. debitorer, kontakter og salgsoplysninger, og holde dataene opdaterede i begge programmer.  

For eksempel kan en sælger i [!INCLUDE[crm_md](includes/crm_md.md)] bruge prislisterne fra [!INCLUDE[prod_short](includes/prod_short.md)], når vedkommende opretter en salgsordre. Når sælgeren føjer varen til salgsordrelinjen i [!INCLUDE[crm_md](includes/crm_md.md)], kan vedkommende se varens lagerniveau (tilgængelighed) fra [!INCLUDE[prod_short](includes/prod_short.md)].

Omvendt kan ordrebehandlere i [!INCLUDE[prod_short](includes/prod_short.md)] håndtere salgsordrer, der automatisk eller manuelt overføres fra [!INCLUDE[crm_md](includes/crm_md.md)]. De kan f.eks. oprette og bogføre salgsordrelinjer for varer eller ressourcer, der er angivet i [!INCLUDE[crm_md](includes/crm_md.md)], som rekvirerede produkter. Du kan finde flere oplysninger i [Håndtering af salgsordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] kan kun integreres med [!INCLUDE[crm_md](includes/crm_md.md)]. Andre programmer i Dynamics 365, der ændrer standardarbejdsprocessen eller datamodellen i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel Project Service Automation, kan bryde integrationen mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records"></a>Sammenkæde poster
Du kan vælge de data, der skal synkroniseres, ved hjælp af den assisterede opsætningsvejledning. Senere kan du også indstille synkroniseringen for bestemte poster. Dette betegnes *sammenkædning*. Du kan f.eks. sammenkæde en bestemt konto i [!INCLUDE[crm_md](includes/crm_md.md)] med en bestemt debitor i [!INCLUDE[prod_short](includes/prod_short.md)]. I dette afsnit beskrives det, hvad du skal tage højde for, når du sammenkæder poster.

Hvis du f.eks. vil se [!INCLUDE[crm_md](includes/crm_md.md)]-konti som debitorer i [!INCLUDE[prod_short](includes/prod_short.md)], skal du sammenkæde de to typer poster. For at gøre det skal du bruge handlingen **Konfigurer sammenkædning** på oversigtssiden **Kunder (Debitorer)** i [!INCLUDE[prod_short](includes/prod_short.md)]. Derefter skal du angive, hvilke [!INCLUDE[prod_short](includes/prod_short.md)]-kunder der svarer til hvilke konti i [!INCLUDE[crm_md](includes/crm_md.md)].

Du kan også oprette (og sammenkæde) en konto i [!INCLUDE[crm_md](includes/crm_md.md)] baseret på f.eks. en debitorpost i [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af **Opret konto i Dynamics 365 Sales** eller omvendt ved hjælp af **Opret kreditor i [!INCLUDE[prod_short](includes/prod_short.md)]**.

Når du opretter sammenkædning mellem to poster, kan du også manuelt anmode om, at en aktuel post, f.eks. en kunde, skal overskrives med det samme af kontodata fra Salg (eller fra [!INCLUDE[prod_short](includes/prod_short.md)]) ved hjælp af handlingen **Synkroniser nu**. Handlingen **Synkroniser nu**, som vil spørge dig, om Salg eller [!INCLUDE[prod_short](includes/prod_short.md)]-postdata skal overskrives.

I nogle tilfælde skal du sammenkæde bestemte datasæt før andre datasæt som vist i følgende tabel.

|Data|Hvad skal sammenkædes først|
|-----|----|
|Debitorer og konti|Sammenkæd sælgere med brugere af [!INCLUDE[crm_md](includes/crm_md.md)]|
|Varer og ressourcer|Sammenkæd enheder med [!INCLUDE[crm_md](includes/crm_md.md)]-enhedsgrupper|
|Priser på varer og ressourcer|Sammenkæd debitorprisgrupper med [!INCLUDE[crm_md](includes/crm_md.md)] -priser|

> [!NOTE]  
> Hvis du bruger priser i udenlandsk valuta, eller dine kunder gør det, skal du sørge for at sammenkæde valutaer med Salg-transaktionsvalutaer.

I [!INCLUDE[crm_md](includes/crm_md.md)] afhænger salgsordrer af ekstra oplysninger som f.eks. kunder, enheder, valutaer, debitorprisgrupper og varer og/eller ressourcer. For at integration med salgsordrer skal fungere, skal du sammenkæde kunder, måleenheder, valutaer, debitorprisgrupper og varer og/eller ressourcer.

## <a name="fully-synchronizing-records"></a>Fuld synkronisering af poster
I slutningen af den assisterede opsætningsvejledning kan du vælge handlingen **Kør fuld synkronisering** for at starte synkronisering af alle [!INCLUDE[prod_short](includes/prod_short.md)]-poster med alle relaterede poster i [!INCLUDE[crm_md](includes/crm_md.md)]. På siden **Fuld synkroniseringsgennemsyn af Dynamics 365 Sales** skal du vælge handlingen **Start**. Det kan tage et stykke tid at fuldføre fuld synkronisering, men du kan fortsætte med at arbejde i [!INCLUDE[prod_short](includes/prod_short.md)], mens den kører i baggrunden.

Når du vil kontrollere status for individuelle sager i en fuld synkronisering, skal du på siden **Fuld synkroniseringsgennemgang af Dynamics 365 Sales** vælge en post for at få vist detaljer. Opdater siden for at opdatere status under synkroniseringen.

Fra siden **Konfiguration af Microsoft Dynamics 365-forbindelse** kan du få oplysninger om fuld synkronisering, når som helst. Her kan du også åbne siden **Integrationstabelkoblinger** for at få vist detaljer om tabellerne i [!INCLUDE[prod_short](includes/prod_short.md)] og Salg, som skal synkroniseres.

## <a name="handling-sales-order-data"></a>Håndtering af salgsordredata
Salgsordrer, som folk indsender i [!INCLUDE[crm_md](includes/crm_md.md)], overføres automatisk til [!INCLUDE[prod_short](includes/prod_short.md)], hvis du markerer afkrydsningsfeltet **Opret salgsordrer automatisk** på siden **Konfiguration af Microsoft Dynamics 365-forbindelse**.
Alternativt kan du manuelt konvertere sendte salgsordrer fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjælp af handlingen **Opret i [!INCLUDE[prod_short](includes/prod_short.md)]**, der er tilgængelig på siden **Salgsordrer – Dynamics 365 for Sales**.
På sådanne salgsordrer overføres og knyttes feltet **Navn** på den oprindelige ordre til feltet **Eksternt bilagsnummer** i [!INCLUDE[prod_short](includes/prod_short.md)].

Dette kan også fungere, hvis den oprindelige salgsordre indeholder rekvirerede produkter, hvilket betyder varer eller ressourcer, der ikke er registreret i nogen af programmerne. I så fald skal du udfylde felterne **Rekvireret produkttype** og **Rekvireret produktnr.** felter på siden **Opsætning af salg og tilgodehavender**, så salg af sådanne ikke-registrerede produkter knyttes til et bestemt vare eller ressourcenummer.

> [!NOTE]
> Du kan ikke knytte en nedskrivning til en vare eller ressource i [!INCLUDE[prod_short](includes/prod_short.md)], der er kombineret med et produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil tillade skrive programmer, anbefales det, at du opretter en vare eller en ressource, der er specielt beregnet til dette formål, og du kan ikke koble det til et produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. 

Hvis beskrivelsen af varen på den oprindelige salgsordre er meget lang, oprettes der en ekstra salgsordrelinje af typen **Bemærkning** for at holde hele teksten i salgsordren i [!INCLUDE[prod_short](includes/prod_short.md)].

Opdateringer til felter i salgsordresidehovedet, som f.eks. Sidste afsendelsesdato eller Ønsket leveringsdato, der er tilknyttet i **SALGSORDRE-ORDRE**-integrationstabelkoblinger synkroniseres regelmæssigt til [!INCLUDE[crm_md](includes/crm_md.md)]. Processer som frigivelse af en salgsordre og levering eller fakturering af en salgsordre bogføres på salgsordrens tidslinje i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Introduktion til aktivitetsopdateringer](/dynamics365/sales-enterprise/manage-activities). <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Periodisk synkronisering, der er baseret på **SALESORDER-ORDE**-integrationstabeltilknytning, fungerer kun, når salgsordreintegration er aktiveret. Du kan få oplysninger i [Forbindelsesindstillinger på siden Opsætning af salgsforbindelse](admin-prepare-dynamics-365-for-sales-for-integration.md). Kun salgsordrer, der er oprettet fra sendte salgsordrer i [!INCLUDE[crm_md](includes/crm_md.md)], synkroniseres. Du kan finde flere oplysninger i [Aktivere integration af salgsordrebehandling](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Håndtering af data i salgstilbud
Salgstilbud, der aktiveres i [!INCLUDE[crm_md](includes/crm_md.md)], overføres til [!INCLUDE[prod_short](includes/prod_short.md)], hvis du markerer afkrydsningsfeltet **Behandl tilbud automatisk** på siden **Konfiguration af Microsoft Dynamics 365-forbindelse**.
Alternativt kan du manuelt konvertere aktiverede salgstilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjælp af handlingen **Behandl i [!INCLUDE[prod_short](includes/prod_short.md)]** på siden **Salgstilbud – Dynamics 365 Sales**.
I sådanne salgstilbud overføres og knyttes feltet **Navn** i det oprindelige tilbud til feltet **Eksternt bilagsnummer** i [!INCLUDE[prod_short](includes/prod_short.md)]. Desuden overføres feltet **Gælder til** i tilbud og tilknyttes feltet **Tilbud gyldigt til** i salgstilbud i [!INCLUDE[prod_short](includes/prod_short.md)].  

Salgstilbud gennemgår mange revisioner, mens de er under udarbejdelse. Både manuel og automatisk behandling af salgstilbud i [!INCLUDE[prod_short](includes/prod_short.md)] sikrer, at tidligere versioner af salgstilbud arkiveres, før nye ændringer af salgstilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] behandles.

Når du vælger **Behandl** i [!INCLUDE[prod_short](includes/prod_short.md)] for et tilbud, der er **vundet**, oprettes der kun en salgsordre i [!INCLUDE[prod_short](includes/prod_short.md)], hvis der sendes en tilsvarende salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)]. Ellers frigives tilbuddet kun i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis en tilsvarende salgsordre er blevet sendt i [!INCLUDE[crm_md](includes/crm_md.md)] senere, og der oprettes en salgsordre, opdateres **Tilbudsnr.** til salgsordren, og tilbuddet arkiveres.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Håndtere bogførte salgsfakturaer, debitorbetalinger og statistik
Når en salgsordre er opfyldt, oprettes der fakturaer for den. Når du fakturerer en salgsordre, kan du overføre den bogførte salgsfaktura til [!INCLUDE[crm_md](includes/crm_md.md)], hvis du markerer afkrydsningsfeltet **Opret faktura i [!INCLUDE[crm_md](includes/crm_md.md)]** på siden **Bogført salgsfaktura**. Bogførte fakturaer overføres til [!INCLUDE[crm_md](includes/crm_md.md)] med status **Faktureret**.

Når der modtages debitorbetaling for salgsfakturaen i [!INCLUDE[prod_short](includes/prod_short.md)], ændres status for salgsfaktura til **Betalt** med **Statusårsag**-feltet indstillet til **Delvis**, hvis det er en delvis betaling eller **Afsluttet**, hvis den er endeligt betalt, når du vælger handlingen **Opdater kontostatistik** på debitorsiden i [!INCLUDE[prod_short](includes/prod_short.md)]. Funktionen **Opdater kontostatistik** opdaterer også værdier, f.eks. **Saldo** og **Salg i alt** i **[!INCLUDE[prod_short](includes/prod_short.md)]-faktaboksen Kontostatistik** i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan også få de planlagte opgaver Debitorstatistik og POSTEDSALESINV-INV til automatisk at køre begge processer i baggrunden. 

## <a name="handling-sales-prices"></a>Håndtering af salgspriser
> [!NOTE]
> I 2020 udgivelsesbølge 2 har vi udgivet strømlinede processer til opsætning og administration af priser og rabatter. Hvis du er ny kunde, der bruger den version, bruger du den nye oplevelse. Hvis du allerede bruger den nye oplevelse, afhænger det af, om din administrator har aktiveret funktionsopdateringen **Ny vareprissætningsopdatering** i **Funktionsadministration**. Du kan finde flere oplysninger i [Aktivere Upcoming Features Ahead of Time](/dynamics365/business-central/dev-itpro/administration/feature-management).

Disse trin, der fuldfører denne proces, varierer afhængigt af, om din administrator har aktiverer ny prissætning. 

> [!NOTE]
> Hvis standardprissynkroniseringen ikke virker, anbefales det, at du bruger integrationstilpasningsmulighederne. Flere oplysninger i [Tilpasning af integration med Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### <a name="current-experience"></a>[Aktuel oplevelse](#tab/current-experience/)
I den aktuelle prissætning synkroniseres [!INCLUDE[prod_short](includes/prod_short.md)] salgspriser, som: 

* Anvendes på alle kunder. Standardsalgsprislister oprettes på basis af prisen i feltet **Enhedspris** på siden **Varekort** for varerne.
* Tildele til en speciel debitorprisgruppekode. Salgspriser for dine detail- eller engroskunder. Hvis du vil synkronisere priser baseret på en debitorprisgruppe, skal du gøre følgende:

    1. Par de varer, hvor priserne er angivet for debitorprisgruppen.
    2. På siden **Debitorprisgrupper** skal du oprette debitorprisgruppen ved at vælge **Relaterede**, derefter **Dynamics 365 Sales**, **Kobling** og derefter **Konfigurer kobling**. Koblingen opretter en aktiv prisliste i [!INCLUDE[prod_short](includes/prod_short.md)] med det samme navn som debitorprisgruppen i [!INCLUDE[crm_md](includes/crm_md.md)] og synkroniserer automatisk alle varer, som debitorprisgruppen definerer prisen for.

:::image type="content" source="media/customer-price-group.png" alt-text="Debitorprisgruppeside.":::

#### <a name="new-experience"></a>[Ny oplevelse](#tab/new-experience/)  

Den nye prissætningsoplevelse synkroniserer prislister, der opfylder følgende kriterier:

* **Tillad opdatering af standarder** er deaktiveret.
* Pristypen er Salg.
* Beløbstypen er Pris.
* Produkttypen på linjerne skal være vare eller ressource. 
* Der er ikke angivet et minimumsantal.

[!INCLUDE[prod_short](includes/prod_short.md)] synkroniserer salgspriser, der gælder for alle debitorer. Standardsalgsprislister oprettes på basis af prisen i feltet **Enhedspris** på siden **Varekort** for varerne.

Hvis du vil synkronisere prislister, skal du på siden **Salgsprisliste** vælge **Relaterede**, **Dynamics 365 Sales**, **Kobling** og derefter **Konfigurer kobling**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Salgsprislisteside.":::

---


## <a name="see-also"></a>Se også
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Relationsstyring](marketing-relationship-management.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)    
[Oversigt over Sales og Salgshub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]