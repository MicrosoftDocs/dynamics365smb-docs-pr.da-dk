---
title: Indsaml debitoropsætningsværdier
description: Konfigurationsspørgeskemaet er med til at reducere implementeringen ved at strømline opsætningen af nye virksomheder og tilbyde kunder en Excel-eller XML-fil.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: d26fb334462ad52a14058e8d5f6b9f86088ad3d7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145966"
---
# <a name="gather-customer-setup-values"></a>Indsaml debitoropsætningsværdier
Du kan bruge konfigurationsspørgeskemaet for at reducere arbejdsbelastningen ved implementering ved at strømline opgave til at oprette en ny virksomhed. Du kan generere konfigurationsspørgeskemaet i [!INCLUDE[prod_short](includes/prod_short.md)] og derefter give det til kunden som en Excel- eller XML-fil.  

Du kan ændre alle standardværdier i et spørgeskema, så de bedre opfylder kundens behov.  

> [!TIP]  
>  Du kan finde flere oplysninger om definition af konfigurationsværdier i felterne til forsyningsplanlægning i [Oprette bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md).  

Når kunden har udfyldt spørgeskemaet, importerer du filen til kundens nye [!INCLUDE[prod_short](includes/prod_short.md)]-virksomhed. Du og din kunde validerer svarene til spørgeskemaet, før du anvender dem i regnskabet.

## <a name="to-create-a-configuration-questionnaire"></a>Sådan oprettes et konfigurationsspørgeskema
Du kan bruge et spørgeskema til at hjælpe dig med at afgøre omfanget af og behovet for konfiguration. Du kan oprette et nyt spørgeskema eller redigere et eksisterende spørgeskema ved at tilføje nye spørgsmål eller spørgeområder.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company information. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Du kan kun oprette spørgeskemaer til tabeller af opsætningstypen. Du kan f.eks. bruge værktøjet til at angive oplysninger på følgende sider:  

-   Virksomhedsoplysninger  
-   Anlægsopsætning  
-   Opsætning af Finans  
-   Opsætning af Lager  
-   Montagekonfiguration
-   Produktionsopsætning  
-   Købsopsætning  
-   Marketingopsætning  
-   Serviceopsætning  
-   Salgsopsætning  
-   Logistikopsætning  

> [!NOTE]  
>  Hvis du vil se en komplet liste over opsætningstabeller, skal du vælge den ![lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Konfiguration**, og vælg derefter det relaterede link. Til at afgøre omfanget af overflytning af data i poster, skal du bruge funktionerne til overflytning. Du kan finde flere oplysninger i [Overflytning af debitordata](admin-migrate-customer-data.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Spørgeskema til konfiguration**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.   
3. Gå til siden **Konfigurationsspørgeskema**, og angiv følgende i feltet **kode**... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[prod_short](includes/prod_short.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Vælg handlingen **Spørgsmålsområder**. Siden **Spørgsmålsområder** åbnes.  
4. Vælg handlingen **Ny**. Siden **Konfig.spørgsmålsområde** åbnes.  
5. I feltet **Tabel-id** skal du vælge id'et på den tabel, du vil indsamle oplysninger om. Feltet **Tabelnavn** udfyldes automatisk.  
6. Vælg handlingen **Opdater spørgsmål**. Hvert felt i tabellen føjes til spørgeskemaet med et spørgsmålstegn efter dets etiket.

Du kan omformulere etiketten for at gøre det klart, hvordan spørgsmålet skal besvares. Hvis et felt f.eks. kaldes "Navn", kan du redigere det til at angive "Hvad er navnet på \<data being collected\>". Du kan også vejlede andre i feltet **Reference**, inklusive en URL-adressen til en side, der indeholder yderligere oplysninger.  

Du kan også slette eventuelle spørgsmål, du ikke vil medtage i spørgeskemaet.  

> [!NOTE]  
>  Feltet **Svarindstilling** beskriver typen og formatet af de data i svaret, som er relevante. Feltet **Svar** indeholder oplysninger, der er angivet af brugeren.  
>   
>  Efter behov, kan du også definere standardsvar i feltet **Svar**. Disse værdier bruges som standard til brugerdefineret installation. Den person, der udfylder spørgeskemaet, kan dog redigere og opdatere svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Sådan udfyldes konfigurationsspørgeskemaet
Du kan bruge konfigurationsspørgeskemaet til at strukturere og dokumentere en detaljeret diskussion om kundens specifikke behov. Du også bruge det til at indsamle opsætningsdata fra kunden for at konfigurere de relevante [!INCLUDE[prod_short](includes/prod_short.md)]-opsætningstabeller, såsom regnskab, lager og kunder.  

> [!NOTE]  
>  Du kan også oprette dit eget konfigurationsspørgeskema, som opfylder dine behov.  

1. Åbn det ønskede regnskab, du vil udfylde spørgeskemaet for.
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Spørgeskema til konfiguration**, og vælg derefter det relaterede link.  
3. Vælg spørgeskemaet for virksomheden, og vælg derefter handlingen **Udlæs til Excel** og eventuelt handlingen **Udlæs til XML**.
4. Få kunden til at udfylde konfigurationsspørgeskemaet ved at angive svarene i Excel-projektmappen. Der er et regneark for hvert spørgsmålsområde i spørgeskemaet.   
5. Gem Excel-projektmappen som *XML-data*. Vælg handlingen **Indlæs fra XML**, og vælg .xml-filen med kundens svar.
6. Vælg handlingen **Spørgeområder** for at begynde processen med at validere og anvende svarene på konfigurationsspørgeskemaet.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Sådan udfyldes et spørgeskema fra konfigurationsregnearket  
Den følgende procedure er en alternativ måde til at få adgang til konfigurationsspørgeskemaer. Det forudsættes, at konfigurationspakken, som du har fået leveret, indeholder spørgeskemaer.  

1. Når du har importeret en konfigurationspakke, skal du åbne konfigurationsregnearket.  
2. For hver tabel, hvor der er et spørgsmålsområde, skal du vælge handlingen **Spørgsmål**. Spørgeskemasiden åbnes.  
3. Besvar spørgsmålene, og vælg derefter handlingen **Anvend svar**.  
4. Vælg knappen **OK** for at lukke spørgeskemaet.

## <a name="to-validate-the-configuration-questionnaire"></a>Sådan valideres konfigurationsspørgeskemaet
Det er vigtigt at validere konfigurationsspørgeskemaet, før du anvender det på [!INCLUDE[prod_short](includes/prod_short.md)]-formatet. Det er en måde at sikre, at dataformateringen bevaers under import fra Excel.  

En almindelig valideringsopgave er at kontrollere, at tekststrenge ikke er indsat i datofelter. Denne revisionsproces er nødvendig, fordi formatet for svaret i spørgeskemaet ikke valideres automatisk, når funktionen **Anvend svar** køres.  

> [!NOTE]  
>  Validering af konfigurationsspørgeskemaet er generelt en manuel proces. Der er dog kontrol for regionale formateringsuoverensstemmelser. Desuden vil du få fejl, hvis strukturen i din [!INCLUDE[prod_short](includes/prod_short.md)]-database ikke stemmer overens med strukturen i overflytningsdatabasen.  

1. På siden **Konfigurationsspørgeskema** skal du vælge det relevante spørgeskema og derefter vælge handlingen **Spørgsmålsområder**.  
2. Åbn det relevante spørgsmålsområde.  
3. For hvert spørgsmål skal du kontrollere, at værdien i feltet **Svar** svarer til det format, der er anført i feltet **Svarindstilling**. Kontrollér f.eks., at adressen på en virksomhed er i tekstformat.  
4. Hvis du finder fejl, kan du foretage fejlfinding og foretage rettelser i Excel ved at udlæse spørgeskemaet og derefter indlæse det igen. Du kan også rette fejl direkte i [!INCLUDE[prod_short](includes/prod_short.md)], efterhånden som du gennemgår svarene på siden **Konfig.spørgsmålsområde**.  
5. Gentag disse trin for hvert spørgsmålsområde.  

Når du har fuldført din validering, er dataene klar til at blive anvendt til databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Sådan anvendes svar fra konfigurationsspørgeskemaet
Når du har indlæst og valideret oplysninger fra et konfigurationsspørgeskema, kan du overføre eller anvende opsætningsdata til de tilsvarende tabeller i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Spørgeskema til konfiguration**, og vælg derefter det relaterede link. Siden **Konfig.spørgeskema** åbnes.  
2. Vælg et konfigurationsspørgeskema på listen, og vælg derefter handlingen **Rediger liste**.  
3. Du kan anvende svar på en af to måder.  

- Hvis du vil anvende hele spørgeskemaet, skal du vælge handlingen **Anvend svar**.  
- Hvis du vil anvende svar kun for et bestemt **Spørgsmålsområde**, skal du vælge handlingen **Spørgeområder**, vælge et **Spørgsmålsområde** på listen og derefter vælge handlingen **Anvend svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Sådan kontrollerer du, at svarene er blevet anvendt korrekt

1. Kontrollér opsætningssiderne for de forskellige funktionelle områder i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde siden ved at vælge ikonet ![Elpære, der åbner funktionen Fortæl mig 5](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") og angive navnet på opsætningssiden og derefter vælge det relaterede link.  
2. Kontrollér, at felterne er blevet udfyldt med de korrekte data fra de forskellige spørgsmålsområder i konfigurationsspørgeskemaet.  

Du har nu konfigureret opsætning med debitorens forretningsmæssige oplysninger og regler.

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]