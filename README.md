## 自己紹介
札幌在住のwebエンジニアです。  
web技術や機械学習が好きです。

主なスキルは以下の通りです。  
- Web技術  
    バックエンド: Django(DRF)  
    フロントエンド: Vue.js, React  
    DB: postgres  
    インフラ: Docker, AWS EC2, Serverless Framework, GitHub  
- 機械学習  
  ライブラリ: Pytorch  
  モデル: CNN, RNN(LSTM), Transformer(BERT, Llama2)  


## ポートフォリオ

### Webサービス

#### [HAKUSHI](https://hakushi.biz/)
<details>
  <summary>詳細はこちらをクリック</summary>
  
URL: https://hakushi.biz/  
      テーマ: モチベーション維持をテーマに設計されたモチベーション支援サービス。  
      開発期間:  2022年6月リリース   
      DAU:3人  

      使用技術  
      バックエンド: Django, DRF  
      フロントエンド: Vue3.2  
      インフラ: Docker, AWS EC2, sentry
</details>

#### [PaperwithFusion](https://staging.d3mw4gj6mldhry.amplifyapp.com/)
<details>
  <summary>詳細はこちらをクリック</summary>
  
URL: [STG環境](https://staging.d3mw4gj6mldhry.amplifyapp.com/)  
      テーマ: 核融合研究者が先行研究調査業務に特化した検索エンジン  
      開発期間:  2024年冬リリース予定   

      使用技術  
      バックエンド: Python  
      フロントエンド: React  
      インフラ: AWS Amplify, Serverless Framework(API GateWay, Docker, Lambda)  
      Embedding(チューニングなし): albert-base-v2  
      形態素解析: spacy  
      近傍探査, TF-IDF: scikit-learn  
</details>

### 情報発信

#### [記事執筆](https://zenn.dev/pikum)  
<details>
  <summary>詳細はこちらをクリック</summary>
  
URL: [Zenn](https://zenn.dev/pikum)  
    個人開発で学んだことのアプトプット

</details>

### その他

#### ツール開発(開発中)

<details>
  <summary>詳細はこちらをクリック</summary>
  
  - TechDebtExplorer  
  技術的負債を可視化することを目的とした計算ツールです。
  
  [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=pikum99&repo=TechDebtExplorer)](https://github.com/pikum99/TechDebtExplorer)

  使用技術  
  言語: Python  
  アルゴリズム: Levenshtein  
</details>

#### 機械学習モデル開発

<details>
  <summary>詳細はこちらをクリック</summary>
  
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
</details>


## プロジェクト経験(業務経験)

### 商品管理プロジェクト

<details>
  <summary>詳細はこちらをクリック</summary>
  
#### 概要
 - 商品管理システムのメンバーとして従事  

#### 規模
- 10人程度  

#### 役職
- メンバー  

#### アピールしたい事項
##### 旧システムから現システムのリプレイスメント案件  

【課題】  
数千万レコードのデータ移管において、現行使用していた移管手法では、多大なる労力かかること。また、ヒューマンエラーが起こる可能性が秘められていたこと  

【工夫したこと】   
現行使用していた移管手法は、本番環境にscpでcsvを送り付け、ログをローカルに保存するという古典的移管手法を用いておりました。これでは、データ起因によるリカバリ対応において多大なる労力がかかることに加え、ヒューマンエラーが起こることが目に見えておりました。そこで私は、現状の問題点をまとめ、このままではリプレイス案件が失敗しかねないことを上長に相談し、バッチを修正する許可をいただきました。具体的に取り組んだことは以下の通りです。  
- AWS S3でデータ移行のCSVを管理し、そこからboto3経由で直で取り込みを行い、ログもS3に吐き出すというところに書き換え
- 移行実行に関してもシェルスクリプトで実行していたが、それも全てpythonに書き換えた
- 実行フローに関しても変更を行った  

【成果】  
本番のデータ移行時期においては、案の定、システム間のDBの設計差異に起因するエラー、他作業者の起因のエラーが多発しましたが、上記の対応を行ったため、リカバリー工数も対してかからなく無事データ移行を行い、リプレイスメント案件の成功に大きく寄与できたと思っております。

##### 部分的クリーンアーキテクチャの導入  

【課題】  
現在のチームでは、一部のスキルの高いエンジニアがクリーンアーキテクチャの概念を用いたコーディングをしていたが、アーキテクチャの概念がチームで行き渡っていなく、十分なPRのレビューがされず、かえって品質低下を招く恐れのあるチーム体制だった


【工夫したこと】  
私はそれを問題視し、自発的に「現在のプロダクトにアーキテクチャの概念は必要か？」という資料を他社の導入事例を交えて作成し上長に提出。その後、チームMTGで用意した資料を発表しました。


【成果】  
    「機能が独立しているバッチ周りから」というアプローチを提案し、チーム全体で部分的に導入を進めることに成功しました。　　
その後、チーム全体で、現在の理解している範囲でクリーンアーキテクチャの知識を講義し、チーム全体の理解の均一化を図りました。結果としてその後のプルリクレビューの精度も向上したと思います。  

##### プロダクトのコア機能を根本改修  
【課題】  
上記の通り「一部のスキルの高いエンジニアがコア機能をクリーンアーキテクチャで書き換える」ということを行われていたが、中途半端な状態で担当者が退職し、それを期限の納期までに動かす


【工夫したこと】   
使えるエンティティに関しては使用し、「依存性が判然とせずに、動的に呼び出す」というスパゲッティになりやすい箇所に関しては根本から書き換えるという作業を行いました。


【成果】  
引き継ぎタスクではありますが、数千行を超える神クラスをちゃんとビジネルロジックに落とし込み、それなりに後続の方が改修しやすいようなコーディングができたと思います。ここからは個人的な考えではありますが、プロダクトのクリーン化に関してはビジネスロジックとデータフロー図やER図等と真剣に向き合って、熟考した結果、着手するべきだと思っております。また、安易な疎結合に関しては疑問視しており、疎結合するべき層としてはいけない層があると考えており、それも日々改善の日々だと思っております。

</details>

### 機械学習を活かしたプロダクトのPoC

<details>
  <summary>詳細はこちらをクリック</summary>

#### プロジェクトの概要
 - インターン生と協力しながら、機械学習を活かしたプロダクトのPoCの業務

#### 規模
- 社員1~2人 (ほぼ私1人)
- インターン生3~5人(最大10名)  

#### 役職
- プロジェクトリーダー

#### アピールしたい事項
【課題】
何も整備されていない状況でインターン生と協力して成果を出す

【工夫したこと】  
- 配属されたインターン生に対して、現状のスキルの聞き取りを行い、スキルに伴ったことを何ができるかを考え実際に手を動かせるレベルで着手できるように課題設定を適宜おこない、人に説明できるレベルまで持っていった
- ピーク時はインターン生9人を一人で商品管理の業務をこなしながら面倒を見た
- 各チームに対して事情を説明し、各チームからデータセットを提供してもらい、研究できる環境を整備した

#### 成果一覧
#####  [汎用的画像分類モデルの作成(1カテゴリ 学習枚数 ~10枚)](https://note.com/diamondhead/n/n0498097e0f06)

技術:   
バックボーン: Conv Next  
エンドポイント: AWS SageMaker  

解決したい課題:   
人間が行なっている画像並び替えをAIにやらせる  

進捗:  
プロダクトの検証環境まで導入完了

##### 商品需要分類モデルの作成 
技術:  
バックボーン: LightGBM  

解決したい課題:
社内の売り上げビックデータを用いてどの商品が売れるか、値段設定はいくらが適切かを予測するモデルの作成  

進捗:  
売れるか売れないかのの分類問題に落とし込み精度8割のモデルが完成。  
プロダクト構想とモックをFigmaで作成。  

#####  商品説明, ハッシュタグ自動生成モデルの作成　
技術:  
バックボーン: Llama2  

解決したい課題:  
現在人間が行なっている商品説明文、ハッシュタグをAIにやらせる

進捗:
データセットを整備し、ほぼ違和感がない商品情報から商品説明分とハッシュタグを自動生成できるモデルを完成。

</details>

## プロジェクト経験(個人開発)

### キャラクターを用いた勉強記録webアプリ

<details>
  <summary>詳細はこちらをクリック</summary>
  
#### プロジェクトの概要
ToCに向けたキャラクターを用いた勉強記録webアプリの企画・開発・運用

#### URL  
[HAKUSHI](https://hakushi.biz/)

#### 開発規模
個人開発

#### ユーザー規模
DAU: 3人

#### 主要技術と選定理由
【主要技術】
```
バックエンド: Django, DRF
フロントエンド: Vue3.2 
インフラ: Docker, AWS EC2, sentry  
イラスト作成: Stable Diffusion  
```

【選定理由】  
バックエンド:   
大学院の知見を活かせるようにpythonを採用しました。また、フレームワークに関してはリッチでスケールできるサイトを作りたかったので、Django(DRF)を採用しました。また、EC2にしている理由は、ECRとECSでスケールできるようにしたいと思っているからです。

フロントエンド:  
Vueは業務で使っていたため、工数削減のため、Vue.jsにしました。

#### アピールしたい事項
全てを一人で作っているので、コンセプト選定〜インフラ構築〜開発〜広告まで一通りのことを経験しました。その中でもアピールしたいのは以下の事項です。  

#### コンセプト選定, 技術選定
【概要】    
自分の思いつく限り、様々な機能を実装していましたが、市場の反応、自分が本当に使うのかというのをPDCAサイクルを2年間回しました。その行き着いた先が、現在のHAKUSHIというサービスになります。  


【使用した技術】  
PDCAサイクルを回す間は比較的工数のかからないMVTのDjangoを採用し、コンセプトが決まってからは、フロントエンドはVue.js、バックエンドはDjango REST frameworkを導入しております。　

#### WebSocketを用いたリアルタイム機能の実装  

【概要】  
以下のWebSocketを用いて機能を実装しました
- リアルタイムで作業しているユーザーを表示させる機能
- リアルタイムで付箋を共有する機能
- リアルタイムで文章を共有する機能(Google Documentの共有的なもの)

【使用した技術】  
この機能の実装には、非同期処理を可能にするAsync Web Serverと、高速なデータストアであるRedisを使用しました。Async Web Serverはリアルタイムでのユーザー情報の更新を、Redisはその情報の高速な取得と保存を担当しています。

</details>

### 核融合研究に特化した論文検索エンジン
<details>
  <summary>詳細はこちらをクリック</summary>

#### プロジェクトの概要
核融合研究に特化した論文検索エンジン

#### URL  
[PapersWithFusion(検証環境)](https://staging.d3mw4gj6mldhry.amplifyapp.com/)

#### 開発規模
個人開発

#### ユーザー規模
リリース前

#### 主要技術と選定理由
【主要技術】
```
バックエンド: Python  
フロントエンド: React(TypeScript)  
インフラ: AWS Amplify, Serverless Framework(API GateWay, Docker, Lambda)  
Embedding(チューニングなし): albert-base-v2  
形態素解析: spacy  
近傍探査, TF-IDF: scikit-learn  
```

【選定理由】  
バックエンド:   
機械学習を用いた並び替え機能を実装したかったので、バックエンドはPythonであること、なるべくデプロイ周りを軽くしたかったので、Serverless Frameworkを採用しました。

フロントエンド:  
HAKUSHIではVue.jsを採用しておりましたが、個人としてはisoアプリ展開をしていきたいと思っていましたので、個人の勉強を兼ねてReactを採用しました。

機械学習まわり:  
近年進捗が目まぐるしいDeepLerningを使いたかったので、Embeddingにはbertを採用しようと思い、その中でも一番軽量であるalbert-base-v2を採用しました。近傍探査に関しては、導入が容易であるscikit-learnを採用しています。検索機構にはよりますが、もし速度がでないという話になってきたら頑張ってnmslibを導入したいと思います。


#### アピールしたい事項
現役研究者にヒアリングしながら、現在業界に足りていないであろう特化型論文検索サイトを作成しております

##### 機械学習を用いた関連順機能
【概要】    
ただのキーワード検索だけではなく、Bertを使いEmbeddingしたのちに、近傍探査を用いて関連順を出すといった機械学習ができる人間ならではのエンジンを作っていきたいと思っております。

また、
- docker
- serverlessフレームワーク
- Bert

以上の技術を組み合わせることによりAWSのlambdaで上記のBertを使うといったコスト対策に特化したアーキテクチャとなっております。

</details>

## その他

### 大学院時代の経験
<details>
  <summary>詳細はこちらをクリック</summary>
  <p>
大学院では、先輩のいない研究室で博士課程を含む計5年間在学しました。研究室内での役割として、後輩のタスク整理と具体的な指導に携わり、研究室の柱としての役割を果たしていました。  
また、個人の成果としては以下の通りです（詳細リンクは経歴を参照）。

- 国際論文誌に2本の論文が掲載
- 日本学術振興会 特別研究員(DC2)に採択
- マックスプランク・プラズマ物理研究所との共同研究
- 核融合年会で若手優秀発表賞を受賞

これらの実績から、人のマネジメント経験や申請書の作成方法、外国人を含むプロジェクトの進行方法、成果の発表手法に関しては、通常以上の実績があると自負しています。
  </p>
</details>


### 目指したいエンジニア像と現状
<details>
  <summary>詳細はこちらをクリック</summary>

1. **フルスタックエンジニアとしての基礎を固める**
   - バックエンド、フロントエンド、インフラなどWebアプリ全般の開発経験を積みたい
   - チームリーディング、プロジェクトマネジメントの経験も積みたい
   - 並行して機械学習(Pytorch等)の実践と理解を深める

2. **MLOpsの知見を身につける**  
   - 機械学習モデルの実運用(MLOps)に関する知識・経験を蓄積
   - 大規模データ処理(Spark,Kafka等)の技術を学ぶ
   - クラウド上での機械学習ワークロードの最適化を習得

3. **機械学習モデルのWebアプリ実装を経験**
   - PoC段階の機械学習モデルをWebアプリに実装する
   - .ipynbファイルを.pyに落とし込み、アーキテクチャ化する
   - 個人開発の機会(負債可視化ツール等)を活用

4. **AI製品開発のリーダー**
   - これまでの経験を活かし、AI×Webの新製品を企画・開発
   - 開発チームのリーダーとして技術的負債管理も行う

</details>


### エンジニアになった背景
<details>
  <summary>詳細はこちらをクリック</summary>

社会に大きなインパクトを与え、社会貢献をすることに人生の進路を重要視してきました。  
大学院では「夢のエネルギー源 核融合発電」の研究に従事していました。  
IT業界に転身したきっかけは、核融合発電の業界規模が非常に大きいため個人の貢献に対するプロダクトへの影響が実感できないことに悩んでいたところ、研究中にweb技術(Django)に触れ、web技術であれば個人の貢献がプロダクトに対して大きな影響を持つ、かつ世界中の人に社会貢献できると考え、IT業界に飛び込みました！  

新しい技術が大好きで、研究でもweb開発においても知らない面白そうな技術があればすぐに試してみることをしております。   
</details>


### 経歴
<details>
  <summary>詳細はこちらをクリック</summary>

- 九州大学大学院工学修士, 2017年 - 2019年
- 九州大学大学院博士課程単位取得退学, 2019年 - 2022年
  - [高温プラズマにおける電磁波相互作用の研究](https://research-er.jp/researchers/view/894298)
  - Ghz帯の偏波制御装置の開発([国際論文雑誌掲載](https://www.sciencedirect.com/science/article/abs/pii/S0920379619302741))
  - 多素子アレイプリント基板アンテナの製造及び回路、計測システムの実装([国際論文雑誌掲載](https://www.jspf.or.jp/PFR/PFR_articles/pfr2019/pfr2019_14-3402111.html))
  - 高温プラズマにおける電磁波シミュレーション([マックスプランク・プラズマ物理研究所との共同研究](http://www.iae.kyoto-u.ac.jp/plasma/pladys/news/2019/PLADyS.Report.20200319.Fukuyama.pdf))
- webエンジニア, 2022年 -
  - 商品管理システム開発メンバー
  - 機械学習チームマネージャー
</details>


### 受賞歴など
<details>
  <summary>詳細はこちらをクリック</summary>

- 学府専攻賞
- ウシオ財団 奨学生
- [日本学術振興会 特別研究員](https://research-er.jp/projects/view/1119159)
- [核融合年会若手優秀発表賞](https://www.jspf.or.jp/award/wakate.html)
</details>
