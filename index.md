---
layout: default
---
<div class="main">
  <div class="cover">
    <div class="cover-content">
      <img src="{{site.url}}/img/logo.png" alt="" class="top-img">
      <!--<h1><a href="" style="color:#ff4d8c">{{site.title}}</a><a href="/profile"><span class="arrow">Click!<img src="/img/arrow.svg" width="60px"></span></a></h1>-->
      <div class="sns">
        <a href="https://twitter.com/YukiMihashi"><i class="fab fa-twitter"></i></a>
        <a href="https://www.instagram.com/yukimihashi/"><i class="fab fa-instagram"></i></a>
        <a href="https://github.com/yuki384"><i class="fab fa-github"></i></a>
        <a href="https://scratch.mit.edu/users/yuki384/"><i class="fas fa-cat"></i></a>
      </div>
    </div>
  </div>
  {% include me.html %}
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
</section>
<section id="achievement">
  <h2 class="top-h2">ACHIEVEMENT</h2>
  <ul class="achi">
  {% for achi in site.data.achievement %}
  <li>{{ achi.date }} <span class="achi-title">{{achi.title}}</span> <a href="{{ achi.url }}" target="_blank" class="achievement">{{ achi.event }}</a></li>
  {% endfor %}
  </ul>
</section>

<section id="Presentation">
  <h2 class="top-h2">PRESENTATION SLIDE</h2>
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
</section>
<section id="Blog">
  <h2 class="top-h2">BLOG</h2>
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
</section>
<section id="Articles">
  <h2 class="top-h2">ARTICLE</h2>
  <ul>
    {% for article in site.data.article %}
      <li><a href="{{article.url}}">{{article.title}}</a></li>
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
