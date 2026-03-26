---
title: Projects
layout: default
permalink: /projects/
---

<div class="projects-page">
    <h1>Projects</h1>

    <div class="filter-chips">
        <button class="filter-chip active" data-filter="all">All</button>
        <button class="filter-chip" data-filter="SaaS">SaaS</button>
        <button class="filter-chip" data-filter="Mobile">Mobile</button>
        <button class="filter-chip" data-filter="Embedded Device">Embedded Device</button>
        <button class="filter-chip" data-filter="Finance">Finance</button>
    </div>

    <div class="projects-grid">
        {% for project in site.projects %}
        {% assign project_images_path = '/assets/images/portfolio/' | append: project.slug | append: '/images/' %}
        {% assign gallery_images = site.static_files | where_exp: "file", "file.path contains project_images_path" %}
        <div class="project-card" data-category="{{ project.category }}">
            <a href="{{ project.url | relative_url }}">
                <div class="project-image">
                    {% if project.image %}
                    <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" class="img-default">
                    {% else %}
                    <img src="{{ '/assets/images/portfolio/' | append: project.slug | append: '/hero.gif' | relative_url }}" alt="{{ project.title }}" class="img-default" onerror="this.style.display='none'">
                    {% endif %}
                    {% if project.hover_image %}
                    <img src="{{ project.hover_image | relative_url }}" alt="{{ project.title }}" class="img-hover">
                    {% elsif gallery_images.size > 0 %}
                    <img src="{{ gallery_images.first.path | relative_url }}" alt="{{ project.title }}" class="img-hover">
                    {% endif %}
                </div>
                <div class="title-tab">
                    <h3>{{ project.title }}</h3>
                </div>
                <div class="project-content">
                    <span class="category-tag">{{ project.category }}</span>
                    <p>{{ project.description }}</p>
                </div>
            </a>
        </div>
        {% endfor %}
    </div>
</div>
