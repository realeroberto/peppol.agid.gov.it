---
layout: page
title: Electronic Invoicing
description:
lang: en
ref: e-invoicing
order: 1
child_of_ref: insights
---

**DIRECTIVE 2014/55/EU OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL of 16
April 2014 on electronic invoicing in public procurement** provided for the
adoption of a **European Standard**, in order to reduce obstacles deriving from
the coexistence of different legal requirements and from the lack of
interoperability in cross-border and trans-sectoral exchanges, as well as in
order to ensure semantic interoperability and to improve legal certainty.

The Directive mandated the **CEN** (European Committee for Standardization) to
develop a European standard (the so-called “Norm”) for the **semantic model**
of an electronic invoice and to define a list of syntaxes compliant with the
semantic model and the corresponding mappings. In October 2017, the **European
standard (EN 16931-1:2017) and related syntaxes** were formally referenced by
the European Commission. These syntaxes are:

-   the UBL invoice and credit note messages defined by the ISO/IEC 19845:2015.7
    standard;

-   the UN/CEFACT XML Cross Industry Invoice message as defined by the XML 16B
    (SCRDM-CII) schemata.

Directive 2014/55 was implemented in Italy by the **Legislative Decree no. 148
of 27 December 2018, entered into force on 1 February 2019**, which applies to
contracting authorities and contracting entities referred to in article 1,
paragraph 1, of the legislative decree 18 April 2016, no. 50, as well as to the
public administrations referred to in article 1, paragraph 2, of the law of 31
December 2009, no. 196. Subsequently, with Provision no. 99370 of 18 April 2019
by the Revenue Agency (Agenzia delle Entrate), both the implementation rules
for European electronic invoicing in public procurement and the technical
specification (the so-called Core Invoice Usage Specification, or CIUS) for the
use of the syntax in the Italian context were approved.

The Italian transposition therefore made the **receipt, translation and
delivery** of electronic invoices compliant with the European standard
(EN16931) **mandatory**, through the national Electronic Exchange System (SdI),
in two phases:

-   from April 18, 2019 for central government authorities;

-   from 18 April 2020 for other regional and local contracting authorities.

**THE PEPPOL NETWORK INFRASTRUCTURE**

The update of the national electronic invoicing infrastructure to ensure the
full adoption of the European electronic invoicing, messaging and eDelivery
(PEPPOL) profiles was carried out thanks to the **EeISI** ([“European
eInvoicing Standard in
Italy”](https://www.agid.gov.it/en/platforms/electronic-invoicing/cef-eeisi-project))
and **eIGOR** ([“elnvoicing GO
Regional”](https://www.agid.gov.it/en/platforms/electronic-invoicing/cef-eigor-project))
projects, co-financed by the European Commission through the [CEF Connecting
Europe Facility](https://ec.europa.eu/inea/en/connecting-europe-facility)
funding instrument.

Moreover, thanks to the integration between the PEPPOL SMP and iPA ([“Indice
delle pubbliche amministrazioni”](https://indicepa.gov.it/), the national
register of public bodies in Italy) carried out as part of the EeISI project,
all Public Administrations can select their own Access Point on iPA itself:
such AP will then act as an intermediary for the invoices received over the
PEPPOL network.

In order to get started transmitting invoices compliant with the European
format European via the PEPPOL network, it is necessary that:

1.  the Public Administration adopts a service provider which is both a
    **Certified PEPPOL Access Point** and a **qualified intermediary** towards the
    Revenue Agency’s SdI;

2.  the PA sets up the PEPPOL reception channel for the electronic billing
    offices on the **iPA register**, thanks to the aforementioned integration
    between the SMP and iPA itself.


The following two illustrative diagrams explain respectively the invoice
transmission flow and the return flow of notifications:

<figure class="figure">
  <img src="/assets/images/e-invoicing-1-en.png" class="figure-img img-fluid rounded" alt="Invoicing transmission flow">
  <figcaption class="figure-caption text-center">Invoicing transmission flow</figcaption>
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
      <th scope="row">1</th>
      <td>The Economic Operator (Corner 1) sends the Peppol BIS 3 document (CIUS-compliant) towards its own Access Point Provider (Corner 2) specifying the receiver (the Public Administration’s UFE endpoint from iPA)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>The Access Point Provider (Corner 2) uses PEPPOL’s dynamic discovery (lookup on SML and SMP) to identify the Access Point (Corner 3) to which it must deliver the document addressed to the PA</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>The Access Point Provider of the Economic Operator (Corner 2) sends the document to the Access Point Provider of the Public Administration (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>The Access Point of the Public Administration (Corner 3) sends the document to Electronic Exchange System (SdI) using the traditional channels provided by SdI itself</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>SdI verifies the compliance of the document with the Italian rules, translates it into the FatturaPA national format and delivers it to the PA by attaching the original Peppol BIS 3 file, using the reception channels registered on SdI itself</td>
    </tr>
  </tbody>
</table>

<figure class="figure">
  <img src="/assets/images/e-invoicing-2-en.png" class="figure-img img-fluid rounded" alt="Notification transmission flow">
  <figcaption class="figure-caption text-center">Notification transmission flow</figcaption>
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
      <th scope="row">1</th>
      <td>The Public Administration (Corner 4) sends to SdI the notification of receipt in FatturaPA format using the traditional SdI channels</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>SdI receives the notification and transmits it, in FatturaPA format, to the PA’s Access Point Provider (Corner 3) using SdI traditional channel</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>The Access Point Provider of the Public Administration (Corner 3) translates the notification from the FatturaPA format to the UBL format creating the Invoice Response</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>The Access Point Provider of the Public Administration (Corner 3) uses PEPPOL’s dynamic discovery (lookup on SML and SMP) to identify the Access Point (Corner 2) to which the Invoice Response must be delivered</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>The Access Point Provider (Corner 3) sends the IR notice on the PEPPOL network to the Access Point Provider of the Economic Operator (Corner 2)</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>The Access Point Provider of the Economic Operator (Corner 2) informs the original sender of the invoice (Corner 1) of the transmission outcome using a type of notification agreed between the parties</td>
    </tr>
  </tbody>
</table>
