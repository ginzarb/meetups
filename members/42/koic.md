# @koic

Koichi ITO

* [Blog](http://koic.hatenablog.com/)
* [GitHub](https://github.com/koic)
* [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントで日々働く会社員。Ruby とかメタルなんか好きです。

## 最近気になること

* https://24pullrequests.com で 24 PRs を 19 日目に達成しました (2016-12-19の昨日のできごと)
* うち Ruby 2.4.0 対応は 16 PRs でした
* さらにうち Unify Fixnum and Bignum into Integer 関連が 13 PRs で、BigDecimal の新仕様の関連が 3 PRs でした

## おまけ

Unify Fixnum and Bignum into Integer が目立つように思うけれど、BigDecimal の新しい振る舞いについても見ておくと良さそうと思ったりしている。

### RUBY_VERSION #=> "2.3.3"

```ruby
require "bigdecimal"

v = sprintf("%#.0e", 1) #=> "1.e+00"
BigDecimal(v)           #=> #<BigDecimal:7f85e08906a8,'0.1E1',9(18)>
BigDecimal(v).to_s      #=> "0.1E1"
```

### RUBY_VERSION #=> "2.4.0"

```ruby
require "bigdecimal"

v = sprintf("%#.0e", 1) #=> "1.e+00"
BigDecimal(v)           #=> ArgumentError: invalid value for BigDecimal(): "1.e+00"
BigDecimal("1.0e0")     #=> 0.1e1
```

### Float の動き

```ruby
Float("1.e+00")         #=> ArgumentError: invalid value for Float(): "1.e+00"
```

ぜんぜん関係ないけれど、`binding.irb` なんかいいですね :santa:
