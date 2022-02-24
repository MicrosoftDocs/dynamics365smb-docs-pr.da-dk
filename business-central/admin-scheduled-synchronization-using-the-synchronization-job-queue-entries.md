---
title: Synkronisering af Business Central og Dynamics 365 Sales | Microsoft Docs
description: Få mere at vide om synkronisering af data mellem Business Central og Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879078"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales
Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-records og [!INCLUDE[crm_md](includes/crm_md.md)] -records, der tidligere har været sammenkædet. Synkroniseringsopgaver kan også oprette og sammenkæde nye records i destinationssystemet for records, der ikke allerede er sammenkædet, afhængigt af synkroniseringsretning og -regler. Der er flere standardsynkroniseringsjobs tilgængelige. Du kan få dem vist på siden **Records for jobkøer**. Du kan finde flere oplysninger i [Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Synkroniseringsproces  
Hver synkronisering af en jobkø-post benytter en bestemt integrationstabeltilknytning, der angiver, hvilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel og [!INCLUDE[crm_md](includes/crm_md.md)]-enhed, der skal synkroniseres. Tabeltilknytningerne omfatter også nogle indstillinger, der bestemmer, hvilke records i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[crm_md](includes/crm_md.md)]-enheden, der skal synkroniseres.  

For at kunne synkronisere data skal [!INCLUDE[crm_md](includes/crm_md.md)]-enheds-records være sammenkædet med [!INCLUDE[d365fin](includes/d365fin_md.md)]-records. F.eks. skal en [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitor være sammenkædet med en [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan konfigurere sammenkædninger manuelt, før du kører synkroniseringsjobbene, eller lade synkroniseringsjobbene konfigurere sammenkædninger automatisk. Den følgende liste beskriver, hvordan data synkroniseres mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], når du benytter posterne i synkroniseringsjobkøen. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

-   Afkrydsningfeltet **Synkroniser kun sammenkoblede poster** kontrollerer, hvorvidt nye poster oprettes, når du synkroniserer. Afkrydsningsfeltet er som standard markeret, hvilket betyder, at kun poster, der er sammenkoblede, synkroniseres. I integrationstabeltilknytningen kan du ændre tabeltilknytningen mellem en [!INCLUDE[crm_md](includes/crm_md.md)]-enhed og en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel, så integrationssynkroniseringsjobbene opretter nye poster i destinationsdatabasen for hver post i kildedatabasen, der ikke er sammenkoblet. Du kan finde flere oplysninger i [Oprettelse af Nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Eksempel**: Hvis du rydder afkrydsningsfeltet **Synkroniser kun sammenkoblede poster** når du synkroniserer kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] med konti i [!INCLUDE[crm_md](includes/crm_md.md)], oprettes der en ny konto til hver kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] og disse sammenkobles automatisk. Som følge af, at synkroniseringen går begge veje i dette tilfælde, vil der blive oprettet og sammenkoblet en ny kunde sammen for hver [!INCLUDE[crm_md](includes/crm_md.md)]-konto, der ikke allerede er sammenkoblet.  

    > [!NOTE]  
    > Der er regler og filtre, der bestemmer, hvilke data der synkroniseres. Du kan finde flere oplysninger under [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Når der oprettes nye records i [!INCLUDE[d365fin](includes/d365fin_md.md)], benytter de enten skabelonen, der er defineret til integrationstabeltilknytning eller standardskabelonen, der er tilgængelig for record-typen. Felter udfyldes automatisk med data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)] afhængigt af synkroniseringsretning. Du kan finde flere oplysninger i [Rediger tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Når der foretages flere synkroniseringer, er det kun records, der er blevet ændret eller tilføjet efter sidste gennemførte synkroniseringsjob for enheden, der opdateres.  

     Nye records i [!INCLUDE[crm_md](includes/crm_md.md)] tilføjes i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis data i felterne i [!INCLUDE[crm_md](includes/crm_md.md)]-records er ændret, kopieres disse data til det tilsvarende felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Ved synkronisering i begge retninger synkroniserer jobbet fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og derefter fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Poster for standardsynkroniseringsjobkø  
I følgende tabel beskrives standardsynkroniseringsjobbene.  

|Post for jobkø|Description|Retning|Integrationstabeltilknytning|Standardhyppighed for synkronisering (min.)|Standardangivelse for dvale ved inaktivitet (min.)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakter.|I begge retninger|KONTAKT|30|720 <br>(12 timer)| 
|VALUTA – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-transaktionsvalutaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|30|720 <br> (12 timer)| 
|KUNDE – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-konti med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorer.|I begge retninger|KUNDE|30|720<br> (12 timer)|
|KUNDEPRISGRUPPE -PRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgsprislister med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorprisgrupper.| |DEBITORPRISGRUPPER-SALGSPRISLISTER|30|1440<br> (24 timer)|
|VARE - PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-varer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|30|1440<br> (24 timer)|
|BOGFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)] fakturaer med [!INCLUDE[d365fin](includes/d365fin_md.md)] bogførte salgsfakturaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOGFØRTE SALGSFAKTURAER|30|1440<br> (24 timer)|
|RESSOURCE-PRODUKT – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-ressourcer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUKT|30|720<br> (12 timer)|  
|SÆLGERE – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[d365fin](includes/d365fin_md.md)]-sælgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brugere.|Fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SÆLGERE|30|1440<br> (24 timer)|
|SALGSPRIS- PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|30|1440<br> (24 timer)|
|MÅLEENHED – Dynamics 365 Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhedsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-måleenheder.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLEENHED|30|720<br> (12 timer)|  
|Debitorstatistik - Dynamics 365 Sales-synkroniseringsjob|Opdaterer [!INCLUDE[crm_md](includes/crm_md.md)] konti med seneste [!INCLUDE[d365fin](includes/d365fin_md.md)] debitordata. I [!INCLUDE[crm_md](includes/crm_md.md)] vises disse oplysninger i **Business Central kontostatistik** i hurtigvisningsformat over konti, der er sammenkædet med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorer.<br /><br /> Disse data skal også opdateres manuelt fra hver debitor-record. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Bemærk:**  denne jobkøpost er kun relevant, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Om Business Central integrationsløsning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ikke tilgængelig|Ikke tilgængelig|30|Ikke tilgængelig|   

## <a name="about-inactivity-timeouts"></a>Vedrørende timeoutperioder for inaktivitet
Nogle opgavekøposter, såsom dem, der planlægger synkronisering mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], anvender feltet **Timeout for inaktivitet** på kortet til Opgavekøpost for at forhindre, at opgavekøposten kører unødigt.  
<br><br>

> ![Rutediagram for, hvornår opgavekøposter sættes på pause pga. inaktivitet.](media/on-hold-with-inactivity-timeout.png)

Når værdien i feltet ikke er nul, og opgavekøen ikke fandt nogen ændringer i løbet af den seneste kørsel, sætter [!INCLUDE[d365fin](includes/d365fin_md.md)] opgavekøposten på pause. Når dette sker, viser feltet **Status for opgavekø** **Sat på pause pga. inaktivitet** og [!INCLUDE[d365fin](includes/d365fin_md.md)] venter på den tidsangivelse, der er angivet i feltet **Timeout for inaktivitet**, inden opgavekøposten køres igen. 

F.eks. vil den valutaopgavekø, der synkroniserer valutaer i [!INCLUDE[crm_md](includes/crm_md.md)] med valutakurser i [!INCLUDE[d365fin](includes/d365fin_md.md)], søge efter ændringer i valutakurserne hvert 30. minut. Hvis der ikke findes nogen ændringer, pauser [!INCLUDE[d365fin](includes/d365fin_md.md)] valutaopgavekøposten i 720 minutter (seks timer). Hvis en valutakurs ændres i [!INCLUDE[d365fin](includes/d365fin_md.md)], mens opgavekøposten er sat på pause, aktiveres opgavekøposten automatisk på ny af [!INCLUDE[d365fin](includes/d365fin_md.md)], og opgavekøen genstartes. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiverer automatisk opgavekøposter, der er sat på pause, når der sker ændringer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ændringer i [!INCLUDE[crm_md](includes/crm_md.md)] vil ikke aktivere opgavekøposter.

## <a name="to-view-the-synchronization-job-log"></a>Sådan får du vist synkroniseringsjobloggen  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationssynkroniseringslog**, og vælg derefter det relaterede link.
2.  Hvis der er opstået en eller flere fejl i et synkroniseringsjob, vises antallet af fejl i kolonnen **Mislykkedes**. Vælg nummeret for at få vist fejlene for jobbet.  

    > [!TIP]  
    > Du kan få vist alle synkroniseringsjobfejl ved at åbne loggen over synkroniseringsjobfejl direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Sådan får du vist loggen over synkroniseringsjobbet fra tabeltilknytninger  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationstabeltilknytninger**, og vælg derefter det relaterede link.
2.  På siden **Integrationstabeltilknytninger**, vælger du en record og derefter vælger du **Integrationssynkronisering. Joblog**.  

## <a name="to-view-the-synchronization-error-log"></a>Sådan får du vist synkroniseringsfejlloggen  
* Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Integrationssynkroniseringsfejl**, og vælg derefter det relaterede link.

## <a name="see-also"></a>Se også  
[Synkronisering af data i Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabeltilknytninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlægning af synkronisering mellem Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration af Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
