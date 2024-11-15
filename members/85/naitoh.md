# @naitoh

NAITOH Jun

- [blog](https://naitoh.hatenablog.com/)
- [github](https://github.com/naitoh)
- [X](https://twitter.com/naitoh)

MedPeer 株式会社で BackEnd エンジニアやっています。

会場に飲み物とお菓子を用意しておりますので、 X に #ginzarb のハッシュタグを付けてアップしてもらえると嬉しいです。

- 最近やったOSS活動
  - ruby/strscan `StringScanner#check_until` の文字列マッチの高速化 (マージ済)
    - https://github.com/ruby/strscan/pull/108 : [CRuby] 正規表現マッチに対する文字列マッチの性能差を 1.18x -> 1.24x に高速化
    - https://github.com/ruby/strscan/pull/109 : [JRuby] 正規表現マッチに対する文字列マッチの性能差を 2.11x -> 2.33x に高速化
    - https://github.com/ruby/strscan/pull/110 : [JRuby] 正規表現マッチに対する文字列マッチの性能差を 2.33x -> 2.40x に高速化
  - ruby/rexml パース処理の高速化 (マージ済)
    - https://github.com/ruby/rexml/pull/216 : `StringScanner#check` を `StringScanner#match?` に置き換え、不要な文字列生成を削除する事で高速化
      - YJIT=ON 状態: 最大 1.09x 高速化
      - YJIT=OFF 状態: 最大 1.06x 高速化
