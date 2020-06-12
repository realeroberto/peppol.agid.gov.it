---
layout: page
title: Electronic Ordering
description:
lang: en
ref: e-ordering
order: 2
child_of_ref: insights
---

The **Italian 2018 Budget Law** (Law no. 205 of 27 December 2017), **paragraphs
411-414**, provides that all **purchase orders** by the public administration
**must be transmitted in electronic format** through the NSO (“[Nodo
Smistamento Ordini della Pubblica
Amministrazione](http://www.rgs.mef.gov.it/VERSIONE-I/e_government/amministrazioni_pubbliche/acquisti_pubblici_in_rete_apir/nodo_di_smistamento_degli_ordini_di_acquisto_delle_amministrazioni_pubbliche_nso/)”),
managed by the Ministry of Economy and Finance (MEF).

The **Decree of 7 December 2018** by MEF provided for the methods,
implementation times and the obligation, in the first phase, for the healthcare
companies of the National Health Service (SSN) starting from 1 October 2019. The
**MEF Decree of 27 December 2019** subsequently changed the starting date of the
obligation as follows:

-   February 1, 2020 for orders relating to goods;

-   January 1, 2021 for orders relating to services.

The **NSO** system is the **central infrastructure** for the exchange of
electronic orders between public bodies and suppliers, which, in addition to
the traditional channels (PEC, FTP, WS), also provides for the transmission of
documents over the PEPPOL network. To this end, NSO natively adopts the PEPPOL
BIS 3 (UBL) [technical specifications](https://peppol-docs.agid.gov.it/) for
the ordering, the order only and the order agreement.

Suppliers already registered on the PEPPOL network can interact with NSO without
further developments, as described below for the Validation and Transmission
with a third party scenarios.

**VALIDATION SCENARIO**

The **Validation** scenario takes place if and only if both the sender and the
recipient are registered on PEPPOL SMP/SML; in such a case, the NSO validates
the order but the transmission occurs entirely over the PEPPOL network.

This scenario assumes that the Public Administration makes use of a Service
Provider which is at the same time **Certified Peppol Access Point** and
**authorised intermediary** towards NSO.

<figure class="figure">
  <img src="/assets/images/e-ordering-1-en.png" class="figure-img img-fluid rounded" alt="Validation scenario">
  <figcaption class="figure-caption text-center">Validation scenario</figcaption>
</figure>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">STEP</th>
      <th scope="col">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">0</th>
      <td>The Supplier (Corner 4) has a PEPPOL Participant ID registered on SMP/SML</td>
    </tr>
    <tr>
      <th scope="row">1</th>
      <td>The Public Administration (Corner 1) sends the PEPPOL BIS 3 order to its Access Point Provider (Corner 2) specifying the recipient (PEPPOL Participant ID of the Supplier - Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>The Access Point Provider of the Public Administration (Corner 2) sends the order to NSO using the traditional channels provided by NSO in order to obtain a validation notification</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>The Access Point Provider (Corner 2) uses PEPPOL’s dynamic discovery (lookup on SML and SMP) to identify the Access Point Provider of the Supplier (Corner 3) to which the order must be delivered</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>The Access Point Provider of the Public Administration (Corner 2) forwards the order to the Supplier’s Access Point Provider (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>The Supplier’s Access Point Provider (Corner 3) confirms reception of the order at the Access Point Provider of the Public Administration (Corner 2) with a “Message Disposition Notification” (MDN) sent over the PEPPOL network; at the same time, it makes the order available to the Supplier (Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>The Access Point Provider of the Public Administration (Corner 2) sends a notification as the outcome of the transmission to the original sender of the order (Corner 1 - Public Administration), using a notification type agreed between the parties</td>
    </tr>
  </tbody>
</table>

**TRANSMISSION SCENARIO WITH THIRD PARTY**

The **Transmission** scenario takes place if it is only the recipient to be
registered on PEPPOL SMP/SML. In such a case, NSO receives the order directly
from the Public Administration with an NSO address through traditional channels
(PEC, FTP and WS). The order is then forwarwed to the to the recipient on the
PEPPOL network.

This scenario is supported thanks to the availability of the national PEPPOL
Access Point for the PA made available by the national PEPPOL Authority and
integrated with NSO.

<figure class="figure">
  <img src="/assets/images/e-ordering-2-en.png" class="figure-img img-fluid rounded" alt="Transmission scenario with third party">
  <figcaption class="figure-caption text-center">Transmission scenario with third party</figcaption>
</figure>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">STEP</th>
      <th scope="col">DESCRIPTION</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">0</th>
      <td>The Supplier (Corner 4) has a PEPPOL Participant ID registered on SMP/SML</td>
    </tr>
    <tr>
      <th scope="row">1</th>
      <td>The PA sends the PEPPOL BIS 3 Order to NSO (Corner 1) specifying the receiver (PEPPOL Participant ID of the Supplier - Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Provided internal checks are successful, NSO (Corner 1) sends the order to the national PEPPOL Access Point for the PA (Corner 2)</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>The national PEPPOL Access Point for the PA (Corner 2) uses PEPPOL’s dynamic discovery (lookup on SML and SMP) to identify the Access Point Provider of the Supplier (Corner 3) to which it must deliver the document</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>The national PEPPOL Access Point for the PA (Corner 2) forwards the order to the Supplier’s Access Point Provider (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>The Supplier's Access Point Provider (Corner 3) acknowledges receipt of the order at the national PEPPOL Access Point for the PA (Corner 2) with a “Message Disposition Notification” transmitted over the PEPPOL network; at the same time, it makes the order available to the Supplier (Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>The national Point Provider for the PA (Corner 2) delivers the notification received for the outcome of the transmission over the PEPPOL network to NSO (Corner 1)</td>
    </tr>
    <tr>
      <th scope="row">7</th>
      <td>NSO (Corner 1) delivers the notification to the Public Administration using the traditional channels provided by NSO itself</td>
    </tr>
  </tbody>
</table>
