---
title: Sammenkæd og synkroniser records manuelt| Microsoft Docs
description: Synkronisering af en integreret tabeltilknytning muliggør synkronisering af data i alle records i en tabel i Business Central og Dynamics 365 Sales-enheden, der er sammenkædet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: fdc407ef26d238ba54a2566cdd9003c29da2eeb3
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196659"
---
# <a name="couple-and-synchronize-records-manually"></a>Sammenkæd og synkroniser records manuelt
Dette emne handler om, hvordan du sammenkæder en eller flere poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)]. Sammenkædning af records lader dig se Common Data Service-oplysninger i [!INCLUDE[d365fin](includes/d365fin_md.md)] og omvendt. Sammenkædningen gør det også muligt at synkronisere data mellem records. Du kan sammenkæde eksisterende records eller oprette og sammenkæde nye records.

> [!Note]
> Sammenkædning og synkronisering af data er kun mulig, hvis din systemadministrator har oprettet en forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)]. Dette kan hurtigt kontrolleres ved at åbne **debitor**-kortet og søge efter handlingen **Konfigurer sammenkædning**. Hvis handlingen er tilgængelig, er programmerne forbundet.   

## <a name="video-example"></a>Videoeksempel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Sådan sammenkædes en record  
1.  Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde. F.eks. debitor- eller kontaktkortet.  

    Du kan også blot åbne listesiden og vælge den record, du vil sammenkæde.  

2.  Vælg handlingen **Konfigurer sammenkædning**.  
3.  Udfyld felterne, og vælg derefter **OK**.  

## <a name="to-synchronize-a-single-record"></a>Sådan synkroniseres en enkelt record  
1.  Åbn kortet i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den record, du ønsker at sammenkæde. F.eks. debitor- eller kontaktkortet.  
2.  Vælg handlingen **Synkroniser nu**.  
3.  Hvis en post kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Sådan synkroniseres en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Åbn formularen til den post, du vil sammenkæde, i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan f.eks. være Kontokort- eller Kontaktkort-formularen.  
2.  Vælg handlingen **[!INCLUDE[d365fin](includes/d365fin_md.md)]** på båndet for at åbne og sammenkæde posten automatisk.

> [!Note]
> Du kan kun synkronisere en enkelt post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk, når **Synkroniser kun sammenkædede poster** er deaktiveret, og synkroniseringsretningen angives til Tovejs eller Fra integrationstabel på siden **Integrationstabelknytning** for posten. Få flere oplysninger i [Tilknytning af tabeller og felter, der skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Sådan synkroniseres flere records  
1.  Åbn listesiden i [!INCLUDE[d365fin](includes/d365fin_md.md)] den record, f.eks. listesiderne for kunder (debitorer) eller kontakter.  
2.  Vælg de records, du vil synkronisere, og vælg derefter handlingen **Synkroniser nu**.  
3.  Hvis poster kan synkroniseres i én retning, skal du vælge den valgmulighed, der angiver retningen for dataopdateringen, og derefter vælge **OK**.  

## <a name="see-also"></a>Se også  
[Bruge Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)
