# ツチノコテクノロジー 開発能力テスト

株式会社ツチノコテクノロジー([https://tutinoko.tech](https://tutinoko.tech))では、プログラマーおよびデザイナーの採用にあたって、開発能力テスト（以下、「本テスト」といいます）を実施しています。  
[tutinokotech/programming-testリポジトリ](https://github.com/tutinokotech/programming-test)（以下、「本リポジトリ」といいます）は、本テストの環境を提供します。  
以下の説明をよく読み、開発能力テストの実施をお願いいたします。   

## 概要

- 本テストは実際の業務のようなシステム（以下「本システム」といいます）の一部を制作します  
- 本テストの課題は、[TASK.md](docs/TASK.md)に記載します  
- 本テストで制作するシステムの機能仕様書は、[FUNCTIONS.md](docs/FUNCTIONS.md)に記載します  
- 本テストのチェックリストは、[CHECKLIST.md](docs/CHECKLIST.md)に記載します

## 開発能力テストの受験にあたって

### デザイナー（コーダー）の場合

1. 開発能力テスト当日にHTML/CSS/JavaScriptを編集できるように、自分のPC環境を整えておいてください。
1. 前提知識  
   HTML/CSS/JavaScript
   [Bootstrap](https://getbootstrap.jp/) を用いてコーディングを行っていただきます。

### システムエンジニアの場合

1. テスト前の準備　※テスト前の準備ができていない場合、テストをする前に不合格とします。
   - 本リポジトリを [fork](https://docs.github.com/ja/get-started/quickstart/fork-a-repo) し、新しいリポジトリを作成します。
   - 新しいリポジトリを `git clone` し、自分の PC にて Docker が起動できることを確認してください。
     - Docker環境の構築方法は、[こちら](./docs/DOCKER_USAGE.md)に記載しています。
   - [プログラマー課題1](https://github.com/tutinokotech/programming-test/blob/main/docs/TASK.md#%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9E%E3%83%BC%E8%AA%B2%E9%A1%8C1)のサンプルHTMLを事前に準備しておいてください。
2. 前提知識  
   HTML/CSS/JavaScript、Git/Docker、PHP/Laravel/SQL  
   [Bootstrap](https://getbootstrap.jp/) を用いてコーディングを行っていただきます。
   Git を使って、本リポジトリをローカル環境にコピーしてもらいます。
   Docker を使って、システムを起動してもらいます
   Laravel を使って、システム開発をしてもらいます。
