# @ttanimichi 谷道 たにみち

https://ttanimichi.com/

![ttanimichi](https://res.cloudinary.com/dvkrqcbms/image/upload/c_scale,h_50/v1537263304/5486854.jpg)

- フリーランス
  - 去年からは株式会社マネーフォワードさんに常駐しています

## 最近気になっていること

- React と Rails のより良い共存
  - そのうち Qiita か何かに詳しく書きます
  - [react-rails のコミッターになりました – たにみち – Medium](https://medium.com/@ttanimichi/react-rails-%E3%81%AE%E3%82%B3%E3%83%9F%E3%83%83%E3%82%BF%E3%83%BC%E3%81%AB%E3%81%AA%E3%82%8A%E3%81%BE%E3%81%97%E3%81%9F-94d1f3286438)
  - [Pull Requests · rails/webpacker](https://github.com/rails/webpacker/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Attanimichi+)
  - [Pull Requests · rails/rails](https://github.com/rails/rails/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Attanimichi+webpacker)

結局、社内用の管理画面は webpacker で `rails-ujs` だけ import して slim 使うことにした。

```
$ cat app/javascript/packs/admin.js
import Rails from 'rails-ujs';
import '../admin/style'; // SCSS

Rails.start();
```
