# 業務経歴書

## 基本情報

|key|value|
|----|----|
|名前|瀬野 哲朗|
|ポートフォリオ|[myrails-react-todo-v4](https://github.com/m17n-dev/myrails-react-todo-v4)(Rails API + React)|
|ポートフォリオ|[BookSearchWpfApp](https://github.com/m17n-dev/BookSearchWpfApp)(.NET Framework)|
|Twitter|[@m17n_dev](https://twitter.com/m17n_dev)|
|Qiita|[@m17n_dev](https://qiita.com/m17n_dev)|

## 概要

- クラウドアーキテクチャ設計、クラウドインフラ構築管理、基盤コード開発、DevOpsが現在の専門です。

- バックエンドの複数の言語/DB/フレームワークを用いた開発経験、AWSの多数のマネージドサービスの開発経験があります。（フロントエンド開発、Androidアプリ開発、Windows系では.NET系の開発も多数経験しておりますが現在はLinuxプラットフォームでの開発がメインです）

- 小規模〜中規模サービスの新規開発フェーズを多く経験してきました。サービスのアーキテクチャ設計の段階から参画させて頂くことでバリューを発揮できるエンジニアだと思います。

## スキル

基本的にすべて実業務で使用した技術だけを列挙しています。

### 言語

Go | Java | Ruby | Python | PHP | Perl | JavaScript | TypeScript | VC++ | C# | Google Apps Script

### フレームワーク等

Gin | Express | Struts | Ruby on Rails | CakePHP | jQuery | React.js | MFC | .NET Framework | RSpec

### RDB/NoSQL

MySQL | PostgreSQL | Oracle | SQL Server | DynamoDB

### クラウド

#### AWS

VPC | S3 | CloudFront | API Gateway | Lambda | ELB | ECR | CodeCommit | CodeBuild | CodeDeploy | CodePipline | EC2 | ECS | Fargate | Route53 | ACM | IAM | RDS(MySQL|PostgreSQL) | DynamoDB | Kinesis firehose | SES | KMS | Parameter Store | CloudFormation | OpenSearch | Cognito | SNS | CloudWatch | EventBridge | Step Functions | Glue | VPC Endpoint

#### Firebase

Auth | RealtimeDatabase | Firestore | Cloud Messaging

### SaaS/PaaS

GitHub | GitLab | CircleCI

### その他

Terraform | Docker | Jenkins | Chef | nginx | Apache | Tomcat | Webpack | BIND | DHCP | JMeter

## バリューを発揮しやすい業務

- クラウドアーキテクチャ設計
- クラウドインフラ構築管理
- 基盤コード開発
- パッケージマネージャの導入
- LinterやFormatterの導入
- アプリケーションのマイクロサービス化
- サーバーレスアーキテクチャの導入
- 認証サービスの導入
- CDNの導入
- CIサービスの導入
- デプロイの自動化
- コンテナ化(Docker化)
- インフラのコード化
- 負荷試験シナリオ作成
- イベント駆動型アプリケーションの構築
- クラウドの権限管理
- ログ収集の構築

## 主な業務経歴

### 不動産情報検索システムのプロトタイプ開発【React/Express/Fargate/CloudFormation/AWS】(2023年〜現在)

【プロジェクト概要】不動産情報検索のWebアプリケーションのプロトタイプ開発とAWSによる基盤構築

【担当業務】各種Webサービスのインフラの設計構築を担当。具体的には下記。

- クライアントからのヒアリングを行いインフラに関係する要件定義、基本設計、詳細設計、AWS構成図を作成する上流工程担当。AWS構成図を元にAWSの月のコストを算出し、AWS関連の見積書を作成。
- CloudFormationによるインフラのコード化(VPC/Fargate/RDS/ELB/Cognito/WAF/CodePipeline/CodeDeploy等)。可読性の向上やエラーの特定が容易になるように、またリソースの変更やアップデートを行いたい場合に柔軟に対応できるようリソースごとにテンプレートを作成。デプロイメントの順序やテンプレート間の関連性を正確に把握し、パラメーター設定を適切に行うことで複数のテンプレート間でのリソースの相互依存性の問題を解決。
- cfn-lintによるAWS CloudFormationテンプレートの静的解析を行なった実装。
- CodeCommit/CodeDeploy/CodePipelineによるCI/CDパイプラインの構築。buildspec.ymlを作成。buildspec.ymlへは環境変数をParameter Storeから取得できるようにIAMの適切な設定を行う。
- Dockerとdocker-composeの導入によるローカル開発環境構築の迅速化。専用のベースイメージの作成によるDRY化/ローカル開発用と本番用Dockerイメージの切り分け/Cache Mountの活用による不要なnpmパッケージビルドの省略化。
- 運用ドメインの取得。Route53のホストゾーンの設定とサブドメインのDNS設定。
- Amazon ACMによるSSL/TLS証明書の取得。ACMへサブドメインを登録し、サブドメインへHTTPSプロトコルによるアクセスを実現。
- Amazon Cognitoを導入。CognitoカスタムドメインをACMへ設定、ALBとの連携。カスタムドメインによるユーザーのサインイン機能を追加し、Webおよびモバイルアプリケーションへのアクセスを制御。
- pgAdminの導入。pgAdminのSSHトンネルを使用してRDS PostgreSQL DBインスタンスに接続するためのEC2ホストの設定。
- AWS WAFの導入。日本以外からのアクセスを遮断する設定。
- ECSの異常検出のルールの作成とそのルール基づいたCloudWatchアラームを作成。異常検出時にはSNSによる通知の仕組みを構築。
- アプリケーション開発の担当ではなかったが、アプリケーション開発の進捗が予定よりも遅れたため、React/ExpressのSPA構成のデモアプリケーションを作成。デモアプリケーションはFargateの動作検証に使用。
- アプリケーションの検索機能のプロトタイプ開発にも参画。Amazon OpenSearchを使用した日本語のサジェストの機能を実装。

【発揮したバリュー】要件定義、詳細設計を行いクラウドアーキテクチャ設計を行ったO->1フェーズに貢献。フロントエンドとバックエンドの豊富な開発経験によるSPA構成のアプリケーションの雛形を作成してアプリケーション開発にも貢献。インフラのコード化、CI/CDパイプラインの構築など、作業フローの効率化と各種自動化作業等に大きく貢献。

### 接続テストページのプロトタイプ開発【JavaScript/AWS】(2022年)

【プロジェクト概要】利用者の接続環境に問題ないかを診断するための自動テストを行うWebアプリケーションの開発

【担当業務】診断項目の調査、フロントエンド自動テストページの作成、AWSインフラの構築、インフラ構築手順書の作成とインフラのコード化。具体的には下記。

- userAgent/JavaScriptのブラウザ機能のテストの作成
- HTTP/Websoketの通信方式のテストの作成
- WebStrage/Cookieのデータ管理のテストの作成
- CloudFront + API Gateway REST/WebSocket + S3の連携の構築
- AWSインフラのCloudFormationによるコード化

【発揮したバリュー】CloudFront + API Gateway WebSocket + S3の構築例の情報が少なかったが、AWS公式ドキュメントを地道に調査し課題を解決。AWSマネージドサービスの幅広い知識とフロントエンド、バックエンドの開発経験を生かし、運用コストを抑えたサーバレスアプリケーション開発に成功。また短期間での開発要望に応え、開発リードタイムの短縮によってクライアントのサービスの付加価値を高めることに貢献。

### CDN調査【CloudFront/S3】(2022年)

【プロジェクト概要】CDNのキャッシュや圧縮に関する設定を最適化して高速化を行うための調査

【担当業務】CloudFrontキャッシュヒット率の向上の調査、圧縮形式GzipとBrotliの比較調査、プロトコルHTTP/2とHTTP/3の比較調査。具体的には下記。

- CloudFrontディストリビューションの作成
- ビヘイビア（パスパターン）の設定
- CloudFrontポリシーの作成
- プロトコルと圧縮形式の設定の違いによるレスポンス時間の測定

【発揮したバリュー】利用が想定される帯域幅を検証環境で作り、実際の利用時のダウンロード時間を再現し計測。圧縮率が大きかったBrotliの方がレスポンスタイムが高速になることや接続タイムがHTTP/3の方が高速になることも検証結果から確認。キャッシュヒット率の向上のため行ったパスパターンの的確な設定はCloudFrontキャッシュ最適化に貢献。

### EdTechサービスWebアプリケーション開発【Rails/JavaScript】(2022年)

【プロジェクト概要】EdTechサービスのRailsによるバックエンドシステムの機能改善

【担当業務】UIの改善、ビジネスロジックの作成、要件定義、詳細設計、実装、テスト、コードレビュー。具体的には下記。

- テンプレートファイル.slim、.erbによるViewの作成
- Rubyモジュールの作成

【発揮したバリュー】自動計算のモジュールを作成し機能改善に貢献。

### 高負荷Webサービスの負荷試験、性能試験【JMeter/BeanShell/Terraform/AWS】(2022年)

【プロジェクト概要】高負荷Webサービスの品質管理チームにおいて、JMeterを使用したシナリオ作成と負荷試験、性能試験の計測

【担当業務】JMeterシナリオ作成、AWS上にJMeterを使った負荷試験環境の構築、JMeterの計測結果の分析。具体的には下記。

- JMeterとBeanShellを使ったシナリオ作成
- JMeterによる計測結果のグラフの作成
- CloudWatchを使った負荷状況の調査
- MySQLとDynamoDBの連携の調査
- TerraformによるEC2上へJMeter Sever構築のコード化

【発揮したバリュー】JMeterは初体験でありJavaから派生したBeanShellスクリプトを使ったシナリオ作成の情報も少なかったが、書籍やネット情報を地道に調査し、さらにJavaの開発経験を活かして素早く作成方法を習得。計測結果のグラフから機能の改善点が判明し、作業方針の策定に貢献。

### 学校一斉メールWebアプリケーションの開発【Rails/React/TypeScript/Terraform/AWS】(2021年)

【プロジェクト概要】学校から生徒の保護者へ連絡する一斉メールWebアプリケーションのプロトタイプ開発

【担当業務】UIデザインのメンテナンスコストの削減。サービス全体のアーキテクチャ設計、Terraformによるインフラのコード化、各種デプロイスクリプトの作成。具体的には下記。

- Terraformによるインフラのコード化(VPC/Fargate/RDS(MySQL)/CodeBuild/CodePipeline等)
- React+TypeScript+axiosによるフロントエンド部分の実装
- Gmail SMTPサーバーの設定
- Rails APIによるバックエンド部分の実装
- Atomic DesignのデザインパターンによるReactコンポーネントを使用したフロントエンドUIの作成
- RSpecを使ったテストファイル（specファイル）の作成
- AWS CodeBuildとCodePipeline連携によるCI/CDパイプラインの構築

【発揮したバリュー】自らクライアントへ営業を行い、プロトタイプの導入を行う。様々な情報を参考にしてコモディティ化されたマルチAZの構成で可用性を高める冗長化を実現。

### Gmailで受信したメール処理の自動化【Google Apps Script】(2020年)

【プロジェクト概要】生徒の保護者からのメールへ自動返信するスクリプトの開発

【担当業務】メールの自動処理を行うスクリプトの実装。具体的には下記。

- Google Apps Scriptによるスクリプトの実装
- 自動返信テンプレートの作成
- Googleスプレッドシートへデータの自動入力

【発揮したバリュー】自らクライアントへ営業を行い、プロトタイプの導入を行う。クライアントが手動で行っていた業務を自動化することで業務の効率化を実現。

### 通知アプリ管理画面の改修【WordPress/Firebase】(2020年)

【プロジェクト概要】学校から生徒の保護者へ通知するアプリの管理画面のUI改善と機能追加

【担当業務】UIの改善、追加機能の要件定義、詳細設計、実装。具体的には下記。

- 既存WordPress管理画面UIの改善
- WordPressプラグインソフトの開発
- WordPress + Firebase（Cloud Messaging、Auth、Realtime Database） 連携による通知機能の実装

### 学校一斉通知アプリの新規開発【Xamarin】(2020年)

【プロジェクト概要】学校から生徒の保護者へ通知するアプリのプロトタイプ開発

【担当業務】要件定義、詳細設計、実装。具体的には下記。

- Androidアプリ(Xamarin.Android)の実装
- Firebase（Auth、Firestore）連携による通知機能の実装

### 学校一斉メールWindowsデスクトップアプリの新規開発【C#/.NET】(2019年)

【プロジェクト概要】学校から生徒の保護者へ連絡する一斉メールWindowsデスクトップアプリのプロトタイプ開発

【担当業務】要件定義、詳細設計、実装、ユニットテスト、運用マニュアルの作成。具体的には下記。

- MVVMモデルによる実装
- テストツールを利用したテスト駆動開発の実施
- 運用マニュアルのドキュメント作成

### Web制作会社コーポレイトサイトの制作【WordPress】(2018年)

【プロジェクト概要】WordPressテーマのカスタマイズによるWebサイト制作

【担当業務】要件定義、プロジェクト管理、テスト。具体的には下記。

- クラウドソーシングにてデザイナー1名、CSSコーダー1名へ作業発注依頼
- CSSコードレビュー
- デザイナーへUI改善指示
- プロジェクト全体の進捗管理
- 統合テスト

### 起業家&投資家マッチングWebアプリケーションの個人開発【WordPress/AWS】(2017年)

【プロジェクト概要】AWSを利用した起業家&投資家マッチングサイトのWebアプリケーション開発

【担当業務】事業企画、要件定義、詳細設計、実装、UI設計、AWS構築とデプロイ作業、運用。具体的には下記。

- WordPressテーマカスタマイズによるUI設計と機能実装
- AWSコンソール画面からAWS（EC2、VPC、S3、Lambda、Route53、IAM、RDS(MySQL)、SES）構築
- EC2へWebアプリケーションをデプロイ
- AWSでの運用（運用期間3ヶ月）

### 学校ホームページの改修【WordPress】(2017年)

【プロジェクト概要】WordPress導入による学校ホームページ更新の効率化

【担当業務】改修案の作成、要件定義、詳細設計、実装、UI設計、操作マニュアル作成。具体的には下記。

- WordPress導入
- WordPressテーマカスタマイズによるUI設計と機能実装
- レスポンシブWebデザインへUIを更新
- WordPress管理画面捜査の説明とマニュアル化

### 小売業商品発注システムAndroidアプリのプロトタイプ開発【Android/Java】(2016年)

【プロジェクト概要】小売業にBYOD導入実施を行うための商品発注モバイルアプリのプロトタイプ開発

【担当業務】アプリ導入の提案書作成、要件定義、詳細設計、実装、UI設計。具体的には下記。

- アプリ開発全般
- 2次元コードの作成／読取のオープンソースZXingの組み込み
- Filebase（Auth、Realtime Database）のMBaaS/BaaSを利用したデータベースを構築

### 料理動画学習Webアプリケーションの個人開発【Linux CentOS/Ruby on Rails/Git/Vagrant】(2015年)

【プロジェクト概要】Ruby on Railsを利用した料理動画Webアプリケーション開発

【担当業務】事業企画、要件定義、詳細設計、実装、UI設計、CI/CD導入、運用、コンテンツ制作。具体的には下記。

- Ruby on RailsのMVCモデルによるアプリケーション開発全般
- VPS（仮想専用サーバー）へCentOSを導入
- CentOSへミドルウェア（Apache、Bind、Sendmail、MySQL）を構築
- CI/CD導入（Vagrant、Chef、Jenkins利用）
- 料理動画のコンテンツ制作

### 語学学習アプリの個人開発【Android/Java】(2012年)

【プロジェクト概要】語学学習Androidアプリ開発

【担当業務】要件定義、詳細設計、実装、UI設計、運用、AdMobの導入。具体的には下記。

- Android StudioによるAndroidアプリ開発全般
- AdMobの導入による広告収入を得るめの戦略の立案
