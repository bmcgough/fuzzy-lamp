---
title: About this Wiki
layout: splash
permalink: /
---

## Auto-generated Table
This table is auto-generated based on the yaml in _data/resources.yaml:

Name|Type|Authentication|Authorization|Location
---|---|---|---|---
{%- for resource in site.data.resources %}
{{ resource.name }}|{{ resource.type }}|{{ resource.access[0].type }}|{{ resource.access[0].auth }}|{{ resource.location }}

{%- endfor %}

## This is the next section

Node Type|Cores|RAM|CPU|Node Count
{%- for node in site.data.resources.gizmo.nodes %}
{{ node }}|{{ node.cores }}|{{ node.memory_gb }}|{{ node.processor_model }}|{{ node.node_count }}
{%- endfor %}

