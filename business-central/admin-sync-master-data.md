---
title: Administrere synkronisering af stamdata
description: Få mere at vide om at administrere synkronisering af stamdata
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization" />Administrere synkronisering af stamdata

Når du har oprettet stamdata og synkroniseret for første gang, er posterne i de valgte tabeller tilkoblet, og der oprettes en tilbagevendende opgavekøpost for hver tabel. Opgavekøposten synkroniserer automatisk data i datterselskaberne, når nogen foretager en ændring i kilderegnskabet. Ellers behøver du ikke foretage dig noget.

> [!NOTE]
> Opgavekøposten er som standard planlagt til kørsel hvert minut, og du kan ikke ændre tidsplanen.

Nogle gange går der ikke noget galt, og der kan være situationer, hvor du skal administrere eller undersøge. Hvis en person f.eks. ændrer samme post i både kilderegnskabet og et datterselskab, mislykkes synkroniseringen, så du kan angive den korrekte ændring. Eller kildevirksomheden installerer muligvis et filtypenavn, der ændrer skemaet i en af de tabeller, der synkroniseres, ved at tilføje et felt eller to. Hvis du vil synkronisere de nye felter i datterselskaberne, skal du installere de samme udvidelser og opdatere tabelskemaerne i deres opsætning.

I denne artikel beskrives de værktøjer, du kan bruge til at holde synkroniseringen kørende uden problemer.

## <a name="investigate-the-status-of-synchronization" />Undersøge status for synkronisering

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

## <a name="synchronize-modified-records" />Synkroniser tilpassede poster

Hvis du ændrer en indstilling for en tabel eller et felt i et datterselskab, skal du opdatere synkroniseringen. Hvis du f. eks. vælger at markere afkrydsningsfeltet **Overskriv lokal ændring** i et felt for at tillade, at data fra kilderegnskabet overskriver lokale ændringer. Hvis du vil opdatere synkroniseringen, skal du bruge handlingen **Synkroniser ændrede poster** på siden **synkroniseringstabeller**.

## <a name="update-table-schemas" />Opdatere tabelskemaer

Hvis kilderegnskabet ændrer en tabel, f.eks. ved at tilføje et felt, som du vil synkronisere, skal datterselskaberne opdatere felttilknytningerne. Brug handlingen **Opdater felter** på siden **synkroniseringsfelter**. 

## <a name="enable-or-disable-couplings-between-records" />Aktivere eller deaktivere kobling mellem poster

Hvis du vil starte eller stoppe koblingen på bestemte poster i en tabel, skal du på siden **synkroniseringsfelter** vælge felterne og enten bruge **Aktiver** eller **Deaktiver** . 

> [!TIP]
> Du kan hurtigt aktivere eller deaktivere flere felter på én gang ved at markere dem på listen og derefter bruge handlingerne **Aktiver** eller **Deaktiver**.

## <a name="adding-extensions" />Tilføje udvidelser

Hvis kilderegnskabet installerer et nyt filtypenavn, skal datterselskabet også installere det, hvis det vil synkronisere dataene for det. Datterselskabet kan bruge handlingen **Opdater felter** på siden **Synkroniseringsfelter** til at føje tabellerne fra udvidelsen til listen.

> [!NOTE]
> Nogle tabeller henter data fra relaterede tabeller. Hvis du tilføjer et filtypenavn, der ikke indeholder relaterede tabeller, vil felterne i disse tabeller ikke være tilgængelige. Kontroller, at du har tilføjet alle relaterede tabeller.

## <a name="clean-up-old-entries" />Rydde op i gamle poster

Med tiden vil antallet af poster i synkroniseringsloggen være større, så du kan evt. Housekeeping fjerne unødvendige poster. Når du vil gøre det nemmere at rydde op i gamle poster, kan du bruge siden **Integrationssynkroniseringsjobs** til følgende:

* **Slet poster, som er ældre end 7 dage**
* **Slet alle poster**

<!--
## <a name="recreate-a-deleted-job-queue-entry" />Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also" />Se også

[Gør dig klar til at synkronisere stamdata](admin-set-up-data-sync.md)
