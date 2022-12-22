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
  - [IDE](#ide)
  - [その他](#%E3%81%9D%E3%81%AE%E4%BB%96)
- [インストール](#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
  - [アプリケーションテンプレート](#%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88)
- [アップグレード](#%E3%82%A2%E3%83%83%E3%83%97%E3%82%B0%E3%83%AC%E3%83%BC%E3%83%89)
- [設定](#%E8%A8%AD%E5%AE%9A)
- [チュートリアル](#%E3%83%81%E3%83%A5%E3%83%BC%E3%83%88%E3%83%AA%E3%82%A2%E3%83%AB)
- [基本概念](#%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5)
  - [Services](#services)
  - [Factories](#factories)
  - [Code Modules](#code-modules)
- [コントローラ](#%E3%82%B3%E3%83%B3%E3%83%88%E3%83%AD%E3%83%BC%E3%83%A9)
  - [ルーティング](#%E3%83%AB%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)
  - [REST API](#rest-api)
  - [バリデーション](#%E3%83%90%E3%83%AA%E3%83%87%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3)
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
  - [多言語化](#%E5%A4%9A%E8%A8%80%E8%AA%9E%E5%8C%96)
  - [JavaScript/CSS](#javascriptcss)
  - [Reactive](#reactive)
  - [Queue](#queue)
  - [Captcha](#captcha)
  - [Long-living PHP](#long-living-php)
  - [Serverless](#serverless)
- [アプリケーション](#%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3)
- [書籍](#%E6%9B%B8%E7%B1%8D)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 最近の動向
- 2022-12-22 CodeIgniter 4.2.11 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.11.html))
  - 脆弱性情報 [Attackers may spoof IP address when using proxy ](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-ghw3-5qvm-3mqc)
  - 脆弱性情報 [Potential Session Handlers Vulnerability](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-6cq5-8cj7-g558)
- 2022-12-22 CodeIgniter DevKit [1.1.1 リリース](https://github.com/codeigniter4/devkit/releases/tag/v1.1.1)
- 2022-11-06 CodeIgniter 4.2.10 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.10.html))
- 2022-10-31 CodeIgniter 4.2.8 & 4.2.9 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.8.html))
- 2022-10-31 公式認証パッケージ CodeIgniter Shield 1.0.0-beta.3 リリース（[ChangeLog](https://github.com/codeigniter4/shield/releases/tag/v1.0.0-beta.3)）
- 2022-10-06 CodeIgniter 4.2.7 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.7.html))
  - 脆弱性情報 [Secure or HttpOnly flag set in Config\Cookie is not reflected in Cookies issued in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-745p-r637-7vvp)
- 2022-09-05 CodeIgniter 4.2.6 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.6.html))
- 2022-08-29 CodeIgniter 4.2.5 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.5.html))
- 2022-08-28 CodeIgniter DevKit [1.1.0 リリース](https://github.com/codeigniter4/devkit/releases/tag/v1.1.0)
- 2022-08-14 CodeIgniter 4.2.4 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.4.html))
- 2022-08-08 公式認証パッケージ [CodeIgniter Shield](https://github.com/codeigniter4/shield#codeigniter-shield) [1.0.0-beta.2 セキュリティ修正](https://github.com/codeigniter4/shield/releases/tag/v1.0.0-beta.2) リリース
  - 脆弱性情報 [SameSite Attackers may Bypass the CSRF Protection](https://github.com/codeigniter4/shield/security/advisories/GHSA-5hm8-vh6r-2cjq)
- 2022-08-07 CodeIgniter 4.2.3 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.3.html))
- 2022-08-06 CodeIgniter 4.2.2 リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.2.html))
- 2022-08-04 [Bonfire2 v1.0.0-beta-1](https://github.com/lonnieezell/Bonfire2/releases/tag/v1.0.0-beta-1) リリース
- 2022-06-17 [CodeIgniter 4.2.1](https://forum.codeigniter.com/showthread.php?tid=82144) リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.1.html))
- 2022-06-10 新しいTwitterアカウント[CodeIgniterPHP](https://twitter.com/CodeIgniterPhp) 開設
- 2022-06-04 CodeIgniter DevKit [v1.0.0 リリース](https://github.com/codeigniter4/devkit/releases)
- 2022-06-04 [CodeIgniter 4.2](https://forum.codeigniter.com/showthread.php?tid=82011) リリース ([ChangeLog](https://codeigniter4.github.io/CodeIgniter4/changelogs/v4.2.0.html))
  - PHP 7.4 以上が必要
  - [CodeIgniter 4.2 の変更点](http://blog.a-way-out.net/blog/2022/12/04/codeigniter-4-2/)
- 2022-06-03 公式認証パッケージ [CodeIgniter Shield](https://github.com/codeigniter4/shield#codeigniter-shield) [v1.0.0-beta](https://github.com/codeigniter4/shield/releases/tag/v1.0.0-beta) [リリース](https://forum.codeigniter.com/showthread.php?tid=82003)
- 2022-02-26 CodeIgniter [v4.1.9](https://codeigniter4.github.io/userguide/changelogs/v4.1.9.html) リリース
  - 脆弱性情報 [Remote CLI Command Execution Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-xjp4-6w75-qrj7)
  - 脆弱性情報 [Cross-Site Request Forgery (CSRF) Protection Bypass Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-4v37-24gm-h554)
- 2022-01-25 CodeIgniter [v4.1.8](https://codeigniter4.github.io/userguide/changelogs/v4.1.8.html) リリース
  - 脆弱性情報 [XSS Vulnerability in API\ResponseTrait in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-7528-7jg5-6g62)
- 2022-01-10 CodeIgniter [v4.1.7](https://codeigniter4.github.io/userguide/changelogs/v4.1.7.html) リリース
- 2022-01-04 [CodeIgniter v4.1.6 released](https://forum.codeigniter.com/thread-80926.html)
  - PHP 8.1 をサポート
  - 脆弱性情報 [Deserialization of Untrusted Data in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-w6jr-wj64-mc9x)

[過去のニュース](./old/News.md)

## 本家
- CodeIgniter 公式サイト http://codeigniter.com/
- CodeIgniter 公式Twitter https://twitter.com/CodeIgniterPhp
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
- v4.2.11 で修正済み
  - [Attackers may spoof IP address when using proxy ](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-ghw3-5qvm-3mqc)
  - [Potential Session Handlers Vulnerability](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-6cq5-8cj7-g558)
- v4.2.7 で修正済み
  - [Secure or HttpOnly flag set in Config\Cookie is not reflected in Cookies issued in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-745p-r637-7vvp)
- v4.1.9 で修正済み
  - [Remote CLI Command Execution Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-xjp4-6w75-qrj7)
  - [Cross-Site Request Forgery (CSRF) Protection Bypass Vulnerability in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-4v37-24gm-h554)
- v4.1.8 で修正済み
  - [XSS Vulnerability in API\ResponseTrait in CodeIgniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-7528-7jg5-6g62)
- v4.1.6 で修正済み
  - [Deserialization of Untrusted Data in Codeigniter4](https://github.com/codeigniter4/CodeIgniter4/security/advisories/GHSA-w6jr-wj64-mc9x)
    - [CodeIgniter 4.1.5 までのオブジェクトインジェクション脆弱性](http://blog.a-way-out.net/blog/2022/12/07/codeigniter4-object-injection-vulnerability/)

## 問題

[過去の問題](./old/Issues.md)

## 開発環境の構築

### Docker
- [Devilboxを使いCodeIgniter4の開発環境を構築する](http://blog.a-way-out.net/blog/2022/12/01/build-codeigniter4-develop-env-with-devilbox/)
- [kenjis/docker-codeigniter-apache: Build a simple CodeIgniter development environment with docker-compose.](https://github.com/kenjis/docker-codeigniter-apache)

### IDE
- [PhpStorm](https://www.jetbrains.com/ja-jp/phpstorm/)
- [CodeIgniter Plugins for Visual Studio Code](https://marketplace.visualstudio.com/search?term=codeigniter&target=VSCode&category=All%20categories&sortBy=Relevance)

### その他
- [codeigniter4/devkit: Development toolkit for CodeIgniter libraries and projects](https://github.com/codeigniter4/devkit)
  - [CodeIgniter DevKit で php-cs-fixer を使いコーディングスタイルを修正する](http://blog.a-way-out.net/blog/2022/12/19/codeigniter-devkit-php-cs-fixer/)
  - [CodeIgniter DevKit で Rector を使いコードを修正する](http://blog.a-way-out.net/blog/2022/12/20/codeigniter-devkit-rector/)

## インストール
- [CodeIgniter 4.2のインストール方法【2022年最新版】](http://blog.a-way-out.net/blog/2022/06/30/how-to-install-codeigniter-421/)
- [CodeIgniter4をインストール (Composer利用) - Qiita](https://qiita.com/kohenji01/items/a36dbbbb19bb8808d104)
- [1つのCodeigniterで複数サイト（例：フロントと管理画面）を運用する - Qiita](https://qiita.com/bananacoffee/items/ca7784ebe0d2d5a320d1)
- [Running Multiple Applications with one CodeIgniter Installation](https://github.com/kenjis/codeigniter4-multiple-apps-sample)

### アプリケーションテンプレート
- [kenjis/ci4-app-template: CodeIgniter4 application template](https://github.com/kenjis/ci4-app-template)
- [lonnieezell/Bonfire2: CodeIgniter 4-based application skeleton](https://github.com/lonnieezell/Bonfire2)
  - [CodeIgniter4 Bonfire2を試す](http://blog.a-way-out.net/blog/2022/12/08/codeigniter4-bonfire2/)

## アップグレード
- [tattersoftware/codeigniter4-patches: Automated project updates for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-patches)
  - [CodeIgniter4のプロジェクトファイルを簡単にアップグレードする](http://blog.a-way-out.net/blog/2022/12/06/easily-upgrade-your-codeIgniter4-project-files/)
- [paulbalandan/liaison-revision: Seamless software updates library for CodeIgniter4 projects.](https://github.com/paulbalandan/liaison-revision)
  - [使用例](https://github.com/kenjis/ci4-composer-installer#liaison-revision)
- [CodeIgniter 4.0を開発版にアップデートする](
  http://blog.a-way-out.net/blog/2020/12/30/update-codeigniter-404/)

## 設定
- [CodeIgniter 4.2の初期設定](http://blog.a-way-out.net/blog/2022/12/17/codeigniter-4-2-initial-settings/)
- [CodeIgniter4の設定クラスについて](http://blog.a-way-out.net/blog/2022/12/18/codeigniter4-config-class/)
- [CodeIgniter4で新しいCI_ENVIRONMENTを定義する](https://zenn.dev/kenjis/articles/24ff7332d32837)
- [CodeIgniter4 .env ファイルを使った encrypt 設定でハマった](https://zenn.dev/naente/articles/e6a7dd8fd51de0)

## チュートリアル
- [CodeIgniter4入門 公式チュートリアル](https://zenn.dev/kenjis/articles/3d5e42f872ff18)
- [CodeIgniter 4 最速マスター](https://zenn.dev/kenjis/articles/811ee63e3fec59)
- [CodeIgniter 4 jQuery DataTables を使用するチュートリアル](https://wdsphere.com/article/codeigniter4-jquery-datatables-tutorial)
- [Learn CodeIgniter](https://learncodeigniter.net/)
- [CodeIgniter 4 Tutorials - Best Place to Learn CodeIgniter 4](https://onlinewebtutorblog.com/category/codeigniter-4/)
- 多言語化
  - Creating a multilingual website with CodeIgniter 4 
    - https://includebeer.com/en/blog/creating-a-multilingual-website-with-codeigniter-4-part-1
    - https://includebeer.com/en/blog/creating-a-multilingual-website-with-codeigniter-4-part-2

## 基本概念

### Services
- [CodeIgniter4のServicesとは？](http://blog.a-way-out.net/blog/2022/12/12/codeigniter4-services/)

### Factories
- [CodeIgniter4のFactoriesとは？](http://blog.a-way-out.net/blog/2022/12/13/codeigniter4-factories/)

### Code Modules
- [CodeIgniter4のモジュール（HMVC）①](http://blog.a-way-out.net/blog/2022/12/14/codeigniter4-modules-1/)

## コントローラ

### ルーティング
- [【改訂版】CodeIgniter4のルーティング](http://blog.a-way-out.net/blog/2022/12/05/codeigniter4-routing/)
- [CodeIgniter 4.2.0 で導入された新しい自動ルーティングについて](https://www.sodo-shed.com/archives/14285)
- [【改訂版】本当は危ないCodeIgniter4の自動ルーティング](http://blog.a-way-out.net/blog/2022/02/08/really-dangerous-codeigniter4-auto-routing/)
- [CodeIgniter4のルーティングでのプレイスホルダー (:any) について](http://blog.a-way-out.net/blog/2022/12/11/codeigniter4-routing-placeholder-any/)
- [Improving Route Filters definition](https://github.com/tangix/ci4-zen-zone/blob/main/improve-route-filters/improving-route-filters.md)
- [kenjis/ci4-attribute-routes: CodeIgniter4 Attribute Routes](https://github.com/kenjis/ci4-attribute-routes)

### REST API
- [CodeIgniter4でREST APIを作成する](http://blog.a-way-out.net/blog/2020/12/20/codeigniter4-rest-api/)
- [CodeIgniterとJSON Web Tokenを使用したセキュアなRESTful APIの構築方法](https://www.twilio.com/blog/create-secured-restful-api-codeigniter-php-jp)

### バリデーション
- [CodeIgniter4のバリデーション](http://blog.a-way-out.net/blog/2022/12/03/codeigniter4-validation/)
- [CodeIgniter4 の $this->validate() でラベル付きのエラーメッセージを使用する - Qiita](https://qiita.com/naente/items/c372dbc3c7f36dbbf373)
- [CodeIgniter4 バリデーションルール valid_date は年月の検証に使用できるのか](https://zenn.dev/naente/articles/49c5717c2a4e26)
- [本当は緩いCodeIgniterのvalid_urlバリデーションルール](http://blog.a-way-out.net/blog/2022/12/02/really-loose-codeigniter-valid-url/)

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
- [tattersoftware/codeigniter4-permits: Model permission handling for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-permits)
- [tattersoftware/codeigniter4-audits: Lightweight object logging for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-audits)

### データベース
- [CodeIgniter4 のクエリビルダ `$builder->selectXXX()` は第2引数にAS句を指定できる - Qiita](https://qiita.com/bananacoffee/items/d5fe9ecb2679e4f9f236)
- [CodeIgniter4 独自ドライバーによるデータベースクラスの拡張](https://zenn.dev/naente/articles/7295d0cf0c5813)
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
- [CodeIgniter 4.3の処理の流れ](http://blog.a-way-out.net/blog/2022/10/31/codeigniter43-process-flow/)
- [CodeIgniter 4.1の処理の流れ](http://blog.a-way-out.net/blog/2021/02/19/codeigniter41-process-flow/)

## フレームワークの拡張
- [CodeIgniter4でMonologを使う](http://blog.a-way-out.net/blog/2021/09/16/codeigniter4-monolog/)
- [[実践CodeIgniter4]第1回：Viewクラスの拡張 | ATTRIBUTE ERROR...](https://www.attribute-error.jp/column/%5B%E5%AE%9F%E8%B7%B5CodeIgniter4%5D%E7%AC%AC1%E5%9B%9E%EF%BC%9AView%E3%82%AF%E3%83%A9%E3%82%B9%E3%81%AE%E6%8B%A1%E5%BC%B5)
- [コントローラの生成をDIコンテナ経由にする](https://github.com/kenjis/ci4-tettei-apps/pull/4)

## ライブラリ

### 公式
- [codeigniter4/settings: Settings Library for CodeIgniter 4](https://github.com/codeigniter4/settings)
- [codeigniter4/cache: PSR-6 and PSR-16 Cache Adapters for CodeIgniter 4](https://github.com/codeigniter4/cache)
- [codeigniter4/shield: Authentication and Authorization for CodeIgniter 4](
  https://github.com/codeigniter4/shield)
- (開発中) [codeigniter4/tasks: Task Scheduler for CodeIgnter 4](https://github.com/codeigniter4/tasks)

### 認証
- [CodeIgniter4の公式認証ライブラリCodeIgniter Shieldを使う](http://blog.a-way-out.net/blog/2022/09/08/codeigniter-shield/)
- [lonnieezell/myth-auth: One-stop Auth package for CodeIgniter 4](https://github.com/lonnieezell/myth-auth)
  - [CodeIgniter4の認証ライブラリMyth Authを使う](https://zenn.dev/kenjis/articles/95f38b7e447155)
- [benedmunds/CodeIgniter-Ion-Auth at 4](https://github.com/benedmunds/CodeIgniter-Ion-Auth/tree/4)
- [Integrating CodeIgniter 4 with Auth0 | michalsn](https://michalsn.dev/posts/integrating-codeigniter-4-with-auth0/)
- [Codeigniter4でソーシャルメディアログインを実装する](https://blog.takeho.com/implement-social-media-login-with-codeigniter-4/)

### データベース
- [daycry/doctrine: Doctrine for Codeigniter 4](https://github.com/daycry/doctrine)
- [Illuminate Database Wrapper for CodeIgniter 4](https://github.com/nfaiz/dbtoolkit)
- [irsyadulibad/ci4-datatables: Server Side Datatables Library for CodeIgniter 4 Framework](https://github.com/irsyadulibad/ci4-datatables)

### ロギング
- [ajmeireles/ci4-sentry: Sentry Integration with CodeIgniter 4](https://github.com/ajmeireles/ci4-sentry)

### REST
- [daycry/restserver: Rest Server for Codeigniter 4](https://github.com/daycry/restserver)

### 多言語化
- [clsmedia/ci4-translation-finder: Translation strings finder for CodeIgniter 4](
  https://github.com/clsmedia/ci4-translation-finder)

### JavaScript/CSS
- [michalsn/minifier: Asset minification and versioning library for CodeIgniter 4](https://github.com/michalsn/minifier)
- [tattersoftware/codeigniter4-assets: Asset handling for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-assets)

### Reactive
- [CodeIgniter4 Viewi Demo](https://github.com/kenjis/ci4-viewi-demo)
- [HTMX helper library for CodeIgniter 4 framework](https://github.com/michalsn/codeigniter-htmx)

### Queue
- [colethorsen/codeigniter4-queue](https://github.com/colethorsen/codeigniter4-queue)
- [arashsaffari/queue](https://github.com/arashsaffari/queue)

### Captcha
- [kenjis/ci3-like-captcha - Packagist](https://packagist.org/packages/kenjis/ci3-like-captcha)
- [Integrate Google ReCaptcha v3 in CodeIgniter 4](http://denis303.com/blog/1-integrate-google-recaptcha-v3-in-codeigniter4)
  - https://forum.codeigniter.com/thread-75779.html
  - https://github.com/denis303/codeigniter4-recaptcha
- [gregwar/captcha - Packagist](https://packagist.org/packages/gregwar/captcha)
- [laminas/laminas-captcha - Packagist](https://packagist.org/packages/laminas/laminas-captcha)

### Long-living PHP
- [CodeIgniter4-Burner](https://github.com/monkenWu/CodeIgniter4-Burner) RoadRunner, Workerman, and OpenSwoole

### Serverless
- [serverless CodeIgniter PHP Framework - powered by Vercel & PlanetScale](https://serverless-codeigniter.vercel.app/)
- [Serverless Codeigniter 4 | michalsn](https://michalsn.dev/posts/serverless-codeigniter-4/)

## アプリケーション
- [『CodeIgniter徹底入門』のサンプルアプリケーション （CodeIgniter v4.1版） ](https://github.com/kenjis/ci4-tettei-apps)
- [CodeIgniter Website](https://github.com/codeigniter4projects/website)
- [samsonasik/ci4-album: 🔥 CodeIgniter 4 example Album module uses Domain Driven Design Architecture with Tactical Pattern](https://github.com/samsonasik/ci4-album)
- [Castopod](https://github.com/ad-aures/castopod) a free and open-source podcast hosting solution

## 書籍
- [CodeIgniter 4 Foundations](https://leanpub.com/codeigniter4foundations) by Lonnie Ezell
- [CodeIgniter 4 Foundations](https://www.amazon.co.jp/dp/B09MJ9RWN9) ペーパーバック
