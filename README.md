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
  - [ツール](#%E3%83%84%E3%83%BC%E3%83%AB)
- [インストール](#%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)
- [チュートリアル](#%E3%83%81%E3%83%A5%E3%83%BC%E3%83%88%E3%83%AA%E3%82%A2%E3%83%AB)
- [コントローラ](#%E3%82%B3%E3%83%B3%E3%83%88%E3%83%AD%E3%83%BC%E3%83%A9)
  - [ルーティング](#%E3%83%AB%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0)
  - [REST API](#rest-api)
- [モデル](#%E3%83%A2%E3%83%87%E3%83%AB)
  - [データベース](#%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9)
- [ビュー](#%E3%83%93%E3%83%A5%E3%83%BC)
  - [テンプレートエンジン](#%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%B3)
- [テスト](#%E3%83%86%E3%82%B9%E3%83%88)
  - [PHPUnit](#phpunit)
  - [フィーチャーテスト](#%E3%83%95%E3%82%A3%E3%83%BC%E3%83%81%E3%83%A3%E3%83%BC%E3%83%86%E3%82%B9%E3%83%88)
- [コード生成](#%E3%82%B3%E3%83%BC%E3%83%89%E7%94%9F%E6%88%90)
- [CLI コマンド](#cli-%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89)
- [CodeIgniter3 からの移行](#codeigniter3-%E3%81%8B%E3%82%89%E3%81%AE%E7%A7%BB%E8%A1%8C)
- [デバッグ](#%E3%83%87%E3%83%90%E3%83%83%E3%82%B0)
- [フレームワーク内部](#%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AF%E5%86%85%E9%83%A8)
- [ライブラリ](#%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA)
  - [認証](#%E8%AA%8D%E8%A8%BC)
  - [データベース](#%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9-1)
  - [REST](#rest)
  - [JavaScript/CSS](#javascriptcss)
  - [Captcha](#captcha)
- [アプリケーション](#%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3)
- [書籍](#%E6%9B%B8%E7%B1%8D)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 最近の動向
- [CodeIgniter 4.0.5と4.1.1がリリースされました](http://blog.a-way-out.net/blog/2021/02/02/codeigniter-405-and-411-released/)
  - 4.0.5 は PHP 7.2 をサポートする最後のバージョン
  - 4.1.0 は PHP 7.3 以上が必要
- [CodeIgniter v4.0.4 released](https://forum.codeigniter.com/thread-77054.html)

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

## コミュニティ
- 本家フォーラム http://forum.codeigniter.com/
- 本家 Slack https://codeigniterchat.slack.com/
- Stack Overflow https://stackoverflow.com/questions/tagged/codeigniter-4
- 日本 CodeIgniter ユーザ会 http://codeigniter.jp/
- Qiita https://qiita.com/tags/codeigniter4

## 脆弱性情報
- n/a

## 問題
- [getCompiledSelect の罠、 useSoftDelete が抜け落ちる - Qiita](https://qiita.com/bananacoffee/items/0aff3f5cd005a5f1bfc6)
- 環境変数名にドットが使えない環境がある
  - https://github.com/codeigniter4/CodeIgniter4/issues/4026

## 開発環境の構築

### Docker
- [codeigniter4-dockerでCodeIgniter4の開発環境を作成してみる](http://blog.a-way-out.net/blog/2020/12/08/codeigniter4-docker/)
- [kenjis/docker-codeigniter-apache: Build a simple CodeIgniter development environment with docker-compose.](https://github.com/kenjis/docker-codeigniter-apache)

### ツール
- [paulbalandan/liaison-revision: Seamless software updates library for CodeIgniter4 projects.](https://github.com/paulbalandan/liaison-revision)

## インストール
- [CodeIgniter 4.0のインストール方法【2020年最新版】](http://blog.a-way-out.net/blog/2020/12/29/how-to-install-codeigniter-404/)
- [CodeIgniter 4.0を開発版にアップデートする](
  http://blog.a-way-out.net/blog/2020/12/30/update-codeigniter-404/)
- [CodeIgniter4をインストール (Composer利用) - Qiita](https://qiita.com/kohenji01/items/a36dbbbb19bb8808d104)
- [1つのCodeigniterで複数サイト（例：フロントと管理画面）を運用する - Qiita](https://qiita.com/bananacoffee/items/ca7784ebe0d2d5a320d1)
- [kenjis/ci4-app-template: CodeIgniter4 application template](https://github.com/kenjis/ci4-app-template)

## チュートリアル
- [CodeIgniter4の公式チュートリアルをやってみる](http://blog.a-way-out.net/blog/2020/12/01/codeigniter4-tutorial-1/)
- [CodeIgniter 4 Tutorials - Best Place to Learn CodeIgniter 4](https://onlinewebtutorblog.com/category/codeigniter-4/)

## コントローラ

### ルーティング
- [CodeIgniter4でDB接続まで - Qiita](https://qiita.com/kohenji01/items/ced458da42ce70e067f8)

### REST API
- [CodeIgniter4でREST APIを作成する](http://blog.a-way-out.net/blog/2020/12/20/codeigniter4-rest-api/)

## モデル
- [CodeIgniter4のModelの基礎 - Qiita](https://qiita.com/kohenji01/items/b3e947623309d478e02b)
- [CodeIgniter ModelはQuery Builderを直接呼べるのでわかりづらい](https://forum.codeigniter.com/thread-75871-post-373699.html#pid373699)

### データベース
- [getCompiledSelect の罠、 useSoftDelete が抜け落ちる - Qiita](https://qiita.com/bananacoffee/items/0aff3f5cd005a5f1bfc6)
- [Databaseクラスを拡張する方法](https://forum.codeigniter.com/thread-78294-post-383813.html#pid383813)

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

### フィーチャーテスト
- [CodeIgniter4のフィーチャーテスト](http://blog.a-way-out.net/blog/2020/12/14/codeigniter4-feature-testing/)

## コード生成
- [CodeIgniter4のコードジェネレータ](http://blog.a-way-out.net/blog/2020/12/07/codeigniter4-cli-generators/)

## CLI コマンド
- [CodeIgniter4でCLIコマンドを作成する](http://blog.a-way-out.net/blog/2020/12/18/create-codeigniter4-cli-commands/)

## CodeIgniter3 からの移行
- [CodeIgniter 3.1と4.1の違い](http://blog.a-way-out.net/blog/2021/02/22/differences-between-codeigniter31-and-41/)
- [Codeigniter3で使っていたアレをCodeigniter4で使う - Qiita](https://qiita.com/bananacoffee/items/6bb631391c2301d28c73)
- [kenjis/ci3-to-4-upgrade-helper: CodeIgniter 3 to 4 Upgrade Helper](https://github.com/kenjis/ci3-to-4-upgrade-helper)

## デバッグ
- [PhpStormとXdebug3でCodeIgniter4をステップ実行する](http://blog.a-way-out.net/blog/2020/12/24/step-debugging-codeigniter4-with-phpstorm-and-xdebug3/)

## フレームワーク内部
- [CodeIgniter 4.1の処理の流れ](http://blog.a-way-out.net/blog/2021/02/19/codeigniter41-process-flow/)

## ライブラリ

### 認証
- [lonnieezell/myth-auth: One-stop Auth package for CodeIgniter 4](https://github.com/lonnieezell/myth-auth)
- [benedmunds/CodeIgniter-Ion-Auth at 4](
  https://github.com/benedmunds/CodeIgniter-Ion-Auth/tree/4)
- [agungsugiarto/codeigniter4-authentication](https://github.com/agungsugiarto/codeigniter4-authentication)

### データベース
- [tattersoftware/codeigniter4-relations: Entity relationships for CodeIgniter 4](https://github.com/tattersoftware/codeigniter4-relations)
- [4spacesdk/CI4OrmExtension: OrmExtension for CodeIgniter 4](https://github.com/4spacesdk/CI4OrmExtension)
- [daycry/doctrine: Doctrine for Codeigniter 4](https://github.com/daycry/doctrine)
- [agungsugiarto/codeigniter4-eloquent: The Illuminate Database package for CodeIgniter 4](https://github.com/agungsugiarto/codeigniter4-eloquent)

### REST
- [daycry/restserver: Rest Server for Codeigniter 4](https://github.com/daycry/restserver)

### JavaScript/CSS
- [michalsn/minifier: Asset minification and versioning library for CodeIgniter 4](https://github.com/michalsn/minifier)

### Captcha
- [kenjis/ci3-like-captcha - Packagist](https://packagist.org/packages/kenjis/ci3-like-captcha)
- [Integrate Google ReCaptcha v3 in CodeIgniter 4](http://denis303.com/blog/1-integrate-google-recaptcha-v3-in-codeigniter4)
  - https://forum.codeigniter.com/thread-75779.html
  - https://github.com/denis303/codeigniter4-recaptcha
- [gregwar/captcha - Packagist](https://packagist.org/packages/gregwar/captcha)
- [laminas/laminas-captcha - Packagist](https://packagist.org/packages/laminas/laminas-captcha)

## アプリケーション
- [『CodeIgniter徹底入門』のサンプルアプリケーション （CodeIgniter v4.1版） ](https://github.com/kenjis/ci4-tettei-apps)
- [samsonasik/ci4-album: 🔥 CodeIgniter 4 example Album module uses Domain Driven Design Architecture with Tactical Pattern](https://github.com/samsonasik/ci4-album)

## 書籍
- [CodeIgniter 4 Foundations](https://leanpub.com/codeigniter4foundations) by Lonnie Ezell
