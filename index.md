---
layout: default
---
<div class="main">
  <div class="cover">
    <h1><a href="/profile/" style="color:#ff4d8c">{{site.title}}</a><a href="/profile"><span class="arrow">Click!<img src="/img/arrow.svg" width="60px"></span></a></h1>
  </div>
<div id="about">
  <div class="section">
    <img src="/img/logo-white.png" alt="yuki mihashi" height="50px"><br>
    {{site.description}}<br>
    <a href="/profile/" style="color:#fff;">プロフィール</a>
    <div class="sns">
      <a href="https://twitter.com/YukiMihashi"><i class="fab fa-twitter"></i><p> Twitter</p></a>
      <a href="https://www.instagram.com/yukimihashi/"><i class="fab fa-instagram"></i><p> Instagram</p></a>
      <a href="https://github.com/yuki384"><i class="fab fa-github"></i><p> GitHub</p></a>
      <a href="https://scratch.mit.edu/users/yuki384/"><i class="fas fa-flag"></i><p> Scratch</p></a>
      <a href="http://scratch-yuki.hatenadiary.jp/"><i class="fas fa-pen-nib"></i><p> Blog</p></a>
    </div>
  </div>
</div>
<div id="Works" class="section">
  <h2>Works</h2>
  {% for post in site.categories.Works %}
  <a href="{{ site.baseurl }}{{ post.url }}"><div class="project">
    {% if post.thumbnail %}
    <img src="/img/{{ post.thumbnail }}" alt="{{post.title}}" class="thumbnail">
    {%else%}
    {%endif%}
    <h3>{{post.title}}</h3>
    {% for tag in post.tags %}
    <p class="tag">{{tag}}</p>
    {% endfor %}
  </div></a>
  {% endfor %}
</div>
<div id="Presentation" class="section">
  <h2>Presentation slide</h2>
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
  <h2>Article</h2>
  <ul>
    {% for article in site.data.article %}
      <li><a href="{{article.url}}">{{article.title}}</a></li>
    {% endfor %}
  </ul>
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
