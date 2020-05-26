---
layout: page
title: Cos'è PEPPOL
description: 
lang: it
ref: cos-e-peppol
order: 3
---

Il [Pan-European Public Procurement On-Line (PEPPOL)](https://peppol.eu/) nasce
come iniziativa progettuale sul tema degli acquisti digitali promossa dalla
Commissione Europea nel periodo compreso tra il 2008 e il 2012. Alla
conclusione del progetto l’associazione OpenPEPPOL ha assunto il governo delle
componenti fondamentali del sistema.

PEPPOL è un insieme di elementi infrastrutturali e di specifiche tecniche 
promosse dalla Commissione Europea nell’ambito delle iniziative CEF e che 
rendono possibile l’interoperabilità tra i vari sistemi di e-procurement, 
a livello transfrontaliero.
Le componenti fondamentali del sistema sono: l’infrastruttura di rete 
PEPPOL eDelivery Network, le specifiche per l’interoperabilità dei 
documenti di Business PEPPOL Business Interoperability Specifications (BIS), 
gli accordi che regolano l’utilizzo della rete PEPPOL Transport Infrastructure 
Agreements (TIA).

AGID coordina le attività finalizzate all’adozione dell’e-Procurement nel
settore pubblico e definisce le regole tecniche per l’interoperabilità dei
sistemi coinvolti.

Con la Circolare n. 3 del 6 dicembre 2016 che definisce le Regole tecniche
aggiuntive per garantire il colloquio e la condivisione dei dati tra i sistemi
telematici di acquisto e di negoziazione, AGID ha introdotto PEPPOL come
architettura di riferimento per garantire l’interoperabilità nell’e-Procurement
pubblico.

## Come funziona PEPPOL?

PEPPOL si basa su un’architettura 4 corner che interconnette i soggetti che si
scambiano documenti in una delle fasi dell’e-Procurement. I 4 corner
rappresentano nello specifico:

- Corner 1: il mittente del documento
- Corner 2: l’Access Point (AP) PEPPOL a cui è connesso il mittente
- Corner 3: l’AP PEPPOL a cui è connesso il destinatario
- Corner 4: il destinatario del documento

Le interazioni tra i 4 corner sono raffigurate nell'immagine in calce, dove il
Service Metadata Publisher (SMP) è il nodo che consente di individuare l'Access
Point su cui è registrato il destinatario e di verificare la sua reale
disponibilità a ricevere una particolare tipologia di documento (ad esempio,
Ordine o Fattura nel formato PEPPOL).

![Come funziona PEPPOL]({{ site.baseurl }}/assets/images/come-funziona-peppol.png)
