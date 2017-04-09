---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
 
 - author: "W. Ke, T. Zhang, J. Chen, F. Wan, Q. Ye and Z. Han"
    title: "Texture Complexity based Redundant Regions Ranking for Object Proposal"
    keywords: "object proposal"
    month: "July "
    year: "2016"
    address: "Las Vegas, USA"
    booktitle: "IEEE International Conference on Computer Vision and Pattern Recognition Workshop (CVPRW)"
    url: http://www.cv-foundation.org/openaccess/content_cvpr_2016_workshops/w24/papers/Ke_Texture_Complexity_Based_CVPR_2016_paper.pdf
    bibtex: ke2016proposal.bib
    
  - author: "W. Ke, Y. Zhang, P. Wei, Q. Ye and J. Jiao"
    title: "Pedestrian detection via PCA filters based convolutional channel features"
    keywords: "Pedestrian detection"
    month: "April "
    year: "2015"
    address: "Brisbane, Australia"
    booktitle: "Acoustics, Speech and Signal Processing (ICASSP), 2015 IEEE International Conference on"
    url: http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7178199
    bibtex: ke2015pedestrian.bib

 
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



