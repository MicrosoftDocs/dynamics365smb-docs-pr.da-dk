---
title: Administrere synkronisering af stamdata
description: Få mere at vide om at administrere synkronisering af stamdata
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 04/05/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# Administrere synkronisering af stamdata

Når du har oprettet stamdata og synkroniseret for første gang, er posterne i de valgte tabeller tilkoblet, og der oprettes en tilbagevendende opgavekøpost for hver tabel. Opgavekøposten synkroniserer automatisk data i datterselskaberne, når nogen foretager en ændring i kilderegnskabet. Ellers behøver du ikke foretage dig noget.

> [!NOTE]
> Opgavekøposten er som standard planlagt til kørsel hvert minut, og du kan ikke ændre tidsplanen.

Nogle gange går der ikke noget galt, og der kan være situationer, hvor du skal administrere eller undersøge. Hvis en person f.eks. ændrer samme post i både kilderegnskabet og et datterselskab, mislykkes synkroniseringen, så du kan angive den korrekte ændring. Eller kildevirksomheden installerer muligvis et filtypenavn, der ændrer skemaet i en af de tabeller, der synkroniseres, ved at tilføje et felt eller to. Hvis du vil synkronisere de nye felter i datterselskaberne, skal du installere de samme udvidelser og opdatere tabelskemaerne i deres opsætning.

I denne artikel beskrives de værktøjer, du kan bruge til at holde synkroniseringen kørende uden problemer.

## Overskriv lokale ændringer

Du kan bruge afkrydsningsfeltet **Overskriv lokal ændring** i de felter og tabeller, du synkroniserer, for at tillade, at data fra kilderegnskabet overskriver data i datterselskabet.

> [!NOTE]
> Du kan ikke aktivere synkroniseringen af et felt og tillade datterselskabet at skrive værdier i det uafhængigt af kildefirmaet. Du skal enten deaktivere synkroniseringen af feltet eller tillade, at kildefirmaet overskriver lokale ændringer.

## Opdatere tabelskemaer

Hvis kilderegnskabet ændrer en tabel, f.eks. ved at tilføje et felt, som du vil synkronisere, skal datterselskaberne opdatere felttilknytningerne. Brug handlingen **Opdater felter** på siden **synkroniseringsfelter**.

## Aktivere eller deaktivere kobling mellem poster

Hvis du vil starte eller stoppe koblingen på bestemte poster i en tabel, skal du på siden **synkroniseringsfelter** vælge felterne og enten bruge **Aktiver** eller **Deaktiver** .

> [!TIP]
> Du kan hurtigt aktivere eller deaktivere flere felter på én gang ved at markere dem på listen og derefter bruge handlingerne **Aktiver** eller **Deaktiver**.

## Kør en fuld synkronisering

Handlingen **Udfør fuld synkronisering** planlægger en synkronisering for alle tabelposter i kildevirksomheden og gensynkroniserer alle poster betingelsesløst. Gensynkronisering er f.eks. nyttig, hvis du aktiverer et ekstra felt i en synkroniseringstabel eller tilføjer et ekstra felt ved hjælp af handlingen **Opdater felter**. Handlingen synkroniserer dataene i disse felter med tilbagevirkende kraft.

## Synkroniser tilpassede poster

Hvis du ændrer en indstilling for en tabel eller et felt i et datterselskab, skal du opdatere synkroniseringen. Hvis du vil opdatere synkroniseringen, skal du bruge handlingen **Synkroniser ændrede poster** på siden **synkroniseringstabeller**.

Handlingen **Synkroniser ændrede poster** planlægger en synkronisering af følgende tabelposter:

* Poster, der ikke kunne synkroniseres i sidste forsøg.
* Poster, der er blevet ændret i kilderegnskabet efter sidste planlagte synkronisering. Du kan gennemse det sidste planlagte synkroniseringstidspunkt på siden **Synkroniseringstabeller** i feltet **Synkroniser ændringer siden**.

Handlingen fungerer på samme måde som en planlagt synkronisering, og du kan bruge den som en metode til synkronisering uden for tidsplanen. Hvis du f. eks. vælger at markere afkrydsningsfeltet **Overskriv lokal ændring** i et felt for at tillade, at data fra kilderegnskabet overskriver lokale ændringer, opdaterer handlingen disse data. Du kan også bare vente, indtil den næste planlagte synkronisering sker.

## Undersøge status for synkronisering

Der er to handlinger på siden **Synkroniseringstabeller**, som kan være en hjælp til at overvåge synkroniseringen:

* **Integrationsynkroniseringsjob**
* **Opgavekøposter**

Den følgende tabel beskriver handlingerne.

|Side  |Beskrivlse  |
|---------|---------|
|**Integrationsynkroniseringsjob**     | Åbne siden **integrationssynkroniseringsjob** for at undersøge, hvad der skete, hver gang en opgavekøpost kørte. Hvis du vil finde mere detaljerede oplysninger om nye poster, der er blevet tilføjet, eller se, hvorfor en post ikke kunne synkroniseres, skal du vælge tallene i de **Indsatte** eller **Mislykkede** kolonner. Du kan også bruge denne side til at rydde op i ældre poster, som du muligvis ikke har brug for. Du kan få mere at vide om oprydning ved at gå til [Rense famle poster](#clean-up-old-entries).        |
|**Opgavekøposter**     | Få adgang til oplysninger om opgavekøposten, der synkroniserer data for en valgt tabel. Brug denne side til at administrere status for opgavekøposten, og du kan lære mere om Opgavekøposter i [Brug opgavekøer for at planlægge opgaver](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Hvis du finder en fejl på siden **integrationssynkroniseringsjob**, som du ikke kan løse, skal du, hvis du kontakter din partner eller Microsoft for support, få fejlmeddelelsen og oplysninger om callstack.

## Rydde op i gamle poster

Med tiden vil antallet af poster i synkroniseringsloggen være større, så du kan evt. Housekeeping fjerne unødvendige poster. Når du vil gøre det nemmere at rydde op i gamle poster, kan du bruge siden **Integrationssynkroniseringsjobs** til følgende:

* **Slet poster ældre end syv dage**
* **Slet alle poster**

## Tilføje udvidelser

Hvis kilderegnskabet installerer et nyt filtypenavn, skal datterselskabet også installere det, hvis det vil synkronisere dataene for det. Datterselskabet kan bruge handlingen **Opdater felter** på siden **Synkroniseringsfelter** til at føje tabellerne fra udvidelsen til listen.

> [!NOTE]
> Nogle tabeller henter data fra relaterede tabeller. Hvis du tilføjer et filtypenavn, der ikke indeholder relaterede tabeller, vil felterne i disse tabeller ikke være tilgængelige. Kontroller, at du har tilføjet alle relaterede tabeller.

<!--
## Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## Se også

[Gør dig klar til at synkronisere stamdata](admin-set-up-data-sync.md)
