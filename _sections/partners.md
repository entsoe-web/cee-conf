---
title: partners
order: 4
published: false
partners:
 - {name: "50", img: "50hertz.png"}
 - {name: "PSE", img: "pse.png"}
 - {name: "eles", img: "eles.png"}
 - {name: "hops", img: "hops.png"}
 - {name: "mavir", img: "mavir.png"}
 - {name: "SEPS", img: "seps.png"}
 - {name: "ceps", img: "ceps.png"}
 - {name: "apg", img: "apg.png"}
 - {name: "te", img: "te.png"}
 - {name: "fsr", img: "fsr.png"}
---

<style type="text/css">
    .part-img {
        
    }
    .wb-50 {
        width:50% !important;
    }
    .partners .columns:last-child:not(:first-child) {
        float: none;
        margin-left: auto;
        margin-right: auto;
    }
    .clear {clear: both;}
</style>

<div class="small-12 columns">
<div class="large-8 text-center small-centered" markdown="1">
# {{page.title | capitalize}}
{:id="{{page.title | append: '_1'}}" style="padding-bottom:1em;"}
</div>
</div>

<div class="row">
<div class="large-8 small-centered partners">
{% for sp in page.partners %}
<div class="{% if forloop.last %}medium-3{%else%}medium-3{% endif %} text-center {{sp.css}} columns">
    <img class="part-img" src="{{sp.img | prepend: "./assets/img/tso/"}}" alt="{{sp.name}}">
</div>
{% endfor %}
</div>
</div>