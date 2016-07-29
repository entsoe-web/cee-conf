---
title: Media &amp; Communications
layout: pub
images:
  - title: Leaderboard
    file: 'cee-leader-board-728x90.gif'
    dim: 728px x 90 px
  - title: Square
    file: 'cee-square-300x250.gif'
    dim: 300px x 250px
limiter: true
---
# Press and Media

Use the following images for advertising on your websites. They are standard square and leaderboard sizes.

{% for im in page.images  %}
<div class="medium-6 columns text-center">
<div class="pad2 fill-grey">
    <img src="{{site.baseurl | append: '/assets/media-img/'}}{{im.file}}" />
    <ul class="meta">
        <li class="keyline-bottom">URL: <a href="http://cee.entsoe.eu">http://cee.entsoe.eu</a></li>
        <li class="keyline-bottom">Dimensions: <span class="pad0 fill-navy dark">{{im.dim}}</span></li>
    </ul>
    <a class="button" href="{{site.baseurl | append: '/assets/media-img/'}}{{im.file}}">Download Advert</a>
</div>
</div>
{% endfor %}

<style type="text/css">
    .meta li {list-style: none; padding: 20px 0; border-bottom: 1px solid rgba(0,0,0,0.10);}
</style>
<script type="text/javascript" src="{{'/assets/js/app.js' | prepend: site.baseurl}}"></script>

__Use the following text to advertise the event__

## Advertising text 

> Strengthening regional cooperation in all three dimensions of markets, planning and operations is indispensable towards achieving the Internal Energy Market and towards delivering the benefits of the Energy Union to European citizens. The CEE Regional Conference, the second among three ENTSO-E regional conferences in 2016, will explore the opportunities of enhanced cooperation within and across regions from the perspective of current developments in Central and Eastern Europe.
>
> Where are we on power market integration in Europe, between Central East and Central West, 27 years after the end of the East-West divide? What are the regional infrastructure needs and how can the necessary investments be attracted? How does market, planning and operational cooperation progress, and how will the regional security coordinators further deliver results? What challenges and opportunities in the areas of TSO-DSO cooperation, smart grids and data can we expect in the future?
>
> Join ENTSO-E, its partner the Florence School of Regulation, and the TSOs of the CEE region from Slovakia, the Czech Republic, Poland, Hungary, Romania, Germany, Austria, Croatia, and Slovenia to discuss together these questions at the second ENTSO-E regional conference in 2016. The conference is organised under the patronage of the Slovak Presidency of the EU Council and of the Ministry of the Economy of the Slovak Republic. Energetika.net is the conference media partner.
> 
> [Register Now](http://cee.entsoe.eu)

