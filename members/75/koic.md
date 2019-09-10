# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

株式会社永和システムマネジメントのコミュニティマネージャ。同社が月次で開催する Rails/OSS パッチ会の主催。
RuboCop のコミッター。Active Record Oracle enhanced adapter のコミッター。Cucumber のコミッター。
Parser のコミッター。Faker の org メンバー。

## 最近

- 10月31日(木) に[Rails/OSSパッチ会](https://blog.agile.esm.co.jp/entry/rails-oss-patch-meetup-20191031)を開催します。
- 11/3(日)に富山で富山Ruby会議01で講演します。
- 11/7(木)〜8(金)に松江でRubyWorld Conference 2019に参加します。
- リコール対象でない MBP でも持ち込めない国際線があって、まいったまいった。
- [Ruby 3.0 での非互換変更とされるらしい Real kwargs](https://bugs.ruby-lang.org/issues/14183) に向けた Ruby 2.7 での非推奨警告。delegate なんかは策定中っぽい。アプリケーションレイヤーへのインパクトのフーディングなんかは各自やってみましょう。

```console
# A warning example
% ruby -vwe '
def foo(k: 1); end
foo({k: 42})
'
ruby 2.7.0dev (2019-09-16T12:51:48Z master 3bb1162cac) [x86_64-darwin17]
-e:3: warning: The last argument is used as the keyword parameter
-e:2: warning: for `foo' defined here
```
