---
layout: default
title:  Dojo自慢
permalink: /dojos
---

<div class="container mt-5">
  <div class="row">
    <div class="col-md-6 offset-md-3 col-12">
      <h1>Dojo自慢</h1>
    </div>
  </div>
  <div class="row">
    <div class="col-12 p-3" id="timetable">
      <p>
        DojoCon Japanでは「Dojo自慢」を募集しています。
      </p>
      <p>
        ご投稿につきましては、以下に掲載させていただきました。
      </p>
      {% for page in site.pages %}
      {% if page.layout == "jiman_media" or page.layout == "jiman_text" %}
      <div class="page">
        <div class="row">
          <div class="col-6 col-md-2">
            <div class="row">
              <div class="col-4 col-md-3 jiman1">
                {% if page.dojo_icon %}
                <img src="https://coderdojo.jp/img/dojos/{{ page.dojo_icon }}" width="100%" alt='Dojo アイコン' />
                {% elsif page.dojo_iconfile %}
                <img src="/img/post/jiman/{{ page.dojo_iconfile }}" width="100%" alt='Dojo アイコン' />
                {% else %}
                <img src="/img/coderdojo.png" width="100%" alt='CoderDojo ロゴ'/>
                {% endif %}
              </div>
              <div class="col-8 col-md-9 jiman1">
                <p class="text-left dojoname">{{ page.dojo_name }}</p>
              </div>
            </div>
          </div>
          <div class="col-9 col-md-8">
            <a href="{{ page.url }}"> <span class="text-left h2">{{ page.title }}</span></a>
          </div>
          <div class="col-3 col-md-2 d-flex align-items-center">
            <a href="{{ page.url }}" class="btn btn-main">もっと見る</a>
          </div>
        </div>
      </div>
      {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<style>
  .dojoname{
    text-align: center;
    padding: 0.8em;
  }
  .jiman1{
    padding-right: 0 !important;
    padding-left: 0 !important;
  }
</style>
