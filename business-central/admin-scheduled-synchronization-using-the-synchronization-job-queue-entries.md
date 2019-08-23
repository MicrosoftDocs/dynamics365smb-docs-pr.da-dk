---
title: Synkronisering af Business Central og Dynamics 365 for Sales | Microsoft Docs
description: Få mere at vide om synkronisering af data mellem Business Central og Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/16/2019
ms.author: bholtorf
ms.openlocfilehash: 9290730bb559d4ac03a437a49ed81b09f3c01853
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755214"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-for-sales"></a>Planlægning af synkronisering mellem Business Central og Dynamics 365 for Sales
Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] med planlagte intervaller ved at konfigurere jobs i jobkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-records og [!INCLUDE[crm_md](includes/crm_md.md)] -records, der tidligere har været sammenkædet. Synkroniseringsopgaver kan også oprette og sammenkæde nye records i destinationssystemet for records, der ikke allerede er sammenkædet, afhængigt af synkroniseringsretning og -regler. Der er flere standardsynkroniseringsjobs tilgængelige. Du kan få dem vist på siden **Records for jobkøer**. Du kan finde flere oplysninger i [Brug af opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synkroniseringsproces  
Hver synkronisering af en jobkø-post benytter en bestemt integrationstabeltilknytning, der angiver, hvilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel og [!INCLUDE[crm_md](includes/crm_md.md)]-enhed, der skal synkroniseres. Tabeltilknytningerne omfatter også nogle indstillinger, der bestemmer, hvilke records i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[crm_md](includes/crm_md.md)]-enheden, der skal synkroniseres.  

For at kunne synkronisere data skal [!INCLUDE[crm_md](includes/crm_md.md)]-enheds-records være sammenkædet med [!INCLUDE[d365fin](includes/d365fin_md.md)]-records. F.eks. skal en [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitor være sammenkædet med en [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan konfigurere sammenkædninger manuelt, før du kører synkroniseringsjobbene, eller lade synkroniseringsjobbene konfigurere sammenkædninger automatisk. Den følgende liste beskriver, hvordan data synkroniseres mellem [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], når du benytter posterne i synkroniseringsjobkøen. Du kan finde flere oplysninger i [Sammenkæd og synkroniser poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Som standard synkroniseres kun records i [!INCLUDE[d365fin](includes/d365fin_md.md)], der er sammenkædet med records i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan ændre tabeltilknytningen mellem en [!INCLUDE[crm_md](includes/crm_md.md)]-enhed og en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel, så integrationssynkroniseringsjobbene opretter nye records i destinationsdatabasen for hver record i kildedatabasen, der ikke er sammenkædet. De nye records sammenkædes også med de tilsvarende records i kilden. Når du f.eks. synkroniserer debitorer med [!INCLUDE[crm_md](includes/crm_md.md)]-konti, oprettes en ny konto-record for hver debitor i [!INCLUDE[d365fin](includes/d365fin_md.md)]. De nye konti sammenkædes automatisk med debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Da synkroniseringen i dette tilfælde går begge veje, oprettes og sammenkædes en ny debitor for hver [!INCLUDE[crm_md](includes/crm_md.md)]-konto, der ikke allerede er sammenkædet.  

    > [!NOTE]  
    > Der er regler og filtre, der bestemmer, hvilke data der synkroniseres. Du kan finde flere oplysninger under [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Når der oprettes nye records i [!INCLUDE[d365fin](includes/d365fin_md.md)], benytter de enten skabelonen, der er defineret til integrationstabeltilknytning eller standardskabelonen, der er tilgængelig for record-typen. Felter udfyldes automatisk med data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)] afhængigt af synkroniseringsretning. Du kan finde flere oplysninger i [Sådan redigeres tabeltilknytninger til synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Når der foretages flere synkroniseringer, er det kun records, der er blevet ændret eller tilføjet efter sidste gennemførte synkroniseringsjob for enheden, der opdateres.  

     Nye records i [!INCLUDE[crm_md](includes/crm_md.md)] tilføjes i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis data i felterne i [!INCLUDE[crm_md](includes/crm_md.md)]-records er ændret, kopieres disse data til det tilsvarende felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Ved synkronisering i begge retninger synkroniserer jobbet fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og derefter fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Poster for standardsynkroniseringsjobkø  
I følgende tabel beskrives standardsynkroniseringsjobbene.  

|Post for jobkø|Description|Retning|Integrationstabeltilknytning|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|KONTAKT - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakter.|I begge retninger|KONTAKT|  
|VALUTA - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-transaktionsvalutaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VALUTA|  
|DEBITOR - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-konti med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorer.|I begge retninger|KUNDE|  
|KUNDEPRISGRUPPE -PRIS - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgsprislister med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorprisgrupper.| |DEBITORPRISGRUPPER-SALGSPRISLISTER|
|VARE - PRODUKT - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-varer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|
|BOGFØRTE SALGSFAKTURAER-FAKTURAER - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)] fakturaer med [!INCLUDE[d365fin](includes/d365fin_md.md)] bogførte salgsfakturaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOGFØRTE SALGSFAKTURAER|
|RESSOURCE-PRODUKT - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-ressourcer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE-PRODUKT|  
|SÆLGERE - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[d365fin](includes/d365fin_md.md)]-sælgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brugere.|Fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SÆLGERE|
|SALGSPRIS- PRODUKTPRIS - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|
|MÅLEENHED - Dynamics 365 for Sales-synkroniseringsjob|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhedsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-måleenheder.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLEENHED|  
|Debitorstatistik - Dynamics 365 for Sales-synkroniseringsjob|Opdaterer [!INCLUDE[crm_md](includes/crm_md.md)] konti med seneste [!INCLUDE[d365fin](includes/d365fin_md.md)] debitordata. I [!INCLUDE[crm_md](includes/crm_md.md)] vises disse oplysninger i **Business Central kontostatistik** i hurtigvisningsformat over konti, der er sammenkædet med [!INCLUDE[d365fin](includes/d365fin_md.md)]-debitorer.<br /><br /> Disse data skal også opdateres manuelt fra hver debitor-record. Du kan finde flere oplysninger i [Sådan sammenkædes og synkroniseres records manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Bemærk:**  denne jobkøpost er kun relevant, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] integrationsløsningen er installeret i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan finde flere oplysninger i [Om Business Central integrationsløsning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ikke tilgængelig.|Ikke tilgængelig.|   

## <a name="to-view-the-synchronization-job-log"></a>Sådan får du vist synkroniseringsjobloggen  
1. Vælg ![lyspære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Integrationssynkroniseringslog**, og vælg derefter det tilhørende link.
2.  Hvis der er opstået en eller flere fejl i et synkroniseringsjob, vises antallet af fejl i kolonnen **Mislykkedes**. Vælg nummeret for at få vist fejlene for jobbet.  

    > [!TIP]  
    > Du kan få vist alle synkroniseringsjobfejl ved at åbne loggen over synkroniseringsjobfejl direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Sådan får du vist loggen over synkroniseringsjobbet fra tabeltilknytninger  
1. Vælg ![elpære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig")-ikon, gå til **Integration af tabeltilknytning**, og vælg derefter det tilhørende link.
2.  På siden **Integrationstabeltilknytninger**, vælger du en record og derefter vælger du **Integrationssynkronisering. Joblog**.  

## <a name="to-view-the-synchronization-error-log"></a>Sådan får du vist synkroniseringsfejlloggen  
* Vælg ![lyspære-ikonet, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), gå til **Integrationssynkroniseringsfejl**, og vælg derefter det tilhørende link.

## <a name="see-also"></a>Se også  
[Synkronisering af data i Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkroniser tabeltilknytninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlægning af synkronisering mellem Business Central og Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integration Dynamics 365 Business Central med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



