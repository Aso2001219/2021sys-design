## データベース詳細

d_purchase
|属性名|型|PK|NN|FK|
|order_id|bigint(20)|〇|〇|------|
|costomer_code|varchar(50)|-|〇|-|
|purchase_date|date|-|〇|-|
|total_price|int(11)|-|〇|-|

d_purchase_detail
|属性名|型|PK|NN|FK|
|detail_id|bigint(20)|〇|〇|-|
|order_id|bigint(20)|〇|〇|〇|
|item_code|int(11)|-|〇|-|
|price|int(11)|-|〇|-|
|num|int(11)|-|〇|-|

m_customers
|属性名|型|PK|NN|FK|
|coustomer_code|varchar(50)|〇|〇|-|
|pass|varchar(50)|〇|〇|〇|
|name|varchar(20)|-|〇|-|
|address|varchar(100)|-|〇|-|
|tel|varchar(20)|-|〇|-|
|mail|varchar(100)|-|〇|-|
|del_flag|int(11)|-|-|-|
|reg_date|date|-|〇|-|

m_category
|属性名|型|PK|NN|FK|
|category_id|int(11)|〇|〇|-|
|name|varchar(20)|-|〇|-|
|reg_date|date|-|〇|-|

m_items
|item_code|int(11)|〇|〇|-|
|item_name|varchar(50)|-|〇|-|
|price|int(11)|-|〇|-|
|category_id|int(11)|-|〇|〇|
|image|varchar(200)|-|〇|-|
|detail|varchar(500)|-|-|-|
|del_flag|int(11)|-|-|-|
|reg_date|date|-|〇|-|



## 画面遷移表

|画面/アクション|ログイン|ログアウト|商品検索|商品画像|会員登録|カートの中|商品一覧|カートに入れる|前の画面に戻る|詳細へ|注文確定|トップページ|
|--------------|-------|---------|-------|-------|--------|---------|--------|------------|-------------|------|-------|-----------|
|トップページ|ログイン|トップページ|トップページ|商品詳細|会員情報|カート内|トップページ|-|-|-|-|トップページ|
|会員情報|-|-|-|-|-|-|-|-|-|-|-|トップページ|
|ログイン|トップページ|-|-|-|-|-|-|-|-|-|-|トップページ|
|商品詳細|-|-|-|-|-|-|-|カート内|トップページ|商品詳細|-|トップページ|
|会員情報|-|-|-|-|-|-|-|-|-|-|-|トップページ|
|カート内||トップページ|-|-|-|-|-|-|-|-|購入完了|トップページ|
|購入完了|-|-|-|-|-|-|-|-|-|-|-|-|トップページ













