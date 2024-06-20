---
title: Bruge e-dokumenter i købsprocessen
description: 'Lære, hvordan du bruger e-dokumentfunktioner, der er relateret til købsfakturaer og ordrer.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Bruge e-dokumenter i købsprocessen

Du kan bruge konfigurerede elektroniske dokumenter (e-dokumenter) sammen med købsdokumenter.

Du kan bruge følgende købsdokumenter med e-dokumenters funktioner:  

- Købsfakturaer
- Købsordrer (fra version 24.0)
- Købskreditnotaer
- Finanskladder

> [!NOTE]
> Fra [!INCLUDE[prod_short](includes/prod_short.md)] version 24.0 er det muligt at forbinde **Købsordrer** med de modtagne **E-dokumenter**.  

## E-dokumenter i køb

Modtagelse af køb af e-dokumenter i Dynamics 365 Business Central kan udføres som en kørsel eller manuelt.  

### Sådan konfigureres kreditorer til at arbejde med forskellige købsdokumenter  

Følg trinnene for at konfigurere kreditorer til at arbejde korrekt med indgående elektroniske fakturaer: 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leverandører**, og vælg derefter det relaterede link. 
2. Vælg den kreditor, du vil konfigurere.   
3. I oversigtspanelet **Modtagelse** skal du finde feltet **Modtag e-dokument til** for at angive det standardkøbsdokument, der skal genereres fra det modtagne e-dokument. 

   > [!NOTE]
   > I feltet **Modtag e-dokument til** kan brugerne enten vælge en **Købsfaktura** eller **Købsordre** baseret på, hvad de vil have oprettet ud fra den modtagne e-faktura. Denne udvælgelse påvirker ikke oprettelsen af korrigerende dokumenter; I begge scenarier genererer systemet en **Kreditnota**.  

   > [!NOTE]
   > Hvis brugeren vælger indstillingen **Købsordre** i feltet **Modtag e-dokument til**, vil systemet forsøge at opdatere en af de eksisterende købsordrer, men hvis købsordren for en leverandør i det modtagne **e-dokument** ikke findes, opretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny **Købsordre** ved hjælp af samme fremgangsmåde som oprettelsen af de nye **Købsfakturaer**, der er forklaret på denne side senere.  

4. Vælg en af de indstillinger, du vil bruge til den valgte kreditor. 
5. Luk siden.   

### Arbejde med købsfakturaer  

#### Kør batchjobbet  

> [!NOTE]
> Dette batchjob bruges til automatisk opkrævning af indgående fakturaer. Det kan kun fungere i et land eller område, hvor funktionaliteten findes.  

Hver gang der køres en **Opgavekø**, og den eksterne tjeneste har indgående fakturaer, der er sendt fra din leverandør, indsamler og importerer systemet disse fakturaer. Udfør disse trin for at fuldføre processen: 

1. Når kørslen er færdig, vises de nyligt importerede fakturaer på siden **E-dokumenter** sammen med deres grundlæggende detaljerede oplysninger. 
2. Hvis du vil se flere detaljer, skal du åbne et bestemt e-dokument.   
3. Hvis der ikke var nogen fejl eller problemer i e-dokumentet, tilknytter feltet **Post** dokumentnummeret på købsfakturaen, hvis den er konfigureret på siden **Leverandørkort** (som systemet oprettede automatisk). Vælg linket til at åbne dokumentet.
 
   > [!NOTE]
   > Dette systemoprettede dokument er ikke det bogførte dokument. 

4. Hvis du vil gå direkte til købsdokumentet, skal du markere feltet **Post**. Kontroller dokumentet, når du har åbnet siden **Købsfaktura**. Hvis alt er korrekt, skal du bogføre dokumentet.  
5. Når du bogfører købsdokumentet, opdateres feltet **Post** på **E-dokumentet** fra **Faktura** til **Købsfaktura** og nummeret på det bogførte købsdokument er tilgængeligt. Du kan vælge nummeret til at åbne den bogførte købsfaktura. 

Oplysningerne om logfiler er de samme som i salgsprocessen for e-dokumenter.  

Da fejl i salgsprocessen for det meste er relateret til tilgængeligheden af tjenesten, kan det indgående bilag indeholde flere årsager. Den mest almindelige årsag til en fejl er, at systemet ikke kan genkende linjerne på det e-dokument, du har fået fra leverandøren. Derfor kan det ikke indsætte linjer på din købsfaktura. 

Der er to almindelige fejl:  

- Hvis du vil bruge denne specifikke linje fra kreditorfakturaen, som blev bogført direkte på finanskontoen, skal du have konfigureret værdien for **Tilknyttet tekst** korrekt. Hvis du vil tilsidesætte denne fejl, hvis du vil bruge finanskonti, skal du vælge **Knyt tekst til konto** for at oprette en specifik tilknytning af værdien **Tilknyttet tekst** med den **Debetkontonr.**-værdi, som du vil bruge. 
- Hvis du vil spore lagerbeholdningen og bruge linjer fra kreditorfakturaen til at udfylde varer på dokumentlinjerne, skal du have konfigureret **Varereferencenr.** korrekt værdi. Hvis du vil omgå denne fejl, skal du knytte den eksterne vare til dine varenumre ved hjælp af varereferenceoversigten. Du kan finde flere oplysninger i [Bruge varereferencer](inventory-how-use-item-cross-refs.md). 

Når du har rettet fejlene og advarslerne, kan du manuelt angive, hvornår systemet skal oprette en købsfaktura baseret på din opsætning, ved at vælge **Opret dokument**.   

#### Importer fakturaer manuelt  

Følg disse trin for manuelt at importere eksterne e-dokumenter:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link. 
2. Vælg den aktive tjeneste på siden **E-dokumenttjeneste**.   
3. Vælg **Modtag**, og overfør den e-dokumentfil, du fik fra kreditoren. 
4. Hvis der vises en fejlmeddelelse, skal du åbne e-dokumentet for at løse problemerne. 
5. Når du er færdig med at løse problemerne, skal du vælge **Opret dokument** i gruppen **Importér manuelt**.  
6. Når dokumentet er oprettet i [!INCLUDE[prod_short](includes/prod_short.md)], ændres den måde, dokumentet vises på, ikke ved hjælp af en kørsel. 

### E-dokumenter med købsordrer  

#### Knyt købsordrer til modtaget e-dokument

Hvis din **leverandør** har konfigureret feltet **Modtag e-dokument** til at arbejde med **Købsordrer**, skal du gøre følgende, når det elektroniske dokument er oprettet i [!INCLUDE[prod_short](includes/prod_short.md)] (manuelt eller fra et eksternt slutpunkt) [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. Hvis **indkøbsordren** for denne bestemte leverandør findes, og der er et indkøbsordrenummer i filen til modtagelse af **e-dokument**, vil [!INCLUDE[prod_short](includes/prod_short.md)] automatisk knytte dette **e-dokument** til den angivne **købsordre**, og **dokumentstatus** for dette **e-dokument** vil være **i gang**, og **e-dokumentstatus** på undersiden **Servicestatus** vil være **ordretilknyttet**. Dette link vil være synligt i feltet **Dokument** på dette specifikke **e-dokument**. Hvis du har brug for at ændre den **købsordre**, der er tilknyttet automatisk, kan du gøre det ved at udføre handlingen **Opdater købsordrelink** og manuelt vælge en af de eksisterende købsordrer for denne leverandør. Du kan kun gøre det, før linjerne mellem **E-dokument** og **købsordre** er matchet.  

2. Hvis **indkøbsordren** for denne bestemte leverandør findes, men der ikke er noget indkøbsordrenummer i den modtagne **E-dokumentfil** , [!INCLUDE[prod_short](includes/prod_short.md)]  giver det mulighed for at vælge en af de eksisterende indkøbsordrer, når og hvis du uploadede dette dokument manuelt. Dette åbner listen **Købsordrer** med ordrer kun til den leverandør, som du modtog **E-dokumentet** fra. Du skal vælge **Købsordre**, du vil bruge, og derefter vælge **OK**. Hvis du ikke kunne vælge den korrekte **købsordre** eller få **e-dokumentet** automatisk fra et eksternt slutpunkt ved hjælp af **opgavekøen**, vil et nyt **e-dokument** ikke blive knyttet til noget købsdokument. **Dokumentstatus** viser **Fejl**, **E-dokumentstatus** på undersiden **Servicestatus** også vise **Importeret dokumentbehandlingsfejl**. Hvis tilknytningen til **købsordren** er afsluttet, skal du vælge handlingen **Opdater link til købsordre** og vælge en af de eksisterende købsordrer for denne leverandør. 

3. Hvis **indkøbsordren** for denne bestemte leverandør ikke findes på oprettelsestidspunktet, oprettes et nyt **e-dokument**, [!INCLUDE[prod_short](includes/prod_short.md)] opretter en ny **indkøbsordre** ved hjælp af den samme oprettelsesmodel, som allerede findes for nye **købsfakturaer**. **Dokumentstatus** for dette **e-dokument** vil blive **behandlet**, og **e-dokumentstatus** på undersiden **Servicestatus** vil være **Importeret dokument oprettet**. Dette link vil være synligt i feltet **Dokument** på dette specifikke **e-dokument**.   

#### Matche linjer fra modtaget e-dokument med købsordre  

Du kan matche dine modtagne elektroniske dokumenter med købsordrelinjer fra to forskellige steder, fra siden: **E-dokument** eller fra siden **Købsordre**. Den nemmeste måde at finde de allerede sammenkædede **købsordrer** på er at bruge feltet **Sammenkædede købsordrer** som en del af **e-dokumentaktiviteter**. Alle ikke-sammenkædede dokumenter kan findes ved hjælp af feltet **Venter på købs-e-fakturaer**, hvor du har en liste over **e-dokumenter**, du skal gennemse.  

> [!NOTE]
> **E-dokumentaktiviteter** med disse to felter findes i følgende **rollecentre**: Evaluering af forretningschef, Forretningschef, Bogholder, Lagerchef og Levering og modtagelse.  

> [!NOTE]
> Hvis momsprocenten er forskellig mellem det indgående bilag og virksomhedens momsprocent, kan matchende dokumenter ikke bruges i et miljø med flere lande.  

##### Matching af linjer fra købsordrer  

Du kan matche linjerne fra listen **Købsordrer** eller fra en af de åbne **købsordrer**. Det kan du gøre ved at benytte følgende fremgangsmåde:  

1. Vælg feltet **Sammenkædede købsordrer** i rollecenteret, hvis der er et nummer. 
2. Vælg en af to muligheder for matchning: 

   - Hvis du vil matche linjerne fra listen **Købsordrer**, skal du vælge den **købsordrelinje**, du vil matche, og vælge handlingen **Tilknyt e-dokumentlinjer**.  
   - Hvis du først vil åbne **købsordren**, skal du åbne dokumentet og derefter vælge handlingen **Tilknyt e-dokumentlinjer**. 

3. Da begge muligheder har samme proces, åbner du siden **Matchning af købsordre** med følgende indhold: 

    1. I sidehovedet findes følgende oplysninger, som kan hjælpe dig med at knytte linjerne lettere: 

       |Feltnavn |Beskrivelse |
       |--------|-----------------|
       |Leverandørnavn |Angiver leverandørens navn på det elektroniske dokument. |
       |E-dokumentnr. |Angiver det linkede elektroniske dokumentnummer. |
       |E-dokumentdato |Angiver bogføringsdatoen for det linkede elektroniske dokument.  |
       |E-dokumentbeløb |Angiver det samlede beløb for det linkede e-dokument inklusive moms. |

    2. På linjerne kan du finde de linjer, der er importeret fra **E-dokumentfilen** i venstre side og linjerne fra den eksisterende **indkøbsordre** i højre side.  
    3. Alle linjer på begge sider har varenumre og beskrivelser sammen med **Købspris** og **Linjerabatpct**.  
    4. På siden **Importerede linjer** kan du også finde feltet **Antal** som et samlet antal fra e-faktura, og feltet **Matchet antal** angiver det antal, der allerede passer til købsordrelinjerne. 
    5. På siden **Købsordrelinjer** kan du også finde **Disponibelt antal** som det antal, der kan matches med linjen (modtaget, men ikke faktureret antal) og **Fakturer antal**, med angivelse af det antal, der allerede er matchet med denne linje. 
    6. Hvis du vil matche linjer, skal du markere de linjer på begge sider, som du vil matche, og vælge handlingen **Match manuelt**. De matchede linjer markeres med grønt. 
    7. Det er muligt at matche en til en, men det er også muligt at matche mange til en eller en til mange ved at vælge flere linjer på den ene eller anden side, før du vælger handlingen **Match manuelt**. 
    8. Du kan også vælge handlingen **Match automatisk** for automatisk at matche alle linjer med samme **Type**, **Nr.**, **Enhedspris**, **Rabat** og **Måleenhed**. 
    9. Hvis du laver en fejl, kan du vælge handlingen **Fjern match** for at fjerne de matchede linjer på købsordresiden eller vælge handlingen **Nulstil matchning** for at nulstille alt, hvad der matcher. 
    10. Hvis dit **e-dokument** har mange linjer, kan du under matchningsprocessen vælge handlingen **Vis ventende linjer** for at fjerne alle e-dokumentlinjerne, hvis de allerede er fuldstændigt matchede. Hvis du har brug for at se alle linjerne, kan du altid vælge handlingen **Vis alle linjer**. 

4. Når du er færdig med matchningen, skal du vælge handlingen **Anvend på købsordre**.   
5. Når du har anvendt matchningen på **købsordren**, [!INCLUDE[prod_short](includes/prod_short.md)] opdateres følgende felter:

    1. **Kreditors fakturanr.** og **Bilagsdato** i dokumenthovedet opdateres med værdier fra det elektroniske dokument, du har modtaget og sammenkædet. 
    2. **Fakturer antal** i linjer opdateres med værdierne fra kolonnen **Fakturer antal** fra siden **Matchning af købsordre** baseret på de matchninger, du har foretaget. 
    3. Du kan nu bogføre dokumentet ved at vælge handlingen **Bogfør**.  
    4. Når du bogfører dokumentet, ændrer feltet **Dokument** på siden **E-dokument** værdien, og det vil relatere til den **bogførte købsfaktura**. 
    5. Luk siden.  

> [!IMPORTANT]
> Som standard kan du kun matche de linjer, der har det samme samlede beløb i begge dokumenter. Det betyder, at **Købspris** sammen med den anvendte **linjerabatpct.** skal være den samme, da du i ét dokument kan have et beløb uden rabat og i et andet med rabat.  

Hvis du vil tilføje en vis tolerance og tillade forskellen mellem linjerne i **E-faktura** og **Købsordre**, skal du følge trinene:   

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Købsopsætning** og vælg derefter det relaterede link.  
2. Du vil tillade tolerance i feltet **E-bilagsmatchningsdifferencepct.**, der angiver den maksimalt tilladte procentdel af omkostningsforskellen, når den indgående **E-dokumentlinje** matches med **købsordrelinjen**. 
3. Denne opsætning vil gælde for alle matchende linjer, men igen under hensyntagen til tolerance for det samlede beløb, som for **Købspris** sammen med anvendt **Linjerabatpct.**.  
4. Luk siden.   

##### Match af linjer fra e-dokument  

Du kan matche linjerne på siden **E-dokument**. Brug følgende trin for at starte dette:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **E-dokumenter**, og vælg derefter det relaterede link. 
2. Vælg det **E-Dokument**, du vil matche.   
3. Vælg handlingen **Match købsordre** for at åbne siden **Matchning af købsordrer**.  
4. Gentag de samme trin, som du brugte, da du begyndte at matche fra købsordrer.

### Hjælp til copilot-matchning af e-dokumenter  

> [!NOTE]
> I øjeblikket har copiloten **Hjælp til matching af e-dokument** status som produktionsklar forhåndsversion, og den er tilgængelig globalt undtagen i Canada. Det fungerer kun på engelsk. 

> [!NOTE]
> Copilot er den AI-drevne assistent, der hjælper folk på tværs af din organisation med at frigøre deres kreativitet og automatisere kedelige opgaver. Copiloten **E-Document Matching Assistance** hjælper brugerne med nemt at matche deres modtagne elektroniske fakturaer med eksisterende indkøbsordrelinjer ved hjælp af LLM-modellen til matchning af linjer mellem to forskellige dokumenter. 

#### Sådan aktiveres copiloten  

Hvis du ikke aktiverede **Hjælp til match af e-dokument**-copilot, skal du gøre det manuelt. Følg trinene for at aktivere copiloten **Hjælp til matchning af e-dokumenter**: 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Copilot- og AI-funktioner**, og vælg derefter det relaterede link. 
2. På listen over funktioner skal du vælge **Hjælp til match af e-dokument** og ændre status til **Aktiv**.  

Når copilot er aktiveret, kan du begynde at bruge den.

#### Brug copilot-matchning af e-dokumenter 

Hvis copilot er aktiveret, vil eksisterende handlinger **Tilknyt E-dokumentlinjer** på købte ordrer og **Match købsordre** på siden **E-dokument** få forskellige ikoner, der symboliserer AI-kapacitet. Du kan køre disse handlinger (samme som i tidligere eksempler fra listen over købsordrer), fra en af **købsordrer** eller fra **E-dokument**. Alle trin til løb er de samme, men når du kører denne handling, bliver resultatet anderledes, og du skal følge disse trin:  

1. Vælg handlingen **Tilknyt e-dokumentlinjer** eller **Match købsordre** for allerede sammenkædede dokumenter.  
2. Bemærk, at **E-dokument match ordrelinjer med Copilot**-prompten fungerer, og du har siden **Købsordrematchning** i baggrunden. Det betyder, at den samme proces sker, men med automatisk support fra **Copilot**, som kører processen med at matche i stedet for dig. 
3. Efter et par sekunder vil **E-dokument match ordrelinjer med Copilot** foreslå linjer til matchning med nogle yderligere detaljer: 

    1. Du kan finde følgende oplysninger i prompthovedet: 

       |Feltnavn |Beskrivelse |
       |--------|-----------------|
       |Automatisk matchet | Angiver antallet af matches, der foreslås automatisk. Dette er baseret på en strengsammenligning, og hvis der er 80 % eller flere beskrivelser, der overlapper hinanden, matcher systemet automatisk disse beskrivelser uden at bruge GPT-funktioner. |
       |Copilot matchet | Angiver antallet af matches, der er foreslået af copilot, ved hjælp af både streng- og semantisk sammenligning. |
       |E-dokumentnr. | Angiver det linkede e-dokumentnummer. |
       |Fakturatotal ekskl. moms | Angiver det samlede fakturabeløb, ekskl. moms. |
       |Matchet totalbeløb inkl. moms | Angiver det matchede beløb inkl. moms. |
    
    2. Hvis alle linjer er matchet, kan du se den grønne tekst i øverste højre hjørne: **Alle linjer (100 %) er matchede. Gennemgå matchforslag**.  
    3. Du kan finde følgende oplysninger i **Matchet forslag**-linjerne:  

       |Feltnavn |Beskrivelse |
       |--------|-----------------|
       |E-dokumentlinjenr. | Angiver e-dokumentlinjenummeret (fra den oprindelige e-dokumentfil). |
       |Beskrivelse af e-dokumentlinje | Angiver e-dokumentlinjebeskrivelsen (fra den oprindelige e-dokumentfil). |
       |Matchet antal | Angiver det antal, der skal anvendes på købsordrelinjen. |
       |Tilbud | Angiver den handling, der foreslås af AI, og disse foreslåede handlinger er relateret til matchning af købsordrelinjerne. |

    4. Alle fuldt foreslåede og matchede linjer er markeret med grøn farve. Hvis der er et problem, dvs. en anden pris, men i det tilladte prisinterval, markeres denne linje som gul, og hvis der er lighed mellem beskrivelsesfelterne, men prisforskellen er større end tilladt, markeres denne linje som rød. 
    5. Hvis du ikke er tilfreds med nogle forslag, kan du slette dem ved hjælp af handlingen **Slet linje**.  
    6. Hvis du vil se matchning af forslag, kan du vælge linket i kolonnen **Forslag** for at åbne siden **Oplysninger om e-dokumentmatch**. 
    7. På siden **E-dokumentmatchdetaljer** kan du sammenligne detaljer fra **E-dokumentet** og **købsordren** for at være sikker på den foreslåede matchning, før du bekræfter den. 
    8. Luk siden efter gennemgang.   

4. Hvis du ikke er tilfreds med de fleste af forslagene, eller hvis du ikke vil bruge **E-dokument match ordrelinjer med Copilot-funktionen**, skal du vælge **Kassér den**, hvorefter du kan fortsætte med den manuelle matchning som forklaret tidligere.  
5. Hvis du vil beholde forslag, skal du vælge knappen **Behold det**, og systemet gemmer alle forslag fra **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lukker Copilot-prompten, og linjerne på siden **Matchning af købsordre** markeres som grønne, da de allerede er matchet. 
7. Nu kan du fortsætte med at arbejde, mens du laver manuel matchning. Det betyder, at du kan fjerne matches, matche manuelt eller nulstille matchning. Hvis du ikke vil foretage ændringer, skal du blot vælge handlingen **Anvend på købsordre** og fortsætte med at **arbejde med købsordren**. 

> [!NOTE]
> Du kan vælge handlingen **Match med Copilot** på siden **Matchning af købsordre** igen, men i dette tilfælde bliver du spurgt, om du vil overskrive de eksisterende matches, da alle linjer allerede er matchet.  

> [!NOTE]
> Analyse af pris/omkostninger og kontrol af tilgængeligt antal er en del af forbehandlingen.   

## Oversigt over e-dokumentstatusser

Hvis du vil have et bedre overblik over alle e-dokumenter i regnskabet, kan du vælge rollecenteret **Bogholder**, hvor der findes e-dokumentstatusser. Der kan du finde e-dokumentaktiviteter, der har følgende statusser:

- **Indgående e-dokumenter:**

    - Behandlet
    - Igangværende
    - Fejl


## Se også

[Opsætte e-dokumenter](finance-how-setup-edocuments.md)    
[Bruge e-dokument i salgsprocessen](finance-how-use-edocuments.md)   
[Udvide e-dokumenters funktionalitet](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Økonomistyring](finance.md)    
[Fakturasalg](sales-how-invoice-sales.md)    
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)    
[Arbejde med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

