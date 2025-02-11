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
Office: CoDa 456
<a href="mailto:kjolstad@stanford.edu">kjolstad@stanford.edu</a><br/>
<a href="kjolstad-cv.pdf">CV</a>
</td>
</table>

My group aims to make it easier to develop applications that are portable across different data representations and different machines. This work includes developing languages on collections of data (tensors, relations, graphs, and objects embedded in space) and developing meta-compilers that generates compilers for different languages and machines.

In particular, we have developed compilers for sparse tensor algebra and other array operations on sparse data, which lets us build tensor algebra and array libraries and languages that are polymorphic over different data structures. This work includes the TACO compiler, the Simit Programming Language, the Distal and Legate Sparse systems, the Sparse Abstract Machine, the Etch Indexed Stream compiler, the RECUMA recurrence compiler, and the Scorch sparse extension to the PyTorch library. We have also developed the Copy-and-Patch compiler technology that makes it possible to derive from LLVM lightning fast online compilers for different ISAs, which have no runtime dependencies on LLVM.

My thesis on <a href="/publications/kjolstad-thesis.pdf">Sparse
Tensor Algebra Compilation</a> is a good place to start reading
about the ideas behind the tensor algebra compiler (taco) and
sparse iteration model. 

<h2 class="tableheading">PhD Students</h2>

<ul>
  <li><a href="https://cs.stanford.edu/people/dongj/">James Dong</a></li>
  <li><a href="https://www.linkedin.com/in/trevorgale/">Trevor Gale</a> (with Matei Zaharia)</li>
  <li><a href="https://cgyurgyik.github.io">Christophe Gyurgyik</a></li>
  <li><a href="https://weiya711.github.io/">Olivia Hsu</a> (with Kunle Olukotun)</li>
  <li><a href="https://cutfree.net/">Scott Kovach</a></li>
  <li><a href="https://www.linkedin.com/in/lrubens">Rubens Lacouture</a> (with Kunle Olukotun)</li>
  <li><a href="https://rootjalex.github.io/">Alexander Root</a></li>
  <li><a href="https://shivsundram.github.io/">Shiv Sundram</a></li>
  <li><a href="https://sillycross.github.io/about/">Haoran Xu</a></li>
  <li><a href="https://rohany.github.io/">Rohan Yadav</a> (with Alex Aiken)</li>
  <li><a href="https://bobbyy.org/">Bobby Yan</a></li>
</ul>


<h2 class="tableheading">Publications</h2>

<table border="0">
  {% for pub_keyval in site.data.publications %}
    <tr>
      {%- assign pub = pub_keyval[1] -%}
        {%- if pub.venue != "arXiv" %}
        <td>
          <b><a href="{{pub_keyval[0]}}.html" style="color: #464646">{{ pub.title }}</a></b><br/>
          {%- for author in pub.authors -%}
            {%- if forloop.last == true and forloop.length > 1 %}
              and
            {%- endif %}
            {%- if author == "kjolstad" %}
              <font color="#000000">{{ site.data.authors[author].name }}</font>
            {%- else %}
              {%- if site.data.authors[author].site %}
                <a href="{{- site.data.authors[author].site -}}" style="color: #464646">{{ site.data.authors[author].name }}</a>
              {%- else %}
                <font color="#464646">{{ site.data.authors[author].name }}</font>
              {%- endif -%}
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
          {% assign cur_year = "now" | date: "%Y" | plus: 0 %}
          {% assign pub_year = pub.year | plus: 0 %}
          {% assign cur_month = "now" | date: "%m" | plus: 0%}
          {% assign pub_month = pub.month | plus: 0%}
          {%- if pub.month == "January" -%}
            {% assign pub_month = 1 %}
          {%- elsif pub.month == "February" -%}
            {% assign pub_month = 2 %}
          {%- elsif pub.month == "March" -%}
            {% assign pub_month = 3 %}
          {%- elsif pub.month == "April" -%}
            {% assign pub_month = 4 %}
          {%- elsif pub.month == "May" -%}
            {% assign pub_month = 5 %}
          {%- elsif pub.month == "June" -%}
            {% assign pub_month = 6 %}
          {%- elsif pub.month == "July" -%}
            {% assign pub_month = 7 %}
          {%- elsif pub.month == "August" -%}
            {% assign pub_month = 8 %}
          {%- elsif pub.month == "September" -%}
            {% assign pub_month = 9 %}
          {%- elsif pub.month == "October" -%}
            {% assign pub_month = 10 %}
          {%- elsif pub.month == "November" -%}
            {% assign pub_month = 11 %}
          {%- elsif pub.month == "December" -%}
            {% assign pub_month = 12 %}
          {%- endif -%}
          {%- if cur_year < pub_year -%}
          (to appear)
          {%- elsif cur_year == pub_year and cur_month < pub_month -%}
          (to appear)
          {%- endif -%}
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
      {% endif %}
    </tr>
{% endfor %}
</table>
