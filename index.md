---
layout: default
---
<div class="main">
  <div class="cover">
    <div class="cover-content">
      <img src="{{site.url}}/img/logo.svg" alt="" class="top-img">
      <!--<h1><a href="" style="color:#ff4d8c">{{site.title}}</a><a href="/profile"><span class="arrow">Click!<img src="/img/arrow.svg" width="60px"></span></a></h1>-->
      {% include sns.html %}
    </div>
  </div>
  <section id="aboutme">
    <div>
      {% include me.html %}
    </div>
    <div>
      <h3>{{site.title}}</h3>
      <p>{{site.description}}</p>
      <a href="/about" class="button" style="width: 240px;">私について</a>
    </div>
  </section>
<section id="Works">
  <h2 class="top-h2">Works</h2>
  <div class="flex">
  {% for post in site.categories.Works %}
  <a href="{{ site.baseurl }}{{ post.url }}" class="project">
    {% if post.thumbnail %}
    <img src="{{site.url}}/img/{{post.categories}}/{{ post.thumbnail }}" alt="{{post.title}}" class="thumbnail" loading="lazy">
    {%else%}
    {%endif%}
    <!--<div class="prj-dsc">
      <h3>{{post.title}}</h3>
      <div class="flex">
      {% for tag in post.tags %}
      <p class="tag">{{tag}}</p>
      {% endfor %}
      </div>
    </div>-->
  </a>
  {% endfor %}
  </div>
</section>
<!--<section id="achievement">
  <h2 class="top-h2">ACHIEVEMENT</h2>
  <ul class="achi">
  {% for achi in site.data.achievement %}
  <li>{{ achi.date }} <span class="achi-title">{{achi.title}}</span> <a href="{{ achi.url }}" target="_blank" class="achievement" rel="noopener">{{ achi.event }}</a></li>
  {% endfor %}
  </ul>
</section>-->

<section id="Presentation">
  <h2 class="top-h2">Presentation Slide</h2>
  <div class="flex">
    {% for prs in site.data.presentation %}
    <a href="{{ prs.url }}" target="_blank" class="prs" rel="noopener">
      <div class="prs-img">
        <img src="{{prs.img}}" alt="" loading="lazy">
      </div>
      <div class="prs-dsc">
        {{ prs.title }}<br>
        {{ prs.date }}
      </div>
    </a>
    {% endfor %}
  </div>
  <a href="https://speakerdeck.com/yuki384" class="button">もっと見る</a>
</section>
<section id="Blog">
  <h2 class="top-h2">Blog</h2>
  {% for post in site.data.blog limit:10 %}
  <a href="{{ post.url }}">
  <article class="posts">
    <div class="post-text">
      <h3><span>{{post.date | date:"%Y/%m/%d"}}</span>{{post.title}}</h3>
    </div>
  </article>
  </a>
  {% endfor %}
  <a href="{{site.url}}/blog" class="button">過去の記事を見る</a>
</section>
<section id="Articles">
  <h2 class="top-h2">Articles</h2>
  <ul>
    {% for article in site.data.article %}
      <li><a href="{{article.url}}" target="_blank" rel="noopener">{{article.title}}</a></li>
    {% endfor %}
  </ul>
</section>
<section>
  <h2 class="top-h2">GitHub Activities</h2>
  <a href="https://github.com/yuki384"><i class="fab fa-github"></i> yuki384<img src="https://grass-graph.moshimo.works/images/yuki384.png" alt="" class="shiba-img"></a>
</section>
</div>
<div id="hukidashis">
</div><div class="neko-anime" onclick="neko()"><img src="img/nyan.svg" alt="" class="neko"></div>
<script type="text/javascript">
  function neko(){
    var serihu = [ "ニャン", "ニャアン", "ミャッ", "ニャーン", "ニャッ", "フニャー", "ミャオー", "ミューン", "ニャゴッ"] ;
    var nekochan= document.createElement("div");
    nekochan.className = "hukidashi";
    nekochan.textContent = serihu[ Math.floor( Math.random() * serihu.length ) ];
    document.getElementById('hukidashis').appendChild(nekochan);
    setTimeout("document.querySelector('#hukidashis > div').parentNode.removeChild(document.querySelector('#hukidashis > div'));", 3000);
  }
</script>
