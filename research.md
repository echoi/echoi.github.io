---
layout: page
permalink: /research/
title: Research
pubs:

    - title:   "Paper title in 3-7 words that sound like Clingon"
      author:  "M. McFly, D. Kirk, L. Skywalker, H.J. Potter, I. Jones, H. Houdini"
      journal: "Transactions on Black Magic"
      note:    "(presented at Oz)"
      year:    "2016"
      url:     "http://publish-more-stuff.org"
      doi:     "http://dx.doi.org"

    - author: "Hong, T.-K., E. Choi, S. Park, and J. S. Shin"
      year: "(2016)"
      title: "Prediction of ground motion and dynamic stress change in Baekdusan (Changbaishan) volcano caused by a North Korean nuclear explosion"
      journal: "Sci. Rep."
      volume: "6"
      page: "21477"
      doi: "10.1038/srep21477"
---

## Publications

{% for pub in page.pubs %}
{% if pub.internal %}[{{pub.title}}]({{pub.url | prepend: site.baseurl}}){% else %}[{{pub.title}}]({{pub.url}}){% endif %},
{{pub.author}}
{{pub.year}}.
*{{pub.journal}}*,
{% if pub.note %} *({{pub.note}})*
{% endif %} doi:[{pub.doi}]({{pub.doi | prepend: dx.doi.org}})
{% endfor %}
