---
title: "VisionAI - Publications"
layout: gridlay
excerpt: "VisionAI -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Group highlights

**At the end of this page, you can find the [full list of publications and patents](#full-list-of-publications). All papers are also available on [arXiv](https://arxiv.org/search/?searchtype=author&query=Allan%2C+M+P).**

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## Copyrights
<em>Madan Kumar Lakshmanan, Sumeet Saurav, Sanjay Singh</em><br />Smart Camera-based remote Plethysmography Techniques for Non-contact Vitals Monitoring<br /> CR Diary/Application No. 15368/2023-CO/SW, Date of Filing: 02/06/2023, Registration No. SW-16892/2023, Date of Registration: 17/07/2023.

<em>Shyam Sunder Prasad, Naval Kishore Mehta, Abeer Banerjee, Sumeet Saurav, Ravi Saini, Sanjay Singh</em><br /> AI-based Software Package for Real-time Face Anti-spoofing in Unconstrained Natural Environment <br /> CR Diary/Application No. 15783/2023-CO/SW, Date of Filing: 08/06/2023, Registration No. SW-16929/2023, Date of Registration: 20/07/2023.

<em>Shyam Sunder Prasad, Naval Kishore Mehta, Sumeet Saurav, Ravi Saini, Sanjay Singh</em><br /> AI-enabled Software Pipeline for Real-time Face Recognition-based Attendance System <br /> CR Diary/Application No. 14881/2023-CO/SW, Date of Filing: 30/05/2023, Registration No. SW-17031/2023, Date of Registration: 03/08/2023.

<em>Abeer Banerjee, Himanshu Kumar, Sumeet Saurav, Sanjay Singh</em><br /> AI-enabled Software Module for Realistic Colorization of Grayscale Images <br /> CR Diary/Application No. 15782/2023-CO/SW, Date of Filing: 08/06/2023, Registration No. SW-17058/2023, Date of Registration: 08/08/2023.

## Full List of publications

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
