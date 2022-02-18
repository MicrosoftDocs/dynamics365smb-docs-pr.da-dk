---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: acde432acabc2d3e73658b0e916d6e4830ccaf52
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104067"
---
I følgende tabel beskrives nogle af nøglerapporterne i anlægsrapporter.

| Report | Objekt-id | Beskrivlse |
|--|--|--|
| **Anlægsoversigt** | 5601 | Viser oversigten over anlægsaktiverne og deres opsætningsoplysninger for en bestemt afskrivningsprofil. |
| **Anlæg - anskaffelsesoversigt** | 5608 | Vis alle aktiver, der er erhvervet inden for et bestemt datointerval. Du kan også inkludere anlægsaktiver, der er oprettet, men som endnu ikke er hentet. |
| **Anlægsposter** | 5604 | Viser anlægsposterne for anlægsaktiverne. |
| **Anlæg - analyse** | 5600 | En analyserapport, hvor du kan angive to datokolonner og tre datakolonner, der skal vises i rapporten. Hvis du f. eks. vil generere en rapport, der skal bruges til at afstemme med finansbogholderiet, skal du tilføje kolonner for anskaffelsespris på slutdato, afskrivninger til slutdato og bogført værdi på slutdato. En checkrapport kunne have anskaffelser/bevægelser, nedskrivnings-eller bevægelses ændringer samt opskrivning/bevægelse, så alle ændringer af anlægsaktivet kan kontrolleres om nødvendigt. Hvis du markerer feltet **budgetrapport** og angiver en slutdato i fremtiden, beregnes den fremtidige afskrivning, og der kan afregnes estimater ved fremtidige afskrivninger og bogførte værdier, hvis du har markeret disse felter som rapportkolonner. |
| **Anlæg - forventet værdi** | 5607 | Viser de forventede afskrivningsbeløb og den bogførte værdi for en fremtidig periode for anlægsaktiver. Rapporten er praktisk, hvis du bruger forskellige afskrivningsmetoder til dine anlæg, og du f. eks. vil beregne afskrivningen næste år. Brug rapporten til at oprette budgetbeløb for afskrivningen ved at vælge et budget og feltet **Kopier til finansbudget**. |
| **Anlæg - bogført værdi 01** | 5605 | Viser detaljerede oplysninger om anskaffelsesbeløb, afskrivninger og bogførte værdier for både enkelte anlægsaktiver og grupper af anlægsaktiver. For hver af de tre beløbstyper beregnes beløbene ved begyndelsen og ved slutningen af den valgte periode samt for selve perioden. Hvis du vælger feltet **budgetrapport**, vil rapporten beregne den forventede afskrivning for perioden. Angiv en *gruppetype*, hvis rapporten skal gruppere anlægsaktiverne og udskrive gruppetotaler. Hvis du f.eks. har oprettet seks anlægsarter, kan du vælge indstillingen *Anlægsart* og få udskrevet gruppetotaler for hver af de seks anlægsartskoder.|
| **Anlæg - bogført værdi 02** | 5606 |Viser opdelingen af anlægs bogført værdi med ændringer i anskaffelse, afskrivning og opskrivning inden for perioden med en yderligere fordeling efter tillæg og salg i perioden. Du kan bruge denne rapport til at beskrive ændringerne i anlægsaktiver for en bestemt periode, når der forekommer mange forskellige ændringer på tværs af anlægsaktivets gruppering. Hvis du vælger feltet **budgetrapport**, vil rapporten beregne den forventede afskrivning for perioden. Angiv en *gruppetype*, hvis rapporten skal gruppere anlægsaktiverne og udskrive gruppetotaler. Hvis du f.eks. har oprettet seks anlægsarter, kan du vælge indstillingen *Anlægsart* og få udskrevet gruppetotaler for hver af de seks anlægsartskoder. |
| **Anlæg - finansanalyse**| 5610 |Viser en analyse af anlægsaktiverne med oplysninger om både enkelte anlægsaktiver og/eller grupper af anlægsaktiver. I oversigtspanelet Anlæg kan du indsætte filtre, hvis rapporten skal afgrænses til kun at omfatte bestemte anlægsaktiver. I oversigtspanelet Indstillinger kan du skræddersy rapporten, så den passer til dine specifikke behov. Rapporten minder om **anlægs analyse**-rapporten, men især for at afstemme med finansmodulet og specielt til validering af salgsposterne. Rapporten forudsætter, at du kender de finanskonti, der er angivet i bogføringsopsætningen. |
| **Anlægsjournal** |5603  |Viser de bogførte anlægsposter, der er sorteret og inddelt efter journalnummer. Du kan indsætte et filter for at angive, hvilke journalers poster, du vil have vist. Det er vigtigt, at du indsætter et filter; ellers vil rapporten indeholde en uoverskuelig mængde oplysninger. |

