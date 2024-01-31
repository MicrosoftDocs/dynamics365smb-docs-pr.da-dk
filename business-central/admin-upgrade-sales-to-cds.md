---
title: Opgradering af en integration med Dynamics 365 Sales
description: 'Få mere at vide om, hvordan du kan flytte Dynamics 365 Business Central-integrationen med Dynamics 365 Sales til den nyeste version.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Opgradering af en integration med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] kan integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], hvilket gør det nemt at forbinde og synkronisere data med andre Dynamics 365-programmer såsom [!INCLUDE[crm_md](includes/crm_md.md)] eller endda apps, som du selv opbygger. Hvis det er første gang, du integrerer, anbefaler vi, at du gør det ved hjælp af [!INCLUDE[prod_short](includes/cds_long_md.md)]. Få flere oplysninger i [Integration med Dataverse](admin-common-data-service.md).

Hvis du allerede har integreret [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsætte med at synkronisere data ved hjælp af din installation. Men hvis du opgraderer [!INCLUDE[prod_short](includes/prod_short.md)] eller deaktiverer din [!INCLUDE[crm_md](includes/crm_md.md)]-integration, skal du oprette forbindelse igen via [!INCLUDE[prod_short](includes/cds_long_md.md)] for at aktivere den igen. 

> [!NOTE]
> Hvis du genopretter forbindelsen via [!INCLUDE[prod_short](includes/cds_long_md.md)], anvendes standardindstillingerne for synkroniseringen, og alle konfigurationer, du har angivet, tilsidesættes. Standard-tabeltilknytningerne anvendes for eksempel.

## Sådan opgraderer du din forbindelse til at bruge Dataverse
1. Åbn siden **Microsoft Dynamics 365-forbindelsesopsætning**, og deaktiver **Aktiveret**. Luk derefter siden for at afbryde forbindelsen fra [!INCLUDE[crm_md](includes/crm_md.md)].
2. Åbn siden **Dataverse-forbindelsesopsætning**, og vælg **Person** i feltet **ejerskabsmodel**. Du skal aktivere forbindelsen til aktivere **Aktiveret** [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til Dataverse.
4. På siden **Microsoft Dynamics 365-forbindelsesopsætning** vælges derefter **Geninstaller integrationsløsning** for at installere og konfigurere den opgraderede Business Central-integrationsløsning.
5. Du skal aktivere forbindelsen til ved at slå **Aktiveret** til [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Når du har aktiveret forbindelsen, installeres Business Central-basisintegrationsløsningen til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette muliggør integration med tabeller, der er specifikke for [!INCLUDE[crm_md](includes/crm_md.md)], f.eks. salgsordrer, tilbud og fakturaer.
6. På siden **Opsætning af Sales-forbindelse** skal du vælge **Brug standard-synkroniseringsopsætning** for at starte integrationstabeltilknytninger for [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!IMPORTANT]
   > Når du bruger handlingen **Brug standardsynkronisering af opsætning**, anvendes standardtilknytningerne for integrationstabellen. Alle brugerdefinerede tilknytninger overskrives. Hvis du har brugerdefinerede tilknytninger, som du vil bevare, anbefales det, at du eksporterer dem til Excel eller taler med din Microsoft-partner om andre metoder til at holde styr på dine egne tilknytninger.    

## Se også
[Integration med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integration med Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]