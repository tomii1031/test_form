# 初めに
開発環境はmacOSで
PHPのバージョンは７.3を使用しています。
あくまで、アウトプットを目的として書いた記事なので、理解しにくい点、間違った内容があるかもしれません。ご容赦ください。

## ポートフォリオについて
名前は『BookList』というアプリで、本のECサイトという設定で開発しました。
私は本を読むことが好きで、本を専門としたECサイトは、まだ少ないと感じ
中古本を買う時に、自分が大切にしていること、買い手、売り手の気持ちになって、出品者は自分の商品を誰にどんな時に読んで欲しいのか、自分の商品のPR文の機能であったり
買い手は円滑に購入できるように、コメント機能を追加したり、
本をよく読む自分が利用したくなるようなECサイトを目指して開発しました。


## アプリの機能一覧

|No|機能|機能について|
|:---:|:---:|:--:|
|1|新規登録機能||
|2|ログイン機能||
|3|ゲストログイン機能|新規登録しなくても、予め用意されているユーザー|
|4|パスワードのハッシュ化|[この機能は記事にまとめました](https://qiita.com/tom111/items/e2c4b7572814f921dddb)|
|5|商品の出品機能|商品の状態、種類、画像、タイトル、値段、著者などを登録|
|6|商品の編集|出品した、個数、値段、PR文、ステータスなどを編集|
|7|商品の削除|出品者は自分の商品を削除|
|8|コメント機能|商品の購入前に、出品者に対してコメントできる|
|9|コメント削除機能||
|10|商品の検索機能|商品の状態、種類で商品を検索できる|
|11|ページネーション|商品一覧ページ、商品別コメントページにそれぞれ|
|12|カートに追加|商品をカートに追加|
|13|カート削除|カートに追加した商品を削除|
|14|商品購入機能|商品を購入する|


ECサイトで必須となる、出品->カートに追加->購入機能を中心に、本を扱うアプリなので、本の状態や、著者、コメント機能なども、追加していきました。

## DB設計
![booklist ER図.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/527269/761dac9a-cc72-d96b-b0a6-24dc1e91ba90.png)

カラムは```id```しか表示させていませんが、DB設計を通じて、主キーや外部キーの繋がりを理解し、論理的に開発することができました。
