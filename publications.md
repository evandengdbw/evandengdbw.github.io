---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "**Bangwen Deng**, and Wenfei Wu"
    title: "NFOpt: Eliminating Redundant Logic in NF Programs using Operation-Time Configurations"
    <!-- month: "March" -->
    year: "2021"
    <!-- address: "San Jose, CA, USA" -->
    booktitle: "<small>In IEEE International Conference on Computer Communications(INFOCOM 2021)</small>"
    <!-- url: NFReducer-SOSR20.pdf -->
    <!-- bibtex: NFReducer-SOSR20.bib -->
  - author: "Hongyi Huang, Wenfei Wu, Yongchao He, **Bangwen Deng**, Ying Zhang, Yongqiang Xiong, Guo Chen, Yong Cui, and Peng Cheng."
    title: "NFD: A Development Framework for Cross-Platform Network Functions"
    <!-- month: "March" -->
    year: "2021"
    <!-- address: "San Jose, CA, USA" -->
    booktitle: "<small>In IEEE International Conference on Computer Communications(INFOCOM 2021)</small>"
    <!-- url: NFReducer-SOSR20.pdf -->
    <!-- bibtex: NFReducer-SOSR20.bib -->
  - author: "Harsha Sharma, Wenfei Wu, and **Bangwen Deng**."
    title: "Symbolic Execution for Network Functions with Time-Driven Logic"
    <!-- month: "March" -->
    year: "2020"
    <!-- address: "San Jose, CA, USA" -->
    booktitle: "<small>*In: Proceedings of the 2020 Symposium on Modelling, Analysis, and Simulation of Computer and Telecommunication Systems. MASCOTS’20*.</small>"
    <!-- url: NFReducer-SOSR20.pdf -->
    <!-- bibtex: NFReducer-SOSR20.bib -->
  - author: "**Bangwen Deng**, Wenfei Wu, Linhai Song"
    title: "NFReducer: Redundant Logic Elimination in Network Functions"
    <!-- month: "March" -->
    year: "2020"
    <!-- address: "San Jose, CA, USA" -->
    booktitle: "<small>The ACM Symposium on SDN Research (ACM SOSR 2020)</small>"
    url: NFReducer-SOSR20.pdf
    bibtex: NFReducer-SOSR20.bib
  - author: "**Bangwen Deng** and Wenfei Wu"
    title: "Redundant Logic Elimination in Network Functions"
    <!-- month: "August" -->
    year: "2018"
    <!-- address: "Budapest, Hungary" -->
    booktitle: "<small>In Proceedings of the ACM SIGCOMM 2018 Conference on Posters and
               Demos</small>"
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
    <!-- {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %} -->{{pub.booktitle}}.
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.year}}.<br> {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}


<!-- {{pub.school}}{{pub.journal}} -->


