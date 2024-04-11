---
title: Fortryde en postering ved at bogføre en tilbageføringspost
description: 'Hvis du finder fejl i en bogføring i finanskladden, kan du bruge funktionen Tilbagefør transaktion til at fortryde bogføringen med et korrekt revisionsspor.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Tilbageføre kladdeposteringer og annullere modtagelser/leverancer

Tilbageførsel af kladdeposteringer er nyttig f.eks. til at rette fejl og til at fjerne en gammel periodiseringspost, før der angives en ny. En tilbageførselpost er den samme som originalposten, men har et modsat tegn i feltet **Beløb**. Tilbageførselsposten skal have samme bilagsnummer og posteringsdato som den oprindelige post. Når du tilbagefører en post, skal du oprette den korrekte post.

Du kan kun tilbageføre poster, der er bogført fra en finanskladdelinje. En post kan kun tilbageføres én gang.

Hvis du vil annullere bogføringen af en modtagelse eller leverance, før de bogføres som faktureret, kan du bruge funktionen **Fortryd** i det bogførte dokument. Du kan annullere antal af typen **Vare** og **Ressource**.

Hvis du har bogført et forkert negativt antal, som f.eks. en købsordre med det forkerte antal varer og bogført dem som modtaget, men ikke faktureret, kan du annullere bogføringen.

Hvis du har bogført et forkert positivt antal som f.eks. en salgsleverance eller købsreturvare med det forkerte antal varer og bogført dem som leveret, men ikke faktureret, kan du annullere bogføringen.

## Sådan tilbageføres kladdepost på en finanspost

Du kan tilbageføre poster fra alle **Poster**-sider: Følgende procedure er baseret på siden **Finansposter**.

> [!NOTE]
> Din bogføring skal stamme fra en kladdepost.
>
> Du kan heller ikke tilbageføre poster, der er bogført med oplysninger fra et projekt, eller som har realiserede gevinster og tab inden for samme transaktion.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Finansposter** , og vælg derefter det relaterede link.
2. Marker den post, du vil tilbageføre, og vælg derefter handlingen **Tilbagefør transaktion**.
3. Vælg handlingen **Tilbagefør** på siden **Tilbagefør transaktionsposter**.
4. Vælg **Ja** for at bekræfte tilbageførslen.

## Sådan bogføres en negativ post  

Brug feltet **Rettelse** til at bogføre en negativ debet i stedet for kredit eller til at bogføre en negativ kredit i stedet for en debet på en konto. Feltet er som standard tilgængeligt i alle kladder. Felterne **Debetbeløb** og **Kreditbeløb** indeholdet både den oprindelige post og den rettede post. Disse felter har ingen indflydelse på kontosaldoen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Finanskladder**, og vælg derefter det relaterede link  
2. Vælg det krævede kladdenavn i feltet **Kladdenavn**.  
3. Angiv oplysningerne i de relevante felter.  
4. I den kladdelinje, som du vil aktivere for negative poster, skal du markere afkrydsningsfeltet **Rettelse**.  
5. Hvis du vil postere kladden, skal du vælge handlingen **Bogfør** og derefter vælge knappen **Ja**.

## Sådan fortrydes et bogført antal på en bogført købsmodtagelse  

Følgende trin beskriver, hvordan du kan fortryde en bogført modtagelse af vare eller ressourcer. Fremgangsmåden er tilsvarende for bogførte leverancer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte kvitteringer** i feltet Søg, og vælg derefter det relaterede link.  
2. Åbn den bogført modtagelse, du vil fortryde.  
3. Vælg den eller de linjer, der skal fortrydes.  
4. Vælg handlingen **Annuller modtagelse**.

Der indsættes en korrektionslinje under den valgte modtagelseslinje. Hvis mængden blev modtaget i en lagermodtagelse, indsættes der en korrektionslinje i den bogførte lagermodtagelse.  

Felterne **Modtaget (antal)** og **Modt. antal (ufakt.)** på den relaterede købsordre , der er angivet til nul.

## Sådan fortryder du og derefter annullerer et bogført antal på en bogført returvareleverance

Følgende trin beskriver, hvordan du kan:

* Annullere en bogført returvareleverance for varer eller ressourcer.
* Bogføre et returkøb igen med et nyt antal.

Fremgangsmåden er tilsvarende for bogførte returvaremodtagelser.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte kvitteringer**, og vælg derefter det relaterede link.  
2. Åbne den bogførte returvare, der skal fortrydes.
3. Vælg den eller de linjer, der skal fortrydes.  

4. Vælg handlingen **Annuller returvareleverance**.  

    En rettelseslinje indsættes i det bogførte dokument, og felterne **Antal sendt retur** og **Afs. ret.vare - ikke fakt.** på returvareordren nulstilles.  

    Gå nu tilbage til købsreturvareordren for at annullere Fortryd bogføring.  

5. Notér tallet i feltet **Returvareordrenr.** på siden **Bogført returvareleverance** .  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsreturvareordrer**, og vælg derefter det relaterede link.  
7. Åbn den pågældende returordre, og vælg derefter handlingen **Genåbn**.  
8. Ret antallet i feltet **Antal**, og bogfør købsreturvareordren igen.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## Se også

[Fortryde bogføring af montage](assembly-how-to-undo-assembly-posting.md)  
[Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]