# @y-yagi

* [github](https://github.com/y-yagi)

RubyかGoかJSかRustを書いています。Swiftもちまちま。

## 最近気になること

* MySQL 8.0と外部キー制約
  * MySQL 8.0.4で行われた、「外部キー制約を持っているテーブルにSELECTするとそのテーブルの親テーブルにもメタデータロック(MDL)を置くようになった」の変更が結構しんどい印象
    * [日々の覚書: MySQL 8\.0 vs 外部キー制約 vs ALTER TABLEでメタデータロック待ちになったら疑うこと](https://yoku0825.blogspot.com/2020/08/mysql-80-vs-vs-alter-table.html)
    * 比較的長時間のSELECTを実行するトランザクションと、オンラインDDLが同時に行えない
  * MySQLだと外部キーを使わない事が(まだ)多いと聞いたが、実際のところどうなのか
* RubyGemsの[Trusted Publishing](https://guides.rubygems.org/trusted-publishing/)を使い始めた
  * Trusted Publishingについては、[trusted publishingとは？ \#Python \- Qiita](https://qiita.com/hoshimado/items/21e58344890de1375647)の記事がわかりやすい気がする
  * GitHubのコミッターがほぼRubyGemsにpushして良い人、とみなせる位の規模のプロジェクトなら使って良い気がする
    * 今、GitHub上でのコミッターはいるがRubyGemsにpush出来る人が誰もいないgemのメンテをしているので、そういうのを減らす意味でも良い気がする