---
title: Bruge profiler til at klassificere kontakter
description: "Definere profilspørgeskemaer for at klassificere dine forretningskontakter"
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 10/01/2018
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6a69a5de1ac0d6e2d238415204ec95fad9af7b9b
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="f1935-103">Bruge profilspørgeskemaer til at klassificere forretningskontakter</span><span class="sxs-lookup"><span data-stu-id="f1935-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="f1935-104">Du kan definere profilspørgeskemaer, du vil bruge til indtastning af oplysninger om kontaktprofiler.</span><span class="sxs-lookup"><span data-stu-id="f1935-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="f1935-105">Du kan i det enkelte spørgeskema definere forskellige spørgsmål, du vil stille dine kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="f1935-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="f1935-106">Du kan også køre spørgeskemaet for at besvare nogle af spørgsmålene automatisk ud fra kontakt-, debitor- eller kreditordata.</span><span class="sxs-lookup"><span data-stu-id="f1935-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="f1935-107">Sådan tilføjes et profilspørgeskema</span><span class="sxs-lookup"><span data-stu-id="f1935-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="f1935-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af spørgeskema**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f1935-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f1935-109">Under fanen **Startside** i gruppen **Ny** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f1935-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="f1935-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f1935-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="f1935-111">Sådan føjes spørgsmål til et profilspørgeskema</span><span class="sxs-lookup"><span data-stu-id="f1935-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="f1935-112">Vælg det relevante profilspørgeskema, og gå til fanen **Start**, og vælg **Rediger opsætning af spørgeskema** i gruppen **Proces**.</span><span class="sxs-lookup"><span data-stu-id="f1935-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="f1935-113">I den første tomme linje skal du i feltet **Type** vælge **Spørgsmål** og skrive dit spørgsmål i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f1935-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="f1935-114">Udfyld de andre felter på linjen.</span><span class="sxs-lookup"><span data-stu-id="f1935-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="f1935-115">Vælg **Svar** i den næste tomme linje i feltet **Type**, og skriv svaret i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f1935-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="f1935-116">Vælg prioriteten i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="f1935-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="f1935-117">I felterne **Fra-værdi** og **Til-værdi** defineres et interval.</span><span class="sxs-lookup"><span data-stu-id="f1935-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="f1935-118">Kontakter, der modtager point inden for det angivne interval, får svaret.</span><span class="sxs-lookup"><span data-stu-id="f1935-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="f1935-119">Gentag disse trin for at indtaste alle spørgsmål og svar i profilspørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="f1935-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="f1935-120">Når du har oprettet et spørgeskema, skal du oprette kontaktpersonvurderinger til at klassificere dine kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="f1935-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="f1935-121">Du kan også oprette spørgsmål, der klassificeres automatisk baseret på oplysningerne på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="f1935-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="f1935-122">Hvis du angiver et spørgsmål, som skal besvares automatisk, skal du vælge <STRONG>Linje</STRONG> og derefter vælge <STRONG>Oplysn. om spørgsmål</STRONG> for at angive de kriterier, som skal anvendes ved den automatiske besvarelse.</span><span class="sxs-lookup"><span data-stu-id="f1935-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="f1935-123">Den automatiske klassificering af kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="f1935-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="f1935-124">Du kan automatisk klassificere kontakter efter debitor-, kreditor- og kontaktoplysninger ved at definere automatisk besvarede profilspørgsmål i vinduet **Opsætn. af profilspørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="f1935-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions in the **Profile Questionnaire Setup** window.</span></span>  

> [!NOTE]
> <span data-ttu-id="f1935-125">Det er kun kontakter, der er registrerede som debitorer, som kan få tildelt en klassificering ud fra debitordata, og kun kontakter registreret som kreditorer kan tildeles en klassificering ud fra kreditordata.</span><span class="sxs-lookup"><span data-stu-id="f1935-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="f1935-126">Klassificeringen opdateres ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1935-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="f1935-127">Det kan derfor være nødvendigt at opdatere profilspørgeskemaerne, hvis du har opdateret de debitor-, kreditor- eller kontaktdata, som de er baseret på.</span><span class="sxs-lookup"><span data-stu-id="f1935-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="f1935-128">Hvis du har angivet automatisk besvarede profilspørgsmål, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk de korrekte svar for kontakterne, når du tildeler en kontakt et profilspørgeskema med de pågældende spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="f1935-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="f1935-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f1935-129">Example</span></span>
<span data-ttu-id="f1935-130">Du kan klassificere kontakter efter deres købsbeløb.</span><span class="sxs-lookup"><span data-stu-id="f1935-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1935-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="f1935-132"><strong>Gælder for</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1935-133">A</span><span class="sxs-lookup"><span data-stu-id="f1935-133">A</span></span></p></td>
<td><p><span data-ttu-id="f1935-134">Kontakter, der har købt for mindst RV 500.000</span><span class="sxs-lookup"><span data-stu-id="f1935-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1935-135">B</span><span class="sxs-lookup"><span data-stu-id="f1935-135">B</span></span></p></td>
<td><p><span data-ttu-id="f1935-136">Kontakter, der har købt for mellem RV 100.000 og 499.999.</span><span class="sxs-lookup"><span data-stu-id="f1935-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1935-137">C</span><span class="sxs-lookup"><span data-stu-id="f1935-137">C</span></span></p></td>
<td><p><span data-ttu-id="f1935-138">Kontakter, der har købt for højst RV 99.999</span><span class="sxs-lookup"><span data-stu-id="f1935-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1935-139">Det gør du ved at udfylde vinduet **Opsætn. af profilspørgeskema** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f1935-139">To do this, fill in the **Profile Questionnaire Setup** window as follows:</span></span>


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
<th><span data-ttu-id="f1935-140"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="f1935-141"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="f1935-142"><strong>Automatisk klassificering</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="f1935-143"><strong>Fra værdi</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="f1935-144"><strong>Til værdi</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1935-145">Spørgsmål</span><span class="sxs-lookup"><span data-stu-id="f1935-145">Question</span></span></p></td>
<td><p><span data-ttu-id="f1935-146">ABC-klassificering</span><span class="sxs-lookup"><span data-stu-id="f1935-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="f1935-147">Indsæt markering ved at klikke</span><span class="sxs-lookup"><span data-stu-id="f1935-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1935-148">Svar</span><span class="sxs-lookup"><span data-stu-id="f1935-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="f1935-149">A</span><span class="sxs-lookup"><span data-stu-id="f1935-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f1935-150">500,000</span><span class="sxs-lookup"><span data-stu-id="f1935-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1935-151">Svar</span><span class="sxs-lookup"><span data-stu-id="f1935-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="f1935-152">B</span><span class="sxs-lookup"><span data-stu-id="f1935-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f1935-153">100,000</span><span class="sxs-lookup"><span data-stu-id="f1935-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="f1935-154">499,999</span><span class="sxs-lookup"><span data-stu-id="f1935-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1935-155">Svar</span><span class="sxs-lookup"><span data-stu-id="f1935-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="f1935-156">L</span><span class="sxs-lookup"><span data-stu-id="f1935-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f1935-157">99,999</span><span class="sxs-lookup"><span data-stu-id="f1935-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1935-158">Udfyld derefter vinduet **Oplysninger om profilspørgsmål** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f1935-158">Then fill in the **Profile Question Details** window as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1935-159"><strong>Felt</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="f1935-160"><strong>Værdi</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f1935-161"><strong>Debitorklassifikationsfelt</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="f1935-162"><emphasis>Salg (RV)</emphasis></span><span class="sxs-lookup"><span data-stu-id="f1935-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f1935-163"><strong>Klassificeringsmetode</strong></span><span class="sxs-lookup"><span data-stu-id="f1935-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="f1935-164"><emphasis>Defineret værdi</emphasis></span><span class="sxs-lookup"><span data-stu-id="f1935-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f1935-165">Når du tildeler et profilspørgeskema med disse spørgsmål til en kontakt, udfyldes de relevante svar for kontakten automatisk på profillinjerne på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="f1935-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1935-166">Se også</span><span class="sxs-lookup"><span data-stu-id="f1935-166">See Also</span></span>
[<span data-ttu-id="f1935-167">Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="f1935-167">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="f1935-168">Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="f1935-168">Create Contact Persons</span></span>](marketing-how-create-contact-persons.md)  
[<span data-ttu-id="f1935-169">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="f1935-169">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  

