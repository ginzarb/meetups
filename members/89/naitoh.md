# @naitoh

NAITOH Jun

- [blog](https://naitoh.hatenablog.com/)
- [github](https://github.com/naitoh)
- [X](https://twitter.com/naitoh)
- [ruby/rexml](https://github.com/ruby/rexml/) のメンテナーです。

MedPeer 株式会社で BackEnd エンジニアやっています。

会場に飲み物とお菓子を用意しておりますので、 X に #ginzarb のハッシュタグを付けてアップしてもらえると嬉しいです。

## 宣伝

RubyKaigi 2025 の 2日目 AM にしゃべりますので、お時間があれば聴きに来てください。

- https://rubykaigi.org/2025/presentations/naitoh.html#day2

去年のLTの話の続きで、 REXMLのXMLのパース処理をStringScanner を使って速くしたので、高速化のポイントを話す予定です。

## 最近やったOSS活動

  - ruby/rexml パース処理(CDATA, comment)の高速化
    - [Improve CDATA parse performance](https://github.com/ruby/rexml/pull/244)
      - YJIT=ON : 1.76x - 1.83x faster
      - YJIT=OFF : 1.82x - 1.97x faster
    - [Improve comment parse performance](https://github.com/ruby/rexml/pull/245)
      - YJIT=ON : 1.90x - 3.62x faster
      - YJIT=OFF : 2.04x - 5.06x faster
    - [Improve CDATA and comment parse performance](https://github.com/ruby/rexml/pull/246)
      - comment
        - YJIT=ON : 3.09x faster
        - YJIT=OFF : 4.28x faster
      - CDATA
        - YJIT=ON : 2.91x - 3.80x faster
        - YJIT=OFF : 4.37x - 5.90x faster
    - StringScanner#scan_until を使う事で高速化しました。
