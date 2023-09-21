---
author: brentholtorf
ms.topic: include
ms.date: 02/15/2022
ms.author: bholtorf
---

> [!NOTE]
> I følgende afsnit antages det, at du har administratoradgang til Exchange Online.

Før du kan konfigurere maillogføring, skal du forberede Office 365 [offentlige mapper](/exchange/collaboration-exo/public-folders/public-folders). Det kan du gøre i [Exchange-administrationen](/exchange/exchange-admin-center?preserve-view=true), eller du kan bruge [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Hvis du vil bruge [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true), kan du finde inspiration til, hvordan du opretter et script i et eksempelscript, som vi har publiceret i [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Følg nedenstående trin for at oprette Exchange Online med links, hvor du kan få mere at vide.

### Opret en administratorrollegruppe

Opret en administratorrollegruppe til offentlige mapper på grundlag af oplysningerne i følgende tabel:

|Egenskab        |Værdi                     |
|----------------|--------------------------|
|Navn            |Administration af offentlige mapper |
|Valgte roller  |Offentlige mapper            |
|Markerede brugere  |Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven|

Du kan finde flere oplysninger i [Administrere rollegrupper i Exchange Online](/exchange/permissions-exo/role-groups).

### Opret en ny postkasse til offentlige mapper

Opret en ny offentlig mappe som postkasse på grundlag af oplysningerne i følgende tabel:

|Egenskab        |Værdi                     |
|----------------|--------------------------|
|Navn            |Offentlig postkasse            |

Du kan finde flere oplysninger i [Oprette en postkasse til offentlig mapper](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### Oprette nye offentlige mapper

1. Opret en ny offentlig mappe med navnet **Email Logging** i roden, så den fulde sti til mappen bliver `\Email Logging\`.
2. Opret to undermapper, så resultatet er følgende fulde stier til mapperne:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Du kan finde flere oplysninger i [Oprette en offentlig mappe](/exchange/collaboration-exo/public-folders/create-public-folder).

### Angiv ejerskabet af mappen Delte

Indstil e-mail-logførings brugeren som ejer af både offentlige mapper, *kø* og *lager*.

Du kan finde flere oplysninger i [Tildele den offentlige mappe tilladelser](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### Aktiver den offentlige mappe *Kø* til mail

  Du kan finde flere oplysninger i [Aktivere eller deaktivere en offentlig mappe til mail](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### E-mail-Aktivér afsendelse af e-mails til den offentlige mappe *Kø*

Aktivere afsendelse af mails til den offentlige mappe *Kø* ved hjælp af Outlook eller Exchange Management Shell.

Du kan finde flere oplysninger i [Tillade anonyme brugere at sende mail til en offentlig mappe, der er aktiveret til mail](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### Oprette regler for mail flow

Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel:

|Formål  |Name |Anvend denne regel, hvis...             |Benyt følgende fremgangsmåde...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|En regel for indgående mail |Logfør mails, der er sendt til denne organisation|*Afsenderen* er placeret *uden for organisationen*, og *modtageren* er placeret *i organisationen*|BCC den mailkonto, der er angivet for den offentlige mappe *Kø*|
|En regel for udgående mail | Logfør mails, der er sendt fra denne organisation |*Afsenderen* er placeret *inde i organisationen*, og *modtageren* er placeret *uden for organisationen*|BCC den mailkonto, der er angivet for den offentlige mappe *Kø*|

Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Hvis du foretager ændringer i Exchange Management Shell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse. De ændringer, der er foretaget i Exchange, vil også være tilgængelige i [!INCLUDE[prod_short](prod_short.md)] efter en forsinkelse. Forsinkelsen kan være flere timer.
