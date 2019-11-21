---
layout: default
---
<div class="main">
  <div class="cover">
    <div class="cover-content">
      <img src="{{site.url}}/img/logo.png" alt="" class="top-img">
      <!--<h1><a href="" style="color:#ff4d8c">{{site.title}}</a><a href="/profile"><span class="arrow">Click!<img src="/img/arrow.svg" width="60px"></span></a></h1>-->
      <div class="sns">
        <a href="https://twitter.com/{{site.twitter_username}}"><i class="fab fa-twitter"></i></a>
        <a href="https://www.instagram.com/yukimihashi/"><i class="fab fa-instagram"></i></a>
        <a href="https://github.com/{{site.github_username}}"><i class="fab fa-github"></i></a>
        <a href="https://scratch.mit.edu/users/yuki384/"><i class="fas fa-cat"></i></a>
      </div>
    </div>
  </div>
  <section id="aboutme">
  {% include me.html %}
  <div class="aboutme-text">
    <h3>三橋 優希 (みはし ゆうき)</h3>
    <i class="fas fa-map-marker-alt fa-fw"></i> 東京<br>
    <i class="fas fa-school fa-fw"></i> N高等学校 4期生<br>
    <i class="fas fa-tools fa-fw"></i> イラスト、UIデザイン、Webサイト<br>
    <i class="fas fa-envelope fa-fw"></i> {{site.email}}<br>
    <i class="fas fa-user fa-fw"></i> CoderDojoメンター / ECoder’s主宰 / 未踏ジュニア 2018年度 スーパークリエータ / SecHack365 2期 トレーニー
  </div>
  </section>
<section id="skill">
  {% for work in site.data.skill %}
  <div class="work">
    <img src="{{site.url}}/img/icons/{{work.img}}" alt="">
    <h3>{{work.name}}</h3>
  </div>
  {% endfor %}
</section>
<section id="Works">
  <h2 class="top-h2">WORK</h2>
  <div class="flex">
  {% for post in site.categories.Works %}
  <a href="{{ site.baseurl }}{{ post.url }}" class="project">
    {% if post.thumbnail %}
    <img src="{{site.url}}/img/{{post.categories}}/{{ post.thumbnail }}" alt="{{post.title}}" class="thumbnail" loading="lazy">
    {%else%}
    {%endif%}
    <div class="prj-dsc">
      <h3>{{post.title}}</h3>
      <div class="flex">
      {% for tag in post.tags %}
      <p class="tag">{{tag}}</p>
      {% endfor %}
      </div>
    </div>
  </a>
  {% endfor %}
  </div>
</section>
<section id="achievement">
  <h2 class="top-h2">ACHIEVEMENT</h2>
  <ul class="achi">
  {% for achi in site.data.achievement %}
  <li>{{ achi.date }} <span class="achi-title">{{achi.title}}</span> <a href="{{ achi.url }}" target="_blank" class="achievement" rel="noopener">{{ achi.event }}</a></li>
  {% endfor %}
  </ul>
</section>

<section id="Presentation">
  <h2 class="top-h2">PRESENTATION SLIDE</h2>
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
  <h2 class="top-h2">BLOG</h2>
  {% for post in site.categories.Blog %}
  <a href="{{ site.baseurl }}{{ post.url }}">
  <article class="post">
    <img src="{{site.url}}/img/{{post.categories}}/{{post.thumbnail}}" alt="" class="blog_thumnail" loading="lazy">
    <div class="post_text">
      <p>{{post.date | date:"%Y/%m/%d"}}</p><h3>{{post.title}}</h3>
    </div>
  </article>
  </a>
  {% endfor %}
</section>
<section id="Articles">
  <h2 class="top-h2">ARTICLE</h2>
  <ul>
    {% for article in site.data.article %}
      <li><a href="{{article.url}}" target="_blank" rel="noopener">{{article.title}}</a></li>
    {% endfor %}
  </ul>
</section>
<section>
  <h2 class="top-h2">GITHUB ACTIVITIES</h2>
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
