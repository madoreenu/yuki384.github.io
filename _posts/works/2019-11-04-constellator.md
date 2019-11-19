---
layout: post
title:  "CONSTELLATOR!"
date:   2019-10-20 12:00:00 +0900
categories: [Works]
tags: フロントエンド Webデザイン
thumbnail: constellator.jpg
---
## 概要
NASA Space Apps Challenge Kushimotoというハッカソンで、「星座をつくり共有するサービス」をチームで開発しました。

### 技術(私が使用した部分)
 - HTML
 - CSS
 - jQuery

### 制作時間
1日

### 公開情報
[https://team-mihashi.github.io/CONSTELLATOR/](https://team-mihashi.github.io/CONSTELLATOR/)

### チームメンバー
- [Yuki Mihashi](https://yuki384.github.io/)
- [Yui Nishimura](https://github.com/nisshi79)
- [Tomohiro Nozaki](https://github.com/nztm)
- [Tenma Kamatani](https://github.com/tenmakamatani)
- [Koichi Murama](https://twitter.com/koichi72love)

## 使い方
「作る」「見る」という2つの機能があります。

作る: 星をクリックしていくことで星座を作れます。  
見る: 他の人が作った星座と、既存の星座を見ることができます。既存の星座と比較でき、学ぶことができます。

## なぜ作ったのか
NASA Space Apps Challenge Kushimoto というハッカソンイベントは「NASAのデータを使用したプロジェクトを作ろう」というコンセプトのものです。

さて、私達は宇宙に特別に興味を持っているわけではなく、専門的な知識はありません。しかし、幼い頃、**星を見て様々な想像** をしていました。「あれがオリオン座かなあ」「あれはスマホ座かもしれない」のように。

私達は、このように星に興味を持つことが、**宇宙に興味を持つきっかけ** につながると考えました。そこで、私達のように知識がない人々でも星に興味を持てるようなサービスを作りました。

## 目的
目的は、子どもたちに星に興味を持ってもらうことです。そこで **星座に着目** しました。星の数は無数にあり、いくらでも新しい星座を作り出せるのではないでしょうか。

私たちは **自分の星座を作れる** ことで、星に興味をもつきっかけになると考えました。

さらに作った星座を **誰でも閲覧できる** ことで、刺激になり、より使ってもらえるのではないかと考えました。類似のものでは他の人が作ったものを見ることができないので、この作品を作ろうと決めました。

## 実際に使ってもらって
ハッカソンの参加者に使ってもらったところ、面白い成り立ちの星座や駄洒落が含まれた星座を見ることができました。

「既存の星座と重ねて表示できたらどうだろう？」という意見をいただいたので、参考にし実装しました。

## 少し技術的な話
NASAの提供している星の画像を使用しています。

マウスがクリックされた時にクリックされた場所付近の色を取得し、一定値以上の明るさのピクセルがあれば星と判定し、座標を保存します。保存された座標をもとに描画し、投稿された時点で座標の情報をサーバに保存します。

## 今後の展望
- つないだ星の情報を表示する
- 幼児〜児童に簡単に使ってもらえるように、インターフェースの単純化
- AR表示
- SNS投稿

## 感想
チーム開発には慣れていなかったのですが、それぞれの得意分野を活かしながら作品を作り上げることができ楽しかったです。最高賞であるグローバル賞をいただくことができ、嬉しいです。

## 発表資料
<script async class="speakerdeck-embed" data-id="5a93f67476cc406fb2e08d1008480221" data-ratio="1.33333333333333" src="//speakerdeck.com/assets/embed.js"></script>

## 関連するURL
[N高生を含むチーム「NASA Space Apps Challenge Kushimoto」で優勝](https://nnn.ed.jp/news/blog/archives/8941.html)
