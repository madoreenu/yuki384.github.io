---
layout: post
title:  "書籍「カンタン！Scratchできること」"
date:   2019-09-22 12:00:00 +0900
categories: [Works]
tags: Re:VIEW
thumbnail: kitsuneko.jpg
---
## 概要
「こんな事もできるんだ！」ビジュアルプログラミング言語の可能性を知ってもらうために、企画・執筆した書籍です。  

題名: カンタン！Scratchでできること

紹介文: なさそうでなかった、ビジュアルプログラミング言語「Scratch」のガチ勢本が登場！
「Scratchでこんなこともできるの！？」と楽しんでもらうため、Scratcher 5人がそれぞれ好きなテーマで書き上げた、Scratchの技術書です。
言語の自作や、物理エンジン実装、ドット絵エディタやフォントづくりなど、盛り沢山な内容となっております！
Scratchやビジュアルプログラミングに興味がある方、Scratcherの将来について知りたい方はぜひご覧ください。

### 技術
 - Re:VIEW
 - Adobe Illustrator
 - CSS

### 制作時間
2019.7~2019.9  
2ヶ月

### 公開情報
9/22に開催された技術書典7にて販売しました。紙の書籍はありがたいことに一旦完売しました。2020年2月現在は紙とPDFをセットで[BOOTHで販売](https://yuki384.booth.pm/items/1728327)しております。

## 内容について
Scratchは「簡単」なものしか作れない、と思われることがあります。しかし、実は複雑なプログラムやスマートフォンゲームのようなクオリティの作品が作れます。そこで、 **「実はこんなものも作れます！」と伝えたい** 、「感嘆」してもらいたい、という思いから本書を書くに至りました。

内容は以下のとおりです。
- 自作プログラミング言語
- 物理演算エンジン
- フォント
- ドット絵エディタ
- 3D描画

私は「SVG出力のできるドット絵エディタを作ろう」という内容の記事を書きました。

## デザインについて
表紙、本文ともにデザインを担当しました。表紙はAdobe Illustrator で制作しました。Scratchの猫を彷彿とさせる色使いとポーズ、そして猫耳をあしらったキャラクターです。

本文のデザインはCSSで組みました。inDesignよりCSSに慣れているため、限られた時間のことも考えてCSSで作ることにしました。

一つ学んだのが、入稿形式に沿っているかのチェックをしっかりすることが大事、ということです。普段モニターで見るデザイン制作をしているので、印刷物のデザインでは初歩的なミスをしてしまいました。

## 技術的なこと
1. Markdownで原稿を書きます。
1. 完成後、Re:VIEW形式に変換します。(ここからGitHubで管理します)
1. 校正して、プルリクエストを出します。
1. 文中の画像をPhotoshopで編集して、可読性をあげます。
1. CSSで見出し等のデザインを作ります。
1. 出力したepubファイルをcalibreというソフトでpdfに変換します。
1. Adobe Acrobatで微調整をし、表紙をつけてページ数調整をして完成です。

## 企画〜頒布まで

### きっかけ
<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">そろそろScratchガチ勢の人が書いた本があっても良いかもしれない。100%ペンもペンテキもクラウドリストも解説した本はまだない。それどころか、コミュに出入りしていない人はその存在すら知らない。</p>&mdash; アベ先生 (CV: 阿部和広) (@abee2) <a href="https://twitter.com/abee2/status/1142024865009950721?ref_src=twsrc%5Etfw">June 21, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
以前からScratchの技術本を書きたいと思っていましたが、このツイートをみてますます **「書きたい！」** という気持ちが強くなりました。ちょうど同じ頃に、[技術書典7](https://techbookfest.org/event/tbf07)という技術書の同人誌即売会の、サークル出展募集がありました。締切や目標があると企画倒れしにくいので、技術書典での頒布を目指し作ることにしました。「やりたいなあ」「読みたいなあ」ではなく、「やります」になった瞬間です。

### 企画
7月中旬からプロジェクトを進めていきました。

まずはじめに、仲が良く、一緒に本を作ったら楽しそうなScratcherに声をかけ、進めていくことにしました。全員が集まったらそれぞれの意見を聞いてまとめながら、本の方向性と内容を決めます。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/%E6%8A%80%E8%A1%93%E6%9B%B8%E5%85%B87?src=hash&amp;ref_src=twsrc%5Etfw">#技術書典7</a> に出すScratch本の内容案がたくさん出てきました…！楽しみ…！<a href="https://twitter.com/hashtag/Scratch?src=hash&amp;ref_src=twsrc%5Etfw">#Scratch</a> <a href="https://t.co/QYPYKTKfcn">pic.twitter.com/QYPYKTKfcn</a></p>&mdash; 三橋優希/Yuki Mihashi (@YukiMihashi) <a href="https://twitter.com/YukiMihashi/status/1149898736329379841?ref_src=twsrc%5Etfw">July 13, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 執筆と編集
入稿の締切や作業にかかる時間を計算し、それぞれの執筆者と連絡をとりながら進めていきました。当初はGitHubにレポジトリを作ったので、それぞれが書くたびにコミットするという流れにしようと思っていました。うまく動けば私も楽だったのですが、執筆者の方々はGitを使うのが得意ではなかったのか、機能しなかったので私がほぼ作業していました。

また、コンセプトがうまく伝わっていなかった点は反省です。

### イベント当日
<blockquote class="twitter-tweet"><p lang="ja" dir="ltr"><a href="https://twitter.com/hashtag/%E6%8A%80%E8%A1%93%E6%9B%B8%E5%85%B87?src=hash&amp;ref_src=twsrc%5Etfw">#技術書典7</a> <br>き04Dでお待ちしております！ <a href="https://t.co/RAnugdfAfy">pic.twitter.com/RAnugdfAfy</a></p>&mdash; 三橋優希/Yuki Mihashi (@YukiMihashi) <a href="https://twitter.com/YukiMihashi/status/1175624369172709377?ref_src=twsrc%5Etfw">September 22, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

さて、イベント当日は200部を用意しました。合計で88冊を買っていただいて、残りは自宅へ宅急便で発送しました。

### その後
帰宅後はBOOTHで販売し、10月25日に無事完売しました！ありがとうございますm(_ \_)m

お金に関しては、全て私が負担しており執筆者の方がリスクを追わないような仕組みにしました。が、計画を少し間違えてしまったため赤字になっています。ここは振り返って次回に活かします。

## 感想
もちろん、簡単なことだけではありませんでした。締め切りに間に合わない方もいて、少し困ってしまいました。次は、締め切りに余裕を持って設定した上で、スムーズに執筆を進められるようサポートしていきたいです。 **チームとのコミュニケーションの大切さ** を学びました。

初めて本を作れて、楽しかったです。読んでいただいて、意見をもらったときはすごく嬉しかったです。ここまで読んでいただき、ありがとうございました。

**[ご購入はこちらから](https://yuki384.booth.pm/items/1728327)**
