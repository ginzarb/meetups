# @expajp

* [Blog](http://expajp-tech.hatenablog.com/)
* [GitHub](https://github.com/expajp)
* [X(Twitter)](https://twitter.com/expajp)

リンカーズ株式会社でエンジニアリングマネージャーをやっています。

## 最近
### 東京Ruby会議12に参加しました
* エラーハンドリングの話が一番印象に残りました

### [ゼロから作るDeep Learning](https://www.oreilly.co.jp/books/9784873117584/) のPythonコードの一部をRubyに移植しました
* 月曜の社内勉強会の当番だったので
* 二層ニューラルネットワークで[MNIST](https://ja.wikipedia.org/wiki/MNIST%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9)の手描き文字認識
* コードは動いたが学習がうまく進まないところで時間切れ
  * ランダムに生成している初期値を固定したいが、データがでかい（`784*10, 10*50` の行列）
  * デバッグしんどい
* 書きやすさの点ではやっぱりRuby
  * 例：横ベクトルと行列のドット演算
  * Python(NumPy): `np.dot(x, A)`
  * Ruby(Numo): `x.dot(A)`
* ただ、パフォーマンスの点でPython(NumPy)の壁が厚い
* [Red Datasets](https://github.com/red-data-tools/red-datasets) で不具合を踏んだのでPR出しときます

### `#rubymusclemixin`
* 筋肉ついた代わりに太ったので、三が日終わった後からケトジェニックダイエット始めました
  * ケトジェニック：極端な糖質制限をして脂質からエネルギーを取り出す体質に変える
* 経過
  * 初日：頭が働かない
  * 2-4日目：頭は働き始めるが、体がだるい
  * 5日目：しんどさが消えてやたら目がバキバキになる
* 3週間で3キロ痩せた（76.8→73.8）
