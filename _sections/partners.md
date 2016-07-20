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
 - {name: "edk", img: "energy-dk.png"}

---
{% comment %}
 - {name: "sk-pres", img: "sk-logo.svg"}
{% endcomment %}
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

.partner-logo.logo-centered img, .partner-logo.logo-centered svg {
    margin: auto;
}
    .partner-logo img, .partner-logo svg {
    width: auto;
    top: 50%;
    max-width: 85%;
    -webkit-transform: translateY(-50%);
    -o-transform: translateY(-50%);
    -ms-transform: translateY(-50%);
    -moz-transform: translateY(-50%);
    transform: translateY(-50%);
    opacity: .8;
    height: 100%;
    max-height: 90%;
    position: absolute;
    left: 0;
    right: 0;
    display: block;
}
.limiter {
    width: 83.3333%;
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
}
.col3 {
    float: left;
    width: 25.0000%;
    max-width: 300px;
}

.partner-logos div {
    height: 120px;
    position: relative;
}

@media screen and (max-width: 640px) {
.col1, .col2, .col3, .col4, .col5, .col6, .col7, .col8, .col9, .col10, .col11, .col12, .fifths > * {
    width: 100%;
    max-width: 100%;
}
}
</style>

<div class="small-12 columns">
<div class="large-8 text-center small-centered" markdown="1">
# {{page.title | capitalize}}
{:id="{{page.title | append: '_1'}}" style="padding-bottom:1em;"}
</div>
</div>

<div class="small-12 columns">
<div class="large-8 text-center small-centered">
<a class="button large" href="{{site.baseurl}}/partners">Find out more about our partners</a>
</div>
</div>


<div class="limiter">
    <div class="clearfix partner-logos">
        {% for sp in page.partners %}
        <div class="col3">
            <span class="block partner-logo logo-centered">
                <img src="{{sp.img | prepend: "./assets/img/tso/"}}" alt="{{sp.name}}">
            </span>
        </div>
        {% endfor %}
    </div>
</div>