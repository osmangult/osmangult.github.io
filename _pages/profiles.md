---
layout: page
permalink: /people/
title: people
description: members of the lab
nav: true
nav_order: 7

pi:
  name: Osman Gültekin, PhD
  role: Principal Investigator
  image: prof_pic.jpg

groups:
  - title: PhD students
    link: /announcements/phd/
    members: []
  - title: MSc students
    link: /announcements/msc/
    members: []
  - title: CE-Star students
    link: /announcements/cestar/
    members: []
---

<div class="clearfix mb-4">
<div class="profile float-right">
<img src="{{ page.pi.image | prepend: '/assets/img/' | relative_url }}" alt="{{ page.pi.name }}" class="img-fluid z-depth-1 rounded">
</div>
<p class="mb-0" style="font-size: 1.25rem;"><strong>{{ page.pi.name }}</strong><br>{{ page.pi.role }}</p>
</div>

{% for group in page.groups %}
<hr>
<h2 class="mt-4 mb-3">{{ group.title }}</h2>
<div class="row">
{% if group.members.size > 0 %}
{% for m in group.members %}
<div class="col-12 col-sm-6 col-md-4 mb-4">
<img src="{{ m.image | prepend: '/assets/img/' | relative_url }}" alt="{{ m.name }}" class="z-depth-1 rounded" style="width:100%; aspect-ratio:3/2; object-fit:cover;">
<p class="mt-2 mb-0"><strong>{{ m.name }}</strong>{% if m.role %}<br>{{ m.role }}{% endif %}</p>
</div>
{% endfor %}
{% else %}
<div class="col-12 col-sm-6 col-md-4 mb-3">
<div class="rounded d-flex align-items-center justify-content-center" style="aspect-ratio:3/2; border:2px dashed var(--global-divider-color); background-color:var(--global-card-bg-color);">
<i class="fa-solid fa-user fa-2x" style="opacity:0.3;"></i>
</div>
</div>
<div class="col-12 col-sm-6 col-md-8 d-flex align-items-center mb-3">
<p class="mb-0">We constantly look for students. Please check the <a href="{{ group.link | relative_url }}">announcements</a>.</p>
</div>
{% endif %}
</div>
{% endfor %}
