---
layout: page
title: Cloud Commander Blog
tagline: blog about cloud file manager
---
{% include JB/setup %}

<ul class="posts">
    {% for post in site.posts %}
        <article class="post">
            <header class="post-header">
                <span class="post-meta"><time datetime="{{ post.date | date_to_string }}">{{ post.date | date_to_string }}</time> </span>
                <h2 class="post-title"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
            </header>
            <section class="post-excerpt">
                <p>{{ post.description }}</p>
            </section>
        </article>
    {% endfor %}
</ul>
