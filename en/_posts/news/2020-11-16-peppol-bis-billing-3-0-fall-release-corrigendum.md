---
layout: post
title: PEPPOL BIS Billing 3.0 fall release corrigendum
lang: en
ref: peppol-bis-billing-3-0-fall-release-corrigendum
excerpt_separator: <!--more-->
tags:
categories: news
permalink: /en/news/peppol-bis-billing-3-0-fall-release-corrigendum/
---

On November 12, 2020, the OpenPeppol consortium published a corrigendum to the autumn release (Post Award BIS Fall Release).

The Corrigendum was implemented by AGID as Peppol Authority with reference to the technical specifications used in the Italian domain and is available [here](https://peppol-docs.agid.gov.it/), to supplement what was already published on November 6, 2020.

Please note that adaptation to the new specifications is mandatory starting today November 16, 2020.

The corrigendum is detailed in the "Release Notes" section and in particular is relevant to:

* DDT: 3.1.0.4 (EN) Update to specification [PEPPOL BIS 3.0.6 - hotfix](https://docs.peppol.eu/poacc/upgrade-3/release-notes/).

Syntax changes:

* Fixed cardinality of cac:DespatchLine/cac:OrderLineReference/cac:OrderLine to 0..1 (formerly 1..1), now in line with BIS (Documentation).

Changes to code lists and validation tools:

* Removed the PEPPOL-T16-R002 rule which generated a warning in the absence of the cac:OrderReference/cbc:ID

The changes have an impact on the controls and logic implemented by the validation tool, which can be downloaded at the abovementioned [link](https://peppol-docs.agid.gov.it/), therefore it is recommended to download the updated version.
