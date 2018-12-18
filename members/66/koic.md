# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

株式会社永和システムマネジメントのコミュニティマネージャ。
RuboCop のコミッター。Active Record Oracle enhanced adapter のコミッター。Cucumber のコミッター。

## 最近

- 1月14日(月・祝) 締め切りの [RubyKaigi 2019 の CFP](https://cfp.rubykaigi.org/events/2019) 進捗これからです。
- 1月24日(木) に [Rails/OSS パッチ会を開催します](http://blog.agile.esm.co.jp/entry/rails-oss-patch-meetup-20190124)。
- 3月22日(金) から 23日(土) に開催される[Rails Developers Meetup 2019](https://railsdm.github.io/) の2日目に登壇します。
- 4月30日(火) から 5月2日(木) にミネアポリスで開催される RailsConf 2019 の往復チケット代がすでに 278,340 円だった。これが GW の世界線 (ゴクリ...
- Ruby 2.6 に向けて取り込まれている私のコードは [Psych へのパッチ](https://github.com/ruby/psych/pull/379) です。

### Example code

```ruby
require 'psych'

Psych.load("--- foo\n", nil)
```

### Before

```console
% ruby -v
ruby 2.6.0dev (2018-10-21 trunk 65252) [x86_64-darwin17]

% ruby /tmp/psych_example.rb
warning: Passing filename with the 2nd argument of Psych.load is deprecated.
Use keyword argument like Psych.load(yaml, filename: ...) instead.
```

### After

```console
% ruby -v
ruby 2.6.0dev (2018-12-18 trunk 66429) [x86_64-darwin17]

% ruby -w /tmp/psych_example.rb
/Users/koic/.rbenv/versions/2.6.0-dev/lib/ruby/site_ruby/2.6.0/rubygems/version.rb:216: warning: deprecated Object#=~ is called on Integer; it always returns nil
/tmp/psych_example.rb:3: Passing filename with the 2nd argument of Psych.load is deprecated.
Use keyword argument like Psych.load(yaml, filename: ...) instead.
```
