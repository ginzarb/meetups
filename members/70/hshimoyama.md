# @hshimoyama

- [github](https://github.com/hshimoyama)
- [twitter](https://twitter.com/_h_s_)

五反田近辺で Rails アプリを開発してます。
最近は Terraform とか yaml とか書いたりもしてます。

## 最近

- keyword arguments と numbered parameters の相性が悪そう
  - https://gist.github.com/hshimoyama/e5d47fd3033a548a06b2c5bfb86d94e6
- 気になった発表
  - ko1 さんの Write a Ruby interpreter in Ruby for Ruby 3
    - ISeq binary の dump/load で高速化するならそのアプローチを gem に広げたり…という現実的な改善方向が見えた
  - Samuel Williams さんの Fibers Are the Right Solution
    - IO が支配的なのであれば Fiber で良いという割り切りは web では一定正しそう
  - 静的型解析は "sound" でないことを前提としてどこまで/どういう情報を rbi に持つのかという割り切りが興味深かった
    - 動的解析前提にしては情報量は抑えてあり、手で書くのも不可能ではない所に落とし所を見つけているのが上手い
