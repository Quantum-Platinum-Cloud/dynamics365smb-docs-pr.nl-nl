---
title: Leveranciersbetalingen elektronisch versturen in de betalingsindeling SEPA ISO 20022
description: In Business Central kunt u elektronische SEPA-leveranciersbetalingen (Single Euro Payments Area) ISO 20022 maken en verzenden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fd1c4c2ffacb21fbb31854c8a16141340ac64bc6
ms.contentlocale: nl-nl
ms.lasthandoff: 03/22/2018

---
# <a name="submit-vendor-payments-electronically-in-sepa-iso-20022-payment-format"></a>Leveranciersbetalingen elektronisch versturen in SEPA ISO 20022-betalingsindeling
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u elektronische SEPA-leveranciersbetalingen (Single Euro Payments Area) ISO 20022 maken en verzenden.  

Voordat u SEPA-leveranciersbetalingen kunt maken en verzenden, moet u SEPA-betalingen activeren. Zie [SEPA-betalingen activeren](how-to-activate-sepa-payments.md) voor meer informatie.  

## <a name="to-submit-vendor-payments-electronically-in-sepa-iso-20022-payment-format"></a>Leverancierbetalingen elektronisch versturen in SEPA ISO 20022-betalingsindeling  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Telebankieren - bankoverzicht** in en kies de gerelateerde koppeling.  
2.  Selecteer de betreffende bankrekening en kies vervolgens de actie **Voorstel**.  
3.  Selecteer de betreffende leveranciersbankrekening en kies vervolgens de actie **Posten ophalen**.  
4.  Vul op het sneltabblad **Opties** van de batchverwerking **Voorstelposten ophalen** de velden in, zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Valutadatum**|Hier geeft u de valutadatum op.|  
    |**Vervaldatum contantkort.**|Hier geeft u de vervaldatum voor de contantkorting op.|  

5.  Selecteer in het sneltabblad **Transactiemodus** de gewenste filters.  
6.  Selecteer in het sneltabblad **Klantenpost** de gewenste filters.  
7.  Selecteer op het sneltabblad **Leverancierspost** het filter **Leveranciersnr.** en selecteer een leveranciersnummer.  

    > [!NOTE]  
    >  Selecteer eventuele overige vereiste filters.  

8.  Kies de knop **OK**.  

De voorstelregels worden opgenomen in het venster **Telebankierenvoorstel**.  

## <a name="see-also"></a>Zie ook  
 [SEPA-betalingen activeren](how-to-activate-sepa-payments.md)   
 [Single EURO Payments Area (SEPA)](single-euro-payments-area-sepa-.md)   
