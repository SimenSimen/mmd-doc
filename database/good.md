## 說明 <!-- omit in toc -->
此為商品相關表格。

## 資料表快速連結<!-- omit in toc -->

- [good|商品資料表](#good%e5%95%86%e5%93%81%e8%b3%87%e6%96%99%e8%a1%a8)
- [good-category|商品分類](#good-category%e5%95%86%e5%93%81%e5%88%86%e9%a1%9e)

#### good|商品資料表
#### good-category|商品分類

資料表名稱: `good`

中文名稱: 商品資料表

|     欄位     |   名稱   |                  設置                  | 說明                     | 備註     |
| :----------: | :------: | :------------------------------------: | ------------------------ | -------- |
|     `id`     |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                   | 自動編號 |
|    `name`    |   名稱   | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `guid`  |  使用者  |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 自行定義使用者           | &nbsp;   |
| `group_name` | 群組名稱 | `varchar(64)`<br>`[null]`<br>`[idx]`  | 分組紀錄                 | &nbsp;   |
|   `ramark`   | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`    | &nbsp;                   | &nbsp;   |
|   `status`   |   狀態   |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 失敗 <br> `1`: 成功 | &nbsp;   |
| `created_by` | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `created_at` | 建立時間 |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

資料表名稱: `good-category`

中文名稱: 商品分類

|     欄位     |   名稱   |                  設置                  | 說明                     | 備註     |
| :----------: | :------: | :------------------------------------: | ------------------------ | -------- |
|     `id`     |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                   | 自動編號 |
|    `name`    |   名稱   | `varchar(64)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `guid`  |  使用者  |  `tinyint(1)`<br>`[null]`<br>`[null]`  | 自行定義使用者           | &nbsp;   |
| `group_name` | 群組名稱 | `varchar(64)`<br>`[null]`<br>`[idx]`  | 分組紀錄                 | &nbsp;   |
|   `ramark`   | 備註(空) |   `text(0)`<br>`[null]`<br>`[null]`    | &nbsp;                   | &nbsp;   |
|   `status`   |   狀態   |  `tinyint(1)`<br>`[null]`<br>`[null]`  | `0`: 失敗 <br> `1`: 成功 | &nbsp;   |
| `created_by` | 建立人員 | `varchar(128)`<br>`[null]`<br>`[idx]` | &nbsp;                   | &nbsp;   |
| `created_at` | 建立時間 |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |

