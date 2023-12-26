## 自己紹介
札幌在住のwebエンジニアです。web技術や機械学習が好きです。

現在得意とするスキルは以下の通りです。  
バックエンド: Django  
フロントエンド: Vue.js  
インフラ: Docker, AWS, GitHub
機械学習: Pytorch

## ポートフォリオ

### Webサービス

- [HAKUSHI](https://hakushi.biz/)  
  キャラクター支援型TODO管理サービス。
  
  使用技術  
  バックエンド: Django  
  フロントエンド: Vue.js  
  インフラ: Docker, AWS  

### ツール開発

- TechDebtExplorer  
  技術的負債を可視化することを目的とした計算ツールです。
  
  [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=pikum99&repo=TechDebtExplorer)](https://github.com/pikum99/TechDebtExplorer)

  使用技術  
  言語: Python  
  アルゴリズム: Levenshtein  

### 機械学習モデル開発

- StockNN  
  株価をテーブル分類問題として予測しようとしたプロジェクトです。
  
  [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=pikum99&repo=StockNN)](https://github.com/pikum99/StockNN)

  使用技術  
  ライブラリ: PyTorch  
  モデル: LSTM + MLP

- BoatRaceNN  
  ボートレースの結果をテーブル分類問題として予測したプロジェクトです。
  
  [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=pikum99&repo=BoatRaceNN)](https://github.com/pikum99/BoatRaceNN)

  使用技術  
  ライブラリ: PyTorch  
  モデル: MLP


### 執筆記事

[qiita プロフィール](https://qiita.com/pikum)


## 目指したいエンジニア像と現状
webサービスにおいて企画・PoC検証・MVP開発・PMF達成・PMF達成後の運営開発しながら技術的負債の管理まで一貫してできる人物になることを目指して、日々過ごしております。  
具体的には、以下の項目に分けて取り組みを行っております。  
 - 企画・PoC検証:  
   機械学習を使って、AIの可能性について収集(現会社、個人開発)
 - MVP開発:  
   負債化可視化ツールの開発(個人開発)
 - PMFを目指す:  
   HAKUSHI(個人開発)
 - 運営開発しながら技術的負債の管理:  
   現在の職場のプロダクト

## 具体的なエピソード

### 機械学習チームマネージャー
 現在の職場で、学部生から大学院博士課程までのインターン生を4〜5人（最大9人）束ね、機械学習チームのマネージャーを務めています。
 上層部からは具体的なタスクが指示されるのではなく、抽象的な目標が提示されている中で、柔軟かつ効果的なチームの運営を行っています。
 インターン生が配属された先には、インターン生の研究スキルの聞き取りを行い、チームが達成するべき目標とインターン生の研究スキルのすり合わせを行い、時に一緒に論文を読みながら、具体的なテーマを設定し、具体的な方針を指導しております。  
 具体的な成果は以下の通りです
 - データセットの概念がないので、私個人で事情を説明し、他チームに頭を下げてデータセットの整備
 - 汎用的画像分類モデルの作成(1カテゴリ 学習枚数 ~10枚) バックボーン: Conv Next
 - 商品需要分類モデルの作成 バックボーン: LightGBM
 - 商品説明, ハッシュタグ自動生成モデルの作成　バックボーン: Llama2
 - 汎用的画像分類モデルAPIを作成し、既存プロダクトと連携
 - 商品需要分類モデルを活用した、値引き最適化サービスの構想とそのプロトタイプの作成


研究とビジネスの境目でマネージャーをしておりましたので、**AIをビジネスに転用するにあたってここは気をつけなければならない**という知見を得ることができました。また、機械学習で学んだ知見を生かして、上記のポートフォリオにあるレポジトリの開発を行っております。

### HAKUSHIの個人開発
[HAKUSHI](https://hakushi.biz/)というwebサービスを個人開発しております。ほぼ全てを一人で作っているので、インフラ構築〜開発〜広告まで一通りのことを経験し、その難しさを痛感しております。
具体的に取り組んだことは以下の通りです。
- コンセプト選定  
  自分の思いつく限り、様々な機能を実装していましたが、市場の反応、自分が本当に使うのかというのをPDCAサイクルを2年間回しました。その行き着いた先が、現在のHAKUSHIというサービスになります。
- 技術選定  
  PDCAサイクルを回す間は比較的工数のかからないMVTのDJnagoを採用し、コンセプトが決まってからは、フロントエンドはVue.js、バックエンドはDjango REST frameworkを導入しております。現在は、EC2にまとめて載せているので、これからは、フロントエンドサーバーを立てる、バックエンドデプロイにはECR+ECSのCICDの構築をやっていけたら良いと思っております。

### 現在の職場のプロダクトにオニオンアーキテクチャの導入
上記の経験を踏まえ、現在の職場のプロダクトではアーキテクチャの概念が不足していたため、チームミーティングで積極的に意見を述べ、アーキテクチャの重要性を説明しました。具体的には、「まずはレポジトリ層から」というアプローチを提案し、部分的な導入を進めることに成功しました。   
また、このプロダクトの具体的な業務として
- フルリプレイスメントに伴うデータ移管  
  旧システムから新システムへの移行時期だったので、様々なデータを移管させるために、仕様書作成から移管バッチ製造を行いました。
- 既存機能改修  
  検索機能がタイムアウトするぐらい遅かったので、ORMの呼び出し方法を変更し、N+1問題を解決して、速度改善を行いました。
- 新規機能開発  
  ふわっとした機能追加要件が多いのですが、そこから**丁寧に**認識合わせを行い、仕様書、試験書を作成してから、製造をおこなっておりました。(丁寧にしないと出戻り工数がもったいないので、、、)
- クライアント対応  
  システム移管ではクライアントのやりとりが必要になるので、その対応も行いました。

### 新規プロジェクト立ち上げ
現在の職場において、新規プロジェクト立ち上げに相談役として参加しました。  
このプロジェクトでは、私が機械学習チームマネージャーとしての経験と、個人開発のスキルを駆使して、新プロダクトのアーキテクチャ構想からAI機能の導入、具体的なユーザー体験の設計まで携わりました。  
この経験を通じて、現場のエンジニアに対する説明の難しさ、上層部との円滑なコミュニケーションの難しさ、さらには社内全体の雰囲気の調整の重要性を身をもって理解することができました。

### 大学院時代の経験
大学院では、先輩のいない研究室で博士課程を含む計5年間在学しました。研究室内での役割として、後輩のタスク整理と具体的な指導に携わり、研究室の柱としての役割を果たしていました。  
また、個人の成果としては以下の通りです。

- 国際論文誌に2本の論文が掲載（経歴を参照）
- 日本学術振興会 特別研究員(DC2)に採択
- マックスプランク・プラズマ物理研究所との共同研究
- 核融合年会で若手優秀発表賞を受賞

これらの実績から、人のマネジメント経験や申請書の作成方法、外国人を含むプロジェクトの進行方法、成果の発表手法に関しては、通常以上の実績があると自負しています。

## 背景
社会に大きなインパクトを与え、社会貢献をすることに人生の進路を重要視してきました。大学院では「無限のエネルギー核融合発電」の研究に従事していましたが、業界の規模に比べて個人での貢献が限られていることを実感していたところ、研究生活中にweb技術という分野に触れ、これなら個人でも大きな影響を持ち、かつ世界中の人に貢献できると考え、迷わずにIT業界に転身したという経歴があります。

新しい技術が大好きで、研究でもweb開発においても知らない面白そうな技術があればすぐに試してみることをしております。

いつの日か、研究 × web × 自分というコンテツを作り出し、自分にしかできない面白いことをゼロから生み出し、社会貢献できればと思っております。

## 経歴
- 工学修士,  旧帝大学, 2017年 - 2019年
- 博士課程単位取得退学, 旧帝大学, 2019年 - 2022年
  - 高温プラズマにおける電磁波相互作用の研究
  - Ghz帯の偏波制御装置の開発(国際論文雑誌掲載)
  - 多素子アレイプリント基板アンテナの製造及び回路、計測システムの実装(国際論文雑誌掲載)
  - 高温プラズマにおける電磁波シミュレーション解析([マックスプランク・プラズマ物理研究所](https://www.ipp.mpg.de/w7x)との共同研究)
- ソフトウェアエンジニア, 2022年 -
  - 商品管理システム開発
  - 機械学習チームマネジメント

## 受賞歴など
- 学府専攻賞
- ウシオ財団 奨学生
- 日本学術振興会 特別研究員(DC2)
- 核融合年会若手優秀発表賞
