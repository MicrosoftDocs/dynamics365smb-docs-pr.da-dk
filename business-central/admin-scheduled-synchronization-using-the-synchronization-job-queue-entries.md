---
title: Synkronisere Business Central og Dataverse
description: Få mere at vide om synkronisering af data mellem Business Central og Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# Planlægning af synkronisering mellem Business Central og Dataverse

Du kan synkronisere [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[prod_short](includes/prod_short.md)]-poster og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-poster, der tidligere har været sammenkædet. For poster, der ikke allerede er sammenkædet, og afhængigt af synkroniseringsretning og -regler, kan der oprettes og sammenkædes nye poster i destinationssystemet.

Der er flere standardsynkroniseringsjobs tilgængelige. Jobbene køres i følgende rækkefølge for at undgå sammenkædning af afhængigheder mellem tabeller. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

1. VALUTA - Common Data Service-synkroniseringsjob.
2. LEVERANDØR - Common Data Service-synkroniseringsjob.
3. KONTAKT - Common Data Service-synkroniseringsjob.
4. DEBITOR - Common Data Service-synkroniseringsjob.
5. SÆLGERE - Common Data Service-synkroniseringsjob.

Du kan se job på siden **Poster for jobkøer**. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## Poster i standardsynkroniseringsjobkø

Følgende tabel viser standardsynkroniseringsjobbene for [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Post for jobkø | Description | Retning | Integrationstabeltilknytning | Standardhyppighed for synkronisering (min.) | Standardangivelse for dvale ved inaktivitet (min.) |
|--|--|--|--|--|--|--|
| KONTAKT - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-kontakter med [!INCLUDE[prod_short](includes/prod_short.md)]-kontakter. | I begge retninger | KONTAKT | 30 | 720 <br>(12 timer) |
| VALUTA - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-transaktionsvalutaer med [!INCLUDE[prod_short](includes/prod_short.md)]-valutaer. | Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | VALUTA | 30 | 720 <br> (12 timer) |
| DEBITOR - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konti med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer. | I begge retninger | KUNDE | 30 | 720<br> (12 timer) |
| LEVERANDØR - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konti med [!INCLUDE[prod_short](includes/prod_short.md)]-debitorer. | I begge retninger | KREDITOR | 30 | 720<br> (12 timer) |
| SÆLGERE - Common Data Service-synkroniseringsjob | Synkroniserer [!INCLUDE[prod_short](includes/prod_short.md)]-sælgere med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-brugere. | Fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] | SÆLGERE | 30 | 1440<br> (24 timer) |

## Synkroniseringsproces

Hver synkronisering af en jobkø-post benytter en bestemt integrationstabeltilknytning, der angiver, hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-tabel og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel, der skal synkroniseres. Tabeltilknytningerne omfatter også nogle indstillinger, der bestemmer, hvilke records i [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellen, der skal synkroniseres.  

For at kunne synkronisere data skal [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabelposter være sammenkædet med [!INCLUDE[prod_short](includes/prod_short.md)]-records. F.eks. skal en [!INCLUDE[prod_short](includes/prod_short.md)]-debitor være sammenkædet med en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto. Du kan konfigurere sammenkædninger manuelt, før du kører synkroniseringsjobbene, eller lade synkroniseringsjobbene konfigurere sammenkædninger automatisk. Den følgende liste beskriver, hvordan data synkroniseres mellem [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], når du benytter posterne i synkroniseringsjobkøen. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

- Afkrydsningfeltet **Synkroniser kun sammenkoblede poster** kontrollerer, hvorvidt nye poster oprettes, når du synkroniserer. Afkrydsningsfeltet er som standard markeret, hvilket betyder, at kun poster, der er sammenkoblede, synkroniseres. I integrationstabeltilknytningen kan du ændre tabeltilknytningen mellem en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel og en [!INCLUDE[prod_short](includes/prod_short.md)]-tabel, så integrationssynkroniseringsjobbene opretter nye poster i destinationsdatabasen for hver række i kildedatabasen, der ikke er sammenkoblet. Du kan finde flere oplysninger i [Oprettelse af Nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Eksempel**: Hvis du rydder afkrydsningsfeltet **Synkroniser kun sammenkoblede poster** når du synkroniserer kunder i [!INCLUDE[prod_short](includes/prod_short.md)] med konti i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], oprettes der en ny konto til hver kunde i [!INCLUDE[prod_short](includes/prod_short.md)] og disse sammenkobles automatisk. Som følge af, at synkroniseringen går begge veje i dette tilfælde, vil der blive oprettet og sammenkoblet en ny kunde sammen for hver [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto, der ikke allerede er sammenkoblet.  

    > [!NOTE]  
    > Der er regler og filtre, der bestemmer, hvilke data der synkroniseres. Du kan finde flere oplysninger i [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md).

- Når der oprettes nye records i [!INCLUDE[prod_short](includes/prod_short.md)], benytter de enten skabelonen, der er defineret til integrationstabeltilknytning eller standardskabelonen, der er tilgængelig for rækketypen. Felter udfyldes automatisk med data fra [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[cds_long_md](includes/cds_long_md.md)] afhængigt af synkroniseringsretning. Du kan finde flere oplysninger i [Rediger tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Når der foretages flere synkroniseringer, er det kun records, der er blevet ændret eller tilføjet efter sidste gennemførte synkroniseringsjob for tabellen, der opdateres.  

     Nye records i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] tilføjes i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis data i felterne i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-records er ændret, kopieres disse data til det tilsvarende felt i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Ved synkronisering i begge retninger synkroniserer jobbet fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], og derefter fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

## Vedrørende inaktive timeoutperioder

Nogle opgavekøposter, såsom dem, der planlægger synkronisering mellem [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)], anvender feltet **Timeout for inaktivitet** på siden **Opgavekøpost** til at forhindre, at opgavekøposten kører unødigt.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Rutediagram for, hvornår opgavekøposter sættes på pause pga. inaktivitet.":::

Når værdien i feltet ikke er nul, og opgavekøen ikke fandt nogen ændringer i løbet af den seneste kørsel, sætter [!INCLUDE[prod_short](includes/prod_short.md)] opgavekøposten på pause. Når dette sker, viser feltet **Status for opgavekø** **Sat på pause pga. inaktivitet** og [!INCLUDE[prod_short](includes/prod_short.md)] venter på den tidsangivelse, der er angivet i feltet **Timeout for inaktivitet**, inden opgavekøposten køres igen.  

F.eks. vil den valutaopgavekø, der synkroniserer valutaer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med valutakurser i [!INCLUDE[prod_short](includes/prod_short.md)], søge efter ændringer i valutakurserne hvert 30. minut. Hvis der ingen ændringer er, sætter [!INCLUDE[prod_short](includes/prod_short.md)] opgavekøposten VALUTA på pause i 720 minutter (12 timer). Hvis en valutakurs ændres i [!INCLUDE[prod_short](includes/prod_short.md)], mens opgavekøposten er sat på pause, aktiveres opgavekøposten automatisk på ny af [!INCLUDE[prod_short](includes/prod_short.md)], og opgavekøen genstartes. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] aktiverer automatisk opgavekøposter, der er sat på pause, når der sker ændringer i [!INCLUDE[prod_short](includes/prod_short.md)]. Ændringer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vil ikke aktivere opgavekøposter.

## Sådan får du vist synkroniseringsjobloggen

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationssynkroniseringslog**, og vælg derefter det relaterede link.
2. Hvis der er opstået en eller flere fejl i et synkroniseringsjob, vises antallet af fejl i kolonnen **Mislykkedes**. Vælg nummeret for at få vist fejlene for jobbet.  

    > [!TIP]  
    > Du kan få vist alle synkroniseringsjobfejl ved at åbne loggen over synkroniseringsjobfejl direkte.

## Sådan får du vist loggen over synkroniseringsjobbet fra tabeltilknytninger

1. Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2. På siden **Integrationstabeltilknytninger**, vælger du en record og derefter vælger du **Integrationssynkronisering. Joblog**.  

## Sådan får du vist synkroniseringsfejlloggen

- Vælg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, åbn **Integrationssynkroniseringsfejl**, og vælg derefter det relaterede link.

## Se også

[Synkronisering af data i Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabeltilknytninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlægning af synkronisering mellem Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration Dynamics 365 Business Central med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
