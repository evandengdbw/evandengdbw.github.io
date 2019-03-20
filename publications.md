---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "Bangwen Deng and Wenfei Wu"
    title: "Redundant Logic Elimination in Network Functions"
    month: "August"
    year: "2018"
    address: "Budapest, Hungary"
    booktitle: "Proceedings of the {ACM} {SIGCOMM} 2018 Conference on Posters and
               Demos, {SIGCOMM} 2018, Budapest, Hungary, August 20-25, 2018"
    <!-- url: redundant-logic-elimilation.pdf -->
    bibtex: DengW18.bib

<!--   - title: Adaptive Checkpointing for Master-Worker Style Parallelism
    author: "Gene Cooperman, Jason Ansel, Xiaoqin Ma"
    booktitle: "IEEE Computer Society International Conference on Cluster Computing"
    address: "Boston, MA"
    month: Sep
    year: 2005
    type: Extended Abstract
    url: 2005cluster.pdf
    bibtex: 2005cluster.bib -->
<!-- - key: "ansel:smart:2011"
    author: "Jason Ansel"
    title: "Autotuning Aspects of PetaBricks"
    booktitle: "Workshop on Statistical, Machine Learning Approaches to Architecture, Compilation (SMART)"
    keywords: "PetaBricks"
    hidden: true
    type: "Talk"
    month: "April"
    year: "2011" -->



---

# Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).
    {% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}.<br>
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}



