---
title: Synkronisering af Business Central og Dataverse | Microsoft Docs
description: Få mere at vide om synkronisering af data mellem Business Central og Dataverse.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 94f969f4d96f31b3b6843614e1bd99790a22307d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755188"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Planlægning af synkronisering mellem Business Central og Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Du kan synkronisere [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[prod_short](includes/prod_short.md)]-records og [!INCLUDE[cds_long_md](includes/cds_long_md.md)] -records, der tidligere har været sammenkædet. Synkroniseringsopgaver kan også oprette og sammenkæde nye records i destinationssystemet for records, der ikke allerede er sammenkædet, afhængigt af synkroniseringsretning og -regler. 

Der er flere standardsynkroniseringsjobs tilgængelige. Jobbene køres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem tabeller. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

1. VALUTA - Common Data Service-synkroniseringsjob.
2. LEVERANDØR - Common Data Service-synkroniseringsjob.
3. KONTAKT - Common Data Service-synkroniseringsjob.
4. DEBITOR - Common Data Service-synkroniseringsjob.
5. SÆLGERE - Common Data Service-synkroniseringsjob.

Du kan se job på siden **Poster for jobkøer**. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Poster for standardsynkroniseringsjobkø

Følgende tabel viser standardsynkroniseringsjobbene for [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Post for jobkø | Description | Retning | Integrationstabeltilknytning | Standardhyppighed for synkronisering (min.) | Standardangivelse for dvale ved inaktivitet (min.) |
|--|--|--|--|--|--|--|
| KONTAKT - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-kontakter med [!INCLUDE[prod_short](includes/prod_short.md)]-kontakter. | I begge retninger | KONTAKT | 30 | 720 <br>(12 timer) |
| VALUTA - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-transaktionsvalutaer med [!INCLUDE[prod_short](includes/prod_short.md)]-valutaer. | Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | VALUTA | 30 | 720 <br> (12 timer) |
| DEBITOR - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konti med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer. | I begge retninger | KUNDE | 30 | 720<br> (12 timer) |
| LEVERANDØR - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konti med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer. | I begge retninger | KREDITOR | 30 | 720<br> (12 timer) |
| SÆLGERE - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[prod_short](includes/prod_short.md)]-sælgere med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-brugere. | Fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] | SÆLGERE | 30 | 1440<br> (24 timer) |

## <a name="synchronization-process"></a>Synkroniseringsproces

Hver synkronisering af en jobkø-post benytter en bestemt integrationstabeltilknytning, der angiver, hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-tabel og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel, der skal synkroniseres. Tabeltilknytningerne omfatter også nogle indstillinger, der bestemmer, hvilke records i [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellen, der skal synkroniseres.  

For at kunne synkronisere data skal [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabelposter være sammenkædet med [!INCLUDE[prod_short](includes/prod_short.md)]-records. F.eks. skal en [!INCLUDE[prod_short](includes/prod_short.md)]-debitor være sammenkædet med en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto. Du kan konfigurere sammenkædninger manuelt, før du kører synkroniseringsjobbene, eller lade synkroniseringsjobbene konfigurere sammenkædninger automatisk. Den følgende liste beskriver, hvordan data synkroniseres mellem [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], når du benytter posterne i synkroniseringsjobkøen. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

- Afkrydsningfeltet **Synkroniser kun sammenkoblede poster** kontrollerer, hvorvidt nye poster oprettes, når du synkroniserer. Afkrydsningsfeltet er som standard markeret, hvilket betyder, at kun poster, der er sammenkoblede, synkroniseres. I integrationstabeltilknytningen kan du ændre tabeltilknytningen mellem en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel og en [!INCLUDE[prod_short](includes/prod_short.md)]-tabel, så integrationssynkroniseringsjobbene opretter nye poster i destinationsdatabasen for hver række i kildedatabasen, der ikke er sammenkoblet. Du kan finde flere oplysninger i [Oprettelse af Nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).

    **Eksempel**: Hvis du rydder afkrydsningsfeltet **Synkroniser kun sammenkoblede poster** når du synkroniserer kunder i [!INCLUDE[prod_short](includes/prod_short.md)] med konti i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], oprettes der en ny konto til hver kunde i [!INCLUDE[prod_short](includes/prod_short.md)] og disse sammenkobles automatisk. Som følge af, at synkroniseringen går begge veje i dette tilfælde, vil der blive oprettet og sammenkoblet en ny kunde sammen for hver [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto, der ikke allerede er sammenkoblet.  

    > [!NOTE]  
    > Der er regler og filtre, der bestemmer, hvilke data der synkroniseres. Du kan finde flere oplysninger under [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md).

- Når der oprettes nye records i [!INCLUDE[prod_short](includes/prod_short.md)], benytter de enten skabelonen, der er defineret til integrationstabeltilknytning eller standardskabelonen, der er tilgængelig for rækketypen. Felter udfyldes automatisk med data fra [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[cds_long_md](includes/cds_long_md.md)] afhængigt af synkroniseringsretning. Du kan finde flere oplysninger i [Rediger tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Når der foretages flere synkroniseringer, er det kun records, der er blevet ændret eller tilføjet efter sidste gennemførte synkroniseringsjob for tabellen, der opdateres.  

     Nye records i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] tilføjes i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis data i felterne i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-records er ændret, kopieres disse data til det tilsvarende felt i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Ved synkronisering i begge retninger synkroniserer jobbet fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], og derefter fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Vedrørende timeoutperioder for inaktivitet
Nogle opgavekøposter, såsom dem, der planlægger synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)], anvender feltet **Timeout for inaktivitet** på kortet til Opgavekøside for at forhindre, at opgavekøposten kører unødigt.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Rutediagram for, hvornår opgavekøposter sættes på pause pga. inaktivitet.":::

Når værdien i feltet ikke er nul, og opgavekøen ikke fandt nogen ændringer i løbet af den seneste kørsel, sætter [!INCLUDE[prod_short](includes/prod_short.md)] opgavekøposten på pause. Når dette sker, viser feltet **Status for opgavekø** **Sat på pause pga. inaktivitet** og [!INCLUDE[prod_short](includes/prod_short.md)] venter på den tidsangivelse, der er angivet i feltet **Timeout for inaktivitet**, inden opgavekøposten køres igen.  

F.eks. vil den valutaopgavekø, der synkroniserer valutaer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med valutakurser i [!INCLUDE[prod_short](includes/prod_short.md)], søge efter ændringer i valutakurserne hvert 30. minut. Hvis der ikke findes nogen ændringer, pauser [!INCLUDE[prod_short](includes/prod_short.md)] valutaopgavekøposten i 720 minutter (seks timer). Hvis en valutakurs ændres i [!INCLUDE[prod_short](includes/prod_short.md)], mens opgavekøposten er sat på pause, aktiveres opgavekøposten automatisk på ny af [!INCLUDE[prod_short](includes/prod_short.md)], og opgavekøen genstartes. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] aktiverer automatisk opgavekøposter, der er sat på pause, når der sker ændringer i [!INCLUDE[prod_short](includes/prod_short.md)]. Ændringer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vil ikke aktivere opgavekøposter.

## <a name="to-view-the-synchronization-job-log"></a>Sådan får du vist synkroniseringsjobloggen

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationssynkroniseringslog**, og vælg derefter det relaterede link.
2. Hvis der er opstået en eller flere fejl i et synkroniseringsjob, vises antallet af fejl i kolonnen **Mislykkedes**. Vælg nummeret for at få vist fejlene for jobbet.  

    > [!TIP]  
    > Du kan få vist alle synkroniseringsjobfejl ved at åbne loggen over synkroniseringsjobfejl direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Sådan får du vist loggen over synkroniseringsjobbet fra tabeltilknytninger

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2. På siden **Integrationstabeltilknytninger**, vælger du en record og derefter vælger du **Integrationssynkronisering. Joblog**.  

## <a name="to-view-the-synchronization-error-log"></a>Sådan får du vist synkroniseringsfejlloggen

- Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationssynkroniseringsfejl**, og vælg derefter det relaterede link.

## <a name="see-also"></a>Se også

[Synkronisering af data i Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synkroniser tabeltilknytninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlægning af synkronisering mellem Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration Dynamics 365 Business Central med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]