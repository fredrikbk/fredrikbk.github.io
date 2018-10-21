---
title: Fredrik Kjolstad
layout: home
---

<table border="0" margin="0">
<td>
<img src="/assets/fred.jpg" width="160">
<!-- ![Fredrik Kjolstad](/assets/fred.jpg){:style="float:left; margin-right:7px; margin-top:7px; width:160px"} -->
</td>
<td valign="top">
PhD Candidate<br/>
Computer Science and Artificial Intelligence Laboratory (CSAIL)<br/>
Department of Electrical Engineering and Computer Science (EECS)<br/>
Massachusetts Institute of Technology<br/>
<a href="mailto:fred@csail.mit.edu">fred@csail.mit.edu</a>
</td>
</table>

I am a PhD candidate at MIT.  I work on the [Taco
compiler](http://tensor-compiler.org) for computing dense and sparse
tensor expressions and the [Simit programming
language](http://simit-lang.org) for computing on graphs and
unstructured meshes with linear and tensor algebra.  My research
interests include compilers, programming models and languages,
performance engineering, parallel computing, and programmer
productivity.


## Publications
<table border="0">
  {% for publication_keyval in site.data.publications %}
    <tr>
      {%- assign publication = publication_keyval[1] -%}
      <td>
        <b>{{ publication.title }}</b><br/>
        {%- for author in publication.authors -%}
          {%- if forloop.last == true and forloop.length > 1 %}
            and
          {%- endif %}
          {%- if author == "kjolstad" %}
            {{ site.data.authors[author].name }}
          {%- else %}
            <a href="{{- site.data.authors[author].site }}">{{ site.data.authors[author].name }}</a>
          {%- endif -%}
          {%- if forloop.last == false and forloop.length > 2 -%}
            ,
          {%- endif %}
        {%- endfor -%}<br/>
        <i>{{ publication.venue }}</i>, {{ publication.month }} {{ publication.year }} <br/>
        {% if publication.award %}
          <i><b>{{ publication.award }}</b></i><br/>
        {%- endif -%}
      </td>
      <td valign="top" width="20">
        {% if publication.pdf %}
          <a href="{{ publication.pdf }}"><img src="/assets/pdf.png" alt="pdf" /></a>
        {% endif %}
        {% if publication.movie %}
          <a href="{{ publication.movie }}"><img src="/assets/movie.png" alt="youtube" /></a>
        {% endif %}
      </td>
    </tr>
{% endfor %}
</table>

<!--
## Press
-->

<!--
## Awards
-->
