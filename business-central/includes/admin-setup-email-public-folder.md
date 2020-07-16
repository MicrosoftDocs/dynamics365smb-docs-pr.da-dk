---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528006"
---
<span data-ttu-id="15514-101">Før du kan konfigurere maillogføring, skal du forberede din Exchange Online til [offentlige mapper](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="15514-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span></span> <span data-ttu-id="15514-102">Det kan du gøre i [Exchange-administrationen](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), eller du kan bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="15514-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span></span>  

> [!TIP]
> <span data-ttu-id="15514-103">Hvis du vil bruge [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), kan du finde inspiration til, hvordan du opretter et script i et eksempelscript, som vi har publiceret til [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="15514-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="15514-104">Følgende liste beskriver de hovedtrin, der indeholder links til flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="15514-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="15514-105">Opret en administratorrolle til offentlige mapper på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="15514-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="15514-106">Egenskab</span><span class="sxs-lookup"><span data-stu-id="15514-106">Property</span></span>        |<span data-ttu-id="15514-107">Værdi</span><span class="sxs-lookup"><span data-stu-id="15514-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="15514-108">Navn</span><span class="sxs-lookup"><span data-stu-id="15514-108">Name</span></span>            |<span data-ttu-id="15514-109">Administration af offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="15514-109">Public Folders Management</span></span> |
  |<span data-ttu-id="15514-110">Valgte roller</span><span class="sxs-lookup"><span data-stu-id="15514-110">Selected roles</span></span>  |<span data-ttu-id="15514-111">Offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="15514-111">Public Folders</span></span>            |
  |<span data-ttu-id="15514-112">Valgte medlemmer</span><span class="sxs-lookup"><span data-stu-id="15514-112">Selected members</span></span>|<span data-ttu-id="15514-113">Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven</span><span class="sxs-lookup"><span data-stu-id="15514-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="15514-114">Du kan finde flere oplysninger i [Administrere rollegrupper](/exchange/permissions/role-groups?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="15514-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019).</span></span>

- <span data-ttu-id="15514-115">Opret en ny offentlig mappe som postkasse på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="15514-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="15514-116">Egenskab</span><span class="sxs-lookup"><span data-stu-id="15514-116">Property</span></span>        |<span data-ttu-id="15514-117">Værdi</span><span class="sxs-lookup"><span data-stu-id="15514-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="15514-118">Navn</span><span class="sxs-lookup"><span data-stu-id="15514-118">Name</span></span>            |<span data-ttu-id="15514-119">Offentlig postkasse</span><span class="sxs-lookup"><span data-stu-id="15514-119">Public MailBox</span></span>            |

  <span data-ttu-id="15514-120">Du kan finde flere oplysninger i [Oprette en offentlig mappe som postkasse i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="15514-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="15514-121">Oprette nye offentlige mapper</span><span class="sxs-lookup"><span data-stu-id="15514-121">Create new public folders</span></span>

  - <span data-ttu-id="15514-122">Opret en ny offentlig mappe med navnet *Email Logging* i roden, så den fulde sti til mappen bliver ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="15514-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="15514-123">Opret to undermapper, så resultatet er følgende fulde stier til mapperne:</span><span class="sxs-lookup"><span data-stu-id="15514-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="15514-124">Du kan finde flere oplysninger i [Oprette en offentlig mappe](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="15514-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span></span>

- <span data-ttu-id="15514-125">Aktiver den offentlige mappe *Kø* til mail</span><span class="sxs-lookup"><span data-stu-id="15514-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="15514-126">Du kan finde flere oplysninger under [Aktivere eller deaktivere en offentlig mappe til mail](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="15514-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span></span>

- <span data-ttu-id="15514-127">Aktivere afsendelse af mails til den offentlige mappe *Kø* ved hjælp af Outlook eller Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="15514-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="15514-128">Du kan finde flere oplysninger i [Tillade anonyme brugere at sende mail til en offentlig mappe, der er aktiveret til mail](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span><span class="sxs-lookup"><span data-stu-id="15514-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span></span>

- <span data-ttu-id="15514-129">Indstil brugeren af maillogføring som ejer af begge offentlige mapper, *Kø* og *Lager*, ved hjælp af Outlook eller Exchange Management Shell på grundlag af oplysningerne i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="15514-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="15514-130">Egenskab</span><span class="sxs-lookup"><span data-stu-id="15514-130">Property</span></span>        |<span data-ttu-id="15514-131">Værdi</span><span class="sxs-lookup"><span data-stu-id="15514-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="15514-132">Bruger</span><span class="sxs-lookup"><span data-stu-id="15514-132">User</span></span>            |<span data-ttu-id="15514-133">Mailen til den brugerkonto, som Business Central bruger til at køre maillogføringsopgaven</span><span class="sxs-lookup"><span data-stu-id="15514-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="15514-134">Tilladelsesniveau</span><span class="sxs-lookup"><span data-stu-id="15514-134">Permission level</span></span>|<span data-ttu-id="15514-135">Ejer</span><span class="sxs-lookup"><span data-stu-id="15514-135">Owner</span></span>                     |

  <span data-ttu-id="15514-136">Du kan finde flere oplysninger i [Tildele den offentlige mappe tilladelser](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="15514-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="15514-137">Opret to regler for mailflow på grundlag af oplysningerne i følgende tabel</span><span class="sxs-lookup"><span data-stu-id="15514-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="15514-138">Formål</span><span class="sxs-lookup"><span data-stu-id="15514-138">Purpose</span></span>  |<span data-ttu-id="15514-139">Navn</span><span class="sxs-lookup"><span data-stu-id="15514-139">Name</span></span> |<span data-ttu-id="15514-140">Betingelser</span><span class="sxs-lookup"><span data-stu-id="15514-140">Conditions</span></span>                        |<span data-ttu-id="15514-141">Handling</span><span class="sxs-lookup"><span data-stu-id="15514-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="15514-142">En regel for indgående mail</span><span class="sxs-lookup"><span data-stu-id="15514-142">A rule for incoming email</span></span> |<span data-ttu-id="15514-143">Logfør mails, der er sendt til denne organisation</span><span class="sxs-lookup"><span data-stu-id="15514-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="15514-144">*Afsenderen* er placeret *uden for organisationen*, og *modtageren* er placeret *i organisationen*</span><span class="sxs-lookup"><span data-stu-id="15514-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="15514-145">BCC den mailkonto, der er angivet for den offentlige mappe *Kø*</span><span class="sxs-lookup"><span data-stu-id="15514-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="15514-146">En regel for udgående mail</span><span class="sxs-lookup"><span data-stu-id="15514-146">A rule for outgoing email</span></span> | <span data-ttu-id="15514-147">Logfør mails, der er sendt fra denne organisation</span><span class="sxs-lookup"><span data-stu-id="15514-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="15514-148">*Afsenderen* er placeret *inde i organisationen*, og *modtageren* er placeret *uden for organisationen*</span><span class="sxs-lookup"><span data-stu-id="15514-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="15514-149">BCC den mailkonto, der er angivet for den offentlige mappe *Kø*</span><span class="sxs-lookup"><span data-stu-id="15514-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="15514-150">Du kan finde flere oplysninger i [Administrere regler for mailflow i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Handlinger for mailflowregel i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span><span class="sxs-lookup"><span data-stu-id="15514-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span></span>

> [!NOTE]
> <span data-ttu-id="15514-151">Hvis du foretager ændringer i Exchange Management Shell, bliver ændringerne synlige i Exchange Administration efter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="15514-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="15514-152">De ændringer, der er foretaget i Exchange, vil også være tilgængelige i [!INCLUDE[prodshort](prodshort.md)] efter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="15514-152">Also, the changes made in Exchange will be available in [!INCLUDE[prodshort](prodshort.md)] after a delay.</span></span>
