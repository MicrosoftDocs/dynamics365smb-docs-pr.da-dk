---
title: Tilføje ekstra linjer for at definere udvidede beskrivelser
description: Du kan tilføje ekstra linjer for at udvide standardteksten, der beskriver en vare, en finanskonto og andre data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1dd6c3085c0cb8696b6e7011fbea3c3cd9a1c86e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920443"
---
# <a name="add-extended-text"></a><span data-ttu-id="c597e-103">Tilføje udvidet tekst</span><span class="sxs-lookup"><span data-stu-id="c597e-103">Add Extended Text</span></span>

<span data-ttu-id="c597e-104">Du kan udvide beskrivelsen af varer, lagerenheder, finanskonti og ressourcer ved at tilføje ekstra linjer som udvidet tekst.</span><span class="sxs-lookup"><span data-stu-id="c597e-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="c597e-105">Du kan også oprette betingelser for brugen af de ekstra linjer.</span><span class="sxs-lookup"><span data-stu-id="c597e-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="c597e-106">I følgende afsnit beskrives, hvordan du føjer udvidet tekst til en beskrivelse af en vare.</span><span class="sxs-lookup"><span data-stu-id="c597e-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="c597e-107">Men de samme trin gælder for lagerenheder, finanskonti og ressourcer.</span><span class="sxs-lookup"><span data-stu-id="c597e-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="c597e-108">Sådan defineres udvidet tekst for en beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c597e-108">To define extended text for an description</span></span>

1. <span data-ttu-id="c597e-109">Åbn kortet for en vare, du vil føje udvidet tekst til, og vælg derefter handlingen **Udvidet tekst**.</span><span class="sxs-lookup"><span data-stu-id="c597e-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="c597e-110">Udfyld felterne **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c597e-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="c597e-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c597e-111">Choose the **New**.</span></span>
4. <span data-ttu-id="c597e-112">Udfyld feltet **Sprogkode**, eller marker afkrydsningsfeltet **Alle sprogkoder**, hvis du bruger sprogkoder.</span><span class="sxs-lookup"><span data-stu-id="c597e-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="c597e-113">Udfyld felterne **Startdato** og **Slutdato**, hvis du vil begrænse den tid, hvor den udvidede tekst bruges.</span><span class="sxs-lookup"><span data-stu-id="c597e-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="c597e-114">Skriv den udvidede tekstkode i feltet **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="c597e-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="c597e-115">Markér de relevante afkrydsningsfelter for de dokumenttyper, hvor den udvidede tekst skal udskrives.</span><span class="sxs-lookup"><span data-stu-id="c597e-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="c597e-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c597e-116">Close the page.</span></span>

<span data-ttu-id="c597e-117">Du kan nu føje denne udvidede tekst til dokumenter.</span><span class="sxs-lookup"><span data-stu-id="c597e-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="c597e-118">Følgende fremgangsmåde beskriver, hvordan du føjer udvidet tekst til en salgsordre, men samme fremgangsmåde gælder for alle andre dokumenter, du har angivet for den udvidede tekst.</span><span class="sxs-lookup"><span data-stu-id="c597e-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="c597e-119">Sådan tilføjes en udvidet varetekst på en salgsordrelinje</span><span class="sxs-lookup"><span data-stu-id="c597e-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="c597e-120">Åbn en salgsordre med en salgslinje for en vare, der har udvidet tekst defineret.</span><span class="sxs-lookup"><span data-stu-id="c597e-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="c597e-121">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="c597e-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="c597e-122">Vælg den ønskede linje, og vælg derefter handlingen **Indsæt udv. tekster**.</span><span class="sxs-lookup"><span data-stu-id="c597e-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="c597e-123">Se også</span><span class="sxs-lookup"><span data-stu-id="c597e-123">See Also</span></span>

[<span data-ttu-id="c597e-124">Opsætning af lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c597e-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="c597e-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c597e-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
