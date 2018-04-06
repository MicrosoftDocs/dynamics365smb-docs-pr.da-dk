---
title: "Sådan konfigureres en virksomhed med guiden RapidStart | Microsoft Docs"
description: "Du kan hurtigt konfigurere en ny virksomhed, som du har oprettet ved hjælp af guiden RapidStart Services-konfiguration."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 264788142ab4f2a84df3e1c9da6e39503a7e820f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Konfigurere en virksomhed med guiden RapidStart
Du kan hurtigt konfigurere en ny virksomhed, som du har oprettet ved hjælp af guiden RapidStart Services-konfiguration.

I følgende procedure har du angivet debitoren med konfigurationspakken, der derefter installeres på en computer. Debitoren åbner den nye virksomhed, som ikke indeholder nogen debitordata. Du eller kunden følger derefter trinnene i guiden RapidStart Services, der er beskrevet i denne fremgangsmåde, for at levere grundlæggende oplysninger om virksomheden. Guiden importerer konfigurationspakken og anvender derefter pakken til virksomheden.  

## <a name="to-configure-a-new-company"></a>Konfigurere en ny virksomhed  
1. I rollecenteret RapidStart Services-implementering skal du vælge handlingen **Guiden RapidStart**.  
2. Udvid oversigtspanelet **Trin 1**, der indeholder generelle oplysninger om den nye virksomhed. Angiv de relevante oplysninger om den nye virksomhed i felterne. Der er et felt, som du skal udfylde: **Navn**. Det er valgfrit, om du vil udfylde resten af felterne.  
3. Udvid oversigtspanelet **Trin 2**, der indeholder kommunikations- og kontaktoplysninger om den nye virksomhed. Angiv de relevante oplysninger om den nye virksomhed i felterne.
4. Udvid oversigtspanelet **Trin 3**, der indeholder bankkonto- og betalingsoplysninger om den nye virksomhed. Angiv de relevante oplysninger om den nye virksomhed i felterne.  
5. Udvid oversigtspanelet **Trin 4**. Vælg knappen **AssistEdit** for at vælge den konfigurationspakke, du vil anvende. Navnet på konfigurationspakken vises. Derefter kan du udføre følgende handlinger i den anførte rækkefølge:  

    1. Anvend konfigurationen ved at vælge handlingen **Anvend pakke**. Dette importerer konfigurationspakken, og alle pakkedatabasedata anvendes på samme tid.  

    2. Gennemse konfigurationen, efter at den er blevet anvendt. Denne indstilling giver dig mulighed for at gennemse konfigurationsoplysninger og spørgeskemaer, der leveres af partneren, og importere nogle masterdata, der kræves til din virksomhed. Vælg handlingen **Konfigurationsregneark**. Yderligere oplysninger finder du i afsnittet "Sådan udfyldes konfigurationsspørgeskemaet" i [Indsaml debitoropsætningsværdier](admin-gather-customer-setup-values.md).  

6. Udvid oversigtspanelet **Trin 5**. Angiv, hvilket rollecenter der skal være standard for den nye virksomhed.  

    > [!IMPORTANT]  
    >  Rediger kun dit rollecenter, når du har afsluttet konfigurationen af virksomheden. Hvis du vil overveje og ændre flere konfigurationsoplysninger, skal du først bruge konfigurationsregnearket til at fortsætte arbejdet. Derefter skal du vende tilbage til guiden for at opdatere dit rollecenter eller vælge handlingen **Fuldfør installation**.

7. Vælg knappen **OK**.  
8. Hvis du vil kontrollere, at konfigurationsoplysningerne er blevet anvendt på den nye virksomhed, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Virksomhedsoplysninger** og derefter vælge det relaterede link.

Vinduet **Virksomhedsoplysninger** indeholder oplysninger, du har angivet.   

Du har nu konfigureret virksomheden og anvendt data.  

## <a name="see-also"></a>Se også  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)

