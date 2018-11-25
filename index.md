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
PhD Candidate<br/>
Computer Science and Artificial Intelligence Laboratory<br/>
Department of Electrical Engineering and Computer Science<br/>
Massachusetts Institute of Technology<br/>
<a href="mailto:fred@csail.mit.edu">fred@csail.mit.edu</a><br/>
<a href="/assets/kjolstad-cv.pdf">Curriculum Vitae</a>
</td>
</table>

I am a PhD candidate at MIT.  I work on the [taco
compiler](http://tensor-compiler.org) for computing sparse
tensor expressions and the [Simit programming
language](http://simit-lang.org) for computing on graphs and
unstructured meshes with linear and tensor algebra.  My research
interests include compilers, programming models and languages,
performance engineering, parallel computing, and programmer
productivity.

<h2 class="tableheading">News</h2>

I am co-organizing an [Invited Workshop on Compiler Techniques for
Sparse Tensor
Algebra](http://groups.csail.mit.edu/commit/2019tensorworkshop/) that
will tentatively bring together researchers from ten universities, six
companies, and two national labs to discuss individual approaches, how
they relate, and how ideas can be combined.

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

