---
title: Arbejde med Smarte notifikationer og angive, hvornår de kan ses | Microsoft Docs
description: Du kan modtage meddelelser, der oplyser dig om statusændringer eller -begivenheder, f.eks. et forfaldent beløb eller lav lagerbeholdning.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 45916dc92513a223ca74cb3d76629fb36b8afa39
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189503"
---
# <a name="manage-notifications"></a><span data-ttu-id="ce787-103">Administrere notifikationer</span><span class="sxs-lookup"><span data-stu-id="ce787-103">Manage Notifications</span></span>

<span data-ttu-id="ce787-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du få hjælp til at arbejde mere effektivt ved at få besked om bestemte hændelser eller ændringer af status, når du er ved at fakturere en kunde, der har et forfaldent beløb, eller den disponible lagerbeholdning f.eks. er lavere end det antal, du er ved at sælge.</span><span class="sxs-lookup"><span data-stu-id="ce787-104">[!INCLUDE[d365fin](includes/d365fin_md.md)] can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="ce787-105">Disse notifikationer skal vises som diskrete tip i forbindelse med den opgave, du udfører, og du kan vælge at ignorere notifikationen eller få vist detaljer om problemet.</span><span class="sxs-lookup"><span data-stu-id="ce787-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="ce787-106">Hvis du vælger at få vist detaljer om en notifikation, kan du gribe ind for at løse problemet, f.eks at kontakte til kunden, købe mere ind til lager osv.</span><span class="sxs-lookup"><span data-stu-id="ce787-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="ce787-107">Du vælger selv, hvad du vil gøre, og [!INCLUDE[d365fin](includes/d365fin_md.md)] giver dig råd og anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="ce787-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="ce787-108">Notifikationer hjælper uøvede brugere med at udføre ukendte opgaver og sænker ikke produktiviteten for den mere øvede bruger.</span><span class="sxs-lookup"><span data-stu-id="ce787-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="ce787-109">Sådan aktiverer eller deaktiverer du notifikationer og styrer, hvornår de sendes</span><span class="sxs-lookup"><span data-stu-id="ce787-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="ce787-110">Når du begynder at bruge [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle notifikationer aktiveret, men du kan slå dem til eller fra, f.eks. hvis du ikke er interesseret i en bestemt hændelse eller status.</span><span class="sxs-lookup"><span data-stu-id="ce787-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="ce787-111">Desuden kan du ved nogle notifikationer angive, hvilke betingelser de skal sendes på.</span><span class="sxs-lookup"><span data-stu-id="ce787-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="ce787-112">F.eks. hvis du vil have besked, når mangler lagervarer, men kun om varer, som du køber fra en bestemt leverandør.</span><span class="sxs-lookup"><span data-stu-id="ce787-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="ce787-113">Det er kun dig, der kan aktivere eller deaktivere notifikationer og angive betingelser.</span><span class="sxs-lookup"><span data-stu-id="ce787-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="ce787-114">I øverste højre hjørne skal du vælge ikonet **Indstillinger** ![Indstillinger](media/ui-experience/settings_icon_small.png "Ikonet Indstillinger for rollecenter") og derefter vælge handlingen **Mine indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="ce787-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="ce787-115">På siden **Mine indstillinger** skal du i feltet **Notifikationer** vælge *Ændr, når jeg modtager notifikationer*.</span><span class="sxs-lookup"><span data-stu-id="ce787-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="ce787-116">link.</span><span class="sxs-lookup"><span data-stu-id="ce787-116">link.</span></span>  
3. <span data-ttu-id="ce787-117">Aktiver eller fjern markeringen i afkrydsningsfeltet **Aktiveret** på den side, der vises.</span><span class="sxs-lookup"><span data-stu-id="ce787-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="ce787-118">Hvis du vil angive betingelser, der skal udløse en notifikation, skal du vælge linket **Vis filterdetaljer** og derefter udfylde felterne.</span><span class="sxs-lookup"><span data-stu-id="ce787-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce787-119">Se også</span><span class="sxs-lookup"><span data-stu-id="ce787-119">See Also</span></span>

<span data-ttu-id="ce787-120">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce787-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
