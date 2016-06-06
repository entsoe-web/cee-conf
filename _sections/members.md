---
title: speakers
order: 3
published: false
---

<div class="small-12 columns">
<div class="large-8" markdown="1">
# {{page.title | capitalize}}
{:id="{{page.title | append: '_1'}}"}
</div>
</div>
<style type="text/css">
    .photo {
    width: 160px;
    height: 160px;
    /* border: 2px dashed; */
    border-radius: 50%;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 30px;
    background-size: cover;
}

.presenter h3 {font-size: 1.3rem;font-weight: 900;}

.presenter {
    background-color: rgba(0, 0, 0, 0.28);
    padding: 30px 20px 30px 40px;
    border-radius: 10px;
    height: auto;
    margin-bottom: 30px;
    min-height: 435px;
    position: relative;
}
.presenter ul {
    -webkit-margin-before: 0px;
    -webkit-padding-start: 0px;
    margin-left: 0;
}
.presenter ul li:first-of-type {
    font-style: italic;
    opacity: 0.7;
    margin-bottom: 30px;
}
.presenter ul li {
    margin-bottom: 10px;
    list-style-type: none;
}
.presenter ul li:last-of-type {
    position: absolute;
    bottom: 20px;
}
.presenter a {
    background-color: white;
    color: #047BF6;
    padding-left: 12px;
    padding-right: 12px;
    padding-top: 3px;
    padding-bottom: 3px;
    border-radius: 20px;
    margin-right: 5px;
}
.twitter:before {
    content: '@';
}
</style>


<div class="row small-up-1 medium-up-4 large-up-4 column">
{% for speaker in site.data.speakers  %}
<div class="column">
      <div class="presenter">
      <!--/placehold.it/300x300-->
          <div class="photo x" style="background-image:url({{speaker.image |prepend:'/speaker_img/' | prepend: site.baseurl}}) "></div>
          <h3>{{speaker.name}}</h3>
          <ul>
            <li>{{speaker.position}} @ {{speaker.company}}</li>
            <li>{% unless speaker.twitter == nil %}<a href="https://twitter.com/{{speaker.twitter}}" class="twitter">{{speaker.twitter}}</a>{% endunless %}<a href="{{speaker.web}}"><i class="fa fa-globe"></i></a></li>
          </ul>
      </div>
  </div>
{% endfor %}
  
</div>