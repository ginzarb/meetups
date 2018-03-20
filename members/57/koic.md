# @koic

Koichi ITO

- [Blog](http://koic.hatenablog.com/)
- [GitHub](https://github.com/koic)
- [Twitter](https://twitter.com/koic)

(株) 永和システムマネジメントという受託開発の会社で働くサラリーマン。RubyKaigi 2018 の CFP 通過マン。

## 最近気になること

- 今週末にある [Rails Developers Meetup 2018: Day 1](https://techplay.jp/event/639872) で Git/GitHub の話をします。
- [4/2(月) に Rails/OSS パッチ会を行います](http://blog.agile.esm.co.jp/entry/rails-oss-patch-meetup-20180226)のでよろしければご参加ください。
- [TRICK 2018 (FINAL)](https://github.com/tric/trick2018)のネタ。
- 空前の `TracePoint` ブームが到来しているようです。

```ruby
class Foo
  def foo
    tmp = 'hello'

    puts tmp
  end
end

class Bar < Foo
  def foo
    trace = TracePoint.trace(:line) do |tp|
      if tp.binding.local_variable_defined?(:tmp)
        tp.binding.local_variable_set(:tmp, 'hi')
      end
    end

    super

    trace.disable
  end
end

Bar.new.foo # => hi
```

https://github.com/bblimke/webmock/pull/751
