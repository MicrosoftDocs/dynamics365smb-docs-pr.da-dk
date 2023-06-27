---
title: Søgning efter kontakter fra Microsoft Teams
description: 'Få mere at vide om, hvordan du kan søge efter Business Central-debitorer, -kreditorer og andre kontakter fra Microsoft Teams.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/12/2021
ms.author: jswymer
---

# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams" />Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]. Introduceret i 2021 udgivelsesbølge 1.

[!INCLUDE [prod_short](includes/prod_short.md)] har et omfattende system til styring af virksomhedskontakter, som er afgørende for brugere inden for salg, drift eller andre afdelinger. Hvis du bruger en af disse roller, er du ofte nødt til at søge efter, mødes med eller starte en samtale med dine kreditorer, debitorer og andre kontakter. Med appen [!INCLUDE [prod_short](includes/prod_short.md)] til Teams kan du udføre disse opgaver direkte fra Teams uden at skulle skifte til [!INCLUDE [prod_short](includes/prod_short.md)]. I Teams kan du:

- Søge efter [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter fra Teams-kommandoboksen eller meddelelsesområdet. Kontakter kan omfatte kundeemner, kreditorer, debitorer eller andre virksomhedsrelationer.
- Dele en kontaktperson som et kort i en Teaks-samtale.
- Få vist detaljer om kontakt, interaktionshistorik og anden indsigt som f.eks. udestående betalinger eller åbne dokumenter.

## <a name="prerequisites" />Forudsætninger

- Du har adgang til Microsoft Teams.
- Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Du kan finde flere oplysninger i [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-konto med adgang til kontakter i mindst én virksomhed.

> [!NOTE]
> Hvis du søger fra kommandoboksen eller meddelelsesboksen, kan du blive bedt om at logge på eller konfigurere appen første gang. Dette trin er nødvendigt, hvis du vil søge efter kontakter i den rette Business Central-virksomhed. Du kan finde oplysninger om, hvordan du konfigurerer appen til at vælge virksomheden, i [Skift af regnskab og andre indstillinger i Teams](across-teams-settings.md).

## <a name="look-up-contacts-from-the-command-box" />Søge efter kontakter fra kommandoboksen

Kommandoboksen er placeret øverst i alle skærmbilleder i Teams. Det gør det muligt at søge efter, udføre hurtige handlinger eller starte apps som f.eks. appen [!INCLUDE [prod_short](includes/prod_short.md)]. Søgning fra kommandoboksen er perfekt til hurtig søgning efter kontakter og deres relaterede data til egen brug. Antag f.eks., at du vil søge efter en mailadresse for en leverandør for at oprette et kalendermøde. Eller måske vil du søge efter interaktionshistorikken under et møde med en kunde.

1. Skriv **@Business Central** i kommandoboksen, og vælg derefter Business Central-appen fra resultaterne.

    ![Åbn Business Central-appen for at søge efter kontakter fra kommandoboksen.](media/teams-contacts-command-1.png)

2. Begynd at indtaste søgetekst som f.eks. et navn, en adresse eller et telefonnummer i boksen **Business Central**.

    Mens du indtaster, vises matchende resultater.

    ![Søge efter Business Central-kontakter fra kommandoboksen i Teams.](media/teams-contacts-command-2.png)
3. Vælg en kontakt fra resultaterne.

    Kontaktkortet vises under kommandoboksen.

4. Hvis du vil føje et kontaktkort til en samtale, skal du gå til øverste højre hjørne af kortet og vælge **... (Flere indstillinger)** > **Kopiér**. Indsæt derefter kopien i meddelelsesboksen til en samtale.  

Du kan finde generelle oplysninger om kommandoboksen i Teams i [Teams - Bruge kommandoboksen](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## <a name="look-up-contacts-from-the-message-compose-box" />Søge efter kontakter fra meddelelsesboksen

Fordelen ved at bruge meddelelsesboksen er, at du kan tilføje et kontaktkort direkte til en samtale, så andre kan se det.

1. Vælg ikonet for **Business Central** for at starte appen under meddelelsesboksen.

    Hvis du ikke kan se ikonet for **Business Central**, skal du vælge **... (Meddelelsesudvidelser)**.

    ![Åbn Business Central-appen for at søge efter kontakter fra meddelelsesboksen.](media/teams-contacts-message-box.png)

2. Begynd at indtaste søgetekst som f.eks. et navn, en adresse eller et telefonnummer i boksen **Business Central**.

    Mens du indtaster, vises matchende resultater.

    ![Søge efter Business Central-kontakter fra meddelelsesboksen.](media/teams-contacts-5.png)
3. Vælg en kontakt fra resultaterne.

    Kontaktkortet vises i meddelelsesboksen.

    > [!NOTE]
    > Kontaktkortet sendes ikke med det samme til samtalen, hvor andre kan se det. Du har mulighed for at gennemgå indholdet af kortet og tilføje tekst efter ønske før og efter det er sendt. Send derefter meddelelsen til chatten, når du er klar.

### <a name="heres-another-way" />En anden metode

1. I stedet for at bruge ikonet for **Business Central** skal du skrive **@Business Central** direkte i meddelelsesboksen.
2. Indtast dine søgeord i feltet.
3. Brug piletasterne Op og Ned på tastaturet til at vælge en kontakt, og tryk derefter på <kbd>Enter</kbd> for at vælge kontakten.

## <a name="viewing-contact-card-details" />Visning af oplysninger fra visitkort

Kontaktkortet i Teams giver dig et hurtigt overblik over debitoren, kreditoren eller kontaktpersonen. Kortet er interaktivt&mdash;hvilket betyder, at du kan få vist flere oplysninger eller ændre en kontakt ved hjælp af knapperne **Detaljer** eller **Pop-op**.

Knappen **Detaljer** åbner et vindue i Teams med flere oplysninger om kontakten, men ikke så mange oplysninger som i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil se alle oplysninger om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)], skal du vælge **Pop-op**.

Kontaktkortet fungerer på samme måde som kort for poster, f.eks. varer, debitorer eller salgsordrer. Du kan finde flere oplysninger om kort i [Vise kortoplysninger](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Alle deltagerne i en Teams-samtale kan få vist kort for den Business Central-kontakt, som du sender til en samtale. Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).

## <a name="see-also" />Se også

[Oversigt over integrationen af Business Central og Microsoft Teams](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Teams, ofte stillede spørgsmål](teams-faq.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Dele poster i Microsoft Teams](across-working-with-teams.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
