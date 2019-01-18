---
title: "Oprette XMLporte baseret på XML-skemaer | Microsoft Docs"
description: Bruge XML-skemaer til at konfigurere til dokumentudvekslingsstrukturen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: fbbf44cd7a98598ed25dadeb4d6e3a8d37a0bfb0
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="c13c9-103">Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner</span><span class="sxs-lookup"><span data-stu-id="c13c9-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="c13c9-104">Hvis du vil aktivere import/eksport af data i XML-filer via dataudvekslingsstrukturen i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruge XML-skemaer til at definere, hvilke dataelementer du vil udveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c13c9-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c13c9-105">Du kan udføre dette arbejde på siden **XML-skemafremviser** ved at indlæse XML-skemafilen, vælge de relevante dataelementer og derefter initialisere enten en dataudvekslingsdefinition eller en XMLport.</span><span class="sxs-lookup"><span data-stu-id="c13c9-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="c13c9-106">Når du har defineret, hvilke dataelementer der skal medtages, baseret på XML-skemaet, kan du bruge handlingen **Generér XMLport** til at oprette XMLport-objektet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="c13c9-107">Alternativt kan du bruge **Generer dataudvekslingsdefinition** som handling til at initialisere en dataudvekslingsdefinition, der er baseret på de valgte dataelementer, som du derefter udfører inden for rammerne til udveksling af data.</span><span class="sxs-lookup"><span data-stu-id="c13c9-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="c13c9-108">Herved oprettes der en post på siden **Bogføringsudvekslingsdefinitioner**, hvor du kan fortsætte ved at definere, hvilke elementer i filen, der knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c13c9-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c13c9-109">Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="c13c9-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="c13c9-110">Dette emne indeholder følgende procedurer:</span><span class="sxs-lookup"><span data-stu-id="c13c9-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="c13c9-111">Sådan indlæses en XML-skemafil</span><span class="sxs-lookup"><span data-stu-id="c13c9-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="c13c9-112">Sådan markeres eller fjernes markeringen af noder i et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="c13c9-113">Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="c13c9-114">Sådan oprettes en XMLport for filen, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="c13c9-115">Sådan importeres en XMLport i Object Designer</span><span class="sxs-lookup"><span data-stu-id="c13c9-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="c13c9-116">Sådan indlæses en XML-skemafil</span><span class="sxs-lookup"><span data-stu-id="c13c9-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="c13c9-117">Sørg for, at den pågældende XML-skemafil er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c13c9-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="c13c9-118">Filtypenavnet er .xsd.</span><span class="sxs-lookup"><span data-stu-id="c13c9-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="c13c9-119">I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c13c9-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="c13c9-120">Under fanen **Startside** i gruppen **Ny** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="c13c9-121">Udfyld felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c13c9-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c13c9-122">Felt</span><span class="sxs-lookup"><span data-stu-id="c13c9-122">Field</span></span>|<span data-ttu-id="c13c9-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c13c9-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c13c9-124">**Kode**</span><span class="sxs-lookup"><span data-stu-id="c13c9-124">**Code**</span></span>|<span data-ttu-id="c13c9-125">Angiv en kode, der identificerer XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="c13c9-126">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="c13c9-126">**Description**</span></span>|<span data-ttu-id="c13c9-127">Angiv en beskrivelse af XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="c13c9-128">Feltet **Målnavneområde** angiver navneområdet i den XML-skemafil, der er indlæst for linjen.</span><span class="sxs-lookup"><span data-stu-id="c13c9-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="c13c9-129">Under fanen **Startside** i gruppen **Proces** skal du vælge **Indlæs skema** og derefter vælge XML-skemafilen.</span><span class="sxs-lookup"><span data-stu-id="c13c9-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="c13c9-130">Når filen er indlæst, udfyldes resten af felterne på linjen med oplysninger fra filen, og afkrydsningsfeltet **Skema er indlæst** markeres.</span><span class="sxs-lookup"><span data-stu-id="c13c9-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c13c9-131">Som standard er træet for det indlæste indlæste XML-skema skjult.</span><span class="sxs-lookup"><span data-stu-id="c13c9-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="c13c9-132">Udvid hver node ved at klikke på knappen **+** på noden.</span><span class="sxs-lookup"><span data-stu-id="c13c9-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="c13c9-133">For at udvide alle noder skal du vælge **Udvid alle** på båndet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="c13c9-134">Sådan markeres eller fjernes markeringen af noder i et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="c13c9-135">I feltet **Søg** skal du indtaste **XML-skemafremviser** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c13c9-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="c13c9-136">Udfyld felterne i sidehovedet som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c13c9-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="c13c9-137">Felt</span><span class="sxs-lookup"><span data-stu-id="c13c9-137">Field</span></span>|<span data-ttu-id="c13c9-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c13c9-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c13c9-139">**Kode til XML-skema**</span><span class="sxs-lookup"><span data-stu-id="c13c9-139">**XML Schema Code**</span></span>|<span data-ttu-id="c13c9-140">Angiv den XML-skemafil, du har indlæst i trin 5 i afsnittet "Sådan indlæses en XML-skemafil".</span><span class="sxs-lookup"><span data-stu-id="c13c9-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="c13c9-141">**Nyt XMLportnummer**</span><span class="sxs-lookup"><span data-stu-id="c13c9-141">**New XMLport No.**</span></span>|<span data-ttu-id="c13c9-142">Angiv nummeret på den XMLport, der er oprettet fra dette XML-skema, når du vælger handlingen **Generér XMLport**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="c13c9-143">Linjerne er nu udfyldt med noder, der repræsenterer alle elementer i XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="c13c9-144">Noder for elementer, der er obligatoriske i henhold til XML-skemaet, er som standard valgt.</span><span class="sxs-lookup"><span data-stu-id="c13c9-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="c13c9-145">På den første linje i kolonnen **Nodenavn** skal du udvide noden **Dokument** og derefter gradvist udvide underliggende noder, du vil gennemgå.</span><span class="sxs-lookup"><span data-stu-id="c13c9-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="c13c9-146">Alternativt kan du højreklikke på en node og derefter vælge **Udvid alle**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="c13c9-147">Brug fanen **Startside** og gruppen **Vis** til at vælge en af følgende handlinger for at ændre, hvilke noder der vises.</span><span class="sxs-lookup"><span data-stu-id="c13c9-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="c13c9-148">**Handling**</span><span class="sxs-lookup"><span data-stu-id="c13c9-148">**Action**</span></span>|<span data-ttu-id="c13c9-149">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c13c9-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="c13c9-150">**Vis alle**</span><span class="sxs-lookup"><span data-stu-id="c13c9-150">**Show All**</span></span>|<span data-ttu-id="c13c9-151">Alle noder vises.</span><span class="sxs-lookup"><span data-stu-id="c13c9-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="c13c9-152">**Skjul ikke-obligatoriske**</span><span class="sxs-lookup"><span data-stu-id="c13c9-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="c13c9-153">Der vises kun de noder, der repræsenterer elementer, der kræves i henhold til XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="c13c9-154">Disse noder er typisk angivet med **1** i feltet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="c13c9-155">Vælg **Vis alle** for at tilbageføre visningen.</span><span class="sxs-lookup"><span data-stu-id="c13c9-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="c13c9-156">**Skjul ikke-valgte**</span><span class="sxs-lookup"><span data-stu-id="c13c9-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="c13c9-157">Kun noder, hvor afkrydsningsfeltet **Markeret** er markeret, vises.</span><span class="sxs-lookup"><span data-stu-id="c13c9-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="c13c9-158">Vælg **Vis alle** for at tilbageføre visningen.</span><span class="sxs-lookup"><span data-stu-id="c13c9-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="c13c9-159">Under fanen **Startside** i gruppen **Administrer** skal du vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="c13c9-160">I afkrydsningsfeltet **Markeret** skal du angive for hver enkelt node, om elementet skal understøttes i dataudvekslingsdefinitionen for den relaterede SEPA-bankfil.</span><span class="sxs-lookup"><span data-stu-id="c13c9-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c13c9-161">Når du vælger en obligatorisk underordnet node, markeres alle overordnede noder ovenfor også.</span><span class="sxs-lookup"><span data-stu-id="c13c9-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="c13c9-162">Vælg handlingen **Marker alle obligatoriske elementer** for at markere alle noder, der repræsenterer elementer, der er obligatoriske i henhold til XML-skemaet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="c13c9-163">Vælg handlingen **Afmarker alt** for at rydde alle markeringer.</span><span class="sxs-lookup"><span data-stu-id="c13c9-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="c13c9-164">Feltet **Valg** angiver, om noden har to eller flere sidestillede noder, der fungerer som valgmuligheder.</span><span class="sxs-lookup"><span data-stu-id="c13c9-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="c13c9-165">Sådan oprettes en dataudvekslingsdefinition, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="c13c9-166">I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c13c9-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="c13c9-167">Vælg det relevante XML-skema, og vælg **Åbn XML-skemafremviser** i gruppen **Proces** under fanen **Startside**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="c13c9-168">Sørg for, at de relevante noder er valgt.</span><span class="sxs-lookup"><span data-stu-id="c13c9-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="c13c9-169">Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".</span><span class="sxs-lookup"><span data-stu-id="c13c9-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="c13c9-170">På siden **XML-skemafremviser** under fanen **Startside** skal du i gruppen **Proces** vælge **Generer dataudvekslingsdefinition**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-170">On the **XML Schema Viewer** page, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="c13c9-171">Der oprettes en dataudvekslingsdefinition på siden **Bogføringsudvekslingsdefinition**, som du kan afslutte ved at angive, hvilke elementer i filen, der skal knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c13c9-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c13c9-172">Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="c13c9-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c13c9-173">Du kan også bruge funktionen **Hent filstruktur** på siden **Bogføringsudvekslingsdefinition**, som bruger funktionerne på siden **XML-skemafremviser** til at udfylde oversigtspanelet **Kolonnedefinitioner**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="c13c9-174">Sådan oprettes en XMLport, der er baseret på et XML-skema</span><span class="sxs-lookup"><span data-stu-id="c13c9-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="c13c9-175">I feltet **Søg** skal du indtaste **XML-skemaer** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c13c9-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="c13c9-176">Vælg det relevante XML-skema, og vælg **Åbn XML-skemafremviser** i gruppen **Proces** under fanen **Startside**.</span><span class="sxs-lookup"><span data-stu-id="c13c9-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="c13c9-177">I feltet **Nyt XMLportnummer**</span><span class="sxs-lookup"><span data-stu-id="c13c9-177">In the **New XMLport No.**</span></span> <span data-ttu-id="c13c9-178">skal du angive det nummer, der tildeles det nye XMLport-objekt, når det er oprettet.</span><span class="sxs-lookup"><span data-stu-id="c13c9-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="c13c9-179">Sørg for, at de relevante noder er valgt.</span><span class="sxs-lookup"><span data-stu-id="c13c9-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="c13c9-180">Du kan finde flere oplysninger i afsnittet "Sådan markeres eller fjernes markeringen af noder i et XML-skema".</span><span class="sxs-lookup"><span data-stu-id="c13c9-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="c13c9-181">Brug fanen **Startside** og gruppen **Proces** til at vælge **Generér XMLPort**, og gem derefter objektet som en .txt-fil på en passende placering.</span><span class="sxs-lookup"><span data-stu-id="c13c9-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="c13c9-182">Indlæs den nye XMLport til [!INCLUDE[d365fin](includes/d365fin_md.md)]-udviklingsmiljøet, og kompiler den.</span><span class="sxs-lookup"><span data-stu-id="c13c9-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="c13c9-183">Se også</span><span class="sxs-lookup"><span data-stu-id="c13c9-183">See Also</span></span>  
<span data-ttu-id="c13c9-184">[Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="c13c9-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="c13c9-185">[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="c13c9-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="c13c9-186">[Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="c13c9-186">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="c13c9-187">Om Data Exchange Framework</span><span class="sxs-lookup"><span data-stu-id="c13c9-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

