---
title: Automatisering af rykker i opkrævninger
description: 'I denne artikel forklares det, hvordan du sparer tid i rykkere ved at automatisere processen med oprettelse, udstedelse og afsendelse af rykkere til kunder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="automate-reminders-in-collections"></a>Automatisering af rykker i opkrævninger

Gør dine rykkere mere effektive ved at automatisere processen med oprettelse, udstedelse og afsendelse af rykkere til kunder. Automatisering kan reducere den tid, du bruger på samlinger, give et bedre overblik over processen og give dig fuld kontrol over hvert trin.

På siden **Automatisering af rykkere** definerer du de enkelte handlinger (trin). Du kan kombinere trinnene til oprettelse, udstedelse og afsendelse af påmindelser, eller du kan oprette en separat automatisering for hvert trin, hvis det er bedre for dine indsamlingsprocesser. Automatiseringer er baseret på rykkerbetingelser og rykkerniveauer. Hvis du vil vide mere om rykkere, skal du gå til [Konfigurere rykkerbetingelser og -niveauer](finance-setup-reminders.md). Du kan angive filtre for rykkerbetingelser for en automatisering som helhed og angive filtre for hver handling i automatiseringen. Du kan også vedhæfte udestående fakturaer til e-mails som PDF-filer.

Automatisering sker via en opgavekøpost. Når du konfigurerer en automatisering, skal du bruge feltet **Kadence** til at angive, angive, hvordan og hvornår den kører. Hvis du vælger **Manuel**, køres automatiseringen én gang, når du bruger handlingen **Start**. Du kan også vælge **Ugentligt**, **Månedligt** eller vælge **Brugerdefineret** for at konfigurere en mere detaljeret kadence. Hvis du vælger **Brugerdefineret**, skal du angive en dataformel. Du kan få mere at vide om angivelse af en datoformel ved at gå til [Brug datoformler](ui-enter-date-ranges.md#use-date-formulas). Når du vælger en anden indstilling end **Manuel**, kører automatiseringen, indtil du sætter den på pause for at sætte den i venteposition. Hvis du vil være endnu mere specifik med, hvornår kørslen kører, kan du bruge handlingen **Opgavekøposter** til at åbne siden **Opgavekøposter** og justere gentagelsen, f.eks. til en daglig eller en bestemt ugedag.

## <a name="automate-the-reminders-flow"></a>Automatiser rykkerflowet

I følgende afsnit beskrives, hvordan du indstiller rykkere, der skal oprettes, udstedes og sendes automatisk.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Automatisering af rykkere**, og vælg derefter det relaterede link.
1. Vælg handlingen **Ny** handling, og udfyld felterne på oversigtspanelet **Generelt** efter behov.
1. Vælg den eller de rykkerbetingelser, som denne automatisering skal bruges til, i feltet **Filter for rykkerbetingelser**.
1. Vælg, hvor ofte automatiseringen skal køres, i feltet **Kadence**.
1. Vælg **Ny** i oversigtspanelet **Handlinger**, og vælg derefter, om automatiseringen skal oprette, udstede eller sende rykkere. Klik **OK**.
1. Afhængigt af den type handling, der udføres automatiseringen, skal du udfylde felterne efter behov på opsætningssiden. Du kan få flere oplysninger om indstillingerne ved at gå til [Indstillinger for påmindelseshandlinger](#settings-for-reminder-actions).
1. Når du har konfigureret handlingerne for automatiseringen, kan du bruge handlingerne **Flyt op** og **Flyt ned** til at justere den rækkefølge, de køres i.

## <a name="settings-for-reminder-actions"></a>Indstillinger for rykkerhandlinger

Konfigurationsindstillingerne er forskellige for handlingerne Opret, Udsted og Send rykker. Følgende afsnit beskriver, hvordan du kan bruge dem.

### <a name="create"></a>Opret

* Indstil højeste niveau på alle rykkerlinjer.  
* Opret rykkere for poster, der afventer. Denne indstilling er f.eks. nyttig, hvis du er i en igangværende tvist med en kunde og gerne vil have, at kunden ser det store billede.
* Oprette rykkere for alle ubetalte fakturaer og ikke kun for forfaldne. I rapporten vises forfaldne fakturaer og fakturaer, der kun er ubetalte, men ikke forfaldne, i separate sektioner.
* Indstil filtre for at gøre påmindelsen mere specifik.

### <a name="issue"></a>Udsted

Når du udsteder en rykker, opretter du poster i debitorposten, der indeholder bogføringsdatoen og skattedatoen. Brug indstillingerne på siden **Opsætning af udstedte rykkere** til at angive, om oplysningerne på den udstedte rykker skal erstattes med oplysningerne fra den oprettede rykker. Hvis du f.eks. oprettede rykkeren i går og udsteder den i dag, flyttes forfaldsdatoen en dag.

### <a name="send"></a>Send

> [!NOTE]
> Automatiseringen Send kræver, at du har konfigureret mail i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan få mere at vide om opsætning af e-mail ved at gå til [Opsætte e-mail](admin-how-setup-email.md).

Indholdet af mails, f.eks. vedhæftede tekster, brødtekst i mails og sprog, kommer fra opsætningen af rykkerudtrykket. Hvis du vil vide mere om e-mailindstillinger, skal du gå til [Konfigurere rykkerbetingelser og -niveauer](finance-setup-reminders.md).

Brug indstillingerne på siden **Send opsætning af rykkere** til at styre følgende:

* Generelle indstillinger, f.eks. beskrivelsen, og hvor mange gange du sender den samme påmindelse.
* Indstillinger for, hvad der skal medtages i påmindelsen.
* Indstillinger for sporing af de rykkere, du sender ved at oprette interaktioner, om du udskriver eller sender rykkeren via mail, og om du kun vil vedhæfte forfaldne fakturaer, alle fakturaer eller ingen fakturaer. 

## <a name="access-the-history-of-a-reminder"></a>Få adgang til historikken for en påmindelse

[!INCLUDE [prod_short](includes/prod_short.md)] holder styr på hver gang en automatisering kører. Du kan få adgang til historikken ved at vælge handlingen **Logfør poster**. Du kan også bruge handlingen **Udstedte rykkere** til at få adgang til en liste over de rykkere, du har udstedt.

## <a name="handle-errors"></a>Håndtere fejl

I oversigtspanelet **Handlinger** kan du for hver handling angive, om automatiseringen skal stoppe, hvis der opstår en fejl i handlingen. Hvis du gør det, behandler automatiseringen ikke de handlinger, der kommer bagefter. Hvis du vil slå denne funktion til eller fra, skal du bruge handlingerne **Indstil stop ved fejl** eller **Ryd stop ved fejl**.

## <a name="change-action-settings-for-an-automation"></a>Ændre handlingsindstillinger for en automatisering

Du kan til enhver tid ændre indstillinger for en automatisering. I oversigtspanelet **Handlinger** skal du vælge **Opsætning** og derefter foretage ændringerne.

## <a name="see-also"></a>Se også

[Konfigurere rykkerbetingelser og -niveauer](finance-setup-reminders.md)  
[Sende rykkere for udestående saldi](receivables-send-reminders.md)  
