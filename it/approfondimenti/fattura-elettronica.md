---
layout: page
title: Fattura elettronica
description:
lang: it
ref: e-invoicing
order: 1
child_of_ref: approfondimenti
---

La **DIRETTIVA 2014/55/UE DEL PARLAMENTO EUROPEO E DEL CONSIGLIO del 16 aprile
2014 relativa alla fatturazione elettronica negli appalti pubblici**, al fine di
rimuovere ostacoli derivanti dalla coesistenza di differenti requisiti legali e
dalla mancanza di interoperabilità negli scambi transfrontalieri e
trans-settoriali garantendo l'interoperabilità semantica e migliorando la
certezza del diritto, ha previsto l’adozione di uno standard europeo per la
fatturazione elettronica negli appalti pubblici verso le Pubbliche
Amministrazioni.

La Direttiva dava mandato al **CEN** (Comitato Europeo di normazione) di
sviluppare uno standard europeo (la cosiddetta “norma”) per il modello semantico
della fattura e di definire un elenco di sintassi compatibili con tale semantica
e le corrispondenti mappature. Nell’ottobre 2017 la **norma europea (EN
16931**-1:2017**) e le relative sintassi** sono state formalmente referenziate
dalla Commissione Europea. Tali sintassi sono:

-   i messaggi di fattura e nota di credito UBL definiti nella norma ISO/IEC
    19845:2015.7;

-   il messaggio Cross Industry Invoice XML dell'UN/CEFACT come specificato
    negli schemi XML 16B (SCRDM-CII).

La Direttiva 55/2014 è stata recepita **in Italia con il decreto legislativo
n.148 del 27 dicembre 2018, entrato in vigore il 1° febbraio 2019** e che si
applica alle amministrazioni aggiudicatrici e agli enti aggiudicatori di cui
all'articolo 1, comma 1, del decreto legislativo 18 aprile 2016, n. 50, nonché
alle amministrazioni di cui all'articolo 1, comma 2, della legge 31 dicembre
2009, n. 196. Successivamente, con il Provvedimento n. 99370 del 18 aprile 2019
dell’Agenzia delle Entrate, sono state approvate le modalità applicative per la
fatturazione elettronica europea negli appalti pubblici e sono state definite le
regole tecniche, cosiddette Core Invoice Usage Specification (CIUS), per
l’utilizzo delle sintassi nel contesto italiano.

Il recepimento ha quindi reso obbligatorie la **ricezione, la traduzione e la
consegna** delle fatture elettroniche redatte secondo lo **standard europeo**
(EN16931), tramite il **Sistema di Interscambio** (SdI) nazionale secondo due
fasi:

-   dal 18 aprile 2019 per le autorità governative centrali;

-   dal 18 aprile 2020 per le altre amministrazioni aggiudicatrici regionali e
    locali.

**L’INFRASTRUTTURA DI RETE PEPPOL**

L’aggiornamento dell'infrastruttura nazionale di fatturazione elettronica per
garantire la piena adozione degli standard di fatturazione elettronica europea,
di messaggistica e di eDelivery (Peppol), è stato realizzato grazie ai progetti
**EeISI-** [European eInvoicing Standard in
Italy](https://www.agid.gov.it/it/piattaforme/fatturazione-elettronica/progetto-cef-eeisi)
e **eIGOR** - [elnvoicing GO
Regional](https://www.agid.gov.it/it/piattaforme/fatturazione-elettronica/progetto-cef-eigor),
co-finanziati dalla Commissione Europea attraverso il programma **CEF**
-[Connecting European
Facility.](https://ec.europa.eu/inea/connecting-europe-facility/cef-telecom)

In virtù dell’integrazione tra l’SMP di Peppol e l’IPA realizzata nell’ambito
del progetto EeISI, tutte le Pubbliche Amministrazioni possono scegliere su
quest’ultima il proprio Access Point che funga da intermediario delle fatture
ricevute su rete Peppol.

Per la trasmissione delle fatture europee tramite la rete Peppol è necessario
che:

1.  la PA si avvalga di un service provider che sia contemporaneamente
    **Certified Peppol Access Point** ed **intermediario qualificato** verso il
    **Sistema di Interscambio** dell’Agenzia delle Entrate;

2.  la PA configuri il canale di ricezione Peppol per gli uffici di fatturazione
    elettronica sull’**Indice delle Pubbliche Amministrazioni** (iPA), in virtù
    della realizzazione dell’integrazione tra l’SMP ed iPA stesso.

Di seguito sono riportati due schemi esemplificativi che illustrano
rispettivamente il flusso di trasmissione di una fattura ed il flusso di ritorno
delle notifiche:

<figure class="figure">
  <img src="/assets/images/e-invoicing-1.png" class="figure-img img-fluid rounded" alt="Schema trasmissione fattura">
  <figcaption class="figure-caption text-center">Schema trasmissione fattura</figcaption>
</figure>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">STEP</th>
      <th scope="col">DESCRIZIONE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Il Fornitore (Corner 1) invia il documento Peppol BIS 3 (conforme alla CIUS) al proprio Access Point Provider (Corner 2) specificando il destinatario (endpoint del’UFE della PA registrata su iPA)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>L'Access Point Provider (Corner 2) utilizza la dynamic discovery (lookup su SML e SMP) di Peppol per individuare l’Access Point (Corner 3) a cui dovrà consegnare il documento destinato alla PA</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>L'Access Point Provider del Fornitore (Corner 2) invia il documento all'Access Point Provider della Pubblica Amministrazione (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>L'Access Point della Pubblica Amministrazione (Corner 3) invia il documento a SdI utilizzando i canali tradizionali previsti dal Sistema di Interscambio</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>SdI verifica la conformità del documento rispetto alle regole italiane, lo traduce nel formato nazionale FatturaPA e lo consegna alla PA allegando il file originario Peppol BIS 3, utilizzando i canali di ricezione censiti sul Sistema di Interscambio</td>
    </tr>
  </tbody>
</table>

<figure class="figure">
  <img src="/assets/images/e-invoicing-2.png" class="figure-img img-fluid rounded" alt="Schema trasmissione notifiche">
  <figcaption class="figure-caption text-center">Schema trasmissione notifiche</figcaption>
</figure>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">STEP</th>
      <th scope="col">DESCRIZIONE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>La Pubblica Amministrazione (Corner 4) invia a SdI la notifica di avvenuta ricezione in formato FatturaPA secondo i canali tradizionali di SdI</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>SdI riceve la notifica e la trasmette, in formato FatturaPA, all’Access Point Provider della PA (Corner 3) secondo i canali tradizionali</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>L'Access Point Provider della Pubblica Amministrazione (Corner 3) traduce la notifica dal formato FatturaPA al formato UBL creando l’Invoice Response</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>L'Access Point Provider della Pubblica Amministrazione (Corner 3) utilizza la dynamic discovery (lookup su SML e SMP) di Peppol per individuare l’Access Point (Corner 2) a cui dovrà recapitare l’Invoice Response</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>L’Access Point Provider (Corner 3) invia all’Access Point Provider del fornitore (Corner 2) la notifica IR su rete Peppol</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>L'Access Point Provider del Fornitore (Corner 2) comunica al mittente originale della fattura (Corner 1) l’esito dell’invio utilizzando una tipologia di notifica concordata tra le parti</td>
    </tr>
  </tbody>
</table>
