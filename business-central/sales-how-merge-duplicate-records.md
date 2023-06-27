---
title: Flette dobbeltregistreringer på kunder og leverandører
description: 'Beskriver, hvordan du kan konsolidere oplysninger om debitorer eller kreditorer, når du har dubletter af poster.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="merge-duplicate-records"></a>Flet dobbeltregistrerede records

Efterhånden som brugere opretter ny kunde, leverandør eller kontaktkort igennem længere tid, eller der oprettes nye records automatisk under migration, kan en kunde, leverandør eller kontakt være repræsenteret i systemet med mere end en record. I dette tilfælde kan du benytte siden **Flet dobbeltregistrering** fra record-kortet, som du ønsker at beholde. Siden giver dig et overblik over dobbeltregistrerede værdier og leverer funktioner til at udvælge, hvilke værdier, der skal beholdes og slettes henholdsvis, når du fletter to records til en.

> [!NOTE]
> Kun brugere med rettighedssættet FLET DOBBELTREGISTRERINGER kan benytte denne funktionalitet.

> [!TIP]
> Siden **Flet dobbeltregistreringer** viser alle felter, hvor værdierne er forskellige fra de to records, som sammenlignes. En dobbeltregistrering er således indikeret ved, at siden viser meget få felter. Hvis siden derimod viser mange felter, er den forventede record sandsynligvis ikke en dobbeltregistrering.

Den følgende procedure er baseret på et kundekort. Trinnene er de samme for leverandør- og kontaktkort.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Vælg den kunde, som du vil ved eller mistænker for at være dobbeltregistreret, og vælg derefter handlingen **Rediger**.
3. Vælg handlingen **Flet med** på siden **Kundekort**.
4. På siden **Flet dobbeltregistrering** i feltet **Flet med** vælger du den kunde, du har åbnet, som du tror er en dobbeltregistrering, der er indikeret i feltet **Aktuel**.

    Oversigtspanelet **Felter** viser felter, hvor værdierne er forskellige for de to kunder. Dette betyder, at hvis den valgte kunde virkelig er en dobbeltregistrering, bør kun ganske få felter blive vist, såsom stavefejl eller andre dataregistreringsfejltagelser.

    Oversigtspanelet **Relaterede tabeller** viser, hvor der er felter med en relation til begge kunder. Felterne **Aktuelt antal** og **Dobbelt antal** viser antallet af felter i relaterede tabeller, hvor **Nr.** værdien for både den aktuelle og den dobbeltregistrerede er benyttet. På siden **Flet dobbeltregistrering** er denne sektion kun til information. Hvis der imidlertid findes flettekonflikter, løser du dem på siden **Flet dobbeltkonflikter**. Se trin 8 til 12.   

5. Vælg afkrydsningsfeltet **Overskriv** for hvert felt, hvor du ønsker at benytte en anden værdi, end den aktuelle. Værdien i feltet **Alternativ værdi** vil så blive overført til den aktuelle record, når du gennemfører processen.
6. Når du har afsluttet udvælgelsen af, hvilke værdier der skal beholdes eller overskrives, vælger du handlingen **Flet**.

    Systemet tjekker, om sammenfletningen af værdier for den dobbeltregistrerede kunde til den aktuelle kunde forårsager nogen konflikter. Der er en konflikt, hvis en værdi i mindst et primært nøglefelt er det samme for begge kunder, mens værdien i feltet **Nr.** er forskelligt for de to kunder.

7. Hvis der ikke findes nogen konflikter, vælger du knappen **Ja** i beskedfeltet til bekræftelse.

    Den dobbeltregistrerede kunde omdøbes, således al forbrug af dens **Nej**- værdier i alle felter med relationer til kundetabellerne vil blive erstattet med **Nej.**- værdien fra den aktuelle kunde.
8. Hvis der er en konflikt, skal du vælge værdien **Løs (xx) konflikter før sammenfletning.** på oversigtspanelet **Konflikter**, som forekommer, hvis konflikten findes
9. Vælg linjen for den relaterede tabel med en konflikt på siden **Flet dobbeltkonflikter** og vælg så handlingen **View Details**.

    Siden **Flet dobbeltkonflikt** viser nu felterne i den valgte tabel, der forårsager en flettekonflikt mellem to kunde-records. Bemærk, i begge opsummerede værdier i felterne **Aktuel** og **Konflikter med** og på linjerne, at mindst et primært nøglefelt er det samme for begge kunder, og værdien i **Nej.**- feltet er forskelligt for begge kunder.   
10. Hvis du ikke ønsker at behold den dobbeltregistrerede kunde-record, vælger du handlingen **Fjern dobbeltregistrering**, og derefter vælger du knappen **Luk**.

    Identiske feltværdier ud over værdien i **Nej.**- feltet fjernes fra den dobbeltregistrerede record og indsættes på den aktuelle record.
11. Hvis du ønsker at beholde den dobbeltregistrerede kunde-record efter sammenfletningen, vælger du **Omdøb dobbeltregistrering**.
12. På linjer ikke for **Nej.**- feltet, hvor feltet har den samme værdi på begge records, ændr værdien i feltet **Alternativ værdi**, og vælg så knappen **Luk**.

    Den konfliktende feltværdi opdateres på den dobbeltregistrerede record, så det kan flettes med den aktuelle record. Den dobbeltregistrerede record eksisterer fortsat efter sammenfletning.
13. Gentag trinnene 8 til 12, indtil alle konflikter er løst. Oversigtspanelet **Konflikter** forsvinder.
14. Vælg handlingen **Flet** igen på siden **Flet dobbeltregistrering**, og vælg så knappen **Ja** i beskedfeltet for bekræftelse.

> [!NOTE]
> For kontakter gælder det, at du kan benytte funktionalitet til at finde dobbeltregistrerede kontakter, før du benytter siden **Flet dobbeltregistreringer**. Se [Søg efter dobbeltregistrerede kontakter](marketing-setup-contacts.md#searching-for-duplicate-contacts) for at få yderligere oplysninger.

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Opsætning af kontakter](marketing-setup-contacts.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
