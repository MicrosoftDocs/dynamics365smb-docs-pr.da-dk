---
title: Knytte e-dokumenter til indkøbsordrelinjer med Copilot
description: 'Få mere at vide om, hvordan du bruger Copilot til at knytte e-dokumenter til købsordrelinjer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# Knytte e-dokumenter til købsordrelinjer med Copilot (forhåndsversion)

Efterhånden som indkøbsprocesserne bliver mere digitale, spiller e-dokumentfunktionen i Business Central en central rolle i automatiseringen af modtagelsen og behandlingen af kreditorfakturaer. Copilot kan hjælpe med denne proces ved at forbedre tilknytningen og matchningen af kreditorfakturaer med købsordrer. Dette reducerer tidskrævende opgaver, der normalt ville indbefatte omfattende søgning, opslag og dataindtastning. Fordelen bliver større af det faktum, at kreditorfakturaer ofte ikke relateret præcist til indkøbsordrer, i hvilket tilfælde Copilot er bedre til at identificere de tilsvarende indkøbsordrer. Forbedrede matchingsfunktioner gavner især små og mellemstore organisationer, der har brug for effektiv dokumentsporing for indkøbsordrelinjer. Copilot er den AI-drevne assistent til arbejde, der øger kreativiteten og forbedrer produktiviteten for Business Central-brugere.

> [!IMPORTANT]
> - Det er en produktionsklar prøveversionsfunktion til produktions- og sandkassemiljøer i alle landes lokaliseringer med undtagelse af Canada.
> - De supplerende vilkår for anvendelse i en produktionsklar forhåndsversion. Flere oplysninger: [Supplerende vilkår for anvendelse af Dynamics 365 Forhåndsversion](https://go.microsoft.com/fwlink/?linkid=2105274)
> - AI-genereret indhold kan være forkert.

I den første version af appen **e-dokument** introducerede vi grundlæggende scenarier for e-dokumenter for hele salgsprocessen. Der er dog behov for forbedringer og automatisering i håndteringen af de modtagne dokumenter, især i forbindelse med købsprocesser. Copilot forfiner, hvordan du administrerer e-dokumenter i købsprocessen, især med hensyn til indkøbsordrer. Med strukturen i e-dokumenter kan du angive den type købsdokument, der skal oprettes for hver kreditor, når du modtager e-fakturaer fra dem. Tidligere var den eneste mulighed at oprette en købsfaktura, enten som et dokument eller en finanskladde.

Du kan nu opdatere en eksisterende indkøbsordre i Business Central med de oplysninger, der modtages i e-fakturaen.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## Sådan aktiveres Copilot  

Hvis du ikke aktiverede **Hjælp til matchning af e-dokumenter** Copilot, skal du gøre det manuelt. Følg trinene for at aktivere copiloten **Hjælp til matchning af e-dokumenter**: 

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Copilot- og AI-funktioner**, og vælg derefter det relaterede link. 
2. På listen over funktioner skal du vælge **Hjælp til matchning af e-dokumenter** og ændre status til **Aktiv**.  

Du kan begynde at bruge Copilot, så snart den er aktiveret. 

## Identificere købsordrer

Først kan du identificere de købsordrer, som du kan matche automatisk. Hvis din **leverandør** har konfigureret feltet **Modtag e-dokument** til at arbejde med **Købsordrer**, skal du gøre følgende, når det elektroniske dokument er oprettet i [!INCLUDE[prod_short](includes/prod_short.md)] (manuelt eller fra et eksternt slutpunkt) [!INCLUDE[prod_short](includes/prod_short.md)]:

1. Hvis **købsordren** for denne bestemte leverandør *findes, og der er et indkøbsordrenummer* i den modtagne **E-dokumentfil**, vil dette [!INCLUDE[prod_short](includes/prod_short.md)] **E-dokument** automatisk blive knyttet til den angivne **købsordre**. **Dokumentstatus** for dette **e-dokument** er **o proces**, og **e-dokumentstatus** på undersiden **Servicestatus** vil være **Ordre tilknyttet**.  
Dette link vil være synligt i feltet **Dokument** på dette specifikke **e-dokument**. Hvis du har brug for at ændre den **købsordre**, der er tilknyttet automatisk, kan du gøre det ved at udføre handlingen **Opdater købsordrelink** og manuelt vælge en af de eksisterende købsordrer for denne leverandør. Du kan kun gøre det, før linjerne mellem **E-dokument** og **købsordre** er matchet.  
2. Hvis **indkøbsordren** for denne bestemte leverandør *findes, men der ikke er et indkøbsordrenummer* i filen til modtagelse af **e-dokument**-filen, hvis du har overført dette dokument manuelt, kan [!INCLUDE[prod_short](includes/prod_short.md)] give mulighed for at vælge en af eksisterende indkøbsordrer, når du åbner listen **Indkøbsordrer** fra de ordrer, du har modtaget fra leverandører, der kun indeholder **E-dokument**, hvor du kan vælge den **Købsordre**, du vil bruge, og vælge **OK**. Hvis du ikke har valgt den rigtige **Købsordre**, eller du automatisk har hentet **e-dokumentet** fra et eksternt slutpunkt ved hjælp af **opgavekøen**, vil det nye **e-dokument** ikke blive knyttet til noget købsdokument, og **Dokumentstatus** vil være **Fejl**, og **E-dokumentstatus** på undersiden **Servicestatus** vil være **Importeret dokumentbehandlingsfejl**. Hvis tilknytningen til **købsordren** er afsluttet, skal du vælge handlingen **Opdater link til købsordre** og vælge en af de eksisterende købsordrer for denne leverandør.  

## Tilknytte linjer

Copilot hjælper dig med automatisk at matche e-fakturalinjer med indkøbsordrelinjer og tilbyder ekstra matchende intelligens for at forbedre matchene.

Når de er matchet og tilknyttet, opdaterer [!INCLUDE [prod_short](includes/prod_short.md)] den matchede købsordre med de relevante modtagelsesoplysninger for at sikre, at de rigtige antal er modtaget på ordrelinjerne.

Du kan matche dine modtagne elektroniske dokumenter med købsordrelinjer fra to forskellige steder, fra siden **E-dokumenter** eller fra siden **Købsordre**. Den nemmeste måde at finde de allerede sammenkædede **købsordrer** på er at bruge feltet **Sammenkædede købsordrer** som en del af **e-dokumentaktiviteter**. Alle ikke-sammenkædede dokumenter kan findes ved hjælp af feltet **Venter på købs-e-fakturaer**, hvor du har en liste over **e-dokumenter**, du skal gennemse.  

> [!NOTE]
> **E-dokumentaktiviteter** med disse to felter findes i følgende rollecentre: **Evaluering af forretningschef**, **Forretningschef**, **Bogholder**, **Lagerchef** og **Levering og modtagelse**.

Når du vil køre matchning fra købsordren, skal du vælge handlingen **Tilknyt e-dokumentlinjer**, som findes på både købsordre- og indkøbsordrelistesiderne. Men hvis du vil køre matchning fra siden **E-dokumenter**, skal du vælge handlingen **Match købsordre** på denne side. Udfør disse trin for at fuldføre processen:

1. Vælg handlingen **Tilknyt e-dokumentlinjer** eller **Match købsordre** for allerede sammenkædede dokumenter.  
2. Du kan bemærke, at **E-dokument match ordrelinjer med Copilot-prompten** fungerer, og du har siden **Købsordrematchning** i baggrunden. Det betyder, at den samme proces sker, men med automatisk support fra **Copilot**, som kører processen med at matche i stedet for dig. 
3. Efter et par sekunder vil **E-dokument match ordrelinjer med Copilot** foreslå linjer til matchning med nogle yderligere detaljer: 

    1. Du kan finde følgende oplysninger i prompthovedet: 

    |Feltnavn |Beskrivelse |
    |--------|-----------------|
    |Automatisk matchet | Angiver antallet af matches, der foreslås automatisk. Dette er baseret på en strengsammenligning, og hvis der er 80 % eller flere beskrivelser, der overlapper hinanden, matcher systemet automatisk disse beskrivelser uden at bruge GPT-funktioner. |
    |Copilot matchet | Angiver antallet af matches, der er foreslået af Copilot, ved hjælp af både streng- og semantisk sammenligning. |
    |E-dokumentnr. | Angiver det linkede e-dokumentnummer. |
    |Fakturatotal ekskl. moms | Angiver det samlede fakturabeløb, ekskl. moms. |
    |Matchet totalbeløb inkl. moms | Angiver det matchede beløb ekskl. moms. |
    
    2. Hvis alle linjer er matchet, kan du se den grønne tekst i øverste højre hjørne: **Alle linjer (100 %) er matchede. Gennemgå matchforslag**.  
    3. Du kan finde følgende oplysninger i **Matchet forslag**-linjerne:  

    |Feltnavn |Beskrivelse |
    |--------|-----------------|
    |E-dokumentlinjenr. | Angiver e-dokumentlinjenummeret (fra den oprindelige e-dokumentfil). |
    |Beskrivelse af e-dokumentlinje | Angiver e-dokumentlinjebeskrivelsen (fra den oprindelige e-dokumentfil). |
    |Matchet antal | Angiver det antal, der skal anvendes på købsordrelinjen. |
    |Tilbud | Angiver den handling, der foreslås af AI, og disse foreslåede handlinger er relateret til matchning af købsordrelinjerne. |

    4. Alle fuldt foreslåede og matchede linjer er markeret med grøn farve. Hvis der er et problem, f.eks. en anden pris, men i det tilladte prisinterval, markeres denne linje som gul, og hvis der er lighed mellem beskrivelsesfelterne, men prisforskellen er større end tilladt, markeres denne linje som rød. 
    5. Hvis du ikke er tilfreds med nogle forslag, kan du slette dem ved hjælp af handlingen **Slet linje**.  
    6. Hvis du vil se matchning af forslag, kan du vælge linket i kolonnen **Forslag** for at åbne siden **Oplysninger om e-dokumentmatch**. 
    7. På siden **E-dokumentmatchdetaljer** kan du sammenligne detaljer fra **E-dokumenter** og **købsordren** for at være sikker på den foreslåede matchning, før du bekræfter den. 
    8. Luk siden efter gennemgang.   

4. Hvis du ikke er tilfreds med de fleste af forslagene, eller hvis du ikke vil bruge **E-dokument match ordrelinjer med Copilot-funktionen**, skal du vælge **Kassér den**, hvorefter du kan fortsætte med den [manuelle matchning](finance-how-use-edocuments-purchase.md).  
5. Hvis du vil beholde forslag, skal du vælge knappen **Behold det**, og systemet gemmer alle forslag fra **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lukker Copilot-prompten, og linjerne på siden **Matchning af købsordre** markeres som grønne, da de allerede er matchet.  
7. Fra dette øjeblik kan du fortsætte med at arbejde, mens du foretager manuel matchning, og det betyder, at du kan fjerne matches, manuelle matches, nulstille matchning, eller hvis der ikke er nogen ændringer, du vil foretage, skal du bare vælge handlingen **Anvend på købsordre** og fortsætte med at arbejde med **købsordren**. 

> [!NOTE]
> Du kan også vælge handlingen **Match med Copilot** på siden **Matchning af købsordre** igen, men i dette tilfælde bliver du spurgt, om du vil overskrive de eksisterende matches, da alle linjer allerede er matchet.  

> [!NOTE]
> Analyse af pris/omkostninger og kontrol af tilgængeligt antal er en del af forbehandlingen. 

## Se også

[Oversigt over e-dokumenter](finance-edocuments-overview.md)    
[Brug e-dokumenter i salg](finance-how-use-edocuments.md)    
[Brug e-dokumenter i køb](finance-how-use-edocuments-purchase.md)   
[Fejlfinde Copilot- og AI-funktioner](ai-copilot-troubleshooting.md)    
[Ofte stillede spørgsmål om ansvarlig AI til hjælp til bankafstemning](faqs-bank-reconciliation.md)    
