# CodeIgniter4 まとめ

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [最近の動向](#%E6%9C%80%E8%BF%91%E3%81%AE%E5%8B%95%E5%90%91)
- [本家](#%E6%9C%AC%E5%AE%B6)
- [公式マニュアル](#%E5%85%AC%E5%BC%8F%E3%83%9E%E3%83%8B%E3%83%A5%E3%82%A2%E3%83%AB)
- [コミュニティ](#%E3%82%B3%E3%83%9F%E3%83%A5%E3%83%8B%E3%83%86%E3%82%A3)
- [脆弱性情報](#%E8%84%86%E5%BC%B1%E6%80%A7%E6%83%85%E5%A0%B1)
- [問題](#%E5%95%8F%E9%A1%8C)
- [開発環境の構築](#%E9%96%8B%E7%99%BA%E7%92%B0%E5%A2%83%E3%81%AE%E6%A7%8B%E7%AF%89)
  - [Docker](#docker)
  - [アップデートツール](#%E3%82%A2%E3%83%83%E3%83%97%E3%83%87%E3%83%BC%E3%83%88%E3%83%84%E3%83%BC%E3%83%AB)
  - [IDE](#ide)
  - [その他](#%E3%81%9D%E3%81%AE%E4%BB%96)
- [インストール](#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
  - [アプリケーションテンプレート](#%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88)
- [チュートリアル](#%E3%83%81%E3%83%A5%E3%83%BC%E3%83%88%E3%83%AA%E3%82%A2%E3%83%AB)
- [コントローラ](#%E3%82%B3%E3%83%B3%E3%83%88%E3%83%AD%E3%83%BC%E3%83%A9)
  - [ルーティング](#%E3%83%AB%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)
  - [REST API](#rest-api)
- [モデル](#%E3%83%A2%E3%83%87%E3%83%AB)
  - [CodeIgniter Model](#codeigniter-model)
  - [データベース](#%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9)
- [ビュー](#%E3%83%93%E3%83%A5%E3%83%BC)
  - [テンプレートエンジン](#%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%B3)
- [テスト](#%E3%83%86%E3%82%B9%E3%83%88)
  - [PHPUnit](#phpunit)
  - [モック](#%E3%83%A2%E3%83%83%E3%82%AF)
  - [フィーチャーテスト](#%E3%83%95%E3%82%A3%E3%83%BC%E3%83%81%E3%83%A3%E3%83%BC%E3%83%86%E3%82%B9%E3%83%88)
- [コード生成](#%E3%82%B3%E3%83%BC%E3%83%89%E7%94%9F%E6%88%90)
- [CLI コマンド](#cli-%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89)
- [CodeIgniter3 からの移行](#codeigniter3-%E3%81%8B%E3%82%89%E3%81%AE%E7%A7%BB%E8%A1%8C)
- [デバッグ](#%E3%83%87%E3%83%90%E3%83%83%E3%82%B0)
- [フレームワーク内部](#%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AF%E5%86%85%E9%83%A8)
- [フレームワークの拡張](#%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AF%E3%81%AE%E6%8B%A1%E5%BC%B5)
- [ライブラリ](#%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA)
  - [公式](#%E5%85%AC%E5%BC%8F)
  - [認証](#%E8%AA%8D%E8%A8%BC)
  - [データベース](#%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9-1)
  - [ロギング](#%E3%83%AD%E3%82%AE%E3%83%B3%E3%82%B0)
  - [REST](#rest)
  - [JavaScript/CSS](#javascriptcss)
  - [Captcha](#captcha)
- [アプリケーション](#%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3)
- [書籍](#%E6%9B%B8%E7%B1%8D)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 最近の動向
- 2022-02-26 CodeIgniter [v4.1.9](https://codeigniter4.github.io/userguide/changelogs/v4.1.9.html) リリース
  - 脆弱性情報 [Remote CLI Command Execution Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-xjp4-6w75-qrj7)
  - 脆弱性情報 [Cross-Site Request Forgery (CSRF) Protection Bypass Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-4v37-24gm-h554)
- 2022-01-25 CodeIgniter [v4.1.8](https://codeigniter4.github.io/userguide/changelogs/v4.1.8.html) リリース
  - 脆弱性情報 [XSS Vulnerability in API\ResponseTrait in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-7528-7jg5-6g62)
- 2022-01-10 CodeIgniter [v4.1.7](https://codeigniter4.github.io/userguide/changelogs/v4.1.7.html) リリース
- 2022-01-04 [CodeIgniter v4.1.6 released](https://forum.codeigniter.com/thread-80926.html)
  - PHP 8.1 をサポート
  - 脆弱性情報 [Deserialization of Untrusted Data in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-w6jr-wj64-mc9x)
- 2021-11-23 CodeIgniter 4 Settings [v2.1.0](https://github.com/codeigniter4/settings/releases/tag/v2.1.0) リリース
- 2021-11-08 [CodeIgniter v4.1.5 released](https://forum.codeigniter.com/thread-80494.html)
- 2021-09-07 [CodeIgniter v4.1.4 released](https://forum.codeigniter.com/thread-80045-post-389804.html)
  - PSR-12 ベースの [新しいコーディング標準](https://github.com/CodeIgniter/coding-standard) への変更
- 2021-06-06 [CodeIgniter v4.1.3 released](https://forum.codeigniter.com/thread-79373.html)
- 2021-05-18 [CodeIgniter v4.1.2 released](https://forum.codeigniter.com/thread-79249.html)
- 2021-02-02 [CodeIgniter 4.0.5と4.1.1がリリースされました](http://blog.a-way-out.net/blog/2021/02/02/codeigniter-405-and-411-released/)
  - PHP 8.0 をサポート
  - 4.0.5 は PHP 7.2 をサポートする最後のバージョン
  - 4.1.0 は PHP 7.3 以上が必要
- 2020-07-16 [CodeIgniter v4.0.4 released](https://forum.codeigniter.com/thread-77054.html)

## 本家
- CodeIgniter 公式サイト http://codeigniter.com/
- リポジトリ
  - 開発 https://github.com/codeigniter4/CodeIgniter4
  - システムメッセージ翻訳 https://github.com/codeigniter4/translations
- バグトラッカー https://github.com/codeigniter4/CodeIgniter4/issues
- [CodeIgniter4の開発に参加する](http://blog.a-way-out.net/blog/2020/12/22/join-codeigniter4-development/)

## 公式マニュアル
- リリース版 https://codeigniter4.github.io/userguide/
- 開発版 https://codeigniter4.github.io/CodeIgniter4/
- [開発版 Google翻訳](https://codeigniter4-github-io.translate.goog/CodeIgniter4/intro/index.html?_x_tr_sl=en&_x_tr_tl=ja&_x_tr_hl=ja)

※ 最新の英語の開発版を（必要なら翻訳して）参照することを推奨します。ググると日本語のユーザーガイドがヒットするかも知れませんが、古いものほど原文に誤りや不備が多いため注意してください。

## コミュニティ
- 本家フォーラム http://forum.codeigniter.com/
- 本家 Slack https://codeigniterchat.slack.com/
- Stack Overflow https://stackoverflow.com/questions/tagged/codeigniter-4
- 日本 CodeIgniter ユーザ会 http://codeigniter.jp/
- Qiita https://qiita.com/tags/codeigniter4

## 脆弱性情報
- [Remote CLI Command Execution Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-xjp4-6w75-qrj7)
- [Cross-Site Request Forgery (CSRF) Protection Bypass Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-4v37-24gm-h554)
  - 〜v4.1.8
  - v4.1.9 で修正済み
- [XSS Vulnerability in API\ResponseTrait in CodeIgniter4 ](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-7528-7jg5-6g62)
  - 〜v4.1.7
  - v4.1.8 で修正済み
- [Deserialization of Untrusted Data in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-w6jr-wj64-mc9x)
  - 〜v4.1.5
  - v4.1.6 で修正済み

## 問題
- v4.1.6
  - [Bug: ErrorException: Undefined index: file: SYSTEMPATH\Debug\Toolbar\Collectors\Database.php at line 142 #5539](https://github.com/codeigniter4/CodeIgniter4/issues/5539) ... 4.1.7 で修正済み
  - [Bug: Debug bar javascript issue with external script toggle #5541](https://github.com/codeigniter4/CodeIgniter4/issues/5541) ... 4.1.7 で修正済み
  - [Bug: BaseConnection::getConnectDuration() number_format(): Passing null to parameter #5535](https://github.com/codeigniter4/CodeIgniter4/issues/5535) ... 4.1.7 で修正済み
- [getCompiledSelect の罠、 useSoftDelete が抜け落ちる - Qiita](https://qiita.com/bananacoffee/items/0aff3f5cd005a5f1bfc6)
- Redis セッションのバグ
  - v4.1.4
  - v4.1.5 で修正済み
    - https://github.com/codeigniter4/CodeIgniter4/pull/5062
- [データベースセッションのバグ](https://github.com/codeigniter4/CodeIgniter4/issues/4807)
  - v4.1.2〜v4.1.4
  - v4.1.5 で修正済み
    - https://github.com/codeigniter4/CodeIgniter4/pull/4876
    - https://github.com/codeigniter4/CodeIgniter4/pull/5060
- 環境変数名にドットが使えない環境がある
  - 〜v4.1.4
  - v4.1.5 で対応済み
    - https://github.com/codeigniter4/CodeIgniter4/pull/5156
    - https://github.com/codeigniter4/CodeIgniter4/issues/4026

## 開発環境の構築

### Docker
- [koolを使いCodeIgniter4の開発環境を構築する](https://zenn.dev/kenjis/articles/c9aecb9d3fd004)
- [codeigniter4-dockerでCodeIgniter4の開発環境を作成してみる](http://blog.a-way-out.net/blog/2020/12/08/codeigniter4-docker/)
- [kenjis/docker-codeigniter-apache: Build a simple CodeIgniter development environment with docker-compose.](https://github.com/kenjis/docker-codeigniter-apache)

### アップデートツール
- [tattersoftware/codeigniter4-patches: Automated project updates for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-patches)
- [paulbalandan/liaison-revision: Seamless software updates library for CodeIgniter4 projects.](https://github.com/paulbalandan/liaison-revision)

### IDE
- [PhpStorm](https://www.jetbrains.com/ja-jp/phpstorm/)
- [CodeIgniter Plugins for Visual Studio Code](https://marketplace.visualstudio.com/search?term=codeigniter&target=VSCode&category=All%20categories&sortBy=Relevance)

### その他
- [SDPM-lab/Codeigniter4-Roadrunner: Make Codeigniter4 work on Roadrunner Server.](https://github.com/SDPM-lab/Codeigniter4-Roadrunner)

## インストール
- [CodeIgniter 4.1のインストール方法【2021年最新版】](https://zenn.dev/kenjis/articles/9a68c7fdbd5aaa)
- [CodeIgniter 4.0を開発版にアップデートする](
  http://blog.a-way-out.net/blog/2020/12/30/update-codeigniter-404/)
- [CodeIgniter4をインストール (Composer利用) - Qiita](https://qiita.com/kohenji01/items/a36dbbbb19bb8808d104)
- [1つのCodeigniterで複数サイト（例：フロントと管理画面）を運用する - Qiita](https://qiita.com/bananacoffee/items/ca7784ebe0d2d5a320d1)
- [CodeIgniter4で新しいCI_ENVIRONMENTを定義する](https://zenn.dev/kenjis/articles/24ff7332d32837)

### アプリケーションテンプレート
- [kenjis/ci4-app-template: CodeIgniter4 application template](https://github.com/kenjis/ci4-app-template)
- [lonnieezell/Bonfire2: CodeIgniter 4-based application skeleton](https://github.com/lonnieezell/Bonfire2)

## チュートリアル
- [CodeIgniter4入門 公式チュートリアル](https://zenn.dev/kenjis/articles/3d5e42f872ff18)
- [CodeIgniter 4 最速マスター](https://zenn.dev/kenjis/articles/811ee63e3fec59)
- [Learn CodeIgniter](https://learncodeigniter.net/)
- [CodeIgniter 4 Tutorials - Best Place to Learn CodeIgniter 4](https://onlinewebtutorblog.com/category/codeigniter-4/)
- 多言語化
  - Creating a multilingual website with CodeIgniter 4 
    - https://includebeer.com/en/blog/creating-a-multilingual-website-with-codeigniter-4-part-1
    - https://includebeer.com/en/blog/creating-a-multilingual-website-with-codeigniter-4-part-2

## コントローラ

### ルーティング
- [CodeIgniter4のルーティング](https://zenn.dev/kenjis/articles/139208ac5e38c9)
- [【改訂版】本当は危ないCodeIgniter4の自動ルーティング](http://blog.a-way-out.net/blog/2022/02/08/really-dangerous-codeigniter4-auto-routing/)
- [kenjis/ci4-attribute-routes: CodeIgniter4 Attribute Routes](https://github.com/kenjis/ci4-attribute-routes)

### REST API
- [CodeIgniter4でREST APIを作成する](http://blog.a-way-out.net/blog/2020/12/20/codeigniter4-rest-api/)
- [CodeIgniterとJSON Web Tokenを使用したセキュアなRESTful APIの構築方法](https://www.twilio.com/blog/create-secured-restful-api-codeigniter-php-jp)

## モデル

- [CodeIgniter\Modelを使わない場合](https://zenn.dev/kenjis/articles/31526cefe34f0c)

### CodeIgniter Model
- [CodeIgniter4のCodeIgniter\Model](https://zenn.dev/kenjis/articles/6fa2af22ba4a5c)
- [CodeIgniter4のModelまわり | BITTER GOURD](https://ittan-dev.net/php/codeigniter4-models-try/)
- [CodeIgniter4のModelの基礎 - Qiita](https://qiita.com/kohenji01/items/b3e947623309d478e02b)
- [CodeIgniter ModelはQuery Builderを直接呼べるのでわかりづらい](https://forum.codeigniter.com/thread-75871-post-373699.html#pid373699)
- [CodeIgniter 4 Models vs Query Builder - Learn CodeIgniter](https://learncodeigniter.net/codeigniter-tutorials/codeigniter-4-models-vs-query-builder/)
- [getCompiledSelect の罠、 useSoftDelete が抜け落ちる - Qiita](https://qiita.com/bananacoffee/items/0aff3f5cd005a5f1bfc6)

#### CodeIgniter Model 関連パッケージ
- [tattersoftware/codeigniter4-relations: Entity relationships for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-relations)
- [tattersoftware/codeigniter4-roster: Bulk name lookup for database relations](https://github.com/tattersoftware/codeigniter4-roster)
- [tattersoftware/codeigniter4-permits: Dynamic permission handling for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-permits)
- [tattersoftware/codeigniter4-audits: Lightweight object logging for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-audits)

### データベース
- [CodeIgniter4 のクエリビルダ `$builder->selectXXX()` は第2引数にAS句を指定できる - Qiita](https://qiita.com/bananacoffee/items/d5fe9ecb2679e4f9f236)
- [Databaseクラスを拡張する方法](https://forum.codeigniter.com/thread-78294-post-383813.html#pid383813)
- [SQL文をQuery Builderに変換するサービス: SQL To Codeigniter Builder](https://sql-to-ci-builder.herokuapp.com/)

#### データベースマイグレーション
- [CodeIgniter4のデータベースマイグレーション](http://blog.a-way-out.net/blog/2020/12/12/codeigniter4-database-migrations/)

#### データベースシーディング
- [CodeIgniter4のデータベースシーダー](http://blog.a-way-out.net/blog/2020/12/13/codeigniter4-database-seeder/)

## ビュー
- [CodeIgniter4のViewの基礎 - Qiita](https://qiita.com/kohenji01/items/44dc6c72077c0a9ec366)
- [Codeigniterのview in viewには引数はなくてもいい - Qiita](https://qiita.com/bananacoffee/items/5efac3a9d8b243922d2a)
- [Codeigniter 4 でビューを変数に代入するときにデバッグコードが出ないようにする - Qiita](https://qiita.com/bananacoffee/items/7b9b86c56609449ae219)

### テンプレートエンジン
- [CodeIgniter4でTwigを使ってみる](http://blog.a-way-out.net/blog/2020/12/10/codeigniter4-twig/)
- [CodeIgniter4でSmartyを使う(Composer利用) - Qiita](https://qiita.com/kohenji01/items/bcf4832af61e0e0c446f)

## テスト

### PHPUnit
- [$this->getDouble()を使いたい](https://github.com/kenjis/phpunit-helper)

### モック
- [認証をモックしたい](https://github.com/tattersoftware/codeigniter4-imposter)

### フィーチャーテスト
- [CodeIgniter4のフィーチャーテスト](http://blog.a-way-out.net/blog/2020/12/14/codeigniter4-feature-testing/)

## コード生成
- [CodeIgniter4のコードジェネレータ](http://blog.a-way-out.net/blog/2020/12/07/codeigniter4-cli-generators/)

## CLI コマンド
- [CodeIgniter4でCLIコマンドを作成する](http://blog.a-way-out.net/blog/2020/12/18/create-codeigniter4-cli-commands/)

## CodeIgniter3 からの移行
- [CodeIgniter 3.1と4.1の違い](https://zenn.dev/kenjis/articles/cc1c76ebc2a15b)
- [Codeigniter3で使っていたアレをCodeigniter4で使う - Qiita](https://qiita.com/bananacoffee/items/6bb631391c2301d28c73)
- [kenjis/ci3-to-4-upgrade-helper: CodeIgniter 3 to 4 Upgrade Helper](https://github.com/kenjis/ci3-to-4-upgrade-helper)

## デバッグ
- [CodeIgniter4でdd()を使う](https://zenn.dev/kenjis/articles/8a3e763d518db0)
- [CodeIgniter4でChrome Loggerを使う](https://zenn.dev/kenjis/articles/66d29306dd91a6)
- [PhpStormとXdebug3でCodeIgniter4をステップ実行する](http://blog.a-way-out.net/blog/2020/12/24/step-debugging-codeigniter4-with-phpstorm-and-xdebug3/)
- [The checklist of things to check when your CodeIgniter 4 web application is not working](https://includebeer.com/en/blog/the-checklist-of-things-to-check-when-your-codeigniter-4-web-application-is-not-working)

## フレームワーク内部
- [CodeIgniter4のアプリケーションフローチャート](https://zenn.dev/kenjis/articles/c8a19f61d62f24)
- [CodeIgniter 4.1の処理の流れ](http://blog.a-way-out.net/blog/2021/02/19/codeigniter41-process-flow/)

## フレームワークの拡張
- [CodeIgniter4でMonologを使う](http://blog.a-way-out.net/blog/2021/09/16/codeigniter4-monolog/)
- [[実践CodeIgniter4]第1回：Viewクラスの拡張 | ATTRIBUTE ERROR...](https://www.attribute-error.jp/column/%5B%E5%AE%9F%E8%B7%B5CodeIgniter4%5D%E7%AC%AC1%E5%9B%9E%EF%BC%9AView%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AE%E6%8B%A1%E5%BC%B5)
- [コントローラの生成をDIコンテナ経由にする](https://github.com/kenjis/ci4-tettei-apps/pull/4)

## ライブラリ

### 公式
- [codeigniter4/settings: Settings Library for CodeIgniter 4](https://github.com/codeigniter4/settings)
- [codeigniter4/cache: PSR-6 and PSR-16 Cache Adapters for CodeIgniter 4](https://github.com/codeigniter4/cache)

### 認証
- [lonnieezell/myth-auth: One-stop Auth package for CodeIgniter 4](https://github.com/lonnieezell/myth-auth)
  - [CodeIgniter4の認証ライブラリMyth Authを使う](https://zenn.dev/kenjis/articles/95f38b7e447155)
- [benedmunds/CodeIgniter-Ion-Auth at 4](https://github.com/benedmunds/CodeIgniter-Ion-Auth/tree/4)
- [lonnieezell/codeigniter-shield: Authentication and Authorization for CodeIgniter 4](
  https://github.com/lonnieezell/codeigniter-shield)

### データベース
- [daycry/doctrine: Doctrine for Codeigniter 4](https://github.com/daycry/doctrine)
- [Illuminate Database Wrapper for CodeIgniter 4](https://github.com/nfaiz/dbtoolkit)

### ロギング
- [ajmeireles/ci4-sentry: Sentry Integration with CodeIgniter 4](https://github.com/ajmeireles/ci4-sentry)

### REST
- [daycry/restserver: Rest Server for Codeigniter 4](https://github.com/daycry/restserver)

### JavaScript/CSS
- [michalsn/minifier: Asset minification and versioning library for CodeIgniter 4](https://github.com/michalsn/minifier)
- [tattersoftware/codeigniter4-assets: Asset handling for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-assets)

### Captcha
- [kenjis/ci3-like-captcha - Packagist](https://packagist.org/packages/kenjis/ci3-like-captcha)
- [Integrate Google ReCaptcha v3 in CodeIgniter 4](http://denis303.com/blog/1-integrate-google-recaptcha-v3-in-codeigniter4)
  - https://forum.codeigniter.com/thread-75779.html
  - https://github.com/denis303/codeigniter4-recaptcha
- [gregwar/captcha - Packagist](https://packagist.org/packages/gregwar/captcha)
- [laminas/laminas-captcha - Packagist](https://packagist.org/packages/laminas/laminas-captcha)

## アプリケーション
- [『CodeIgniter徹底入門』のサンプルアプリケーション （CodeIgniter v4.1版） ](https://github.com/kenjis/ci4-tettei-apps)
- [CodeIgniter Website](https://github.com/codeigniter4projects/website)
- [samsonasik/ci4-album: 🔥 CodeIgniter 4 example Album module uses Domain Driven Design Architecture with Tactical Pattern](https://github.com/samsonasik/ci4-album)

## 書籍
- [CodeIgniter 4 Foundations](https://leanpub.com/codeigniter4foundations) by Lonnie Ezell
- [CodeIgniter 4 Foundations](https://www.amazon.co.jp/dp/B09MJ9RWN9) ペーパーバック
