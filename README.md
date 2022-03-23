---
layout: default
title: Member Handbook
nav_order: 1
permalink: /
---

# Member Handbook

Your handy handbook to being a member of Farset Labs Hackerspace.
{: .fs-6 .fw-300 }

[Become a Member](https://farsetlabs.spaces.nexudus.com/){: .btn .btn-purple }
[Go to the Farset Labs Website](https://www.farsetlabs.org.uk){: .btn }

In this handbook we cover everything from your first visit, to helping manage the hackerspace. So, depending on the area some content can be fairly technical. However, all writing should be clear enough for anyone to be able to pick up the handbook and figure things out without relying on tribal knowledge.

Members are welcome and encourated to edit the handbook. If you want to learn about how to do it, check out [Just the Docs](https://github.com/just-the-docs/just-the-docs) documentation.

## Contributors

{% comment %}Using the jekyll-github-metadata plugin included with github-pages.{% endcomment %}
{% comment %}These assignments will randomise the order of listing contributors on deployment.{% endcomment %}
{% assign number_of_contributors = site.github.contributors | size %}
{% assign contributors = site.github.contributors | sample: number_of_contributors %}

{% for contributor in contributors %}
![]({{contributors.avatar_url}})
[{{contributor.login}}]({{contributor.html_url}})
{% endfor %}

## Contributors

<a href="https://github.com/farsetlabs/member-handbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=farsetlabs/member-handbook"/>
</a>
