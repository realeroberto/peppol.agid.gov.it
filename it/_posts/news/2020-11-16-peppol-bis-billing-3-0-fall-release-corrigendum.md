---
layout: post
title: PEPPOL BIS Billing 3.0 fall release corrigendum
lang: it
ref: peppol-bis-billing-3-0-fall-release-corrigendum
excerpt_separator: <!--more-->
tags:
categories: news
permalink: /it/news/peppol-bis-billing-3-0-fall-release-corrigendum/
---

Il 12 novembre 2020 il consorzio OpenPeppol ha pubblicato un corrigendum alla release autunnale (Post Award BIS Fall Release).

Il Corrigendum è stato recepito dalla Peppol Authority Agid per quanto riguarda le specifiche tecniche utilizzate nel dominio italiano ed è disponibile [qui](https://peppol-docs.agid.gov.it/), ad integrazione di quanto già pubblicato il 6/11/2020.

Si ricorda che l'adeguamento alle nuove specifiche è obbligatorio a partire da oggi 16 novembre 2020.

Il corrigendum è dettagliato nella sezione “Note di rilascio” ed in particolare riguarda:

* DDT: 3.1.0.4(IT) Aggiornamento alle specifiche [PEPPOL BIS 3.0.6 - hotfix](https://docs.peppol.eu/poacc/upgrade-3/release-notes/).

Cambiamenti alla sintassi:

* Corretta la cardinalità del cac:DespatchLine/cac:OrderLineReference/cac:OrderLine a 0..1 (prima 1..1), ora in linea con la BIS (Documentazione).

Cambiamenti alle code lists e ai tool di validazione:

* Rimossa la regola PEPPOL-T16-R002 che generava un warning in assenza del cac:OrderReference/cbc:ID

Le modifiche impattano sui controlli e sulle logiche implementate dal tool di validazione, scaricabile al [link](https://peppol-docs.agid.gov.it/) sopracitato, pertanto si raccomanda di scaricare la versione aggiornata.
