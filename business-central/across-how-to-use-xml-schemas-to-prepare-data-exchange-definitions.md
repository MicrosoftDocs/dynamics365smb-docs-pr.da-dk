---
title: Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner
description: Bruge XML-skemaer til at konfigurere til dokumentudvekslingsstrukturen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/01/2020
ms.author: edupont
ms.openlocfilehash: e244afdb7690ad10eeb99f0c8004cb171469744b
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781956"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="12479-103">Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="12479-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="12479-104">Hvis du vil aktivere import/eksport af data i XML-filer via dataudvekslingsstrukturen i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge XML-skemaer til at definere, hvilke dataelementer du vil udveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="12479-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="12479-105">Du kan udføre dette arbejde på siden **XML-skemafremviser** ved at indlæse XML-skemafilen, vælge de relevante dataelementer og derefter initialisere en dataudvekslingsdefinition.</span><span class="sxs-lookup"><span data-stu-id="12479-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="12479-106">Når du har defineret, hvilke dataelementer der skal medtages, baseret på XML-skemaet, kan du bruge **Generer dataudvekslingsdefinition** som handling til at initialisere en dataudvekslingsdefinition, der er baseret på de valgte dataelementer, som du derefter udfører i dataudvekslingsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="12479-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="12479-107">Herved oprettes der en post på siden **Bogføringsudvekslingsdefinitioner**, hvor du kan fortsætte ved at definere, hvilke elementer i filen, der knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="12479-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="12479-108">Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="12479-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="12479-109">Dette emne indeholder følgende procedurer:</span><span class="sxs-lookup"><span data-stu-id="12479-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="12479-110">Sådan indlæses en XML-skemafil</span><span class="sxs-lookup"><span data-stu-id="12479-110">To load an XML schema file</span></span>  

- <span data-ttu-id="12479-111">Sådan markeres eller fjernes markeringen af noder i et XML-skema</span><span class="sxs-lookup"><span data-stu-id="12479-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="12479-112">Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="12479-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="12479-113">Sådan indlæses en XML-skemafil</span><span class="sxs-lookup"><span data-stu-id="12479-113">To load an XML schema file</span></span>

1. <span data-ttu-id="12479-114">Sørg for, at den pågældende XML-skemafil er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="12479-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="12479-115">Filtypenavnet er .xsd.</span><span class="sxs-lookup"><span data-stu-id="12479-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="12479-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XML-skemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="12479-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="12479-117">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="12479-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="12479-118">Udfyld felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="12479-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="12479-119">Felt</span><span class="sxs-lookup"><span data-stu-id="12479-119">Field</span></span>|<span data-ttu-id="12479-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12479-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="12479-121">**Kode**</span><span class="sxs-lookup"><span data-stu-id="12479-121">**Code**</span></span>|<span data-ttu-id="12479-122">Angiv en kode, der identificerer XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="12479-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="12479-123">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="12479-123">**Description**</span></span>|<span data-ttu-id="12479-124">Angiv en beskrivelse af XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="12479-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="12479-125">Feltet **Målnavneområde** angiver navneområdet i den XML-skemafil, der er indlæst for linjen.</span><span class="sxs-lookup"><span data-stu-id="12479-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="12479-126">Vælg handlingen **Indlæs skema**, og vælg derefter XML-skemafilen.</span><span class="sxs-lookup"><span data-stu-id="12479-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="12479-127">Når filen er indlæst, udfyldes resten af felterne på linjen med oplysninger fra filen, og afkrydsningsfeltet **Skema er indlæst** markeres.</span><span class="sxs-lookup"><span data-stu-id="12479-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="12479-128">Som standard er træet for det indlæste indlæste XML-skema skjult.</span><span class="sxs-lookup"><span data-stu-id="12479-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="12479-129">Udvid hver node ved at klikke på knappen **+** på noden.</span><span class="sxs-lookup"><span data-stu-id="12479-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="12479-130">For at udvide alle noder skal du vælge **Udvid alle** på båndet.</span><span class="sxs-lookup"><span data-stu-id="12479-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="12479-131">Sådan markeres eller fjernes markeringen af noder i et XML-skema</span><span class="sxs-lookup"><span data-stu-id="12479-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="12479-132">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XML-skemafremviser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="12479-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="12479-133">Udfyld felterne i sidehovedet som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="12479-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="12479-134">Felt</span><span class="sxs-lookup"><span data-stu-id="12479-134">Field</span></span>|<span data-ttu-id="12479-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12479-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="12479-136">**Kode til XML-skema**</span><span class="sxs-lookup"><span data-stu-id="12479-136">**XML Schema Code**</span></span>|<span data-ttu-id="12479-137">Angiv den XML-skemafil, du har indlæst i trin 5 i afsnittet "Sådan indlæses en XML-skemafil".</span><span class="sxs-lookup"><span data-stu-id="12479-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="12479-138">**Nyt XMLport-nr.**</span><span class="sxs-lookup"><span data-stu-id="12479-138">**New XMLport No.**</span></span>|<span data-ttu-id="12479-139">Angiv nummeret på den XMLport, der er oprettet fra dette XML-skema, når du vælger handlingen **Generér XMLport**.</span><span class="sxs-lookup"><span data-stu-id="12479-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="12479-140">Linjerne er nu udfyldt med noder, der repræsenterer alle elementer i XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="12479-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="12479-141">Noder for elementer, der er obligatoriske i henhold til XML-skemaet, er som standard valgt.</span><span class="sxs-lookup"><span data-stu-id="12479-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="12479-142">På den første linje i kolonnen **Nodenavn** skal du udvide noden **Dokument** og derefter gradvist udvide underliggende noder, du vil gennemgå.</span><span class="sxs-lookup"><span data-stu-id="12479-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="12479-143">Alternativt kan du højreklikke på en node og derefter vælge **Udvid alle**.</span><span class="sxs-lookup"><span data-stu-id="12479-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="12479-144">Vælg en af følgende handlinger for at ændre, hvilke noder der vises.</span><span class="sxs-lookup"><span data-stu-id="12479-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="12479-145">**Handling**</span><span class="sxs-lookup"><span data-stu-id="12479-145">**Action**</span></span>|<span data-ttu-id="12479-146">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12479-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="12479-147">**Vis alle**</span><span class="sxs-lookup"><span data-stu-id="12479-147">**Show All**</span></span>|<span data-ttu-id="12479-148">Alle noder vises.</span><span class="sxs-lookup"><span data-stu-id="12479-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="12479-149">**Skjul ikke-obligatoriske**</span><span class="sxs-lookup"><span data-stu-id="12479-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="12479-150">Der vises kun de noder, der repræsenterer elementer, der kræves i henhold til XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="12479-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="12479-151">Disse noder er typisk angivet med **1** i feltet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="12479-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="12479-152">Vælg **Vis alle** for at tilbageføre visningen.</span><span class="sxs-lookup"><span data-stu-id="12479-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="12479-153">**Skjul ikke-valgte**</span><span class="sxs-lookup"><span data-stu-id="12479-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="12479-154">Kun noder, hvor afkrydsningsfeltet **Markeret** er markeret, vises.</span><span class="sxs-lookup"><span data-stu-id="12479-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="12479-155">Vælg **Vis alle** for at tilbageføre visningen.</span><span class="sxs-lookup"><span data-stu-id="12479-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="12479-156">Vælg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="12479-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="12479-157">I afkrydsningsfeltet **Markeret** skal du angive for hver enkelt node, om elementet skal understøttes i dataudvekslingsdefinitionen for den relaterede SEPA-bankfil.</span><span class="sxs-lookup"><span data-stu-id="12479-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="12479-158">Når du vælger en obligatorisk underordnet node, markeres alle overordnede noder ovenfor også.</span><span class="sxs-lookup"><span data-stu-id="12479-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="12479-159">Vælg handlingen **Marker alle obligatoriske elementer** for at markere alle noder, der repræsenterer elementer, der er obligatoriske i henhold til XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="12479-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="12479-160">Vælg handlingen **Afmarker alt** for at rydde alle markeringer.</span><span class="sxs-lookup"><span data-stu-id="12479-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="12479-161">Feltet **Valg** angiver, om noden har to eller flere sidestillede noder, der fungerer som valgmuligheder.</span><span class="sxs-lookup"><span data-stu-id="12479-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="12479-162">Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="12479-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="12479-163">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **XML-skemaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="12479-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="12479-164">Vælg det relevante XML-skema, og vælg derefter handlingen **Åbn XML-skemafremviser**.</span><span class="sxs-lookup"><span data-stu-id="12479-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="12479-165">Sørg for, at de relevante noder er valgt.</span><span class="sxs-lookup"><span data-stu-id="12479-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="12479-166">Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".</span><span class="sxs-lookup"><span data-stu-id="12479-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="12479-167">På siden **XML-skemafremviser** skal du vælge handlingen **Generer dataudvekslingsdefinition**.</span><span class="sxs-lookup"><span data-stu-id="12479-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="12479-168">Der oprettes en dataudvekslingsdefinition på siden **Bogføringsudvekslingsdefinition**, som du kan afslutte ved at angive, hvilke elementer i filen, der skal knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="12479-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="12479-169">Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="12479-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="12479-170">Du kan også bruge funktionen **Hent filstruktur** på siden **Bogføringsudvekslingsdefinition**, som bruger funktionerne på siden **XML-skemafremviser** til at udfylde oversigtspanelet **Kolonnedefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="12479-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="12479-171">I frigivelsesbølge 1 i 2019 og tidligere versioner kan du generere en XMLport, der er baseret på skemaet, og derefter indlæse den i løsningen.</span><span class="sxs-lookup"><span data-stu-id="12479-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="12479-172">Dette understøttes ikke længere.</span><span class="sxs-lookup"><span data-stu-id="12479-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="12479-173">Se også</span><span class="sxs-lookup"><span data-stu-id="12479-173">See Also</span></span>

[<span data-ttu-id="12479-174">Konfigurere dataudvekslingsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="12479-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="12479-175">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="12479-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="12479-176">Indhente betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="12479-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="12479-177">Om Data Exchange Framework</span><span class="sxs-lookup"><span data-stu-id="12479-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
