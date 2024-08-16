---
title: Spore vareprisreguleringer
description: 'Få mere at vide om, hvordan sporingsreguleringer af varepriser kan hjælpe dig med at holde dine varepriser nøjagtige.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 07/30/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Spore vareprisreguleringer

Det er vigtigt at holde vareomkostningerne nøjagtige og forkorte tiden mellem det tidspunkt, hvor du bogfører en post, og det tidspunkt, hvor finansbogholderiet afspejler prisen. Du kan spore resultaterne af omkostningsreguleringer for individuelle reguleringskørsler og varer. Hvis der opstår fejl, kan du identificere de varer, der har problemer, og foretage rettelser. Du kan f.eks. udelukke varerne fra beregningerne for at sikre, at reguleringerne ikke afbrydes for andre varer. Du kan regulere omkostningerne for enkelte varer eller oprette varekørsler og regulere dem alle på én gang.

## Begynd at spore omkostningsreguleringer

Det er nemt at komme i gang. På siden **Lageropsætning** indeholder feltet **Logføring af omkostningsregulering** et par indstillinger:

* **Deaktiveret** betyder, at du ikke logfører kørsler af omkostningsreguleringer.
* **Kun fejl** betyder, at du kun logger kørsler, der mislykkedes.
* **Alle** betyder, at alle kørsler logges.

> [!NOTE]
> For at minimere størrelsen på loggen logføres de reguleringer, der sker automatisk, ikke i [!INCLUDE [prod_short](includes/prod_short.md)], når nogen bogfører et element.

Du skal også konfigurere opgavekøposten **Bogfør lagerregulering til Finans (1002)**. Denne opgavekøpost regulerer automatisk omkostningerne i henhold til en plan. Få mere at vide om poster på opgavekøer i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## Håndtere omkostningsreguleringer

Brug siden **Regulering af lageromkostninger** til at administrere og overvåge omkostningsreguleringsprocessen. På denne side vises varer sammen med deres omkostningsparametre og status for omkostningsregulering. Du kan filtrere listen for at fokusere på varer, der kræver regulering, eller som ikke er medtaget i omkostningsreguleringen.

### Om varebatches

Du kan foretage omkostningsregulering for flere varer ved at gruppere dem i batches. Batches gør det nemt at regulere nogle varer separat, f.eks. fordi det tager længere tid at regulere dem. Batches kan også hjælpe med at identificere varer, der er problemer med.

Hvis du vil oprette en batch, skal du benytte en af følgende fremgangsmåder på siden **Regulering af lageromkostninger**:

* Vælg varerne på listen, vælg **Kør omkostningsregulering**, og vælg derefter **Tilføj batch**.
* Hvis du vil oprette en batch og udføre omkostningsregulering med det samme, skal du markere varerne på listen, vælge **Kør omkostningsregulering** og derefter vælge **Tilføj batch og kør**.
* Vælg **Kør omkostningsregulering**, vælg **Varebatches**, og angiv derefter et filter i feltet **Varefilter**.
  
> [!TIP]
> Hvis du hurtigt vil oprette en ny batch for alle varer, der ikke allerede er inkluderet i en batch, skal du vælge **Tilføj manglende varer** på siden **Kostregulering – Varepartier**.

Når en kørsel for en batch afsluttes, har batchen én af følgende statusser på siden **Varenavne**:

* **Fuldført**: Omkostningsreguleringen lykkedes.
* **Mislykket**: Hvis omkostningsreguleringen mislykkes, identificeres [!INCLUDE [prod_short](includes/prod_short.md)] den vare, der forårsagede fejlen, og den aktuelle batch opdeles derefter i to. En batch med den problematiske vare og en anden med de øvrige varer. Omkostningsregulering køres igen for batchen med de resterende varer. Hvis det mislykkes igen, gentages processen. Du definerer det maksimale antal opdelinger i feltet **Maks. antal nye forsøg**. Standardværdien for nye forsøg er 10, men du kan angive en ny grænse.
* **Timeout**: Hvis omkostningsreguleringen for en batch ikke afsluttes inden for den periode, der er angivet i feltet **Timeout (minutter)** (fra 1 til 720 minutter), afsluttes sessionen, og ændringerne annulleres. [!INCLUDE [prod_short](includes/prod_short.md)] opdeler derefter den aktuelle batch i to og kører omkostningsreguleringsprocessen for hver halvdel igen. Denne proces fortsætter, indtil omkostningsreguleringen er fuldført eller når det maksimale antal nye forsøg.

> [TIP!] Hver batch kører i en separat session. Hvis du vil overvåge status, skal du bruge handlingen **Opdater**.

### Kør omkostningsregulering

Brug siden **Regulering af lageromkostninger** til at foretage reguleringer.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Regulering af lageromkostninger**, og vælg derefter det relaterede link.
1. Afhængigt af hvad du vil gøre, skal du bruge en af følgende muligheder:

  * For en eller flere varer skal du straks markere elementerne på listen og derefter vælge **Kør omkostningsregulering**.
  * For batches kan du bruge en af følgende muligheder:

    * Hvis du vil oprette en batch og regulere omkostninger med det samme, skal du vælge varerne på listen, vælge **Kør omkostningsregulering** og derefter vælge **Tilføj batch og kør**.
    * Hvis du vil køre den for alle batches, skal du vælge **Kør omkostningsregulering**, **Varebatches** og derefter vælge **Kør**.
    
    Du kan få mere at vide om batches ved at gå til [Om varebatches](#about-item-batches).

### Udforske varedetaljer

Brug menuen **Vare** til at få adgang til oplysninger om omkostningsreguleringer for en valgt vare.

* **Vareposter**: Vis vareposter for varen. Med handlingen **Markér til regulering** kan du gennemtvinge en ny kørsel af omkostningsregulering for varer, der er direkte eller indirekte knyttet til de indgående poster, du vælger. Det kan være nyttigt at gennemtvinge en ny kørsel, hvis tidligere kørsler har ført til forkerte omkostninger.
* **Værdiposter**: Vis værdiposter for varen.
* **Indgangspunkter til omkostningsregulering**: Åbn siden **Indf.sted, regl. gnsn. kostpr.**, som du primært bruger til at beregne den gennemsnitlige kostpris. Siden viser kombinationer af varer, lokationer, varianter og værdiansættelsesdatoer, hvor der er kørt eller skal køres omkostningsreguleringer.
* **Ordrer til omkostningsregulering**: Åbn siden **Indtastningsordre til lagerregulering**, hvor du kan regulere produktions- og montageordrer. Den viser, at ordrerne er justeret eller skal justeres.

### Få vist resultatet

Brug menuen **Log pr.** til at få vist resultatet af omkostningsreguleringer:

* **Kør**: Vis logfiler over omkostningsregulering for hver kørsel. Loggen indeholder data om varefilter, status (Fuldført/Mislykket/Timeout), start- og slutdato/-klokkeslæt, varighed og de omkostningsforskelle, der er opstået som følge af kørslen.
* **Vare**: Vis detaljerede oplysninger om reguleringsprocessen for den valgte vare.

### Medtag eller udelad varer fra reguleringer

Hvis der er fejl i en eller flere varer, kan du udelade varerne fra reguleringskørslen og derefter medtage dem i senere kørsler. Vælg en af følgende i menuen **Funktioner**:

* **Udeluk vare fra regulering** og **Medtag element i regulering**: Midlertidigt deaktivere og derefter genaktivere kostregulering for en valgt vare. Omkostningsregulering fortsætter med at holde omkostningerne nøjagtige for andre varer, mens du undersøger et problem med en bestemt vare.

## Bogføre regulerede kostpriser i finansbogholderiet

Nye værdiposter bogføres typisk i finansbogholderiet i overensstemmelse med tidsplanen for opgavekøposten **Bogfør lagerregulering til Finans (1002)**. Du kan dog bogføre reguleringer i finansbogholderiet med det samme fra siden **Regulering af lageromkostninger**. I menuen **Funktioner** skal du vælge **Bogfør lagerregulering til Finans**.

## Fejlfinding af omkostningsreguleringer

Brug følgende indstillinger i menuen **Diagnostik** til at foretage fejlfinding af kørsler af omkostningsreguleringer.

* **Eksportér varedata**: Eksportér varerelaterede data til en tekstfil. Du kan bruge filen til yderligere analyse i et sandkassemiljø eller vedhæfte den til en supportanmodning, når du undersøger problemer med beregning af omkostninger.
* **Importer varedata**: Importer den tidligere eksporterede tekstfil tilbage til databasen. Denne handling er kun aktiveret i sandkassemiljøer eller evalueringsfirmaer.
* **Nulstil kostpris er reguleret**: Nulstil til/fra-knappen **Omkostningen er reguleret** for varer, produktionsordrer eller montageordrer. Med denne indstilling kan du gennemtvinge en ny kørsel af omkostningsreguleringen for dem.
* **Rapporten** Registrering af kostprisproblemer: Diagnosticer typiske dataproblemer, der forårsager beregningsfejl i kostberegningen. Det kontrolleres, om vareposter, værdiposter, vareudligningsposter og kapacitetsposter er korrekte.
* **Slet varedata**: Ryd alle varerelaterede tabeller i databasen. Denne handling er kun tilgængelig i sandkassemiljøer eller evalueringsfirmaer.

## Se også

[Justere varepriser](inventory-how-adjust-item-costs.md)  
[Designoplysninger: Beregningsregulering](design-details-cost-adjustment.md)  
