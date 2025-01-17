---
permalink: /board
---

# Editorial board

The editorial board of JSys is made of people committed to open access for all, open review, and high-quality feedback.

## Areas

JSys editorial board is organized into topical areas, with their own chairs, reviewer boards, and call for papers. Below is the list of active areas and their current chairs.

<!-- I tried compacting with <summary> but it is not supported by Jekyll by default. Here is how it can be done if we really want it.:
http://movb.de/jekyll-details-support.html -->

<!-- Loop through all areas -->
{% assign areas = site.data.areas.meta.area | sort: "id" %}
{% for area in areas %}
{% if area.active == 1 %}
{% assign active_chairs = site.data.areas[area.id].board.chairs | where_exp: "person", "person.until==0" | sort: "name"%}
- [{{area.title}}](/cfp_{{area.id}}/){% for chair in active_chairs %}
  - [{{chair.name}}]({{chair.webpage}}), {{chair.affiliation}}{% endfor %}
{% endif %}{% endfor %}<!-- Loop through all areas -->

## Artifact Evaluation Board

The [Artifact Evaluation Board](/cfp_artifacts/) is chaired by
{% for chair in site.data.areas.artifacts.board.chairs %}
  - [{{ chair.name}}]({{chair.webpage}}), {{chair.affiliation}}{% endfor %}

## Journal Management

### Editors-in-Chief

{% for person in site.data.management.eic %}- [{{ person.name}}]({{person.webpage}})  
    {{person.affiliation}}  
    <i class="fab fa-orcid"></i>   &nbsp; [{{person.orcid}}](https://orcid.org/{{person.orcid}})  
    <i class="fab fa-twitter"></i> &nbsp; [@{{person.twitter}}](https://twitter.com/{{person.twitter}})
{% endfor %}

### Assistant Editors

{% assign assistants = site.data.management.assistants | sort: "name" %}

{% for person in assistants %}
- [{{ person.name}}]({{person.webpage}}), {{person.affiliation}}{% endfor %}

### Publicity Chairs

{% assign publicity = site.data.management.publicity | sort: "name" %}

{% for person in publicity %}
- [{{ person.name}}]({{person.webpage}}), {{person.affiliation}}{% endfor %}

### Former members

{% assign alumni = site.data.management.alumni | sort: "until" | reverse %}

{% for person in alumni %}
- [{{ person.name}}]({{person.webpage}}), {{person.role}} until {{person.until}}{% endfor %}

## Co-Founders

{% for member in site.data.co-founders.list %}- [{{ member.name}}]({{member.webpage}})  
    [<i class="fab fa-orcid"></i>   &nbsp; {{member.orcid}}](https://orcid.org/{{member.orcid}})  
{% endfor %}
