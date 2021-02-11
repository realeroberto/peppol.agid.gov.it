---
layout: default
title: Home
hero_title: "L’Italia per il business digitale"
hero_description: "PEPPOL consente alle imprese e alle pubbliche amministrazioni di inviare e ricevere documenti di business in formato standard su una rete aperta, globale e sicura."
lang: it
ref: homepage
---
{% capture hero_title_first_card %}
Cos'è PEPPOL?
{% endcapture %}

{% capture hero_text_first_card %}
PEPPOL abilita il commercio veloce, efficiente e senza confini.

Le specifiche dei documenti PEPPOL integrano i processi aziendali globali
standardizzando il modo in cui le informazioni sono strutturate e scambiate.

PEPPOL oltre ai tracciati standard e ad una rete sicura fornisce la governance
per farla funzionare, attraverso accordi vincolanti che garantiscono la
conformità delle parti coinvolte.
{% endcapture %}

{% assign about_peppol = site.pages | where: "ref", "cos-e-peppol" | where: "lang", page.lang | first %}

{% capture hero_title_second_card %}
Cos'è PEPPOL?
{% endcapture %}

{% capture hero_text_second_card %}
PEPPOL abilita il commercio veloce, efficiente e senza confini.

Le specifiche dei documenti PEPPOL integrano i processi aziendali globali
standardizzando il modo in cui le informazioni sono strutturate e scambiate.

PEPPOL oltre ai tracciati standard e ad una rete sicura fornisce la governance
per farla funzionare, attraverso accordi vincolanti che garantiscono la
conformità delle parti coinvolte.
{% endcapture %}

{% assign about_peppol = site.pages | where: "ref", "cos-e-peppol" | where: "lang", page.lang | first %}

{% include hero.html
    title_first_card=hero_title_first_card
    text_first_card=hero_text_first_card
    read_more_page_first_card=about_peppol
    title_second_card=hero_title_second_card
    text_second_card=hero_text_second_card
    read_more_page_second_card=about_peppol
%}

<main class="container my-5" markdown="1">

{% include news.html %}

</main>
