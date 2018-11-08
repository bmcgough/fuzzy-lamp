---
title: Scientific Computing Supported Resources
last_modified_at: 2018-09-14
---

## Auto-generated Table
This table is auto-generated based on the yaml in _data/scicomp_resources.yaml:

Name|Type|Authentication|Authorization|Location
---|---|---|---|---
{% for resource in site.data.scicomp_resources -%}
{{ resource.name }}|{{ resource.type }}|{{ resource.access[0].type }}|{{ resource.access[0].auth }}|{{ resource.location }}
{%- endfor -%}
