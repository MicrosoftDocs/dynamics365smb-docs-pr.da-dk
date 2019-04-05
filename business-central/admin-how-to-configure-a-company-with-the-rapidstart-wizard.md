---
title: Sådan konfigureres en virksomhed med guiden RapidStart | Microsoft Docs
description: Du kan hurtigt konfigurere en ny virksomhed, som du har oprettet ved hjælp af guiden RapidStart Services-konfiguration.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 63120671100b7caac7f3cb08bd3fbbcd1d29ff5c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792870"
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

    2. Gennemse konfigurationen, efter at den er blevet anvendt. Denne indstilling giver dig mulighed for at gennemse konfigurationsoplysninger og spørgeskemaer, der leveres af partneren, og importere nogle masterdata, der kræves til din virksomhed. Vælg handlingen **Konfigurationsregneark**. Du kan finde flere oplysninger i [Sådan udfyldes konfigurationsspørgeskemaet](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Udvid oversigtspanelet **Trin 5**. Angiv, hvilket rollecenter der skal være standard for den nye virksomhed.  

    > [!IMPORTANT]  
    >  Rediger kun dit rollecenter, når du har afsluttet konfigurationen af virksomheden. Hvis du vil overveje og ændre flere konfigurationsoplysninger, skal du først bruge konfigurationsregnearket til at fortsætte arbejdet. Derefter skal du vende tilbage til guiden for at opdatere dit rollecenter eller vælge handlingen **Fuldfør installation**.

7. Vælg knappen **OK**.  
8. Hvis du vil kontrollere, at konfigurationsoplysningerne er blevet anvendt på den nye virksomhed, skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Virksomhedsoplysninger** og derefter vælge det relaterede link.

Siden **Virksomhedsoplysninger** indeholder oplysninger, du har angivet.   

Du har nu konfigureret virksomheden og anvendt data.  

## <a name="see-also"></a>Se også  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
