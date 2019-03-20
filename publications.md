---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
<!--   - author: "Bangwen Deng and Wenfei Wu"
    title: "Redundant Logic Elimination in Network Functions"
    month: "August"
    year: "2018"
    address: "Budapest, Hungary"
    booktitle: "Proceedings of the ACM SIGCOMM 2018 Conference on Posters and
               Demos"
    url: "https://github.com/evandengdbw/evandengdbw.github.io/blob/master/publications/redundant-logic-elimination.pdf" 
    bibtex: DengW18.bib -->

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

- key: "ding:mitcsail-tr:2014"
    author: "Yufei Ding, Jason Ansel, Kalyan Veeramachaneni, Xipeng Shen, Una-May O'Reilly, Saman Amarasinghe"
    month: "June"
    year: "2014"
    title: "Autotuning Algorithmic Choice for Input Sensitivity"
    url: "http://groups.csail.mit.edu/commit/papers/2014/MIT-CSAIL-TR-2014-014.pdf"
    keywords: "PetaBricks"
    number: "MIT/CSAIL Technical Report MIT-CSAIL-TR-2014-014"
    type: "Technical Report"
    address: "Cambridge, MA"
    institution: "Massachusetts Institute of Technology"



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



