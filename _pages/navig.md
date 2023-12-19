---
layout: default
permalink: /navig/
title: TOC
# description: table of content
nav: true
nav_order: 2

---
<div class="port">
{% for category in site.categories %}
    <h1 class="post-title">{{ category[0] }}</h1>

    <article style="padding-top:20px; padding-bottom: 20px">
        <div class="table-responsive">
            <table class="table table-sm table-borderless">
                {% for post in category[1] %}
                    <tr>
                        <th style="width:200px" scope="row">{{ post.date | date: "%b %-d, %Y" }}</th>
                        <td><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a></td>
                    </tr>
                {% endfor %}
            </table>
        </div>
    </article>
{% endfor %}
</div>