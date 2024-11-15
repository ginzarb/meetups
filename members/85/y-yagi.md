# @y-yagi

* [github](https://github.com/y-yagi)

RubyかGoかJSかRustを書いています。Swiftもちまちま。最近はJSが多くってきた。

## 最近気になること

* gRPCとRuby
  * gRPCの特定の機能がRubyだと動かない、という事が時折ある
  * gRPCのクライアントリトライ機能が、サーバがRubyだと動かない、というもの
  * [gRPC Ruby Server seemingly not respecting configured retry policy](https://github.com/grpc/grpc/issues/36461)
  * [Add retry example for Ruby](https://github.com/grpc/grpc/pull/27323) で解決しそうな気配があったのだが、残念ながらレビューがされてなかった
    * 個人的なPRでは、[[Ruby] Reduce log when starting a server](https://github.com/grpc/grpc/pull/37608) もレビューが進まないのだった
  * こういうのがちょいちょいあって厳しい。みんなどうやって対応しているのか。気合？