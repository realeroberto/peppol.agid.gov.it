---
layout: post
title: Spring Release 2021
lang: it
ref: spring-release-2021
excerpt_separator: <!--more-->
tags:
categories: news
permalink: /it/news/spring-release-2021/
---

Il giorno 3 Maggio 2021 OpenPeppol pubblicherà formalmente gli aggiornamenti
relativi alla Spring Release 2021, contenenti una serie di modifiche le cui
release notes complete sono disponibili agli indirizzi di test:<!--more-->

*   <https://test-docs.peppol.eu/2021-Spring-ReleaseCandidate/poacc/upgrade-3/release-notes/> per
    quel che riguarda vari profili tra cui quelli degli ordini, attualmente in
    uso dal Nodo Smistamento Ordini (NSO)
*   <https://test-docs.peppol.eu/2021-Spring-ReleaseCandidate/poacc/upgrade-3/>
    per accedere direttamente alle nuove specifiche attualmente in revisione
    pubblica interna alla Post Award Coordinating Community

Tali aggiornamenti saranno pubblicati (Publication date) ed avranno efficacia
in via obbligatoria (Mandatory date) in conformità con le seguenti date (cfr
<https://peppol.eu/downloads/post-award/>):

| Review date | Publication date | Mandatory date |
|-------------|------------------|----------------|
| 11.04.2021  | 03.05.2021       | 17.05.2021     |

Il MEF-RGS e la Peppol Authority italiana AgID stanno collaborando al
recepimento delle modifiche e, pertanto, si comunica che sarà pubblicata una
nuova versione delle Regole tecniche NSO e delle specifiche Peppol italiane il
prossimo 4/05 con entrata in vigore dal 17/05/201.

Di seguito si riepilogano i principali cambiamenti che sono previsti per
**Ordinazione Semplice** e **Documento di Trasporto**:

### ORDINAZIONE SEMPLICE

* *Cambiamenti alla specifica (Documentazione)*
    - Corretto refuso nel paragrafo sul calcolo dei totali. Tutti i campi
      citati sono all'interno del cac:AnticipatedMonetaryTotal invece di
      cac:LegalMonetaryTotal
* *Cambiamenti alla sintassi*
    - Aggiunto il campo cac:Shipment/cbc:ID, campo obbligatorio in UBL, da
      valorizzare con valore fisso NA
    - Invertito l'ordine di cac:Contat e cac:PostalAddress nel
      cac:DeliveryParty (ora viene prima cac:PostalAddress, con tutti i campi
      al suo interno)
* *Cambiamenti alle code lists e ai tool di validazione*
    - Codifica ICD: aggiunti i codici 0210 (Codice Fiscale), 0211 (Partita
      IVA), 0212, 0213
    - Codifica EAS: aggiunti i codici 0210 (Codice Fiscale), 0211 (Partita
      IVA), 0212, 0213. Rimosso 9956

### DOCUMENTO DI TRASPORTO

* *Cambiamenti alla specifica (Documentazione)*
    - Modificate le regole PEPPOL-T16-R009 e PEPPOL-T16-R010, prima riferite al
      "Buyer Party" ed ora rispettivamente a "Seller party" e "Originator
      customer party"
* *Cambiamenti alla sintassi*
    - Aggiunta descrizione e tir id al campo cac:DespatchAddress/cbc:ID
* *Cambiamenti alle code lists e ai tool di validazione*
    - Codifica ICD: aggiunti i codici 0210 (Codice Fiscale), 0211 (Partita
      IVA), 0212, 0213
    - Codifica EAS: aggiunti i codici 0210 (Codice Fiscale), 0211 (Partita
      IVA), 0212, 0213. Rimosso 9956

È importante porre particolare attenzione alla modifica relativa all'aggiunta
dei nuovi codici 0210 (Codice Fiscale) e 0211 (Partita IVA) che sostituiscono i
precedenti codici temporanei italiani 9907 (CF) e 9906 (Partita IVA) sia a
livello di lista EAS (indirizzi elettronici registrati) sia a livello di lista
ISO 6523 (identificativi delle parti).

L'introduzione dei nuovi schemeID avverrà secondo un periodo di transizione che
seguirà le seguenti date:

* **a partire dal 3 Maggio 2021**, sarà opzionale supportare i nuovi codici
  0210 e 0211 e sarà quindi possibile registrare nuovi participantID Peppol
  (endpointID) sulla rete Peppol. Resterà tuttavia possibile continuare a
  registrare participantID con i vecchi codici 9906 e 9907.
* **a partire dal 17 Maggio 2021**, data di entrata in vigore della Spring
  Release 2021, sarà obbligatorio supportare 0210 e 0211 e pertanto i codici
  temporanei 9906 e 9907 saranno deprecati, pertanto, ogni nuova registrazione
  dovrà avvenire utilizzando i codici 0210 e 0211. I participant identifier
  precedentemente registri con i codici 9906 e 9907 resteranno validi e la
  trasmissione dei documenti avverrà comunque per consentire ai Provider ed ai
  relativi clienti di aggiornare tutti i soggetti coinvolti e le relative
  anagrafiche.
* **a partire dal 15/11/2021** con l'entrata in vigore della Fall Release 2021
  saranno rimossi definitivamente i codici 9906 e 9907 e, pertanto, per quella
  data è necessario che tutti i participant identifier registrati utilizzando i
  vecchi schemeID siano rimossi dall'SML ed registrati con i nuovi codici 0210
  e 0211.

Si precisa che in concomitanza con la Spring Release sarà rilasciata una nuova
versione delle codelist dell'eDelivery Peppol
([qui](https://docs.peppol.eu/edelivery/codelists/)), che includerà i nuovi
SchemeID.

Si avvisa infine che le modifiche descritte impattano sui controlli e sulle
logiche implementate dal tool di validazione, sarà pertanto opportuno scaricare
la versione aggiornata, disponibile
[qui](https://peppol-docs.agid.gov.it/docs/my_index.jsp) a partire dal 4 maggio
2021.
