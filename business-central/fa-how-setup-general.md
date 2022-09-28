---
title: Konfigurere generelle anlægsoplysninger
description: Inden du kan arbejde med anlægsaktiver, skal du konfigurere standardfinanskonti, bogføringsgrupper, fordelingsnøgler, kladdetyper og -navne samt klassekoder.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4f56c74eb3fd9bf80381171e304700c90caaee8b
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533666"
---
# <a name="set-up-general-fixed-assets-information"></a>Angive generelle oplysninger om anlægsaktiver

Før du kan administrere anlægsaktiver, skal du oprette standardfinanskonti, allokeringsnøgler, kladdetyper og -navne for bogføring og ompostering af anlægsaktiver, og du kan klassificere anlægsaktiver i arter, f.eks materielle og immaterielle.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Sådan defineres generelle standardværdier for anlæg

Du definere den generelle funktionsmåde eller anlægsaktivets funktion og oprette dokumentnummerserier på siden **Anlægsopsætning**.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsopsætning**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Sådan oprettes anlægsbogføringsgrupper

Bogføringsgrupper bruges til at definere grupper af anlægsaktiver. Disse bogføringsgruppers poster bogføres på samme finanskonti.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov på siden **Anlægsbogføringsgruppekort**.

    > [!NOTE]  
    >   For at sikre, at modkonti for forskellige anlægsbogføringer bliver indsat automatisk, når du vælger handlingen **Indsæt anlægsmodkonto** på kladdelinjer, skal du følge det næste trin baseret på opskrivningsbogføringer.
4. I oversigtspanelet **Modkonto** skal du vælge den finanskonto i feltet **Opskrivningsmodkonto**, som du vil bogføre modposter for ved opskrivning.

Yderligere oplysninger om brug af handlingen **Indsæt anlægsmodkonto** til anlægskassekladdelinjer finder du f.eks. under [Regulere anlægsaktiver](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Sådan defineres allokeringsnøgler for anlægsaktiver

Transaktioner kan allokeres på forskellige afdelinger eller projekter ud fra brugerdefinerede allokeringsnøgler. Du kan f.eks. definere en allokeringsnøgle til at allokere afskrivningerne på biler med 35 procent til administrationsafdelingen og 65 procent til salgsafdelingen. Du kan finde flere oplysninger i [Fordele omkostninger og indtægter](year-allocate-costs-income.md).

Allokeringsnøgler gælder for anlægsarter og ikke for de enkelte anlægsaktiver.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsbogføringsgrupper**, og vælg derefter det relaterede link.  
2. På siden **Anlægsbogføringsgrupper** skal du vælge handlingen **Allokeringer** og derefter vælge en bogføringstype.
3. På siden **Anlægsallokeringer** skal du udfylde felterne efter behov.
4. Gentag trin 2 og 3 for hver bogføringstype, du vil definere allokeringsnøgler for.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Sådan defineres anlægskladdetyper

En type er et foruddefineret format for en kladde. Typen indeholder oplysninger om sporingskoder, rapporter og nummerserier. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] opretter automatisk en anlægskladdetype, første gang du åbner siden **Anlægskladde**, men du kan definere flere kladdetyper.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskladdetyper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Sådan defineres anlægskladdenavne

Du kan angive flere kladdenavne, som er individuelle kladder for hver kladdetype. En medarbejder kan f.eks. have sin egen kladde, hvor medarbejderens initialer anvendes som kladdenavn. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskladdetyper**, og vælg derefter det relaterede link.  
2. Markér den relevante kladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Anlægskladdenavne** skal du udfylde felterne efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Sådan defineres anlægsomposteringskladdetyper

Du kan bruge dedikerede omposteringskladder, når du skal overføre, opdele eller kombinere anlægsaktiver. [!INCLUDE[prod_short](includes/prod_short.md)] opretter automatisk en anlægsomposteringskladdetype, første gang du åbner siden **Anlægsompost.kladde**, men du kan definere flere omposteringskladdetyper. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsompost.kladdetype**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Sådan defineres anlægsomposteringskladdenavne

Du kan angive flere kladdenavne, som er individuelle kladder for hver omposteringskladdetype. En medarbejder kan f.eks. have sin egen omposteringskladde, hvor medarbejderens initialer anvendes som omposteringskladdenavn. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsompost.kladdetype**, og vælg derefter det relaterede link.  
2. Markér den relevante kladdetype, og vælg derefter handlingen **Navne**.
3. På siden **Anlægsompost.kld.navne** skal du udfylde felterne efter behov.

## <a name="to-set-up-fixed-asset-class-codes"></a>Sådan angives anlægsartskoder

Anlægsartskoder kan bruges til at gruppere anlægsaktiver, f.eks. materielle og immaterielle aktiver.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsarter**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de arter, du vil oprette.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Sådan angives anlægsgruppekoder

Du kan bruge anlægsgruppekoder til at gruppere anlægsaktiver i kategorier, f.eks. bygninger, køretøjer, møbler eller maskiner.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsgrupper**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de arter, du vil oprette.

## <a name="to-set-up-fixed-asset-location-codes"></a>Sådan angives anlægslokationskoder

Du kan bruge anlægslokationskoder til at registrere anlæggets lokation, f.eks. salgsafdelingen, receptionen, administrationen, produktionen eller lagerstedet. Disse oplysninger er nyttige i forbindelse med forsikring og lagerstedet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægslokationer**, og vælg derefter det relaterede link.
2. Angiv koder og navne for de anlægslokationer, du vil oprette.

## <a name="to-register-opening-entries"></a>Sådan registreres åbningsposter

Hvis det er første gang, du bruger modulet Anlæg i [!INCLUDE[prod_short](includes/prod_short.md)], skal du konfigurere finansmodulet, før du konfigurerer anlægsaktiver. Hvordan du gør dette afhænger af, om anlægsaktiverne er integreret med regnskabet.  

 Følgende fremgangsmåde bruges, hvis anlægstransaktioner skal bogføres til finansposterne.  

1. Kontroller, at du er færdig med de grundlæggende opsætningsprocedurer for anlægsaktiver.  
2. Opret et anlægskort for hvert anlæg, der allerede findes.  
3. Oprette en anlægsafskrivningsprofil til hvert afskrivningsformål, (f.eks. skatteregnskaber eller årsregnskaber). Du skal selv definere betingelserne for hver afskrivningsprofil som f.eks. integration med finansbogholderiet.  

    Aktivér finansintegration ved hjælp af de næste trin. Først skal sikre dig, at finansintegration er deaktiveret for alle afskrivningsprofiler, og derefter skal du bogføre åbningsposter og endelig aktivere finansintegration.  
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningsprofiloversigt**, og vælg derefter det relaterede link.  
5. Vælg det relevante afskrivningsprofilkort, og vælg derefter handlingen **Rediger** for at åbne siden **Afskrivningsprofilkort**.
6. På oversiftspanelet **Integration** skal du sørge for, at alle felter er tomme, ved at fjerne alle markeringer. Hvis du har mere end én afskrivningsprofil, skal du deaktivere finansintegration for hver enkelt.  
7. Skriv følgende linjer for hvert aktiv i anlægskladden:
   * En linje med anskaffelsen.
   * En linje med den akkumulerede afskrivning i slutningen af det foregående regnskabsår.
   * En linje med den akkumulerede afskrivning fra begyndelsen af det aktuelle regnskabsår til den dato, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er indstillet til at starte afskrivningen.

    Hvis du har andre åbningsposter, kan du også angive dem nu, f.eks. nedskrivning og opskrivning.  
8. Når du har angivet og bogført kladdelinjerne for hvert anlæg, skal du aktivere finansintegration i afskrivningsprofilerne.

Hvis anlægsaktiverne ikke er integreret med finansposterne, skal du springe trin 6 og 8 over.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/set-up-fixed-assets-management/)

## <a name="see-also"></a>Se også

[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
