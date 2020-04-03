---
layout: default
---

<section id="aboutme">
  <div>
    {% include me.html %}
  </div>
  <div>
    <h3>{{site.title}}</h3>
    <p>{{site.description}}</p>
  </div>
</section>
<section>
  <h2 class="top-h2">Skills</h2>
  <h3>ツール</h3>
  <p>Adobe Illustrator, Photoshop, XD, figma, Unity</p>
  <h3>開発</h3>
  <p>Git, HTML, CSS, Scss, JavaScript, C#, Scratch</p>
  <h3>資格/検定</h3>
  <p>商工会議所認定 2分野 1級カラーコーディネーター「商品色彩」</p>
</section>
<section>
  <h2 class="top-h2">Experience</h2>
  <div class="history">
    {% for elem in site.data.history %}
      {% include historyElm.html %}
    {% endfor %}
  </div>
</section>

<script>
twemoji.parse(document.body);
</script>
