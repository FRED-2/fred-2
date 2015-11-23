---
layout: home
permalink: /
image:
  feature: HIV-infected_H9_T_cell.jpg
---

<div class="tiles">

<div class="tile">
  <h2 class="post-title">What is FRED2</h2>
  <p class="post-excerpt">FRED is a framework for T-cell epitope detection, and vaccine design. It offers consistent, 
  and easy access to well established immunoinformatics methods.</p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Getting Started</h2>
  <p class="post-excerpt">The best way to familiarize yourself with FRED2 is by starting with our 
  <b><a href="http://fred-2.github.io/getting-started/">tutorials</a></b>. The 
  <b><a href="http://fred-2.github.io/getting-started/">tutorials</a></b> cover the basic 
  functionality of FRED2.</p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Documentation</h2>
  <p class="post-excerpt">We spent a significant amount of effort on documenting FRED2’s functions and classes. 
  You can find the documentation <b><a href="http://fred2.readthedocs.org">here</a></b>.</p>
</div><!-- /.tile -->

<div class="tile">
  <h2 class="post-title">Get Involved</h2>
  <p class="post-excerpt">Your favorite prediction method is missing? You discovered a bug, or just want to extend 
  FRED2's functionality? Have a look at our tutorials for developers 
  <b><a href="https://github.com/FRED-2/Fred2/wiki#for-developers">here</a></b>.</p>
</div><!-- /.tile -->

</div><!-- /.tiles -->


<div class="archive-wrap">
    <h3> Latest Posts </h3>
    <div class="bullets">
        {% for post in site.posts limit:4%}
        <div class="bullet one-col-bullet">
            <div class="bullet-icon">
                <a href="{{ site.url }}{{ post.url }}"><img src="{{ site.url }}/images/{{ post.image.teaser }}" alt=""></a>
            </div>
            <div class="bullet-content">
                <h2><a href="{{ site.url }}{{ post.url }}">{{ post.title }}  &nbsp;</a></h2>
                <small>{{ post.date | date:'%A, %B %d, %Y'}}</small>
                <article class="excerpt">{{ post.content | strip_html | truncatewords: 50 }}</article>
                <br></br>
                <small><a class="pull-left marginBottom10" href="{{ site.url }}{{ post.url }}">Read More</a></small>
            </div>
        </div>
        {% endfor %}
    </div>

</div><!-- /.tiles -->
