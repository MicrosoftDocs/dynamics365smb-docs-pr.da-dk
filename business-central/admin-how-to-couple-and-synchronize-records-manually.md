---
title: Kobling og synkronisering | Microsoft Docs
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 Sales-tabellen, der er sammenkædet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 53b12b6ab7e53a20bb1b8fcc659b2f1454e85321
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779928"
---
# <a name="coupling-and-synchronizing"></a>Kobling og synkronisering
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

## <a name="to-synchronize-multiple-records"></a>Sådan synkroniseres flere records  
1.  Åbn listesiden i [!INCLUDE[prod_short](includes/prod_short.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.  
2.  Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.  
3.  Hvis poster kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.  

## <a name="uncoupling-records"></a>Ophævelse af sammenkædning af poster
Du kan fjerne frakoble en eller flere poster fra listesider eller siden **Koblede datasynkroniseringsfejl** ved at vælge en eller flere linjer og vælge **Slet kobling**. Du kan også fjerne alle koblinger for en eller flere tabeltilknytninger på siden **Tilknytninger til integrationstabel**.

## <a name="see-also"></a>Se også  
[Bruge Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]