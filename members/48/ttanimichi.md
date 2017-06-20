
# @ttanimichi

- [homepage](https://ttanimichi.com/)
- [twitter](https://twitter.com/ttanimichi)

久しぶりに ginza.rb 来ました。
1年くらい前にフリーランスになりました。今は不動産 Tech の会社（@銀座7丁目！）に常駐しています。Rails です。

僕の代わりに Rails バージョンアップしてくれる方を探しています。

- Rails 4.2.8 から 5.1.1 へアップグレードしたい
- フリーランス可
- リモート可
- 金払いは良さそう
- @y-yagi さんとかどうですかね...
  - もちろん他の方でもどなたか是非
- ちなみに Ruby は 2.4.1 です

あと、週1で [TECH::CAMP](https://tech-camp.in/) の講師もしています。

## 最近気になること

### Rails における無効な options の取り扱い

```ruby
Post.has_many :comments, invalid_option: true
#<ArgumentError: Unknown key: :touch. Valid keys are: :class_name, :anonymous_class, :foreign_key, :validate, :autosave, :table_name, :before_add, :after_add, :before_remove, :after_remove, :extend, :primary_key, :dependent, :as, :through, :source, :source_type, :inverse_of, :counter_cache, :join_table, :foreign_type, :index_errors>
```

`has_many` は ArgumentError を吐いてくれる

```
helper.number_to_currency(1234567890, invalid_option: true)
=> "$1,234,567,890.00" # 無言で無視される
```

！？

- 仕様に統一感なくない？
- issue 立てようかな...
