---
layout: default
title: Home
hero_title: "Italy for digital business"
hero_description: "PEPPOL allows companies and public administrations to send and receive business documents in standard format over an open, global, and secure network."
lang: en
ref: homepage
---
{% capture hero_title_first_card %}
What is PEPPOL?
{% endcapture %}

{% capture hero_text_first_card %}
PEPPOL allows fast, efficient, and borderless commercial exchanges.

PEPPOL document specifications encompass global business processes by
standardizing the way information is structured and exchanged.

In addition to the standard formats and to a secure network, PEPPOL provides
the governance to make it work, through binding agreements that guarantee the
compliance of the parties involved.
{% endcapture %}

{% assign about_peppol = site.pages | where: "ref", "cos-e-peppol" | where: "lang", page.lang | first %}

{% capture hero_title_second_card %}
What is PEPPOL?
{% endcapture %}

{% capture hero_text_second_card %}
PEPPOL allows fast, efficient, and borderless commercial exchanges.

PEPPOL document specifications encompass global business processes by
standardizing the way information is structured and exchanged.

In addition to the standard formats and to a secure network, PEPPOL provides
the governance to make it work, through binding agreements that guarantee the
compliance of the parties involved.
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
