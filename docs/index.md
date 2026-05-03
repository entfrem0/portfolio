---
title: Portfolio
short_title: Index
lead: This portfolio shows projects in science and engineering fields.
layout: default
nav_order: 0
sidebar_title: Related Articles
---

## Introduction

ここに説明を加える

## Find out of categories

<div class="kb-cards">
  {% assign all_pages = site.pages | sort: "nav_order" %}

  {% for sec in site.sections %}
    {% assign sec_key = sec[0] %}
    {% assign sec_meta = sec[1] %}

    {% assign section_pages = all_pages | where: "section", sec_key | sort: "nav_order" %}

    {% if section_pages and section_pages.size > 0 %}
      <section class="kb-card">
        <header class="kb-card__header">
          <h2 class="kb-card__title">
            <a href="{{ sec_meta.url | relative_url }}">{{ sec_meta.title | default: sec_key }}</a>
          </h2>

          {% if sec_meta.description %}
            <p class="kb-card__desc">{{ sec_meta.description }}</p>
          {% endif %}
        </header>

        <ul class="kb-card__list">
          {% for p in section_pages limit: 3 %}
            {% if p.title and p.url != sec_meta.url %}
              <li class="kb-card__item">
                <a class="kb-card__link" href="{{ p.url | relative_url }}">{{ p.title }}</a>
                {% if p.lead %}
                  <div class="kb-card__meta">{{ p.lead }}</div>
                {% endif %}
              </li>
            {% endif %}
          {% endfor %}
        </ul>

        <div class="kb-card__footer">
          <a class="kb-card__more" href="{{ sec_meta.url | relative_url }}">View All →</a>
        </div>
      </section>
    {% endif %}
  {% endfor %}
</div>