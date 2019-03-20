---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - key: "ding:pldi:2015"
    author: "Yufei Ding, Jason Ansel, Kalyan Veeramachaneni, Xipeng Shen, Una-May O’Reilly, Saman Amarasinghe"
    title: "Autotuning Algorithmic Choice for Input Sensitivity"
    url: "http://groups.csail.mit.edu/commit/papers/2015/yding-pldi15-pbinput.pdf"
    keywords: "OpenTuner"
    month: "June"
    year: "2015"
    address: "Portland, Oregon"
    booktitle: "ACM SIGPLAN Conference on Programming Language Design, Implementation"



  - author: "Bangwen Deng and Wenfei Wu"
    title: "Redundant Logic Elimination in Network Functions"
    month: "August"
    year: "2018"
    address: "Budapest, Hungary"
    booktitle: "Proceedings of the ACM SIGCOMM 2018 Conference on Posters and
               Demos"
    url: redundant-logic-elimination.pdf
    bibtex: DengW18.bib

  


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



