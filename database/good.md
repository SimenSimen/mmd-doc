## 說明 <!-- omit in toc -->
此為商品相關表格。

## 資料表快速連結<!-- omit in toc -->

- [data-good|商品資料表](#data-good%e5%95%86%e5%93%81%e8%b3%87%e6%96%99%e8%a1%a8)
- [data-good-first-category|商品第一層類別表](#data-good-first-category%e5%95%86%e5%93%81%e7%ac%ac%e4%b8%80%e5%b1%a4%e9%a1%9e%e5%88%a5%e8%a1%a8)
- [data-good-second-category|商品第二層類別表](#data-good-second-category%e5%95%86%e5%93%81%e7%ac%ac%e4%ba%8c%e5%b1%a4%e9%a1%9e%e5%88%a5%e8%a1%a8)
- [data-good-third-category|商品第三層類別表](#data-good-third-category%e5%95%86%e5%93%81%e7%ac%ac%e4%b8%89%e5%b1%a4%e9%a1%9e%e5%88%a5%e8%a1%a8)

#### data-good|商品資料表

資料表名稱: `data_good`

中文名稱: 商品資料表

|       欄位        |   名稱   |                   設置                   | 說明                     | 備註     |
| :---------------: | :------: | :--------------------------------------: | ------------------------ | -------- |
|       `id`        |   編號   |    `int(20)`<br>`[null]`<br>`[pkey]`     | &nbsp;                   | 自動編號 |
|      `name`       |   名稱   |   `varchar(64)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|    `spec_name`    | 規格名稱 |  `varchar(64)`<br>`[null]`<br>`[null]`   | 顏色、尺寸等             | &nbsp;   |
|      `guid`       |  識別碼  |  `varchar (64)`<br>`[null]`<br>`[idx]`   | 產品通用條碼             | &nbsp;   |
|      `uuid`       | 產品編碼 | `varchar (64)`<br>`[null]`<br>`[unique]` | 由使用者命名之產品編碼   | &nbsp;   |
|   `category_id`   |   分類   |  `varchar(64)`<br>`[null]`<br>`[null]`   | good-category表          |          |
|      `price`      |   售價   |    `int(20)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
|  `special_price`  |   特價   |    `int(20)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
| `iamge_link_good` | 圖片連結 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   |
|     `ramark`      | 備註(空) |    `text(0)`<br>`[null]`<br>`[null]`     | &nbsp;                   | &nbsp;   |
|     `active`      | 啟用狀態 |   `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 停用 <br> `1`: 啟用 | &nbsp;   |
|   `created_by`    | 建立人員 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `created_at`    | 建立時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `updated_by`    | 更新人員 |  `varchar(128)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
|   `updated_at`    | 更新時間 |   `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |



#### data-good-first-category|商品第一層類別表

資料表名稱: `data_good_main_category`

中文名稱: 商品第一層類別表

|      欄位       |   名稱   |                 設置                  | 說明                     | 備註     |
| :-------------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|      `id`       |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp                    | 自動編號 |
| `category_name` | 分類名稱 | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `ramark`     | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|    `status`     |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
|  `created_by`   | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `created_at`   | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
|  `updated_by`   | 更新人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `updated_at`   | 更新時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

#### data-good-second-category|商品第二層類別表

資料表名稱: `data_good_main_category`

中文名稱: 商品第二層類別表

|      欄位       |   名稱   |                 設置                  | 說明                     | 備註     |
| :-------------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|      `id`       |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp                    | 自動編號 |
|   `parent_id`   |  父類ID  |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
| `category_name` | 分類名稱 | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `ramark`     | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|    `status`     |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
|  `created_by`   | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `created_at`   | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
|  `updated_by`   | 更新人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `updated_at`   | 更新時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

#### data-good-third-category|商品第三層類別表

資料表名稱: `data_good_main_category`

中文名稱: 商品第三層類別表

|      欄位       |   名稱   |                 設置                  | 說明                     | 備註     |
| :-------------: | :------: | :-----------------------------------: | ------------------------ | -------- |
|      `id`       |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`   | &nbsp                    | 自動編號 |
|   `parent_id`   |  父類ID  |   `int(20)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
| `category_name` | 分類名稱 | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
|    `ramark`     | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`   | &nbsp;                   | &nbsp;   |
|    `status`     |   狀態   | `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 刪除 <br> `1`: 存在 | &nbsp;   |
|  `created_by`   | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `created_at`   | 建立時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
|  `updated_by`   | 更新人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
|  `updated_at`   | 更新時間 | `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |