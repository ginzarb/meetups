# @UsaMomokawa

小松ももか

- [GitHub](https://github.com/UsaMomokawa)
- [Twitter](https://twitter.com/komammkw)

明治大学政治経済学部4年生。[フィヨルドブートキャンプ](https://bootcamp.fjord.jp/)に1年間在籍していました。今年4月よりGMOペパボにて新卒エンジニアとして勤務します。

## 最近のこと
[Rails Girls Tokyo 13th](http://railsgirls.com/tokyo.html)が2月14日〜15日に開催されます。
(メドピア様にスポンサードいただいています。ありがとうございます！)
私はロゴ・グッズデザインとスタッフを担当しています。


## 参加動機
Mailerをgenerateしたら、Zeitwerkが動かなくなってしまいました。
コードを読んでZeitwerkの動きを学びたいです。

### 再現手順
Ruby 2.7.0
Rails 6.0.2

1. `$ rails new hoge`

2. config/application.rbにログの設定

```
Rails.autoloaders.logger = Logger.new("#{Rails.root}/log/autoloading.log")
```

3. `$ rails g mailer UserMailer`

4. `$ rails r UserMailer`

```
$ rails r UserMailer

uninitialized constant UserMailer
```

Zeitwerkが壊れて、ログも吐かれなくなります。

### 回避方法の例
- [定数読み込みをclassicモードに設定する](https://railsguides.jp/autoloading_and_reloading_constants.html#zeitwerk%E3%82%92%E4%BD%BF%E3%82%8F%E3%81%AA%E3%81%84%E5%A0%B4%E5%90%88)

- Mailer作成時に、テストを作成しない
  - `$ rails g mailer UserMailer --skip-test-framework`
