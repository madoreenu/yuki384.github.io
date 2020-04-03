---
layout: default
---
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
