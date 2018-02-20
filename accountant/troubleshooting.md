---
title: "Metoder til at fejlfinde eller løse problemer | Microsoft Docs"
description: "Få at vide, hvordan du kan løse problemerne med Accountant Hub til Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: da-dk
ms.lasthandoff: 12/14/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a><span data-ttu-id="6420b-103">Fejlfinding [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6420b-103">Troubleshooting [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="6420b-104">Tilmelding til [!INCLUDE[d365acc](includes/d365acc_md.md)] er nemt og kan udføres hurtigt.</span><span class="sxs-lookup"><span data-stu-id="6420b-104">Signing up for [!INCLUDE[d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="6420b-105">Det er også nemt at føje kunder til dashboardet, men denne artikel vedrører problemer, der eventuelt opstår undervejs.</span><span class="sxs-lookup"><span data-stu-id="6420b-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a><span data-ttu-id="6420b-106">Hvilken mailadresse kan jeg bruge til [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span><span class="sxs-lookup"><span data-stu-id="6420b-106">What email address can I use with [!INCLUDE[d365acc](includes/d365acc_md.md)]?</span></span>
[!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="6420b-107"> kræver, at du bruger en arbejds- eller skolemailadresse til at tilmelde dig.</span><span class="sxs-lookup"><span data-stu-id="6420b-107"> requires that you use a work or school email address to sign up.</span></span> [!INCLUDE[d365acc](includes/d365acc_md.md)]<span data-ttu-id="6420b-108"> understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere.</span><span class="sxs-lookup"><span data-stu-id="6420b-108"> does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="6420b-109">Dette omfatter outlook.com, hotmail.com, gmail.com og andre.</span><span class="sxs-lookup"><span data-stu-id="6420b-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="6420b-110">Hvis du forsøger at tilmelde dig med en privat mailadresse, får du en meddelelse om, at du skal bruge en arbejds- eller skolemailadresse.</span><span class="sxs-lookup"><span data-stu-id="6420b-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="6420b-111">Hvorfor kan jeg ikke oprette forbindelse til min kundes data?</span><span class="sxs-lookup"><span data-stu-id="6420b-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="6420b-112">Der kan være en række årsager, herunder følgende:</span><span class="sxs-lookup"><span data-stu-id="6420b-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="6420b-113">URL-adressen i feltet **Kundens URL-adresse** er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="6420b-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="6420b-114">Gå til **Administrere kunder**, åbn den kunde, du ikke kan oprette forbindelse til, og vælg derefter **Test kundes URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="6420b-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="6420b-115">Kundens virksomhed er offline, f.eks. hvis den er ved at blive opgraderet</span><span class="sxs-lookup"><span data-stu-id="6420b-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="6420b-116">På dashboardet skal du vælge menupunktet **Værktøjer** og derefter vælge **Kontroller fejl**.</span><span class="sxs-lookup"><span data-stu-id="6420b-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="6420b-117">Dermed åbnes en liste med tekniske oplysninger, så du skal måske kontakte systemadministratoren, hvis du får vist fejl.</span><span class="sxs-lookup"><span data-stu-id="6420b-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="6420b-118">Meddelelsen "Serveren har afvist kundens legitimationsoplysninger" angiver f.eks., at du ikke har adgang.</span><span class="sxs-lookup"><span data-stu-id="6420b-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="6420b-119">Du har ikke modtaget en mail fra din kunde, der inviterer dig til at deltage i deres [!INCLUDE[d365fin](includes/d365fin_md.md)], eller du har ikke åbnet linket i mailen, eller du ikke har accepteret invitationen</span><span class="sxs-lookup"><span data-stu-id="6420b-119">You have not received an email from your client that invites them to their [!INCLUDE[d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="6420b-120">Du skal åbne linket i invitationen og acceptere de trin, der tilføjer dig til kundens [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6420b-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6420b-121">Indtil da har du ikke adgang til deres data.</span><span class="sxs-lookup"><span data-stu-id="6420b-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="6420b-122">Du har ikke adgang til alle regnskaber i din kundes [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6420b-122">You do not have access to all companies in your client's [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="6420b-123">Din kunde kan have flere afdelinger eller virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)], og invitationen inkluderer ikke altid alle regnskaber.</span><span class="sxs-lookup"><span data-stu-id="6420b-123">Your client can have multiple business units or companies in [!INCLUDE[d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="6420b-124">Arbejd sammen med kunden for at sikre, at du har adgang til de virksomheder, som kunden ønsker, at du skal arbejde i.</span><span class="sxs-lookup"><span data-stu-id="6420b-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="6420b-125">Hvorfor opdateres dataene i mit dashboard ikke?</span><span class="sxs-lookup"><span data-stu-id="6420b-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="6420b-126">Når du tilføjer en kunde eller anmoder om en opdatering af dataene, henter [!INCLUDE[d365acc](includes/d365acc_md.md)] dataene.</span><span class="sxs-lookup"><span data-stu-id="6420b-126">When you add a client or request a refresh of the data, [!INCLUDE[d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="6420b-127">Men du skal selv opdatere vinduet, f.eks. ved at vælge handlingen "Vis alle virksomheder igen", opdatere browservinduet, navigere væk fra dashboardet og derefter tilbage igen eller noget lignende.</span><span class="sxs-lookup"><span data-stu-id="6420b-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="6420b-128">Dette er et kendt problem, som vi arbejder på at forbedre i en senere opdatering.</span><span class="sxs-lookup"><span data-stu-id="6420b-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6420b-129">Se også</span><span class="sxs-lookup"><span data-stu-id="6420b-129">See Also</span></span>
<span data-ttu-id="6420b-130">[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="6420b-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="6420b-131">[Tilføje kunder til dit dashboard i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="6420b-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

