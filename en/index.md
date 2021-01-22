---
layout: default
title: Home
hero_title: "Italy for digital business"
hero_description: "PEPPOL allows companies and public administrations to send and receive business documents in standard format over an open, global, and secure network."
lang: en
ref: homepage
---
{% capture hero_title %}
What is PEPPOL?
{% endcapture %}

{% capture hero_text %}
PEPPOL allows fast, efficient, and borderless commercial exchanges.

PEPPOL document specifications encompass global business processes by
standardizing the way information is structured and exchanged.

In addition to the standard formats and to a secure network, PEPPOL provides
the governance to make it work, through binding agreements that guarantee the
compliance of the parties involved.
{% endcapture %}

{% include hero.html text=hero_text title=hero_title %}

<main class="container my-5" markdown="1">

{% include news.html %}

</main>
