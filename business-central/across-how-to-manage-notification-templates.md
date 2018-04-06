---
title: "Sådan administrerer du notifikationsskabeloner | Microsoft Docs"
description: "Notifikationer sendes til arbejdsgangsbrugere for at give dem besked om trin, de skal foretage, eller informere dem om statussen for trin i arbejdsgangen. Du konfigurerer, hvem der modtager besked og hvornår, ved opsætning af godkendelsesbrugere, brugernes notifikationsplan og de involverede arbejdsgangssvar for at definere notifikationsmodtageren. Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d6c7637527c9a93024ee62dbdd32ba63d665661d
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="manage-notification-templates"></a>Administrere notifikationsskabeloner
Notifikationer sendes til arbejdsgangsbrugere for at give dem besked om trin, de skal foretage, eller informere dem om statussen for trin i arbejdsgangen. Du konfigurerer, hvem der modtager besked og hvornår, ved opsætning af godkendelsesbrugere, brugernes notifikationsplan og de involverede arbejdsgangssvar for at definere notifikationsmodtageren. Du kan finde flere oplysninger i [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md).  

 Notifikationer er baseret på skabeloner, der definerer indholdet og layoutet af notifikationen. Du kan eksportere indholdet af en notifikationsskabelon, redigere den og derefter importere til den samme eller en ny notifikationsskabelon. Dette beskrives i følgende fremgangsmåder.  

 Den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder tre notifikationsskabeloner, en til at give besked om godkendelsesanmodninger, en til at give besked om nye poster og en til at give besked om forfaldne godkendelsesanmodninger. De tre foruddefinerede notifikationsskabeloner understøtter **Mail** og **Note** som notifikationsmetode. Hvis du vil se indholdet af de tre notifikationsskabeloner, skal du se i afsnittet "Indholdet af notifikationsskabelonerne" i dette emne.

## <a name="to-create-a-new-notification-template"></a>Sådan opretter du en ny notifikationsskabelon  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Notifikationsskabeloner**, og vælg derefter det relaterede link.  
2.  I vinduet **Notifikationsskabeloner** skal du vælge handlingen **Ny**.  
3.  Udfyld felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Identificer notifikationsskabelonen.|  
    |**Beskrivelse**|Beskriv notifikationsskabelonen.|  
    |**Notifikationsmetode**|Angiv, om notifikationen er sendt via mail eller som en note.|  
    |**Type**|Angiv de forretningsprocesser, som notifikationen skal bruges til.<br /><br /> Vælg én af følgende typer:<br /><br /> -   **Godkendelse** angiver, at skabelonen bruges til at give besked til brugere i godendelsesworkflows.<br />-   **Ny post** angiver, at skabelonen har til formål at give godkenderne besked, når en ny post, f.eks. et debitorkort, kræver deres godkendelse.<br />-   **Forfald** angiver, at skabelonen skal bruges til at underrette brugere om forfaldne godkendelsesanmodninger.|  
    |**Standard**|Angiv, om notifikationsskabelonen skal bruges som standard.|  

## <a name="to-modify-a-notification-template"></a>Sådan redigerer du en notifikationsskabelon  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Notifikationsskabeloner**, og vælg derefter det relaterede link.  
2.  I vinduet **Notifikationsskabeloner** skal du vælge den notifikationsskabelon, du vil redigere.  
3.  Vælg handlingen **Eksportér skabelonindhold**.  
4.  I vinduet **Udlæs fil** skal du klikke på knappen **Gem** og derefter navngive og gemme HTML-filen et relevant sted.  
5.  Højreklik på filen fil, vælg **Åbn med**, og vælg derefter det relevante program.  

    > [!NOTE]  
    >  Indhold til notifikationsskabeloner af typen Mail er i HTML-format. Indhold til notifikationsskabeloner af typen Note er i TXT-format.  
6.  Redigér indholdet af notifikationsskabelonen ved at tilføje, ændre eller fjerne parametervariabler for at definere det ønskede, og gem den. Du kan finde flere oplysninger i afsnittet "Indholdet af feltet notifikationsskabeloner".  

    Fortsæt med at indlæse det redigerede indhold tilbage til samme notifikationsskabelon eller til en ny.  
7.  For at redigere den notifikationsskabelon, du har eksporteret, skal du i vinduet **Notifikationsskabeloner** vælge den skabelon, du valgte i trin 2.  

    Du kan også importere det redigerede skabelonindhold til en ny notifikationsskabelon ved at følge proceduren i "Sådan opretter du en ny notifikationsskabelon" og vælge den nye notifikationsskabelon.  
8.  Vælg handlingen **Importér skabelonindhold**.  
9. Hvis du vil redigere en eksisterende notifikationsskabelon, skal du klikke på knappen **Ja** på meddelelsen om, at den eksisterende skabelon overskrives.  
10. I vinduet **Vælg en fil, der skal importeres** skal du vælge den HTML-fil, du ændrede i trin 6, og derefter klikke på knappen **Åbn**.  

Eksisterende eller nye notifikationsskabeloner i vinduet **Notifikationsskabeloner** opdateres nu med det redigerede indhold.  

### <a name="content-of-the-notification-templates"></a>Indhold af notifikationsskabelonerne  
De tre typer af notifikationsskabelon, **Ny post**, **Godkendelse** og **Forfald**, har forskelligt indhold.  

Parameterværdierne indsættes automatisk i notifikationer i overensstemmelse med typen af notifikationsskabelon.  

#### <a name="new-record"></a>Ny post  
 ![NAV&#95;notification&#95;template&#95;new&#95;record&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Godkendelse  
 ![NAV&#95;notification&#95;template&#95;approval&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Forfald  
 ![NAV&#95;notification&#95;overdue&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Se også  
 [Konfiguration af arbejdsgangsnotifikationer](across-setting-up-workflow-notifications.md)   
 [Konfigurere mail](admin-how-setup-email.md)   
 [Oprette brugere til arbejdsgange](across-how-to-set-up-workflow-users.md)   
 [Konfigurere godkendelsesbrugere](across-how-to-set-up-approval-users.md)   
 [Oprette arbejdsgange](across-how-to-create-workflows.md)   
 [Du kan bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)   
 [Workflow](across-workflow.md)   

