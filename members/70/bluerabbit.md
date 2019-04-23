## Description
# @bluerabbit

![gyazo](https://gyazo.com/210b0aac6140cb3f08ccc9a7aa9bc449.png)

* [Twitter](https://twitter.com/bluerabbit777jp)
* [GitHub](https://github.com/bluerabbit)
* [Blog](http://bluerabbit.hatenablog.com/)
* [note](https://note.mu/bluerabbit)

* RailsでDBに入れたりDBから出したりするお仕事をしています。
* 将棋が趣味で棋譜が動く[将棋アイオー](https://shogi.io)ってサイトを運営しています。
* パフォーマンス・チューニングが得意です。[ISUCON8は6位でした](http://bluerabbit.hatenablog.com/entry/2018/10/21/005607)

## 最近気になること

* 本番環境でmodels配下のファイルで未使用のメソッドを記録するgemみたいなの作れないかな?
* RubyでわかるSQLチューニングって内容を社内のメンバーに勉強会で話したら好評だったのでブログにまとめたいと思っています

### RubyでわかるSQLチューニング

次のSQLが以下の場合に

- Nested Loop Join
- 駆動表がdepartments
- 内部表がusers

```sql
SELECT
  departments.name AS dept_name,
  users.name AS user_name
FROM
  users
    INNER JOIN departments
      ON departments.id = users.dept_id
WHERE
  users.department_id IN (1, 2)
ORDER BY
  users.name
```

rubyの擬似コードでActiveRecord風に書くと次のようになる

```ruby
rows = [] # 結果セット

Department.where(id: [1, 2]).each do |dept|
  User.where(department_id: dept.id).each do |user|
    rows << {user_name: user.name, department_name: dept.name}
  end
end

rows.sort_by {|row| row.user_name }
```

- SQLの結果セット(rows)がメモリに収まりきれない場合にMySQLだと実行計画に`Using temporary`と表示される。
- `Using temporary`になるとtemporaryテーブルにINSERTが始まりDBのFileI/Oが発生する
- メモリに収まる場合は`Using filesort`になる。
