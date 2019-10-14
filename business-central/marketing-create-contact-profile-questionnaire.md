---
title: Bruge profiler til at klassificere kontakter
description: Definere profilspørgeskemaer for at klassificere dine forretningskontakter
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2019
ms.openlocfilehash: 22471a6e0281f6f7aa4e9c9bbf0b2d9c5a0fd710
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309288"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Bruge profilspørgeskemaer til at klassificere forretningskontakter
Du kan definere profilspørgeskemaer, du vil bruge til indtastning af oplysninger om kontaktprofiler. Du kan i det enkelte spørgeskema definere forskellige spørgsmål, du vil stille dine kontaktpersoner.  

Du kan også køre spørgeskemaet for at besvare nogle af spørgsmålene automatisk ud fra kontakt-, debitor- eller kreditordata.  

## <a name="to-add-a-profile-questionnaire"></a>Sådan tilføjes et profilspørgeskema
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af spørgeskema**, og vælg derefter det relaterede link.  
2.  Under fanen **Startside** i gruppen **Ny** skal du vælge **Ny**.  
3.  Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Sådan føjes spørgsmål til et profilspørgeskema
1.  Vælg det relevante profilspørgeskema, og gå til fanen **Start**, og vælg **Rediger opsætning af spørgeskema** i gruppen **Proces**.  
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

Hvis du har angivet automatisk besvarede profilspørgsmål, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk de korrekte svar for kontakterne, når du tildeler en kontakt et profilspørgeskema med de pågældende spørgsmål.  

## <a name="example"></a>Eksempel
Du kan klassificere kontakter efter deres købsbeløb.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Svar</strong></th>
<th><strong>Gælder for</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>Kontakter, der har købt for mindst RV 500.000</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>Kontakter, der har købt for mellem RV 100.000 og 499.999.</p></td>
</tr>
<tr class="odd">
<td><p>U</p></td>
<td><p>Kontakter, der har købt for højst RV 99.999</p></td>
</tr>
</tbody>
</table>

Det gør du ved at udfylde siden **Opsætn. af profilspørgeskema** på følgende måde:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Type</strong></th>
<th><strong>Beskrivelse</strong></th>
<th><strong>Automatisk klassificering</strong></th>
<th><strong>Fra værdi</strong></th>
<th><strong>Til værdi</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Spørgsmål</p></td>
<td><p>ABC-klassificering</p></td>
<td><p>Indsæt markering ved at klikke</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>T</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Svar</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>U</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Udfyld derefter siden **Oplysninger om profilspørgsmål** på følgende måde:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Felt</strong></th>
<th><strong>Værdi</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Debitorklassifikationsfelt</strong></td>
<td><emphasis>Salg (RV)</emphasis></td>
</tr>
<tr>
<td><strong>Klassificeringsmetode</strong></td>
<td><emphasis>Defineret værdi</emphasis></td>
</tr>
</tbody>
</table>

Når du tildeler et profilspørgeskema med disse spørgsmål til en kontakt, udfyldes de relevante svar for kontakten automatisk på profillinjerne på kontaktkortet.

## <a name="see-also"></a>Se også
[Oprettelse af kontakter](marketing-create-contact-companies.md)  
