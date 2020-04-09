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
    booktitle: "Proceedings of the ACM SIGCOMM 2018 Conference on Posters and
               Demos"
    url: redundant-logic-elimination.pdf
    bibtex: DengW18.bib
  - author: "Bangwen Deng, Wenfei Wu, Linhai Song"
    title: "NFReducer: Redundant Logic Elimination in Network Functions"
    month: "March"
    year: "2020"
    address: "San Jose, CA, USA"
    booktitle: "The ACM Symposium on SDN Research (ACM SOSR 2020)"
    url: NFReducer-SOSR20.pdf
    bibtex: NFReducer-SOSR20.bib


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



