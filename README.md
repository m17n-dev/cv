# 業務経歴書

## 基本情報

|key|value|
|----|----|
|名前|瀬野 哲朗|
|ポートフォリオ|[myrails-react-todo-v4](https://github.com/m17n-dev/myrails-react-todo-v4)(Rails API + React)|
|ポートフォリオ|[BookSearchWpfApp](https://github.com/m17n-dev/BookSearchWpfApp)(.NET Framework)|
|Twitter|[@m17n_dev](https://twitter.com/m17n_dev)|
|Qiita|[@m17n_dev](https://qiita.com/m17n_dev) 

## 概要

- バックエンドの複数の言語/DB/フレームワークを用いた開発経験、AWSの多数のマネージドサービスの開発経験があります。（フロントエンド開発、Androidアプリ開発、Windows系では.NET系の開発も多数経験しておりますが現在はLinuxプラットフォームでの開発がメインです）

- 小規模〜中規模サービスの新規開発フェーズを多く経験してきました。サービスのアーキテクチャ設計の段階から参画させて頂くことでバリューを発揮できるエンジニアだと思います。

## スキル
基本的にすべて実業務で使用した技術だけを列挙しています。

### 言語
Java | Ruby | Python | PHP | Perl | JavaScript | TypeScript | VC++ | C# | Google Apps Script

### フレームワーク等
Express | Struts | Ruby on Rails | CakePHP | jQuery | React.js | MFC | .NET Framework | RSpec

### RDB/NoSQL
MySQL | PostgreSQL | Oracle | SQL Server | DynamoDB

### クラウド

#### AWS

VPC | S3 | CloudFront | API Gateway | Lambda | ELB | ECR | CodeBuild | CodePipline | EC2 | ECS | Fargate | Route53 | ACM | IAM | RDS(MySQL) | DynamoDB | Kinesis firehose | SES | KMS | SSM | CloudFormation

#### Firebase

Auth | RealtimeDatabase | Firestore | Cloud Messaging

### SaaS/PaaS
GitHub | GitLab | CircleCI

### その他
Terraform | Docker | Jenkins | Chef | nginx | Apache | Tomcat | Webpack | BIND | DHCP | JMeter

## バリューを発揮しやすい業務

- クラウドアーキテクチャ設計
- CIサービスの導入
- コンテナ化(Docker化)
- インフラのコード化
- 負荷試験シナリオ作成

## 主な業務経歴

### 接続テストページの作成【JavaScript/AWS】
【プロジェクト概要】利用者の接続環境に問題ないかを診断するための自動テストを行うWebアプリケーションの開発を担当(2022年)

【担当業務】診断項目の調査、フロントエンド自動テストページの作成、AWSインフラの構築、インフラ構築手順書の作成とインフラのコード化。具体的には下記。

- userAgent/JavaScriptのブラウザ機能のテストの作成
- HTTP/Websoketの通信方式のテストの作成
- WebStrage/Cookieのデータ管理のテストの作成
- CloudFront + API Gateway REST/WebSocket + S3の連携の構築
- AWSインフラのCloudFormationによるコード化

【発揮したバリュー】CloudFront + API Gateway WebSocket + S3の構築例の情報が少なかったが、AWS公式ドキュメントを地道に調査し課題を解決。AWSマネージドサービスの幅広い知識とフロントエンド、バックエンドの開発経験を生かし、運用コストを抑えたアプリケーション開発に成功。また短期間での開発要望に応え、開発リードタイムの短縮によってクライアントのサービスの付加価値を高めることに貢献。

### CDN調査【CloudFront/S3】
【プロジェクト概要】CDNのキャッシュや圧縮に関する設定を最適化して高速化を行うための調査を担当(2022年)

【担当業務】CloudFrontキャッシュヒット率の向上の調査、圧縮形式GzipとBrotliの比較調査、プロトコルHTTP/2とHTTP/3の比較調査。具体的には下記。

- CloudFrontディストリビューションの作成
- ビヘイビア（パスパターン）の設定
- CloudFrontポリシーの作成
- プロトコルと圧縮形式の設定の違いによるレスポンス時間の測定

【発揮したバリュー】利用が想定される帯域幅を検証環境で作り、実際の利用時のダウンロード時間を再現し計測。圧縮率が大きかったBrotliの方がレスポンスタイムが高速になることや接続タイムがHTTP/3の方が高速になることも検証結果から確認。キャッシュヒット率の向上のため行ったパスパターンの的確な設定はCloudFrontキャッシュ最適化に貢献。

### EdTechサービスWebアプリケーション開発【Rails/JavaScript】
【プロジェクト概要】EdTechサービスのRailsによるバックエンドシステムの機能改善を担当(2022年)

【担当業務】UIの改善、ビジネスロジックの作成、要件定義、詳細設計、実装、テスト、コードレビュー。具体的には下記。

- テンプレートファイル.slim、.erbによるViewの作成
- Rubyモジュールの作成

【発揮したバリュー】自動計算のモジュールを作成し機能改善に貢献。

### 高負荷Webサービスの負荷試験、性能試験【JMeter/BeanShell/Terraform/AWS】

【プロジェクト概要】高負荷Webサービスの品質管理チームにおいて、JMeterを使用したシナリオ作成と負荷試験、性能試験の計測を担当(2022年)

【担当業務】JMeterシナリオ作成、AWS上にJMeterを使った負荷試験環境の構築、JMeterの計測結果の分析。具体的には下記。

- JMeterとBeanShellを使ったシナリオ作成
- JMeterによる計測結果のグラフの作成
- CloudWatchを使った負荷状況の調査
- MySQLとDynamoDBの連携の調査
- TerraformによるEC2上へJMeter Sever構築のコード化

【発揮したバリュー】JMeterは初体験でありJavaから派生したBeanShellスクリプトを使ったシナリオ作成の情報も少なかったが、書籍やネット情報を地道に調査し、さらにJavaの開発経験を活かして素早く作成方法を習得。計測結果のグラフから機能の改善点が判明し、作業方針の策定に貢献。


### 学校一斉メールWebアプリケーションの開発【Rails/React/TypeScript/Terraform/AWS】

【プロジェクト概要】学校から生徒の保護者へ連絡する一斉メールWebアプリケーションのプロトタイプ開発(2021年)

【担当業務】UIデザインのメンテナンスコストの削減。サービス全体のアーキテクチャ設計、Terraformによるインフラのコード化、各種デプロイスクリプトの作成。具体的には下記。

- Terraformによるインフラのコード化(VPC/Fargate/RDS(MySQL)/CodeBuild/CodePipeline等)
- React+TypeScript+axiosによるフロントエンド部分の実装
- Rails APIによるバックエンド部分の実装
- Atomic DesignのデザインパターンによるReactコンポーネントを使用したフロントエンドUIの作成
- RSpecを使ったテストファイル（specファイル）の作成
- AWS CodeBuildとCodePipeline連携によるCI/CDパイプラインの構築

【発揮したバリュー】自らクライアントへ営業を行い、プロトタイプの導入を行う。様々な情報を参考にしてコモディティ化されたマルチAZの構成で可用性を高める冗長化を実現。

