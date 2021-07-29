---
title: Rydde op i data med opbevaringspolitikker | Microsoft Docs
description: Du kan angive, hvor ofte du vil slette bestemte datatyper.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delete, data, retention, policy, policies
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 3ee0149461730e20e996f31dc7175ff3325bceca
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443914"
---
# <a name="define-retention-policies"></a>Definere opbevaringspolitikker
Administratorer kan definere opbevaringspolitikker for at angive, hvor ofte [!INCLUDE[prod_short](includes/prod_short.md)] skal slette forældede data i tabeller, der indeholder logposter og poster, der er arkiveret. Hvis du f.eks. rydder poster i logfilen, bliver det nemmere at arbejde med de data, der rent faktisk er relevante. Politikker kan omfatte alle data i de tabeller, der ligger ud over udløbsdatoen, eller du kan tilføje filterkriterier, som kun skal indeholde bestemte udløbne data i politikken. 

## <a name="required-setups-and-permissions"></a>Krævede opsætninger og tilladelser
Før du kan oprette med opbevaringspolitikker, skal du angive følgende.

|Installation  |Description  |
|---------|---------|
|**Tilladte tabeller**     |Der er en liste over de tabeller, der kan inkluderes i opbevaringspolitikkerne. Hvis du vil føje tabeller fra en filtype til en opbevaringspolitik, skal udvikleren imidlertid føje deres tabeller til listen. Du kan finde flere oplysninger i [Herunder din udvidelse i en opbevaringspolitik](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Opbevaringsperioder**     |Angive perioder, hvor der skal være data i tabellerne i en politik. Perioderne bestemmer, hvor ofte data vil blive slettet.         |

Derudover skal du have tilladelse som SUPER-bruger eller til opsætning af opbevaringspolitik. Brugere, der har fået tildelt tilladelsen til opsætning af tilbageholdelsespolitik, kan definere opbevaringspolitikker for tabeller, selvom de ikke har læse-og slette tilladelser til tabellerne. Opgavekøposten skal køre som en bruger med tilladelse til at læse og slette dataene. Det anbefales, at du ikke tildeler tilladelsen opsætning af opbevaringspolitik som angivet for brugere, som ikke skal have tilladelse til at slette data.

> [!NOTE]
> Hvis du bruger [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, og du vil afprøve opbevaringspolitikkerne i CRONUS-demonstrationsdatabasen, er der et par ting, du skal gøre. Demonstrationsregnskabet indeholder ikke tabeller, som du kan bruge med opbevaringspolitikker, så du skal tilføje dem. Hvis du vil gøre dette, skal du oprette et nyt tomt regnskab i demonstrationsdatabasen. Importér den RapidStart-konfigurationspakke, der svarer til standard NAV17.0.W1.ENU.STANDARD.rapidstart-pakken, i det nye regnskab. Konfigurationsdataene for opbevaringspolitikker vil være tilgængelige i det nye regnskab.

### <a name="to-create-retention-periods"></a>Sådan oprettes opbevaringsperioder
Opbevaringsperioderne kan være så lange eller korte, som du har lyst til. Hvis du vil oprette opbevaringsperioder på siden **Opbevaringspolitikker**, skal du bruge handlingen **Opbevaringsperiode**. De perioder, du definerer, er tilgængelige for alle politikker.

> [!NOTE]
> Af hensyn til kompatibiliteten har vi defineret en mindste opbevaringsperiode for nogle tabeller. Hvis du angiver en opbevaringsperiode, der er kortere end minimumkravet, viser en meddelelse den obligatoriske periode.

### <a name="set-up-a-retention-policy"></a>Opsæt opbevaringspolitik
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Opbevaringspolitikker**, og vælg derefter det relaterede link.
2. I feltet **Tabel-id** skal du vælge den tabel, du vil medtage i politikken.
3. I feltet **Opbevaringsperiode** skal du angive, hvor længe dataene i tabellen skal være.
4. Valgfrit: Hvis du vil anvende politikken på specifikke data i en tabel, skal du slå funktionen Anvend på alle poster fra. Oversigtspanelet til opbevaring af oplysninger vises, hvor du kan angive filtre for at oprette datasæt for hver linje. Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Hver linje har sin egen opbevaringsperiode. Hvis du angiver forskellige opbevaringsperioder for de samme data, bruges den længste periode. Nogle tabeller indeholder også filtre, som du ikke kan ændre eller fjerne. Som en hjælp til at identificere disse filtre vises de med farven lysere skrifttype.

## <a name="applying-retention-policies"></a>Anvende opbevaringspolitikker
Du kan bruge en Opgavekøpost til at anvende opbevaringspolitikker til at slette data automatisk, eller du kan anvende politikker manuelt.

Hvis du vil anvende en opbevaringspolitik automatisk, skal du blot oprette og aktivere en politik. Når du aktiverer en politik, opretter vi en Opgavekøpost, som anvender opbevaringspolitikker i overensstemmelse med den angivne opbevaringsperiode. Alle opbevaringspolitikker benytter den samme Opgavekøpost. Som standard anvender opgavekøposten politikken hver dag kl. 0200. Du kan ændre standardindstillingen, men hvis du gør det, anbefales det at køre uden for normal arbejdstid. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md). 

Du kan anvende en politik manuelt vha handlingen **Anvend manuelt** på siden **Opbevaringspolitikker**. Hvis du altid vil anvende en politik manuelt, skal du aktivere den **Manuelt**. Opgavekøposten ignorerer politikken, når den kører.

## <a name="viewing-retention-policy-log-entries"></a>Se logførte poster for opbevaringspolitikker
Se aktivitet, der er relateret til opbevaringspolitikker, på siden **Opbevaringspolitiklog**. Der oprettes f.eks. poster, når der anvendes en politik, eller hvis der opstod fejl, når det skete. 

## <a name="including-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Medtage din udvidelse i en opbevaringspolitik (kræver hjælp fra en udvikler)
Opbevaringspolitikker dækker som standard kun tabeller, der er medtaget på den liste over [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller, som vi yder. Du kan fjerne standardtabeller fra listen, og du kan tilføje tabeller, som du ejer. Det vil sige, at du ikke kan tilføje en tabel, som du ikke selv har oprettet. Du kan f.eks. ikke tilføje andre tabeller fra [!INCLUDE[prod_short](includes/prod_short.md)] eller fra en udvidelse, du har købt.

Hvis du vil føje tabeller til listen over tilladte tabeller, skal en udvikler tilføje en kode, f.eks. codeunit til installationsprogrammet til udvidelsen (en codeunit med undertypen *Installation*). 

Når en udvikler tilføjer en tabel, kan de angive obligatoriske og standardfiltre. Obligatoriske filtre kan ikke fjernes eller ændres senere, når du tilføjer tabeller for at definere en opbevaringspolitik. Standardfiltre er blot brugervenlige forslag.

I det følgende finder du eksempler på, hvordan du kan føje en tabel til listen over tilladte tabeller med og uden obligatorisk eller standardfiltre. Hvis du vil have et mere komplekst eksempel, skal du se codeunit 3999 "Reten. Pol. Installation - BaseApp". 

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Følgende eksempel indeholder et obligatorisk filter.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Når en udvikler har føjet tabeller til listen, kan en administrator medtage dem i en opbevaringspolitik. 

## <a name="see-also"></a>Se også

[Analyse af Retention Policy Trace Telemetry](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Ændringer af revision i Business Central](across-log-changes.md)  
[Filtrering](ui-enter-criteria-filters.md#filtering)  
[Du kan bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]