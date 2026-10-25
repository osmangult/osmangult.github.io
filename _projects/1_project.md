---
layout: page
title: Project 1
description: One-line description of the project
# img: assets/img/projects/project1.jpg
# video: assets/video/project1.mp4
importance: 1
category: work
---

{% if page.img %}
<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path=page.img class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Figure caption.
</div>
{% endif %}

{% if page.video %}
<div class="row justify-content-sm-center mt-3">
  <div class="col-sm-10 mt-3 mt-md-0">
    <video controls class="img-fluid rounded z-depth-1" style="width:100%;">
      <source src="{{ page.video | relative_url }}" type="video/mp4">
    </video>
  </div>
</div>
<div class="caption">
  Video caption.
</div>
{% endif %}

Write one paragraph here: the physical problem, the modelling approach, and what the project aims to deliver.

## References

1. O. Gültekin, H. Dal, G. A. Holzapfel (2016). A phase-field approach to model fracture of arterial walls: Theory and finite element analysis. *Computer Methods in Applied Mechanics and Engineering* 312, 542–566. [link](URL)
2. Second reference.
3. Third reference.
4. Fourth reference.
5. Fifth reference.
