---
title: Fredrik Kjolstad
layout: home
---

<table border="0" cellpadding="0">
<td valign="top" style="min-width:140px;">
<img src="/assets/fred.jpg" width="160">
<!-- ![Fredrik Kjolstad](/assets/fred.jpg){:style="float:left; margin-right:7px; margin-top:7px; width:160px"} -->
</td>
<td valign="top">
Assistant Professor<br/>
Department of Computer Science<br/>
Stanford University<br/>
Office: 440 Gates
<a href="mailto:kjolstad@stanford.edu">kjolstad@cs.stanford.edu</a><br/>
<!-- <a href="/assets/kjolstad-cv.pdf">Curriculum Vitae</a> -->
</td>
</table>


I aim to make it easy to program sparse computing applications that can run
everywhere with end-to-end performance that matches or exceeds the best
hand-optimized codes.  A sparse application computes on a system where most
parts do not interact—they are sparsely interconnected. Examples include sparse
matrices, meshes, and graphical arrangements used to simulate the dynamics of
robots, optimize the flow of traffic, compute the rank of web pages, estimate
the similarity of genome loci, or train sparse deep neural networks.  Sparse
computing is ubiquitous and will become increasingly important with the growth
of robotic and autonomous vehicle applications, data analytics, and machine
learning.

I have developed the [taco compiler](http://tensor-compiler.org) for computing
sparse tensor expressions and the [Simit programming
language](http://simit-lang.org) for computing on sparse systems.  My broad
research interests include compilers, programming models and languages,
parallel computing, software engineering, and performance engineering.

My thesis on <a href="/publications/kjolstad-thesis.pdf">Sparse
Tensor Algebra Compilation</a> is the best place to start reading
about the ideas behind the tensor algebra compiler (taco) and
sparse iteration theory.

<h2 class="tableheading">PhD Students</h2>

<table border="0">
  <tr>
      <td>Olivia Hsu (with Kunle Olukotun)<\td>
  </tr>
  <tr>
      <td>Scott Kovach<\td>
  </tr>
  <tr>
      <td>Amalee Wilson (with Clark Barrett)<\td>
  </tr>
  <tr>
      <td>Haoran Xu<\td>
  </tr>
  <tr>
      <td>Rohan Yadav (with Alex Aiken)<\td>
  </tr>
</table>


<h2 class="tableheading">Publications</h2>

<table border="0">
  {% for pub_keyval in site.data.publications %}
    <tr>
      {%- assign pub = pub_keyval[1] -%}
      <td>
        <b><a href="{{pub_keyval[0]}}.html" style="color: #464646">{{ pub.title }}</a></b><br/>
        {%- for author in pub.authors -%}
          {%- if forloop.last == true and forloop.length > 1 %}
            and
          {%- endif %}
          {%- if author == "kjolstad" %}
            <font color="#000000">{{ site.data.authors[author].name }}</font>
          {%- else %}
            <a href="{{- site.data.authors[author].site -}}" style="color: #464646">{{ site.data.authors[author].name }}</a>
          {%- endif -%}
          {%- if forloop.last == false and forloop.length > 2 -%}
            ,
          {%- endif %}
        {%- endfor -%}<br/>
        <i>{{ pub.venue }}
        {%- if pub.venuenote %}
        ({{ pub.venuenote }})
        {%- endif -%}
        {%- if pub.volume -%}
        , Volume {{ pub.volume }}
        {%- endif -%}
        {%- if pub.issue -%}
        , Issue {{ pub.issue }}
        {%- endif -%}
        </i>, {{ pub.month }} {{ pub.year }}<br/>
        {%- if pub.award -%}
          <i><b>{{ pub.award }}</b></i><br/>
        {%- endif -%}
      </td>
      <td valign="top" width="20">
        {% if pub.pdf %}
          <a href="{{ pub.pdf }}"><img src="/assets/pdf.png" alt="pdf" /></a>
        {% endif %}
        {% if pub.movie %}
          <a href="{{ pub.movie }}"><img src="/assets/movie.png" alt="youtube" /></a>
        {% endif %}
      </td>
    </tr>
{% endfor %}
</table>


<h2 class="tableheading">Press</h2>

<table border="0">
{%- for press_keyval in site.data.press %}
  {%- assign press= press_keyval[1] -%}
  <tr>
  <td> 
    <b><a href="{{press.url}}">{{press.title}}</a></b><br/>{{press.venue}}
  </td>
  </tr>
{% endfor %}
</table>

