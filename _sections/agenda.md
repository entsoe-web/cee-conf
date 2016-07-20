---
title: agenda
order: 2
fill: 'fill-grey'
---
<style type="text/css">
    .speakers {display: block;}
    .panel-name {font-weight: 900;}
    #agenda table>tbody>tr>td {font-weight: 200}
    #agenda table {color: #333;}
    #agenda table>tbody>tr>td {border-top: 1px solid #ddd;vertical-align: top;background-color:transparent;}
    #agenda table>tbody>tr {background-color: transparent;}
    #agrenda table thead, #agenda table tbody {background-color: transparent;border:0;}
</style>
{% assign events = site.events | sort: 'time' %}

<div class="small-12 columns">
<div class="large-8" markdown="1">
# {{page.title | capitalize}}
{:id="{{page.title | append: '_1'}}"}
</div>
</div>

<table>
<thead>
    <tr>
        <th>Time</th>
        <th>Event</th>
    </tr>
</thead>
<tbody>
{% comment %}
{% for i in site.data.baltics_agenda %}
<tr><td>{{i.Time}}</td><td>{{i.Event}}</td></tr>
{% endfor %}
{% endcomment %}

{% for i in events %}
{% if i.type == 'multi' %}
<tr><td>{{i.time}}</td>
    {% for title in i.titles  %}
    <td>{{title}}</td>
    {% endfor %}
</tr>
{%else%}
<tr>
 <td>{{i.time}}</td>
 <td colspan="2">
   {% if i.type == "break" %}
   {{i.title}}
   {% else %}
   <a href="{{i.url | prepend: site.baseurl}}" class="panel-name">{{i.title}}</a>
   {% endif %}
   <span class="speakers">
   {{i.speakers | join: ', '}} {% if i.moderator %}<br>Moderator: {{i.moderator}}{% endif %}
   </span>
 </td>
</tr>
{% endif %}
{% endfor %}


</tbody>
</table>