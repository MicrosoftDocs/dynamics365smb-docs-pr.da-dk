---
title: Sådan registrerer du bæredygtighedsposter
description: Sådan kan du registrere drivhusgas (GHG)-udledninger.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="record-sustainability-entries"></a>Sådan registrerer du bæredygtighedsposter

I øjeblikket er den eneste måde at registrere drivhusgasemissioner til **Finansposter for bæredygtighed** på at bruge **Bæredygtighedskladder**.   

## <a name="sustainability-journals"></a>Bæredygtighedskladde

**Bæredygtighedskladder** er designet til at spore og registrere bæredygtighedsrelaterede aktiviteter ved hjælp af den samme brugeroplevelse som andre kladder i Business Central. Inden for kladden har brugerne mulighed for at indtaste emissioner manuelt, hvis de har de nødvendige oplysninger. Alternativt, hvis de mangler disse data, kan de bruge indbyggede formler til nøjagtigt at beregne emissioner baseret på specifikke kendte parametre svarende til forskellige typer kilder og konti. 

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til **Finansposter for bæredygtighed** på individuelle **Bæredygtighedskonti**, hvor de ikke kan ændres. Du kan dog bogføre tilbageførsels- eller rettelsesposter.  

### <a name="use-journal-templates-and-batches"></a>Bruge kladdeskabeloner og -batches

Der er som standard to **bæredygtighedskladdetyper**, standarden og den tilbagevendende. For hver kladdetype kan du angive din egen private kladde som kladdenavn. For at gøre dette skal du vælge handlingen **Batches** på siden **Skabeloner til bæredygtighedskladde** og oprette den nye **Bæredygtighedskladdenavn** på den nye side. Du kan f.eks. definere din egen kladde for hvert emissionsomfang ved hjælp af indstillingen **Udledningsomfang**, hvor du kan vælge mellem tre eksisterende omfang. Du kan også tilføje eller ændre **kildesporet** og **årsagskoden** for hvert af navnene. 

>[!TIP]
>Du kan have en kladdebatch for hver af emissionstyperne, hvis du har mange linjer, da det kan reducere risikoen for fejl, men du kan også bruge den fælles batch til alle typer emissioner.   

### <a name="validate-sustainability-journals"></a>Validering af bæredygtighedskladder

Du kan aktivere en baggrundskontrol på siden **Opsætning af bæredygtighed**, som medvirker til at forhindre forsinkelser ved bogføring. Kontrollen giver dig besked, når der opstår fejl i **bæredygtighedskladden**, og den vil forhindre, at du arbejder med at bogføre kladden.  

Når du aktiverer valideringen, viser faktaboksen **Kladdekontrol** problemer på den aktuelle linje og på hele kørslen. Validering sker, når du indlæser et kladdenavn, og når du vælger en anden kladdelinje. Feltet **Fejl i alt** i faktaboksen viser det samlede antal problemer, som [!INCLUDE [prod_short](includes/prod_short.md)] har fundet, og du kan vælge den for at åbne en oversigt over problemerne. 

### <a name="work-with-sustainability-journals"></a>Arbejde med bæredygtighedskladder

Følg trinene for at begynde at arbejde med **bæredygtighedskladder**:   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bæredygtighedskladde**, og vælg derefter det relaterede link. 
2. På siden **Bæredygtighedskladde** kan du indtaste lige så mange linjer, som du planlægger at bogføre med samme batch.  
3. Som **dokumenttype** kan du holde tom mulighed eller vælge at bruge **Faktura** eller **Kreditnota**.  
4. I feltet **Kontonr.** kan du vælge kun **bæredygtighedskonti** med valgt felt **Direkte bogføring**,  **Bogføring**  som **Regnskabstype** og ikke-spærret konto. Konti skal også have konfigureret med kategori og underkategori.  

>[!NOTE]
>Hvis du bruger det batch, hvor emissionsomfanget er konfigureret, skal **Udledningsomfanget** i **Bæredygtighedskontoen** svare til **Udledningsomfanget** i anvendte batch.  

5. Du har to muligheder: Enten bogføre beløbene manuelt eller bruge formler.   

    1. Hvis du har nøjagtige oplysninger om emissionen, du vil bogføre den (dvs. hvis du har den på den modtagne faktura), skal du markere feltet **Manuel indtastning** for at angive, at mængderne skal indtastes manuelt. I dette tilfælde kan du ikke udfylde dine data i felterne **Brændstof/elektricitet**, **Afstand**, **Brugerdefineret antal**, **Installationsmultiplikator** og **Tidsfaktor**, da de ikke kan redigeres for dette valg. Men felterne **Udledning af CO2**, **Udledning af CH4** og **Udledning af N2O** kan redigeres, og du kan udfylde dine data direkte der. 
    2. Hvis du ikke kender din emission nøjagtigt, skal du beregne den, og du behøver ikke at have valgt feltet **Manuelt input**, og i dette tilfælde kan felterne **Udledning af CO2**, **Udledning af CH4** og **Udledning af N2O** ikke redigeres, men du kan indtaste dine beregningsoplysninger baseret på den formel, du bruger. Du kan finde mere om de anvendte formler, der er defineret i kategorien **Bæredygtighedskonto**, her i [Diagram over bæredygtighedskonti og hovedbøger](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Vælg handlingen **Bogfør** for at bogføre kladden. Når der bogføres i en **Bæredygtighedskladde**, genereres poster på **Bæredygtighedsposten**. 

Hvis din formel er baseret på indstillingen **Beregn fra finans** i kategorien **Bæredygtighedskonto**, skal du bruge handlingen **Indsaml beløb fra finansposter** , før du bogfører kladden, for at beregne udledninger baseret på denne datakilde. Hvis du har foretaget nogle ændringer i emissionsfaktorerne, efter at du har udfyldt kladdelinjerne, skal du desuden vælge handlingen **Genberegn** for at få den korrekte mængde i kladden.  

### <a name="recurring-journals"></a>Gentagelseskladder

En gentagelseskladde er en **Bæredygtighedskladde** med særlige felter til styring af transaktioner, som bogføres ofte med få eller ingen ændringer. For eksempel bæredygtighedstransaktioner som el, varme eller andre lignende transaktioner. Du kan bruge gentagelseskladder til at bogføre faste og variable beløb. Med gentagelseskladder kan du oprette de poster, der bogføres regelmæssigt, én gang. F.eks. bliver de konti, dimensioner og dimensionsværdier og så videre, du indtaster i felterne, i kladden efter bogføringen. Hvis det er nødvendigt at foretage ændringer, kan du gøre det, hver gang du bogfører. 

Feltet **Gentagelsesmetode** er vigtigt. Dette felt bestemmer, hvordan beløbet på kladdelinjen bliver behandlet efter bogføringen. Hvis du f.eks. bogfører det samme beløb, hver gang du bogfører linjen, kan du lade beløbet stå, og i så fald skal du bruge **F Fast** som en mulighed. Eller du kan vælge at lade det slette, fordi konti og tekst i linjen kan genbruges ved hver bogføring, men beløbet hver gang varierer, og i dette tilfælde vil du vælge indstillingen **V Variabel**. 

Du skal også konfigurere feltet **Gentagelsesinterval**, da dette datoformel angiver, hvor ofte posten på kladdelinjen skal bogføres, og det skal udfyldes. Flere oplysninger i [Bruge datoformler](ui-enter-date-ranges.md#use-date-formulas).  

Feltet **Udløbsdato** bestemmer, på hvilken dato kladdelinjen bliver bogført for sidste gang. Linjen bogføres ikke efter denne dato. Fordelen ved at bruge feltet **Udløbsdato** er, at linjen ikke slettes fra kladden med det samme. Du kan angive en senere dato, så du kan bruge linjen i fremtiden. Hvis feltet er tomt, bogføres linjen, hver gang du bogfører, indtil den slettes fra kladden.  

## <a name="see-also"></a>Se også
[Finance](finance.md)    
[Oversigt over styring af bæredygtighed](finance-manage-sustainability.md)   
[Opsætning af bæredygtighed](finance-sustainability-setup.md)   
[Diagram over bæredygtighedskonti og finans](finance-sustainability-accounts-ledger.md)   
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
