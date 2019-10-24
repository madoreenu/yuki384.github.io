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
  <h2>作品</h2>
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
  <h2>発表・登壇</h2>
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
  <h2>最近の記事</h2>
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
  <h2>掲載記事</h2>
  <ul>
    <li><a href="https://sukusuku.tokyo-np.co.jp/life/15192/">＜子どもの平成　下・デジタルネーティブ＞「プログラミング、楽しいから」　社会を変える斬新な発想　2週間でパイロットの飲酒チェックアプリ</a></li>
    <li><a href="https://progate.com/success_interviews/ymitsuhashi">「やりたいことを忘れない」小5でScratchを始めてから未踏ジュニアに認定されるまで</a></li>
    <li><a href="https://kidsna.com/magazine/entertainment-report-18120703-6410">【天才の育て方】三橋優希　～アプリ開発を行う15歳の若きクリエータ</a></li>
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
