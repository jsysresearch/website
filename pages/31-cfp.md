---
permalink: /cfp
---

# Call for Papers

<!-- This all feels quite redundant. I think most of this 

- is already covered in the home page;
- has nothing to do with "CfP." 

Ultimately, that would be more content for "About" -->

<!-- The Journal of Systems Research (JSys) is a diamond open-access (no fees for authors or readers) journal that seeks to publish research that moves the field forward and will be of interest to the systems community. JSys emphasizes rigorous research that improves the state-of-the-art, even if the increment is modest. JSys requires that papers that put forth a new tool, benchmark, or software solution undergo Artifact Evaluation and make their artifact publicly available.

-->

This page present general information about the scope of JSys' call for papers and the submission deadlines.

Prospective authors should carefully read the [instructions for authors](/instructions) as well as the [journal policies](/policies) for more information.

## Aims and Scope

JSys is organized into areas with their own chairs, reviewer boards, and call for papers.
The calls clarify what is considered in scope for each area.

In addition, JSys calls for four different [paper types](#paper-types), each with its specific set of acceptance criteria.

### Active Areas

JSys currently welcomes submissions in the following areas.

{% assign areas = site.data.areas.meta.area | sort: "id" %}
{% for area in areas %}{% if area.active == 1 %}
- [{{ area.title}}](/cfp_{{area.id}}/){% endif %}{% endfor %}

### Paper Types

JSys categorizes papers into four types, each with their own publicly-available acceptance criteria. 

{% for item in site.data.papers.type %}{% if item.active == 1 %}
- [{{ item.title}}]({{item.url}}){% endif %}{% endfor %}

## Deadlines

JSys has multiple deadlines each year, each set at 11:59 PM GMT.

- March 1st
- May 1st
- August 1st
- October 1st

For each deadline, reviews will be available within 1.5 months.
For example, for a work submitted by March 1st, JSys commits to provide initial reviews by April 15th.

Recent deadlines and their submission portals:
> Note: due to a migration to a new publication platform the March 1st 2026 deadline will be extended by a week to March 8th.
{% for item in site.data.openReview.forums %}{% if item.show == 1 %}
- [{{ item.title}}]({{item.url}}) {% if item.open == 0 %} <span class="text-muted">(closed)</span>{% endif %} {% endif %}{% endfor %}

<!-- <i class="fas fa-exclamation-triangle"></i> ****  
Papers will be publicly viewable on OpenReview upon submission.  
Authors requiring secrecy of their submitted work should take this into account. -->

|<i class="fas fa-exclamation-triangle"></i>||Reminder|
|:---|:---|:---|
|||Papers will be **publicly viewable** on OpenReview **upon submission**.|
|||Authors requiring secrecy of their submitted work should take this into account.|

## Artifact Evaluation

JSys submissions for the Solution or Tools/Benchmark category **must** be accompanied by artifacts that are evaluated by [JSys Artifact Evaluation Board](cfp_artifacts/).

Refer to the [Artifact Evaluation page](/artifact_evaluation) for details about the evaluation procedure, expectations, and tips for authors.
