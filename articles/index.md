---
layout: archive
title: "Articles"
date: 2014-05-30T11:39:03-04:00
modified:
tags: []
image:
  feature: HIV-infected_H9_T_cell_45h.png
  teaser: mhc.png
  thumb: mhc.png
 
---

<div class="archive-wrap">
    <div class="bullets">
        {% for post in site.posts %}
        <div class="bullet one-col-bullet">
            <div class="bullet-icon">
                <a href="{{ site.url }}{{ post.url }}"><img src="{{ site.url }}/images/{{ post.image.teaser }}" alt=""></a>
            </div>
            <div class="bullet-content">
                <h2><a href="{{ site.url }}{{ post.url }}">{{ post.title }}  &nbsp;</a></h2>
                <small>{{ post.date | date:'%A, %B %d, %Y'}}</small>
                <article class="excerpt">{{ post.content | strip_html | truncatewords: 50 }}</article>
                <br></br>
                <small><a class="pull-left marginBottom10" href="{{post.url | prepend: site.baseurl }}">Read More</a></small>
            </div>
        </div>
        {% endfor %}
    </div>
</div><!-- /.tiles -->