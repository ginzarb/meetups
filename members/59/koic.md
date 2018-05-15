# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントという日本企業で働くプログラマー。

## 最近気になること

- willnet さん第一子お誕生おめでとうございます :tada:
- 5/31(木)から6/2(土)で開催される [RubyKaigi 2018](http://rubykaigi.org/2018) で RuboCop の話をします。進捗65%くらい？
- [RubyKaigi 2018 前夜祭](https://speee.connpass.com/event/85072/)に乗り遅れました。乗り遅れた人がいたら一緒に晩御飯に行きませんか？ ([Cなんとかさんもいるよ](https://twitter.com/chiastolite/status/996245124995661824))
- 6/18(月) に Rails/OSS パッチ会を行いますのでよければご参加ください。
- splat keyword arguments について :thinking:

```console
# 警告が出る (`A#m`)
% ruby -wve "class A; def m(a) end; end; h = {foo: 1}; A.new.m(**h)"
ruby 2.6.0dev (2018-05-08 trunk 63359) [x86_64-darwin17]
-e:1: warning: passing splat keyword arguments as a single Hash to `m'
```

```console
# 警告が出ない (`A#initialize`)
% ruby -wve "class A; def initialize(a) end; end; h = {foo: 1}; A.new(**h)"
ruby 2.6.0dev (2018-05-08 trunk 63359) [x86_64-darwin17]
```

```console
# bbatsov/rubocop#5887 より
options = { opt1: 1, opt2: 2 }
def method1(kw_args); end

def method2(**kw_args); end

method1(**options) # This will warn in ruby 2.6 and currently warns in rubocop.

method2(**options) # This does not warn in ruby 2.6 and should not warn in rubocop.
```
