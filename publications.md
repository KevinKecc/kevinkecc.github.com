---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "W. Ke, J. Chen, J. Jiao, G. Zhao, and Q. Ye"
    title: "SRN: Side-output Residual Network for Object Symmetry Detection in the Wild"
    keywords: "symmetry detection"
    month: "July "
    year: "2017"
    address: "Hawaii, USA"
    booktitle: "IEEE International Conference on Computer Vision and Pattern Recognition (Oral)"
    url: https://arxiv.org/abs/1703.02243
    bibtex: ke2017srn.bib
    code: https://github.com/KevinKecc/SRN
	
  - author: "Q. Ye, T. Zhang, W. Ke, Q. Qiu, J. Chen, G. Sapiro and B. Zhang"
    title: "Self-learning Scene-specific Pedestrian Detectors using a Progressive Latent Model"
    keywords: "self-learning"
    month: "July "
    year: "2017"
    address: "Hawaii, USA"
    booktitle: "IEEE International Conference on Computer Vision and Pattern Recognition"
    url: https://arxiv.org/abs/1611.07544
    bibtex: ye2017sl.bib

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
    booktitle: "IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)"
    url: http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7178199
    bibtex: ke2015pedestrian.bib

  - author: "G. Ch, P. Wei, W. Ke, Q. Ye and J. Jiao"
    title: "Pedestrian Detection with Deep Convolutional Neural Network"
    keywords: "Pedestrian detection"
    year: "2014"
    booktitle: "Asia Conference on Computer Vision Workshop"
    url: https://link.springer.com/chapter/10.1007/978-3-319-16628-5_26
    bibtex: chen2014pedestrain.bib
 
---

# Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).{% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}. {% if pub.address %}{{pub.address}}.
    {% endif %}{{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %} {% if pub.code %}[Code]({{pub.code}}).
    {% endif %} {% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %} {% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}



