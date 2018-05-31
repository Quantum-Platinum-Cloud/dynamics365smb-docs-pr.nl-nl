---
title: Een prioriteitsniveau toewijzen aan een leverancier | Microsoft Docs
description: U kunt nummers toewijzen aan uw leveranciers om deze te prioriteren en betalingsvoorstellen in Business Central te vergemakkelijken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f7834f0f99b775125425eb7209c3c648de4ccd1f
ms.contentlocale: nl-nl
ms.lasthandoff: 03/22/2018

---
# <a name="prioritize-vendors"></a>De prioriteit van leveranciers bepalen
[!INCLUDE[d365fin](includes/d365fin_md.md)] heeft een functie die voorstellen kan doen voor betalingen aan leveranciers, bijvoorbeeld bij betalingen die binnenkort moeten worden betaald, of als voor een betaling een korting mogelijk is. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).

Eerst moet u aan uw leveranciers eerst een prioriteit toewijzen door nummers aan hen toe te wijzen.

## <a name="to-prioritize-vendors"></a>Leveranciers in een prioriteitsvolgorde plaatsen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de relevante leverancier en kies **Bewerken**.
3. Voer in het veld **Prioriteit** een nummer in.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] heeft het laagste nummer, 0 uitgezonderd, de hoogste prioriteit. Als u bijvoorbeeld de nummers 1, 2 en 3 toewijst, heeft nummer 1 de hoogste prioriteit.

Als u geen prioriteitsnummer wilt toekennen aan een leverancier, laat u het veld **Prioriteit** leeg. Die leverancier wordt onder alle leveranciers met prioriteitsnummers geplaatst wanneer u betalingsvoorstellen in het programma inschakelt. U kunt zo veel prioriteitsniveaus invoeren als er nodig zijn.

## <a name="see-also"></a>Zie ook
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
