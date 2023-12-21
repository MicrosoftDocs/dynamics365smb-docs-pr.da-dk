---
title: Bruger-adgangsflow til Microsoft 365-licenser
description: 'Få et overblik over, hvad der sker, når en bruger åbner Business Central-data med deres Microsoft 365-licens første gang.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a>Bruger-adgangsflow til Microsoft 365-licenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Denne artikel beskriver, hvad der sker, når en bruger åbner Business Central-data med deres Microsoft 365-licens første gang. Ved at forstå dette flow kan administratorer planlægge deres metode og konfigurere Business Central, så de passer til virksomhedens forretningsbehov.

1. Først godkendes brugerens identitet 
2. Business Central kontrollerer, at alle [minimumkravene](admin-access-with-m365-license.md#minimum-requirements) er opfyldt.
3. Business Central kontrollerer, at denne bruger ikke har en større licens, f. eks. en Business Central-licens eller en administrativ rolle som f. eks. en administratorrolle. 
4. Business Central kontrollerer, om brugeren får adgang til data, der hører til et miljø, som har aktiveret adgang med Microsoft 365-licenser. 
5. Brugerposten er klargjort i Business central, tildeling af den brugergruppe, profil og tilladelsessæt, der er defineret på siden med Microsoft 365-licenskonfiguration. Som standard tildeles Teams-brugergruppen, medarbejderprofilen tildeles, og kun logon-tilladelsessættet tildeles. Alle andre standard brugerindstillinger anvendes også ligesom en licenseret Business Central-bruger. 
6. Modellen Full Business central-sikkerhed bestemmer, om brugeren skal kunne få adgang til posten, siden, i det angivne regnskab og i det angivne miljø. 

Hvis alle trin lykkes, kan brugeren nu få vist disse Business Central-data i Teams. Business central-tjenesten sikrer automatisk skrivebeskyttet adgang og forenkler UI. 

Brugerkontoen er nu registreret i Business central og kan administreres som en hvilken som helst Business Central-bruger.

> [!NOTE]
> Trinnene kan variere afhængigt af den yderligere sikkerhedskonfiguration, du har angivet i Microsoft 365 eller Business central.

## <a name="see-also"></a>Se også

[Business Central-adgang med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurere adgang til Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
