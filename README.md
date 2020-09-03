# CircleCI ✖︎ AWSでCI/CDを体験しよう！！

## はじめに
### CI/CDとは

CI/CDとは高度な継続的自動化と継続的監視をアプリケーション開発に取り組むこと、また、そのプロセスのこと

![image](https://user-images.githubusercontent.com/66664167/92073666-39264f00-edef-11ea-8e05-c9db7127b3e9.png)

<br>
<br>

### - 継続的インテグレーション　-

>継続的インテグレーションは、コードを共有リポジトリの master ブランチに常時頻繁に統合することを奨励する開発手法です。それぞれの機能を個別にビルドして、開発サイクルの最後に統合するのではなく、各開発者のコードが 1 日に何度も共有リポジトリに統合されます。
>すべての開発者が共有メインラインに毎日コミットします。コミットされるたびに、自動化されたビルドとテストがトリガーされます。ビルドやテストが失敗しても、数分以内にすばやく修復できます。
>チームの生産性、効率、満足度を向上させます。 問題をすばやく検出して解決できます。 より高品質で安定したプロダクトをリリースできます。
<br>
※　CircleCi公式ドキュメントより：https://circleci.com/docs/ja/2.0/about-circleci/#section=welcome
<br>

![image](https://user-images.githubusercontent.com/66664167/92101045-83232b00-ee17-11ea-89d9-38ee6caee2df.png)

<br>
※　技術評論社より：https://gihyo.jp/book/pickup/2015/0045
<br>

### - 継続的デリバリー -
>検証されたコードのリポジトリへのリリースを自動化します。継続的デリバリーの目標は、本番環境にデプロイできるコードベースを常に保持しておくことです。
継続的デリバリーでは、コード変更のマージから本番環境対応のビルドのデリバリーまで、すべてのステージでテストの自動化とコードリリースの自動化が実施されます。このプロセスの終了時には、運用チームはアプリケーションを本番環境にすばやく簡単にデプロイできます。
<br>

### - 継続的デプロイメント -
>成熟した CI/CD パイプラインの最終ステージは、継続的デプロイメントです。本番環境対応のビルドをコードリポジトリへ自動的にリリースする継続的デリバリーの延長として、継続的デプロイメントはアプリケーションを本番環境に自動的にリリースします。本番環境に移す前のパイプラインのステージでは手動でのチェックはないので、継続的デプロイメントは主に、入念に設計されたテスト自動化を活用します。
<br>
<br>

## なぜCI/CDなのか？
#### ・自動化テストの重要性の高まり<br>
これだけソフトウェアが普及していくと、品質に対する要求も高くなり、今まで手動でテストしていた分野でも積極的に自動化テストを取り入れるようになってきます。なぜならCI/CDを使うと、コードの変更が発生するたびに自動でテストが行われるので、テストの実行忘れや、環境依存のテストを失くすことでの品質を向上させることができるからです。

#### ・アジャイル開発のプラクティスの浸透と進化<br>
アジャイル開発で重要なことはスピードです。より小さな粒度の変更をいかに早くテスト／リリースしてフィードバックを得るかがアジャイル開発の成功の鍵となりますが、CI/CDを使うことでこれらを実現することができます。
<br>
<br>

## CI/CDツール選定
### Jenkins
#### - メリット - <br>
- 拡張性が高い。プロジェクトに合わせてカスタマイズしやすい
- オンプレ上に構築するため、IPが固定される
- ドキュメントが豊富で調査しやすい

#### - デメリット - <br>
- サーバを用意する必要があるため、費用がかかる、準備に時間がかかる
- 本番を含めワークフローに組み込むため、導入は計画的に行う必要がある
- 保守・運用が必要なため管理を怠ると属人化しやすい

### TravisCI
#### - メリット - <br>
- Cloudであるため、サーバの管理・運用は不要になる
- Githubとの親和性高い
- ドキュメントが豊富で調査しやすい

#### - デメリット - <br>
- コンテナにsshで入れないのでデバッグしにくい
- $129がかかるため、CIをはじめて導入する際には提案しにくい
- Cloudなのでビルドの度にIPが変わる

### CircleCI
#### - メリット - <br>
- Cloudであるため、サーバの管理・運用は不要
- 公式のサポートが手厚い
- ドキュメントが豊富で調査しやすい
- sshでコンテナに入れるので、デバッグしやすい
- 無料で使い始められる

#### - デメリット - <br>
- Clouldなのでビルドの度に毎回IPが変わる
- GitHubまたはBitbucketとの連携が前提
<br>
<br>

## ★　Hands-On　★

### 1.目的
### 2.今日のゴール
### 3.環境・言語
### 4.事前準備
- AWS アカウント作成
- AWS EC2インスタンの起動、Elastic IPの設定
- Docker　インストール
- docker-compose インストール
- GitHub アカウント作成




CI/CD パイプラインのさまざまなテストおよびリリースステージに合わせて自動化されたテストを作成する必要があるため、まとまった事前の投資も必要です。

