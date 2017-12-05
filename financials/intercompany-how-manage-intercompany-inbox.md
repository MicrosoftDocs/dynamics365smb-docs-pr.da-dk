---
title: "Behandle indgående og udgående IC-transaktioner | Microsoft Docs"
description: IC-transaktioner, som du modtager fra koncerninterne partnere, vises i IC-indbakken, hvor du behandle dem manuelt eller automatisk.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5cf49fa7b1c2d4385cd05f44e10237078e1214a4
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-the-intercompany-inbox-and-outbox"></a><span data-ttu-id="94889-103">Fremgangsmåde: Administrere IC-indbakken og -udbakken</span><span class="sxs-lookup"><span data-stu-id="94889-103">How to: Manage the Intercompany Inbox and Outbox</span></span>
<span data-ttu-id="94889-104">Alle IC-transaktioner, som du modtager elektronisk fra koncerninterne partnere, vises i den koncerninterne indbakke.</span><span class="sxs-lookup"><span data-stu-id="94889-104">All of the intercompany transactions that you receive electronically from your intercompany partners are listed in the intercompany Inbox.</span></span>  

## <a name="organizing-the-inbox"></a><span data-ttu-id="94889-105">Organisere indbakken</span><span class="sxs-lookup"><span data-stu-id="94889-105">Organizing the Inbox</span></span>  
 <span data-ttu-id="94889-106">Du kan bruge filterfelterne øverst i indbakken til at bestemme, hvilke transaktioner der skal vises i vinduet.</span><span class="sxs-lookup"><span data-stu-id="94889-106">You can use the filter fields at the top of the inbox window to determine which transactions are shown in the window.</span></span> <span data-ttu-id="94889-107">Hvis du f.eks. kun vil have vist transaktioner oprettet af en bestemt partner, kan du angive det i filtrene **Transaktionskilde** og **Koncernintern partnerkode**.</span><span class="sxs-lookup"><span data-stu-id="94889-107">For example, if you only want to look at transactions a particular partner created, you can enter filters in the **Transaction Source** and **Intercompany Partner Code** filters.</span></span>  

### <a name="transaction-source"></a><span data-ttu-id="94889-108">Transaktionskilde</span><span class="sxs-lookup"><span data-stu-id="94889-108">Transaction Source</span></span>  
<span data-ttu-id="94889-109">Hvad du kan foretage dig med en transaktion, afhænger af om den er:</span><span class="sxs-lookup"><span data-stu-id="94889-109">What you can do with a transaction depends whether it was:</span></span>  

- <span data-ttu-id="94889-110">Oprettet af din koncerninterne partner</span><span class="sxs-lookup"><span data-stu-id="94889-110">Created by your intercompany partner</span></span>  
- <span data-ttu-id="94889-111">Afvist af din koncerninterne partner og returneret til dig</span><span class="sxs-lookup"><span data-stu-id="94889-111">Rejected by your intercompany partner and returned to you</span></span>  

<span data-ttu-id="94889-112">Du kan bruge feltet **Vis transaktionskilde** til at filtrere vinduet **Koncerninterne indbakketransaktioner**, så der kun vises én af disse typer transaktioner.</span><span class="sxs-lookup"><span data-stu-id="94889-112">You can use the **Show Transaction Source** field to filter the **Intercompany Inbox Transactions** window so that it displays only one of these types of transactions.</span></span> <span data-ttu-id="94889-113">Du kan også filtrere efter koncernintern partner eller efter oplysningerne i feltet **Linjehandling**.</span><span class="sxs-lookup"><span data-stu-id="94889-113">(You can also filter by intercompany partner, or by the contents of the **Line Action** field.)</span></span>  

#### <a name="created-by-intercompany-partner"></a><span data-ttu-id="94889-114">Oprettet af koncernintern partner</span><span class="sxs-lookup"><span data-stu-id="94889-114">Created by Intercompany Partner</span></span>  
 <span data-ttu-id="94889-115">Når du modtager en ny transaktion, der er oprettet af en partner, kan du vælge enten at:</span><span class="sxs-lookup"><span data-stu-id="94889-115">When you receive a new transaction that was created by your partner, you can choose to either:</span></span>

- <span data-ttu-id="94889-116">Acceptere transaktionen</span><span class="sxs-lookup"><span data-stu-id="94889-116">Accept the transaction</span></span>  
- <span data-ttu-id="94889-117">Afvise transaktionen (returnere den til partneren)</span><span class="sxs-lookup"><span data-stu-id="94889-117">Reject the transaction (Return to partner)</span></span>  
- <span data-ttu-id="94889-118">Annullere transaktionen (slette transaktionen uden at returnere den til partneren)</span><span class="sxs-lookup"><span data-stu-id="94889-118">Cancel the transaction (Delete the transaction but do not return it to your partner)</span></span>  

#### <a name="returned-from-intercompany-partner"></a><span data-ttu-id="94889-119">Returneret fra koncernintern partner</span><span class="sxs-lookup"><span data-stu-id="94889-119">Returned from Intercompany Partner</span></span>  
 <span data-ttu-id="94889-120">Hvis transaktionen blev afvist af din koncerninterne partner, har du kun mulighed for at annullere transaktionen i indbakken.</span><span class="sxs-lookup"><span data-stu-id="94889-120">If the transaction was rejected by your intercompany partner, your only choice is to cancel the transaction in the inbox.</span></span> <span data-ttu-id="94889-121">Derefter skal du oprette rettelseslinjer eller tilbageføre kladden eller dokumentet i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="94889-121">Then you must create correction lines or reverse the journal or document in your company.</span></span>  

## <a name="re-creating-inbox-entries"></a><span data-ttu-id="94889-122">Gendanne indbakkeposter</span><span class="sxs-lookup"><span data-stu-id="94889-122">Re-creating Inbox Entries</span></span>  
 <span data-ttu-id="94889-123">Hvis du har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.</span><span class="sxs-lookup"><span data-stu-id="94889-123">If you accepted a transaction in your inbox but then deleted the document or journal instead of posting it, you can re-create the inbox entry and accept it again.</span></span>  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a><span data-ttu-id="94889-124">Få vist en oversigt over IC-transaktioner i en periode</span><span class="sxs-lookup"><span data-stu-id="94889-124">Getting an Overview of Intercompany Transactions for a Period</span></span>  
 <span data-ttu-id="94889-125">Du kan få vist en oversigt over alle de IC-transaktioner, som du har sendt og modtaget i en periode.</span><span class="sxs-lookup"><span data-stu-id="94889-125">You can get an overview of all of the intercompany transactions that you have sent and received in a period.</span></span> <span data-ttu-id="94889-126">Brug rapporten **Koncerninterne transaktioner** til at se alle IC-finansposter, -debitorposter og -kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="94889-126">The **Intercompany Transactions** report lists all intercompany G/L entries, customer ledger entries, and vendor ledger entries.</span></span>

 > [!NOTE]  
 > <span data-ttu-id="94889-127">Hvis de koncerninterne partnere findes i samme database, overføres transaktioner uden brug af fil eller e-mail.</span><span class="sxs-lookup"><span data-stu-id="94889-127">If the intercompany partners are in the same database, then transactions are transferred without the need for file or email.</span></span> <span data-ttu-id="94889-128">Få vist feltet **Overførselstype** i vinduet **Koncernintern partner**.</span><span class="sxs-lookup"><span data-stu-id="94889-128">See the **Transfer Type** field in the **Intercompany Partner** window.</span></span> <br /><br />
<span data-ttu-id="94889-129">I så fald kan du indstille systemet til at spring indbakke og udbakke over ved at markere henholdsvis afkrydsningsfeltet **Automatisk accept af transaktioner** i vinduet **Koncernintern partner** og afkrydsningsfeltet **Automatisk afsendelse af transaktioner** i vinduet **Koncernintern opsætning**.</span><span class="sxs-lookup"><span data-stu-id="94889-129">In that case, you can set the system up to bypass the inbox and outbox by selecting the **Auto. Accept Transactions** check box in the **Intercompany Partner** window and the **Auto. Send Transactions** check box in the **Intercompany Setup** window respectively.</span></span>

## <a name="to-import-intercompany-transactions-from-a-file"></a><span data-ttu-id="94889-130">Sådan indlæses IC-transaktioner fra en fil</span><span class="sxs-lookup"><span data-stu-id="94889-130">To import intercompany transactions from a file</span></span>  
<span data-ttu-id="94889-131">Hvis du har en IC-partner, der ikke er med i den samme database som dit regnskab, kan du modtage IC-transaktioner fra partneren i en .xml-fil.</span><span class="sxs-lookup"><span data-stu-id="94889-131">If you have an intercompany partner that is not in the same database as your company, you can receive intercompany transactions from that partner in an .xml file.</span></span> <span data-ttu-id="94889-132">Derefter kan du indlæse transaktionerne til din indbakke.</span><span class="sxs-lookup"><span data-stu-id="94889-132">Then you must import the transactions into your inbox.</span></span>  

1.  <span data-ttu-id="94889-133">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Virksomhedsoplysninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94889-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Company Information** , and then choose the related link.</span></span>
2. <span data-ttu-id="94889-134">Gem filen på den placering, som du har angivet i feltet **Koncerninterne indbakkeoplysninger** i vinduet **Virksomhedsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="94889-134">Save the file to the location that you specified in the **Intercompany Inbox Details** field in the **Company Information** window.</span></span>  
3. <span data-ttu-id="94889-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94889-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Intercompany Inbox Transactions**, and then choose the related link.</span></span>
4. <span data-ttu-id="94889-136">I vinduet **Koncerninterne indbakketransaktioner** skal du vælge handlingen **Indlæs transaktionsfil**.</span><span class="sxs-lookup"><span data-stu-id="94889-136">In the **Intercompany Inbox Transactions** window, choose the **Import Transaction File** action.</span></span>  
5. <span data-ttu-id="94889-137">Marker den .xml-fil, der indeholder transaktionerne i det vindue, som vises, og vælg derefter knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="94889-137">In the window that appears, select the .xml file that contains the transactions, and then choose the **Open** button.</span></span>  

<span data-ttu-id="94889-138">Transaktioner indlæses nu til indbakken, hvor du kan arbejde med dem.</span><span class="sxs-lookup"><span data-stu-id="94889-138">The transactions are imported into the inbox and you can now process them.</span></span>

## <a name="to-process-incoming-intercompany-transactions"></a><span data-ttu-id="94889-139">Sådan behandles indgående IC-transaktioner</span><span class="sxs-lookup"><span data-stu-id="94889-139">To process incoming intercompany transactions</span></span>  
<span data-ttu-id="94889-140">Når dine partnere sender dig IC-transaktioner, ender transaktionerne i IC-indbakken.</span><span class="sxs-lookup"><span data-stu-id="94889-140">When your intercompany partners send you intercompany transactions, the transactions end up in your intercompany inbox.</span></span> <span data-ttu-id="94889-141">Du skal tage stilling til hver transaktion i indbakken og følge op på den.</span><span class="sxs-lookup"><span data-stu-id="94889-141">You must evaluate each transaction in your inbox and act upon it.</span></span>  

1. <span data-ttu-id="94889-142">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94889-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Intercompany Inbox Transactions**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94889-143">I vinduet **Koncerninterne indbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Accepter**, til behandling af linjen.</span><span class="sxs-lookup"><span data-stu-id="94889-143">In the **Intercompany Inbox Transactions** window, select a line, and then choose an action, such as **Accept**, to process the line.</span></span>
3. <span data-ttu-id="94889-144">I vinduet **Fuldfør IC-indbakkehandling** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="94889-144">In the **Complete IC Inbox Action** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="94889-145">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="94889-145">Choose the **OK** button.</span></span>  

<span data-ttu-id="94889-146">For linjer, som du har behandlet med handlingen **Accepter** oprettes dokument- eller kladdelinjer i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="94889-146">For lines that you processed with the **Accept** action, document or journal lines will be created in your company.</span></span> <span data-ttu-id="94889-147">Åbn hvert dokument eller hver kladde, foretag alle eventuelle ændringer, og bogfør dem derefter.</span><span class="sxs-lookup"><span data-stu-id="94889-147">Open each document or journal, make any necessary changes, and then post them.</span></span>  

<span data-ttu-id="94889-148">Linjer, som du har behandlet med handlingen **Returner til partner**, bliver flyttet til udbakken, hvorfra du derefter kan sende dem til partneren.</span><span class="sxs-lookup"><span data-stu-id="94889-148">Lines that you processed with the **Return to Partner** action will be moved to the outbox from where you can then send them to your partner.</span></span>

<span data-ttu-id="94889-149">For linjer, som du har behandlet med handlingen **Returneret af partner**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="94889-149">For lines that you processed with the **Returned by Partner** action, you must now post a correction to the original transaction that you posted in your company.</span></span>

## <a name="to-process-outgoing-intercompany-transactions"></a><span data-ttu-id="94889-150">Sådan håndteres udgående IC-transaktioner</span><span class="sxs-lookup"><span data-stu-id="94889-150">To process outgoing intercompany transactions</span></span>  
<span data-ttu-id="94889-151">Når du bogfører en IC-kladde eller et IC-dokument eller sender en IC-ordrebekræftelse, sendes transaktionerne til din IC-udbakke.</span><span class="sxs-lookup"><span data-stu-id="94889-151">When you post an intercompany journal or document, or send an intercompany order confirmation, the transactions are sent to your intercompany outbox.</span></span> <span data-ttu-id="94889-152">Du skal åbne udbakken og behandle transaktionerne, før de kan sendes til dine partnere.</span><span class="sxs-lookup"><span data-stu-id="94889-152">In order for them to be sent on to your intercompany partners, you must open the outbox and process them.</span></span>  

1.  <span data-ttu-id="94889-153">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne udbakketransaktioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94889-153">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Intercompany Outbox Transactions**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94889-154">I vinduet **Koncerninterne udbakketransaktioner** skal du vælge en linje og derefter vælge en handling, f.eks. **Returner til indbakke**, til behandling af linjen.</span><span class="sxs-lookup"><span data-stu-id="94889-154">In the **Intercompany Outbox Transactions** window, select a line, and then choose an action, such as **Return to Inbox**, to process the line.</span></span>

<span data-ttu-id="94889-155">Linjer, som du har behandlet med handlingen **Send til koncernintern partner**, sendes til den relevante partners indbakke.</span><span class="sxs-lookup"><span data-stu-id="94889-155">Lines that you processed with the **Send to Intercompany Partner** action will be sent to the relevant partner's inbox.</span></span>

<span data-ttu-id="94889-156">Linjer, som du har behandlet med handlingen **Returner til Indbakke**, flyttes til indbakken, hvor du derefter kan acceptere dem for at oprette dokumenter eller kladdelinjer i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="94889-156">Lines that you processed with the **Return to Inbox** action will be moved to the inbox where you can then accept them to create documents or journal lines in your company.</span></span>  

<span data-ttu-id="94889-157">For linjer, som du har behandlet med handlingen **Annuller**, skal du nu bogføre en rettelse af den oprindelige transaktion, som du har bogført i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="94889-157">For lines that you processed with the **Cancel** action, you must now post a correction to the original transaction that you posted in your company.</span></span>  

## <a name="to-recreate-intercompany-inbox-transactions"></a><span data-ttu-id="94889-158">Sådan gendannes transaktioner i ICindbakken</span><span class="sxs-lookup"><span data-stu-id="94889-158">To recreate intercompany inbox transactions</span></span>  
<span data-ttu-id="94889-159">Af og til vil du måske gendanne en transaktion i indbakken eller udbakken.</span><span class="sxs-lookup"><span data-stu-id="94889-159">Occasionally, you may want to re-create a transaction in the inbox or outbox.</span></span> <span data-ttu-id="94889-160">Hvis du f.eks. har accepteret en transaktion i indbakken, men efterfølgende har slettet dokumentet eller kladden i stedet for at bogføre den/det, kan du gendanne indbakkeposten og acceptere dokumentet eller kladden igen.</span><span class="sxs-lookup"><span data-stu-id="94889-160">For example, if you accepted a transaction in your inbox but then deleted the document or journal instead of posting it, you can re-create the inbox entry and accept it again.</span></span>  

<span data-ttu-id="94889-161">Følgende procedure beskriver, hvordan du gendanner transaktioner i indbakken, men proceduren er den samme for udbakken.</span><span class="sxs-lookup"><span data-stu-id="94889-161">The following procedure describes to re-create inbox transactions, but the same steps also apply to the outbox.</span></span>

  1.  <span data-ttu-id="94889-162">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Koncerninterne indbakketransaktioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="94889-162">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Handled IC Inbox Transactions**, and then choose the related link.</span></span>  

  2.  <span data-ttu-id="94889-163">I vinduet **Håndterede IC-indbakketransaktioner**, skal du markere linjen med den transaktion, som du vil gendanne i indbakken, og derefter vælge handlingen **Genopret indbakketransaktion**.</span><span class="sxs-lookup"><span data-stu-id="94889-163">In the **Handled IC Inbox Transactions** window, select the line with the transaction that you want to re-create in the inbox, and then choose the **Re-create Inbox Transaction** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94889-164">Se også</span><span class="sxs-lookup"><span data-stu-id="94889-164">See Also</span></span>
[<span data-ttu-id="94889-165">Administrere Intercompany-transaktioner (IC)</span><span class="sxs-lookup"><span data-stu-id="94889-165">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="94889-166">Finans</span><span class="sxs-lookup"><span data-stu-id="94889-166">Finance</span></span>](finance.md)  
[<span data-ttu-id="94889-167">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="94889-167">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="94889-168">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="94889-168">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="94889-169">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94889-169">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
