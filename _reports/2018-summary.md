---
categories: reports
title: "CoderDojo長津田2018年まとめ (CoderDojo Advent Calendar 2018)"
header:
  overlay_image: /assets/images/posts/19/33.jpg
  overlay_filter: "0.5"
  teaser: /assets/images/posts/19/33.jpg
excerpt: "CoderDojo長津田2018年のまとめ記事です。"
---

この記事は[CoderDojo Advent Calendar 2018](https://adventar.org/calendars/2955)の19日目の記事です。

2017年も書いてました。

[CoderDojo長津田2017年のまとめ](/reports/2017-listicle/)（同じく19日目！）

## 自己紹介

CoderDojo長津田（横浜市緑区）のチャンピオンをやっている植田です。普段はフリーランスとしてiOS, Androidのアプリ制作やサーバサイドの開発をやっています。

![image-center](/assets/images/posts/19/IMG_0333.jpg){: .align-center}

全然関係ないですが、最近はロードバイクとSUPにハマってまして、一緒に遊んでいただけるお仲間募集中でございます。

![image-center](/assets/images/midori-front.jpg){: .align-center}

さて、CoderDojo長津田は長津田駅近くの横浜市緑区の公民館（みどりアートパーク）で月1度開催していまして、約1年半運営してきました。

今回は下記のような流れで1年の振り返りをしていきます。

- 前回開催レポート
- 数値でみるCoderDojo長津田（2018年版）
- 運営で工夫したこと
- 運営で感じた課題
- 今後やりたいこと

## 先日第19回CoderDojo長津田開催しました

![image-center](/assets/images/posts/19/19.jpg){: .align-center}

ニンジャ16名、メンター5名の参加でした。

![image-center](/assets/images/posts/19/10.jpg){: .align-center}

いつもワイワイ賑やかにやってます。

CoderDojo長津田では、Scratch、Minecraft、micro:bit、ロボット系など、様々な取り組みをしているのが一つの特徴です。

まだ初心者の方から、Scratchでいつも面白いゲームを作るニンジャ、PythonのWebプログラムを書いてしまうニンジャまで、さまざまなレベルのニンジャがいます。

## 数値で見るCoderDojo長津田 2018年版

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
      ["9", 13, 3],
      ["10", 14, 2],
      ["11", 11, 3],
      ["12", 18, 2],
      ["13", 16, 2],
      ["14", 20, 3],
      ["15", 16, 3],
      ["16", 15, 2],
      ["17", 13, 2],
      ["18", 13, 3],
      ["19", 14, 2],
    ]);

    var options = {
      title: '開催回ごとのニンジャ数',
      height: 300,
      isStacked: true,
      hAxis: {
        title: '開催回',
        viewWindow: {
          min: [7, 30, 0],
          max: [23, 30, 0]
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
      ['5歳以下', 7],
      ['6歳',  17],
      ['7歳',  46],
      ['8歳',  40],
      ['9歳',  64],
      ['10歳',  23],
      ['11歳',  8],
      ['12歳',  6],
      ['13歳以上',  0],
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
      ["9", 50.00, 7.41],
      ["10", 75.00, 11.11],
      ["11", 78.57, 10.19],
      ["12", 50.00, 9.26],
      ["13", 83.33, 13.89],
      ["14", 69.57, 14.81],
      ["15", 73.68, 12.96],
      ["16", 76.47, 12.04],
      ["17", 86.67, 12.04],
      ["18", 93.75, 13.89],
      ["19", 87.50, 12.96],
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
      ["9", 4],
      ["10", 5],
      ["11", 4],
      ["12", 7],
      ["13", 5],
      ["14", 7],
      ["15", 6],
      ["16", 5],
      ["17", 4],
      ["18", 7],
      ["19", 5],
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

今年は11回の開催で、今年だけで延べ190人もニンジャが来てくれました。

ありがたいことに最近は、CoderDojoの募集を開始すると1日で参加人数が定員に達するようになりました。

統計は取っていませんが、来てくれてるほとんどは地元長津田ではなく、近くの駅から電車で通ってくれていました。

### ニンジャの年齢比率

<div id="chart_div_age"></div>

こちらは2018年だけのものです。だいたい小学生1-3年の年齢で3/4を占めていました。（感覚ではもう少し高いかと思ってましたが。）

中学生以上にもぜひ来てほしいなあとは思うんですが、クラブ活動、塾などで忙しいんですよね。。

### リピート率

<div id="chart_div_repeater"></div>

リピーター率はリピーター数を各回のニンジャ数で割ったもの。

リピート率はリピーター数を今までのニンジャのユニーク数で割ったものです。

最近は、うれしいことに特にリピーターの割合がかなり上がっています。

募集の枠がすぐに埋まってしまっていて、新しい人が入りにくくなっている可能性があるので、それはまた別の受け皿が必要かもしれません。

### メンター数

<div id="chart_div_mentor"></div>

今年に入ってメンターで来ていただける方がかなり増えました。

昨年はメンターが少なくて、本当に困っていたので特にうれしい！

## 運営で工夫したこと

### アンケートと発表シート

CoderDojo長津田ではアンケートを毎回書いてもらって、運営の改善の材料にしています。子供が書くとまあ楽しい感じになっていたりもするんですが、奇譚ないご意見はとても参考になっています。

[CoderDojo長津田アンケート](/assets/pdf/CoderDojoNagatsutaSurveyVer2.pages.pdf)

あと他のDojoの方からも、「いいですね」と言ってもらえるのが、「発表シート」です。

みんなの前で発表するのに何をしゃべるかわからないということがよくありますが、この発表シートに事前に書いてあれば読むだけで発表ができるというものです。

[CoderDojo長津田発表シート](/assets/pdf/CoderDojoNagatsutaPresentationVer1.pages.pdf)

良ければ自由にアレンジなりしてご利用ください。

### 情報共有

Facebook、Twitter、ホームページの更新をできる限り行うようにして、どういう雰囲気のDojoなのか、運営している人たちがどういう人なのかをわかるようにして、初めて参加される方が参加しやすいように工夫してきました。

やっぱりアクティブに活動しているかどうかというのが、目に見てわかるほうが、初めての方も安心できるかと思います。

また、問い合わせに関しても、保護者の方や、Dojoの開設、メンター相談含めてかなり増えましたが、なるべく早く答えられるようにしてきました。

### Minecraftの活用、その他のコンテンツも増えた

小学生はマイクラ好きが多いです。（私も大好きです！）

Minecraft目当てで来てくれるニンジャも、長津田は多いと感じます。Minecraftはプログラミング学習の導入には、かなり良いツールだと個人的には思っています。学習やっているのか遊んでるのか、、みたいなことも多々ありますが、これからもしっかりサポートしていこうと考えています。

また、今年はScratch Dayを開催したり、MESHのトライアルプログラムが出来たり、Progateさんとのプログラミング教育コンテンツが増えたり、またメンターさんが持ってきてくれた、micro:bitやロボットなども含めて、体験できるコンテンツが増えたのもとても良かったと思います。

### メンター間の共有

昨年はニンジャが増えても、メンターがなかなか増えない、という状態があり、ニンジャの人数を増やせない事情がありましたが、今年に入った頃から、積極的に参加していただける、優秀なメンターの方々が増えました。（いつもありがとうございます！）

またFacebookでメンター間で情報共有していますが、情報や問題点を流すとメンターの方からすぐに返信をいただけたりして、本当に助かっています。

CoderDojoを通じてメンター仲間を緩く増やすことも、私自身の運営をやっている目的の一つですので、興味のある方いらっしゃいましたら、次回メンター予約をお願いしますmm

[第20回 CoderDojo長津田](https://coderdojo-nagatsuta.connpass.com/event/113255/)

## 運営で感じた課題

### 会場問題（人数、ネット環境）

今の会場では学習できて、人数が増やせる部屋がないのが現状です。

また会場が地下にあり人数が多いということもあり、ネット環境でトラブルもそれなりに多いです。

ネット環境に関しては、会場の懇親会で設備を訴えかけてきて、先方の担当の方も是非取り組みたいと言ってくださっていたので、使えるようになるんじゃないかという期待を持っています。

会場も市内、市外で探していて、良いところもあったんですが、会場の審査関連でいろいろ問題があったり、市外だとそもそも長津田ではなくなるので、どうしようみたいなこともあったりしますが、引き続き来年も取り組んでいきます。

開催日を増やすという選択肢はいまのところあまり考えていないです。

最近は近辺のDojoがかなり増えたので、それで解決するかもしれません！

### 資金、運用面

現状はすべて会場での募金で会場の運用費などは賄っていますが、当初1年半でやっと収支がトントンでした。

[CoderDojo長津田 収支](/support/)

当初はプログラミング体験できるものを増やすような投資をしていきたいと考えていましたが、まだそこまでにはなっていません。

## 今後やりたいこと

最後に来年やりたいことを書いておきます。

 - 神奈川県地域のCoderDojoでまた「でかDojo」をやりたい！
 - いつもと違う環境、場所でDojo開催してみたい（キャンプ場とか！）
 - ニンジャたちが共同開発できるようなイベント、ワークショップ企画
 - メンター、保護者同士の勉強会、交流会

![image-center](/assets/images/posts/19/42.jpg){: .align-center}

長くなりましたが、これからもCoderDojo長津田をどうぞよろしくお願いいたします。

<!--
明日20日の[CoderDojo Advent Calendar 2018](https://adventar.org/calendars/2955)は、

taniokahさんの[]()

です。 -->
