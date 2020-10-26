---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Systems Biology, University of Oxford, 2020
* Masters degree in Mathematics, Durham University, 2015

Work experience
======
* 2019-2020: Assistant programmer
    * European Molecular Biology Laboratory (EMBL) Heidelberg

* 2016-2019: Teaching Assistant
    * Mathematical Institute, University of Oxford
    * Courses:
        - C8.1 Stochastic differential equations
        - B5.1 Stochastic modelling of biological processes
        - B5.5 Further mathematical biology

* 2016-2019: Demonstrator
    * Doctoral Training Center, University of Oxford
    * Courses:
        - Essential maths
        - High performance computing
        - Introduction to C++
        - Computational biology
        - Mathematical biology
        - Introduction to programming

Skills
======
* C++
    - OpenMP
    - MPI
    - Boost
    - Pybind11
    - Chaste
    - C++98, C++11 and C++17 standards
* Python
    - numpy
    - matplotlib
    - scipy
    - pandas
* Container
    - Singularity
    - Docker
* Version control
    - svn
    - git
* Matlab
* Bash
* HTML


Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
