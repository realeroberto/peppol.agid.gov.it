---
layout: page
title: Sorting node for public administration purchase orders (NSO)
description:
lang: en
ref: nso
order: 3
child_of_ref: insights
---

As required by the 2018 Budget Law, starting from the date that will be established with specific ministerial decrees,
purchasing in the public procurement process related to health sector will be handled with electronic orders.
NSO, the “Sorting node for public administration purchase orders” managed by the Ministry of Economy and Finance (MEF),
is the central gateway for exchanging eOrders between public bodies and suppliers.

The eOrder format adopted by NSO is compliant with the PEPPOL BIS 3.0 <a aria-label="PEPPOL BIS 3.0 - External link" href="https://docs.peppol.eu/poacc/upgrade-3/" title="External link">technical specifications</a>.

More information on NSO can be found on the <a aria-label="Ministry of Economy and Finance - External link" href="http://www.rgs.mef.gov.it/VERSIONE-I/e_government/amministrazioni_pubbliche/acquisti_pubblici_in_rete_apir/nodo_di_smistamento_degli_ordini_di_acquisto_delle_amministrazioni_pubbliche_nso/" title="External link">MEF website</a>.

PPEPPOL, among other channels, is supported by NSO as official infrastructure for transmitting eOrders.

## PEPPOL and NSO

According to NSO’s technical rules, the buyer must interact with NSO in order to validate an eOrder document:
this action can be taken directly by the buyer or an intermediary prior to sending the document.

If the eOrder is addressed to a supplier, whose identifier is given by a PEPPOL Participant ID,
then the message will be delivered through the PEPPOL network. This means that if you are an Access Point (AP)
Service Provider and your clients need to receive eOrder documents from an Italian public body,
then there are no actions to be taken as the PEPPOL specifications will be enough to receive the message.

Instead, if you are an AP Service Provider that acts as intermediary for an
Italian public administration (buyer), then you need to adopt one of the
channels available to communicate with NSO for the validation step prior to
forwarding the eOrder on the PEPPOL network. The channels are the same
available for the SdI, the national <a aria-label="FatturaPa - External link"
href="https://www.fatturapa.gov.it/export/fatturazione/en/normativa/f-3.htm"
title="External link">Invoice Exchange Gateway</a>.

Nevertheless, complex scenario that require the supplier to reply to the buyer (like “Ordering” and “Order agreement”)
could require different actions to the AP Service Providers. More detailed specifications are available on the
<a aria-label="Ministry of Economy and Finance - External link" href="http://www.rgs.mef.gov.it/VERSIONE-I/e_government/amministrazioni_pubbliche/acquisti_pubblici_in_rete_apir/nodo_di_smistamento_degli_ordini_di_acquisto_delle_amministrazioni_pubbliche_nso/" title="External link">MEF website</a>.
