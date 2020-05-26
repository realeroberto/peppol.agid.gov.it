---
layout: page
title: Ordine elettronico
description:
lang: it
ref: e-ordering
order: 2
child_of_ref: approfondimenti
---

**La legge di Bilancio 2018** (Legge n. 205 del 27 dicembre 2017) **commi
411-414** prevede che tutti gli **ordini di acquisto** della pubblica
amministrazione debbano essere effettuati **esclusivamente in formato
elettronico** e trasmessi tramite **NSO** – [Nodo Smistamento Ordini della
Pubblica
Amministrazione](http://www.rgs.mef.gov.it/VERSIONE-I/e_government/amministrazioni_pubbliche/acquisti_pubblici_in_rete_apir/nodo_di_smistamento_degli_ordini_di_acquisto_delle_amministrazioni_pubbliche_nso/),
gestito dal Ministero dell’Economia e delle Finanze (MEF).

Il **decreto MEF** del **7 dicembre 2018** ha stabilito le modalità, i tempi di
attuazione e l’obbligatorietà, in un primo momento, per le aziende sanitarie del
Servizio Sanitario Nazionale (SSN) a partire dal 1° ottobre 2019. Il **decreto
MEF** del **27 dicembre 2019** ha **modificato la decorrenza** dell’obbligo a
partire dal:

-   1° febbraio 2020 per gli ordini relativi ai beni;

-   1° febbraio 2021 per gli ordini relativi ai servizi.

**Il sistema NSO**, rappresenta l’**infrastruttura centrale** per lo scambio di
ordini elettronici tra enti pubblici e fornitori, il quale prevede, oltre ai
canali tradizionali (PEC, FTP, WS) anche la trasmissione dei documenti su
**rete Peppol**. A tal fine NSO adotta, nativamente, le [specifiche
tecniche](https://peppol-docs.agid.gov.it/) **Peppol BIS 3 (UBL)** per
l’ordine, l’ordine semplice e l’ordine pre-concordato.

I fornitori già registrati su rete Peppol possono interagire con NSO senza
ulteriori sviluppi, semplicemente in virtù dello scenario di *Validazione* o di
*Trasmissione* con terza parte in uscita.

**SCENARIO DI VALIDAZIONE**

Lo scenario di **Validazione** si attua se mittente e destinatario sono entrambi
registrati su **SMP**/**SML** Peppol, in questo caso NSO valida l’ordine ma la
trasmissione avviene su rete Peppol.

Tale scenario presuppone che la PA si avvalga di un service provider che sia
contemporaneamente **Certified Peppol Access Point** ed **intermediario
qualificato** verso **NSO**.

<figure class="figure">
  <img src="/assets/images/e-ordering-1-it.png" class="figure-img img-fluid rounded" alt="Scenario di validazione">
  <figcaption class="figure-caption text-center">Scenario di validazione</figcaption>
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
      <th scope="row">0</th>
      <td>Il Fornitore (Corner 4) ha un Participant ID Peppol registrato su SMP-SML</td>
    </tr>
    <tr>
      <th scope="row">1</th>
      <td>La PA (Corner 1) invia l’ordine Peppol BIS 3 al proprio Access Point Provider (Corner 2) specificando il destinatario (Participant ID Peppol)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>L’Access Point Provider (Corner 2) invia l’ordine a NSO utilizzando i canali tradizionali previsti da NSO al fine di ottenere una notifica di validazione</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>L'Access Point Provider (Corner 2) utilizza la dynamic discovery (lookup su SML e SMP) di Peppol per individuare l’Access Point (Corner 3) a cui dovrà inviare l’ordine</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>L’Access Point Provider della PA (Corner 2) inoltra l’ordine all'Access Point Provider del Fornitore (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>L’Access Point Provider del Fornitore (Corner 3) conferma la ricezione dell’ordine al Corner 2 con una “Message Disposition Notification” trasmessa su rete Peppol; simultaneamente mette a disposizione l’ordine al Fornitore (Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>L'Access Point Provider (Corner 2) notifica ricevuta sull’esito della trasmissione al mittente originale dell’ordine (Corner 1), utilizzando una tipologia di notifica concordata tra le parti</td>
    </tr>
  </tbody>
</table>

**SCENARIO DI TRASMISSIONE CON TERZA PARTE IN USCITA**

Lo scenario di **Trasmissione** si attua se il solo destinatario è registrato su
**SMP**/**SML** Peppol, in questo caso NSO riceve l’ordine tramite i canali
tradizionali (PEC, FTP e WS) e lo trasmette al destinatario su rete Peppol.

Tale scenario è supportato dalla disponibilità **dell’Access Point Peppol unico
per la PA** realizzato da **AgID** ed integrato con NSO.

<figure class="figure">
  <img src="/assets/images/e-ordering-2-it.png" class="figure-img img-fluid rounded" alt="Scenario di trasmissione con terza parte in uscita">
  <figcaption class="figure-caption text-center">Scenario di trasmissione con terza parte in uscita</figcaption>
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
      <th scope="row">0</th>
      <td>Il Fornitore (Corner 4) ha un Participant ID Peppol registrato su SMP-SML</td>
    </tr>
    <tr>
      <th scope="row">1</th>
      <td>La PA invia l’ordine Peppol BIS 3 ad NSO (Corner 1) specificando il destinatario (Participant ID Peppol)</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>NSO, effettuati i controlli, invia l’ordine all’Access Point Peppol unico per la PA (Corner 2)</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>L’Access Point Peppol unico per la PA (Corner 2) utilizza la dynamic discovery (lookup su SML e SMP) di Peppol per individuare l’Access Point (Corner 3) a cui dovrà consegnare il documento</td>
    </tr>
    <tr>
      <th scope="row">4</th>
      <td>L’Access Point Peppol unico per la PA (Corner 2) inoltra l’ordine all'Access Point Provider del Fornitore (Corner 3)</td>
    </tr>
    <tr>
      <th scope="row">5</th>
      <td>L’Access Point Provider del Fornitore (Corner 3) conferma la ricezione dell’ordine al Corner 2 con una “Message Disposition Notification” trasmessa su rete Peppol; simultaneamente mette a disposizione l’ordine al Fornitore (Corner 4)</td>
    </tr>
    <tr>
      <th scope="row">6</th>
      <td>L'Access Point Provider (Corner 2) consegna la notifica ricevuta sull’esito della trasmissione su rete Peppol a NSO (Corner 1)</td>
    </tr>
    <tr>
      <th scope="row">7</th>
      <td>NSO (Corner 1) recapita la notifica alla Pubblica Amministrazione utilizzando i canali tradizionali previsti da NSO</td>
    </tr>
  </tbody>
</table>
