## yui-knk

- [Twitter](https://twitter.com/spikeolaf)
- [GitHub](https://github.com/yui-knk)

### 関心ごと

- parser
- parser generator
- syntax tree

### 最近やっていること

- `RubyVM::AbstractSyntaxTree::Node#locations` を実装した
  - https://github.com/ruby/ruby/pull/11226
  - 各Nodeへのlocationの追加については https://github.com/ruby/ruby/pull/11227 を参考にしつつ、以下の手順で行います
  - rubyparser.h
    - Nodeの構造体定義に必要な rb_code_location_t fieldを追加する
  - parse.y
    - Node 構造体生成用の関数を更新する (`rb_node_unless_new` など)
    - 対応するマクロの更新 (`NEW_UNLESS` など)
    - 生成規則でlocationを渡すようにする。省略可能なケースなど、対応するlocationがない場合は `NULL_LOC` を渡す
  - node_dump.c
    - `F_LOC` を追加
  - ast.c
    - `node_locations` に `CASE` を追加する
  - test/ruby/test_ast.rb
    - test を追加する

- CRubyのNodeの整理
  - できた
    - NODE_UNDEFの構造を修正する (`undef :a, :b`)
      - https://github.com/ruby/ruby/pull/11213
    - NODE_RESBODYの例外用の変数を`nd_exc_var`に切り出す (`begin; rescue Error => e; end`)
      - https://github.com/ruby/ruby/pull/11243
  - これから
    - NODE_ITERとNODE_CALLの位置関係を調整する (`1.times do end`)
    - NODE_ENSURE, NODE_RESCUEの階層構造をフラットにする (`begin a; rescue; ensure; end`)
    - NODE_ARGSCAT, NODE_ARGSPUSH を消し去る (`m(1, *a, 2, *b)`)
