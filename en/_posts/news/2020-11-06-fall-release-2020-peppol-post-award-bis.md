---
layout: post
title: Fall Release 2020 PEPPOL Post-Award BIS
lang: en
ref: fall-release-2020-peppol-post-award-bis
excerpt_separator: <!--more-->
tags:
categories: news
permalink: /en/news/fall-release-2020-peppol-post-award-bis/
---

The OpenPEPPOL consortium has published the Post Award BIS Fall Release of the technical documentation covering all PEPPOL profiles.

This release has been acknowledged by AGID as PEPPOL Authority with reference to the technical specifications used in the Italian domain and, **starting from today November 6, 2020**, they are available for consultation at: <https://peppol-docs.agid.gov.it/>

**The adaptation** to the new specifications **is mandatory starting from November 16, 2020**.

The changes summarized below are also reported in the "Release Notes" section at [this link](https://peppol-docs.agid.gov.it/):

-   **Changes to the specification (Documentation)**

-   For Order only, fixed a typo in the documentation about the use of the charge indicator "false vs true" in the table in paragraph "6.9. Calculation of totals (AnticipatedMonetaryTotals)", where the reference to the indicator was inverted.

-   **Syntax changes**

-   For Order only, added a new optional Business Term *at header level*: "Shipping label" (tir01-p036);
-   For Order only, added a new optional Business Term *at line level*: "Delivery location ID" (tir01-p037).

-   **Changes to code lists and validation tools (for Simple Ordering, Complete Ordering and Transport Document)**

-   PEPPOL-COMMON-R040 rule: "GLN must have a valid format according to GS1 rules". Severity changed from "warning" to "fatal". (the rule was introduced in the fall release of 2019 with severity "warning" to avoid interruptions but with the intention of changing it to "fatal" after 6-12 months);
-   EAS coding: code 0209 added, code 9958 removed. PEPPOL rule updated accordingly;
-   ICD coding: added codes 0205, 0206, 0206, 0207, 0208, 0209;
-   Currency code encoding (ISO 4217): eliminated duplicate codes.

**Beware:** the changes affect the controls and logic implemented by the validation tool, which can be downloaded at [this link](https://peppol-docs.agid.gov.it/), therefore it is recommended to download the version updated.
