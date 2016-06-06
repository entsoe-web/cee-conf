---
layout: pub
title: "Home"
permalink: "/"
---

<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">


<div class="bleed-section" style="background-size:cover;color:#fff;height:30em;background-image:url({{'/assets/img/header-3.jpg' | prepend:site.baseurl ;}});">

<a href="" id="first"></a>

<div class="medium-12 columns text-center" markdown="1" style="text-shadow: 0px 0px 3px rgba(0, 0, 0, 0.6);">
# Completing the European Power Market Integration
{:class="page-title" style="margin-top:50px;"}

## A Central East European Perspective
{:class="page-title"}

<div class="text-center" style="margin-top:2em;">
<p style="font-weight: 600;">Bratislava, Slovakia - 22 - 23 September 2016</p>
<a class="button large" href="{{'/register' | prepend: site.baseurl}}">Register now!</a>
</div>
<div class="text-center" style="margin-top:2em;">
<a href="#about" class="page-scroll button large btn-circle"><i class="fa fa-angle-down"></i></a>
</div>

</div>

</div>


{% assign sections2 = site.sections | sort: 'order' %}
{% for section in sections2 %}
{% if section.title != "intro" %}
{% assign slug = {{section.title | slugify}} %}
{% include section_block.html section_id=slug section_content=section.content fill_class=section.fill order=section.order %}
{% endif %}
{% endfor %}

<style type="text/css">
.page-title {font-weight: 900;}
.custom-nav {
    background: 0 0;
    -webkit-transition: background .5s ease-in-out,padding .5s ease-in-out;
    -moz-transition: background .5s ease-in-out,padding .5s ease-in-out;
    transition: background .5s ease-in-out,padding .5s ease-in-out;
}
.top-nav-collapse {
    padding:10px 2%;
    background-color:#0253A6;
    border-bottom: 10px solid #444;
    color: #FFF;
}
.btn-circle {
    width: 70px;
    height: 70px;
    margin-top: 15px;
    padding: 15px 18px;
    border: 2px solid #fff;
    border-radius: 35px;
    font-size: 40px !important;
    color: #fff;
    background: 0 0;
    -webkit-transition: background .3s ease-in-out;
    -moz-transition: background .3s ease-in-out;
    transition: background .3s ease-in-out;
}

.active {font-weight: 900;border-bottom:3px solid white;}
.global-header {border-bottom: none;}
</style>



<script type="text/javascript" src="{{'/assets/js/app.js' | prepend: site.baseurl}}"></script>
<script type="text/javascript">
$(window).scroll(function() {
    if (($(".sticky").offset().top - $("#first").offset().top) > 10) {
        $(".sticky").addClass("top-nav-collapse");
    } else {
        $(".sticky").removeClass("top-nav-collapse");
    }
});
    $(function() {
    $('a.page-scroll').bind('click', function(event) {
        var $anchor = $(this);
        $('html, body').stop().animate({
            scrollTop: $($anchor.attr('href')).offset().top
        }, 1500, 'easeInOutExpo');
        event.preventDefault();
    });
});
</script>

