---
layout: page
title: About PEPPOL
description: 
lang: en
ref: cos-e-peppol
order: 1
child_of_ref: chi-siamo
---

AGID coordinates the activities aimed at the adoption of e-Procurement in the public sector 
and defines the technical rules for the interoperability of the systems involved.

With the Circular letter n. 3 of 6 December 2016, which defines the additional technical 
rules to guarantee the communication and sharing of data between the electronic purchasing 
and trading systems, AGID has introduced PEPPOL as a reference architecture to guarantee 
interoperability in public e-Procurement.


## How does PEPPOL work?

The [Pan-European Public Procurement On-Line (PEPPOL)](https://peppol.eu/) is
based on a 4 corner architecture that interconnects the subjects that exchange
documents in one of the phases of e-Procurement. The 4 corners specifically
represent:

- Corner 1: the sender of the document
- Corner 2: the PEPPOL Access Point (AP) to which the sender is connected
- Corner 3: the PEPPOL AP to which the recipient is connected
- Corner 4: the recipient of the document

The interactions between the 4 corners are depicted in the image below, where
the Service Metadata Publisher (SMP) is the node that allows to identify the
Access Point on which the recipient is registered and to verify his real
willingness to receive a particular type of document (for example, Order or
Invoice in the PEPPOL format).

![How does PEPPOL work]({{ site.baseurl }}/assets/images/come-funziona-peppol.png)
