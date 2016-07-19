# @koic

Koichi ITO

* [GitHub](https://github.com/koic)
* [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントで働く会社員。Ruby とか好きです。

## 最近気になること

スローテスト刑事。

* タグで対象のテストを絞る (しかし CI の全テスト実行の前には無力)
* [test-queue](https://github.com/tmm1/test-queue), [parallel_tests](https://github.com/grosser/parallel_tests) などで並列化
* sleep を取り締まる
* テストの重複を消す
* 使われていないテスト (と呼び出される不要な) コードを捨てる
* before(:all), before(:each), aggregate_failures あたりの最適化
* 不要な AR オブジェクト作らない (factory で関連作らず nil にしておく)
* DB にアクセスさせない (FactoryGirl.create -> build)
* system 呼び出さない
* サムネイル作らない

To be continued... Thanks to @onk @1syo @yattom
