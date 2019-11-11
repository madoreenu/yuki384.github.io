---
layout: default
---
<div class="main">
  <!--<div class="cover">
    <h1>{{site.title}}</h1>
    <h1><a href="" style="color:#ff4d8c">{{site.title}}</a><a href="/profile"><span class="arrow">Click!<img src="/img/arrow.svg" width="60px"></span></a></h1>
  </div>-->
<div id="about">
  <div class="section">
    <img src="/img/logo-white.png" alt="yuki mihashi" height="50px"><br>
    {{site.description}}<br>
    <h3>三橋 優希 (みはし ゆうき)</h3>
    <i class="fas fa-map-marker-alt"></i> 東京<br>
    <i class="fas fa-school"></i> N高等学校 4期生<br>

    絵を描いたり、Webアプリを作ったり、ゲームを作ったりしています。<br>
    yukimihashih@gmail.com
    <h3>どんなことをやっているの？</h3>
    プログラミング道場「CoderDojo」メンター<br>
    プログラミングサークル「ECoder’s」主宰<br>
    未踏ジュニア 2018年度 スーパークリエータ<br>
    セキュリティハッカソン「SecHack365」2期 トレーニー<br>
    <div class="sns">
      <a href="https://twitter.com/YukiMihashi"><i class="fab fa-twitter"></i><p> Twitter</p></a>
      <a href="https://www.instagram.com/yukimihashi/"><i class="fab fa-instagram"></i><p> Instagram</p></a>
      <a href="https://github.com/yuki384"><i class="fab fa-github"></i><p> GitHub</p></a>
      <a href="https://scratch.mit.edu/users/yuki384/"><i class="fas fa-flag"></i><p> Scratch</p></a>
      <a href="http://scratch-yuki.hatenadiary.jp/"><i class="fas fa-pen-nib"></i><p> Blog</p></a>
    </div>
  </div>
</div>
<div id="skill" class="section">
  {% for work in site.data.skill %}
  <div class="work">
    <img src="{{site.url}}/img/icons/{{work.img}}" alt="">
    <h3>{{work.name}}</h3>
  </div>
  {% endfor %}
</div>
<div id="Works" class="section">
  <h2>Works</h2>
  {% for post in site.categories.Works %}
  <a href="{{ site.baseurl }}{{ post.url }}"><div class="project">
    {% if post.thumbnail %}
    <img src="/img/{{ post.thumbnail }}" alt="{{post.title}}" class="thumbnail">
    {%else%}
    {%endif%}
    <div class="prj-dsc">
      <h3>{{post.title}}</h3>
      {% for tag in post.tags %}
      <p class="tag">{{tag}}</p>
      {% endfor %}
    </div>
  </div></a>
  {% endfor %}
</div>
<div id="achievement" class="section">
  <h2>Achievements</h2>
  <ul class="achi">
  {% for achi in site.data.achievement %}
  <li>{{ achi.date }} <span class="achi-title">{{achi.title}}</span> <a href="{{ achi.url }}" target="_blank" class="achievement">{{ achi.event }}</a></li>
  {% endfor %}
  </ul>
</div>
<div id="Presentation" class="section">
  <h2>Presentation Slides</h2>
  {% for prs in site.data.presentation %}
  <a href="{{ prs.url }}" target="_blank" class="prs">
    <div class="prs-img">
      <img src="{{prs.img}}" alt="">
    </div>
    <div class="prs-dsc">
      {{ prs.title }}<br>
      {{ prs.date }}
    </div>
  </a>
  {% endfor %}
</div>
<div id="Blog" class="section">
  <h2>Blog</h2>
  {% for post in site.categories.Blog %}
  <a href="{{ site.baseurl }}{{ post.url }}">
  <article class="post">
    <img src="/img/{{post.thumbnail}}" alt="" class="blog_thumnail">
    <div class="post_text">
      <p>{{post.date | date:"%Y/%m/%d"}}</p><h3>{{post.title}}</h3>
    </div>
  </article>
  </a>
  {% endfor %}
</div>
<div id="Articles" class="section">
  <h2>Articles</h2>
  <ul>
    {% for article in site.data.article %}
      <li><a href="{{article.url}}">{{article.title}}</a></li>
    {% endfor %}
  </ul>
</div>
<div class="section">
  <h2>GitHub Activities</h2>
  <a href="https://github.com/yuki384"><i class="fab fa-github"></i> yuki384<img src="https://grass-graph.moshimo.works/images/yuki384.png" alt="" class="shiba-img"></a>
</div>
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
