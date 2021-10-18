---
title: Kobling og synkronisering
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 Sales-tabellen, der er sammenkædet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8e2b36b4b90e1cc348ef381a6d0f6145a87ed043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588722"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Kobling og synkronisering af poster mellem Dataverse og Business Central

Dette emne handler om, hvordan du sammenkæder en eller flere poster i [!INCLUDE[prod_short](includes/prod_short.md)] med poster i Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)]. Sammenkædning af records lader dig se Dataverse-oplysninger i [!INCLUDE[prod_short](includes/prod_short.md)] og omvendt. Sammenkædningen gør det også muligt at synkronisere data mellem records. Du kan sammenkæde eksisterende records eller oprette og sammenkæde nye records.

> [!Note]
> Sammenkædning og synkronisering af data er kun mulig, hvis din systemadministrator har oprettet en forbindelse mellem [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)]. Dette kan hurtigt kontrolleres ved at åbne **debitor**-kortet og søge efter handlingen **Konfigurer sammenkædning**. Hvis handlingen er tilgængelig, er programmerne forbundet.   

## <a name="video-example"></a>Videoeksempel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Sådan sammenkædes en record  
1.  Åbn kortet i [!INCLUDE[prod_short](includes/prod_short.md)] til den record, du ønsker at sammenkæde. F.eks. debitor- eller kontaktkortet.  

    Du kan også blot åbne listesiden og vælge den record, du vil sammenkæde.  

2.  Vælg handlingen **Konfigurer sammenkædning**.  
3.  Udfyld felterne, og vælg derefter **OK**.  

## <a name="to-synchronize-a-single-record"></a>Sådan synkroniseres en enkelt record  
1.  Åbn kortet i [!INCLUDE[prod_short](includes/prod_short.md)] til den record, du ønsker at sammenkæde. F.eks. debitor- eller kontaktkortet.  
2.  Vælg handlingen **Synkroniser nu**.  
3.  Hvis en post kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Sådan synkroniseres en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Åbn formularen til den post, du vil sammenkæde, i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan f.eks. være Kontokort- eller Kontaktkort-formularen.  
2.  Vælg handlingen **[!INCLUDE[prod_short](includes/prod_short.md)]** på båndet for at åbne og sammenkæde posten automatisk.

> [!Note]
> Du kan kun synkronisere en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk, når **Synkroniser kun sammenkædede poster** er deaktiveret, og synkroniseringsretningen angives til Tovejs eller Fra integrationstabel på siden **Integrationstabelknytning** for posten. Få flere oplysninger i [Tilknytning af tabeller og felter, der skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Sådan sammensætter du flere poster ved hjælp af matchbaseret sammenkædning

Du kan angive de data, der skal synkroniseres for et objekt, f.eks. kunde eller kontakt ved at sammenkæde poster baseret på matches. Du kan begrænse overensstemmelserne ved at gøre søgningen forskel og tildele en prioritet for hver match. Hvis der ikke findes noget match, kan du også angive, at du vil oprette objektet i Dataverse. Yderligere oplysninger finder du under [Tilpasse den matchbaserede sammenkædning](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. Åbn listesiden i [!INCLUDE[prod_short](includes/prod_short.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.
2. Vælg den **matchbaserede sammenkædningshandling**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Sådan synkroniseres flere records  
1.  Åbn listesiden i [!INCLUDE[prod_short](includes/prod_short.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.  
2.  Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.  
3.  Hvis poster kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.  

## <a name="uncoupling-records"></a>Ophævelse af sammenkædning af poster
Du kan fjerne frakoble en eller flere poster fra listesider eller siden **Koblede datasynkroniseringsfejl** ved at vælge en eller flere linjer og vælge **Slet kobling**. Du kan også fjerne alle koblinger for en eller flere tabeltilknytninger på siden **Tilknytninger til integrationstabel**.

## <a name="see-also"></a>Se også  
[Bruge Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]