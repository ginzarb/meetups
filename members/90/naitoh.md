# @naitoh

NAITOH Jun

- [blog](https://naitoh.hatenablog.com/)
- [github](https://github.com/naitoh)
- [X](https://twitter.com/naitoh)
- [ruby/rexml](https://github.com/ruby/rexml/) のメンテナーです。

MedPeer 株式会社で BackEnd エンジニアやっています。

会場に飲み物とお菓子を用意しておりますので、 X に #ginzarb のハッシュタグを付けてアップしてもらえると嬉しいです。

## 宣伝

RubyKaigi 2025 で StringScanner を用いた REXML の高速化について、お話しましたので、よかったらご視聴下さい。

- https://rubykaigi.org/2025/presentations/naitoh.html#day2

## 最近やったOSS活動

  - ruby/rexml XPath の内部処理のキャッシュ化による高速化
    - [Improve using // in XPath performance](https://github.com/ruby/rexml/pull/249)      
      - YJIT=ON : 4.52x faster
      - YJIT=OFF : 8.04x faster
  - ruby/rexml DOM パース処理の高速化
    - [Improve Text.check performance](https://github.com/ruby/rexml/pull/256)
      - YJIT=ON : dom: 1.11x faster
      - YJIT=OFF : dom: 1.20x faster
  - ruby/rexml XPath で、following, following-sibling, preceding, preceding-sibling 指定時に応答結果が二重になる問題を修正
    - [Fix duplicate responses in XPath following, following-sibling, preceding, preceding-sibling](https://github.com/ruby/rexml/pull/255)

