---
layout: default
---
<div class="post-head">
{% include header.html %}
<h2></h2>
<h1>About Me</h1>
</div>
<section id="aboutme">
  <div>
    {% include me.html %}
  </div>
  <div>
    <h3>{{site.title}}</h3>
    {% include sns.html %}
    <p>{{site.description}}</p>
  </div>
</section>
<section>
  <h2 class="top-h2">Skills</h2>
  <h3>開発</h3>
  {% include skill-list.html category="code"%}
  <h3>ツール</h3>
  {% include skill-list.html category="tool"%}
  <h3>資格/検定</h3>
  {% include skill-list.html category="certification"%}
</section>
<section>
  <h2 class="top-h2">Experiences</h2>
  <div class="history">
    {% for elem in site.data.history %}
      {% include historyElm.html %}
    {% endfor %}
  </div>
</section>

<script>
twemoji.parse(document.body);
</script>
