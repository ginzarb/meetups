# @y-yagi

* [github](https://github.com/y-yagi)

RubyかGoかJSかRustを書いています。Swiftもちまちま。最近はJSが多め。

## 最近気になること

* `OBJC_DISABLE_INITIALIZE_FORK_SAFETY`問題
  * [[__NSCFConstantString initialize] may have been in progress in another thread when fork() was called](https://github.com/rails/rails/issues/38560)
  * [Bug \#14009: macOS High Sierra and “fork” compatibility](https://bugs.ruby-lang.org/issues/14009)
  * forkを使うライブラリを作っているのだが、これが未だにmacで普通に問題になる事があるのかどうか
* メンテされなくなったライブラリをうまい事メンテする方法
  * [annotaterb](https://github.com/drwl/annotaterb)のようなやり方、個人的にはあまり好きではないがこういう方法しか無いのか
