---
title: 'Procedure: Inkomsten en kosten uitstellen'
description: 'Als u inkomsten en kosten wilt verantwoorden in perioden waarin de transactie niet is geboekt, kunt u kosten en inkomsten automatisch uitstellen via een opgegeven schema.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="defer-revenues-and-expenses" />Procedure: Inkomsten en kosten uitstellen

Als u inkomsten of kosten wilt verantwoorden in een andere periode dan waarin de transactie is geboekt, kunt u deze functionaliteit gebruiken om kosten en inkomsten automatisch uit te stellen via een opgegeven schema.

Om kosten of omzet over de betrokken boekhoudperioden te verdelen stelt u een uitstelsjabloon in voor de bron, het artikel of de grootboekrekening waarnaar de inkomsten of kosten worden geboekt. Wanneer u het gerelateerde verkoop- of inkoopdocument boekt, worden de inkomsten of kosten uitgesteld tot de betrokken boekhoudperioden, volgens een uitstelschema dat wordt bepaald door instellingen in de uitstelsjabloon en de boekingsdatum.

## <a name="to-set-up-a-gl-account-for-deferral" />Een grootboekrekening instellen voor uitstel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de velden in om een grootboekrekening te maken voor uitgestelde inkomsten. Zie voor meer informatie [Het grootboek en het rekeningschema](finance-general-ledger.md).
4. Herhaal stap 2 en 3 om een nieuwe grootboekrekening te maken voor uitgestelde kosten.

Selecteer voor beide soorten uitstel **Balans** in het veld **Type** en geef de rekeningen geschikte namen, zoals "Niet-gerealiseerde onkosten" voor uitgestelde inkomsten en "Niet-gerealiseerde onkosten" voor uitgestelde onkosten.

## <a name="to-set-up-a-deferral-template" />Een uitstelsjabloon instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Uitstelsjablonen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in.
4. Geef in het veld **Berekeningsmethode** op hoe het veld **Bedrag** voor elke periode op de pagina **Uitstelschema** wordt berekend. U hebt de volgende mogelijkheden:

   * **Lineair**: de periodieke uitstelbedragen worden berekend volgens het aantal perioden, verdeeld volgens de periodelengte.
   * **Gelijk per periode**: de periodieke uitstelbedragen worden berekend volgens het aantal perioden, gelijkelijk verdeeld over perioden.
   * **Dagen per periode**: de periodieke uitstelbedragen worden berekend volgens het aantal dagen in de periode.
   * **Door gebruiker gedefinieerd**: de periodieke uitstelbedragen worden niet berekend. U moet het veld **Bedrag** handmatig invullen voor elke periode op de pagina Uitstelschema. Zie voor meer informatie het gedeelte "Een uitstelschema wijzigen vanuit een verkoopfactuur".
5. Geef in het veld **Periodebeschrijving** een beschrijving op die wordt weergegeven op posten voor de uitstelboeking. U kunt de volgende codes voor tijdelijke aanduidingen invoeren voor veel voorkomende waarden, die automatisch worden ingevoegd wanneer de periodebeschrijving wordt weergegeven.

   * %1 = het dagnummer van de periodeboekingsdatum
   * %2 = het weeknummer van de periodeboekingsdatum
   * %3 = het maandnummer van de periodeboekingsdatum
   * %4 = de maandnaam van de periodeboekingsdatum
   * %5 = de boekhoudperiodenaam van de periodeboekingsdatum
   * %6 = het boekjaar van de periodeboekingsdatum

Voorbeeld: de boekingsdatum is 06-02-2016. Als u 'Kosten uitgesteld voor %4%6' invoert, wordt de weergegeven beschrijving 'Kosten uitgesteld voor februari 2016'.

## <a name="to-assign-a-deferral-template-to-an-item" />Een uitstelsjabloon toewijzen aan een artikel

> [!NOTE]  
> De stappen in deze procedure zijn hetzelfde als wanneer u een uitstelsjabloon toewijst aan een grootboekrekening of een resource.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor het artikel waarvoor de inkomsten en de kosten moeten worden uitgesteld naar de boekhoudperioden waarin het artikel is verkocht of gekocht.
3. Selecteer in het veld **Standaarduitstellingssjabloon** de relevante uitstelsjabloon.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice" />Een uitstelschema wijzigen vanuit een verkoopfactuur

> [!NOTE]  
> De stappen in deze procedure zijn hetzelfde als wanneer u een uitstelschema voor onkosten wijzigt vanuit een inkoopfactuur.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.
2. Maak een verkoopfactuur voor een artikel waaraan een uitstelsjabloon is toegewezen. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.

    U ziet dat wanneer u het artikel (of de bron of grootboekrekening) op de factuurregel invoert, het veld **Uitstelcode** wordt gevuld met de code van de toegewezen uitstelsjabloon.
3. Kies de actie **Uitstelschema**.
4. Wijzig op de pagina **Uitstelschema** instellingen in de kop of waarden op de regels, bijvoorbeeld om het bedrag naar een extra boekhoudperiode uit te stellen.
5. Kies de actie **Schema berekenen**.
6. Kies de knop **Ok**. Het uitstelschema wordt bijgewerkt voor de verkoopfactuur. De relateerde uitstelsjabloon is ongewijzigd.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger" />Zien hoe uitgestelde kosten of inkomsten naar het grootboek worden geboekt

> [!NOTE]  
> De stappen in deze procedure zijn hetzelfde als wanneer u bekijkt hoe uitgestelde onkosten worden geboekt.

1. Kies op de pagina **Verkoopfactuur** de actie **Voorbeeld van boeking weergeven**.
2. Kies op de pagina **Voorbeeld van boeking weergeven** de actie **Grootboekpost** en kies vervolgens de actie **Verwante posten weergeven**.

Grootboekposten die moeten worden geboekt naar de opgegeven uitstelrekening, bijvoorbeeld Niet-gerealiseerde inkomsten, worden aangegeven door de beschrijving die u hebt ingevoerd in het veld **Periodebeschrijving** in de uitstelsjabloon, bijvoorbeeld 'Uitgestelde kosten voor februari 2016'.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report" />Geboekte uitstellingen bekijken in het rapport Overzicht van verkoopuitstel

> [!NOTE]  
> De stappen in deze procedure zijn hetzelfde als wanneer u het rapport Overzicht van inkoopuitstel bekijkt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Overzicht van verkoopuitstel** in en kies vervolgens de gerelateerde koppeling.
2. Voer op de pagina **Overzicht van verkoopuitstel** in het veld **Saldo per** de datum in tot wanneer u uitgestelde inkomsten wilt zien.
3. Kies de knop **Voorbeeld**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting" />Een periode opgeven waarin uitstelboeking wordt toegestaan

U kunt een periode opgeven waarin mensen transacties kunnen boeken door datums in de velden **Boeken toestaan vanaf** en **Boeken toestaan tot** als volgt in te voeren:

* Voor alle gebruikers, op de pagina **Grootboekinstellingen**
* Voor specifieke gebruikers, op de pagina **Gebruikersinstellingen**

Als u dat hebt gedaan, moet u een uitzondering maken voor uitstel, zodat ze buiten de periode kunnen worden geboekt. Als u de periode wilt definiëren, volgt u deze stappen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekinstellingen** of **Gebruikerisnstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Voer in de velden **Uitstelboeking toestaan vanaf** en **Uitstelboeking toestaan tot** een begin- en einddatum voor de periode in.

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-central" />Zie gerelateerde [Microsoft-training](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
