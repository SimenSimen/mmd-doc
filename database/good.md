## 說明 <!-- omit in toc -->
此為商品相關表格。

## 資料表快速連結<!-- omit in toc -->

- [data_good|商品資料表](#datagood%e5%95%86%e5%93%81%e8%b3%87%e6%96%99%e8%a1%a8)
- [data_good_spec|商品規格表](#datagoodspec%e5%95%86%e5%93%81%e8%a6%8f%e6%a0%bc%e8%a1%a8)
- [data_good_category|商品分類表](#datagoodcategory%e5%95%86%e5%93%81%e5%88%86%e9%a1%9e%e8%a1%a8)

#### data_good|商品資料表

資料表名稱: `data_good`

中文名稱: 商品資料表

|       欄位        |   名稱   |                   設置                   | 說明                     | 備註     |
| :---------------: | :------: | :--------------------------------------: | ------------------------ | -------- |
|       `id`        |   編號   |    `int(20)`<br>`[null]`<br>`[pkey]`     | &nbsp;                   | 自動編號 |
|      `name`       |   名稱   |   `varchar(64)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|      `guid`       |  識別碼  |  `varchar (64)`<br>`[null]`<br>`[idx]`   | 產品通用條碼             | &nbsp;   |
|      `uuid`       | 產品編碼 | `varchar (64)`<br>`[null]`<br>`[unique]` | 由使用者命名之產品編碼   | &nbsp;   |
|   `category_id`   |   分類   |  `varchar(64)`<br>`[null]`<br>`[null]`   | good-category表          |          |
|      `price`      |   售價   |    `int(20)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
| `iamge_link_good` | 圖片連結 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   |
|     `ramark`      | 備註(空) |    `text(0)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
|     `active`      | 啟用狀態 |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 停用 <br> `1`: 啟用 | &nbsp;   |
|   `created_by`    | 建立人員 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `created_at`    | 建立時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `updated_by`    | 更新人員 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `updated_at`    | 更新時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |

#### data_good_spec|商品規格表

資料表名稱: `data_good_spec`

中文名稱: 商品規格表

|     欄位     |    名稱    |                 設置                  | 說明                     | 備註     |
| :----------: | :--------: | :-----------------------------------: | ------------------------ | -------- |
|     `id`     |    編號    |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp;                   | 自動編號 |
| `spec_name`  |  規格名稱  | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `good_guid`  | 產品識別碼 | `tinyint(1)`<br>`[null]`<br>`[null]`  | 對應good->uuid           | &nbsp;   |
|   `amount`   |    數量    |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `ramark`   |  備註(空)  |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|   `status`   |    狀態    | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
| `created_by` |  建立人員  | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `created_at` |  建立時間  | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
| `updated_by` |  更新人員  | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `updated_at` |  更新時間  | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

#### data_good_category|商品分類表

資料表名稱: `data_good_category`

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
|  `updated_by`   | 更新人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `updated_at`   | 更新時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

