---
title: Oversigt over opgaver til fordeling af omkostninger og indtægter
description: 'Beskriver de opgaver, du skal udføre for at allokere en post i en gentagen finanskladde til flere forskellige konti, når du bogfører kladden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 08/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="allocate-recurring-costs-and-income"></a>Fordele gentagende omkostninger og indtægter

Du kan allokere en post i en tilbagevendende finanskladde til flere forskellige konti, når du bogfører kladden. Du kan få mere at vide om gentagelseskladder ved at gå til [Arbejde med gentagelseskladder](ui-work-general-journals.md#work-with-recurring-journals). 

Allokeringen kan foretages på tre forskellige måder:

* Antal
* Procent (%)
* Beløb

Allokeringsfunktionen kan bruges sammen med finansgentagelseskladder og i anlægskladder.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

I følgende procedurer beskrives, hvordan du forbereder at allokere omkostninger i en finansgentagelseskladde ved at definere fordelingsnøgler. Når der er defineret fordelingsnøgler, skal du udfylde og bogføre kladden ligesom alle andre finansgentagelseskladder. Du kan finde flere oplysninger i [Arbejde med finanskladder](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Sådan konfigureres fordelingsnøgler

Du kan allokere en post i en finansgentagelseskladde til flere forskellige konti, når du bogfører kladden. Allokeringen kan foretages efter antal, procent eller beløb.  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Finansgentagelseskladder**, og vælg derefter den relaterede sammenkæde.
2. Vælg feltet **Kladdenavn** for at åbne siden **Finanskladdenavne**.
3. Du kan ændre fordelinger for et eksisterende navn på listen eller oprette et nyt navn med fordelinger.
   * Du kan oprette en ny kladde ved at vælge handlingen **Ny** og gå til næste trin.
   * Vælg kladden og gå til trin 7, hvis du vil ændre fordelingerne af en eksisterende kladde.    
4. Angiv navnet på en ny kladde i feltet **Navn**, f.eks. Rengøring. Angiv en beskrivelse i feltet **Beskrivelse**, f.eks. Kladde til rengøringsudgifter.
5. Luk siden, når du er færdig. Der åbnes en ny tom gentagelseskladde.
6. Udfyld felterne på linjen.
7. Vælg handlingen **Fordelinger**.
8. Tilføj en linje for hver fordeling. Du skal udfylde et af følgende felter: **Allokeringspct.**, **Andel i antal** eller **Beløb**. Du skal også udfylde kontonummeret **.**, og hvis du allokerer transaktionen mellem globale dimensioner, global dimension felter.
9. Hvis du angiver en procent på en linje, beregnes beløbet i feltet **Beløb** automatisk. Disse beløb har det modsatte tegn af tegnet fra det totale beløb i feltet **Beløb** i gentagelseskladden.
10. Når du har angivet linjerne med fordelinger, skal du vælge **OK** for at gå tilbage til siden **Finansgentagelseskladde**. Feltet **Fordelt beløb (RV)** udfyldes og svarer til feltet **Beløb**.
11. Bogfør journalen.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Sådan ændres en fordelingsnøgle, der allerede er oprettet

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , angiv **Finansgentagelseskladder**, og vælg derefter den relaterede sammenkæde.
2. Vælg kladden **med allokeringen på siden Finansgentagelseskladder** .
3. Vælg linjen med fordelingen og vælg derefter handlingen **Fordelinger**.
4. Rediger de relevante felter, og vælg derefter knappen **OK**.

## <a name="see-also"></a>Se også

[Ultimoår og -perioder](year-close-years-periods.md)    
[Arbejde med finanskladder](ui-work-general-journals.md)    
[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
