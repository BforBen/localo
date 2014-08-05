---
layout: default
title: Localo
---
This project's goal is to author, through community consensus, **local government data specifications** relating to the services and information provided by local government. A related goal is to make it easier for civic developers to create additional software built on these standards.

## Specifications

<div class="row">
  <div class="col-xs-4">
    <nav>
      <h3>Contents</h3>
      <ol class="list-group">
      {% assign sorted_pages = (site.pages | sort:"category" | where: "type", "spec" ) %}
      {% for p in sorted_pages %}
        {% ifchanged p.version %}
          <li class="list-group-item"><a href="#{{ p.category }}">{{ p.category | capitalize }}</a></li>
        {% endifchanged %}
      {% endfor %}
      </ol>
    </nav>
  </div>

  <div class="col-xs-8">
      {% assign sorted_pages = (site.pages | sort:"category" | where: "type", "spec" ) %}
      {% for p in sorted_pages %}
        {% ifchanged p.version %}
          <h3 id="#{{ p.category }}">{{ p.category | capitalize }}</a></h3>
        {% endifchanged %}
      {% endfor %}
      {% assign version_category = 'waste' %}
      {% include _versions-links.html %}
  </div>
</div>