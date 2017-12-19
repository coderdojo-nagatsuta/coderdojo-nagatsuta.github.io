---
categories: reports
title: "CoderDojo長津田2017年のまとめ (CoderDojo Advent Calendar 2017)"
header:
  overlay_image: /assets/images/posts/8/1.jpg
  overlay_filter: "0.5"
  teaser: /assets/images/posts/8/1.jpg
excerpt: "CoderDojo長津田2017年のまとめ記事です。CoderDojo Advent Calendar 2017に登録しています"
---

この記事は[CoderDojo Advent Calendar 2017](https://adventar.org/calendars/2184)の19日の記事です。

せっかくなので、CoderDojo長津田の紹介と8ヶ月ほどやってきたことの簡単なまとめをします。

## 自己紹介

CoderDojo長津田のチャンピオンをやっている植田です。普段はフリーランスとしてiOS, Androidのアプリ制作やサーバサイドの開発をやっています。

長津田は横浜市のなかの山側にあり、東急田園都市線と横浜線の交わるところに位置していまして、駅周りは住宅地ですが、少し行くと田園風景が広がるようなそんな場所です。

<iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d122251.79079909314!2d139.55003529317705!3d35.504638198928454!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6018f850ed7f1c8b%3A0x5e5675d0d7f58ec5!2z6ZW35rSl55Sw6aeF!5e0!3m2!1sja!2sjp!4v1513641557616" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>

都心からは少し離れてます。

![image-center](/assets/images/midori-front.jpg){: .align-center}

駅近くの横浜市緑区の公民館（みどりアートパーク）で月1度開催しています。

## 先日第8回CoderDojo長津田開催しました

![image-center](/assets/images/posts/8/9.jpg){: .align-center}

CoderDojo長津田は今年(2017年)の5月から第1回目を開始しまして、先日8回目を終えました。

![image-center](/assets/images/posts/8/13.jpg){: .align-center}

全くの初心者から、Scratchですぐにゲームを1本作ってしまうような上級者まで幅広いスキルのニンジャが集まっています。最近は特にMinecraftでのプログラミングを楽しむニンジャも増えてきました。

## CoderDojoをはじめたきっかけ

ちょうど1年前くらいに小学2年の長男と一緒にMinecraftにはまり、何か調べ物をしているうちにMinecraft内でプログラミングが出来ることを知りました。

長男がゲームやYoutubeで動画ばかり見てるくらいなら、マイクラ内でプログラミングでもやったほうが、色々勉強になることも多いんじゃないか！と考えたことがきっかけで、子ども向けのプログラミングについて調べまくった結果、CoderDojoにいきつき、CoderDojo横浜を見学させていただいて、これはもうやるしかない！と走りはじめたのがきっかけです。

（ちなみに長男はMinecraftのプログラミングにはあまり興味がないようです。。）

子ども向けのプログラミングの効用については、賛否あるところではありますが、趣味としてまた経験として幼少期に触れたことは、すごく影響が大きいと考えます。

個人的にも幼少期にパソコンを触ったことがあってそれがすごく楽しかったので、今の職業に影響があったと感じます。そんな楽しい体験、経験を提供出来る場所を作れたら良いなと思っています。

## 数値で見るCoderDojo長津田

<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>

<script type="text/javascript">
  google.charts.load('current', {packages: ['corechart', 'bar', 'line']});
  google.charts.setOnLoadCallback(drawNinja);
  google.charts.setOnLoadCallback(drawAge);
  google.charts.setOnLoadCallback(drawRepeater);
  google.charts.setOnLoadCallback(drawMentor);

  function drawNinja() {
    var data = new google.visualization.DataTable();
    data.addColumn('string', '開催回');
    data.addColumn('number', '男子');
    data.addColumn('number', '女子');

    data.addRows([
      ["1", 11, 4],
      ["2", 5, 3],
      ["3", 14, 2],
      ["4", 8, 1],
      ["5", 11, 1],
      ["6", 11, 0],
      ["7", 11, 1],
      ["8", 9, 0],
    ]);

    var options = {
      title: '開催回ごとのニンジャ数',
      height: 300,
      isStacked: true,
      hAxis: {
        title: '開催回',
        viewWindow: {
          min: [7, 30, 0],
          max: [17, 30, 0]
        }
      },
      vAxis: {
        title: '人数'
      }
    };

    var chart = new google.visualization.ColumnChart(document.getElementById('chart_div_ninja'));
    chart.draw(data, options);
  }

  function drawAge() {
    var data = google.visualization.arrayToDataTable([
      ['年齢', '人数'],
      ['5歳以下', 1],
      ['6歳',  4],
      ['7歳',  12],
      ['8歳',  25],
      ['9歳',  15],
      ['10歳',  9],
      ['11歳',  11],
      ['12歳',  4],
      ['13歳',  1],
      ['14歳',  1],
      ['15歳',  3],
      ['不明',  5],
    ]);

    var options = {
      title: 'ニンジャの年齢比率',
      height: 400,
    };

    var chart = new google.visualization.PieChart(document.getElementById('chart_div_age'));
    chart.draw(data, options);
  }

  function drawRepeater() {
    var data = new google.visualization.DataTable();
    data.addColumn('string', '開催回');
    data.addColumn('number', 'リピーター率');
    data.addColumn('number', 'リピート率');

    data.addRows([
      ["1", 0, 0],
      ["2", 87.5, 13.46],
      ["3", 12.5, 3.85],
      ["4", 55.56, 9.62],
      ["5", 50, 11.54],
      ["6", 63.64, 13.46],
      ["7", 66.67, 15.38],
      ["8", 66.67, 11.54],
    ]);

    var options = {
      height: 300,
      hAxis: {
        title: '開催回'
      },
      vAxis: {
        title: '%'
      },
      series: {
        1: {curveType: 'function'}
      }
    };

    var chart = new google.visualization.LineChart(document.getElementById('chart_div_repeater'));
    chart.draw(data, options);
  }

  function drawMentor() {
    var data = new google.visualization.DataTable();
    data.addColumn('string', '開催回');
    data.addColumn('number', 'メンター');

    data.addRows([
      ["1", 4],
      ["2", 5],
      ["3", 2],
      ["4", 3],
      ["5", 2],
      ["6", 3],
      ["7", 2],
      ["8", 3],
    ]);

    var options = {
      title: '開催回ごとのメンター数',
      height: 300,
      isStacked: true,
      hAxis: {
        title: '開催回',
      },
      vAxis: {
        title: '人数'
      }
    };

    var chart = new google.visualization.ColumnChart(document.getElementById('chart_div_mentor'));
    chart.draw(data, options);
  }

</script>

### ニンジャ数

<div id="chart_div_ninja"></div>

8回で延べ92人のニンジャに来ていただきました。
各回平均すると約11人ほどになります。

### ニンジャの年齢比率

<div id="chart_div_age"></div>

だいたい小学生低学年が半分ほどで、あと小学生高学年が1/4くらい、その他と続きます。

### リピート率

<div id="chart_div_repeater"></div>

リピーター率はリピーター数を各回のニンジャ数で割ったもの。
リピート率はリピーター数を今までのニンジャのユニーク数で割ったものです。

母数が少なくて1人変わるだけで結構変わるので微妙なところではありますが、だいたい各回6割くらいはリピーターが来ていただいている状況です。

### メンター数

<div id="chart_div_mentor"></div>

メンターはいつも少なくて、、1メンターあたりだいたい4人くらい見ているような計算になっています。

## よかったこと

### 話のネタになる！

本業がフリーランスなので、はじめて会った方やSNSで繋がった方などと、子ども向けのプログラミングについての話のネタになるのは本当にありがたいです。

### Minecraft、Scratchけっこう楽しい

毎月、Scratchの課題を考えたり、Minecraftでみんなの前でみせるネタを考えたりするんですが、それが結構楽しいです。特にScratchは作っているたびにこんなことも簡単にできるのかと、学びながらつくってます。仕事と違ってしょぼいコードを書いても指摘されることはないですしね（笑）

## 課題

### メンターが慢性的にすくない...

わたくしと、メンターのあきさん2人が定常的にメンターをやっていて、あとは毎月応募してくれるメンターの方がお手伝いしてくれる形でやっていますが、足りないと感じることが多いです。他の道場の方も話していましたが、大人も楽しめるような仕組みが必要だと感じています。

### マンネリ化しないか...

長津田はまだ1年もやっていないので、まだマンネリを感じているわけではないですが、毎月同じ繰り返しだと、メンターもニンジャも飽きを感じるようにならないかなという心配はあります。

### 資金面

現状は募金でだいたい会場代を賄うくらいにはなっていますが、当初考えていた子どものプログラミングを体験する機会に対する投資が出来る状況ではないです。

## 今後について

まとまりもなく長くなりましたが、これからも今までと同じようにCoderDojo長津田は続けていく予定です！

2018年も何か面白いことができるように、変化を恐れずやっていきたいと思います。

最後に来年やりたいことを書いておきます。

 - ScratchやMinecraft以外にも、体験できる教材、対応できるプログラムを増やす。
 - 大人も子どもと一緒にプログラミングを勉強できるようにする。
 - 地域のつながりを増やす。各種地域イベントなどとのつながり。
 - 神奈川県地域のCoderDojoで何か横連携したい！
