---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: 1b9f60eab5b0bcf812343e82389087ac5535301a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749776"
---
<span data-ttu-id="2e716-101">Før du kan konfigurere maillogføring, skal du forberede din Exchange Online til [offentlige mapper](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ).</span><span class="sxs-lookup"><span data-stu-id="2e716-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ).</span></span> <span data-ttu-id="2e716-102">Det kan du gøre i [Exchange-administrationen](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), eller du kan bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).</span><span class="sxs-lookup"><span data-stu-id="2e716-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).</span></span>  

> [!TIP]
> <span data-ttu-id="2e716-103">Hvis du vil bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), kan du finde inspiration til, hvordan du opretter et script i et eksempelscript, som vi har publiceret til [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="2e716-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="2e716-104">Følgende liste beskriver de hovedtrin, der indeholder links til flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2e716-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="2e716-105">Opret en administratorrolle til offentlige mapper på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="2e716-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="2e716-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="2e716-106">Property</span></span>        |<span data-ttu-id="2e716-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="2e716-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="2e716-108">Navn</span><span class="sxs-lookup"><span data-stu-id="2e716-108">Name</span></span>            |<span data-ttu-id="2e716-109">Administration af offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="2e716-109">Public Folders Management</span></span> |
  |<span data-ttu-id="2e716-110">Valgte roller</span><span class="sxs-lookup"><span data-stu-id="2e716-110">Selected roles</span></span>  |<span data-ttu-id="2e716-111">Offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="2e716-111">Public Folders</span></span>            |
  |<span data-ttu-id="2e716-112">Valgte medlemmer</span><span class="sxs-lookup"><span data-stu-id="2e716-112">Selected members</span></span>|<span data-ttu-id="2e716-113">Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven</span><span class="sxs-lookup"><span data-stu-id="2e716-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="2e716-114">Du kan finde flere oplysninger i [Administrere rollegrupper](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2e716-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).</span></span>

- <span data-ttu-id="2e716-115">Opret en ny offentlig mappe som postkasse på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="2e716-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="2e716-116">Egenskab</span><span class="sxs-lookup"><span data-stu-id="2e716-116">Property</span></span>        |<span data-ttu-id="2e716-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="2e716-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="2e716-118">Navn</span><span class="sxs-lookup"><span data-stu-id="2e716-118">Name</span></span>            |<span data-ttu-id="2e716-119">Offentlig postkasse</span><span class="sxs-lookup"><span data-stu-id="2e716-119">Public MailBox</span></span>            |

  <span data-ttu-id="2e716-120">Du kan finde flere oplysninger i [Oprette en offentlig mappe som postkasse i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="2e716-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="2e716-121">Oprette nye offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="2e716-121">Create new public folders</span></span>

  - <span data-ttu-id="2e716-122">Opret en ny offentlig mappe med navnet *Email Logging* i roden, så den fulde sti til mappen bliver ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="2e716-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="2e716-123">Opret to undermapper, så resultatet er følgende fulde stier til mapperne:</span><span class="sxs-lookup"><span data-stu-id="2e716-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="2e716-124">Du kan finde flere oplysninger i [Oprette en offentlig mappe](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2e716-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).</span></span>

- <span data-ttu-id="2e716-125">Aktiver den offentlige mappe *Kø* til mail</span><span class="sxs-lookup"><span data-stu-id="2e716-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="2e716-126">Du kan finde flere oplysninger under [Aktivere eller deaktivere en offentlig mappe til mail](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="2e716-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)</span></span>

- <span data-ttu-id="2e716-127">Aktivere afsendelse af mails til den offentlige mappe *Kø* ved hjælp af Outlook eller Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="2e716-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="2e716-128">Du kan finde flere oplysninger i [Tillade anonyme brugere at sende mail til en offentlig mappe, der er aktiveret til mail](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="2e716-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)</span></span>

- <span data-ttu-id="2e716-129">Indstil brugeren af maillogføring som ejer af begge offentlige mapper, *Kø* og *Lager*, ved hjælp af Outlook eller Exchange Management Shell på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="2e716-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="2e716-130">Egenskab</span><span class="sxs-lookup"><span data-stu-id="2e716-130">Property</span></span>        |<span data-ttu-id="2e716-131">Værdi</span><span class="sxs-lookup"><span data-stu-id="2e716-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="2e716-132">Bruger</span><span class="sxs-lookup"><span data-stu-id="2e716-132">User</span></span>            |<span data-ttu-id="2e716-133">Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven</span><span class="sxs-lookup"><span data-stu-id="2e716-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="2e716-134">Tilladelsesniveau</span><span class="sxs-lookup"><span data-stu-id="2e716-134">Permission level</span></span>|<span data-ttu-id="2e716-135">Ejer</span><span class="sxs-lookup"><span data-stu-id="2e716-135">Owner</span></span>                     |

  <span data-ttu-id="2e716-136">Du kan finde flere oplysninger i [Tildele den offentlige mappe tilladelser](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="2e716-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="2e716-137">Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel</span><span class="sxs-lookup"><span data-stu-id="2e716-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="2e716-138">Formål</span><span class="sxs-lookup"><span data-stu-id="2e716-138">Purpose</span></span>  |<span data-ttu-id="2e716-139">Navn</span><span class="sxs-lookup"><span data-stu-id="2e716-139">Name</span></span> |<span data-ttu-id="2e716-140">Betingelser</span><span class="sxs-lookup"><span data-stu-id="2e716-140">Conditions</span></span>                        |<span data-ttu-id="2e716-141">Handling</span><span class="sxs-lookup"><span data-stu-id="2e716-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="2e716-142">En regel for indgående mail</span><span class="sxs-lookup"><span data-stu-id="2e716-142">A rule for incoming email</span></span> |<span data-ttu-id="2e716-143">Logfør mails, der er sendt til denne organisation</span><span class="sxs-lookup"><span data-stu-id="2e716-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="2e716-144">*Afsenderen* er placeret *uden for organisationen*, og *modtageren* er placeret *i organisationen*</span><span class="sxs-lookup"><span data-stu-id="2e716-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="2e716-145">BCC den mailkonto, der er angivet for den offentlige mappe *Kø*</span><span class="sxs-lookup"><span data-stu-id="2e716-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="2e716-146">En regel for udgående mail</span><span class="sxs-lookup"><span data-stu-id="2e716-146">A rule for outgoing email</span></span> | <span data-ttu-id="2e716-147">Logfør mails, der er sendt fra denne organisation</span><span class="sxs-lookup"><span data-stu-id="2e716-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="2e716-148">*Afsenderen* er placeret *inde i organisationen*, og *modtageren* er placeret *uden for organisationen*</span><span class="sxs-lookup"><span data-stu-id="2e716-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="2e716-149">BCC den mailkonto, der er angivet for den offentlige mappe *Kø*</span><span class="sxs-lookup"><span data-stu-id="2e716-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="2e716-150">Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="2e716-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

> [!NOTE]
> <span data-ttu-id="2e716-151">Hvis du foretager ændringer i Exchange Management Shell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="2e716-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="2e716-152">De ændringer, der er foretaget i Exchange, vil også være tilgængelige i [!INCLUDE[prod_short](prod_short.md)] efter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="2e716-152">Also, the changes made in Exchange will be available in [!INCLUDE[prod_short](prod_short.md)] after a delay.</span></span>
