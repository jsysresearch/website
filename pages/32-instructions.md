---
permalink: /instructions
---

# Instructions for Authors

This page provides detailed instructions for authors submitting to JSys.

> Prospective authors should also read carefully the [journal policies](/policies) for more information.

## Communication via OpenReview

JSys uses [OpenReview](https://openreview.net/) for submission, review, revision, and comments.

The area chairs and reviewers will communicate with authors via OpenReview comments. Please ensure that you receive emails from the OpenReview system. We recommend authors to sign in regurlarly in OpenReview to ensure they do not miss an important notification.

## Submitting a New Paper

JSys uses [OpenReview](https://openreview.net/) for submitting and reviewing papers. Papers should be submitted electronically as PDF.
Papers and artifacts are reviewed separately.

JSys opens new submission forums for each deadline. Here are the links for recent and upcoming deadlines.

{% for item in site.data.openReview.forums %}{% if item.show == 1 %}
- [{{ item.title}}]({{item.url}}) {% if item.open == 0 %} <span class="text-muted">(closed)</span>{% endif %} {% endif %}{% endfor %}

### Formatting Instructions

All text and figures must fit within a 7” x 9” text block, centered on the page, using two columns with .33 inches of separation. The paper should be typeset using a 10-point font (Times New Roman or similar) with a 12-point (single-spaced) leading.

The easiest (and recommended) way to follow these formatting instructions is to use the [JSys LaTeX template](#template) (see below).

**Double Blind**. JSys reviews papers in a double-blind fashion: the reviewers do not know who the authors are, and the authors do not know who the reviewers are (until acceptance). The authors must make a good-faith effort to ensure the submitted document cannot identify the authors or their institution. For example, if they build on their own prior work, it should be referred to in the third person (i.e., “The paper by Brown et al.” and not “Our previous paper”).

**Open Source**. JSys encourages authors to make their code, data, and other artifacts open source.
However, if the open source repository is _not_ anonymized, it should not be linked directly in the submitted paper, as doing so breaks double-blindness. Instead, one simple way to link an already published repository to your JSys submission is to use services such as [Anonymous GitHub](https://anonymous.4open.science/).

**Page Limits**. There is no page limit. **However**, we strongly encourage authors to make their paper as brief as possible. Reviewer time and attention are limited; a compelling case for the paper must be made in the first 12-14 pages.

### Template

The JSys LaTeX template is available on [GitHub](https://github.com/jsysresearch/template). To get started and build a sample PDF:

```bash
git clone https://github.com/jsysresearch/template.git
cd template
make
```

Alternatively, one can download the zip file [here](https://github.com/jsysresearch/template/archive/refs/heads/main.zip) and import the zip in, e.g., Overleaf.

### DOI and Bibliography

JSys articles are assigned a Crossref DOI upon publication.

Consequently, every reference in the bibliography must include a DOI whenever available. The [JSys LaTeX template](#template) includes everything necessary to display DOIs according to [Crossref's guidelines](https://www.crossref.org/display-guidelines/). The only thing you have to do is **fill in the DOI fields** in your `.bib` file.

## Submitting a Revision

If the authors receive a [*Revise* decision](/policies#revise), they will are invite to submit their revised manuscript in a subsequent JSys deadline.

A revision is a contract between the authors and the reviewers: as long as the authors complete the requested changes in good faith by the deadline, the paper will be accepted after a quick review.
Nevertheless, the editors reserve the right to reject the paper if additional evidence indicates that the central hypothesis or result of the paper no longer holds.

The revised manuscript must be submitted on OpenReview and include:

- A cover letter explaining the changes made, and how they address reviewer concerns. The cover letter can take as many pages as required. Authors should be thorough in responding to reviewer comments.
- The revised manuscript with changes highlighted for easy reviewing.

In case authors are unsure if or how they should address a given point from the reviews, they should contact the area chairs via OpenReview or email for assistance.

## Preparing the Final Version

> Congratulations on getting your work accepted to JSys!

For the final version of the PDF, please use the `jsys_camera_ready.tex` [template](https://github.com/jsysresearch/template). Please note that the final version should use the `jsys_camera_ready` package (`jsys_camera_ready.tex` does this by default) and that the title should not be prefixed with the paper type. The final version should also include the authors and their affiliation. We strongly encourage including ORCIDs.

The final version should be uploaded using the "Final version" button on OpenReview. Please leave a comment ("Official Comment" button) indicating that the final version has been uploaded (this is important to notify the Area Chair).

One of the authors, on behalf of all authors, must sign [this publication agreement](https://github.com/jsysresearch/community/blob/main/agreement.pdf), and mail it to `editors@jsys.org`.

Once the PDF and the signed agreement are received, we will publish the final PDF on the website within two business days.

|<i class="fas fa-exclamation-triangle"></i>||Reminder|
|:---|:---|:---|
|||Solution and Tools/Benchmark papers are **required** to pass the [JSys Artifact Evaluation](#artifact-evaluation) prior to publication. |
|||If artifacts are missing or not yet accepted, we will hold the publication of accepted manuscripts until the accompanying artifacts pass the artifact evaluation as well.|

## Artifact Evaluation

JSys submissions for the Solution or Tools/Benchmark category **must** be accompanied by artifacts that are evaluated by JSys Artifact Evaluation Board.
Different from traditional evaluations, note that the JSys Artifact Evaluation proceeds **in parallel** of the paper evaluation (and not after the paper has been accepted).

Refer to the [Artifact Evaluation page](/artifact_evaluation) for details about the evaluation procedure, expectations, and tips for authors.

### Referencing the Artefact

The recommended method to reference an artifact is using a service like [Zenodo](https://about.zenodo.org/) to obtain a DOI and a persistent link.
Zenodo interfaces directly with GitHub, the instructions can be found [here](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content).

## Conflicts

When submitting your paper to JSys, authors must provide information about their conflicts with reviewers on the editorial board.
JSys considers the following cases as conflicts.

- The reviewer is your PhD or post-doc advisor.
- You are currently employed at the same institution, have been previously employed at the same institution within the past two years (not counting concluded internships), or are going to begin employment at the same institution during the reviewing period.
- You have collaborated with the reviewer on a publication, grant, or other academic projects in the past two years.

> Students are conflicted with an institution only when they are doing an internship at that institution. For example, if Jane does an internship with X in summer 2020, and then another internship with X in summer 2021, Jane is free to review papers from X (provided they are not from her direct collaborators) as long as she is not currently doing an internship at X.

Authors _must not_ improperly identify a reviewer as in conflict if none of these circumstances applies; doing so may lead to the work being rejected without review. In particular, note that reviewers are _not_ considered as conflicts if

- They have reviewed the work before, or
- You have discussed the work with them, or
- They are your personal friend.

The Editor-in-Chief and Area Chairs will review paper conflicts to ensure the integrity of the reviewing process, adding or removing conflicts if necessary. If you have any questions about conflicts, please [contact the Editor-in-Chiefs](/contact).

## Advertising

JSys allows authors to advertise their work under submission as long as minimal precautions are taken to not blatantly violate double-blind reviewing.

We describe common cases below. In case of doubts, please [contact the Editors-in-Chief](/contact).

### Arxiv

JSys allows submission of papers already uploaded on Arxiv. However,

- the title of the JSys submission must be different from the Arxiv submission, and
- the system's name (if any) used in the two papers must be different.

The authors should make a good-faith effort to preserve the double-blind nature of the JSys submission.

> Please inform the Editor-in-Chief and Area Chairs if there is a previous Arxiv submission; this helps if reviewers unintentionally find the Arxiv paper.

### Social Media

JSys does not forbid authors to advertise their work on social media.
However, they should do not link to the OpenReview submission, as doing so breaks double-blindness.

For example,

- Tweeting “We have done some work on FooBar, here’s the Arxiv paper” is fine. 
- Tweeting “We have just submitted our work on FooBar to JSys! We are submission #42” is not fine.
