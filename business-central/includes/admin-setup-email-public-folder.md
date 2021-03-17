---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: d58d8d628577f163d36199b8fc5785982aac830a
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5492996"
---
Før du kan konfigurere maillogføring, skal du forberede din Exchange Online til [offentlige mapper](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Det kan du gøre i [Exchange-administrationen](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), eller du kan bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Hvis du vil bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), kan du finde inspiration til, hvordan du opretter et script i et eksempelscript, som vi har publiceret til [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Følgende liste beskriver de hovedtrin, der indeholder links til flere oplysninger.  

- Opret en administratorrolle til offentlige mapper på grundlag af oplysningerne i følgende tabel:

  |Egenskab        |Værdi                     |
  |----------------|--------------------------|
  |Navn            |Administration af offentlige mapper |
  |Valgte roller  |Offentlige mapper            |
  |Valgte medlemmer|Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven|

  Du kan finde flere oplysninger i [Administrere rollegrupper](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Opret en ny offentlig mappe som postkasse på grundlag af oplysningerne i følgende tabel:

  |Egenskab        |Værdi                     |
  |----------------|--------------------------|
  |Navn            |Offentlig postkasse            |

  Du kan finde flere oplysninger i [Oprette en offentlig mappe som postkasse i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Oprette nye offentlige mapper

  - Opret en ny offentlig mappe med navnet *Email Logging* i roden, så den fulde sti til mappen bliver ```\Email Logging\```
  - Opret to undermapper, så resultatet er følgende fulde stier til mapperne:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Du kan finde flere oplysninger i [Oprette en offentlig mappe](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Aktiver den offentlige mappe *Kø* til mail

  Du kan finde flere oplysninger under [Aktivere eller deaktivere en offentlig mappe til mail](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Aktivere afsendelse af mails til den offentlige mappe *Kø* ved hjælp af Outlook eller Exchange Management Shell

  Du kan finde flere oplysninger i [Tillade anonyme brugere at sende mail til en offentlig mappe, der er aktiveret til mail](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Indstil brugeren af maillogføring som ejer af begge offentlige mapper, *Kø* og *Lager*, ved hjælp af Outlook eller Exchange Management Shell på grundlag af oplysningerne i følgende tabel:

  |Egenskab        |Værdi                     |
  |----------------|--------------------------|
  |Bruger            |Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven|
  |Tilladelsesniveau|Ejer                     |

  Du kan finde flere oplysninger i [Tildele den offentlige mappe tilladelser](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel

  |Formål  |Navn |Betingelser                        |Handling                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |En regel for indgående mail |Logfør mails, der er sendt til denne organisation|*Afsenderen* er placeret *uden for organisationen*, og *modtageren* er placeret *i organisationen*|BCC den mailkonto, der er angivet for den offentlige mappe *Kø*|
  |En regel for udgående mail | Logfør mails, der er sendt fra denne organisation |*Afsenderen* er placeret *inde i organisationen*, og *modtageren* er placeret *uden for organisationen*|BCC den mailkonto, der er angivet for den offentlige mappe *Kø*|
  
  Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Hvis du foretager ændringer i Exchange Management Shell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse. De ændringer, der er foretaget i Exchange, vil også være tilgængelige i [!INCLUDE[prod_short](prod_short.md)] efter en forsinkelse. Forsinkelsen kan være flere timer.
