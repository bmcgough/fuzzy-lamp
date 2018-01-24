---
layout: default
title: linux docs
---

{% for linux in site.linux %}


<a href="{{ linux.url | prepend: site.baseurl }}">
        <h2>{{ linux.title }}</h2>
</a>

<p class="post-excerpt">{{ linux.description | truncate: 160 }}</p>

{% endfor %} 
