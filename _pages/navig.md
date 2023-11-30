---
layout: default
permalink: /navig/
title: navigation
description: here is all my posts splitted by categories
nav: true
nav_order: 3

---
<div class="port">
{% for category in site.categories %}
    <h1 class="post-title"><i class="fas fa-tag fa-sm"></i>{{ category[0] }}</h1>
    <p class="post-desription">an archive of posts</p>

    <article>
        <div class="table-responsive">
            <table class="table table-sm table-borderless">
                {% for post in category[1] %}
                    <tr>
                        <th scope="row">{{ post.date | date: "%b %-d, %Y" }}</th>
                        <td><a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a></td>
                    </tr>
                {% endfor %}
            </table>
        </div>
    </article>
{% endfor %}
</div>