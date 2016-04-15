---
layout: page
permalink: /research/
title: Research
pubs:

    - author: "Hong, T.-K., E. Choi, S. Park, and J. S. Shin"
      year: "(2016)"
      title: "Prediction of ground motion and dynamic stress change in Baekdusan (Changbaishan) volcano caused by a North Korean nuclear explosion"
      journal: "Sci. Rep."
      kudos: "http://goo.gl/NYQczl"
      doi: "10.1038/srep21477"
---

## Publications

{% for pub in page.pubs %}
{% if pub.internal %}[{{pub.title}}]({{pub.url | prepend: site.baseurl}}){% else %}[{{pub.title}}]({{pub.url}}){% endif %},
{{site.baseurl}}
{{pub.author}}
{{pub.year}}.
*{{pub.journal}}*,
{% if pub.note %} *({{pub.note}})*
{% endif %} doi:[{{pub.doi}}](dx.doi.org/{{pub.doi}}).
<!-- Read about this paper on Kudos as well: [{{pub.kudos}}]({{pub.kudos}}) -->
{% endfor %}
