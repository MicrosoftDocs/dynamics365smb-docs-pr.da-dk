---
title: Bruge profiler til at klassificere kontakter
description: 'Flere oplysninger om, hvordan du definerer profilspørgeskemaer for at hjælpe med at klassificere forretningskontaktpersonernes profiler.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: edupont
ms.date: 05/20/2022
---

# <a name="use-profile-questionnaires-to-classify-business-contacts" />Bruge profilspørgeskemaer til at klassificere forretningskontakter

Du kan vurdere et emne, så du kan identificere de ideelle emner, som din salgskampagne skal fokusere på. Du kan definere profilspørgeskemaer, du vil bruge til indtastning af oplysninger om kontaktprofiler. Du kan i det enkelte spørgeskema definere forskellige spørgsmål, du vil stille dine kontaktpersoner. På den måde kan du gruppere kontaktpersoner, så kampagnerne er mere sandsynlige for de rigtige personer på grundlag af de kriterier, du definerer med spørgeskemaerne.  

Med de rette spørgeskemaer kan du vurdere dine emner og gruppere dem i kategorier. Eksisterende spørgsmål og svar kan kombineres med nye spørgsmål og svar, som danner grundlag for din bedømmelse. Hvert svar i vurderingen får en pointværdi og afhængigt af det interval, du har defineret for kategorierne (*Fra værdi* og *Til værdi*), grupperer vurderingssystemet dine kontaktpersoner i de kategorier, du har defineret. F.eks. *ABC*-kunder, leverandører med *høj/lav loyalitet* eller *platin//guld/sølv*-kundeemner.  

Du kan også køre spørgeskemaet for at besvare nogle af spørgsmålene automatisk ud fra kontakt-, debitor- eller kreditordata.  

## <a name="to-add-a-profile-questionnaire" />Sådan tilføjes et profilspørgeskema

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **opsætning af spørgeskema**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire" />Sådan føjes spørgsmål til et profilspørgeskema

1. Vælg det relevante profilspørgeskema, og vælg handlingen **Rediger opsætning af spørgeskema**.  
2. I den første tomme linje skal du i feltet **Type** vælge **Spørgsmål** og skrive dit spørgsmål i feltet **Beskrivelse**. Udfyld de andre felter på linjen.  

    Du kan også vælge at føje oplysninger til spørgsmålet.

    1. Vælg linjen med spørgsmålet, Vælg derefter menuen **linje**, og vælg derefter **oplysninger om spørgsmål**.  

    2. Marker feltet **Automatisk kontaktklassificering** i oversigtspanelet **Klassificering** på siden **Oplysninger om profilspørgsmål**.  

    3. I feltet **Kontaktklassefelt** vælges indstillingen **Vurdering**.  

    4. Udfyld feltet **Min. besvarelsespct.**. Standardværdien er **0**.  

        Dette angiver procentdelen af de spørgsmål, der skal besvares, for at denne vurdering kan beregnes i systemet.

    5. Under fanen **Handlinger** i gruppen **Side** vælges **Svarpoint**. Angiv det antal point, du vil give hvert svar på siden **Svarpoint**.

        Hvis du vil have vist en oversigt over de point, du har givet hvert svar, skal du vælge handlingen **Svarpoint**.

    6. Hvis du vil køre en opdatering, skal du vende tilbage til siden **opsætning af profilspørgeskema**. På fanen **Handlinger** i gruppen **Funktioner** vælges **Opdater klassifikation**.

    På siden **Opsætn. af profilspørgeskema** vises det antal kontaktpersoner, der opfylder dette kriterium, i feltet **Antal kontakter** samt på **kontaktkortet** for hver kontaktperson.

3. Vælg **Svar** i den næste tomme linje i feltet **Type**, og skriv svaret i feltet **Beskrivelse**.  
4. Vælg prioriteten i feltet **Prioritet**. I felterne **Fra-værdi** og **Til-værdi** defineres et interval. Kontakter, der modtager point inden for det angivne interval, får svaret.  

Gentag disse trin for at indtaste alle spørgsmål og svar i profilspørgeskemaet.

Når du har oprettet et spørgeskema, kan du bruge det til at vurdere og klassificere dine kontaktpersoner. Du kan også oprette spørgsmål, der klassificeres automatisk baseret på oplysningerne på kontaktkortet.  

> [!NOTE]
> Hvis du angiver et spørgsmål, som skal besvares automatisk, skal du vælge **Linje** og derefter vælge **Oplysn. om spørgsmål** for at angive de kriterier, som skal anvendes ved den automatiske besvarelse.

## <a name="apply-questionnaires-to-contacts" />Anvende spørgeskemaer på kontakter

Du kan anvende dine spørgeskemaer til kontakter manuelt. Åbn blot det relevante kontaktkort, og vælg handlingen **Profil**. Derefter kan du begynde at bruge kategorierne i kampagnerne, når du har anvendt de spørgeskemaer, du vil udligne.  

## <a name="the-automatic-classification-of-contacts" />Den automatiske klassificering af kontaktpersoner

Du kan automatisk klassificere kontakter efter debitor-, kreditor- og kontaktoplysninger ved at definere automatisk besvarede profilspørgsmål på siden **Opsætn. af profilspørgeskema**.  

> [!NOTE]
> Det er kun kontakter, der er registrerede som debitorer, som kan få tildelt en klassificering ud fra debitordata, og kun kontakter registreret som kreditorer kan tildeles en klassificering ud fra kreditordata. Klassificeringen opdateres ikke automatisk. Det kan derfor være nødvendigt at opdatere profilspørgeskemaerne, hvis du har opdateret de debitor-, kreditor- eller kontaktdata, som de er baseret på.  

Hvis du har angivet automatisk besvarede profilspørgsmål, udfylder [!INCLUDE[prod_short](includes/prod_short.md)] automatisk de korrekte svar for kontakterne, når du tildeler en kontakt et profilspørgeskema med de pågældende spørgsmål.  

## <a name="example" />Eksempel

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

## <a name="see-also" />Se også

[Oprettelse af kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
