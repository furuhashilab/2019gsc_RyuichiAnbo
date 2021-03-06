# 2019年度古橋研究室ゼミ論文

『FOOTBALL×GPS』

地球社会共生学部 1A117007 安保龍一/Ryuichi Anbo

-----------
# 資料
- [ゼミ論中間報告　報告書](https://medium.com/furuhashilab/12-20-%E3%82%BC%E3%83%9F%E8%AB%96%E4%B8%AD%E9%96%93%E5%A0%B1%E5%91%8A-ec9fd72af741?source=friends_link&sk=75de87c6009de1261cd6251de238a594)


- [ゼミ論中間報告　プレゼン用資料](https://docs.google.com/presentation/d/1OoMceupmSV5lmiR66yzRAXN-5ewf4eF814-CYeI9b1w/edit?usp=sharing)

- [ゼミ論最終報告　提出用資料](https://docs.google.com/document/d/1qflv5P9f4mjFx2pE4thZjV8PdTn9mnQMXT3bqYnNFck/edit?usp=sharing)

- [ヒートマップ](https://github.com/furuhashilab/2019gsc_RyuichiAnbo/blob/master/data/temp/スクリーンショット%202020-01-18%2023.07.24.png)

- [アプリ](https://fdutz.glideapp.io)

- [ゼミ論最終報告　プレゼン用資料](https://docs.google.com/presentation/d/1hx8v2ZQERkS5ezE8MNQh7KyUz56WjiyeuxRrcIA_6uw/edit?usp=sharing)

- [参考文献](https://docs.google.com/spreadsheets/d/1tF85AooQjIDpIcdRMANfpsv9Awpu4CfdAofZbnkmW3k/edit?usp=sharing)

--------------
### 本文
## 目次
①はじめに

②動機

③方法

④結果

⑤論点

⑥結論

⑦参考文献

⑧謝辞
## はじめに
近年の技術の進歩や発展は単に我々の生活の向上をさせただけでなく、様々な分野でその効力を発揮している。その一つともされるのがスポーツ分野である。特にサッカーでは多くの国、リーグ、チームでデータ化が浸透している。これまでは客観的に試合を見てその中でのプレーからでしか技術や戦術の向上を図ることができなかったが、主にGPSを用いたデータ分析により今までとは全く違う観点で試合を分析できるようになった。本研究では、このデータによって分析するハウツーを青山学院大学体育会サッカー部にも取り入れる事を目的とする。GPSデータとはいっても様々なデータを入手する事が可能なため、今回はX値Y値(座標)と時間軸をリンクさせてQGISも用いてヒートマップの作成とする。大学サッカーは前期後期を通じて22試合が行われる。ヒートマップとして情報を収集するのは、より高いレベルである関東2部大学サッカーリーグに限定して行う。また、ヒートマップの展開先としてはGlideで作成したアプリを青学サッカー部員限定で公開する。その他にも青学サッカー部にとって優位性のある情報発信や、スケジュール管理などをアプリを通して行使していく。あくまでも公開対象はサッカー部関係者とする。
## 動機
私は青山学院大学体育会サッカー部に所属しており何か古橋研究室での研究とリンクさせたいと思いヒートマップ作成をすることにした。私自身も現在プレーを続けている環境の中で大学サッカー界ではあまりデータを活用しているチームが少ないという印象を受けた。プロの世界ではもう当たり前とされているデータ分析をどうにか形にして大学サッカーに還元したいと考えた。今回の先行研究として用いたのは古橋教授から推奨していただいた岡部篤行氏らが研究した「無線位置システムによる話飼鶏の追跡データ取得とその空間分析」である。
## 方法
本研究で行ったことは以下である。
・GPSports EVOでリーグ戦の各選手のGPSデータを収集、編集
・QGISにてヒートマップ作成
・PowerPointにて土台なるサッカーフィールドをトレース
・GIMPにて2つのデータ(画像)を結合
・Glideにてアプリ作成
基本的にはリーグ戦での各選手にGPSを装着して頂いき、試合のデータを測定。試合後GPSユニットをドッキングステーションに戻しそのデータをパソコンに落とし込む。その後このデータを各選手ごとで分割し、編集を行う。そのデータを元にQGISにデータをインポートして地図にデータを落とし込む。ヒートマップの背景はサッカーコートなので高画質な画像をPowerPointにてトレースし、GIMPで2つを結合。最終的にはスプレッドシートのみでアプリが作成可能なGlideでアプリを展開して情報を公開する。
## 結果
今回ヒートマップ作成にあたってQGISを使用した。基本的にはこのような作業をした経験がないのでネットで情報を収集しながら探り探りで進めていった。QGISにデータソースとしてCSVで取り入れようとしたがデータが重すぎてフリーズ。それもそのはず、今回使用したのがGPSports EVOと呼ばれる機材で性能は15hzで1秒間に15回計測をすることができる。1試合90分のデータをこの機材で扱うと11万ポイントにもなる。ここで古橋教授の助言によってGeoPackage形式にしてデータを取り込んだ。CSVと比較してQGISへのデータインポートが容易にできる。実際にQGISがバージョン3にアップデートさらてからはCSVを用いるよりGeoPackageを用いるのが圧倒的に効率が良い。アップデートに伴ったマニュアルがあれば初心者にも易しいと感じた。また、当たり前ではあるがネットにソースフリーとして上がっている画像が解像度が非常に低い。そこでトレースして高画質にする必要がある。今回はIllustratorは使わずに最も容易にトレースすることができるPowerPointを用いた。
## 論点
データ活用が本当に勝ちに繋がるのか。これは誰もが考える素朴な疑問だと思う。実際に私も当初はその様な疑問を抱いていたが、スポーツがデータ化され分析の質は格段に発展した。GPSユニットを装着することで今回はX値Y値の座標データのみを用いたが、もっと簡単に試合をデータとしてみる方法もある。最高速度、スプリント回数、走行距離など当たり前なものかもしれないが、この数値はプレーをしている選手からしてみれば非常に優位なものである。ユニットを付けずに普通にプレーしているだけでは自身がどのくらい走ったのかというのは自身の感覚のみになる。負けた試合にはそれなりの理由があるし、少なくともそのソースの一つとしてデータを活用できたらより迅速に練習に落とし込むことができる。それ程この時代のスポーツにおいてデータ化というものは欠かせないものとなる。
## 結論
本研究ではGPSユニットで収集したデータをもとに、QGISでヒートマッを作成しました。冒頭で述べた通りサッカー界でもデータ分析の導入が積極的に行われているのが実態です。ヒートマップという座標のみを活用した極一部のデータではあるが、青山学院大学体育会サッカー部に還元させていきたい。また、Glideで作成したアプリで情報を発信していく。現状として４つのタブを使っているがこれ以上多くなると少し情報が渋滞する恐れがあるため本当に必要な情報発信アプリとして見つめ直しが必要だ。今回は、ゼミ論としてとある一選手のみでヒートマップ作成を行ったのでチーム全体のマップを作成していく。
## 参考文献
[Qiita](https://qiita.com/Yfuruchin/items/5aa60ad983b3b58a7ac1#qgisにとりこむ):サッカーのヒートマップをQGISで作ってみるのページ

[QGIS Tutorials and Tips](https://l.facebook.com/l.php?u=https%3A%2F%2Fwww.qgistutorials.com%2Fen%2Fdocs%2F3%2Fcreating_heatmaps.html%3Ffbclid%3DIwAR2QrbKK2Pn7yLgsdZ4wJJ_yZKthVK9DTbER1nUJrG29hLFOR8nBRuLx-DI&h=AT1g8ZzKxPwt4PIEum0LHc7z_5T5j4wdMm0Nnp5tAAXIx3r-i1TGgfnR2XD7saes1kHM1D2ibjif5RLs470dMqQAl8ReLKbut80SHyTMYQWUKzzQVTGfBaj1PbFXUsz9fTgjEa9xuYo):Creating Heatmaps (QGIS3)のページ

[synclogue navi](https://synclogue-navi.com/category/gimp/):GIMP の使い方のページ

## 謝辞
本研究を進めるにあたり青山学院大学古橋研究室の古橋教授をはじめ多くの方々より多大な助言を賜りました。厚く感謝を申し上げます。
