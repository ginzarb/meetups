# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントという受託開発の会社で働くサラリーマン。
2017年秋くらいからは構文解析チックな OSS 活動をよくしています。

## 最近気になること

- [Screamers という自作 Gem](https://github.com/koic/screamers) を使って [Oracle の型変換](https://github.com/rsim/oracle-enhanced/#upgrade-rails-42-or-older-version-to-rails-5)をやる気持ち
- タイムスタンプのミリ秒単位でのテストどうしていますか？

RDBMS (Oracle) の `TIMESTAMP(6)` は小数点以下6桁まで保持している。

```
> model.created_at.iso8601(9)
=> "2017-12-15T15:45:37.671693000+09:00"
```

Ruby の `Time` のミリ秒をどこまで表現するかは OS によって異なる。

```
# Mac
> Time.current.iso8601(9)
=> "2017-12-15T15:45:37.671693000+09:00"

# Linux
> Time.current.iso8601(9)
=> "2017-12-15T15:54:49.610580819+09:00"
```

例えばローカルの Mac だとテストをパスして、CI の Linux だと落ちる。
