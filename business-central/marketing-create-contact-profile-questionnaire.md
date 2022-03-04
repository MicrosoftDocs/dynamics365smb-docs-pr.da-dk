---
title: Bruge profiler til at klassificere kontakter
description: Flere oplysninger om, hvordan du definerer profilspørgeskemaer for at hjælpe med at klassificere forretningskontaktpersonernes profiler.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 42ef7c92d138d717f10eb98a7fa9208eaf73ef54
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140836"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Bruge profilspørgeskemaer til at klassificere forretningskontakter
Du kan definere profilspørgeskemaer, du vil bruge til indtastning af oplysninger om kontaktprofiler. Du kan i det enkelte spørgeskema definere forskellige spørgsmål, du vil stille dine kontaktpersoner.  

Du kan også køre spørgeskemaet for at besvare nogle af spørgsmålene automatisk ud fra kontakt-, debitor- eller kreditordata.  

## <a name="to-add-a-profile-questionnaire"></a>Sådan tilføjes et profilspørgeskema
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **opsætning af spørgeskema**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Sådan føjes spørgsmål til et profilspørgeskema
1.  Vælg det relevante profilspørgeskema, og vælg handlingen **Rediger opsætning af spørgeskema**.  
2.  I den første tomme linje skal du i feltet **Type** vælge **Spørgsmål** og skrive dit spørgsmål i feltet **Beskrivelse**. Udfyld de andre felter på linjen.  
3.  Vælg **Svar** i den næste tomme linje i feltet **Type**, og skriv svaret i feltet **Beskrivelse**.  
4.  Vælg prioriteten i feltet **Prioritet**. I felterne **Fra-værdi** og **Til-værdi** defineres et interval. Kontakter, der modtager point inden for det angivne interval, får svaret.  

Gentag disse trin for at indtaste alle spørgsmål og svar i profilspørgeskemaet.

Når du har oprettet et spørgeskema, skal du oprette kontaktpersonvurderinger til at klassificere dine kontaktpersoner. Du kan også oprette spørgsmål, der klassificeres automatisk baseret på oplysningerne på kontaktkortet.  

> [!NOTE]
> Hvis du angiver et spørgsmål, som skal besvares automatisk, skal du vælge <STRONG>Linje</STRONG> og derefter vælge <STRONG>Oplysn. om spørgsmål</STRONG> for at angive de kriterier, som skal anvendes ved den automatiske besvarelse.

## <a name="the-automatic-classification-of-contacts"></a>Den automatiske klassificering af kontaktpersoner
Du kan automatisk klassificere kontakter efter debitor-, kreditor- og kontaktoplysninger ved at definere automatisk besvarede profilspørgsmål på siden **Opsætn. af profilspørgeskema**.  

> [!NOTE]
> Det er kun kontakter, der er registrerede som debitorer, som kan få tildelt en klassificering ud fra debitordata, og kun kontakter registreret som kreditorer kan tildeles en klassificering ud fra kreditordata. Klassificeringen opdateres ikke automatisk. Det kan derfor være nødvendigt at opdatere profilspørgeskemaerne, hvis du har opdateret de debitor-, kreditor- eller kontaktdata, som de er baseret på.  

Hvis du har angivet automatisk besvarede profilspørgsmål, udfylder [!INCLUDE[prod_short](includes/prod_short.md)] automatisk de korrekte svar for kontakterne, når du tildeler en kontakt et profilspørgeskema med de pågældende spørgsmål.  

## <a name="example"></a>Eksempel

Du kan klassificere kontakter efter deres købsbeløb.

|Svar|Gælder for|
|--- |--- |
|A|Kontakter, der har købt for mindst RV 500.000|
|B|Kontakter, der har købt for mellem RV 100.000 og 499.999.|
|U|Kontakter, der har købt for højst RV 99.999|

Det gør du ved at udfylde siden **Opsætn. af profilspørgeskema** på følgende måde:

| Type     | Beskrivlse        | Automatisk klassificering     | Fra værdi | Til værdi |
|----------|--------------------|------------------------------|------------|----------|
| Spørgsmål | ABC-klassificering | Indsæt markering ved at klikke |            |          |
| Svar   | T                  |                              | 500,000    |          |
| Svar   | B                  |                              | 100,000    | 499,999  |
| Svar   | U                  |                              |            | 99,999   |

Udfyld derefter siden **Oplysninger om profilspørgsmål** på følgende måde:

| Felt                         | Værdi         |
|-------------------------------|---------------|
| Debitorklassifikationsfelt | Salg (RV)   |
| Klassificeringsmetode         | Defineret værdi |

Når du tildeler et profilspørgeskema med disse spørgsmål til en kontakt, udfyldes de relevante svar for kontakten automatisk på profillinjerne på kontaktkortet.

## <a name="see-also"></a>Se også

[Oprettelse af kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]