---
title: Administrere kunder ved hjælp af Dynamics 365 for Sales| Microsoft Docs
description: Du kan bruge Dynamics 365 for Sales fra Business Central til at tilknytte data og få gnidningsløs integration og synkronisering i lead-til-kontant-processen.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3cc053158581d4fc9b87dc3e505a23ed809c1c8f
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620857"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Brug af Dynamics 365 for Sales fra Business Central
Hvis du bruger Dynamics 365 for Sales til Customer Engagement, kan du nyde godt af problemfri lead-til-kontant-processen ved hjælp af [!INCLUDE[d365fin](includes/d365fin_md.md)] for back end-aktiviteter som f.eks. behandling af ordrer, administration af lageret og håndtering af økonomien.

> [!NOTE]
> I dette emnet antages det, at du bruger onlineversioner af [!INCLUDE[d365fin](includes/d365fin_md.md)] og Salg. Du kan blande onlineversioner og lokale versioner, men det kræver speciel konfiguration. Du kan finde flere oplysninger i [Forberedelse af integration med Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Ved integration af programmerne kan du få adgang til data i Salg fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt i nogle tilfælde. Du kan arbejde med og synkronisere datatyper, der er fælles for begge tjenester, f.eks. debitorer, kontakter og salgsoplysninger, og holde dataene opdaterede i begge programmer.  

For eksempel kan en sælger i Salg bruge prislisterne fra [!INCLUDE[d365fin](includes/d365fin_md.md)], når vedkommende opretter en salgsordre. Når sælgeren føjer varen til salgsordrelinjen i Salg, kan vedkommende også få vist lagerniveauet (tilgængelighed) af varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

Omvendt kan ordrebehandlere i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndtere salgsordrer, der automatisk eller manuelt overføres fra salg. De kan f.eks. oprette og bogføre salgsordrelinjer for varer eller ressourcer, der er angivet i Salg, som rekvirerede produkter. Du kan finde flere oplysninger i [Håndtering af salgsordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] kan kun integreres med Dynamics 365 for Sales. Andre programmer i Dynamics 365, der ændrer standardarbejdsprocessen eller datamodellen i Salg, for eksempel Project Service Automation, kan bryde integrationen mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Salg.

### <a name="coupling-records"></a>Sammenkæde poster
Du kan vælge de data, der skal synkroniseres, ved hjælp af den assisterede opsætningsvejledning. Senere kan du også indstille synkroniseringen for bestemte poster. Dette betegnes *sammenkædning*. Du kan f.eks. sammenkæde en bestemt konto i Salg med en bestemt debitor i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I dette afsnit beskrives det, hvad du skal tage højde for, når du sammenkæder poster.

Hvis du f.eks. vil have vist konti i Salg som debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du sammenkæde de to typer poster. For at gøre det skal du bruge handlingen **Konfigurer sammenkædning** på oversigtssiden **Kunder (Debitorer)** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Derefter skal du angive, hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder der svarer til hvilke konti i Salg.

Du kan også oprette (og sammenkæde) en konto i Salg baseret på f.eks. en debitorpost i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af **Opret konti i Dynamics 365 for Sales**, eller omvendt, ved hjælp af **Opret kreditor i [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Når du opretter sammenkædning mellem to poster, kan du også manuelt anmode om, at en aktuel post, f.eks. en kunde, skal overskrives med det samme af kontodata fra Salg (eller fra [!INCLUDE[d365fin](includes/d365fin_md.md)]) ved hjælp af handlingen **Synkroniser nu**. Handlingen **Synkroniser nu**, som vil spørge dig, om Salg eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-postdata skal overskrives.

I nogle tilfælde skal du sammenkæde bestemte datasæt før andre datasæt som vist i følgende tabel.

|Data|Hvad skal sammenkædes først|
|-----|----|
|Debitorer og konti|Sammenkæd sælgere med brugere af Salg|
|Varer og ressourcer|Sammenkæd måleenhed med Salg-enhedsgrupper|
|Priser på varer og ressourcer|Sammenkæd debitorprisgrupper med Salg-priser|

> [!NOTE]  
> Hvis du bruger priser i udenlandsk valuta, eller dine kunder gør det, skal du sørge for at sammenkæde valutaer med Salg-transaktionsvalutaer.

I Salg afhænger salgsordrer af ekstra oplysninger som f.eks. kunder, enheder, valutaer, debitorprisgrupper og varer og/eller ressourcer. For at integration med salgsordrer skal fungere, skal du sammenkæde kunder, måleenheder, valutaer, debitorprisgrupper og varer og/eller ressourcer.

### <a name="fully-synchronizing-records"></a>Fuld synkronisering af poster
I slutningen af den assisterede opsætningsvejledning kan du vælge handlingen **Kør fuld synkronisering** for at starte synkronisering af alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterede poster i Salg. På siden **Dynamics 365 for Sales Fuld synkroniseringsgennemgang** skal du vælge handlingen **Start**. Det kan tage et stykke tid at fuldføre fuld synkronisering, men du kan fortsætte med at arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)], mens den kører i baggrunden.

Når du vil kontrollere status for individuelle sager i en fuld synkronisering, skal du på siden **Dynamics 365 for Sales Fuld synkroniseringsgennemgang** vælge en post for at få vist detaljer. Opdater siden for at opdatere status under synkroniseringen.

Fra siden **Konfiguration af Microsoft Dynamics 365-forbindelse** kan du få oplysninger om fuld synkronisering, når som helst. Her kan du også åbne siden **Integrationstabelkoblinger** for at få vist detaljer om tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)] og Salg, som skal synkroniseres.

## <a name="handling-sales-order-data"></a>Håndtering af salgsordredata
Salgsordrer, som personer indsender i [!INCLUDE[crm_md](includes/crm_md.md)], overføres til [!INCLUDE[d365fin](includes/d365fin_md.md)], hvis du markerer afkrydsningsfeltet **Opret salgsordrer automatisk** på siden **Konfiguration af Microsoft Dynamics 365-forbindelse**.
Alternativt kan du manuelt konvertere sendte salgsordrer fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjælp af handlingen **Opret i [!INCLUDE[d365fin](includes/d365fin_md.md)]**, der er tilgængelig på siden **Salgsordrer – Dynamics 365 for Sales**.
På sådanne salgsordrer overføres og knyttes feltet **Navn** på den oprindelige ordre til feltet **Eksternt bilagsnummer** i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dette kan også fungere, hvis den oprindelige salgsordre indeholder rekvirerede produkter, hvilket betyder varer eller ressourcer, der ikke er registreret i nogen af programmerne. I så fald skal du udfylde felterne **Rekvireret produkttype** og **Rekvireret produktnr.** på siden **Opsætning af salg og tilgodehavender**, så sådanne ikke-registrerede produktsalg knyttes til et bestemt vare/ressourcenummer for finansielle analyser.

Hvis beskrivelsen af varen på den oprindelige salgsordre er meget lang, oprettes der en ekstra salgsordrelinje af typen **Bemærkning** for at holde hele teksten i salgsordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Opdateringer til felter i salgsordresidehovedet, som f.eks. Sidste afsendelsesdato eller Ønsket leveringsdato, der er tilknyttet i SALGSORDRE-ORDRE **Integrationstabelkoblinger** synkroniseres regelmæssigt til [!INCLUDE[crm_md](includes/crm_md.md)]. Processer som frigivelse af en salgsordre og levering eller fakturering af en salgsordre bogføres på salgsordrens tidslinje i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Introduktion til aktivitetsopdateringer](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

## <a name="handling-sales-quotes-data"></a>Håndtering af data i salgstilbud
Salgstilbud, der aktiveres i [!INCLUDE[crm_md](includes/crm_md.md)], overføres til [!INCLUDE[d365fin](includes/d365fin_md.md)], hvis du markerer afkrydsningsfeltet **Behandl tilbud automatisk** på siden **Konfiguration af Microsoft Dynamics 365-forbindelse**.
Alternativt kan du manuelt konvertere aktiverede salgstilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjælp af handlingen **Behandl i [!INCLUDE[d365fin](includes/d365fin_md.md)]** på siden **Salgstilbud – Dynamics 365 for Sales**.
I sådanne salgstilbud overføres og knyttes feltet **Navn** i det oprindelige tilbud til feltet **Eksternt bilagsnummer** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Desuden overføres feltet **Gælder til** i tilbud og tilknyttes feltet **Tilbud gyldigt til** i salgstilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Salgstilbud gennemgår mange revisioner, mens de er under udarbejdelse. Både manuel og automatisk behandling af salgstilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)] sikrer, at tidligere versioner af salgstilbud arkiveres, før nye ændringer af salgstilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] behandles. 

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Håndtere bogførte salgsfakturaer, debitorbetalinger og statistik
Når en salgsordre er opfyldt, oprettes der fakturaer for den. Når du fakturerer en salgsordre, kan du overføre bogført salgsfaktura til [!INCLUDE[crm_md](includes/crm_md.md)], hvis du vælger **Opret faktura i [!INCLUDE[crm_md](includes/crm_md.md)]** på siden Bogført salgsfaktura. Bogførte fakturaer overføres til [!INCLUDE[crm_md](includes/crm_md.md)] med statussen **Faktureret**. Når der modtages debitorbetaling for salgsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)], ændres status for salgsfaktura til **Betalt** med Statusårsag **Delvis**, hvis det er en delvis betaling eller **Afsluttet**, hvis den er endeligt betalt, når du kører **Opdater kontostatistik** på debitorsiden i [!INCLUDE[d365fin](includes/d365fin_md.md)]. **Opdater kontostatistik** opdaterer også værdier typen Saldo og Salg i alt i [!INCLUDE[d365fin](includes/d365fin_md.md)] faktaboksen Kontostatistik i [!INCLUDE[crm_md](includes/crm_md.md)].
Du kan også få planlagt opgaver (Debitorstatistik og POSTEDSALESINV-INV) til automatisk at køre begge processer i baggrunden. 

## <a name="see-also"></a>Se også
[Forberede integration med Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Relationsstyring](marketing-relationship-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ændre, hvilke funktioner der vises](ui-experiences.md)  
[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)    
[Onboarding af din organisation og dine brugerne til Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
