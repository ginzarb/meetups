# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントという受託開発の会社で働くサラリーマン。[工藤派](https://www.google.co.jp/search?q=%E4%BA%8C%E6%AC%A1%E4%BC%9A%E3%81%A8%E3%81%AF)。
2017年秋くらいからは構文解析チックな OSS 活動をよくしています。

## 最近気になること

[前回の Ginza.rb のふりかえりで挙がった Try](https://github.com/ginzarb/meetups/wiki/%E7%AC%AC54%E5%9B%9E#try) へのアクション。

CentOS 6 の GCC 4.4 と Autoconf 2.67 未満では Ruby 2.5.0 をビルドできない。鋭意 CentOS 6 でのビルドを試みているところ。
koic/ruby を使った ruby-build での指定と Autoconf のビルドで、あと一歩っぽいところまで行っていて openssl と readline でつっかえている。
http://koic.hatenablog.com/entry/ruby-2-5-build-with-gcc-4-4

諸般の事情で 2.5 にアップグレードできない人向けに、Ruby 2.4 以前でもせめて `Kernel#yield_self` くらい使えるようにバックポート gem を作っておいた。
https://github.com/koic/backport_yield_self

まとめるとレガシーインフラは大変。
