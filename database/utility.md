## 說明<!-- omit in toc -->

工具相關表格

## 資料表快速連結<!-- omit in toc -->

- [u-banner|橫幅資料表](#u-banner橫幅資料表)
- [u-upload|上傳檔案資料表](#u-upload上傳檔案資料表)
- [資料表](#資料表)

#### u-banner|橫幅資料表

資料表名稱: `u_banner`

中文名稱: 橫幅資料表

若需要區分多個使用者，則可以建立**關聯表**來規劃橫幅的使用權。

|     欄位     |     名稱     |                  設置                   | 說明                     | 備註     |
| :----------: | :----------: | :-------------------------------------: | ------------------------ | -------- |
|     `id`     |     編號     |    `int(10)`<br>`[null]`<br>`[pkey]`    | &nbsp;                   | 自動編號 |
|    `name`    |   名稱(空)   | `varchart(64)`<br>`[null]`<br>`[null]`  | &nbsp;                   | &nbsp;   |
| `image_link` |   圖片路徑   | `varchart(255)`<br>`[null]`<br>`[null]` | &nbsp;                   | &nbsp;   |
| `group_name` |   群組名稱   |  `varchart(64)`<br>`[null]`<br>`[idx]`  | 區分橫幅區塊。           | &nbsp;   |
|   `status`   |     狀態     |  `tinyint(1)`<br>`[null]`<br>`[null]`   | `0`: 停用 <br> `1`: 啟用 | &nbsp;   |
| `created_by` |   建立人員   | `varchart(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
| `edited_by`  | 更新人員(空) | `varchart(128)`<br>`[null]`<br>`[idx]`  | &nbsp;                   | &nbsp;   |
| `created_at` |   建立時間   |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |
| `updated_at` |   更新時間   |  `datetime(0)`<br>`[null]`<br>`[idx]`   | &nbsp;                   | &nbsp;   |

#### u-upload|上傳檔案資料表

名稱: `u_upload`

中文名稱: 上傳檔案資料表

|     欄位     |   名稱   |                  設置                  | 說明                                    | 備註     |
| :----------: | :------: | :------------------------------------: | --------------------------------------- | -------- |
|     `id`     |   編號   |   `int(20)`<br>`[null]`<br>`[pkey]`    | &nbsp;                                  | 自動編號 |
|    `name`    |   名稱   | `varchart(128)`<br>`[null]`<br>`[idx]` | &nbsp;                                  | &nbsp;   |
|    `path`    |   路徑   | `varchart(255)`<br>`[null]`<br>`[idx]` | &nbsp;                                  | &nbsp;   |
|    `ext`     |  副檔名  | `varchart(10)`<br>`[null]`<br>`[null]` | &nbsp;                                  | &nbsp;   |
|    `size`    |   大小   |     `int(20)`<br>`[0]`<br>`[null]`     | &nbsp;                                  | &nbsp;   |
|    `type`    |   類型   |   `tinyint(1)`<br>`[9]`<br>`[null]`    | `1`: 圖片 <br>`2`: office<br> `9`: 其他 | &nbsp;   |
| `created_by` | 建立人員 | `varchart(128)`<br>`[null]`<br>`[idx]` | &nbsp;                                  | &nbsp;   |
| `created_at` | 建立時間 |  `datetime(0)`<br>`[null]`<br>`[idx]`  | &nbsp;                                  | &nbsp;   |

#### 資料表