---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Det var muligt at hente data fra forskellige firmaer i en enkelt rapport med OData-webtjenester. Men siden [!INCLUDE [prod_short](prod_short.md)] 2021 Udgivelsesbølge 2, hvor kun ODataV4 understøttes, kan der ikke eksporterer data fra flere regnskaber. Funktionen **$Expand** i Power BI, som du tænker kan være en anden måde at oprette en rapport på med flere virksomheder, kan heller ikke bruges. Den vil oprette en kolonne med firmanavnet, men vil ikke blive udfyldt med firmadataene efter en opdatering.