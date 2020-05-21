---
title: 'Fejlfinding: Adgang til kamera og placering'
description: Denne artikel beskriver, hvordan du retter fejl i forbindelse med adgang til kamera- og placeringsoplysninger i Business central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics365-business-central
ms.openlocfilehash: befb7af01ba26512a4b62005e81b5a3ff351b02f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324460"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="3e559-103">Fejlfinding: Adgang til kamera og placering</span><span class="sxs-lookup"><span data-stu-id="3e559-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="3e559-104">Der kan opstå fejl, når du forsøger at få adgang til en enheds kamera- og placeringsoplysninger via [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3e559-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3e559-105">På listen nedenfor kan du se de mulige årsager til disse fejl, og hvordan du retter dem.</span><span class="sxs-lookup"><span data-stu-id="3e559-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="3e559-106">Enhed skal have kamera- og placeringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="3e559-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="3e559-107">For at du kan få adgang til kameraet eller brugerens placering på en enhed, skal enheden have et fysisk kamera eller muligheden for at hente oplysninger om placeringen.</span><span class="sxs-lookup"><span data-stu-id="3e559-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="3e559-108">Hvis din enhed har kamera- og placeringsfunktioner, men der stadig opstår fejl, skal nogle af driverne muligvis opdateres eller geninstalleres.</span><span class="sxs-lookup"><span data-stu-id="3e559-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="3e559-109">Selvom du ikke er sikker, anbefaler vi altid, at du opdaterer enhedens operativsystem, drivere og browser til den seneste version, så du får den bedste oplevelse.</span><span class="sxs-lookup"><span data-stu-id="3e559-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="3e559-110">Adgangstilladelser er ikke aktiveret</span><span class="sxs-lookup"><span data-stu-id="3e559-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="3e559-111">Du skal aktivere generel adgang til kamera og placering i enhedens indstillinger for beskyttelse af personlige oplysninger og give [!INCLUDE[prodshort](includes/prodshort.md)] udtrykkeligt tilladelse til at få adgang til dem.</span><span class="sxs-lookup"><span data-stu-id="3e559-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="3e559-112">Hvis du f. eks. vil se eller ændre tilladelser for en enhed, der kører i Windows, skal du gå til **Indstillinger**, vælge **Beskyttelse af personlige oplysninger** og derefter gå til **App-tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="3e559-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="3e559-113">I forbindelse med mobilenheder skal du give kamera- og placeringsadgangstilladelserne til [!INCLUDE[prodshort](includes/prodshort.md)]-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="3e559-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="3e559-114">Hvis du vil gøre det for en iOS-enhed, skal du gå til **Indstillinger**, vælge **Beskyttelse af personlige oplysninger** og derefter vælge **Kamera** eller **Placering**.</span><span class="sxs-lookup"><span data-stu-id="3e559-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="3e559-115">Hvis du bruger en Android-enhed, skal du vælge **Indstillinger**, vælge **Apps og meddelelser**, **Avanceret**, **Rettighedsadministrator** og derefter **Kamera** eller **Placering**.</span><span class="sxs-lookup"><span data-stu-id="3e559-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="3e559-116">Hvis du bruger [!INCLUDE[prodshort](includes/prodshort.md)] i en browser, skal du desuden give [!INCLUDE[prodshort](includes/prodshort.md)]-webstedet tilladelse til at få adgang til oplysninger om kamera eller placering.</span><span class="sxs-lookup"><span data-stu-id="3e559-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="3e559-117">Hvis du vil se eller ændre tilladelserne for et websted i Microsoft Edge-browseren, skal du gå til **Indstillinger**, vælge **Webstedstilladelser** og derefter vælge **Kamera** eller **Placering**.</span><span class="sxs-lookup"><span data-stu-id="3e559-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="3e559-118">Bemærk, at dette kan være anderledes for andre browsere.</span><span class="sxs-lookup"><span data-stu-id="3e559-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="3e559-119">Som standard viser enheden eller browseren en anmodning om at få adgang til disse egenskaber, når brugeren aktiverer dem første gang.</span><span class="sxs-lookup"><span data-stu-id="3e559-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="3e559-120">Nogle ældre browsere giver ikke adgang til kamera og placering.</span><span class="sxs-lookup"><span data-stu-id="3e559-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="3e559-121">Kameraet er f. eks. ikke tilgængeligt i Internet Explorer eller den tidligere Edge-browser.</span><span class="sxs-lookup"><span data-stu-id="3e559-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="3e559-122">Webklientens forbindelse er ikke sikker</span><span class="sxs-lookup"><span data-stu-id="3e559-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="3e559-123">Kamera- og placeringsfunktionerne er kun tilgængelige, når du får adgang til webklienten via SSL-sikrede HTTP-forbindelser ved hjælp af `https://` URI-skemaet.</span><span class="sxs-lookup"><span data-stu-id="3e559-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="3e559-124">Den eneste undtagelse er at oprette forbindelse til `http://localhost`, der bruges til udviklings- og testformål.</span><span class="sxs-lookup"><span data-stu-id="3e559-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="3e559-125">Arbejde med virtualiseringsteknologier</span><span class="sxs-lookup"><span data-stu-id="3e559-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="3e559-126">Når der oprettes forbindelse til [!INCLUDE[prodshort](includes/prodshort.md)] med fjernskrivebordet eller en anden virtualisering, er der muligvis ikke adgang til kameraet eller placeringen.</span><span class="sxs-lookup"><span data-stu-id="3e559-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="3e559-127">Hvis det er tilfældet, skal du bruge det fysiske system i stedet for.</span><span class="sxs-lookup"><span data-stu-id="3e559-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="3e559-128">Antivirusprogram</span><span class="sxs-lookup"><span data-stu-id="3e559-128">Antivirus Software</span></span>
<span data-ttu-id="3e559-129">Nogle antivirusprogrammer blokerer som standard for kamera og placering.</span><span class="sxs-lookup"><span data-stu-id="3e559-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="3e559-130">Husk at kontrollere indstillingerne for dit antivirusprogram.</span><span class="sxs-lookup"><span data-stu-id="3e559-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e559-131">Se også</span><span class="sxs-lookup"><span data-stu-id="3e559-131">See Also</span></span>
[<span data-ttu-id="3e559-132">Implementering af kameraet i AL</span><span class="sxs-lookup"><span data-stu-id="3e559-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="3e559-133">Implementering af placeringen i AL</span><span class="sxs-lookup"><span data-stu-id="3e559-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
