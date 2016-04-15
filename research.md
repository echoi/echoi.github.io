---
layout: page
permalink: /research/
title: Research
pubs:

    - author: "Hong, T.-K., E. Choi, S. Park, and J. S. Shin"
      year: "(2016)"
      title: "Prediction of ground motion and dynamic stress change in Baekdusan (Changbaishan) volcano caused by a North Korean nuclear explosion"
      journal: "Sci. Rep."
      doi: "10.1038/srep21477"
      kudos: "http://goo.gl/NYQczl"

    - author: "Choi, E., and K. D. Petersen"
      year: "(2015)"
      title: "Making Coulomb angle-oriented shear bands in numerical tectonic models"
      journal: "Tectonophysics"
      doi: "10.1016/j.tecto.2015.06.026"
      kudos: "http://goo.gl/wvoYeE"

    - author: "Ta, T., K. Choo, E. Tan, B. Jang, and E. Choi"
      year: "(2015)"
      title: "Accelerating DynEarthSol3D on tightly coupled CPU–GPU heterogeneous processors"
      journal: "Comput. Geosci."
      doi: "10.1016/j.cageo.2015.03.003"
      kudos: "http://goo.gl/pLKmhL"
---

## Publications

{% for pub in page.pubs %}
{% if pub.internal %}[{{pub.title}}]({{pub.url | prepend: site.baseurl}}){% else %}[{{pub.title}}]({{pub.kudos}}){% endif %} <br />
{{pub.author}}
{{pub.year}}.
*{{pub.journal}}*,
{% if pub.note %} *({{pub.note}})*
{% endif %} doi:[{{pub.doi}}](http://dx.doi.org/{{pub.doi}}).
{% endfor %}
