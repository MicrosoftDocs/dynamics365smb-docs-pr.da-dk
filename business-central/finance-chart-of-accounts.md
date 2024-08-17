---
title: Forstå kontoplaner
description: 'Beskriver kontoplanen, hvordan den konfigureres, og hvordan den bruges.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/06/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Forstå kontoplaner

En kontoplan (COA) fungerer som et omfattende bibliotek over finansielle konti og deres tilsvarende referencenumre. Et ægthedsbevis består typisk af to hovedkategorier af konti:

- Balancekonti: Disse konti sporer din virksomheds aktiver, gæld og nettoværdi.
- Resultatopgørelseskonti: Disse konti registrerer indtægter fra forskellige kilder og sporer også udgifter.

Balancekonti er yderligere kategoriseret i tre grupper:

1. Aktivkonti: Disse konti sporer alle de værdifulde ressourcer, der ejes af din virksomhed.
1. Passivkonti: De registrerer din virksomheds gæld.
1. Egenkapitalkonti: Repræsenter restværdien i virksomheden efter fradrag af forpligtelser fra aktiver.

Resultatkonti er opdelt i to grupper:

1. Indtægtskonti: Disse konti registrerer din virksomheds indtægter fra forskellige kilder.
1. Udgiftskonti: Disse konti registrerer alle virksomhedens udgifter.

Brug ægthedsbeviset til at registrere transaktioner i organisationens finansposter. Hver konto har typisk et id (kontonummer) og en beskrivende billedtekst eller overskrift, og de kodes systematisk baseret på deres kontotype.

[!INCLUDE[prod_short](includes/prod_short.md)] indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.

Sammensætningen af din virksomheds kontoplan er en strategisk beslutning, der træffes af din ledelse (eller af landespecifik regulering). Det varierer afhængigt af din virksomheds branche, forretningsmodel og økonomiske struktur. Afhængigt af din branche kan du f.eks. have specifikke aktivkonti, der er skræddersyet til din virksomheds unikke drift og behov:

* En detailvirksomhed kan lægge vægt på lager og tilgodehavender.
* En teknologivirksomhed kan fokusere på immaterielle aktiver som patenter og software.
* Et produktionsanlæg ville spore anlægsaktiver og forsyninger.

## <a name="the-chart-of-accounts-page"></a>Siden Kontoplan

Kontoplanen viser alle finanskonti. Fra kontoplanen kan du gøre ting som at:  

* Vise rapporter med finansposter og saldi.  
* Lukke din resultatopgørelse.  
* Åbne finanskontokortet for at tilføje eller ændre indstillinger.  
* Se en oversigt over bogføringsgrupper til kontoen.
* Se separate debet- og kreditsaldi for en enkelt konto.

Du kan tilføje, ændre eller slette finanskonti. Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen. Hvis du vil undgå fejltagelser i følsomme perioder, kan du også blokere for sletning af konti. Du kan få flere oplysninger om, hvordan du beskytter konti mod sletning, ved at gå til [Sletning af konti](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>Kodehierarkiet i finanskonti

Virksomheder opretter typisk en hierarkisk struktur i finanskontokoder for at afspejle, hvor de hører hjemme i kontoplanen. I nogle implementeringer angiver finanskontokoder, der starter med **1**, aktivkonti, mens finanskontokoder, der starter med 3, angiver egenkapitalkonti. I nogle områder er der lokale regler for brug af en standardkontoplan. For at hjælpe brugerne med at forstå dette hierarki uden at kende den interne kodestruktur kan du definere overskrifter og subtotaler i din kontoplan, der indkapsler disse interne strukturer.

## <a name="designing-your-chart-of-accounts"></a>Design af din kontoplan

Hver linje i kontoplaner er en finanskonto på en af typerne:

* Bogføring (kladder kan bogføre linjer til disse konti)
* Overskrift (definerer en overordnet overskrift i kontoplanen)
* I alt (definerer en formel for en subtotal i kontoplanen)
* Fra-sum (definerer en begyndelsesoverskrift for en subtotal i kontoplanen. Alle efterfølgende linjer indtil en Til-sum-linje indrykkes)
* Til-sum (definerer en slutoverskrift for en subtotal og formlen for den i kontoplanen. Alle efterfølgende linjer efter denne Til-sum-linje rykkes ud)

En minimalistisk kontoplan kan kun bestå af linjer med bogføringskonti. Du kan bruge de fire andre typer til at definere, hvordan kontoplanen også viser et regnskab med hoveder og subtotaler. Sammentællingskonti bruges ofte i forbindelse med Financial Reporting.

> [!TIP]
> Hvis du bruger andre kontotyper end **Bogføring** i kontoplanen, kan du definere forskellige visninger, så de "rå" bogføringskonti vises, uden rapporteringskontotyperne for sammentælling og overskrifter. Vis f.eks. kun bogføringskonti og Skjul spærrede konti.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Brug dimensioner til at forenkle din kontoplan

Dimensioner er værdier, der kategoriserer poster, så du kan spore og analysere dem i dokumenter som f.eks. salgsordrer. Dimensioner kan f.eks. angive det projekt eller den afdeling, en post kommer fra. Så i stedet for at oprette separate finanskonti for hver afdeling og hvert projekt kan du bruge dimensioner som grundlag for analyse og undgå at skulle oprette en kompliceret kontoplan.

Hvis du vil vide mere om dimensioner, skal du gå til [Arbejde med dimensioner](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Få et hurtigt overblik over din økonomi

**Kontoplan** viser kontiene på en hierarkisk liste, der giver hurtig adgang til nøgleoplysninger for hver konto. Listen er imidlertid statisk, og hvis du har mange konti, skal du muligvis rulle for at få vist forskellige konti. Hvis du blot vil have et hurtigt overblik over det grundlæggende, f. eks. bevægelser og saldi, er siden **Oversigt over kontoplaner** et nyttigt alternativ. Kolonnelayoutet på siden er nu den samme, som du finder på siden **Kontoplan** (men med færre kolonner), så du ikke behøver at orientere dig igen. Du kan udvide eller skjule de hierarkiske niveauer. Hvis du vil gøre det nemt at skifte mellem siderne, er siden **Oversigt over kontoplan** tilgængelig på siden **kontoplan**.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Adgang til at oprette og redigere kontoplanen

I en mindre organisation, f.eks. CRONUS-demoregnskabet, kan de fleste brugere redigere kontoplanen, undtagen brugere med en licens som TEAMMEDLEM. I større organisationer bruges roller og tilladelser typisk til at begrænse adgang til redigering af kontoplanen. Hvis du er administrator, eller du har rollen Forretningschef eller Bogholder, kan du kontrollere tilladelserne for alle brugere for at sikre, at de rette personer har adgang til de relevante tabeller. Du kan finde flere oplysninger i afsnittet [Sådan får du vist en oversigt over en brugers rettigheder](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Bedste fremgangsmåder for kontoplan

Her er nogle anbefalede fremgangsmåder, som du kan overveje, når du udvikler og vedligeholder dine kontoplaner:

* Sammensæt din virksomheds kontoplan for at understøtte de finansielle rapporteringsbehov, så din ledelse kan træffe strategiske beslutninger.
* Overvej at starte simpelt med færre finanskonti. Du kan altid tilføje mere detaljerede konti, hvis det er nødvendigt.
* Definere overskrifter og subtotaler i din kontoplan, der opsummerer de interne strukturer i finanskonti.
* Brug dimensioner til at forenkle din kontoplan. Har ikke specifikke finanskonti for hvert produkt eller afdeling.
* Tilføj nye finanskonti, efterhånden som de kommer ind, men fjern kun konti fra kontoplanen ved slutningen af regnskabsperioden.

## <a name="see-also"></a>Se også

[Oprette eller ændre kontoplanen](finance-setup-chart-accounts.md)    
[Forstå Finans](finance-general-ledger.md)  
[Finansiel analyse](bi.md)    
[Oversigt for Finance](finance.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
