---
layout: post
title: Fall Release 2020 PEPPOL Post-Award BIS
lang: it
ref: fall-release-2020-peppol-post-award-bis
excerpt_separator: <!--more-->
tags:
categories: news
permalink: /it/news/fall-release-2020-peppol-post-award-bis/
---

Il consorzio OpenPEPPOL ha pubblicato la release autunnale (Post Award BIS Fall Release) della documentazione tecnica riguardante tutti i profili PEPPOL.

Tale release è stata recepita dalla PEPPOL Authority Agid per quanto riguarda le specifiche tecniche utilizzate nel dominio italiano e, **a partire da oggi 6 Novembre 2020,** sono disponibili in consultazione all'indirizzo: <https://peppol-docs.agid.gov.it/> 

**L'adeguamento** alle nuove specifiche **è obbligatorio a partire dal** **16 Novembre 2020**.

Le modifiche riepilogate di seguito sono riportate anche nella sezione "Note di rilascio" a [questo link](https://peppol-docs.agid.gov.it/):

-   **Cambiamenti alla specifica (Documentazione)**

-   Per l'Ordinazione semplice, corretto il refuso presente nella documentazione circa l'uso del charge indicator "false vs true" nella tabella del paragrafo "6.9. Calcolo dei totali (AnticipatedMonetaryTotals)", dove il riferimento all'indicatore era invertito.

-   **Cambiamenti alla sintassi**

-   Per l'Ordinazione semplice, aggiunto un nuovo Business Term opzionale *a livello di testata*: "Shipping label" (tir01-p036);
-   Per l'Ordinazione semplice, aggiunto un nuovo Business Term opzionale *a livello di riga*: "Delivery location ID" (tir01-p037).

-   **Cambiamenti alle code lists e ai tool di validazione (per Ordinazione semplice, Ordinazione Completa e Documento di Trasporto)**

-   Regola PEPPOL-COMMON-R040: "GLN deve avere un formato valido secondo le regole GS1". Modificata la gravità da "warning" a "fatal". (la regola è stata introdotta nella fall release del 2019 con gravità "warning" per evitare interruzioni ma con l'intenzione di modificarla a "fatal" dopo 6-12 mesi);
-   Codifica EAS: aggiunto codice 0209, rimosso codice 9958. Regola PEPPOL aggiornata conseguentemente;
-   Codifica ICD: aggiunti i codici 0205, 0206, 0206, 0207, 0208, 0209;
-   Codifica Currency code (ISO 4217): eliminati i codici duplicati.

**Attenzione:** le modifiche impattano sui controlli e sulle logiche implementate dal tool di validazione, scaricabile a [questo link](https://peppol-docs.agid.gov.it/), pertanto si raccomanda di scaricare la versione aggiornata.
