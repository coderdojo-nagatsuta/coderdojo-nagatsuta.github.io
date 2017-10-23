---
permalink: /
layout: splash
title: "CoderDojo長津田へようこそ！"
author_profile: false
header:
  overlay_image: /assets/images/topimage.jpg
  overlay_filter: "0.5"
  caption: "CoderDojo長津田"
  cta_label: "次回開催の予約をする"
  cta_url: "https://coderdojo-nagatsuta.connpass.com/"
excerpt: "CoderDojoは子どものためのプログラミング道場です"
intro:
  - excerpt: "次回開催は2017年11月26日（日）です！"
feature_row:
  - image_path: /assets/images/announce-front.jpg
    alt: "活動内容を知りたい！"
    title: "活動内容を知りたい！"
    excerpt: "活動内容や過去の開催内容についてはこちらから"
    btn_label: "活動内容"
    btn_class: "btn--success"
    url: "/about/"
  - image_path: /assets/images/midori-front.jpg
    alt: "CoderDojo長津田に参加したい！"
    title: "参加したい！"
    excerpt: "CoderDojo長津田に参加する方法、活動場所についてはこちらから"
    btn_label: "参加方法、活動場所"
    btn_class: "btn--success"
    url: "/access/"
  - image_path: /assets/images/room-front.jpg
    alt: "お問い合わせ"
    title: "お問い合わせ"
    excerpt: "お問い合わせ、ご支援についてはこちらから"
    btn_label: "お問い合わせ、ご支援"
    btn_class: "btn--success"
    url: "/access/"
gallery:
  - url: /assets/images/gallery/1.jpg
    image_path: /assets/images/gallery/1.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/2.jpg
    image_path: /assets/images/gallery/2.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/3.jpg
    image_path: /assets/images/gallery/3.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/4.jpg
    image_path: /assets/images/gallery/4.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/5.jpg
    image_path: /assets/images/gallery/5.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/6.jpg
    image_path: /assets/images/gallery/6.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/7.jpg
    image_path: /assets/images/gallery/7.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/8.jpg
    image_path: /assets/images/gallery/8.jpg
    alt: ""
    title: ""
  - url: /assets/images/gallery/9.jpg
    image_path: /assets/images/gallery/9.jpg
    alt: ""
    title: ""
---

{% include feature_row id="intro" type="center" %}{: .notice--success}

{% include feature_row %}

## CoderDojoってなに？
CoderDojo は7〜17歳の子どもを対象にしたプログラミング道場です。2011年にアイルランドで始まり、世界では70カ国・1,200の道場、日本では全国に100以上の道場があります。

- [CoderDojo公式ホームページ（英語）](https://coderdojo.com)
- [CoderDojo Japan（日本語）](https://coderdojo.jp)

## CoderDojo長津田 （Nagatsuta）

2017年4月より横浜市緑区長津田にて道場を開始しました！

プログラミングでモノを作る楽しさを体験できる場所にしたいと考えています。新たな技術、アイデアの出会い、きっかけ作り、友だち作りができる環境を作って行きます。

初心者、経験者は問わず、自由に出入りできるサークルです。

## 写真ギャラリー

{% include gallery caption="" %}

## Facebook, Twitter

Facebook、Twitterで随時情報を発信しています。ぜひフォローしてください！

[CoderDojo 長津田 Facebook](https://www.facebook.com/coderdojo.nagatsuta/){: .btn .btn--inverse}

[CoderDojo 長津田 Twitter](https://twitter.com/CoderDojoNGTD){: .btn .btn--inverse}

## 過去の開催レポート

<div class="grid__wrapper">
  {% for post in site.reports %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
