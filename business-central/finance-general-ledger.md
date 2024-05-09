---
title: Forstå Finans og Kontoplan
description: 'Beskriver finans-, kontoplans- og kontokategorier. Brug siden Opsætning af Finans til at angive, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Forstå Finans og Kontoplan

Finansregnskabet gemmer de finansielle data, og kontoplanen viser de konti, som alle finansposter bogføres til. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansopsætning og bogføringsopsætning

Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data. To sider spiller især en vigtig rolle for konfigurering af dine økonomiske processer:  

* **Regnskabsopsætning**
* **Bogføringsopsætning**

### <a name="the-general-ledger-setup-page"></a>Åbn siden **Finansopsætning**

På siden **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:  

* Detaljer om fakturaafrunding  
* Adresseformater  
* Økonomirapportering

> [!TIP]
> Siden **Regnskabsopsætning** indeholder generiske felter og felter, der er specifikke for dit land eller område. Hvis du ikke er sikker på, hvad et felt betyder, anbefaler vi, at du spørger din bogholder, om det er relevant for din virksomhed. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Hvis du vil åbne siden nu, skal du bruge følgende link [Regnskabsopsætning](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>Siden **Finansopsætning**

Brug vinduet **Bogføringsopsætning** til at angive kombinationer af virksomheds- og produktbogføringsgrupper. Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper. Men du kan også åbne hver linje på sit eget bogføringsopsætningskort. Flere oplysninger i [Opsætning af bogføringsgrupper](finance-posting-groups.md).  

> [!TIP]
> Hvis du ikke kan se de ønskede felter på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

Hvis du vil åbne siden nu, skal du bruge følgende link [Bogføringsopsætning](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Kontoplanen

**Kontoplanen** viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper til kontoen.
* Se separate debet- og kreditsaldi for en enkelt konto.

Få mere at vide i [Forståelse af Kontoplanen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.  

Siden **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem. Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.  

Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje på siden **Finanskontokategorier**. Med kategorigrupper kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo. Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.  

Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter. Kontokategorier hjælper med at definere layoutet af regnskabet.  

### <a name="example"></a>Eksempel

F.eks. har standardsaldoopgørelsen en underkategori for *Kassebeholdning* under *Omsætningsaktiver*. Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, kan du gør følgende:

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finanskontokategorier**, og vælg derefter det relaterede link.
   1. Eller [åbn siden her](https://businesscentral.dynamics.com/?page=790).
2. Vælg handlingen **Rediger liste**.
3. Tilføje to nye underkategorier: Én for kontantbeholdning og én for din checkkonto:
   1. Vælg kategorien **Omsætningsaktiver**.
   2. Vælg handlingen **Ny**.
   3. Angiv navnet på underkategorien i feltet **Beskrivelse**.
   4. Vælg den relevante finanskonto i feltet **Finanskonto i kategori**.
   5. Vælg indstillingen **Kontantkonti** i feltet **Ekstra rapportdefinition**.
4. Indrykke dem under underkategorien **Kassebeholdning**.
   1. Vælg den under kategori, der blev oprettet i trin 3.
   2. Vælg handlingen **Indryk**.
   3. Vælg handlingen **Flyt ned**.
   4. Vælg handlingen **Indryk** for at indrykke under kategorien **Kontant**.

Når du vælger handlingen **Generér finansielle rapporter**, eller næste gang rapporten genereres, vil saldoopgørelsen vise følgende linjer:

* Total balance for kontanter.
* Linjer med saldi for kontantbeholdning og checkkontoen.  

> [!NOTE]
> Hvis du opretter en finanskonto uden at tilknytte en kontokategori, tildeles kontoarten automatisk fra finanskontoen, når du knytter kontoen til en bogføringsgruppe [!INCLUDE[prod_short](includes/prod_short.md)], lige over kontoen i din kontoplan. Hvis du vil medtage den nye konto i dine regnskabsrapporter, skal du imidlertid vælge handlingen **Generér finansielle rapporter** på siden **Finanskontokategorier**. Du kan også åbne finanskortsiden ved at angive kontoarten og derefter generere din finansrapport igen.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Adgang til at oprette og redigere finanskonti og kontokategorier

I en mindre organisation, f.eks. CRONUS-demoregnskabet, kan de fleste brugere redigere finansielle objekter som f.eks. finanskonti, kontokategorier og kontoplanen, undtagen brugere med en licens som TEAMMEDLEM. I større organisationer bruges roller og tilladelser typisk til at begrænse adgang til redigering af disse objekter. Hvis du er administrator, eller du har rollen *Forretningschef* eller *Bogholder*, kan du kontrollere tilladelserne for alle brugere for at sikre, at de rette personer har adgang til de relevante tabeller. Du kan finde flere oplysninger i afsnittet [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Brug dimensioner til at forenkle din kontoplan

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra. Så i stedet for at oprette separate finanskonti for hver afdeling og hvert projekt kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplan.

Du kan lære mere om dimensioner ved at få til [Sådan konfigureres standarddimensioner for kunder, leverandører og andre konti](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Se også

[Forstå kontoplaner](finance-chart-of-accounts.md)  
[Arbejde med dimensioner](finance-dimensions.md)  
[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Finans](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
