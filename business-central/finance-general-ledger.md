---
title: Om Finans og kontoplanen
description: 'Beskriver finans-, kontoplans- og kontokategorier. Brug siden Opsætning af Finans til at angive, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a><a name="understanding-the-general-ledger-and-chart-of-accounts"></a><a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Forstå Finans og Kontoplan

Finansregnskabet gemmer de finansielle data, og kontoplanen viser de konti, som alle finansposter bogføres til. [!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

## <a name="general-ledger-setup-and-general-posting-setup"></a><a name="general-ledger-setup-and-general-posting-setup"></a><a name="general-ledger-setup-and-general-posting-setup"></a>Finansopsætning og bogføringsopsætning

Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data. To sider spiller især en vigtig rolle for konfigurering af dine økonomiske processer:  

* Åbn siden **Finansopsætning**

  På siden **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:  

  * Detaljer om fakturaafrunding  
  * Adresseformater  
  * Økonomirapportering

  > [!TIP]
  > Siden **Regnskabsopsætning** indeholder generiske felter og felter, der er specifikke for dit land eller område. Hvis du ikke er sikker på, hvad et felt betyder, anbefaler vi, at du spørger din bogholder, om det er relevant for din virksomhed. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Åbn siden [her](https://businesscentral.dynamics.com/?page=118).
  
* Siden **Finansopsætning**

  Desuden kan du på siden **Bogføringsopsætning** angive, hvordan du vil oprette kombinationer af virksomheds- og produktbogføringsgrupper. Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti. Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper. Men du kan også åbne hver linje på sit eget bogføringsopsætningskort. Flere oplysninger i [Opsætning af bogføringsgrupper](finance-posting-groups.md).  

  > [!TIP]
  > Hvis du ikke kan se de ønskede felter på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

  Åbn siden [her](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper til kontoen.
* Se separate debet- og kreditsaldi for en enkelt konto.

Du kan tilføje, ændre eller slette finanskonti. Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen. Du kan også starte med 2022 Release Wave 2, men du kan også blokere for utilsigtet sletning af konti i følsomme perioder. Få mere at vide i afsnittet [Sletning af konti](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a><a name="account-categories"></a><a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.  

Siden **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem. Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.  

Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje på siden **Finanskontokategorier**. Med kategorigrupper kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo. Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.  

Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter. Kontokategorier hjælper med at definere layoutet af regnskabet.  

### <a name="example"></a><a name="example"></a><a name="example"></a>Eksempel

F.eks. har standardsaldoopgørelsen en underkategori for *Kassebeholdning* under *Omsætningsaktiver*. Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Finanskontokategorier**, og vælg derefter det relaterede link.
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

## <a name="get-a-quick-overview"></a><a name="get-a-quick-overview"></a><a name="get-a-quick-overview"></a>Få et hurtigt overblik

**Kontoplan** viser kontiene på en hierarkisk liste, der giver hurtig adgang til nøgleoplysninger for hver konto. Listen er imidlertid statisk, og hvis du har mange konti, skal du muligvis rulle for at få vist forskellige konti. Hvis du blot vil have et hurtigt overblik over det grundlæggende, f. eks. bevægelser og saldi, er siden **Oversigt over kontoplaner** et nyttigt alternativ. Kolonnelayoutet på siden er nu den samme, som du finder på siden **Kontoplan** (men med færre kolonner), så du ikke behøver at orientere dig igen. Du kan udvide eller skjule de hierarkiske niveauer for at gøre visningen smallere. Hvis du vil gøre det nemt at skifte mellem siderne, er siden **Oversigt over kontoplan** tilgængelig på siden **kontoplan**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a><a name="access-to-create-and-edit-accounts-and-account-categories"></a><a name="access-to-create-and-edit-accounts-and-account-categories"></a>Adgang til at oprette og redigere konti og kontokategorier

I en mindre organisation, f.eks. CRONUS-demoregnskabet, kan de fleste brugere redigere kontoplanen, undtagen brugere med en licens som TEAMMEDLEM. I større organisationer bruges roller og tilladelser typisk til at begrænse adgang til redigering af kontoplanen. Hvis du er administrator, eller du har rollen *Forretningschef* eller *Bogholder*, kan du kontrollere tilladelserne for alle brugere for at sikre, at de rette personer har adgang til de relevante tabeller. Du kan finde flere oplysninger i afsnittet [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/business-central-configure-general-ledger-setup/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Konfigurere eller ændre kontoplanen](finance-setup-chart-accounts.md)  
[Tildel rettigheder til brugere og grupper](ui-define-granular-permissions.md)  
[Business Intelligence](bi.md)  
[Finans](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
