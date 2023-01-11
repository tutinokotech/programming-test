# 開発能力テストの課題

プログラマーとデザイナーで課題が異なりますので、ご確認ください。  

## デザイナー課題

本システムでは、 [Bootstrap](https://getbootstrap.jp/) を使用します  
以下の画面をデザインし、コーディングしてください  
画面サイズとして、PC、タブレット、スマートフォンサイズにそって、レスポンシブデザインの設定をしてください  
コーディングしたHTMLは、以下のパスのとおりsampleフォルダに格納してください  

1. ログインフォーム `sample/login.html`  
1. マイページ `sample/mypage.html`  
1. 紹介者の追加 `sample/add_syoukaisya.html`  
1. 人事部に紹介する `sample/syoukai.html`  
1. 紹介された方の確認 `sample/syoukai-kakunin.html`  
1. 追加情報を依頼する（紹介者の登録） `sample/more_syoukaisya.html`  

![logo.png](img/logo.png)  

ロゴ情報  

- アイコン色 #5da9f5  
- 文字色 #2e3740  

ヘッダー

- 左側にロゴマークを表示します  
- 右側にマイページ、ログアウトへのリンク（ボタンでもよい）を表示します  
  - ログインフォームでは、マイページ、ログアウトは表示しません  
  - 画面サイズが小さい場合には、マイページ、ログアウトは `navbar-collapse` を使用して、親ブレークポイントによってナビゲーションバーのコンテンツをグループ化します（バーガーアイコン）  

フッター

- `&copy; XXXX Corp. 20XX` を表示します（`&copy;`は丸の中にcが入ったCopyrightを表す特殊文字です）  

その他

- ロゴ画像をもとに、favicon.ico を作成して設定してください  

## プログラマー課題  

プログラマーの課題では、 [Laravel](http://laravel.jp/) を使用したシステム構築をおこないます  
開発環境として、Dockerを準備しています  
[DOCKER_USAGE.md](DOCKER_USAGE.md) に構築方法を記載しています  

バージョン情報は以下のとおりです  

- PHP 8  
- Laravel 8  
- MySQL 5.7  

### プログラマー課題1

[Bootstrap](https://getbootstrap.jp/) を使用して、簡単な説明用のモックアップを作成します  
作成したモックアップは sample フォルダに格納します  

- [Bootstrap](https://getbootstrap.jp/) の Examples より  
  - Sign-in の HTML を利用して、ログインフォームを作成します  
    `sample/login.html` として保存します  
  - Navbar の HTML を利用して、マイページなどで表示される共通のヘッダーを作成します  
    - ロゴとして、テキストで「List of Excellent Young-man」を表示します  
    - ヘッダーの右側に、「ログアウト」のリンクを設置します  
- 以下の2つの画面についてサンプルを作成します。  
  コーディングしたHTMLは、以下のパスのとおりsampleフォルダに格納してください  
  1. マイページ `sample/mypage.html`  
  1. 紹介者の追加 `sample/add_syoukaisya.html`  

### プログラマー課題2

シナリオ 1 までを実現する機能を作成してください  

- ログイン画面は、すでに準備されている `laravel\resources\views\auth\login.blade.php` を使用して作成してください  
- データベースへのテーブル追加は、`php artisan migrate` を使用してください  
- 画面は blade を使用して構築し、 `laravel\resources\views` に格納してください  
- メール送信は `config/mail.php` に設定を記述し、 `php artisan make:mail` コマンドを使用して Mailable クラスを記述して作成してください  
  - 送信されたメールは、開発環境では MailHog で受信を確認します  

### プログラマー課題3

本システムのシナリオは紹介者・紹介など、同じような単語で別の意味で使われている言葉がいくつか存在します。どのように言い分ければ齟齬がないシステムがつくれるでしょうか？  
検討し、画面に反映してください  
