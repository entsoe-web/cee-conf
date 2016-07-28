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