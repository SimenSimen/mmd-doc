## 說明 <!-- omit in toc -->
此為消費流程相關表格。

## 資料表快速連結<!-- omit in toc -->

- [data-shopping-cart|購物車資料表](#data-shopping-cart%e8%b3%bc%e7%89%a9%e8%bb%8a%e8%b3%87%e6%96%99%e8%a1%a8)
- [data-link-history|連結瀏覽紀錄表](#data-link-history%e9%80%a3%e7%b5%90%e7%80%8f%e8%a6%bd%e7%b4%80%e9%8c%84%e8%a1%a8)

#### data-shopping-cart|購物車資料表

資料表名稱: `data_shopping_cart`

中文名稱: 購物車資料表

|     欄位      |   名稱   |                   設置                   | 說明                     | 備註     |
| :-----------: | :------: | :--------------------------------------: | ------------------------ | -------- |
|     `id`      |   編號   |    `int(20)`<br>`[null]`<br>`[pkey]`     | &nbsp;                   | 自動編號 |
|   `shopper`   |  購物人  |   `varchar(64)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `good_id`   |  商品ID  |  `varchar (64)`<br>`[null]`<br>`[idx]`   | 產品通用條碼             | &nbsp;   |
|  `good_name`  | 商品名稱 | `varchar (64)`<br>`[null]`<br>`[unique]` | 由使用者命名之產品編碼   | &nbsp;   |
| `good_price`  | 商品售價 |  `varchar(64)`<br>`[null]`<br>`[null]`   | good-category表          |          |
| `good_amount` | 商品數量 |    `int(20)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
|   `active`    | 啟用狀態 |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
| `created_at`  | 建立時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
| `updated_at`  | 更新時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |

#### data-link-history|連結瀏覽紀錄表

資料表名稱: `data_link_history`

中文名稱: 連結瀏覽紀錄表

|     欄位      |   名稱   |                   設置                   | 說明                     | 備註     |
| :-----------: | :------: | :--------------------------------------: | ------------------------ | -------- |
|     `id`      |   編號   |    `int(20)`<br>`[null]`<br>`[pkey]`     | &nbsp;                   | 自動編號 |
|   `user_id`   | 瀏覽者ID |     `int(20)`<br>`[null]`<br>`[idx]`     | &nbsp;                   | &nbsp;   |
|  `good_link`  | 商品連結 |  `varchar (64)`<br>`[null]`<br>`[idx]`   | 商品頁面之網址             | &nbsp;   |
|   `good_id`   |  商品ID  |  `varchar (64)`<br>`[null]`<br>`[idx]`   | 產品通用條碼             | &nbsp;   |
|  `good_name`  | 商品名稱 | `varchar (64)`<br>`[null]`<br>`[unique]` | 由使用者命名之產品編碼   | &nbsp;   |
| `good_price`  | 商品售價 |  `varchar(64)`<br>`[null]`<br>`[null]`   | good-category表          |          |
| `good_amount` | 商品數量 |    `int(20)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
|   `active`    | 啟用狀態 |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
| `created_at`  | 建立時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
| `updated_at`  | 更新時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
