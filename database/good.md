## 說明 <!-- omit in toc -->
此為商品相關表格。

## 資料表快速連結<!-- omit in toc -->

- [good|商品資料表](#good%E5%95%86%E5%93%81%E8%B3%87%E6%96%99%E8%A1%A8)
- [good-spec|商品規格表](#good-spec%E5%95%86%E5%93%81%E8%A6%8F%E6%A0%BC%E8%A1%A8)
- [good-category|商品分類表](#good-category%E5%95%86%E5%93%81%E5%88%86%E9%A1%9E%E8%A1%A8)

#### good|商品資料表
#### good-spec|商品規格表
#### good-category|商品分類表

資料表名稱: `good`

中文名稱: 商品資料表

|     欄位      |   名稱   |                 設置                  | 說明                     | 備註     |
| :-----------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|     `id`      |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp;                   | 自動編號 |
|    `name`     |   名稱   | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `guid`     |  識別碼  | `tinyint(1)`<br>`[null]`<br>`[null]`  | 預設為產品序號           | 產品序號 |
| `category_id` |   分類   | `varchar(64)`<br>`[null]`<br>`[idx]`  | good-category表          |          |
|    `price`    |   售價   |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `ramark`    | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `status`    |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
| `created_by`  | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `created_at`  | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |


資料表名稱: `good-spec`

中文名稱: 商品資料表

|     欄位     |    名稱    |                 設置                  | 說明                     | 備註     |
| :----------: | :--------: | :-----------------------------------: | ------------------------ | -------- |
|     `id`     |    編號    |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp;                   | 自動編號 |
| `spec_name`  |  規格名稱  | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `guid`    |   識別碼   | `tinyint(1)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
| `good_guid`  | 產品識別碼 | `tinyint(1)`<br>`[null]`<br>`[null]`  | 對應good->guid           | &nbsp;   |
|   `amount`   |    數量    |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `ramark`   |  備註(空)  |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `status`   |    狀態    | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
| `created_by` |  建立人員  | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `created_at` |  建立時間  | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

資料表名稱: `good-category`

中文名稱: 商品分類

|      欄位       |   名稱   |                 設置                  | 說明                     | 備註     |
| :-------------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|      `id`       |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp                    | 自動編號 |
| `category_name` | 分類名稱 | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|     `guid`      |  識別碼  | `tinyint(1)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
|    `ramark`     | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|    `status`     |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
|  `created_by`   | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `created_at`   | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

