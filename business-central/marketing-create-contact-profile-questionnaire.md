---
title: Bruge profiler til at klassificere kontakter
description: Definere profilspørgeskemaer for at klassificere dine forretningskontakter
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2020
ms.openlocfilehash: ef8b2c90ef01841e2c641b9fc96348d899d4997e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919334"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="0fb19-103">Bruge profilspørgeskemaer til at klassificere forretningskontakter</span><span class="sxs-lookup"><span data-stu-id="0fb19-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="0fb19-104">Du kan definere profilspørgeskemaer, du vil bruge til indtastning af oplysninger om kontaktprofiler.</span><span class="sxs-lookup"><span data-stu-id="0fb19-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="0fb19-105">Du kan i det enkelte spørgeskema definere forskellige spørgsmål, du vil stille dine kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="0fb19-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="0fb19-106">Du kan også køre spørgeskemaet for at besvare nogle af spørgsmålene automatisk ud fra kontakt-, debitor- eller kreditordata.</span><span class="sxs-lookup"><span data-stu-id="0fb19-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="0fb19-107">Sådan tilføjes et profilspørgeskema</span><span class="sxs-lookup"><span data-stu-id="0fb19-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="0fb19-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af spørgeskema**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="0fb19-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0fb19-109">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="0fb19-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="0fb19-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="0fb19-111">Sådan føjes spørgsmål til et profilspørgeskema</span><span class="sxs-lookup"><span data-stu-id="0fb19-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="0fb19-112">Vælg det relevante profilspørgeskema, og vælg handlingen **Rediger opsætning af spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="0fb19-113">I den første tomme linje skal du i feltet **Type** vælge **Spørgsmål** og skrive dit spørgsmål i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="0fb19-114">Udfyld de andre felter på linjen.</span><span class="sxs-lookup"><span data-stu-id="0fb19-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="0fb19-115">Vælg **Svar** i den næste tomme linje i feltet **Type**, og skriv svaret i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="0fb19-116">Vælg prioriteten i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="0fb19-117">I felterne **Fra-værdi** og **Til-værdi** defineres et interval.</span><span class="sxs-lookup"><span data-stu-id="0fb19-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="0fb19-118">Kontakter, der modtager point inden for det angivne interval, får svaret.</span><span class="sxs-lookup"><span data-stu-id="0fb19-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="0fb19-119">Gentag disse trin for at indtaste alle spørgsmål og svar i profilspørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="0fb19-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="0fb19-120">Når du har oprettet et spørgeskema, skal du oprette kontaktpersonvurderinger til at klassificere dine kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="0fb19-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="0fb19-121">Du kan også oprette spørgsmål, der klassificeres automatisk baseret på oplysningerne på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="0fb19-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="0fb19-122">Hvis du angiver et spørgsmål, som skal besvares automatisk, skal du vælge <STRONG>Linje</STRONG> og derefter vælge <STRONG>Oplysn. om spørgsmål</STRONG> for at angive de kriterier, som skal anvendes ved den automatiske besvarelse.</span><span class="sxs-lookup"><span data-stu-id="0fb19-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="0fb19-123">Den automatiske klassificering af kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="0fb19-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="0fb19-124">Du kan automatisk klassificere kontakter efter debitor-, kreditor- og kontaktoplysninger ved at definere automatisk besvarede profilspørgsmål på siden **Opsætn. af profilspørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="0fb19-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="0fb19-125">Det er kun kontakter, der er registrerede som debitorer, som kan få tildelt en klassificering ud fra debitordata, og kun kontakter registreret som kreditorer kan tildeles en klassificering ud fra kreditordata.</span><span class="sxs-lookup"><span data-stu-id="0fb19-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="0fb19-126">Klassificeringen opdateres ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="0fb19-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="0fb19-127">Det kan derfor være nødvendigt at opdatere profilspørgeskemaerne, hvis du har opdateret de debitor-, kreditor- eller kontaktdata, som de er baseret på.</span><span class="sxs-lookup"><span data-stu-id="0fb19-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="0fb19-128">Hvis du har angivet automatisk besvarede profilspørgsmål, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk de korrekte svar for kontakterne, når du tildeler en kontakt et profilspørgeskema med de pågældende spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="0fb19-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="0fb19-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0fb19-129">Example</span></span>
<span data-ttu-id="0fb19-130">Du kan klassificere kontakter efter deres købsbeløb.</span><span class="sxs-lookup"><span data-stu-id="0fb19-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fb19-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="0fb19-132"><strong>Gælder for</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fb19-133">A</span><span class="sxs-lookup"><span data-stu-id="0fb19-133">A</span></span></p></td>
<td><p><span data-ttu-id="0fb19-134">Kontakter, der har købt for mindst RV 500.000</span><span class="sxs-lookup"><span data-stu-id="0fb19-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb19-135">B</span><span class="sxs-lookup"><span data-stu-id="0fb19-135">B</span></span></p></td>
<td><p><span data-ttu-id="0fb19-136">Kontakter, der har købt for mellem RV 100.000 og 499.999.</span><span class="sxs-lookup"><span data-stu-id="0fb19-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fb19-137">U</span><span class="sxs-lookup"><span data-stu-id="0fb19-137">C</span></span></p></td>
<td><p><span data-ttu-id="0fb19-138">Kontakter, der har købt for højst RV 99.999</span><span class="sxs-lookup"><span data-stu-id="0fb19-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0fb19-139">Det gør du ved at udfylde siden **Opsætn. af profilspørgeskema** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0fb19-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fb19-140"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="0fb19-141"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="0fb19-142"><strong>Automatisk klassificering</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="0fb19-143"><strong>Fra værdi</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="0fb19-144"><strong>Til værdi</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fb19-145">Spørgsmål</span><span class="sxs-lookup"><span data-stu-id="0fb19-145">Question</span></span></p></td>
<td><p><span data-ttu-id="0fb19-146">ABC-klassificering</span><span class="sxs-lookup"><span data-stu-id="0fb19-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="0fb19-147">Indsæt markering ved at klikke</span><span class="sxs-lookup"><span data-stu-id="0fb19-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb19-148">Svar</span><span class="sxs-lookup"><span data-stu-id="0fb19-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="0fb19-149">T</span><span class="sxs-lookup"><span data-stu-id="0fb19-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0fb19-150">500,000</span><span class="sxs-lookup"><span data-stu-id="0fb19-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fb19-151">Svar</span><span class="sxs-lookup"><span data-stu-id="0fb19-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="0fb19-152">B</span><span class="sxs-lookup"><span data-stu-id="0fb19-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0fb19-153">100,000</span><span class="sxs-lookup"><span data-stu-id="0fb19-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="0fb19-154">499,999</span><span class="sxs-lookup"><span data-stu-id="0fb19-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb19-155">Svar</span><span class="sxs-lookup"><span data-stu-id="0fb19-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="0fb19-156">U</span><span class="sxs-lookup"><span data-stu-id="0fb19-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0fb19-157">99,999</span><span class="sxs-lookup"><span data-stu-id="0fb19-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0fb19-158">Udfyld derefter siden **Oplysninger om profilspørgsmål** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="0fb19-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0fb19-159"><strong>Felt</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="0fb19-160"><strong>Værdi</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0fb19-161"><strong>Debitorklassifikationsfelt</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="0fb19-162"><emphasis>Salg (RV)</emphasis></span><span class="sxs-lookup"><span data-stu-id="0fb19-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0fb19-163"><strong>Klassificeringsmetode</strong></span><span class="sxs-lookup"><span data-stu-id="0fb19-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="0fb19-164"><emphasis>Defineret værdi</emphasis></span><span class="sxs-lookup"><span data-stu-id="0fb19-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0fb19-165">Når du tildeler et profilspørgeskema med disse spørgsmål til en kontakt, udfyldes de relevante svar for kontakten automatisk på profillinjerne på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="0fb19-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fb19-166">Se også</span><span class="sxs-lookup"><span data-stu-id="0fb19-166">See Also</span></span>
[<span data-ttu-id="0fb19-167">Oprettelse af kontakter</span><span class="sxs-lookup"><span data-stu-id="0fb19-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
