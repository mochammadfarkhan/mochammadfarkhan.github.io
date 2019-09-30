---
layout: page
title: portfolio
permalink: /portofolio
---
<html>
  <head>
    <style>
      body {
        text-align: center;
        background-color: #f0e8c5;
      }
      div {
        margin-top: 15px;
      }
      image-section {
        display: flex;
        justify-content: center;
      }
      section-style {
        margin-right: 25px;
        margin-left: 25px;
        background-color: white;
      </style>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <link rel="stylesheet" href="_styles/styles.css" />

    <div class="image-section">
      <div class="section-style">
        <img src="https://source.unsplash.com/random/400x200" alt="" />
        <p>A random image courtesy of unsplash.com.</p>
      </div>

      <div class="section-style">
        <img src="https://source.unsplash.com/random/400x200" alt="" />
        <p>A random image courtesy of unsplash.com.</p>
      </div>
    </div>

    <div class="image-section">
      <div class="section-style">
        <img src="https://source.unsplash.com/random/400x200" alt="" />
        <p>A random image courtesy of unsplash.com.</p>
      </div>

      <div class="section-style">
        <img src="https://source.unsplash.com/random/400x200" alt="" />
        <p>A random image courtesy of unsplash.com.</p>
      </div>
    </div>
  </body>
</html>

<p><b>html + css</b> : including themes for Jekyll and other web based projects.</p>
{% for project in site.portfolio %}
{% if project.cat == "web" %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% endif %}
{% endfor %}

<div class="clearfix"></div>
<br/>
<hr/>
<br/>

<p><b>architecture</b> : projects completed for studio and computational architecture classes.</p>
{% for project in site.portfolio %}
{% if project.cat == "arch" %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% endif %}
{% endfor %}
